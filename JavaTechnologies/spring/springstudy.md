
Gen
---

|                  |                                          |
| ---------------- | ---------------------------------------- |
| it is created by | `Rod Johnson` at 2002 ,  released in June 2003 |
|                  | Spring is modular framework, there are module for most of programming |

## How Spring Help to java Developers

1. DI and AOP
2. Remove boilerplate code by Template pattern and aspect
3. Gives Power to POJOs
4. declarative programming either by annotation/ javaconfig/ xml




## Best Practice

1. use of annotation, to integrate with JPA and hibernate (@PersistenceConstext, @autoWire ) , we no need to use any Spring specific classes.
2. Better to depend autowire and autodiscovery.
3. Define custome annotation for project's service/any layer ( Inherint of @Component )
4. define pointcut separately and refer it by application
5. have separate AOP for dao , to print the parameters from pojo, at delivery I may disable this alone
6. Have separate AOP for service, to print the parameters from pojo, I can use any pointcut for bug analysis
7. try to use AOP to print stack trace 
8. use  point cut, to use when i need layer specific advice need
9. use @PreDestory, @Postconstruct Annotation for lifecyle instead of use Spring specific faclity
10. put all of @Pointcut expression definition in single class and share with many advices
11. use Conditional Configuration and @profile
12. one property file load using @PropertySource and access Environment object
13. use @Profile bounded bean for different deployment environment.
14. Entire SpringContext/WebContext should configure using JavaConfig.
15. Have separate marker interface in each layer and use that for scanning path specification
16. Have as many as configuration files in separate config package
17. use of AOP, for at least logger entry-exit statements using AspectJ annotations.
18. Test cases for each controller or each service bean.
19. create custom annotation as complements of spring specific annotation.

Transaction

1. use readOnly attribute @Transactional annoation for select method



Suggestion & idea
-----------------

|               |                                          |
| ------------- | ---------------------------------------- |
| Configuration |                                          |
|               | Instead of adding annotations in every service, dao, controller class, we can specify the packages for different layers, those should consider appropriate beans. |


What Spring Gives
-----------------

|                                          |                         |
| ---------------------------------------- | ----------------------- |
| It never force developer to implement any interface like EJB, Servlets |                         |
| It avoid developer to implements set of design pattern themselves |                         |
|                                          | Factory pattern         |
|                                          | Observer Pattern        |
|                                          | Service Locator pattern |
|                                          | Single Pattern          |
|                                          | Template Pattern        |
|                                          | Startegy pattern        |
| It give power to normal java bean        |                         |
| It reduce amount of coding by annotation or xml file |                         |
| By DI, Code become simpler, easier       |                         |
| provide best to unit testing             |                         |

**Spring framework has several  Bean containers.**

1. BeanFactory typed containers
2. ApplicationContext typed containers 



API - AOP
---------

 AOP programming in spring possible in  three ways

 1. Clasic method use of java API
 2. Declarative using XML aop: namespace
 3. Annotated using AspectJ annotation. ( i prefer this only )

+ Aspect 
- Advice - logging logic, security logic
- Joinpoints  - methods, variable access
    - pointcuts - identify methods to be woweven with advice. usaully regular expression



Spring Web Flow
---------------

+ flow executor
+ flow registry



Spring Persistence
------------------ 

There are 4 different ways to create datasource in spring project.

+ DataSource open source implementation
    + Apache Common DPCP
    + c3p0
    + BoneCP
+ DataSource from Spring- driver-manager based (3 types are there)
+ DataSource from Jndi-lookup
+ DataSource from embedded DB.


# Spring Portlet MVC

