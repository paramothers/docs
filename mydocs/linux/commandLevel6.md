###Command usage idea


|                    |                                                                   |
|--------------------|-------------------------------------------------------------------|
| ls command usage   | ls -l \* ( to display all the directory along with its content )  |
| file command usage | File \* ( to display type of all the child of current directory ) |
|                    | File \*.jar ( to display info about the jar files only )          |
|                    | File \* | grep link                                               |

------------------------------------------------------------------------

###Permission

|                                           |       |     |
|-------------------------------------------|-------|-----|
| change permission on a file               | chmod | R   |
| change group of a file                    | chgrp |     |
| change owner of a file( only super user ) | chown |     |

------------------------------------------------------------------------

###File

|                                                      |          |                                     |                                                          |
|------------------------------------------------------|----------|-------------------------------------|----------------------------------------------------------|
|                                                      | more     |                                     |                                                          |
| used to view the large file                          | less     | it is do scroll bar task of windows |                                                          |
|                                                      | pg       |                                     |                                                          |
|                                                      | tail     | f                                   |                                                          |
| **display first or last given no. Of lines of file** | head     |                                     |                                                          |
| **display content of file**                          | cat      |                                     |                                                          |
|                                                      |          |                                     |                                                          |
| sort the file content                                | sort     |                                     |                                                          |
| remove duplicate line of given file                  | uniq     |                                     |                                                          |
| create a empty file in given name                    | touch    | c                                   | if it file/folder already exist, those timestamp updated |
| display content type of a file                       | file     |                                     |                                                          |
| get only file without path                           | basename |                                     |                                                          |
|                                                      |          |                                     |                                                          |
|                                                      |          |                                     |                                                          |
| move/rename files/directory                          | mv       |                                     |                                                          |
| remove file/directory                                | rm       |                                     |                                                          |
| copy file                                            | cp       |                                     |                                                          |

------------------------------------------------------------------------

###directory

|                                              |       |                                                                                                                                     |
|----------------------------------------------|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| present working directory                    | pwd   |                                                                                                                                     |
| change directory                             | cd    |                                                                                                                                     |
| list directory & files \[LS – list storage\] | ls    | a(also display hidden files ), i ( i-node no. ), p ( display directory name with slash ), R ( recursively display of sub direcory ) |
| create directory                             | mkdir |                                                                                                                                     |
| delete directory                             | rmdir |                                                                                                                                     |

------------------------------------------------------------------------

###Shell

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
| recent process or command's exit status                                                                                     | $?            |                          |
|                                                                                                                             |               |                          |
| diplay only GLOBAL the environment variable                                                                                 | env           |                          |
| diplay only GLOBAL the environment variable                                                                                 | printenv      |                          |
| diplay all LOCAL as well as ENVIRONMENT (exported ) the environment variable                                                | set           |                          |
| Make unavailable variable name and any user defined function                                                                | unset         |                          |
| diplay only GLOBAL the environment variable                                                                                 | env           |                          |

------------------------------------------------------------------------

###archieve
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

###search

|                                                                                                           |          |                               |
|-----------------------------------------------------------------------------------------------------------|----------|-------------------------------|
| search a given file in computer using metadata but not by content of file( it check all dir/subdirecory ) | find     | -name, -mtime, Schedule.C9wat |
| quick search in system database for given file ( check only PATH value )                                  | locate   |                               |
|                                                                                                           |          |                               |
|                                                                                                           |          |                               |
| search a line in file for given regular expression                                                        | grep     | I,v,n,c                       |
| extended grep                                                                                             | egrep    |                               |
| used to search for given TEXT for given files                                                             | fgrep    | I,v,n                         |
| translate SINGLE charactors usually, special \\n, \\t, or any alphanumic charactor                        | tr       |                               |
|                                                                                                           |          |                               |
| used to find/replace/search MORE THAN One Charactor                                                       | sed      | e                             |
| another popular stream editor like sed                                                                    | awk/gawk |                               |
| find printable string in a file                                                                           | strings  |                               |

------------------------------------------------------------------------

###System info
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

###Process
|                                             |              |               |        |
|---------------------------------------------|--------------|---------------|--------|
| to list name of process                     | ps           | e, f, a, u, x | forest |
| to send ANY singal to running process       | kill         | l             |        |
|                                             | killall      |               |        |
| display the process in tree structure       | pstree       |               |        |
| display top 5 process usage of cpu          | top          |               |        |
| show virutual memory statuss                | vmstat       |               |        |
|                                             |              |               |        |
| to bring a background process to forgroound | fg           |               |        |
| to move a foreground process to background  | bg           |               |        |
| to run any process in background            | \[command\]& |               |        |
| size of memory segment of a process         | size         |               |        |
| usage of shared library                     | ldd          |               |        |
| i dont know                                 | ulimit       |               |        |

------------------------------------------------------------------------

###Schedule
|                                                                 |         |     |
|-----------------------------------------------------------------|---------|-----|
| used to edit etc/crontab file,                                  | crontab | l,e |
| it is process thread, check periodically etc/crontab file       | cron    |     |
|                                                                 |         |     |
| run a task at specfic (run only one) time, it is deamon process | atd     |     |
|                                                                 |         |     |
| execute the given command every 2 mins                          | watch   |     |

------------------------------------------------------------------------

###help

|                                                                 |         |                     |
|-----------------------------------------------------------------|---------|---------------------|
| to know path of a command (that is existence of command in os ) | which   | which ls/cd/mv/etc. |
| to know all path of a command ( binary, source, man page )      | whereis | s,b,m               |
| to know the command information                                 | apropos |                     |
| short version of a command                                      | info    |                     |
| Display detail help content of a command                        | man     | -k                  |

------------------------------------------------------------------------

###Maths

|                                                  |       |
|--------------------------------------------------|-------|
| desktop calucator ( like our calc )              | dc    |
| more complex float or double artimetic operation | bc    |
| expression evaluation                            | expr  |
|                                                  |       |
| open GUI calculator                              | xcalc |

------------------------------------------------------------------------

###User

|                                           |         |                                         |
|-------------------------------------------|---------|-----------------------------------------|
| change the password                       | passwd  |                                         |
| id of current user                        | id      | it just a mechanism to manage the users |
| to list name of groups in system          | groups  | it just a mechanism to manage the users |
|                                           |         |                                         |
| add a user                                | adduser |                                         |
| to set miniimum & maximum password expire | chage   | n, m, l                                 |
| delete a user                             | deluser |                                         |
|                                           |         |                                         |
|                                           |         |                                         |
| to get root access                        | sudo    | s,l                                     |
| to switch user                            | su      |                                         |

------------------------------------------------------------------------

###Hardware
|                                                                                                  |          |                                |
|--------------------------------------------------------------------------------------------------|----------|--------------------------------|
| disk free information of each disk or partition ( mounted with file system )                     | df       | h                              |
| size of current folder / file \[ disk usage\]                                                    | du -hs   |                                |
| to check the file system for inconsistency( any dirty )                                          | fsck     |                                |
|                                                                                                  | scandisk |                                |
| display the hardisk all partitions                                                               | fdisk    | l                              |
| display the OS name, processor, mother board architecure, etc,                                   | uname    | o, hardware-platform, p,a, all |
| give name of computer                                                                            | hostname |                                |
| mount a file system under unix file system. It can be any file system                            
 We should mount any file system like floppy, cd, pen drive, other hard disk partition, before to  
 To use. Now a days it happed on single click instead running commands                             | mount    | a                              |
| un mount a file system under unix file system                                                    | umount   | /dev/sdb1                      |
| display x widget package                                                                         | xdpyinfo |                                |
|                                                                                                  | dd       |                                |
|                                                                                                  | mksf     |                                |
|                                                                                                  | newfs    |                                |
|                                                                                                  | dcopy    |                                |
| it show main memory and swap memory size of system                                               | free     |                                |
|                                                                                                  |          |                                |
| list the availaable recordable devices                                                           | arecord  | l                              |

------------------------------------------------------------------------

### Useful command

|                   |                                                        |
|-------------------|--------------------------------------------------------|
| find delete files | find . -type f -name "FILE-TO-FIND" -exec rm -f {} \\; |

------------------------------------------------------------------------

###Others
|         |
|------------------------------------------------------------------------------------|---------|
| translate SINGLE charactors usually, special \\n, \\t, or any alphanumic charactor | tr      |
|                                                                                    |         |
| screen shot                                                                        | xv      |
| screen shot                                                                        | xwd     |
| screen shot                                                                        | gimp    |
| screen shot                                                                        | xeyes   |
|                                                                                    |         |
|                                                                                    |         |
| it is linux mint funny command.                                                    | cowsay  |
| display temp of cpu                                                                | sensors |
|                                                                                    |         |
|                                                                                    |         |
|                                                                                    | alias   |
|                                                                                    | unalias |

------------------------------------------------------------------------

###Network

|                                               |          |
|-----------------------------------------------|----------|
| email utility                                 | mail     |
| email utility                                 | mailx    |
|                                               |          |
| utility to convert rpm package to deb package | alien    |
| used by oracle installation                   | libaio1  |
| tell about DNS server                         | Nm-tool  |
| tell hardware reagaring network               | lspci    |
|                                               |          |
| default firewall in linux mint                | iptables |
