
Spring 4.X
==========

https://devotter.com/converter

Spring Context configuration annotation
=======================================

|   |  |  | |
|---|---|---|----|
|  spring 2.0 annotation for bean configuration. Alternative to element | @Component | value | |
|  it is used to translate SQLException to spring exception hierarchy when JPA or Hibernate used and not using any templates of Spring | @Repository |  | |
|  it is used to import @Bean configuration from another of @Configuration class | @Import |  | |
|  it is used to import bean configured using xml file into java config class | @ImportResource |  | |
|  it is used for service classes | @Service |  | |
|   |  custom annotation with @Component annotated |  | |
|   used when explicit configuration as alternative to auto scanning beans| @Bean | name | |
|   | @DateTimeFormat |  | |
|  startup context, used in Junit test | @ContextConfiguration |  | |
|  java config instead of xml file | @Configuration |  | |
|  package path to find spring bean | @ComponentScan | basePackages | basePackageClassess |
|  use at constructor, setter and variable declaration |  @Autowired | required | |
|  when ambibuity for bean type, to specify one among them |  @Primary |  | |
|  Fine-grained auto wiring, when more than one bean possible for autowire It is Spring based and introduced at 2.5 |  @Qualifier | name | |
|  it is spring annotation. It is alternative for 'scope' attribute of tag |  @Scope | value | proxyMode |
|  loan the given property file from classpath and access p9roperty using Envionment object |  @PropertySource |  |  |
|  it is spring 3.0 annotation, used to hold Spring Expression language Superooo super annotation. Using Spring expression language it simplify code a lot at least access value and assiging values| @Value |  | |

Spring MVC, RestFul
===================


|   |  |  |  |  |
|---|---|---|----|----|
| define spring MVC controller ( like actions in struts )  | @Controller |  |  |  |
|  method mapping in controller | @RequestMapping | method |  produces |  consumes |
|  specify the request paramters | @RequestParam |  value | defaultValue |  |
|   | @SessionAttriute |  |  |  |
|   | @EnableWebMvc |  |  |  |
|   | @EnableWebSecurity |  |  |  |
|   | @EnableWebMvcSecurity |  |  |  |
|   | @AuthenticationPrincipal |  |  |  |
| introduced in spring 4.0  | @RestController |  |  |  |
| it is used to bind URL path as parameter variables | @PathVariable |  |  |  |
|  bypass view based rendering | @ResponseBody |  |  |  |
|  convert HTTP data into java object | @RequestBody |  |  |  |
|  Content-Type header | @RequestMapping | consumes | produces |  |
|  used to map multipart request | @RequestPart |  |  |  |
|  introduced in 3.2 version | @ExceptionHandler |  |  |  |
|  introduced in 3.2 version |  @ControllerAdvice |  |  |  |
|  introduced in 3.2 version | @ModelAttributes |  |  |  |
|   | @CookieValue |  |  |  |
|   | @RequestHeader |  |  |  |


Spring-Profile
===========

|   |  | 
|---|---|
| define a bean belongs to pariticular profile, spring.profiles.default and spring.profiles.active  environment variable used  | @Profile | 
|  it is used in integration testing along with Test Class | @ActiveProfiles | 
|  to define bean condition rather than depends on only Profile feature | @Conditional | 

Transaction Handling
============

|   |   |   |   |   |   |   |   | 
|---|---|---|---|---|---|---|---|
| it is spring annotation, used for specify a method or entire class itself to be a part of transaction, it is introduced in spring 2.0 itself  | @Transactional  | propgation  | isolation  | timeout  |  noRollbackfor |  Rollbackfor |  readOnly | 

<table>
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>




<tr class="even">
<td align="left">validate request parameters, it is Java annotation, spring 3.0 support it</td>
<td align="left">@Valid</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>


<tr class="odd">
<td align="left"><span style="font-family: sans-serif;">introduced in 3.2 version</span></td>
<td align="left">@InitBuilder</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>

<tr class="even">
<td align="left"> </td>
<td align="left">@MatrixVariable</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>

<tr class="odd">
<td align="left"><strong>Schedule – annotation</strong></td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"> </td>
<td align="left">@Schedule</td>
<td align="left">fixedRate</td>
<td align="left">fixedDelay</td>
<td align="left">cron</td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"> </td>
<td align="left">@Async</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"><strong>Spring Webservice – annotation</strong></td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"> </td>
<td align="left">@Endpoint</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"> </td>
<td align="left">@payloadRoot</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"><strong>Spring JMX– annotation</strong></td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"> </td>
<td align="left">@ManagedResource,<br />
 @ManagedAttribute,</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"> </td>
<td align="left">@ManagedOperation</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>

<tr class="odd">
<td align="left"><strong>Spring 3.0 Junit 4.5 – annotation</strong></td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>

<tr class="odd">
<td align="left">Define default transaction parameters for the class</td>
<td align="left">@TransactionConfiguration</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left">Method to execute before a transaction</td>
<td align="left">@BeforeTransaction</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left">Method to execute after a transaction</td>
<td align="left">@AfterTransaction</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left">Change rollback settings for methods</td>
<td align="left">@RollBack</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left">the class or method level, mark the app context as dirty and should be closed. The app context will be recreated for subsequent test</td>
<td align="left">@DirtiesContext</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left">Specify the number of times the test method will repeat</td>
<td align="left">@Repeat</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left">Defined maximum time that method has to execute</td>
<td align="left">@Timed</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"> </td>
<td align="left">@NotTransactional</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"> </td>
<td align="left">@ExpectedException</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"> </td>
<td align="left">@IfProfileValue</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="odd">
<td align="left"> </td>
<td align="left">@ProfileValueSourceConfiguration</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>


<tr class="odd">
<td align="left"> </td>
<td align="left">@ConstructorProperties</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>
<tr class="even">
<td align="left"> </td>
<td align="left">@Required</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>


<tr class="odd">
<td align="left"> </td>
<td align="left">@Configurable</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left">it is used for configuration external object via Spring framework</td>
</tr>
<tr class="even">
<td align="left"> </td>
<td align="left">@Provider</td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
<td align="left"> </td>
</tr>


</tbody>
</table>

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
| used tell a class for Aspect = pointcut + advices                                                                                                     
  It just marker to proxy to be created for this class                                                                                                  | @Aspect          |           |             |          |
| used to define pointcut and share among many advice annotation, when pointcut are repeating.                                                                                       | @Pointcut        |           |             |          |
| it used to say a advice should execute before to joint point                                                                                          | @Before          | returning | argNames    |          |
| used for AOP programming prior to Spring 2.0                                                                                                          | @AfterReturning  | throwing  | argNames    | pointcut |
| used to say after throwing advice                                                                                                                     | @AfterThrowing   |           |             |          |
| it is like finally block in java code. This advice execute regardless of method executed or throwed some exception.we use this to close any resources | @After           |           |             |          |
| it is best for Transaction management. It is executed even if it got exception                                                                        | @Around          |           |             |          |
| introducing  new method in existing bean, support multiple Inheritance ( introduce by Spring )                                                             | @DeclaredParents | value     | defaultImpl |          |
