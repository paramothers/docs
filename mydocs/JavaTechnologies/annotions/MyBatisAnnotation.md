
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
