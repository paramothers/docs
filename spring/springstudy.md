-   [Genneral](#table0)
-   [Best Practice](#table3)
-   [Suggestion & idea](#table4)
-   [What Spring Gives](#table6)
-   [API-CORE](#table7)
-   [API - AppContext](#table14)
-   [API - core Life cycle & Aware](#table15)
-   [API - AOP](#table16)
-   [API - JDBC](#table17)
-   [API - iBATIS](#table18)
-   [API - Hibernate](#table19)
-   [API - JPA](#table20)
-   [API - Transaction](#table21)
-   [API - Web](#table22)
-   [API - Unit test](#table23)
-   [API - Exception](#table24)
-   [API - EJB](#table26)
-   [API - Remote Services](#table27)
-   [Spring-WS](#table28)
-   [API - JMS](#table29)
-   [API - JavaMail](#table30)
-   [API - JMX](#table32)
-   [API - schedule](#table33)
-   [API - Rest](#table34)
-   [API - Security](#table35)

Gen
===

|                     |                                                             |
|---------------------|-------------------------------------------------------------|
| it is created by    | **Rod Johnson **at 2002                                     |
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

BeanFactory typed Containers
============================

|                     |                            |                                |                |                        |                     |
|---------------------|----------------------------|--------------------------------|----------------|------------------------|---------------------|
| BeanFactory         |                            |                                |                |                        |                     |
|                     | DefaultListableBeanFactory |                                |                |                        |                     |
|                     |                            | XMLBeanFactory                 |                |                        |                     |
|                     |                            |                                |                |                        |                     |
|                     | BeanDefinitionRegistry     |                                |                |                        |                     |
|                     |                            | XmlBeanDefinitionReader        |                |                        |                     |
|                     |                            | PropertiesBeanDefinitionReader |                |                        |                     |
|                     |                            |                                | BeanDefinition |                        |                     |
|                     |                            |                                |                | BeanDefinitionVisistor |                     |
|                     |                            |                                |                |                        | StringValueResolver |
|                     |                            |                                | Resource       |                        |                     |
|                     |                            |                                |                | FileSystemResource     |                     |
|                     |                            |                                |                | ByteArrayResource      |                     |
|                     |                            |                                |                | ClassPathResource      |                     |
|                     |                            |                                |                | DescriptiveResource    |                     |
|                     |                            |                                |                | InputStreamResource    |                     |
|                     |                            |                                |                | PortletContextResource |                     |
|                     |                            |                                |                | ServletContextResource |                     |
|                     |                            |                                |                | UrlResource            |                     |
|                     |                            |                                | ResourceLoader |                        |                     |
|                     |                            |                                |                | DefaultResourceLoader  |                     |
| MethodReplacer      |                            |                                |                |                        |                     |
| FactoryBean         |                            |                                |                |                        |                     |
|                     | JndiObjectFactoryBean      |                                |                |                        |                     |
| PropertyEditor      |                            |                                |                |                        |                     |
|                     | PropertyEditorSupport      |                                |                |                        |                     |
| ExpressionParser    |                            |                                |                |                        |                     |
|                     | Expression                 |                                |                |                        |                     |
| ParseException      |                            |                                |                |                        |                     |
| EvaluationException |                            |                                |                |                        |                     |
|                     |                            |                                |                |                        |                     |
|                     |                            |                                |                |                        |                     |
| FileUtil            |                            |                                |                |                        |                     |
| ExceptionUtil       |                            |                                |                |                        |                     |
| FileCopyUtil        |                            |                                |                |                        |                     |

ApplicationContext typed Container
==================================

|                                |                                                                                              |                                  |                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------|----------------------------------|--------------------------------------------------------|
| ApplicationContext             |                                                                                              |                                  |                                                        |
| ConfigurableApplicationContext |                                                                                              |                                  |                                                        |
|                                | ~~ClassPathXmlApplicationContext~~                                                           |                                  | Load configuration from classpath                      |
|                                | ~~FileSystemXmlApplicationContext~~                                                          |                                  | Load configuration from filesystem                     |
|                                | ~~XmlPortletApplicationContext~~                                                             |                                  |                                                        |
|                                | ~~WebApplicationContext~~                                                                    |                                  |                                                        |
|                                |                                                                                              | ~~XmlWebApplicationContext~~     | Load configuration from war file                       |
|                                | <span style="background-color: rgb(0, 255, 0);">AnnotationConfigApplicationContext</span>    |                                  | Load configuration from JavaConfig                     |
|                                | <span style="background-color: rgb(0, 255, 0);">AnnotationWebConfigApplicationContext</span> |                                  | Load configuration from JavaConfig for web application |
|                                |                                                                                              |                                  |                                                        |
|                                | ContextLoader                                                                                |                                  |                                                        |
|                                |                                                                                              | ContextLoaderListener            |                                                        |
|                                |                                                                                              | ContextLoaderServlet             |                                                        |
|                                |                                                                                              |                                  |                                                        |
|                                |                                                                                              | ApplicationContextAwareProcessor |                                                        |
|                                |                                                                                              |                                  |                                                        |
| LoadTimeWeaverAware            |                                                                                              |                                  |                                                        |
| MessageSourceAware             |                                                                                              |                                  |                                                        |
| ApplicationEventPublisherAware |                                                                                              |                                  |                                                        |
| ResourceLoaderAware            |                                                                                              |                                  |                                                        |
| LifeCycle                      |                                                                                              |                                  |                                                        |
| ApplicationEvent               |                                                                                              |                                  |                                                        |
|                                | ApplicationListener                                                                          |                                  |                                                        |
| ApplicationEventPublisher      |                                                                                              |                                  |                                                        |
|                                | ContextClosedEvent                                                                           |                                  |                                                        |
|                                | ContextRefreshedEvent                                                                        |                                  |                                                        |
|                                | RequestHandledEvent                                                                          |                                  |                                                        |
| ApplicationEventMulticaster    |                                                                                              |                                  |                                                        |
| BeanNameGenerator              |                                                                                              |                                  |                                                        |

Bean life-cycle API
===================

Bean life-cycle phases

1. Instantiate

2. populate properties

3. BeanName<span style="color: rgb(255, 0, 0);">Aware</span>

4. BeanFactory<span style="color: rgb(255, 0, 0);">Aware</span>

5. ApplicationContext<span style="color: rgb(255, 0, 0);">Aware</span>

6. Bean<span style="color: rgb(45, 229, 45);">PostProcessor</span>( Pre-Initialization )

7. InitializingBean's afterPropertiesSet();

8. call custom init-method

9. Bean<span style="color: rgb(45, 229, 45);">PostProcessor</span>( Post - Initialization )

 ( Live Bean in Application context )

10. DisposableBean

11. custom-destory method

|                                   |                                                                  |
|-----------------------------------|------------------------------------------------------------------|
| InitializingBean                  | replace by @PostConstruct                                        |
| DisposableBean                    | replace by @PreDestory                                           |
| BeanPostProcessors                |                                                                  |
|                                   | **CommonAnnotationBeanPostProcessor**                            |
|                                   | **AutowiredAnnotationBeanPostProcessor**                         |
| DestructionAwareBeanPostProcessor |                                                                  |
|                                   | **InitDestroyAnnotationBeanPostProcessor**                       |
| BeanFactoryPostProcessor          |                                                                  |
|                                   | it has 8 BeanFactory post process comes with spring distribution |
| BeanNameAware                     |                                                                  |
| BeanFactoryAware                  |                                                                  |
| ApplicationContextAware           |                                                                  |

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

|     |                                                          |                                    |                                   |                                                                            |
|-----|----------------------------------------------------------|------------------------------------|-----------------------------------|----------------------------------------------------------------------------|
|     | JointPoint                                               |                                    |                                   | used with @Before, @After, @AfterThrowing annotation                       |
|     |                                                          | ProceedingJointPoint               |                                   | used with @Around annotation                                               |
|     |                                                          |                                    |                                   |                                                                            |
|     | it is classic spring AOP API. But we prefere to          |  | | |
|     |  Either XML or Annotation .it may help to understand      | | | |
|     |  What is happing in behind the scene. Otherwise no need.  |                                    |                                   |                                                                            |
|     |                                                          |                                    |                                   |                                                                            |
|     | ProxyFactory                                             |                                    |                                   |                                                                            |
|     |                                                          | DefaultAopProxyFactory             |                                   |                                                                            |
|     |                                                          |                                    | Cblib2AopProxy                    |                                                                            |
|     |                                                          |                                    | JdkDynamicAopProxy                |                                                                            |
|     | AspectJProxyFactory                                      |                                    |                                   |                                                                            |
|     | AopContext                                               |                                    |                                   |                                                                            |
|     | ProxyFactoryBean                                         |                                    |                                   |                                                                            |
|     | Advisor                                                  |                                    |                                   |                                                                            |
|     |                                                          | IntroductionAdvisor                |                                   |                                                                            |
|     |                                                          | PointcutAdvisor                    |                                   |                                                                            |
|     |                                                          |                                    | DefaultPointcutAdvisor            |                                                                            |
|     |                                                          |                                    |                                   | RegexpMethodPointcutAdvisor                                                |
|     |                                                          |                                    |                                   | AspectJExpressionPointcutAdvisor                                           |
|     |                                                          |                                    |                                   | NameMatchMethodPointcutAdvisor                                             |
|     | Advise                                                   |                                    |                                   |                                                                            |
|     |                                                          | BeforeAdvice                       |                                   |                                                                            |
|     |                                                          |                                    | Interceptor                       |                                                                            |
|     |                                                          | AfterAdvice                        | staticMethodMatcherPointcut       |                                                                            |
|     |                                                          |                                    | AfterReturningAdvice              |                                                                            |
|     |                                                          | ThrowsAdvice                       |                                   |                                                                            |
|     |                                                          |                                    | MethodBeforeAdvice                |                                                                            |
|     |                                                          | MethodInterceptor ( Aop alliance ) |                                   |                                                                            |
|     |                                                          |                                    | MethodInvocation ( Aop alliance ) |                                                                            |
|     | Pointcut                                                 |                                    |                                   |                                                                            |
|     |                                                          | ClassFilter                        |                                   |                                                                            |
|     |                                                          | MethodMatcher                      |                                   |                                                                            |
|     |                                                          |                                    | StaticMethodMatcherPointcut       | used for statically method matcher                                         |
|     |                                                          |                                    | DynamicMethodMatcherPointcut      | used for dynamically method matcher based argument value                   |
|     |                                                          |                                    | NameMatchMethodPointcut           | used to match set of given methods name irrespective of return /parameters |
|     |                                                          |                                    | JdkRegexpMethodPointcut           | used to match methods based on regular expression                          |
|     |                                                          |                                    | Pearl5RegexpMethodPointcut        | used to match methods based on Perl expression                             |
|     |                                                          |                                    | AspectJExpressionPointcut         | used to match methods based on AspectJ expression                          |
|     |                                                          |                                    | AnnotationMatchingPointcut        | used to match methods based on given annotation                            |
|     |                                                          |                                    | ControlFlowPointcut               | used to match methods based on from which method is called                 |
|     |                                                          |                                    | ComposablePointcut                |                                                                            |
|     | PointcutS                                                |                                    |                                   |                                                                            |

API - JDBC
==========

|                                                                                                                                                                                                               |                                                                                                 |                              |                                                             |                                    |                                    |                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|------------------------------|-------------------------------------------------------------|------------------------------------|------------------------------------|-----------------|
| It is best for Master table, at 2.5                                                                                                                                                                           | RdbmsOperation                                                                                  | SQLCall                      |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              | **StoredProcedure**                                         |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 | SQLOperation                 |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              | **SQLQuery**                                                |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              |                                                             | updatableSQLQuery                  |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              |                                                             | MappingSQLQueryWithParameter       |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              |                                                             |                                    | MappingSQLQuery                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              |                                                             |                                    |                                    | **SQLFunction** |
|                                                                                                                                                                                                               |                                                                                                 |                              | **SQLUpdate**                                               |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              |                                                             | BatchSQLUpdate                     |                                    |                 |
|                                                                                                                                                                                                               | LobHandler                                                                                      |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 | DefaultLobHandler            |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 | OracleLobHandler             |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 | NativeJdbcExtractor          |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               | JdbcDaoSupport                                                                                  |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               | SimpleJdbcOperations                                                                            |                              |                                                             | it is deprecated at 3.1            |                                    |                 |
| Prefer to use this from Spring 3.0 onwards.                                                                                                                                                                   
  Java 5 features, easy batch                                                                                                                                                                                   |                                                                                                 | **SimpleJdbcTemplate**       |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               | SimpleJdbcCallOperations                                                                        |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 | AbstractJdbcCall             |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              | **SimpleJdbcCall**                                          |                                    |                                    |                 |
|                                                                                                                                                                                                               | SimpleJdbcInsertOperations                                                                      |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 | AbstractInsertCall           |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              | **SimpleJdbcInsert**                                        |                                    |                                    |                 |
|                                                                                                                                                                                                               | JdbcDaoSupport                                                                                  |                              |                                                             |                                    |                                    |                 |
| All of our DAO should be extend this class                                                                                                                                                                    |                                                                                                 | **SimpleJdbcDaoSupport**     |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               | SqlParameterSource                                                                              |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 | AbstractSqlParameterSource   |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              | MapSqlParameterSource                                       |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              | **BeanPropertySqlParameterSource**                          |                                    |                                    |                 |
|                                                                                                                                                                                                               | SqlParameter                                                                                    |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               | DataSourceUtils                                                                                 |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               | EntityManagerFactoryUtils                                                                       |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               | SessionFactoryUtils                                                                             |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               | SQLExceptionTranslator                                                                          |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               | PersistenceManagerFactoryUtils                                                                  |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              |                                                             |                                    |                                    |                 |
| it is spring own datasource implementation class class to provide new db connection for every requestinstead of either DBCP pool or App server connection pool                                                | DriverManagerDataSource                                                                         |                              |                                                             |                                    |                                    |                 |
| it is spring own datasource implementation class class to provide same db connection for every request instead of either DBCP pool or App server connection pool. It is best while developing the application | SingleConnectionDataSource                                                                      |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              |                                                             |                                    |                                    |                 |
| it is re-ENGINERED in spring 3.1                                                                                                                                                                              | JdbcTemplate                                                                                    |                              |                                                             |                                    |                                    |                 |
| it is generic statement execution.                                                                                                                                                                            
  Usually, It will return one or more Domain objects                                                                                                                                                            | one or more JDBC operation                                                                      | StatementCallback            |                                                             |                                    |                                    |                 |
| it is generic preparement statement execution.                                                                                                                                                                
  Usually, It will return one or more Domain objects                                                                                                                                                            | one or more JDBC operation                                                                      | PrepareStatementCallback     |                                                             |                                    |                                    |                 |
| it is generic callable statement execution.                                                                                                                                                                   
  Usually, It will return one or more Domain objects                                                                                                                                                            | one or more JDBC operation                                                                      | CallableStatementCallback    |                                                             |                                    |                                    |                 |
| **Consider below light green background classes, when same query used many times, need cohesive create sql, populate values**                                                                                 |                                                                                                 |                              |                                                             |                                    |                                    |                 |
| used to create CUSTOMized Statement, if need                                                                                                                                                                  | I can create and share with more                                                                
                                                                                                                                                                                                                  Than one DAOs.                                                                                  | StatementCreator             | I could not find any java class or interface at this name   |                                    |                                    |                 |
| it is closed by JdbcTemplate itself                                                                                                                                                                           | I can create and share with more                                                                
                                                                                                                                                                                                                  Than one DAOs.                                                                                  | PrepareStatementCreater      | try to use this, and code at beginning of DAO class         |                                    |                                    |                 |
| let me create all of callablestatement at single place and share across dao                                                                                                                                   | i can create and share with more                                                                
                                                                                                                                                                                                                  Than one DAOs.                                                                                  | CallableStatementCreater     | try to use this, and keep all callable only in single class |                                    |                                    |                 |
| it is utility class                                                                                                                                                                                           |                                                                                                 | StatementCreatorUtils        |                                                             |                                    |                                    |                 |
| **Consider below light green background classes, when to populate values for prepared statement**                                                                                                             |                                                                                                 |                              |                                                             |                                    |                                    |                 |
| it is to set values in single record preparedStatement                                                                                                                                                        | no need to be used only along                                                                   
                                                                                                                                                                                                                  XXXCreator object                                                                               | PreparedStatementSetter      |                                                             |                                    |                                    |                 |
| set values for batch                                                                                                                                                                                          | it is extra ordinary                                                                            | BatchPreparedStatementSetter |                                                             |                                    |                                    |                 |
| **Consider below blue background classes, when Report generations, count, create XML for records,build object from many rows.**                                                                               |                                                                                                 |                              |                                                             |                                    |                                    |                 |
| **It is generic. It will call for every row but resultSet is in JdbcTemplate Control.                                                                                                                         
  Used for SELECT Query                                                                                                                                                                                         
  Use this to create xml for every record**                                                                                                                                                                     | It is used by query() methods jdbcTemplate.                                                     
                                                                                                                                                                                                                  Its method dont return any.                                                                     
                                                                                                                                                                                                                  In majority cases, I have to use along with PreparedStatmentCreator and PreparedStatmentSetter  | RowCallbackHandler           |                                                             |                                    |                                    |                 |
| super utility class                                                                                                                                                                                           |                                                                                                 |                              | RowCountCallbackHandler                                     |                                    |                                    |                 |
| **It is generic. it will give entire resultSet to me and I have to iterate the resultSet and receive the records                                                                                              
  Used for SELECT Query                                                                                                                                                                                         
  This is good for Report or build a object from many row, skip few rows,etc**                                                                                                                                  | it is used by query() methods jdbcTemplate.                                                     
                                                                                                                                                                                                                  In majority cases, I have to use along with PreparedStatmentCreator and PreparedStatmentSetter  
                                                                                                                                                                                                                  It can return object                                                                            | ResultSetExtractor           |                                                             |                                    |                                    |                 |
| **Consider below yellow background classes when you want to EXACTLY one row of resultset to ONE Domain or ONE map**                                                                                           |                                                                                                 |                              |                                                             |                                    |                                    |                 |
| it run for every row and map to a Java Object                                                                                                                                                                 
  Used for SELECT Query                                                                                                                                                                                         | it is reusable since stateless                                                                  | RowMapper                    |                                                             |                                    |                                    |                 |
| no need to use 3.0 version onwards.                                                                                                                                                                           
  Just RowMapper Alone is good enough                                                                                                                                                                           | this is for SimpleJdbcTemplate                                                                  |                              | ParameterizedRowMapper                                      |                                    |                                    |                 |
| return each row in a Map object.                                                                                                                                                                              |                                                                                                 |                              | ColumnMapRowMapper                                          |                                    |                                    |                 |
| it is for single column but one or more row                                                                                                                                                                   |                                                                                                 |                              | SinglecolumnRowMapper                                       |                                    |                                    |                 |
| This is came for SimpleJdbcTemplate.                                                                                                                                                                          
  That itself deprecated in 3.1                                                                                                                                                                                 |                                                                                                 |                              |                                                             | ParameterizedSingleColumnRowMapper |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              | AbstractBeanPropertyRowMapper                               |                                    |                                    |                 |
| use this when column name and bean attribute name both are same.                                                                                                                                              | **it is really good**                                                                           |                              |                                                             | BeanPropertyRowMapper              |                                    |                 |
| use this when column name and bean attribute name both are same.                                                                                                                                              | This is came for SimpleJdbcTemplate.                                                            
                                                                                                                                                                                                                  That itself deprecated in 3.1                                                                   
                                                                                                                                                                                                                  So ignore it.it is introduce performance degrade                                                |                              |                                                             |                                    | ParameterizedBeanPropertyRowMapper |                 |
| it is helps to give best contextual information when exception occurred                                                                                                                                       | it is used along with                                                                           
                                                                                                                                                                                                                  PreparedStatementCreator                                                                        | SQLProvider                  |                                                             |                                    |                                    |                 |
| it is to keep the Generated keys while insert a records. I may not use.                                                                                                                                       |                                                                                                 | KeyHolder                    |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 |                              | GeneratedKeyHolder                                          |                                    |                                    |                 |
| it is to use EXITING Dao code with JdbcTemplete. Better rewrite the exiting dao code if possible. Otherwise just reuse that ugly code.                                                                        | Never use this for newly DAO                                                                    
                                                                                                                                                                                                                  Implementation                                                                                  | ConnectionCallback           |                                                             |                                    |                                    |                 |
| it is introduce at spring 2.0                                                                                                                                                                                 | NamedParameterJdbcTemplate                                                                      |                              |                                                             |                                    |                                    |                 |
|                                                                                                                                                                                                               |                                                                                                 | NamedParameterJdbcDaoSupport |                                                             |                                    |                                    |                 |

API - iBATIS
============

|                                    |                                                                      |                      |
|------------------------------------|----------------------------------------------------------------------|----------------------|
| just load the iBatis configuration | SqlMapClientFactoryBean                                              |                      |
|                                    |                                                                      |                      |
|                                    | SqlMapClientDaoSupport                                               |                      |
|                                    |                                                                      | SqlMapClientTemplate |
|                                    | one these three . Nothing else there to integrate iBatis with spring |                      |

API - Hibernate
===============

|                                                                                  |                            |                                  |                   |
|----------------------------------------------------------------------------------|----------------------------|----------------------------------|-------------------|
|                                                                                  | AbstractSessionFactoryBean |                                  |                   |
| if xml file for mapping, load the configuration                                  |                            | **LocalSessionFactoryBean**      |                   |
| if annotation for mapping, load the configuration                                |                            | **AnnotationSessionFactoryBean** |                   |
| Advent of ContextualSession in Hibernate 3.2, we no need this class to work with 
  Spring                                                                           | HibernateDaoSupport        |                                  |                   |
|                                                                                  |                            | HibernateTemplate                |                   |
|                                                                                  |                            |                                  | HibernateCallback |

API - JPA
=========

|                                                                                                                         |                                        |               |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------|---------------|
| No need in Spring 3.0 onwards                                                                                           | JpaTemplate                            |               |
|                                                                                                                         |                                        | JpaDaoSupport |
| used to create EntityManagerFactory by loading configuration files and wire factory instance in our DAO                 | LocalEntityManagerFactoryBean          |               |
| it allow to modify the configuration such as, DataSoruce, Dialect and obtain JPA context from Container ( App. Server ) | LocalContainerEntityManagerFactoryBean |               |
|                                                                                                                         | JpaDialect                             |               |
| use to autowire EntityManger instance to @PersistenctConext variable in DAO.                                            | PersistenceAnnotationBeanPostProcessor |               |

API - Transaction
=================

|     |                                                                                                    |                             |                              |                                    |
|-----|----------------------------------------------------------------------------------------------------|-----------------------------|------------------------------|------------------------------------|
|     | offers a set of technology-independent facilities, including transaction managers (interface )     |                             | PlatformTransactionManager   |                                    |
|     | for JDBC, Spring JDBC , ibATIS, to provide transaction, single database                            |                             |                              | DataSourceTransactionManager       |
|     | for JEE server's transaction implementation usage.                                                 |                             |                              | JtaTransactionManager              |
|     |                                                                                                    |                             |                              | JpaTransactionManager              |
|     |                                                                                                    |                             |                              | HibernateTransactionManager        |
|     |                                                                                                    |                             |                              | TransactionSysnchronizationManager |
|     |                                                                                                    |                             |                              | JdoTransactionManager              |
|     | it is used in Spring-Batch on-memory repository                                                    |                             |                              | ResourcelessTransactionManager     |
|     |                                                                                                    |                             |                              |                                    |
|     | Easy the programmatic style transaction                                                            | TransactionTemplate         |                              |                                    |
|     | It used to define anonymous class                                                                  |                             | TransactionCallback          |                                    |
|     | when no need, return a object.                                                                     |                             |                              | TransactionCallbackWithoutResult   |
|     |                                                                                                    | TransactionProxyFactoryBean |                              |                                    |
|     |                                                                                                    |                             |                              |                                    |
|     | it just interface                                                                                  | TransactionDefinition       |                              |                                    |
|     | it will hold all the transaction attributes. There are 5 different attributes are, can be defined. |                             | DefaultTransactionDefinition |                                    |
|     |                                                                                                    | TransactionStatus           |                              |                                    |

API - Web
=========

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">RequestContextFilter</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left">servlet config without web.xml</td>
<td align="left">AbstractDispatcherServletInitializer</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
</tr>
<tr class="odd">
<td align="left">servlet config by Javaconfig</td>
<td align="left">AbstractAnnotationConfigDispatcherServletInitializer</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left">RequestContextListener</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left">it is entry point servlet<br />
</td>
<td align="left">DispatcherServlet</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">BeanNameUrlHandlerMapping</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">ControllerBeanNameHandlerMapping</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">ControllerClassNameHandlerMapping</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">DefaultAnnotationHandlerMapping</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">SimpleUrlHandlerMapping</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
</tr>
<tr class="even">
<td align="left">to build uri<br />
</td>
<td align="left"> UriComponentsBuilder</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">Controller</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">SimpleFormController</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">Validator</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">ValidationUtils</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">DefaultBeanValidator</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">DefaultValidatorFactory</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">Error</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">BeanWrapper</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">BeanWrapperImpl</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">SimpleMappingExceptionResolver</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
</tr>
<tr class="even">
<td align="left">it is view configurar<br />
</td>
<td align="left">ViewResolver</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left">resolve as bean name</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left">BeanNameViewResolver</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><span style="color: rgb(255, 153, 102);">ContentNegotiatingViewResolver ( deprecated)</span></td>
</tr>
<tr class="odd">
<td align="left">usually for JSP</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left">InternalResourceViewResolver</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><table>
<tbody>
<tr class="odd">
<td align="left">TilesViewResolver</td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left">ResourceBundleMessageSource</td>
<td align="left"><br />
</td>
<td align="left">TilesJstlView</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
<td align="left"><br />
</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">TilesView</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left">TilesConfigurer</td>
<td align="left"><br />
</td>
<td align="left">ComponentControlerSupport</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">View</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">AbstractExcelView</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left">AbstractPdfView</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">AbstractView</td>
<td align="left"><br />
</td>
<td align="left">SimpleUrlHandlerMapping</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">FlowControler</td>
<td align="left"><br />
</td>
<td align="left">SpringBindingActionForm</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">FlowExecutorFactoryBean</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left">FlowAction</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left">DefaultAdvisorAutoProxyCreator</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">AnnotationAwareAspectJAutoProxyCreator</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left">CustomEditorConfigurator</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">PropertyPlaceholderConfigurer</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">MessageSource</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">ResourceBundleMessageSource</td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">StaticMessageSource.</td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left">HierarchicalMessageSource</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left">ReloadableResourceBundleMessageSource</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><br />
</td>
<td align="left">FlowHandlerMapping</td>
<td align="left"><br />
</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><br />
</td>
<td align="left"> </td>
<td align="left"><br />
</td>
<td align="left">FlowHandlerAdapter</td>
</tr>
</tbody>
</table>

API - Rest
==========

|                                       |     |                           |     |     |
|---------------------------------------|-----|---------------------------|-----|-----|
|                                       |     | HttpMethodConverter       |     |     |
|                                       |     | RestTemplate              |     |     |
|                                       |     | ContentNegotiationManager |     |     |
| it carry metadata about http response |     | ResponseEntity            |     |     |
|                                       |     | HttpStatus                |     |     |
|                                       |     | HttpHeaders               |     |     |

API - Security 3.2
==================

|     |     |                      |     |     |
|-----|-----|----------------------|-----|-----|
|     |     | DelegtingFilterProxy |     |     |
|     |     | FilterChainProxy     |     |     |
|     |     |                      |     |     |
|     |     |                      |     |     |
|     |     |                      |     |     |
|     |     |                      |     |     |

    API - Unit test
===================

|                           |                            |                                               |                                                   |                                           |
|---------------------------|----------------------------|-----------------------------------------------|---------------------------------------------------|-------------------------------------------|
|                           | AbstractSpringContextTests |                                               |                                                   |                                           |
|                           |                            | AbstractDependencyInjectionSpringContextTests |                                                   |                                           |
|                           |                            | AbstractTransactionalSpringContextTests       |                                                   |                                           |
|                           |                            |                                               | AbstractTransactionalDataSourceSpringContextTests |                                           |
|                           |                            |                                               |                                                   | AbstractAnnotationAwareTransactionalTests |
|                           |                            |                                               |                                                   |                                           |
| Good for integration test | SpringJUnit4ClassRunner    |                                               |                                                   |                                           |

API - Exception
===============

|                              |                                |
|------------------------------|--------------------------------|
|                              | BeanCreationException          |
| I will get when use Autowire | UnsatisfiedDependencyException |
|                              | NoSuchBeanDefinitionException  |

API - EJB
=========

|                                                    |                                                         |                            |
|----------------------------------------------------|---------------------------------------------------------|----------------------------|
| EJB 2.1 statless session bean                      | AbstractStatelessSessionBean ( EJB 2.x)                 | no boiler plate code       |
| EJB 2.1 stateful session bean                      | AbstractStatefulSessionBean ( EJB 2.x)                  |                            |
| EJB 2.1 general Message driven bean                | AbstractJMSMessageDrivenBean ( EJB 2.x)                 |                            |
| EJB 2.1 JMS message driven bean                    | AbstractMessageDrivenBean ( EJB 2.x)                    |                            |
|                                                    |                                                         |                            |
| statless remote session â€“ client                 | SimpleRemoteStatelessSessionProxyFactoryBean ( EJB 2.x) | handle checkeced exception |
| statless local session â€“ client                  | LocalStatelessSessionProxyFactoryBean ( EJB 2.x)        |                            |
|                                                    |                                                         |                            |
|                                                    |                                                         |                            |
| it allow, a EJB, to use Spring application context | SpringBeanAutowiringInterceptor ( EJB 3.x)              |                            |

API - Remote Services
=====================

|                                            |                              |
|--------------------------------------------|------------------------------|
| exporting a rmi service                    | RmiServiceExporter           |
| export Hessian service                     | HessianServiceExporter       |
| export Burlap service                      | BurlapServiceExorter         |
| export HTTP invoker service                | HttpInvokerServiceExporter.  |
| export JAX-WS web service                  | SimpleJaxWsServiceExporter   |
| use Xfire framework to export a webservice | XFireExporter.               |
| export webservice devloped by annotation   | Jsr181HandlerMapping         |
|                                            |                              |
| used for accessing a rmi service           | RmiProxyFactoryBean          |
| Hessian client proxy                       | HessianProxyFactoryBean      |
| Burlap client proxy                        | BurlapProxyFactoryBean       |
| HTTP invoker client proxy                  | HttpInvokerProxyFactoryBean  |
| JAX-WS client                              | JaxWsPortProxyFactoryBean,   |
| Xfire web service client                   | XfireClientFactoryBean       |
|                                            |                              |
| enable JAX-WS autowirng with spring bean   | SpringBeanAutowiringSupport, |

Spring-WS
=========

|                                                    |                                    |
|----------------------------------------------------|------------------------------------|
| servlet used to configure SOAP based               | MessageDispatcherServlet           |
|                                                    |                                    |
| to dynamically generate WSDL                       | DynamicWsdl11Definition            |
|                                                    |                                    |
|                                                    |                                    |
|                                                    |                                    |
| Spring-WS based client                             | WebServiceTemplate                 |
| it is like DAOsupport class for WebServiceTemplate | WebServiceGatewaySupport           |
|                                                    |                                    |
| for easy marshall / unmarshall in Spring-WS        | AbstractMarshallingPayloadEndpoint |

API - JMS
=========

|                                                                 |                                 |                |         |
|-----------------------------------------------------------------|---------------------------------|----------------|---------|
| dealing with boilerplate code of JMS                            | JmsTemplate ( JMS 1.1 )         |                |         |
| we implement this interface to create a message                 |                                 | MessageCreater |         |
|                                                                 |                                 |                | Message |
| it is used receive jmsTemplate like daosupport                  | JmsGatewaySupport               |                |         |
|                                                                 |                                 |                |         |
| like marhalling / unmarll jms message to java object            | MessageConverter                |                |         |
| convert JMS message to business object                          | SimpleMessageConvertor          |                |         |
|                                                                 |                                 |                |         |
| converty JMS exception to runtime and classify                  | JmsUtil                         |                |         |
|                                                                 |                                 |                |         |
| to give POJO, asynchronous message listener,without transaction | SimpleMessageListenerContainer  |                |         |
| to give POJO, asynchronous message listener,with transaction    | DefaultMessageListenerContainer |                |         |

API - JavaMail
==============

|                                           |                   |                    |
|-------------------------------------------|-------------------|--------------------|
|                                           | JavaMailSender    |                    |
| this has to be configured in XML file     |                   | JavaMailSenderImpl |
|                                           |                   |                    |
| to send simple message without attachment | SimpleMailMessage |                    |
|                                           | MimeMessage       |                    |
| to send attachment                        |                   | MimeMessageHelper  |

API - JMX
=========

|                                      |                             |
|--------------------------------------|-----------------------------|
| export a spring bean as Mbean        | MbeanExporter               |
|                                      |                             |
| used to start or locate Mbean server | MBeanServerFactoryBean.     |
|                                      |                             |
| used by Mbean Connector for remote   | ConnectorServerFactoryBean. |

API - schedule
==============

|                                       |                                    |
|---------------------------------------|------------------------------------|
| to define a timer task declatively    | MethodInvokingTimerTaskFactoryBean |
| schedule a tak                        | ScheduledTimerTask                 |
| start timer to execute scheduled task | TimerFactoryBean                   |
