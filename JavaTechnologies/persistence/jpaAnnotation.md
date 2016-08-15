JPA Entity Manger Factory
=========================

|                                                                          |                    |          |
|--------------------------------------------------------------------------|--------------------|----------|
| JPA configure                                                            |                    |          |
| to inject Container Managed EntityManager, but thread safe               | PersistenceContext | unitName |
| it helps to create Application managed EntityManager, in JEE enviornment | PersistenceUnit    |          |
|                                                                          | PostLoad           |          |
|                                                                          | PrePersist         |          |
|                                                                          | PostPersist        |          |
|                                                                          | PreUpdate          |          |
|                                                                          | PostUpdate         |          |
|                                                                          | PreRemove          |          |
|                                                                          | PostRemove         |          |
|                                                                          | EntityListener     |          |


JPA 2.1 class level\_Physical
=============================

|                                     |                  |            |                |                   |
|-------------------------------------|------------------|------------|----------------|-------------------|
| to specify table name for an entity | Table            | name       | schema/catelog | uniqueConstraints |
|                                     | SecondaryTables  |            |                |                   |
|                                     | SecondaryTable   |            |                |                   |
|                                     | UniqueConstraint | columnName |                |                   |

JPA 2.1 class level\_logical
============================

|                                                      |    |                     |              |             |  |          |                   |             |                  |
|------------------------------------------------------|----|---------------------|--------------|-------------|--|----------|-------------------|-------------|------------------|
| every java entity class must be annotated            | 1  | Entity              |              |             |  | name     |                   |             |                  |
|                                                      | 2  | Inheritance         |              |             |  | startegy |                   |             |                  |
|                                                      | 3  | DiscriminatorValue  |              |             |  |          |                   |             |                  |
|                                                      | 4  | DiscriminatorColumn |              |             |  | name     | discriminatorType |             |                  |
|                                                      | 5  | MappedSuperClass    |              |             |  |          |                   |             |                  |
| override, the default access type                    | 6  | Access              |              |             |  |          |                   |             |                  |
|                                                      | 7  | Cachable            |              |             |  |          |                   |             |                  |
| used to define JP QL                                 | 8  | NamedQuery          |              |             |  | name     | query             |             |                  |
| used when define more than one query in single class | 9  | NamedQueries        |              |             |  |          |                   |             |                  |
|                                                      | 10 | NamedNativeQuery    |              |             |  | name     | query             | resultClass | resultSetMapping |
|                                                      | 11 | NamedNativeQueries  |              |             |  |          |                   |             |                  |
|                                                      | 12 | SqlResultSetMapping |              |             |  | name     | entities          | column      |                  |
|                                                      | 13 |                     | EntityResult |             |  |          | fields            | entityClass |                  |
|                                                      | 14 |                     |              | FieldResult |  | name     | column            |             |                  |
|                                                      | 15 |                     | ColumnResult |             |  | name     |                   |             |                  |
|                                                      | 16 | BatchSize           |              |             |  |          |                   |             |                  |
|                                                      | 17 | Where               |              |             |  |          |                   |             |                  |
|                                                      | 18 | Check               |              |             |  |          |                   |             |                  |
|                                                      | 19 | SubSelect           |              |             |  |          |                   |             |                  |
|                                                      | 20 | Synchronize         |              |             |  |          |                   |             |                  |

JPA2.1 attribute level
======================

|                                                                  |    |                      |  |              |                    |                    |                |                      |                 |                  |
|------------------------------------------------------------------|----|----------------------|--|--------------|--------------------|--------------------|----------------|----------------------|-----------------|------------------|
|                                                                  | 1  | id                   |  |              |                    |                    |                |                      |                 |                  |
| this value generated in domain object                            | 2  | GeneratedValue       |  | name         | startegy/generator |                    |                |                      |                 |                  |
|                                                                  | 3  | SequenceGenerator    |  | name         | sequenceName       | initialValue       | allocationSize |                      |                 |                  |
| explicitly spccify the keyValue for table generator              | 4  | TableGenerator       |  | name         | table              | initialValue       | allocationSize | pkColumnName         | valueColumnName |                  |
|                                                                  | 5  | IdClass              |  |              |                    |                    |                |                      |                 |                  |
| mixed type access or value to be retained accross JVM            | 6  | Transient            |  |              |                    |                    |                |                      |                 |                  |
| it is optional, it is explitly says, primitive type of attribute | 7  | Basic                |  | fetch        | optional           |                    |                |                      |                 |                  |
| just to tell the provider this is lob column                     | 8  | Lob                  |  |              |                    |                    |                |                      |                 |                  |
| to explity says enum type of value to be stored                  | 9  | Enumerated           |  |              |                    |                    |                |                      |                 |                  |
| used only when java.util.Date/Calendar used                      | 10 | Temporal             |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 11 | Version              |  |              |                    |                    |                |                      |                 |                  |
| target is shared by many source ( non-collection )               | 12 | ManyToOne            |  |              |                    |                    | cascade        |                      |                 |                  |
| target is never shared ( non- collection )                       | 16 | OneToOne             |  | mappedBy     | targetEntity       | fetch              |                |                      |                 |                  |
| Collection based relationship                                    | 13 | OneToMany            |  | mappedBy     |                    | fetch              |                |                      |                 |                  |
| used to spcify FOREIGN key column name                           | 14 | JoinColumn           |  | name         | updatable          | unique             | nullable       | referencedColumnName |                 |                  |
|                                                                  | 15 | JoinColumns          |  | name         |                    |                    |                | referencedColumnname |                 |                  |
| Collection based relationship                                    | 17 | ManyToMany           |  | targetEntity | cascade            |                    |                |                      |                 |                  |
| Many-to-many/one-to-many by join table                           | 18 | JoinTable            |  | name         | joinColumns        | inverseJoinColumns |                |                      |                 |                  |
|                                                                  | 19 | MapsId               |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 20 | OrderColumn          |  | name         |                    |                    |                |                      |                 |                  |
| it is just element collection, not any relationship              | 21 | ElementCollection    |  |              | targetClass        | fetch              |                |                      |                 |                  |
|                                                                  | 22 | CollectionTable      |  | name         | joinColumns        |                    |                |                      |                 |                  |
|                                                                  | 23 | OrderBy              |  |              |                    |                    |                |                      |                 |                  |
| any java class can be used as embeddable                         | 24 | Embeddable           |  |              |                    |                    |                |                      |                 |                  |
| any java attribute is embeddalble Type                           | 25 | Embedded             |  |              |                    |                    |                |                      |                 |                  |
| just to override column mapping of embeddable type               | 26 | AttributeOverride    |  | name         | column             |                    |                |                      |                 |                  |
|                                                                  | 27 | AttributeOverrides   |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 28 | EmbeddedId           |  |              |                    |                    |                |                      |                 |                  |
| to overide default attribute name                                | 29 | Column               |  | name         | unique             | nullable           | length         | precision            | scale           | columnDefinition |
|                                                                  | 30 | NotNull              |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 31 | GenericGenerator     |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 32 | GenericGenerators    |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 33 | Type                 |  | type         |                    |                    |                |                      |                 |                  |
|                                                                  | 34 | TypeDef              |  | name         | defaultClassType   | typeClass          |                |                      |                 |                  |
|                                                                  | 35 | TypeDefs             |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 36 | Immutable            |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 37 | proxy                |  | lazy         | proxyClass         |                    |                |                      |                 |                  |
|                                                                  | 38 | FilterDefs           |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 39 | FilterDef            |  | name         | parameter          | condition          |                |                      |                 |                  |
|                                                                  | 40 | Filters              |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 41 | Filter               |  | name         | condition          |                    |                |                      |                 |                  |
|                                                                  | 42 | ParamDef             |  | name         | type               |                    |                |                      |                 |                  |
|                                                                  | 43 | FilterJoinTable      |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 44 | DiscriminatorFormula |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 45 | Formula              |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 46 | Generated            |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 47 | JoinColumnOrFormula  |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 48 | EmbeddedId           |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 49 | MappedSuperClass     |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 50 | Parent               |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 51 | PrimaryKeyJoinColumn |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 52 | SecondaryTable       |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 53 | FetchProfile         |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 54 | Cache                |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 55 | onDelete             |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 56 | NotFound             |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 57 | ForeignKey           |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 58 | NaturalId            |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 59 | Any                  |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 60 | AnyDef               |  |              |                    |                    |                |                      |                 |                  |
|                                                                  | 61 | Sort                 |  | type         | comparator         |                    |                |                      |                 |                  |
|                                                                  | 62 | OptimisticLock       |  |              |                    |                    |                |                      |                 |                  |
