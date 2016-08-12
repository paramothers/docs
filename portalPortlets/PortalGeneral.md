Portal - is a collection many mini-web application (many portlets)

Portlet - each mini application in web portal called as portlet/ portal page

## PorTAL application's features are

1. Content Aggregation , Personalization, Customization, Authentication
2. it is as gateway to enter many individual web applications
3. Inter-portlet commuication provided by **portal container**
4. portlet.xml used as DD.

## PortLET

1. "Script Portlet" is helps to use AngularJS to develop portal applications for IBM Portal server


## Best Practice

1.  Avoid to dumb all rendering logic in single method, use mode facility to split up
2.  Avoid to use action method just to set mode
3.  When use spring, have separate controllers for handing render request