

Gradle API
==========

|                                       |                          |                        |                    |                                 |
|---------------------------------------|--------------------------|------------------------|--------------------|---------------------------------|
| rep. Project of grale build file      | Project                  |                        |                    |                                 |
|                                       |                          | Gradle                 | TaskExecutionGraph |                                 |
|                                       |                          | ConfigurationContainer | Configuration      |                                 |
|                                       |                          | DependencyHandler      | Dependency         |                                 |
| for dependency graph                  |                          | ResolutionResult       |                    |                                 |
|                                       |                          |                        |                    |                                 |
|                                       |                          | RepositoryHandler      |                    |                                 |
|                                       |                          |                        | ArtifactRepository |                                 |
|                                       |                          |                        |                    | MavenArtifactRepository         |
|                                       |                          |                        |                    | FlatDirectoryArtifactRepository |
|                                       |                          |                        |                    | IvyArtifactRepository           |
|                                       | Task                     | DefaultTask            |                    |                                 |
|                                       |                          |                        | TaskInputs         |                                 |
|                                       |                          |                        | TaskOutputs        |                                 |
|                                       |                          |                        | Test               | TestLoggingContainer            |
| it used to locate a task              | TaskContainer            |                        |                    |                                 |
|                                       |                          |                        |                    |                                 |
|                                       |                          |                        |                    |                                 |
| represents settings.gradle file       | Settings                 | ProjectDescriptor      |                    |                                 |
|                                       |                          |                        |                    |                                 |
| to migrate ant build script to gradle | AntBuilder               |                        |                    |                                 |
|                                       |                          |                        |                    |                                 |
| rep. Build script file                | Script                   |                        |                    |                                 |
|                                       | ExtraPropertiesExtension |                        |                    |                                 |
|                                       |                          |                        |                    |                                 |
