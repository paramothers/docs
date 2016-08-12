
1. Java has to be updated  to 8
2. Spring has to be updated to 4.3
3. Entittlement has to be migrated as MicroService/ Plain-Restful-Spring
4. Tomcat with pluto has to be usable. ( Any WPS dependency has to be migrated /avoided )
5. Gradle has to be used for workflow
6. WAS should be mim 8.5


Tool changes
===========

1. Eclipse Neno instead of RAD
2. ToadEclpse plugin instead of SQL Developer
3. Eclispe RSE instead of WinSCP
4. Git among developer by shared drive


In existing setup
=============
1. few coding standard in java
2. Attribte key move to constatn
3. Entitlement object check move to interceptor
4. date format move to joda and util
2. JSP practise



   Profile = Entitilement, from EJB call for given user id
   populate variouse profile info to AdminEntReportTO
   
   
   #AUTHICATion  servlet name#
   
   https://olbbdev4.tsa.bmo.com/ctpauth/CTPEAILogin/CustUserPasswordAuthServlet
   https://olbbbccld4web13.tsa.bmo.com/ctpauth/CTPEAILogin/BankUserPasswordAuthServlet
   
   **home portal**
   
   https://olbbbccld4web13.tsa.bmo.com/wps/myportal/olbb/home ***then admin***
   https://olbbbccld4web13.tsa.bmo.com/wps/myportal/olbb/administration
   
   
   
   DispatchPortlet -> DefaultAnnotationHandlerMapping - >.AuthenticationInterceptor > Entitlment EJB, jasper session > controller -> ViewRendererServlet
                     
