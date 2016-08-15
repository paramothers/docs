## Understanding

+ How the Jasper Report template designed/ customized 
+ why Http Client has been used
+ EJB used becauseof JPA
+ do you have have dedicated jasper server
+ why jasper report than bo/etc ?
+ portlet 2.0
+ springProtlet module


Assumption
==========
1. Just online template design/update and expoert template.

2. AUTHICATion  servlet name

     ctpauth/CTPEAILogin/CustUserPasswordAuthServlet 

   ctpauth/CTPEAILogin/BankUserPasswordAuthServlet

      **home portal**

     /wps/myportal/olbb/home **then admin**   /wps/myportal/olbb/administration   

      DispatchPortlet -> DefaultAnnotationHandlerMapping - >.AuthenticationInterceptor > Entitlment EJB, jasper session > controller -> ViewRendererServlet​     

   Profile = Entitilement, from EJB call for given user id   populate variouse profile info to AdminEntReportTO




===================


