[Linux Page](linuxindex.html)

------------------------------------------------------------------------

|                                                                                                                             |                  |                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------|------------------|-----------------------------------------------------------------|
| I classified the linux commands basic which used for regular use and tool specific commands                                 |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
| in linux all are files even hardware and directory                                                                          |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
| **description**                                                                                                             | **command**      | **USED option instead of complete list**                        |
|                                                                                                                             |                  |                                                                 |
| change the shell                                                                                                            | chsh             |                                                                 |
| list the command history of shell                                                                                           | fc               | l                                                               |
| recently used commands                                                                                                      | history          |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
| disk free information                                                                                                       | df               | k                                                               |
| size of current folder ( disk usage )                                                                                       | du -hs           |                                                                 |
| to know who are else logged into system                                                                                     | finger           |                                                                 |
|                                                                                                                             |                  |                                                                 |
| short version of a command                                                                                                  | info             |                                                                 |
| Display detail help content of a command                                                                                    | man              | -k                                                              |
|                                                                                                                             |                  |                                                                 |
| used to display the large file                                                                                              | More & less      | it is do scroll bar task of windows                             |
| display first or last given no. Of lines of file                                                                            | Head & tail      |                                                                 |
| display content of file                                                                                                     | cat              |                                                                 |
| display content type of a file                                                                                              | file             |                                                                 |
|                                                                                                                             | basename         |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
| small editor                                                                                                                | nano             |                                                                 |
| basic editor                                                                                                                | vi               |                                                                 |
|                                                                                                                             |                  | Xmanager – tool for connect unix                                |
| change the password                                                                                                         | passwd           | vmc server install in linux , and use client in window machine. |
| add one directory in a variable ( usully PATH )                                                                             | export           |                                                                 |
|                                                                                                                             |                  |                                                                 |
| desktop calucator                                                                                                           | dc               |                                                                 |
| more complex float or double artimetic operation                                                                            | bc               |                                                                 |
| expression evaluation                                                                                                       | expr             |                                                                 |
|                                                                                                                             |                  |                                                                 |
| present working directory                                                                                                   | pwd              |                                                                 |
|                                                                                                                             | cd               |                                                                 |
|                                                                                                                             | ls               |                                                                 |
| copy file                                                                                                                   | cp               |                                                                 |
|                                                                                                                             | mv               |                                                                 |
|                                                                                                                             | rm               |                                                                 |
|                                                                                                                             | echo             | n                                                               |
| display all the command who are aliased                                                                                     | alias            |                                                                 |
|                                                                                                                             | sort             |                                                                 |
|                                                                                                                             | uniq             |                                                                 |
|                                                                                                                             | spell            |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
| search a given file in computer ( it check all dir/subdirecory )                                                            | find             |                                                                 |
| quick search in system database for given file ( check only PATH value )                                                    | locate           |                                                                 |
| search a line in file for given pattern                                                                                     | grep             | -n,-v,-c,-i                                                     |
| extended grep                                                                                                               | egrep            |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
| to list name of installed package, it is debian specific                                                                    | dpkg -l          | RedHad and suse are mostly used in industries                   |
| to list name of groups in system                                                                                            | groups           | it just a mechanism to manage the users                         |
|                                                                                                                             |                  |                                                                 |
| used to edit etc/crontab file,                                                                                              | crontab          |                                                                 |
| it is daemon thread, check periodically etc/crontab file                                                                    | cron             |                                                                 |
|                                                                                                                             |                  |                                                                 |
| to check the file system.                                                                                                   | fsck             |                                                                 |
| to know path of a command (that is existence of command in os )                                                             | which            | which ls/cd/mv/etc.                                             |
| to know all path of a command                                                                                               | whereis          |                                                                 |
| It is mainly used for abbreviating a system command, or for adding default arguments to a regularly used command            | alias            |                                                                 |
|                                                                                                                             |                  |                                                                 |
| to list name of process                                                                                                     | ps               | e, f, a, u, x                                                   |
| display the process in tree structure                                                                                       | pstree           |                                                                 |
| display top 5 proecess                                                                                                      | top              |                                                                 |
| show virutual memory statuss                                                                                                | vmstat           |                                                                 |
|                                                                                                                             |                  |                                                                 |
| to know the command information                                                                                             | apropos          |                                                                 |
| to know how long a given command executed                                                                                   | time &lt;cmd&gt; |                                                                 |
|                                                                                                                             |                  |                                                                 |
| to lanuch another command                                                                                                   | exec             |                                                                 |
| config network devices                                                                                                      | ifconfig         |                                                                 |
| to reflect configuration file changes to current session without logout                                                     | source           |                                                                 |
| shell sleep for given seconds                                                                                               | sleep            |                                                                 |
| to terminate shell script execution                                                                                         | exit             |                                                                 |
| make is command to create binary file ( like ant )                                                                          | make             |                                                                 |
| always return true used in shell scripting (Built in command in shell itself . No binary file for this command)             | 1                |                                                                 |
| always return true used in shell scripting (Built in command in shell itself . No binary file for this command)             | 0                |                                                                 |
| Built in command in shell itself for test numeric, string and file comparision . No binary file for this command in system. | test             |                                                                 |
| it used to identity shell built in commands like true, false, test, \[, etc. type itself built in command                   | type             | ex: type test, type true                                        |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             | tr               |                                                                 |
| octal dump                                                                                                                  | od               | a                                                               |
| diplay only GLOBAL the environment variable                                                                                 | env              |                                                                 |
| diplay only GLOBAL the environment variable                                                                                 | printenv         |                                                                 |
| diplay all LOCAL as well as ENVIRONMENT (exported ) the environment variable                                                | set              |                                                                 |
| just remove a variable name itself.                                                                                         | unset            |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             | cut              |                                                                 |
| used to find/replace/search on a given file and create new file from output                                                 | sed              | e                                                               |
| another popular stream editor like sed                                                                                      | awk/gawk         |                                                                 |
| another popular stream editor like sed                                                                                      | perl             |                                                                 |
|                                                                                                                             |                  |                                                                 |
| to send message to all user who logged into system                                                                          | wall             |                                                                 |
| to send message to a particular user                                                                                        | write            |                                                                 |
|                                                                                                                             |                  |                                                                 |
| archieve utility                                                                                                            | tar              |                                                                 |
| compress and expand utility                                                                                                 | zcat             |                                                                 |
| data dumper                                                                                                                 | dd               |                                                                 |
|                                                                                                                             |                  |                                                                 |
|                                                                                                                             |                  |                                                                 |
| display the OS name, processor, mother board architecure, etc,                                                              | uname            | o, hardware-platform, p,a, all                                  |
| administrative command                                                                                                      | who              |                                                                 |
| who are all logged in, administrative command                                                                               | w                |                                                                 |
| display the current user                                                                                                    | whoami           |                                                                 |
|                                                                                                                             |                  |                                                                 |
| make many file to single file                                                                                               | tar              | c, f                                                            |
| compress while creating archieve file                                                                                       | compress         |                                                                 |
| uncompress while extracting archieve file                                                                                   | uncompress       |                                                                 |
| it is best compare with compress command. It take a tar file to compress                                                    | gzip             |                                                                 |
| it is lates of gzip                                                                                                         | bzip2            |                                                                 |
| to un compress a compressed file by gzip                                                                                    | gunzip           |                                                                 |
| it has both create and compress the archieve file. It useful to if file used in window os                                   | zip              |                                                                 |
|                                                                                                                             |                  |                                                                 |
| test command's alternative                                                                                                  | \[               |                                                                 |
| truncate the file                                                                                                           | &gt;or : &gt;    |                                                                 |
| continuation for command line                                                                                               | \\               |                                                                 |
| input rediirect from a file                                                                                                 | &lt;             |                                                                 |
| redirect output and append if a file alreay                                                                                 | &gt;&gt;         |                                                                 |
| redirect output and truncate if file already                                                                                | &gt;             |                                                                 |
| recirect output of a command to ANOTHER COMMAND                                                                             | |                |                                                                 |
| to run a command in background mode                                                                                         | &                |                                                                 |
| current process id                                                                                                          | $$               |                                                                 |
| recent background process id                                                                                                | $!               |                                                                 |
| recent command's exit status                                                                                                | $?               |                                                                 |