# In existing setup (what I can contribute)

- 1. few coding standard in java
  2. Attribte key move to constatn
  3. Entitlement object check move to interceptor
  4. date format move to joda and util
  5. JSP practise
  6. more use of @RequestParam
  7. more use of @SessionAttribute/ @ModelAttribute instead of direct usage of potletSession object. it easy to test.
- 1. use Restful call to  JasperServer rather than use HTTPclient library
  2. avoid websphere depencency completly
  3. make war or jar (bundled JAR) as deployment artifact rather than EAR
  4. create another Jenkin Job to deploy in DEV-webshpere
  5. Use of validation framework on Domain objects.
  6. develop custom validator and use bind service interface. So any DB-Specific implementation applied at dynamically
  7. Writing Junit test at least at controller level
  8. constant util for all String accross project
  9. java file with minimum no. line.
  10. what are the services/built-in portlets has been used from WPS.
  11. use of SimpleDateFormat is tend to error prone
  12. use of EXTJS by recommended architecture with REST/HTTP calls. Use of DispatcherServlet.doHeader() .
  13. use of BuileStep plugin for Jenkin, ex. run a job ONLY if a particular person checkin files.
  14. right now , we have only one portlet..!!!

#    Drastic Changes -  Need client approval


1. Java has to be updated  to 8
2. Spring has to be updated to 4.3
3. Entittlement has to be migrated as MicroService/ Plain-Restful-Spring
4. Tomcat with pluto has to be usable. ( Any WPS dependency has to be migrated /avoided )
5. Gradle has to be used for workflow
6. WAS should be mim 8.5
7. Angular JS along with BootStrap for UI
8. gradle as build tool & multimodule
9. spring @profile
10. JavaConfig- no more xml
11. DB access via Spring-DATA
12. micro services for print/view demo/ help/ contact us /  signout / Entitlement 



Tool changes - Team  need to put learning effort
===========

1. Eclipse Neno instead of RAD
2. ToadEclpse plugin instead of SQL Developer
3. Eclispe RSE instead of WinSCP
4. Git among developer by shared drive​

