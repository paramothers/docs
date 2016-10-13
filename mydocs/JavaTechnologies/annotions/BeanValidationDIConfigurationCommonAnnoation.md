


Bean validation
===============

|             |      |      |         |          |
| ----------- | ---- | ---- | ------- | -------- |
| size        |      |      | max     | min      |
| NotNull     |      |      | message |          |
| Past        |      |      |         |          |
| Null        |      |      |         |          |
| AssertTrue  |      |      |         |          |
| AssertFalse |      |      |         |          |
| Min         |      |      | value   |          |
| Max         |      |      | value   |          |
| DecimalMin  |      |      | value   |          |
| DecimalMax  |      |      | value   |          |
| Digits      |      |      | integer | fraction |
| Future      |      |      |         |          |
| pattern     |      |      | regexpr | flag     |


Java Dependency
===============

|                         |                                          |            |      |
| ----------------------- | ---------------------------------------- | ---------- | ---- |
| supported in Spring 3.1 | use this not to dependency with spring. It provide same facility like Autowired .It introduced by sun, implemented in spring 3.0 | @inject    |      |
| supported in Spring 3.1 | it is Java dependency injection. It helps to indentify bean by its id and alternative to @Component annotation | @Named     |      |
| supported in Spring 3.1 | it cannot be used directly, but it can be used to define custom qualifier annotation | @Qualifier | name |


Java Common Annotations
=======================

|                         |                                          |                |
| ----------------------- | ---------------------------------------- | -------------- |
| supported in Spring 3.0 | it is java common annotation supported in spring 2.5. Used to as same purpose @Autowire annotation | @Resource      |
| supported in Spring 3.0 | use instead of implementing InitializingBean interfaces or init-method in xml file | @Postconstruct |
| supported in Spring 3.0 | use instead of implementing Disposable interfaces or destory-method in xml file | @PreDestroy    |


#Java CONFIGURATION 

|                         |                                          |                                          |                |                |
| ----------------------- | ---------------------------------------- | ---------------------------------------- | -------------- | -------------- |
|                         | Java Configuration ( courtesy ..Google Guice ) | It is best way to configuration when ensure all bean configured and type safe |                |                |
| supported in Spring 3.0 | used to when modularized configuration for every layer and import others | @Import                                  |                |                |
| supported in Spring 3.0 | it is java annotation supported in spring 3.0 | Mark a class, which will provide all Bean definition | @Configuration |                |
| supported in Spring 3.0 | used to explicitly say bean and its id in JAVA configuration | @Bean                                    | Init-method    | Destory-method |
| supported in Spring 3.0 | to ensure dependecy created before       | @DependsOn                               |                |                |
| supported in Spring 3.0 | when more than matching bean has implemented same interface, use this to specify which one among them should take | @Primary                                 |                |                |
| supported in Spring 3.0 | postpone bean creation until exactly need or used | @Lazy                                    |                |                |

