------------------------------------------------------------------------



OVERVIEW


Version
 API
 Type of drivers

------------------------------------------------------------------------



SHEET 1: _VERSION_


  ------ -------------------------------------
  JDBC   introduced in 1997, Jdk 1.1 version
  ------ -------------------------------------

------------------------------------------------------------------------



SHEET 2: _API_


  --------------- ----------------------- -------------------
  DriverManager   datasource properties   
  Connection                              
                  DatabaseMetadata        
                                          Statement
                                          PreparedStatement
                                          CallableStatement
  ResultSet                               
                  ResultSetMetadata       
  --------------- ----------------------- -------------------

------------------------------------------------------------------------



SHEET 3: _TYPE OF DRIVERS_


  ---------------------------------------------- ---------------------------------------------------- ----------------------- --------------------------------
  TYPE 1                                         TYPE 2                                               TYPE 3                  TYPE 4
                                                                                                                              
  written native language                        partially native(c,c++) languge, partially java      need middle ware        100 % java
  OS dependent                                   partially OS dependent                               Middle ware dependent   java dependent
  thick driver                                   thick driver                                         thin driver             thin driver
  need client installation                       need client installation                             no client install       no client install
                                                                                                      DBMS independent        
  error handling is not in application control   error handling is not in application control                                 
  oracle's odbc                                  Oracle OCI                                           not available           Oracle thin
                                                 it is best if application has more usage of pl/sql                           
                                                                                                                              applet must use this type only
  ---------------------------------------------- ---------------------------------------------------- 
