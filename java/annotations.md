Paramannotations156605 (Click to Expand/Collapse)Copy to Clipboard
[Core Java Page](javacoreindex.html)

------------------------------------------------------------------------

-   [JPA 2.1 class level\_Physical](#table0)
-   [JPA 2.1 class level\_logical](#table1)
-   [JPA2.1 attribute level](#table2)
-   [JPA Entity Manger Factory](#table3)
-   [AspectJ annotation](#table6)
-   [EJB 3.1](#table8)
-   [Mybatis 3.2.8](#table10)
-   [Gradle 2.3](#table11)
-   [Bean validation](#table12)
-   [Java Dependency](#table13)
-   [Java Common Annotations](#table14)
-   [Java CONFIGURATION ( aVOID )](#table15)
-   [Eclipse 4](#table16)
-   [Struts 2.1](#table17)
-   [JAX-WS 2.1](#table18)
-   [JAXB](#table19)
-   [Juni 4](#table20)

 

JPA 2.1 class level\_Physical
=============================

|                                     |     |                  |     |            |                |                   |
|-------------------------------------|-----|------------------|-----|------------|----------------|-------------------|
| to specify table name for an entity |     | Table            |     | name       | schema/catelog | uniqueConstraints |
|                                     |     | SecondaryTables  |     |            |                |                   |
|                                     |     | SecondaryTable   |     |            |                |                   |
|                                     |     | UniqueConstraint |     | columnName |                |                   |

JPA 2.1 class level\_logical
============================

|                                                      |     |                     |              |             |     |          |                   |             |                  |
|------------------------------------------------------|-----|---------------------|--------------|-------------|-----|----------|-------------------|-------------|------------------|
|                                                      |     |                     |              |             |     |          |                   |             |                  |
|                                                      |     |                     |              |             |     |          |                   |             |                  |
| every java entity class must be annotated            | 1   | Entity              |              |             |     | name     |                   |             |                  |
|                                                      |     |                     |              |             |     |          |                   |             |                  |
|                                                      | 2   | Inheritance         |              |             |     | startegy |                   |             |                  |
|                                                      | 3   | DiscriminatorValue  |              |             |     |          |                   |             |                  |
|                                                      | 4   | DiscriminatorColumn |              |             |     | name     | discriminatorType |             |                  |
|                                                      | 5   | MappedSuperClass    |              |             |     |          |                   |             |                  |
| override, the default access type                    | 6   | Access              |              |             |     |          |                   |             |                  |
|                                                      | 7   | Cachable            |              |             |     |          |                   |             |                  |
|                                                      |     |                     |              |             |     |          |                   |             |                  |
| used to define JP QL                                 | 8   | NamedQuery          |              |             |     | name     | query             |             |                  |
| used when define more than one query in single class | 9   | NamedQueries        |              |             |     |          |                   |             |                  |
|                                                      | 10  | NamedNativeQuery    |              |             |     | name     | query             | resultClass | resultSetMapping |
|                                                      | 11  | NamedNativeQueries  |              |             |     |          |                   |             |                  |
|                                                      | 12  | SqlResultSetMapping |              |             |     | name     | entities          | column      |                  |
|                                                      | 13  |                     | EntityResult |             |     |          | fields            | entityClass |                  |
|                                                      | 14  |                     |              | FieldResult |     | name     | column            |             |                  |
|                                                      | 15  |                     | ColumnResult |             |     | name     |                   |             |                  |
|                                                      | 16  | BatchSize           |              |             |     |          |                   |             |                  |
|                                                      | 17  | Where               |              |             |     |          |                   |             |                  |
|                                                      | 18  | Check               |              |             |     |          |                   |             |                  |
|                                                      | 19  | SubSelect           |              |             |     |          |                   |             |                  |
|                                                      | 20  | Synchronize         |              |             |     |          |                   |             |                  |
|                                                      |     |                     |              |             |     |          |                   |             |                  |

JPA2.1 attribute level
======================

|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
|------------------------------------------------------------------|-----|----------------------|-----|--------------|--------------------|--------------------|----------------|----------------------|-----------------|------------------|
|                                                                  | 1   | id                   |     |              |                    |                    |                |                      |                 |                  |
| this value generated in domain object                            | 2   | GeneratedValue       |     | name         | startegy/generator |                    |                |                      |                 |                  |
|                                                                  | 3   | SequenceGenerator    |     | name         | sequenceName       | initialValue       | allocationSize |                      |                 |                  |
| explicitly spccify the keyValue for table generator              | 4   | TableGenerator       |     | name         | table              | initialValue       | allocationSize | pkColumnName         | valueColumnName |                  |
|                                                                  | 5   | IdClass              |     |              |                    |                    |                |                      |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
| mixed type access or value to be retained accross JVM            | 6   | Transient            |     |              |                    |                    |                |                      |                 |                  |
| it is optional, it is explitly says, primitive type of attribute | 7   | Basic                |     | fetch        | optional           |                    |                |                      |                 |                  |
| just to tell the provider this is lob column                     | 8   | Lob                  |     |              |                    |                    |                |                      |                 |                  |
| to explity says enum type of value to be stored                  | 9   | Enumerated           |     |              |                    |                    |                |                      |                 |                  |
| used only when java.util.Date/Calendar used                      | 10  | Temporal             |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 11  | Version              |     |              |                    |                    |                |                      |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
| target is shared by many source ( non-collection )               | 12  | ManyToOne            |     |              |                    |                    | cascade        |                      |                 |                  |
| target is never shared ( non- collection )                       | 16  | OneToOne             |     | mappedBy     | targetEntity       | fetch              |                |                      |                 |                  |
| Collection based relationship                                    | 13  | OneToMany            |     | mappedBy     |                    | fetch              |                |                      |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
| used to spcify FOREIGN key column name                           | 14  | JoinColumn           |     | name         | updatable          | unique             | nullable       | referencedColumnName |                 |                  |
|                                                                  | 15  | JoinColumns          |     | name         |                    |                    |                | referencedColumnname |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
| Collection based relationship                                    | 17  | ManyToMany           |     | targetEntity | cascade            |                    |                |                      |                 |                  |
| Many-to-many/one-to-many by join table                           | 18  | JoinTable            |     | name         | joinColumns        | inverseJoinColumns |                |                      |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 19  | MapsId               |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 20  | OrderColumn          |     | name         |                    |                    |                |                      |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
| it is just element collection, not any relationship              | 21  | ElementCollection    |     |              | targetClass        | fetch              |                |                      |                 |                  |
|                                                                  | 22  | CollectionTable      |     | name         | joinColumns        |                    |                |                      |                 |                  |
|                                                                  | 23  | OrderBy              |     |              |                    |                    |                |                      |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
| any java class can be used as embeddable                         | 24  | Embeddable           |     |              |                    |                    |                |                      |                 |                  |
| any java attribute is embeddalble Type                           | 25  | Embedded             |     |              |                    |                    |                |                      |                 |                  |
| just to override column mapping of embeddable type               | 26  | AttributeOverride    |     | name         | column             |                    |                |                      |                 |                  |
|                                                                  | 27  | AttributeOverrides   |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 28  | EmbeddedId           |     |              |                    |                    |                |                      |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
| to overide default attribute name                                | 29  | Column               |     | name         | unique             | nullable           | length         | precision            | scale           | columnDefinition |
|                                                                  | 30  | NotNull              |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 31  | GenericGenerator     |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 32  | GenericGenerators    |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 33  | Type                 |     | type         |                    |                    |                |                      |                 |                  |
|                                                                  | 34  | TypeDef              |     | name         | defaultClassType   | typeClass          |                |                      |                 |                  |
|                                                                  | 35  | TypeDefs             |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 36  | Immutable            |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 37  | proxy                |     | lazy         | proxyClass         |                    |                |                      |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 38  | FilterDefs           |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 39  | FilterDef            |     | name         | parameter          | condition          |                |                      |                 |                  |
|                                                                  | 40  | Filters              |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 41  | Filter               |     | name         | condition          |                    |                |                      |                 |                  |
|                                                                  | 42  | ParamDef             |     | name         | type               |                    |                |                      |                 |                  |
|                                                                  | 43  | FilterJoinTable      |     |              |                    |                    |                |                      |                 |                  |
|                                                                  |     |                      |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 44  | DiscriminatorFormula |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 45  | Formula              |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 46  | Generated            |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 47  | JoinColumnOrFormula  |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 48  | EmbeddedId           |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 49  | MappedSuperClass     |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 50  | Parent               |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 51  | PrimaryKeyJoinColumn |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 52  | SecondaryTable       |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 53  | FetchProfile         |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 54  | Cache                |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 55  | onDelete             |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 56  | NotFound             |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 57  | ForeignKey           |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 58  | NaturalId            |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 59  | Any                  |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 60  | AnyDef               |     |              |                    |                    |                |                      |                 |                  |
|                                                                  | 61  | Sort                 |     | type         | comparator         |                    |                |                      |                 |                  |
|                                                                  | 62  | OptimisticLock       |     |              |                    |                    |                |                      |                 |                  |

JPA Entity Manger Factory
=========================

|     |                                                                          |                    |     |     |          |
|-----|--------------------------------------------------------------------------|--------------------|-----|-----|----------|
|     | JPA configure                                                            |                    |     |     |          |
|     |                                                                          |                    |     |     |          |
|     | to inject Container Managed EntityManager                                | PersistenceContext |     |     | unitName |
|     | it helps to create Application managed EntityManager, in JEE enviornment | PersistenceUnit    |     |     |          |
|     |                                                                          |                    |     |     |          |
|     |                                                                          | PostLoad           |     |     |          |
|     |                                                                          | PrePersist         |     |     |          |
|     |                                                                          | PostPersist        |     |     |          |
|     |                                                                          | PreUpdate          |     |     |          |
|     |                                                                          | PostUpdate         |     |     |          |
|     |                                                                          | PreRemove          |     |     |          |
|     |                                                                          | PostRemove         |     |     |          |
|     |                                                                          | EntityListener     |     |     |          |

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

Mybatis 3.2.8
=============

|                                               |     |                    |            |     |                          |             |     |        |            |               |
|-----------------------------------------------|-----|--------------------|------------|-----|--------------------------|-------------|-----|--------|------------|---------------|
| explicitly spcify parameter name              |     | @Param             |            |     |                          |             |     |        |            |               |
| instead of element                            |     | @Alias             |            |     |                          |             |     |        |            |               |
|                                               |     | @select            |            |     |                          |             |     |        |            |               |
| insert SQL statement                          |     | @insert            |            |     |                          |             |     |        |            |               |
|                                               |     | @delete            |            |     |                          |             |     |        |            |               |
|                                               |     | @update            |            |     |                          |             |     |        |            |               |
| domian object constructors                    |     | @ConstructurArgs   |            |     |                          |             |     |        |            |               |
|                                               |     |                    | @Arg       |     |                          |             |     |        |            |               |
| it will be used with @Insert for generate key |     | @options           |            |     |                          |             |     |        |            |               |
| get primary key value from sequence           |     | @SelectKey         |            |     | statement                | keyProperty |     | before | resultType | statementType |
| result mapping to a java object               |     | @Results           |            |     |                          |             |     |        |            |               |
|                                               |     |                    | @Result    |     | column                   | property    | id  |        |            |               |
|                                               |     |                    |            |     | one= @One(select=””)     |             |     |        |            |               |
|                                               |     |                    |            |     | Many = @Many (Select=””) |             |     |        |            |               |
| refere id from corresponding XML file.        |     | @ResultMap         |            |     |                          |             |     |        |            |               |
| when return type is Map                       |     | @MapKey            |            |     |                          |             |     |        |            |               |
|                                               |     |                    |            |     |                          |             |     |        |            |               |
| A class, to give dynmaic Insert SQL           |     | @InsertProvider    |            |     | type                     | method      |     |        |            |               |
| A class, to give dynmaic select SQL           |     | @SelectProvider    |            |     |                          |             |     |        |            |               |
| A class, to give dynmaic update SQL           |     | @UpdateProvider    |            |     |                          |             |     |        |            |               |
| A class, to give dynmaic delete SQL           |     | @DeleteProvider    |            |     |                          |             |     |        |            |               |
|                                               |     |                    |            |     |                          |             |     |        |            |               |
|                                               |     |                    |            |     |                          |             |     |        |            |               |
|                                               |     |                    |            |     |                          |             |     |        |            |               |
| it is used with spring-mybatis                |     | @MapperScan        |            |     |                          |             |     |        |            |               |
|                                               |     |                    |            |     |                          |             |     |        |            |               |
| to specify DB column type on typehandler      |     | @MappedJdbcType    |            |     |                          |             |     |        |            |               |
| to specify java type on typehandlder          |     | @MappedTypes       |            |     |                          |             |     |        |            |               |
|                                               |     |                    |            |     |                          |             |     |        |            |               |
|                                               |     | @Interceptor       |            |     |                          |             |     |        |            |               |
|                                               |     |                    | @Signature |     | type                     | method      |     | args   |            |               |
|                                               |     | @TypeDescriminator |            |     |                          |             |     |        |            |               |
|                                               |     |                    | @Case      |     |                          |             |     |        |            |               |

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
