[Linux Page](linuxindex.html)

------------------------------------------------------------------------

Overview
========

[to do shell script](#table0)
 [Shell script](#table1)
 [Shell variable](#table2)
 [Shell Learning Topic](#table4)
 [SED](#table5)

------------------------------------------------------------------------

1: *to do shell script*
=======================

|                                                                                                               |
|---------------------------------------------------------------------------------------------------------------|
| back up my ebook                                                                                              |
| open set of application, like eclipse, a pdf, and set of excel and ppt at startup                             |
| connect net once aftet statup                                                                                 |
| install a set of basic software after OS installed ( eclipse, oracle, java, install some linux softare, etc ) |

------------------------------------------------------------------------

2: *Shell script*
=================

|                              |                                                                                 |                                                                                           |
|------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Shell script                 |                                                                                 |                                                                                           |
|                              | it is a file which declared a set of commands                                   |                                                                                           |
|                              |                                                                                 |                                                                                           |
|                              |                                                                                 |                                                                                           |
| Gawk                         | it is GNOME version of AWK                                                      |                                                                                           |
|                              |                                                                                 |                                                                                           |
|                              |                                                                                 | AWK is utility used in shell script for string and text manipulation                      |
|                              |                                                                                 | As per my understanding AWK is like Expression language used in JSP, Spring configuration |
|                              |                                                                                 |                                                                                           |
|                              |                                                                                 | AWK is best to manipulate feed files which is in a record-fields                          |
|                              |                                                                                 | it is pattern-matching language                                                           |
|                              |                                                                                 |                                                                                           |
|                              |                                                                                 |                                                                                           |
| Shell scipt                  |                                                                                 |                                                                                           |
|                              | it is interpreted not compiled                                                  |                                                                                           |
|                              | it is readable as well as executable                                            |                                                                                           |
|                              | script file passed as argument to a shell                                       |                                                                                           |
|                              | if a file is executable (by chmod), it can be executed like other command       |                                                                                           |
|                              |                                                                                 |                                                                                           |
|                              | for a shell script we can create alias. But it is availble only current session |                                                                                           |
|                              |                                                                                 |                                                                                           |
|                              |                                                                                 |                                                                                           |
| **Other scripting language** |                                                                                 |                                                                                           |
|                              |                                                                                 |                                                                                           |
|                              |                                                                                 |                                                                                           |
|                              | perl                                                                            | it is old style of scripting language                                                     |
|                              | python                                                                          | object oriented scriptiong language                                                       |
|                              | tcl/tk                                                                          | it is another scripting language. Used with x-window for GUI tool                         |
|                              |                                                                                 |                                                                                           |
|                              |                                                                                 |                                                                                           |
| **usage of shell script**    |                                                                                 |                                                                                           |
|                              |                                                                                 | Automation for common task                                                                |
|                              |                                                                                 | System administration                                                                     |

------------------------------------------------------------------------

3: *Shell variable*
===================

|                            |                                                    |
|----------------------------|----------------------------------------------------|
| Shell variable declaration |                                                    |
|                            |                                                    |
|                            | variable name are case-senstive like java          |
|                            | variable is untyped                                |
|                            | decimal value is treated as text                   |
|                            | as best practice use CAPS for environment variable |
| shell variable scope       |                                                    |
|                            | it is available for with in scope of session       |
|                            |                                                    |
| comment                    |                                                    |
|                            | any line begin with \# will be ignored             |
| white line                 |                                                    |
|                            | any empty white line will be ignored               |

------------------------------------------------------------------------

4: *Shell Learning Topic*
=========================

|                 |                                                                                                        |                                                               |
|-----------------|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Building Blocks | variable, if, case, for, while, until, built-in commands, environment variable, command line arguments |                                                               |
| function        | function, function file, function arguments                                                            |                                                               |
| pipe            | pipe and filters                                                                                       |                                                               |
| File Handling   | file permission and size check                                                                         |                                                               |
|                 | usage of “here file”                                                                                   |                                                               |
| text processing | sed, awk, rc                                                                                           | GNU Sed, Ssed, BSD Sed, POSIX Sed, mod\_sed and csed and etc. |
|                 |                                                                                                        |                                                               |
| usage of        | fork() and exec()                                                                                      |                                                               |

------------------------------------------------------------------------

5: *SED*
========

|     |     |                |                  |                                                            |     |
|-----|-----|----------------|------------------|------------------------------------------------------------|-----|
|     |     |                |                  |                                                            |     |
|     |     | **option**     | **commond**      | **description**                                            |     |
|     |     |                |                  |                                                            |     |
|     | sed |                | d                | delete the current line in patten buffer                   |     |
|     |     | e              |                  | read the content from a file instead of pipe               |     |
|     |     | n/quiet/slient |                  | dont printout the output of processing                     |     |
|     |     |                | p                | print the output. This 'p' always used along with 'n' flag |     |
|     |     |                | location         | tell the line no.                                          |     |
|     |     |                | address          | it select as a range                                       |     |
|     |     |                | address negation | negate the selected range                                  |     |
|     |     |                | address step     |                                                            |     |
|     |     |                | s                | substituion                                                |     |
|     |     |                |                  |      
