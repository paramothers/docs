# Changes  Required ( Need approval )

1. Cut down EJB usage
2. Rest Client to connect Jasper Server instead of HttpClient API
3. Java Validation JSR 338 for Request Parameter Validation
4. Use of Spring 4.3 
5. USe of Java 8 ( About WPS and WAS upgrade !! )



# In existing setup

##Minor/no impact

1. date format move to joda and util
2. few method used @ResourceMapping instead of @ActionMapping
3. Attribte key move to constatant
4. use of @ExceptionResolver for exception handling to avoid repeated code in controller
5. more use of @RequestParam
6. make war or jar (bundled JAR) as deployment artifact rather than EAR
7. constant util for all String accross project
8. java file with minimum no. line.
9. mainReport DAO should set size in connection
10. why EXTJS specfic javascript files are in project ? Remove

##Medium impact

1. extjs script include by doHeader() method/ WPS specfic file
2. service method parameter count is more.
3. JSP practise
4. more use of @SessionAttribute/ @ModelAttribute instead of direct usage of potletSession object. it easy to test
5. Use of validation framework on Domain objects
6. Writing Junit test at least at controller level
7. use of EXTJS by recommended architecture with REST/HTTP calls. Use of DispatcherServlet.doHeader() 
8. few render method in controller can be removed by favor of <portlet:renderURL>
9. HttpSession/ProtletSession must be wrapped by a wrapper class. So session usage o0nly by wrapper
10. use @sessionAttribute with @ModelAttribute to get "adminReportObj"
11. gradle should build only current project but not dependent project
12. JavaConfig- no more xml



##Major Impact

1. Use of EJB as DAO, really bad 
2. Entity and *TO object for same domain. it must be either one
3. use Restful call to  JasperServer rather than use HTTPclient library
4. create another Jenkin Job to deploy in DEV-webshpere
5. develop custom validator and use bind service interface. So any DB-Specific implementation applied at dynamically
6. use of BuileStep plugin for Jenkin, ex. run a job ONLY if a particular person checkin files
7. Tomcat with pluto has to be usable. ( Any WPS dependency has to be migrated /avoided )
8. gradle as build tool & multimodule


##No Way without Re-structor

1. avoid websphere depencency completly
2. WAS should be mim 8.5
2. what are the services/built-in portlets has been used from WPS
3. Java has to be updated  to 8
4. Spring has to be updated to 4.3
5. Entittlement has to be migrated as MicroService/ Plain-Restful-Spring ( at least ejb stub alone)
6. Angular JS along with BootStrap for UI
7. spring @profile
8. DB access via Spring-DATA
9. micro services for print/view demo/ help/ contact us /  signout / Entitlement 



Tool changes - Team  need to put learning effort
===========

1. Eclipse Neno instead of RAD
2. ToadEclpse plugin instead of SQL Developer
3. Eclispe RSE instead of WinSCP
4. Git among developer by shared drive​

