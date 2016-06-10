
Gradle
======
                                                                                                                                                                                                                                                                   
 + first release in April 2008 ,it is also from apache, it is JVM based build tool                                                                                                                                                                                   
 + Groovy used as build script , Gradle is based on DSL rather than xml file like ant or maven                                                                                                                                                                       
 + it built having in mind both ant and maven , gradle has set of tasks those are **logically grouped into plugin**                                                                                                                                                  
 + android development tool also going to be gradle based instead eclipse plugin.  it has support to REUSE existing ant build script.                                                                                                                                
 + gradle adopt “configuration over convension” philosphy                                                                                                                                                                                                               
 + dependency support not only for external library, but other project also can be a dependency                                                                                                                                                                      
 + It’s not uncommon to face projects that use client-side languages like JavaScript that communicate with a mixed,  
    multilingual backend like Java, Groovy, and Scala, which in turn calls off to a C++ legacy application. 
 + It’s all about the right tool for the job
 + it support smart exclude for tasks , gradle can run as deamon process , when we do build often                                                                                                                                                                    
 + Each time you initiate a build, the JVM has to be started, Gradle’s dependencies have to be loaded into the class loader, and the project object model has to be constructed. This procedure usually takes a couple of seconds. Gradle daemon to the rescue       


Setup
=====     
 
+ GRADLE\_HOME 
+ GRADLE\_OPTS 

Configuration block
===================

to configure sub-product that is multimodule project
subprojects
repositories

command Options
===============

|                                                                      |        |                          |                         |
|----------------------------------------------------------------------|--------|--------------------------|-------------------------|
| gradle task syntax                                                   | gradle |                          |                         |
| to display the all the commad line options                           |        | –help                    |                         |
| show particular task usage detail                                    |        | -help –task &lt;task&gt; |                         |
|                                                                      |        |                          |                         |
| to execlude a task, and its dependent task also                      |        | -x                       | &lt;taskName&gt;        |
| give command line option of Gradle command                           |        | -?/-h/--help             |                         |
| to specify build file name explicitly                                |        | -b/--build-file          | &lt;build file name&gt; |
| run the build in offline                                             |        | --offline                |                         |
|                                                                      |        |                          |                         |
| to add system variabe                                                |        | -D/--system-prop         |                         |
| add custom propeties                                                 |        | -p/--project-prop        |                         |
|                                                                      |        |                          |                         |
| to run a particular task in quite mode, only sysout are coming out   |        | -q                       | &lt;taskName&gt;        |
| it give more logs                                                    |        | -i/--info                |                         |
| give about track trace                                               |        | -s/--stacktrace          |                         |
|                                                                      |        |                          |                         |
| to run gradle jvm process as deamon                                  |        | --deamon                 |                         |
| run build as non-deamon                                              |        | --no-deamon              |                         |
| stop deamon gradle process                                           |        | --stop                   |                         |
|                                                                      |        |                          |                         |
| run build in offline mode                                            |        | --offline                |                         |
|                                                                      |        | --refresh-dependencies   |                         |
|                                                                      |        |                          |                         |
|                                                                      |        | -u/--no-search-upword    |                         |
|                                                                      |        | -c/settings-file         |                         |
|                                                                      |        |                          |                         |
| partial build                                                        |        | -a/--no-rebuild          |                         |
|                                                                      |        |                          |                         |
| show as much as possible errors in build file                        |        | --continue               |                         |
|                                                                      |        |                          |                         |
| display all the subproject of multi-module project                   |        | --projects               |                         |
|                                                                      |        |                          |                         |
|                                                                      |        | -profile                 |                         |
|                                                                      |        |                          |                         |
| to Gui view for build file, it is really useful as a tool for gradle |        | -gui                     |                         |
| force to compile script, though it can use from cache                |        | --recompile-scripts      |                         |

Tasks
=====

|                                                         |                         |             |
|---------------------------------------------------------|-------------------------|-------------|
| **description**                                         
                                                          | **Built in Tasks Nam3** | **options** |
| to display all the tasks avilable in given build script | tasks                   | --all       |
|                                                         | help                    |             |
|                                                         | components              |             |
| display dependency of a project in tree                 | dependecies             |             |
|                                                         | dependecyInsite         |             |
| it is used in multi-project, to list out sub projects   | projects                |             |
| it print all the properties available in build          | properties              |             |
|                                                         |                         |             |
|                                                         | init                    |             |
|                                                         | wrapper                 |             |
|                                                         |                         |             |
|                                                         | buildNeeded             |             |
|                                                         | buildDependents         |             |


Plugin & Its Tasks
==================

|                                                              |             |                    |
|--------------------------------------------------------------|-------------|--------------------|
                                                               | **Plugin**  | **available Task** |
| for java compile, package, give default structor for project | java        | build              |
| to avoid running test case                                   |             | jar                |
|                                                              |             | test               |
|                                                              |             | check              |
|                                                              |             | assemble           |
|                                                              | war         | war                |
|                                                              |             |                    |
|                                                              | jetty       | jettyRun           |
| make easy to build and run the application                   | application |                    |
|                                                              |             |                    |



Gradle API
==========

|                                  |                          |                        |                    |                                 |     |     |
|----------------------------------|--------------------------|------------------------|--------------------|---------------------------------|-----|-----|
| rep. Project of grale build file | Project                  |                        |                    |                                 |     |     |
|                                  |                          | Gradle                 | TaskExecutionGraph |                                 |     |     |
|                                  |                          | ConfigurationContainer | Configuration      |                                 |     |     |
|                                  |                          | DependencyHandler      | Dependency         |                                 |     |     |
| for dependency graph             |                          | ResolutionResult       |                    |                                 |     |     |
|                                  |                          |                        |                    |                                 |     |     |
|                                  |                          | RepositoryHandler      |                    |                                 |     |     |
|                                  |                          |                        | ArtifactRepository |                                 |     |     |
|                                  |                          |                        |                    | MavenArtifactRepository         |     |     |
|                                  |                          |                        |                    | FlatDirectoryArtifactRepository |     |     |
|                                  |                          |                        |                    | IvyArtifactRepository           |     |     |
|                                  |                          |                        |                    |                                 |     |     |
|                                  | Task                     | DefaultTask            |                    |                                 |     |     |
|                                  |                          |                        |                    | doLast()                        |     |     |
|                                  |                          |                        |                    | doFirst()                       |     |     |
|                                  |                          |                        |                    | onlyIf()                        |     |     |
|                                  |                          |                        |                    |                                 |     |     |
|                                  |                          |                        |                    | didWork                         |     |     |
|                                  |                          |                        |                    | enable                          |     |     |
|                                  |                          |                        |                    | path                            |     |     |
|                                  |                          |                        |                    | logger                          |     |     |
|                                  |                          |                        |                    | logging                         |     |     |
|                                  |                          |                        |                    | description                     |     |     |
|                                  |                          |                        |                    | temporaryDir                    |     |     |
|                                  |                          |                        |                    |                                 |     |     |
|                                  |                          |                        | TaskInputs         |                                 |     |     |
|                                  |                          |                        | TaskOutputs        |                                 |     |     |
|                                  |                          |                        | Test               | TestLoggingContainer            |     |     |
| it used to locate a task         | TaskContainer            |                        |                    |                                 |     |     |
|                                  |                          |                        |                    |                                 |     |     |
|                                  |                          |                        |                    |                                 |     |     |
|                                  | Settings                 | ProjectDescriptor      |                    |                                 |     |     |
|                                  |                          |                        |                    |                                 |     |     |
|                                  | AntBuilder               |                        |                    |                                 |     |     |
|                                  |                          |                        |                    |                                 |     |     |
| rep. Build script file           | Script                   |                        |                    |                                 |     |     |
|                                  | ExtraPropertiesExtension |                        |                    |                                 |     |     |



Maven & Gradle Comparision
==========================

|                                            |            |               |
|--------------------------------------------|------------|---------------|
| **Featues**                                | **Gradle** | **Maven**     |
|                                            |            |               |
| build script                               | Grooovy    | xml           |
| core implemeted                            | As plugin  | as plugin     |
| unit of work                               | task       | Goal ( mojo ) |
| archetyp support                           | No ( 1.7 ) | yes           |
| site support                               | No ( 1.7 ) | yes           |
| run spcecifc unit test or class or package | yes        | no            |
| Wrapper script support,                    | yes        | No            |
| indexing given (maven) repository          | yes        | No            |
|                                            |            |               |
|                                            |            |               |
|                                            |            |               |
|                                            |            |               |
|                                            |            |               |


session for others
==================

|                       |         |
|-----------------------|---------|
| plugin                |         |
| task                  |         |
| configuration options |         |
| action                |         |
|                       |         |
|                       | install |
|                       | wrapper |
|                       | IDE     |