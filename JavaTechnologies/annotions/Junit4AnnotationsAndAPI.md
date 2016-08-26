#Junit 4


| Description                              | Annotation            | Attributes | Attributes |
| ---------------------------------------- | --------------------- | ---------- | ---------- |
| define a unit test                       | @Test                 | expected   | timeout    |
| ignore the test case instead of commenting any test method/test class itself | @Ignore               |            |            |
|                                          | @Theory               |            |            |
|                                          | @DataPoint            |            |            |
|                                          | @DataPoints           |            |            |
|                                          | @ParametersSuppliedBy |            |            |
| before to every unit test                | @Before               |            |            |
| after to every unit test                 | @After                |            |            |
| run code before all tests in a particular class | @BeforeClass          |            |            |
| run code after all tests in a particular class | @AfterClass           |            |            |
| it is used with spring                   | @Runwith              |            |            |
|                                          | @Assert               |            |            |
|                                          | @Rule                 |            |            |
| it is from mockit to framework for testing | @Mock                 |            |            |
|                                          | @Suite                |            |            |
|                                          | @SuiteClasses         |            |            |
|                                          | @Parameters           |            |            |
|                                          | @Parameter            | value      |            |
|                                          | @FixMethodOrder       |            |            |
|                                          | @Rule                 |            |            |
|                                          | @Category             |            |            |
|                                          | @IncludeCategory      |            |            |
|                                          | @ExculdeCategory      |            |            |



# API

+ Runner
  + Junit4
  + Suite
  + SpringJunit4Runner
  + Parameterized
  + Theories
  + Categories
+ Assert
+ Assume
+ ParemeterSupplier
+ PotentialAssignment

# Built-in Rule

+ Timeout
+ ExceptedException
+ TemporaryFolder
+ ErrorCollector
+ Verifier
+ TestWatcher
+ TestName
+ ExternalResource