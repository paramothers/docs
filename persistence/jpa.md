OVERVIEW


Best Practice
 JPA 2.1 - API
 JPA - persistence config
 General

------------------------------------------------------------------------



SHEET 1: _BEST PRACTICE_


  ------- -----------------------------------------------------------------------------------------------------------------------------------------------
          Better have separate project for JPA with its test case. So this project can be used by many application those want to use the same database.
          Dont have DAO classes inside of JPA project. Since service layer may be with or without spring
          And also, deverloper may add any logic / log / etc. in his DAO class .

  ID      use wrapper instead primitive type, to allow null for unsaved objects

  Field   try to avoid use of Public field
  ------- -----------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------



SHEET 2: _JPA 2.1 - API_


  --------------------------------------------- ------------- ---------------------- ---------------------------------------- ------------------- --------------------------------------------
                                                                                                                                                  
  Persistence class used only in Java SE        Persistence                                                                                       
                                                              EntityManagerFactory   EntityManager                                                
  EntityTransaction also used only in Java SE                                                                                 EntityTransaction   
  when result type unknown or dynamic queries                                                                                 Query               
  when result type known                                                                                                                          TypedQuery ( used for Static/named query )
                                                                                                                              CriteriaBuilder     
                                                                                                                                                  CriteriaQuery ( used for Dynamic Query )
                                                                                                                                                  
                                                                                                                                                  
                                                              PersistenceProvider    org.hibernate.ejb.HibernatePersistence                       
  --------------------------------------------- ------------- ---------------------- ---------------------------------------- ------------------- --------------------------------------------

------------------------------------------------------------------------



SHEET 3: _JPA - PERSISTENCE CONFIG_


  --------------- -------------------- ------------------------------ ------------ --------------------------------- ------------------
  <persistence>                                                                                                      
                  <persistence-unit>                                               name                              transaction-type
                                       <provider>                                                                    
                                       <jta-datasource>                                                              
                                       <non-jta-datasoruce>                                                          
                                       <mapping-file>                                                                
                                       <class>                                                                       
                                       <jar-file>                                                                    
                                       _<exclued-unlisted-classes>_                                                  
                                       <shared-cache-mode>                                                           
                                       <validation-mode>                                                             
                                       <properties>                                                                  
                                                                      <property>   name                              value
                                                                                                                     
                                                                                   javax.persistence.jdbc.driver     
                                                                                   javax.persistence.jdbc.url        
                                                                                   javax.persistence.jdbc.user       
                                                                                   javax.persistence.jdbc.password   
  --------------- -------------------- ------------------------------ ------------ --------------------------------- ------------------

------------------------------------------------------------------------



SHEET 4: _GENERAL_


  ------------------------------------------------------------------------------------
  Toplink from oracle first developed for SmallTalk language, now suppot java
  Toplink is commercial product
  Hibernate is open source
  JDBC released in 97 in JDK 1.1
  EJB Entity bean was added in J2EE
  JDO is next attempt after few failure of EJB entity bean, it enhance the byte code
  JPA, introduced by combination of vendors, taken few feature from JDO
  JPA 1.0 released in 2006
  JPA 2.0 released in 2009
  JPA 2.1 released in 2013
  ------------------------------------------------------------------------------------
