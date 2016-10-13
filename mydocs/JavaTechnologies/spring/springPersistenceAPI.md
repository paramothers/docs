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

API - Transaction

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