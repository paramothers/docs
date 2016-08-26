

# API - Security 3.2

-   **DelegtingFilterProxy**, it is filter and delegate filtering logic to a spring Bean type (FilterChainProxy).
    -   **FilterChainProxy**, type of spring bean, which do actual filtering

**AbstractSecurityWebApplicationInitializer**, has to extend for java based configuration

-   **WebSecurityConfigurer**
    -   **WebSecurityConfigurerAdaptor**, is a spring bean, to configure spring security and annotated with **@EnableWebSecurity**
-   AuthenticationBuilder
-   UserDetailServices

-   **GlobalMethodSecurityConfiguration**, it is much like WebSecurityConfigurerAdaptor



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

|                                          |                           |                            |
| ---------------------------------------- | ------------------------- | -------------------------- |
| exporting Spring bean as a rmi service   |                           | RmiServiceExporter         |
| export Hessian service                   |                           | HessianServiceExporter     |
|                                          | HessianServlet            |                            |
| export Burlap service                    |                           | BurlapServiceExporter      |
| export HTTP invoker service              |                           | HttpInvokerServiceExporter |
| export JMS based RCP service             |                           | JmsInvokerServiceExporter  |
| export JAX-WS 2.0 web service            | SpringBeanAutowireSupport |                            |
|                                          |                           | SimpleJaxWsServiceExporter |
| use Xfire framework to export a webservice |                           | XFireExporter              |
| export webservice devloped by annotation |                           | Jsr181HandlerMapping       |

# API - Remote service Client

|                                          |                             |
| ---------------------------------------- | --------------------------- |
| used for accessing a rmi service         | RmiProxyFactoryBean         |
| Hessian client proxy                     | HessianProxyFactoryBean     |
| Burlap client proxy                      | BurlapProxyFactoryBean      |
| HTTP invoker client proxy                | HttpInvokerProxyFactoryBean |
| JAX-WS client                            | JaxWsPortProxyFactoryBean   |
| Xfire web service client                 | XfireClientFactoryBean      |
| jms based rcp client                     | JmsInvokerProxyFactoryBean  |
| enable JAX-WS autowirng with spring bean | SpringBeanAutowiringSupport |



# API - JMX

|                                      |                             |
| ------------------------------------ | --------------------------- |
| export a spring bean as Mbean        | MbeanExporter               |
| used to start or locate Mbean server | MBeanServerFactoryBean.     |
| used by Mbean Connector for remote   | ConnectorServerFactoryBean. |

# API - schedule

|                                       |                                    |
| ------------------------------------- | ---------------------------------- |
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

|                                          |                   |                    |
| ---------------------------------------- | ----------------- | ------------------ |
|                                          | JavaMailSender    |                    |
| it use JavaMail API, to use to send email |                   | JavaMailSenderImpl |
|                                          | MailSession       |                    |
| to send simple message without attachment | SimpleMailMessage |                    |
|                                          | MimeMessage       |                    |
| to send attachment                       |                   | MimeMessageHelper  |

# API - Unit test

+ TextContextManager
  + TestContext
    + **ContextLoader**, it load spring context
      + **SmartContextLoader**, support @ActiveProfile
  + **TestExecutionListener**, it heart of test execution class
+ **SpringJUnit4ClassRunner**,  one of Junit Runner.
+ AbstractSpringContextTests
  + AbstractDependencyInjectionSpringContextTests
  + AbstractTransactionalSpringContextTests
    + AbstractTransactionalDataSourceSpringContextTests
      + AbstractAnnotationAwareTransactionalTests

# API - Exception

|                              |                                |
| ---------------------------- | ------------------------------ |
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

# Validation Framework

+ Validator
  + LocalValidatorFactoryBean
+ BindingResult