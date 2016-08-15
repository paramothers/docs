
EJB 3.1
=======

|                                                                              |                             |                           |     |       |                  |                          |               |
|------------------------------------------------------------------------------|-----------------------------|---------------------------|-----|-------|------------------|--------------------------|---------------|
|                                                                              | @Stateless                  |                           |     | name  | mappedBy         |                          |               |
|                                                                              | @Stateful                   |                           |     | name  |                  |                          |               |
|                                                                              | @Remove                     |                           |     |       |                  |                          |               |
|                                                                              | @PrePassivate               |                           |     |       |                  |                          |               |
|                                                                              | @PostActivate               |                           |     |       |                  |                          |               |
|                                                                              | @Singleton                  |                           |     |       |                  |                          |               |
|                                                                              | @Startup                    |                           |     |       |                  |                          |               |
|                                                                              | @ConcurrencyManagement      |                           |     |       |                  |                          |               |
|                                                                              | @Lock                       |                           |     |       |                  |                          |               |
|                                                                              | @AccessTimeout              |                           |     | value | unit             |                          |               |
|                                                                              | @MessageDriven              |                           |     | name  | activationConfig | messageListenerInterface |               |
|                                                                              |                             | @ActivationConfigProperty |     |       | propertyName     | propertyValue            |               |
|                                                                              | @Asynchronous               |                           |     |       |                  |                          |               |
|                                                                              | @Local                      |                           |     |       |                  |                          |               |
|                                                                              | @Remote                     |                           |     |       |                  |                          |               |
|                                                                              | @WebService                 |                           |     |       |                  |                          |               |
|                                                                              | *@LocalBean*                |                           |     |       |                  |                          |               |
|                                                                              | *@LocalHome*                |                           |     |       |                  |                          |               |
|                                                                              | *@RemoteHome*               |                           |     |       |                  |                          |               |
| one of the usage of this annotation is, to plug Spring context in a EJB bean | @Interceptors               |                           |     |       |                  |                          |               |
|                                                                              | @AroundInvoke               |                           |     |       |                  |                          |               |
|                                                                              | @ExcludeDefaultInterceptors |                           |     |       |                  |                          |               |
|                                                                              | @ExcludeClassInterceptors   |                           |     |       |                  |                          |               |
|                                                                              | @Timeout                    |                           |     |       |                  |                          |               |
|                                                                              | @TransactionManagement      |                           |     |       |                  |                          |               |
|                                                                              | @TransactionAttribute       |                           |     |       |                  |                          |               |
|                                                                              | @ApplicationException       |                           |     |       | rollback         |                          |               |
|                                                                              | @EJB                        |                           |     | name  | beanName         | mappedName               | beanInterface |
|                                                                              | @Resource                   |                           |     | name  | type             | mappedName               |               |
|                                                                              |                             |                           |     |       |                  |                          |               |
|                                                                              |                             | **GENERAL ANNOTATION**    |     |       |                  |                          |               |
|                                                                              | @DeclareRoles               |                           |     |       |                  |                          |               |
|                                                                              | @RolesAllowed               |                           |     |       |                  |                          |               |
|                                                                              | @PermitAll                  |                           |     |       |                  |                          |               |
|                                                                              | @DenyAll                    |                           |     |       |                  |                          |               |
|                                                                              | @RunAs                      |                           |     |       |                  |                          |               |

Gradle 2.3
==========

|             |
|-------------|
| @TaskAction |

Bean validation
===============

|             |     |     |         |          |
|-------------|-----|-----|---------|----------|
| size        |     |     | max     | min      |
| NotNull     |     |     | message |          |
| Past        |     |     |         |          |
| Null        |     |     |         |          |
| AssertTrue  |     |     |         |          |
| AssertFalse |     |     |         |          |
| Min         |     |     | value   |          |
| Max         |     |     | value   |          |
| DecimalMin  |     |     | value   |          |
| DecimalMax  |     |     | value   |          |
| Digits      |     |     | integer | fraction |
| Future      |     |     |         |          |
| pattern     |     |     | regexpr | flag     |

Java Dependency
===============

|                         |                                                                                                                                                              |            |      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|------|
| supported in Spring 3.1 | use this not to dependency with spring. It provide same facility like Autowired .It introduced by sun, implemented in spring 3.0                             | @inject    |      |
| supported in Spring 3.1 | it is Java dependency injection. It helps to indentify bean by its id and <span style="color: rgb(51, 255, 51);">alternative to @Component annotation</span> | @Named     |      |
| supported in Spring 3.1 | it cannot be used directly, but it can be used to define custom qualifier annotation                                                                         | @Qualifier | name |

Java Common Annotations
=======================

|                         |                                                                                                    |                |
|-------------------------|----------------------------------------------------------------------------------------------------|----------------|
| supported in Spring 3.0 | it is java common annotation supported in spring 2.5. Used to as same purpose @Autowire annotation | @Resource      |
| supported in Spring 3.0 | use instead of implementing InitializingBean interfaces or init-method in xml file                 | @Postconstruct |
| supported in Spring 3.0 | use instead of implementing Disposable interfaces or destory-method in xml file                    | @PreDestroy    |

Java CONFIGURATION ( aVOID )
============================

|                         |                                                                                                                   |                                                                               |             |                |
|-------------------------|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|----------------|
|                         | **Java Configuration ( courtesy ..Google Guice )**                                                                | It is best way to configuration when ensure all bean configured and type safe |             |                |
| supported in Spring 3.0 | it is java annotation supported in spring 3.0.                                                                    
                            Mark a class, which will provide all Bean definition                                                              | @Configuration                                                                |             |                |
| supported in Spring 3.0 | used to explicitly say bean and its id in JAVA configuration                                                      | @Bean                                                                         | Init-method | Destory-method |
| supported in Spring 3.0 | to ensure dependecy created before                                                                                | @DependsOn                                                                    |             |                |
| supported in Spring 3.0 | when more than matching bean has implemented same interface, use this to specify which one among them should take | @Primary                                                                      |             |                |
| supported in Spring 3.0 | postpone bean creation until exactly need or used                                                                 | @Lazy                                                                         |             |                |
| supported in Spring 3.0 | used to when modularized configuration for every layer and import others                                          | @Import                                                                       |             |                |

Eclipse 4
=========

|               |
|---------------|
| @Singleton    |
| @Optional     |
| @Active       |
| @Execute      |
| @CanExecute   |
| @Preference   |
| @Creatable    |
| @Focus        |
| @AboutToShow  |
| @AboutToHide  |
| @GroupUpdate  |
| @EventTopic   |
| @UIEventTopic |

Struts 2.1
==========

|                         |        |     |            |       |         |      |
|-------------------------|--------|-----|------------|-------|---------|------|
| Results                 |        |     |            |       |         |      |
|                         | Result |     | name       | value |         |      |
|                         |        |     |            |       |         |      |
| Validation              |        |     |            |       |         |      |
| ExpressionValidator     |        |     | expression |       | message |      |
| RequiredStringValidator |        |     |            |       | message | type |
| EmailValidator          |        |     |            | key   | message | type |
| StringLengthValidator   |        |     |            |       | message | type |
|                         |        |     |            |       |         |      |
|                         |        |     |            |       |         |      |
| Inject                  |        |     |            |       |         |      |
|                         |        |     |            |       |         |      |
| SkipValidation          |        |     |            |       |         |      |

JAX-WS 2.1
==========


 
 
 
This colored attribute customize XMLSchema generation
 
 
 
This colored attribute customize WSDL generation
 
 
 
 
declared in Service endpoint interface
@WebService
 
name
declare handler of SOAP message
@HandlerChain
 
file
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
specify either rpc or document
@SOAPBinding
 
style
use
parameterStyle
 
 
 
 
 
to use SOAP 1.2 version
@BindingType
 
value
 
 ![](Paramannotations_html_1b382aa9.png)
 
 
 
 
@RespectBinding
 
enabled
 
 
 
 
 
@Addressing
 
enabled
required
 
 
 
 
@MTOM
 
enabled
threshold
 
 
 
 
 
 
 
 
 
 
 
declared in Service endpoint interface's method
@WebMethod
 
operationName
action
 
 
 
customize response message part
@WebResult
 
name
targetNamespace
partName
header
 
 
 
 
it give custom name for parameter istead 'arg0'
@WebParam
 
name
targetNamespace
partName
header
mode
 
 
 
soap fault exception class
@WebFault
 
 
 
 
 
 
 
 
 
when a method return type is VOID
@OneWay
 
*it does not have any attirbutes*
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
used for JAXB
@RequestWrapper
 
localName
targetNamespace
className
 
 
 
 
 
 
@ResponseWrapper
 
localName
targetNamespace
className
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
@XMLSeeAlso
 
 
 
 
 
 
 
 
 
 
@WebServiceClient
 
name
targetNamespace
wsdlLocation
 
 
 
 
 
 
@WebEndpoint
 
name
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
it is annotation used for JEE web service client
@WebServiceRef
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
RESTFul web service
@WebServiceProvider
 
 
 
 
 
 
 
 
 
RESTFul web service
@ServiceMode
 
 
 
 
 
 
 
 
 
 
@Path
 
 
 
 
 
 
 
 
 
 
@GET
 
 
 
 
 
 
 
 
 
 
@Produces
 
 
 
 
 
 
 
 
 
 
@POST
 
 
 
 
 
 
 
 
 
 
@FormParam
 
 
 
 
 
 
 
 
 
 
@DELETE
 
 
 
 
 
 
 
 
 
![](Paramannotations_html_1c45fdda.png) ![](Paramannotations_html_c8e18182.png) ![](Paramannotations_html_4a99c2f5.png) ![](Paramannotations_html_acd59b40.png) ![](Paramannotations_html_db75570.png) ![](Paramannotations_html_9398d40d.png) ![](Paramannotations_html_7cfd9cf5.png) ![](Paramannotations_html_70036831.png) ![](Paramannotations_html_d7799293.png) ![](Paramannotations_html_2159c6d1.png) ![](Paramannotations_html_f79a5c34.png) ![](Paramannotations_html_fb3ba81f.png)

JAXB
====

|                                                                                               |                          |     |      |           |           |
|-----------------------------------------------------------------------------------------------|--------------------------|-----|------|-----------|-----------|
| this will give package path for all of our domain class, by having create method for each DTO | @XmlRegistry             |     |      |           |           |
|                                                                                               | @XmlAccessorOrder        |     |      |           |           |
|                                                                                               | @XmlAccessType           |     |      |           |           |
|                                                                                               | @XmlTransient            |     |      |           |           |
|                                                                                               |                          |     |      |           |           |
| among many DTO, this added dto will be root element                                           | @XmlRootElement          |     | name | namespace |           |
| java field as xml attribute                                                                   | @XmlAttribute            |     |      |           |           |
| used to specify interface type member, when only one implementation u have                    | @XmlElement              |     | name | namespace |           |
| used to specify interface type member                                                         | @XmlAnyElement           |     |      |           |           |
| it add a element as a wrapper for its member, usually it is a collection                      | @XmlElementWrapper       |     |      |           |           |
|                                                                                               | @XmlElementRef           |     |      |           |           |
|                                                                                               |                          |     |      |           |           |
|                                                                                               | @XmlType                 |     | name | namespace | propOrder |
|                                                                                               | @XmlMimeType             |     |      |           |           |
| define custom data type between java & xml                                                    | @XmlSchemaType           |     |      |           |           |
| for custom data type adaptor, used when interface has only one impl.                          | @XmlJavaTypeAdapter      |     |      |           |           |
|                                                                                               | @NormalizedStringAdapter |     |      |           |           |
|                                                                                               |                          |     |      |           |           |
|                                                                                               | @XmlValue                |     |      |           |           |
|                                                                                               |                          |     |      |           |           |
|                                                                                               | @XmlInlineBinaryData     |     |      |           |           |
|                                                                                               | @Generated               |     |      |           |           |

Juni 4
======

|                                                 |              |          |
|-------------------------------------------------|--------------|----------|
| define a unit test                              | @Test        | expected |
| ignore the test case                            | @Ignore      |          |
|                                                 |              |          |
| before to every unit test                       | @Before      |          |
| after to every unit test                        | @After       |          |
|                                                 |              |          |
| run code before all tests in a particular class | @BeforeClass |          |
| run code after all tests in a particular class  | @AfterClass  |          |
|                                                 |              |          |
| it is used with spring                          | @Runwith     |          |
|                                                 | @Assert      |          |
