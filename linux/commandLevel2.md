[Linux Page](linuxindex.html)

------------------------------------------------------------------------

Overview
========

[File management](#table0)
 [directory managment](#table1)
 [Shell](#table2)
 [archieve managment](#table3)
 [search commands](#table4)
 [System info](#table5)
 [Process](#table6)
 [Schedule](#table7)
 [help](#table8)
 [Maths](#table9)
 [User](#table10)
 [Hardware](#table11)

------------------------------------------------------------------------

1: *File management*
====================

|                                                  |             |                                     |
|--------------------------------------------------|-------------|-------------------------------------|
| used to display the large file                   | More & less | it is do scroll bar task of windows |
|                                                  | pg          |                                     |
| display first or last given no. Of lines of file | Head & tail |                                     |
| display content of file                          | cat         |                                     |
|                                                  |             |                                     |
| sort the file content                            | sort        |                                     |
| remove duplicate line of given file              | uniq        |                                     |
| create a empty file in given name                | touch       | c                                   |
| display content type of a file                   | file        |                                     |
| get only file without path                       | basename    |                                     |
|                                                  |             |                                     |
|                                                  |             |                                     |
|                                                  | mv          |                                     |
|                                                  | rm          |                                     |
| copy file                                        | cp          |                                     |
|                                                  |             |                                     |
|                                                  |             |                                     |
| change permission on a file                      | chmod       |                                     |
| change group of a file                           | chgrp       |                                     |
| change owner of a file( only super user )        | chown       |                                     |

------------------------------------------------------------------------

2: *directory managment*
========================

|                           |       |
|---------------------------|-------|
| present working directory | pwd   |
| change directory          | cd    |
| list directory            | ls    |
| create directory          | mkdir |
| delete directory          | rmdir |

------------------------------------------------------------------------

3: *Shell*
==========

|                                                                                                                             |               |                          |
|-----------------------------------------------------------------------------------------------------------------------------|---------------|--------------------------|
| change the default login shell                                                                                              | chsh          |                          |
| list the command history of shell                                                                                           | fc            | l                        |
| recently used commands                                                                                                      | history       |                          |
| I am not clear                                                                                                              | stty          |                          |
|                                                                                                                             |               |                          |
| to record current session in a file ( it will useful to give another developer wht to do )                                  | Script & exit | -a                       |
|                                                                                                                             |               |                          |
|                                                                                                                             |               |                          |
| to lanuch another command                                                                                                   | exec          |                          |
| config network devices                                                                                                      | ifconfig      |                          |
| to reflect configuration file changes to current session without logout                                                     | source        |                          |
| shell sleep for given seconds                                                                                               | sleep         |                          |
| to terminate shell script execution                                                                                         | exit          |                          |
| make is command to create binary file ( like ant )                                                                          | make          |                          |
|                                                                                                                             |               |                          |
| always return true used in shell scripting (Built in command in shell itself . No binary file for this command)             | 1             |                          |
| always return true used in shell scripting (Built in command in shell itself . No binary file for this command)             | 0             |                          |
|                                                                                                                             | case          |                          |
|                                                                                                                             | while         |                          |
|                                                                                                                             | for           |                          |
|                                                                                                                             | if            |                          |
| Built in command in shell itself for test numeric, string and file comparision . No binary file for this command in system. | test          |                          |
| it used to identity shell built in commands like true, false, test, \[, etc. type itself built in command                   | type          | ex: type test, type true |
| it is used to define a function                                                                                             | declare       | f                        |
| null command ( colon )                                                                                                      | :             |                          |
| execute shell script file ( dot )                                                                                           | .             |                          |
| change directory to home directory ( note. No argument )                                                                    | cd            |                          |
|                                                                                                                             | echo          |                          |
|                                                                                                                             | eval          |                          |
|                                                                                                                             | exec          |                          |
| exit the current shell                                                                                                      | exit          |                          |
| to make avilable a variable for sub shell                                                                                   | export        |                          |
|                                                                                                                             | pwd           |                          |
|                                                                                                                             | read          |                          |
|                                                                                                                             | set           |                          |
|                                                                                                                             | trap          |                          |
| all the user defined alias stored in .bashrc file for bash shell                                                            | alias         |                          |
|                                                                                                                             |               |                          |
|                                                                                                                             |               |                          |
|                                                                                                                             |               |                          |
|                                                                                                                             |               |                          |
| test command's alternative                                                                                                  | \[            |                          |
| truncate the file                                                                                                           | &gt;or : &gt; |                          |
| continuation for command line                                                                                               | \\            |                          |
| input rediirect from a file                                                                                                 | &lt;          |                          |
| redirect output and append if a file alreay                                                                                 | &gt;&gt;      |                          |
| redirect output and truncate if file already                                                                                | &gt;          |                          |
| recirect output of a command to ANOTHER COMMAND                                                                             | |             |                          |
| to run a command in background mode                                                                                         | &             |                          |
| current process id                                                                                                          | $$            |                          |
| recent background process id                                                                                                | $!            |                          |
| recent command's exit status                                                                                                | $?            |                          |
| diplay only GLOBAL the environment variable                                                                                 | env           |                          |
| diplay only GLOBAL the environment variable                                                                                 | printenv      |                          |
| diplay all LOCAL as well as ENVIRONMENT (exported ) the environment variable                                                | set           |                          |
| Make unavailable variable name and any user defined function                                                                | unset         |                          |
| diplay only GLOBAL the environment variable                                                                                 | env           |                          |

------------------------------------------------------------------------

4: *archieve managment*
=======================

|                                                                                           |            |      |
|-------------------------------------------------------------------------------------------|------------|------|
| make many file to single file                                                             | tar        | c, f |
| compress and expand utility                                                               | zcat       |      |
| data dumper                                                                               | dd         |      |
| compress while creating archieve file                                                     | compress   |      |
| uncompress while extracting archieve file                                                 | uncompress |      |
| it is best compare with compress command. It take a tar file to compress                  | gzip       |      |
| it is lates of gzip                                                                       | bzip2      |      |
| to un compress a compressed file by gzip                                                  | gunzip     |      |
| it has both create and compress the archieve file. It useful to if file used in window os | zip        |      |

------------------------------------------------------------------------

5: *search commands*
====================

|                                                                             |          |         |
|-----------------------------------------------------------------------------|----------|---------|
| search a given file in computer ( it check all dir/subdirecory )            | find     |         |
| quick search in system database for given file ( check only PATH value )    | locate   |         |
|                                                                             |          |         |
|                                                                             |          |         |
| search a line in file for given regular expression                          | grep     | I,v,n,c |
| extended grep                                                               | egrep    |         |
| used to search for given TEXT for given files                               | fgrep    | I,v,n   |
| used to find/replace/search on a given file and create new file from output | sed      | e       |
| another popular stream editor like sed                                      | awk/gawk |         |
| find printable string in a file                                             | strings  |         |

------------------------------------------------------------------------

6: *System info*
================

|                                                          |         |                                               |
|----------------------------------------------------------|---------|-----------------------------------------------|
| to list name of installed package, it is debian specific | dpkg -l | RedHad and suse are mostly used in industries |
|                                                          |         |                                               |
| who are all logged in, administrative command            | Who & W |                                               |
| who are all logged in, administrative command            | finger  |                                               |
| display the current user                                 | whoami  |                                               |
|                                                          |         |                                               |
| to log off from system                                   | logout  |                                               |
|                                                          |         |                                               |
| to know how long a given command executed                | time    |                                               |

------------------------------------------------------------------------

7: *Process*
============

|                                       |        |               |
|---------------------------------------|--------|---------------|
| to list name of process               | ps     | e, f, a, u, x |
|                                       | kill   | l             |
| display the process in tree structure | pstree |               |
| display top 5 proecess                | top    |               |
| show virutual memory statuss          | vmstat |               |

------------------------------------------------------------------------

8: *Schedule*
=============

|                                                          |         |
|----------------------------------------------------------|---------|
| used to edit etc/crontab file,                           | crontab |
| it is daemon thread, check periodically etc/crontab file | cron    |

------------------------------------------------------------------------

9: *help*
=========

|                                                                 |         |                     |
|-----------------------------------------------------------------|---------|---------------------|
| to know path of a command (that is existence of command in os ) | which   | which ls/cd/mv/etc. |
| to know all path of a command ( binary, source, man page )      | whereis | s,b,m               |
| to know the command information                                 | apropos |                     |
| short version of a command                                      | info    |                     |
| Display detail help content of a command                        | man     | -k                  |

------------------------------------------------------------------------

10: *Maths*
===========

|                                                  |      |
|--------------------------------------------------|------|
| desktop calucator ( like our calc )              | dc   |
| more complex float or double artimetic operation | bc   |
| expression evaluation                            | expr |

------------------------------------------------------------------------

11: *User*
==========

|                                  |        |                                                                 |
|----------------------------------|--------|-----------------------------------------------------------------|
| change the password              | passwd | vmc server install in linux , and use client in window machine. |
| id of current user               | id     | it just a mechanism to manage the users                         |
| to list name of groups in system | groups | it just a mechanism to manage the users                         |

------------------------------------------------------------------------

12: *Hardware*
==============

|                                                                |          |                                |
|----------------------------------------------------------------|----------|--------------------------------|
| disk free information of each disk or partition                | df       |                                |
| size of current folder / file                                  | du -hs   |                                |
| to check the file system.                                      | fsck     |                                |
|                                                                |          |                                |
| display the OS name, processor, mother board architecure, etc, | uname    | o, hardware-platform, p,a, all |
| give name of computer                                          | hostname |                                |
