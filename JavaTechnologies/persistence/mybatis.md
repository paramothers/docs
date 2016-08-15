OVERVIEW


General
 Mybatis-xml-mapping
 Mybatis-xml-configuration
 Java-API
 Compare of iBatis & Hibernate
 LLR Mybatis use

------------------------------------------------------------------------



SHEET 1: _GENERAL_


  -------- --------------------------------------------------------------------------------------
  Ibatis   
           it is for simplicty
           it is SQL-Centric framework. But hibernate java-centric framework, where SQL hidden.
           
           
           started at 2002
  -------- --------------------------------------------------------------------------------------

------------------------------------------------------------------------



SHEET 2: _MYBATIS-XML-MAPPING_


  -------------------------------------- -------- ----------- ------------- -------- ---- --------------- ------------ ------------------ ------------- --
                                         mapper                                           namespace                                                     
                                                                                                                                                        
                                                  Insert                             id   parameterType                useGeneratedKey    keyProperty   
  used when Sequence used                                     selectKey                                   resultType   order              keyProperty   
                                                  update                             id   parameterType                                                 
                                                  delete                             id   parameterType                                                 
                                                  select                             id   parameterType   resultType   resultMap                        
                                                                                                                                                        
                                                                                                                                                        
                                                  resultMap                          id                   type                                          
                                                              ID                                                       column             property      
                                                              result                                                   column             property      
  for one-to-one                                              association                 select          javaType     resultMap/column   property      
  if the association defined as inline                                      id                                                                          
  if the association defined as inline                                      result                                                                      
                                                              collection                  select                       resultMap          property      
                                                                                                                                                        
                                                                                                                                                        
                                                  mapper                                  namespace                                                     
  -------------------------------------- -------- ----------- ------------- -------- ---- --------------- ------------ ------------------ ------------- --

------------------------------------------------------------------------



SHEET 3: _MYBATIS-XML-CONFIGURATION_


  --------------- -------------------- ------------- -------------------- ---------- -- ------------- --------- ---------- ----------
  Configuration                                                                                                            
                  Environments                                                          default                            
                                       Environment                                      id                                 
                                                     transactionManager                 type                               
                                                                          property      name          value                
                                                     datasouce                          type                               
                                                                          property      name          value                
                  Mappers                                                                                                  
                                       mappers                                          resource      classs    url        
                                       package                                          name                               
                  properties                                                                                               
                                       property                                         name          value                
                  settings                                                                                                 
                                       setting                                          name          value                
                  typeAliases                                                                                              
                                       typeAlias                                        name          alias                
                  typeHandlers                                                                                             
                                       package                                                                             
                                       typeHandler                                                    handler   javaType   jdbcType
                  databaseIdProvider                                                    type                               
                                       property                                         name          value                
                  plugins                                                                                                  
                                       plugin                                           interceptor                        
                                                     property                           name          value                
                  objectFactory                                                         type                               
                                       property                                         name          value                
  --------------- -------------------- ------------- -------------------- ---------- -- ------------- --------- ---------- ----------

------------------------------------------------------------------------



SHEET 4: _JAVA-API_


  ------------------------------------------------------------- --------------------------- ---------------------- --------------------- --------------------------- ---------------------------
                                                                                                                                                                     
                                                                                                                                                                     
                                                                SqlSessionFactoryBuilder                                                                             
                                                                                            SqlSessionFactory      SqlSession                                        
                                                                                            Configuration                                                            
  Environment rep. Each database                                                                                   Environment                                       
                                                                                                                   DataSourceFactory     UnpooledDataSourceFactory   
                                                                                                                                         BlogDataSourceFactory       
                                                                                                                                         Datasource                  PooledDataSource
  application itself handle tranactions                                                                                                  TransactionFactory          JdbcTransactionFactory
                                                                                                                                                                     ManagedTransactionFactory
                                                                                                                                                                     Transaction
                                                                                                                   TypeAliasRegistry                                 
                                                                                                                   TypeHandlerRegistry                               
                                                                                                                   Mapper                                            
  it is utiliy to create dynamic sql                            SQL                                                                                                  
                                                                                                                                                                     
  it is from mybatis-spring api                                 MapperScannerconfigurar                                                                              
  it is from mybatis-spring api                                 MapperFactoryBean                                                                                    
                                                                                                                                                                     
  default enum type handler                                     EnumTypeHandler                                                                                      
  enum ordinal value stroed in DB instread of string itself     EnumOrdinalTypeHandler                                                                               
                                                                                                                                                                     
  to load my batis configuration file from different location   Resources                                                                                            
                                                                                                                                                                     
  used for pagination by setting offset, limit                  RowBounds                                                                                            
  custom ResulstSet handler                                     ResultHandler               ResultContext                                                            
                                                                                                                                                                     
  base class for define custom type handler                     TypeHandler                 BaseTypeHandler                                                          
                                                                                                                                                                     
                                                                DatabaseIdProvider                                                                                   
                                                                                                                                                                     
  plugin api to intercept                                       Interceptor                                                                                          
                                                                                            Executor                                                                 
                                                                                            ParameterHandler                                                         
                                                                                            ResultSetHandler                                                         
                                                                                            StatementHandler                                                         
                                                                                                                                                                     
  this factory create our domain object for every row           ObjectFactory               DefaultObjectFactory                                                     
                                                                                                                                                                     
                                                                TransactionIsolationLevel                                                                            
                                                                ExecutorType                                                                                         
  ------------------------------------------------------------- --------------------------- ---------------------- --------------------- --------------------------- ---------------------------

------------------------------------------------------------------------



SHEET 5: _COMPARE OF IBATIS & HIBERNATE_


  --- ------------------------------------------------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------
      IBATIS                                                                                      HIBERNATE

                                                                                                  

  1   Simplicty. Only 2 configuration file, only need 3 Jar files. Use of very few API.           It need separate mapping file for each object. It has API, HQL, Criteria API, Qery by Examples, mapping of OOPs like inheritance, Abstract class
                                                                                                   it need a lot of jar file to be run

  2   Since, it externalize SQL, have full Control of SQL, even easy to debug or tune the query   since SQL automatically generated.

  3   avoid Reptition of JDBC code                                                                

  4   it is good for Single DB. Avoid use of iBatis if a application has more than DB             it can be used even more than one DB.

  5   when use of Legacy or existing DB, iBatis is good                                           Hiberenate is good for Fresh DB design application

  6   it is Query Mapping tool                                                                    it is ORM tool

  7   it don’t have any machanism to avoid record level locking for concurrent modification       it has

  8   it don’t have ability to referenced object update or delete in owned object update/delete   it has

                                                                                                  

                                                                                                  

      in Developer aspect, avoid repeatition code for JDBC                                        

      in Developer aspect, easy to learn and practice                                             

      in PM aspect, getting more productivity                                                     
  --- ------------------------------------------------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------



SHEET 6: _LLR MYBATIS USE_


  -----------------------------------------------------------
  use 'databaseId' in every stataement to note the database
  -----------------------------------------------------------
