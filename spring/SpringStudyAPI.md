# BeanFactory typed Containers

|                     |                            |                                |                |                        |                     |
|---------------------|----------------------------|--------------------------------|----------------|------------------------|---------------------|
| BeanFactory         |                            |                                |                |                        |                     |
|                     | DefaultListableBeanFactory |                                |                |                        |                     |
|                     |                            | fgfgXMLBeanFactory                 |                |                        |                     |
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

# ApplicationContext typed Container

<table>
<colgroup>
<col width="15%" />
<col width="43%" />
<col width="15%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td>ApplicationContext</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>ConfigurableApplicationContext</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><del>ClassPathXmlApplicationContext</del></td>
<td></td>
<td>Load configuration from classpath</td>
</tr>
<tr class="even">
<td></td>
<td><del>FileSystemXmlApplicationContext</del></td>
<td></td>
<td>Load configuration from filesystem</td>
</tr>
<tr class="odd">
<td></td>
<td><del>XmlPortletApplicationContext</del></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><del>WebApplicationContext</del></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><del>XmlWebApplicationContext</del></td>
<td>Load configuration from war file</td>
</tr>
<tr class="even">
<td></td>
<td><span style="background-color: rgb(0, 255, 0);">AnnotationConfigApplicationContext</span></td>
<td></td>
<td>Load configuration from JavaConfig</td>
</tr>
<tr class="odd">
<td></td>
<td><span style="background-color: rgb(0, 255, 0);">AnnotationWebConfigApplicationContext</span></td>
<td></td>
<td>Load configuration from JavaConfig for web application</td>
</tr>
<tr class="even">
<td></td>
<td>ContextLoader</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td>ContextLoaderListener</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>ContextLoaderServlet</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td>ApplicationContextAwareProcessor</td>
<td></td>
</tr>
<tr class="even">
<td>LoadTimeWeaverAware</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>MessageSourceAware</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>ApplicationEventPublisherAware</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>ResourceLoaderAware</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>LifeCycle</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>ApplicationEvent</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>ApplicationListener</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>ApplicationEventPublisher</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>ContextClosedEvent</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td>ContextRefreshedEvent</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>RequestHandledEvent</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>ApplicationEventMulticaster</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>BeanNameGenerator</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

# Bean life-cycle API

Bean life-cycle phases

1.  Instantiate

2.  populate properties

3.  BeanName<span style="color: rgb(255, 0, 0);">Aware</span>

4.  BeanFactory<span style="color: rgb(255, 0, 0);">Aware</span>

5.  ApplicationContext<span style="color: rgb(255, 0, 0);">Aware</span>

6.  Bean<span style="color: rgb(45, 229, 45);">PostProcessor</span>( Pre-Initialization )

7.  InitializingBean's afterPropertiesSet();

8.  call custom init-method

9.  Bean<span style="color: rgb(45, 229, 45);">PostProcessor</span>( Post

-   Initialization )

( Live Bean in Application context )

1.  DisposableBean

2.  custom-destory method

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

# API - Web

# Servlet Container Initializer

-   **javax.servlet.ServletContainerInitializer**, this type given by Servlet 3.0, to initialize container
    -   **SpringServletContainerInitializer**, spring provide default implementation of `ServletContainerInitializer`
        -   **WebApplicationInitializer**, we can implements when we need to configure more application serverlts, filters, Listeners
            -   AbstractDispatcherServletInitializer
            -   **AbstractAnnotationConfigDispatcherServletInitializer**, one of the implementation of `WebApplicationInitializer` dispatch servlet config automatically by Javaconfig
                -   (App specific servlet container initialzier)
-   WebApplicationContext
    -   **AnnotationConfigWebApplicationContext**, load javaconfig for Spring MVC by web.xml
-   **MultipartResolver**, used to parse multipart request
    -   **CommonsMultipartResolver**, use Common File upload library
    -   **StandardServletMultipartResolver**, use container support of Servlet 3.0
-   MultipartFile
-   HandlerMapping
    -   SimpleUrlHandlerMapping

# Spring MVC tool-bean configure (Web initializer is first step . Web MVC configurer is second step )

-   WebMvcConfigurer
    -   **WebMvcConfigurerAdapter**, configure Spring MVC tools. it is used by WebApplicationInitializer
        -   (app MVC config class), annotated with **@EnableSpringMvc**

# Spring View implementation

-   View
    -   AbstractExcelView
    -   AbstractPdfView
    -   AbstractView
    -   JstlView
-   ViewResolver
    -   **InternalResourceViewResolver**, to resolve JSP files as view
    -   ContentNegotiatingViewResolver
    -   UrlBasedViewResolver
    -   **BeanNameViewResolver**, to resolve Bean ID
    -   XmlViewResolver
    -   XsltViewResolver
    -   ResourceBundleViewResolver
        -   FreeMarkerViewResolver
        -   JasperReportsViewResolver
        -   TilesViewResolver
        -   VelocityLayoutViewResolver
        -   VelocityViewResolver
-   Model , it is just like a map and to add attribute by controller method
-   **Errors**, any POJO validation error
-   ResourceBundleMessageSource
-   ReloadableResourceBundleMessageSource

# API - web flow

-   **FlowHandlerMapping**, it forward request from DispatcherServlet to Spring Web flow based on url
-   **FlowHandlerAdapter**, it is like mvc controller

# API - Rest

|                                       |     |                           |     |     |
|---------------------------------------|-----|---------------------------|-----|-----|
|                                       |     | HttpMethodConverter       |     |     |
|                                       |     | RestTemplate              |     |     |
|                                       |     | ContentNegotiationManager |     |     |
| it carry metadata about http response |     | ResponseEntity            |     |     |
|                                       |     | HttpStatus                |     |     |
|                                       |     | HttpHeaders               |     |     |

# API - Security 3.2

-   **DelegtingFilterProxy**, it is filter and delegate filtering logic to a spring Bean type (FilterChainProxy).
    -   **FilterChainProxy**, type of spring bean, which do actual filtering

**AbstractSecurityWebApplicationInitializer**, has to extend for java based configuration

-   **WebSecurityConfigurer**
    -   **WebSecurityConfigurerAdaptor**, is a spring bean, to configure spring security and annotated with **@EnableWebSecurity**
-   AuthenticationBuilder
-   UserDetailServices

-   **GlobalMethodSecurityConfiguration**, it is much like WebSecurityConfigurerAdaptor

# API - Persistence

#### Datasource

1.  **BasicDataSource**, is from apache data source (apache common )
2.  **DriverManagerDataSource**, is from spring by driver based with out pooling, new connection every call.
3.  **SimpleDataSource**, is from spring for osgi container environment
4.  **SingleConnectionDataSource**, is from spring, same connection return for all call.
5.  EmbeddedDataSourceBuilder

#### Template

-   JdbcOperation, is a interface
    1.  JdbcTemplate
-   NamedParameterJdbcOperation, is a interface
    1.  NamedParameterJdbcTemplate

# API - Hibernate Integration

-   LocalSessionFactoryBean ( use hibernate 4 and above)
-   AnnotationSessionFactoryBean ( use &lt; hibernate 4 version)

# API - JPA

-   PersistenceProvider
    -   EntityManagerFactory
        -   EntityManager
-   ~~LocalEntityManagerFactoryBean~~, Dont use since all the DB configurtion depends on persistence.xml
-   **LocalContainerEntityManagerFactoryBean**, it can use datasource, jpavendor exist in SpringContext.

-   JpaVendorAdaptor
    -   **HibernateJpaVendorAdaptor**, use Hibernate as jpa implementation
    -   **EclipseLinkJpaVendorAdaptor**, use when eclipselink as jpa implementation
    -   OpenJpaVendorAdaptor
-   **PersistenceAnnotationBeanPostProcessor**, to work with JPA specific PersistenceUnit/Context annotation
-   **PersistenceExceptionTranslationPostProcessor**, to translate exception to spring specefic exception when template are not used in Hibernate/JPA

# API- Spring Data - JPA

-   Repository
    -   JpaRepository
    -   PagingAndSortingRepository
    -   CrudRepository

# API - Spring data-mongodb

-   AbstractMongoConfiguration
-   MongoOperations
    -   MongoTemplate
    -   Query
-   MongoRepository

# API - Sprig Caching

-   CacheManager
    -   SimpleCacheManager
    -   NoOpCacheManager
    -   ConcurrentMapCacheManager
    -   CompositeCacheManager
    -   EhCacheCacheManager
    -   RedisCacheManager
    -   GemfireCacheManager

# API - Remote Services

-   **Remote Procedure call ( RPC ) Models**
    -   Remote Method Invocation (RMI)
    -   Spring HTTP's invoker
    -   JAX-WS web service
    -   Hessian or Burlap
    -   JMS based RCP

# API - Remote service Endpoint

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

# API - Remote service Client

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

# API - Transaction

<table style="width:100%;">
<colgroup>
<col width="1%" />
<col width="49%" />
<col width="14%" />
<col width="15%" />
<col width="18%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td>offers a set of technology-independent facilities, including transaction managers (interface )</td>
<td></td>
<td>PlatformTransactionManager</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>for JDBC, Spring JDBC , ibATIS, to provide transaction, single database</td>
<td></td>
<td></td>
<td>DataSourceTransactionManager</td>
</tr>
<tr class="odd">
<td></td>
<td>for JEE server's transaction implementation usage.</td>
<td></td>
<td></td>
<td>JtaTransactionManager</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td>JpaTransactionManager</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td>HibernateTransactionManager</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td>TransactionSysnchronizationManager</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td>JdoTransactionManager</td>
</tr>
<tr class="even">
<td></td>
<td>it is used in Spring-Batch on-memory repository</td>
<td></td>
<td></td>
<td>ResourcelessTransactionManager</td>
</tr>
<tr class="odd">
<td></td>
<td>Easy the programmatic style transaction</td>
<td>TransactionTemplate</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>It used to define anonymous class</td>
<td></td>
<td>TransactionCallback</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td>when no need, return a object.</td>
<td></td>
<td></td>
<td>TransactionCallbackWithoutResult</td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>TransactionProxyFactoryBean</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td>it just interface</td>
<td>TransactionDefinition</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>it will hold all the transaction attributes. There are 5 different attributes are, can be defined.</td>
<td></td>
<td>DefaultTransactionDefinition</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td>TransactionStatus</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

# API - JMX

|                                      |                             |
|--------------------------------------|-----------------------------|
| export a spring bean as Mbean        | MbeanExporter               |
| used to start or locate Mbean server | MBeanServerFactoryBean.     |
| used by Mbean Connector for remote   | ConnectorServerFactoryBean. |

# API - schedule

|                                       |                                    |
|---------------------------------------|------------------------------------|
| to define a timer task declatively    | MethodInvokingTimerTaskFactoryBean |
| schedule a tak                        | ScheduledTimerTask                 |
| start timer to execute scheduled task | TimerFactoryBean                   |

# Spring-WS

<table>
<colgroup>
<col width="58%" />
<col width="41%" />
</colgroup>
<tbody>
<tr class="odd">
<td>servlet used to configure SOAP based</td>
<td>MessageDispatcherServlet</td>
</tr>
<tr class="even">
<td>to dynamically generate WSDL</td>
<td>DynamicWsdl11Definition</td>
</tr>
<tr class="odd">
<td>Spring-WS based client</td>
<td>WebServiceTemplate</td>
</tr>
<tr class="even">
<td>it is like DAOsupport class for WebServiceTemplate</td>
<td>WebServiceGatewaySupport</td>
</tr>
<tr class="odd">
<td>for easy marshall / unmarshall in Spring-WS</td>
<td>AbstractMarshallingPayloadEndpoint</td>
</tr>
</tbody>
</table>

# API - JMS

Two main components are

1.  MessageBrokers (Message Server)
2.  Destination (Queu/Topic)

<table>
<colgroup>
<col width="45%" />
<col width="23%" />
<col width="23%" />
<col width="6%" />
</colgroup>
<tbody>
<tr class="odd">
<td>dealing with boilerplate code of JMS &amp; handle JMSException</td>
<td>JmsOperations</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>dealing with boilerplate code of JMS &amp; handle JMSException</td>
<td></td>
<td>JmsTemplate ( JMS 1.1 )</td>
<td></td>
</tr>
<tr class="odd">
<td>we implement this interface to create a message</td>
<td></td>
<td>MessageCreator</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td>Message</td>
</tr>
<tr class="odd">
<td>it is used receive jmsTemplate like daosupport</td>
<td>JmsGatewaySupport</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>like marhalling / unmarll jms message to java object</td>
<td>MessageConverter</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>convert JMS message to text object</td>
<td></td>
<td>SimpleMessageConverter</td>
<td></td>
</tr>
<tr class="even">
<td>convert JMS message to JSON object</td>
<td></td>
<td>MappingJacksonMessageConverter</td>
<td></td>
</tr>
<tr class="odd">
<td>convert JMS message to JSON2 object</td>
<td></td>
<td>MappingJackson2MessageConverter</td>
<td></td>
</tr>
<tr class="even">
<td>convert JMS message to XML object</td>
<td></td>
<td>MarshallingMessageConverter</td>
<td></td>
</tr>
<tr class="odd">
<td>convert JMS exception to runtime and classify</td>
<td>JmsUtils</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>to give POJO, asynchronous message listener,without transaction</td>
<td>SimpleMessageListenerContainer</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>to give POJO, asynchronous message listener,with transaction</td>
<td>DefaultMessageListenerContainer</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

# API - WebSocket

-   WebSocketHandler
    -   AbstractWebSocketHandler
        -   TextWebSocketHandler
        -   BinaryWebSocketHandler
    -   WebSocketSession
    -   WebSocketMessage
        -   TextMessage
-   WebSocketConfigurer

# API - STOMP

-   AbstractWebSocketMessageBrokerConfigurer
-   StompEndpointRegistry
-   MessageBrokerRegistry

# API - JavaMail

|                                           |                   |                    |
|-------------------------------------------|-------------------|--------------------|
|                                           | JavaMailSender    |                    |
| it use JavaMail API, to use to send email |                   | JavaMailSenderImpl |
|                                           | MailSession       |                    |
| to send simple message without attachment | SimpleMailMessage |                    |
|                                           | MimeMessage       |                    |
| to send attachment                        |                   | MimeMessageHelper  |

# API - Unit test

|                           |                            |                                               |                                                   |                                           |
|---------------------------|----------------------------|-----------------------------------------------|---------------------------------------------------|-------------------------------------------|
|                           | AbstractSpringContextTests |                                               |                                                   |                                           |
|                           |                            | AbstractDependencyInjectionSpringContextTests |                                                   |                                           |
|                           |                            | AbstractTransactionalSpringContextTests       |                                                   |                                           |
|                           |                            |                                               | AbstractTransactionalDataSourceSpringContextTests |                                           |
|                           |                            |                                               |                                                   | AbstractAnnotationAwareTransactionalTests |
| Good for integration test | SpringJUnit4ClassRunner    |                                               |                                                   |                                           |

# API - Exception

|                              |                                |
|------------------------------|--------------------------------|
|                              | BeanCreationException          |
| I will get when use Autowire | UnsatisfiedDependencyException |
|                              | NoSuchBeanDefinitionException  |

# API - EJB

<table>
<colgroup>
<col width="37%" />
<col width="41%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td>EJB 2.1 statless session bean</td>
<td>AbstractStatelessSessionBean ( EJB 2.x)</td>
<td>no boiler plate code</td>
</tr>
<tr class="even">
<td>EJB 2.1 stateful session bean</td>
<td>AbstractStatefulSessionBean ( EJB 2.x)</td>
<td></td>
</tr>
<tr class="odd">
<td>EJB 2.1 general Message driven bean</td>
<td>AbstractJMSMessageDrivenBean ( EJB 2.x)</td>
<td></td>
</tr>
<tr class="even">
<td>EJB 2.1 JMS message driven bean</td>
<td>AbstractMessageDrivenBean ( EJB 2.x)</td>
<td></td>
</tr>
<tr class="odd">
<td>statless remote session â€“ client</td>
<td>SimpleRemoteStatelessSessionProxyFactoryBean ( EJB 2.x)</td>
<td>handle checkeced exception</td>
</tr>
<tr class="even">
<td>statless local session â€“ client</td>
<td>LocalStatelessSessionProxyFactoryBean ( EJB 2.x)</td>
<td></td>
</tr>
<tr class="odd">
<td>it allow, a EJB, to use Spring application context</td>
<td>SpringBeanAutowiringInterceptor ( EJB 3.x)</td>
<td></td>
</tr>
</tbody>
</table>


