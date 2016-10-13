
General
=======

Jasper Report Server consist of

1. a WAR file, contain jasper library
2. optional, Tomcat as a web container
3. optional, PostgreSQL DB


it uses Spring 3.1

it need minimum 2 gb RAM, 10gb harddisk

it uses, ant script for install/ uninstll/ test the environment

1. lets use Server's Datasoruce pool for DB connection
2. lets NOT embed the SQL query in template, to speed the development by avoiding unnecessary compile the tmeplate
3. and also possible to run any procedure or function get the Cursor
4. let use JRVirtualizer for large volume of data
5. if XML template is not create at runtime, use of ANT task to compile is good idea
6. always use JasperReport object to represent compiled Native format of jasper report
7. i should use <sortField> only if data source other than DB such as CSV
8. I SHOUld use <filterExpression> only if data source other than DB.
9. I should use <group> only if data souce other than DB
10. use of <subreport> when same report content displayed by different report. It is like <jsp:Include>
11. load the image one time into memory and use entire life of application
12. Export filled jasper report into xml when u want to keep report in DB. So that it is human readable, again convert to JasperPring

## Jasper Report Server

1. it is accessed by RESTful web services
   1. now it has version 2 API.

# Built-in Variable

1. PAGE_COUNT	
2. PAGE_NUMBER	
3. COLUMN_COUNT	
4. COLUMN_NUMBER	
5. REPORT_COUNT	Contains the total number of records in the report.
6. <NameOfGroup>_COUNT	Contains the total number of records in the group named NameOfGroup

# Built-in Parameter

1. REPORT_PARAMETERS_MAP	refer java.util.HashMap object, used to pass subreport
2. REPORT_DATA_SOURCE	refer implementation of JRDataSource, used to pass subreport
3. REPORT_CONNECTION	refer java.sql.Connection object, used to pass subreport
4. IS_IGNORE_PAGINATION	used in HTML/text report generation
5. REPORT_LOCALE	
6. REPORT_RESOURCE_BUNDLE	refer implementation of ResourceBundle
7. REPORT_MAX_COUNT	
8. REPORT_SCRIPTLET	refer implementation of JRDefaultScriptlet
9. REPORT_VIRTUALIZER	refere implementation of .JRVirtualizer