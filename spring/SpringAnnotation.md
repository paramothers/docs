Spring 4.X
==========

https://devotter.com/converter

Spring annotation to enable any spring module
=============================================

|                        |
|------------------------|
| @EnableWebMvc          |
| @EnableWebSecurity     |
| @EnableWebMvcSecurity  |
| @EnableJpaRepositories |
|                        |


Spring Context configuration annotation
=======================================

|                                                                                                                                                                                                   |                                             |              |                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|--------------|---------------------|
| spring 2.0 annotation for bean configuration. Alternative to element                                                                                                                              | @Component                                  | value        |                     |
| it is used to translate SQLException to spring exception hierarchy when JPA or Hibernate used and not using any templates of Spring                                                               | @Repository                                 |              |                     |
| it is used to import @Bean configuration from another of @Configuration class                                                                                                                     | @Import                                     |              |                     |
| it is used to import bean configured using xml file into java config class                                                                                                                        | @ImportResource                             |              |                     |
| it is used for service classes                                                                                                                                                                    | @Service                                    |              |                     |
|                                                                                                                                                                                                   | custom annotation with @Component annotated |              |                     |
| used when explicit configuration as alternative to auto scanning beans                                                                                                                            | @Bean                                       | name         |                     |
|                                                                                                                                                                                                   | @DateTimeFormat                             |              |                     |
| startup context, used in Junit test                                                                                                                                                               | @ContextConfiguration                       |              |                     |
| java config instead of xml file                                                                                                                                                                   | @Configuration                              |              |                     |
| package path to find spring bean                                                                                                                                                                  | @ComponentScan                              | basePackages | basePackageClassess |
| use at constructor, setter and variable declaration                                                                                                                                               | @Autowired                                  | required     |                     |
| when ambibuity for bean type, to specify one among them                                                                                                                                           | @Primary                                    |              |                     |
| Fine-grained auto wiring, when more than one bean possible for autowire It is Spring based and introduced at 2.5                                                                                  | @Qualifier                                  | name         |                     |
| it is spring annotation. It is alternative for 'scope' attribute of tag                                                                                                                           | @Scope                                      | value        | proxyMode           |
| loan the given property file from classpath and access p9roperty using Envionment object                                                                                                          | @PropertySource                             |              |                     |
| it is spring 3.0 annotation, used to hold Spring Expression language Superooo super annotation. Using Spring expression language it simplify code a lot at least access value and assiging values | @Value                                      |              |                     |
|                                                                                                                                                                                                   |                                             |              |                     |

Spring MVC, RestFul
===================
Xp7p3so964

|                                                         |                          |        |              |          |
|---------------------------------------------------------|--------------------------|--------|--------------|----------|
| define spring MVC controller ( like actions in struts ) | @Controller              |        |              |          |
| method mapping in controller                            | @RequestMapping          | method | produces     | consumes |
| specify the request paramters                           | @RequestParam            | value  | defaultValue |          |
| validate request parameters, as in POJO                 | @Valid                   |        |              |          |
|                                                         | @RequestHeader           |        |              |          |
| introduced in 3.2 version                               | @ModelAttributes         |        |              |          |
|                                                         | @SessionAttriute         |        |              |          |
|                                                         | @CookieValue             |        |              |          |
|                                                         | @AuthenticationPrincipal |        |              |          |
| **Exception Handling**                                  |                          |        |              |          |
| annotate method to handle exception  in controller      | @ExceptionHandler        |        |              |          |
| handle exception across many controller                 | @ControllerAdvice        |        |              |          |
| used to map a exception to http status code             | @ResponseStatus          |        |              |          |
| **RestFul**                                             |                          |        |              |          |
| introduced in spring 4.0                                | @RestController          |        |              |          |
| it is used to bind URL path as parameter variables      | @PathVariable            |        |              |          |
| bypass view based rendering                             | @ResponseBody            |        |              |          |
| convert HTTP data into java object                      | @RequestBody             |        |              |          |
| **File Upload**                                         |                          |        |              |          |
| used to map multipart request for file upload           | @RequestPart             |        |              |          |


Spring-Profile
==============

|                                                                                                                             |                 |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------|
| define a bean belongs to pariticular profile, spring.profiles.default and spring.profiles.active  environment variable used | @Profile        |
| it is used in integration testing along with Test Class                                                                     | @ActiveProfiles |
| to define bean condition rather than depends on only Profile feature                                                        | @Conditional    |

Transaction Handling
====================

|                                                                                                                                              |                |            |           |         |               |             |          |
|----------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|-----------|---------|---------------|-------------|----------|
| it is spring annotation, used for specify a method or entire class itself to be a part of transaction, it is introduced in spring 2.0 itself | @Transactional | propgation | isolation | timeout | noRollbackfor | Rollbackfor | readOnly |


Spring JMX– annotation
======================

+ @ManagedResource
+ @ManagedAttribute
+ @ManagedOperation

Schedule – annotation
=====================

+ @Async
+ @Schedule

Spring Webservice – annotation
==============================

+ @Endpoint
+ @payloadRoot

Spring 3.0 Junit 4.5 – annotation
=================================

+ @TransactionConfiguration
+ @BeforeTransaction
+ @AfterTransaction
+ @RollBack
+ @DirtiesContext
+ @Repeat
+ @Timed
+ @NotTransactional
+ @ExpectedException
+ @IfProfileValue
+ @ProfileValueSourceConfiguration
+ @ConstructorProperties
+ @Required
+ @Configurable
+ @Provider


Spring-Batch
============

|                                                   |                           |
|---------------------------------------------------|---------------------------|
| which method has to be execute before a job start | @BeforeJob                |
| which method has to be execute after a job start  | @AfterJob                 |
|                                                   |                           |
|                                                   | @BeforeStep               |
|                                                   | @AfterStep                |
|                                                   | @BeforeChunk              |
|                                                   | @AfterChunk               |
|                                                   |                           |
|                                                   | @EnableBatchConfiguration |
|                                                   | @EnableBatchProcessing    |
|                                                   |                           |
|                                                   | @BeforeRead               |
|                                                   | @AfterRead                |
|                                                   | @OnReadError              |
|                                                   |                           |
|                                                   | @BeforeProcess            |
|                                                   | @AfterProcess             |
|                                                   | @OnProcessError           |
|                                                   |                           |
|                                                   | @BeforeWrite              |
|                                                   | @AfterWrite               |
|                                                   | @OnWriteError             |
|                                                   |                           |
| skip listener annotations                         | @OnSkipInRead             |
|                                                   | @OnSkipInProcess          |
|                                                   | @OnSkipInWrite            |

AspectJ annotation
==================

|                                                                                                                                                       |                  |           |             |          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-----------|-------------|----------|
| **AOP ( These annotation from ASPECTJ , NOT FROM SPRING, but spring gives implementation for them )**                                                 |                  |           |             |          |
| used tell a class for Aspect = pointcut + advices                                                                                                     |                  |           |             |          |
| It just marker to proxy to be created for this class                                                                                                  | @Aspect          |           |             |          |
| used to define pointcut and share among many advice annotation, when pointcut are repeating.                                                          | @Pointcut        |           |             |          |
| it used to say a advice should execute before to joint point                                                                                          | @Before          | returning | argNames    |          |
| used for AOP programming prior to Spring 2.0                                                                                                          | @AfterReturning  | throwing  | argNames    | pointcut |
| used to say after throwing advice                                                                                                                     | @AfterThrowing   |           |             |          |
| it is like finally block in java code. This advice execute regardless of method executed or throwed some exception.we use this to close any resources | @After           |           |             |          |
| it is best for Transaction management. It is executed even if it got exception                                                                        | @Around          |           |             |          |
| introducing  new method in existing bean, support multiple Inheritance ( introduce by Spring )                                                        | @DeclaredParents | value     | defaultImpl |          |
