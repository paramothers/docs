
command Options
===============

|                                                                      |        |                          |                         |
|----------------------------------------------------------------------|--------|--------------------------|-------------------------|
| gradle task syntax                                                   | gradle |                          |                         |
| to display the all the commad line options                           |        | –help                    |                         |
| show particular task usage detail                                    |        | -help –task &lt;task&gt; |                         |
| to execlude a task, and its dependent task also                      |        | -x                       | &lt;taskName&gt;        |
| give command line option of Gradle command                           |        | -?/-h/--help             |                         |
| to specify build file name explicitly                                |        | -b/--build-file          | &lt;build file name&gt; |
| run the build in offline                                             |        | --offline                |                         |
| to add system variabe                                                |        | -D/--system-prop         |                         |
| add custom propeties                                                 |        | -p/--project-prop        |                         |
| to run a particular task in quite mode, only sysout are coming out   |        | -q                       | &lt;taskName&gt;        |
| it give more logs                                                    |        | -i/--info                |                         |
| give about track trace                                               |        | -s/--stacktrace          |                         |
| to run gradle jvm process as deamon                                  |        | --deamon                 |                         |
| run build as non-deamon                                              |        | --no-deamon              |                         |
| stop deamon gradle process                                           |        | --stop                   |                         |
| run build in offline mode                                            |        | --offline                |                         |
|                                                                      |        | --refresh-dependencies   |                         |
|                                                                      |        | -u/--no-search-upword    |                         |
|                                                                      |        | -c/settings-file         |                         |
| To force to run the all the sequential task, though it up-to-date    |        | --rerun-tasks            |                         |
| partial build                                                        |        | -a/--no-rebuild          |                         |
| show as much as possible errors in build file                        |        | --continue               |                         |
| display all the subproject of multi-module project                   |        | --projects               |                         |
|                                                                      |        | -profile                 |                         |
| to Gui view for build file, it is really useful as a tool for gradle |        | -gui                     |                         |
| force to compile script, though it can use from cache                |        | --recompile-scripts      |                         |
