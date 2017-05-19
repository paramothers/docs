# Gradle

* first release in April 2008 ,it is also from apache, it is JVM based build tool                                                                                                                                                                                   
* it built having in mind both ant and maven , gradle has set of tasks those are **logically grouped into plugin**                                                                                                                                                  
* gradle adopt “configuration over convension” philosphy                                                                                                                                                                                                               
* dependency support not only for external library, but other project also can be a dependency                                                                                                                                                                    
* Each time you initiate a build, the JVM has to be started, Gradle’s dependencies have to be loaded into the class loader, and the project object model has to be constructed. This procedure usually takes a couple of seconds. Gradle daemon to the rescue       

# Gradle Selling Points

* Groovy used as build script , Gradle is based on DSL rather than xml file like ant or maven                                                                                                                                                                       
* it support smart exclude for tasks , gradle can run as deamon process , when we do build often                                                                                                                                                                    
* Gradle ship with its own Groovy library
* android development tool also going to be gradle based instead eclipse plugin.  it has support to REUSE existing ant build script.                                                                                                                                
* It’s not uncommon to face projects that use client-side languages like JavaScript that communicate with a mixed,  
   multilingual backend like Java, Groovy, and Scala, which in turn calls off to a C++ legacy application. 
* It’s all about the right tool for the job

# Lifecycle

1. Initialization
2. Configuration
3. Execution

# Different file

1. **build.gradle** , it consist of project, task and properties defintion
2. gradle.properties
3. settings.gradle

# Setup - environment variables

* **GRADLE\_HOME** , installation path of gradle. usaully unzipped directory
* **GRADLE\_OPTS** , this environment variable used when jvm settings affect only for Gradle

# Configuration block

to configure sub-product that is multimodule project  
subprojects  
repositories

# Gradle Built-in Tasks

| **description** | **Built in Tasks Nam3** | **options** |
| --- | --- | --- |
| to display all the tasks avilable in given build script | tasks | --all |
|  | help |  |
|  | components |  |
| display dependency of a project in tree | dependecies |  |
|  | dependecyInsite |  |
| it is used in multi-project, to list out sub projects | projects |  |
| it print all the properties available in build | properties |  |
|  | init |  |
|  | wrapper |  |
|  | buildNeeded |  |
|  | buildDependents |  |

# Task Flow Controller

1. dependsOn
2. finalizedBy
3. onlyIf
4. mustRunAfter
5. shouldRunAfter
6. defaultTasks

# Enhanced\(Custom\) tasks

Copy, Zip, Exec, Jar, compileJava, Test, Sync

# Maven & Gradle Comparison

|  |  |  |
| --- | --- | --- |
| **Featues** | **Gradle** | **Maven** |
|  |  |  |
| build script | Grooovy | xml |
| core implemeted | As plugin | as plugin |
| unit of work | task | Goal \( mojo \) |
| archetyp support | No \( 1.7 \) | yes |
| site support | No \( 1.7 \) | yes |
| run spcecifc unit test or class or package | yes | no |
| Wrapper script support, | yes | No |
| indexing given \(maven\) repository | yes | No |
| assembly of app | easy | difficult, need separate xml file need |
| easy to refer private libraries from file system | easy | diffucult, need to push all the jar into local .m2 manually |

# session for others

|  |  |
| --- | --- |
| plugin |  |
| task |  |
| configuration options |  |
| action |  |
|  |  |
|  | install |
|  | wrapper |
|  | IDE |



