
Gen
===

|                     |                                                             |
|---------------------|-------------------------------------------------------------|
| it is created by    | `Rod Johnson` at 2002 ,  released in June 2003              |
|                     | spring is modular framework, a lot of module works together |
| what Spring give us | DI and AOP                                                  |
|                     | Remove boilerplate code by Template pattern and aspect      |
|                     | Gives Power to POJOs                                        |
|                     | declarative programming                                     |

Best Practice
=============

|             |                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
|             | use of annotation, to integrate with JPA and hibernate (@PersistenceConstext, @autoWire ) , we no need to use any Spring specific classes.       |
|             |                                                                                                                                                  |
|             | use Autowire. We can re factor any reference variable at any time                                                                                |
|             | use AutoDiscover. Reduce element in xml file                                                                                                     |
|             |                                                                                                                                                  |
|             | Better to depend autowire and autodiscovery.                                                                                                     |
|             | Override some of bean ONLY whenever exactly need for them.                                                                                       |
| transaction | use readOnly attribute @Transactional annoation for select method                                                                                |
| annotation  | define custome annotation for project's service layer ( Component )                                                                              |
| annotation  | use Repositary annotation, only if we use JPA or hibernate                                                                                       |
| annotation  | define custome annotation for project's dao layer, if we use plain JDBC or SimpleJDBCTemplate                                                    |
| pointcut    | define pointcut separately and refer it by application                                                                                           |
| AOP         | have separate AOP for dao , to print the parameters from pojo, at delivery I may disable this alone                                              |
| AOP         | Have separate AOP for service, to print the parameters from pojo, I can use any pointcut for bug analysis                                        |
| AOP         | try to use AOP to print stack trace                                                                                                              |
| AOP         | use  point cut, to use when i need layer specific advice need                                                                        |
| DAO         | At least, use interface to access dao layer, provided that service layer not having interfaces                                                   |
|             |                                                                                                                                                  |
|             | Dont all un necessary jar files in class path                                                                                                    |
|             | use external **configuration** files for Datasource                                                                                              |
|             |                                                                                                                                                  |
| annotation  | use @PreDestory, @Postconstruct Annotation for lifecyle instead of use Spring specific faclity                                                   |
| annotation  | use @Inject (java common ) annotation instead of using Spring Specfic @Autowire annotation                                                       |
|             | use Resource.getResources() to load external resources                                                                                           |
|             |                                                                                                                                                  |
| AOP         | if we use AOP, for logging, later if we want to change logging framework, we easily change.                                                      
                More over, logging method will be scattered across application code. If need I can any no. of                                                    
                Logging statement for debuging, I can delete them whenever no need.                                                                              |
| AOP         | put all of @Pointcut expression definition in single class and share with many advices.                                                          
                When referring add package, class name along with method name                                                                                    |
| DAO         | create my application specific DAO layer exception by extending directly or indirectly spring's DataAccessException                              |
| Spring-JDBC | create Callable/PreparedStatmentCreator implementation and try to share among more than one DAO or method if possible                            |
|             |                                                                                                                                                  |
| XML file    | have separate xml configuration file for JMS related configuration, though minimal element only                                                  |
| XML file    | have separate xml configuration file for Datasource, ORM related configuration, though minimal element only                                      |
| XML file    | have separate xml configuration file for Transaction manager though u have only one resource                                                     |
| XML file    | have separate xml configuration file for AOP, though minimal element only                                                                        |
| XML file    | have separate xml configuration file as main configuration file, though minimal element only                                                     |
| XML file    | have separate xml configuration file for Junit test, usually, it will import other bean configuration file and we can point to our test database |
| Junit       | use in-memory Derby , HSQLDB for testing.                                                                                                        |

Suggestion & idea
=================

|               |                                                                                                                                                                   |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Configuration |                                                                                                                                                                   |
|               | Instead of adding annotations in every service, dao, controller class, we can specify the packages for different layers, those should consider appropriate beans. |

What Spring Gives
=================

|                                                                        |                         |
|------------------------------------------------------------------------|-------------------------|
| It never force developer to implement any interface like EJB, Servlets |                         |
| It avoid developer to implements set of design pattern themselves      |                         |
|                                                                        | Factory pattern         |
|                                                                        | Observer Pattern        |
|                                                                        | Service Locator pattern |
|                                                                        | Single Pattern          |
|                                                                        | Template Pattern        |
|                                                                        | Startegy pattern        |
|                                                                        |                         |
| It give power to normal java bean                                      |                         |
| It reduce amount of coding by annotation or xml file                   |                         |
| By DI, Code become simpler, easier                                     |                         |
| provide best to unit testing                                           |                         |

**Spring framework has several  Bean containers.**

1. BeanFactory typed containers
2. ApplicationContext typed containers 

API - AOP
=========

 AOP programming in spring possible in  three ways
 
 1. Clasic method use of java API
 2. Declarative using XML aop: namespace
 3. Annotated using AspectJ annotation. ( i prefer this only )

 + Aspect 
  - Advice - logging logic, security logic
  - Joinpoints  - methods, variable access
  - pointcuts - identify methods to be woweven with advice. usaully regular expression



