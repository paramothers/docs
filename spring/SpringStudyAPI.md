BeanFactory typed Containers
============================

|                     |                            |                                |                |                        |                     |
|---------------------|----------------------------|--------------------------------|----------------|------------------------|---------------------|
| BeanFactory         |                            |                                |                |                        |                     |
|                     | DefaultListableBeanFactory |                                |                |                        |                     |
|                     |                            | XMLBeanFactory                 |                |                        |                     |
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
|                                | ContextLoader                                                                                |                                  |                                                        |
|                                |                                                                                              | ContextLoaderListener            |                                                        |
|                                |                                                                                              | ContextLoaderServlet             |                                                        |
|                                |                                                                                              | ApplicationContextAwareProcessor |                                                        |
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

6. Bean<span style="color: rgb(45, 229, 45);">PostProcessor</span>(
   Pre-Initialization )

7. InitializingBean's afterPropertiesSet();

8. call custom init-method

9. Bean<span style="color: rgb(45, 229, 45);">PostProcessor</span>( Post
- Initialization )

( Live Bean in Application context )

1. DisposableBean

2. custom-destory method

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


API - Web
=========

Servlet Container Initializer
=============================

+ **javax.servlet.ServletContainerInitializer**, this type given by
  Servlet 3.0, to initialize container
    + **SpringServletContainerInitializer**, spring provide default
      implementation of `ServletContainerInitializer`
        + **WebApplicationInitializer**, we can implements when we need
          to configure more application serverlts, filters, Listeners
            + AbstractDispatcherServletInitializer
            +  **AbstractAnnotationConfigDispatcherServletInitializer**,
               one of the implementation of `WebApplicationInitializer`
               dispatch servlet config automatically by Javaconfig
                + (App specific servlet container initialzier)


+ WebApplicationContext
    + **AnnotationConfigWebApplicationContext**, load javaconfig for
      Spring MVC by web.xml

+ **MultipartResolver**, used to parse multipart request
    + **CommonsMultipartResolver**, use Common File upload library
    + **StandardServletMultipartResolver**, use container support of
      Servlet 3.0
+ MultipartFile
+ HandlerMapping
    + SimpleUrlHandlerMapping


Spring MVC tool-bean configure (Web initializer is first step . Web MVC configurer is second step )
===================================================================================================

+ WebMvcConfigurer
    + **WebMvcConfigurerAdapter**, configure Spring MVC tools. it is
      used by WebApplicationInitializer
        + (app MVC config class), annotated with **@EnableSpringMvc**


Spring View implementation
==========================

+ View
    + AbstractExcelView
    + AbstractPdfView
    + AbstractView
    + JstlView


+ ViewResolver
    + **InternalResourceViewResolver**, to resolve JSP files as view
    + ContentNegotiatingViewResolver
    + UrlBasedViewResolver
    + **BeanNameViewResolver**, to resolve Bean ID
    + XmlViewResolver
    + XsltViewResolver
    + ResourceBundleViewResolver
        + FreeMarkerViewResolver
        + JasperReportsViewResolver
        + TilesViewResolver
        + VelocityLayoutViewResolver
        + VelocityViewResolver

+ Model , it is just like a map and to add attribute by controller
  method
+ **Errors**, any POJO validation error
+ ResourceBundleMessageSource
+ ReloadableResourceBundleMessageSource


API - web flow
==============

+ **FlowHandlerMapping**, it forward request from DispatcherServlet to
  Spring Web flow based on url
+ **FlowHandlerAdapter**, it is like mvc controller

API - Rest
==========

|                                       |  |                           |  |  |
|---------------------------------------|--|---------------------------|--|--|
|                                       |  | HttpMethodConverter       |  |  |
|                                       |  | RestTemplate              |  |  |
|                                       |  | ContentNegotiationManager |  |  |
| it carry metadata about http response |  | ResponseEntity            |  |  |
|                                       |  | HttpStatus                |  |  |
|                                       |  | HttpHeaders               |  |  |

API - Security 3.2
==================

+ **DelegtingFilterProxy**, it is filter and delegate filtering logic to
  a spring Bean type (FilterChainProxy).
    + **FilterChainProxy**, type of spring bean, which do actual
      filtering

**AbstractSecurityWebApplicationInitializer**, has to extend for java
based configuration

+ **WebSecurityConfigurer**
    + **WebSecurityConfigurerAdaptor**, is a spring bean, to configure
      spring security and annotated with **@EnableWebSecurity**

+ AuthenticationBuilder
+ UserDetailServices


+ **GlobalMethodSecurityConfiguration**, it is much like
  WebSecurityConfigurerAdaptor

API - Persistence
=================

#### Datasource ####

1. **BasicDataSource**, is from apache data source (apache common )
2. **DriverManagerDataSource**, is from spring by driver based with out
   pooling, new connection every call.
3. **SimpleDataSource**, is from spring for osgi container environment
4. **SingleConnectionDataSource**, is from spring, same connection
   return for all call.
5. EmbeddedDataSourceBuilder

#### Template ####

+ JdbcOperation, is a interface
    1. JdbcTemplate
+ NamedParameterJdbcOperation, is a interface    
    1. NamedParameterJdbcTemplate


API - Hibernate Integration
===========================

+ LocalSessionFactoryBean ( use hibernate 4 and above)
+ AnnotationSessionFactoryBean ( use < hibernate 4 version)


API - JPA
=========

+ PersistenceProvider
    + EntityManagerFactory
        + EntityManager

+ ~~LocalEntityManagerFactoryBean~~, Dont use since all the DB
  configurtion depends on persistence.xml
+ **LocalContainerEntityManagerFactoryBean**, it can use datasource,
  jpavendor exist in SpringContext.

+ JpaVendorAdaptor
    + **HibernateJpaVendorAdaptor**, use Hibernate as jpa implementation
    + **EclipseLinkJpaVendorAdaptor**, use when eclipselink as jpa
      implementation
    + OpenJpaVendorAdaptor

+ **PersistenceAnnotationBeanPostProcessor**, to work with JPA specific
  PersistenceUnit/Context annotation
+ **PersistenceExceptionTranslationPostProcessor**, to translate
  exception to spring specefic exception when template are not used in
  Hibernate/JPA


API- Spring Data - JPA
======================

* Repository
    * JpaRepository
    * PagingAndSortingRepository
    * CrudRepository


API - Spring data-mongodb
=========================

* AbstractMongoConfiguration
* MongoOperations
    * MongoTemplate
    * Query
* MongoRepository


API - Sprig Caching
===================

+ CacheManager
    + SimpleCacheManager
    + NoOpCacheManager
    + ConcurrentMapCacheManager
    + CompositeCacheManager
    + EhCacheCacheManager
    + RedisCacheManager
    + GemfireCacheManager


API - Remote Services
=====================


+ **Remote Procedure call ( RPC ) Models**
    +  Remote Method Invocation (RMI)
    +  Spring HTTP's invoker
    +  JAX-WS web service
    +  Hessian or Burlap
    +  JMS based RCP

API - Remote service Endpoint
=============================

|                                            |                           |                            |
|--------------------------------------------|---------------------------|----------------------------|
| exporting Spring bean as a rmi service     |                           | RmiServiceExporter         |
| export Hessian service                     |                           | HessianServiceExporter     |
|                                            | HessianServlet            |                            |
| export Burlap service                      |                           | BurlapServiceExporter      |
| export HTTP invoker service                |                           | HttpInvokerServiceExporter |
| export JMS based RCP service               |                           | JmsInvokerServiceExporter  |
| export JAX-WS 2.0 web service              | SpringBeanAutowireSupport |                            |
|                                            |                           | SimpleJaxWsServiceExporter |
| use Xfire framework to export a webservice |                           | XFireExporter              |
| export webservice devloped by annotation   |                           | Jsr181HandlerMapping       |


API - Remote service Client
===========================

|                                          |                             |
|------------------------------------------|-----------------------------|
| used for accessing a rmi service         | RmiProxyFactoryBean         |
| Hessian client proxy                     | HessianProxyFactoryBean     |
| Burlap client proxy                      | BurlapProxyFactoryBean      |
| HTTP invoker client proxy                | HttpInvokerProxyFactoryBean |
| JAX-WS client                            | JaxWsPortProxyFactoryBean   |
| Xfire web service client                 | XfireClientFactoryBean      |
| jms based rcp client                     | JmsInvokerProxyFactoryBean  |
| enable JAX-WS autowirng with spring bean | SpringBeanAutowiringSupport |


API - Transaction
=================

|  |                                                                                                    |                             |                              |                                    |
|--|----------------------------------------------------------------------------------------------------|-----------------------------|------------------------------|------------------------------------|
|  | offers a set of technology-independent facilities, including transaction managers (interface )     |                             | PlatformTransactionManager   |                                    |
|  | for JDBC, Spring JDBC , ibATIS, to provide transaction, single database                            |                             |                              | DataSourceTransactionManager       |
|  | for JEE server's transaction implementation usage.                                                 |                             |                              | JtaTransactionManager              |
|  |                                                                                                    |                             |                              | JpaTransactionManager              |
|  |                                                                                                    |                             |                              | HibernateTransactionManager        |
|  |                                                                                                    |                             |                              | TransactionSysnchronizationManager |
|  |                                                                                                    |                             |                              | JdoTransactionManager              |
|  | it is used in Spring-Batch on-memory repository                                                    |                             |                              | ResourcelessTransactionManager     |
|  | Easy the programmatic style transaction                                                            | TransactionTemplate         |                              |                                    |
|  | It used to define anonymous class                                                                  |                             | TransactionCallback          |                                    |
|  | when no need, return a object.                                                                     |                             |                              | TransactionCallbackWithoutResult   |
|  |                                                                                                    | TransactionProxyFactoryBean |                              |                                    |
|  | it just interface                                                                                  | TransactionDefinition       |                              |                                    |
|  | it will hold all the transaction attributes. There are 5 different attributes are, can be defined. |                             | DefaultTransactionDefinition |                                    |
|  |                                                                                                    | TransactionStatus           |                              |                                    |


API - JMX
=========

|                                      |                             |
|--------------------------------------|-----------------------------|
| export a spring bean as Mbean        | MbeanExporter               |
| used to start or locate Mbean server | MBeanServerFactoryBean.     |
| used by Mbean Connector for remote   | ConnectorServerFactoryBean. |

API - schedule
==============

|                                       |                                    |
|---------------------------------------|------------------------------------|
| to define a timer task declatively    | MethodInvokingTimerTaskFactoryBean |
| schedule a tak                        | ScheduledTimerTask                 |
| start timer to execute scheduled task | TimerFactoryBean                   |


Spring-WS
=========

|                                                    |                                    |
|----------------------------------------------------|------------------------------------|
| servlet used to configure SOAP based               | MessageDispatcherServlet           |
| to dynamically generate WSDL                       | DynamicWsdl11Definition            |
| Spring-WS based client                             | WebServiceTemplate                 |
| it is like DAOsupport class for WebServiceTemplate | WebServiceGatewaySupport           |
| for easy marshall / unmarshall in Spring-WS        | AbstractMarshallingPayloadEndpoint |

API - JMS
=========

Two main components are

1. MessageBrokers (Message Server)
2. Destination (Queu/Topic)

|                                                                 |                                 |                                 |         |
|-----------------------------------------------------------------|---------------------------------|---------------------------------|---------|
| dealing with boilerplate code of JMS & handle JMSException      | JmsOperations                   |                                 |         |
| dealing with boilerplate code of JMS & handle JMSException      |                                 | JmsTemplate ( JMS 1.1 )         |         |
| we implement this interface to create a message                 |                                 | MessageCreator                  |         |
|                                                                 |                                 |                                 | Message |
| it is used receive jmsTemplate like daosupport                  | JmsGatewaySupport               |                                 |         |
| like marhalling / unmarll jms message to java object            | MessageConverter                |                                 |         |
| convert JMS message to text object                              |                                 | SimpleMessageConverter          |         |
| convert JMS message to JSON object                              |                                 | MappingJacksonMessageConverter  |         |
| convert JMS message to JSON2 object                             |                                 | MappingJackson2MessageConverter |         |
| convert JMS message to XML object                               |                                 | MarshallingMessageConverter     |         |
| convert JMS exception to runtime and classify                   | JmsUtils                        |                                 |         |
| to give POJO, asynchronous message listener,without transaction | SimpleMessageListenerContainer  |                                 |         |
| to give POJO, asynchronous message listener,with transaction    | DefaultMessageListenerContainer |                                 |         |


API - WebSocket & STOMP
=======================

+ WebSocketHandler
    + AbstractWebSocketHandler
        + TextWebSocketHandler
        + BinaryWebSocketHandler
    + WebSocketSession
    + WebSocketMessage
        + TextMessage
+ WebSocketConfigurer



API - JavaMail
==============

|                                           |                   |                    |
|-------------------------------------------|-------------------|--------------------|
|                                           | JavaMailSender    |                    |
| it use JavaMail API, to use to send email |                   | JavaMailSenderImpl |
|                                           | MailSession       |                    |
| to send simple message without attachment | SimpleMailMessage |                    |
|                                           | MimeMessage       |                    |
| to send attachment                        |                   | MimeMessageHelper  |


API - Unit test
===============

|                           |                            |                                               |                                                   |                                           |
|---------------------------|----------------------------|-----------------------------------------------|---------------------------------------------------|-------------------------------------------|
|                           | AbstractSpringContextTests |                                               |                                                   |                                           |
|                           |                            | AbstractDependencyInjectionSpringContextTests |                                                   |                                           |
|                           |                            | AbstractTransactionalSpringContextTests       |                                                   |                                           |
|                           |                            |                                               | AbstractTransactionalDataSourceSpringContextTests |                                           |
|                           |                            |                                               |                                                   | AbstractAnnotationAwareTransactionalTests |
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
| statless remote session â€“ client                 | SimpleRemoteStatelessSessionProxyFactoryBean ( EJB 2.x) | handle checkeced exception |
| statless local session â€“ client                  | LocalStatelessSessionProxyFactoryBean ( EJB 2.x)        |                            |
| it allow, a EJB, to use Spring application context | SpringBeanAutowiringInterceptor ( EJB 3.x)              |                            |
