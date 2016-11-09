## MogonDB 3.2

1. dbpath - variable point to location, where all the data are stored
2. db - variable, is a handle for current DB.

### command line tool

1. mongod - executable file for Core Server
2. mongos - for routing request process
3. mongo - javascript shell to work with mongodb
4. mongodump - tool to create backup
5. mongorestore - tool to restore database from backup
6. mongoexport - tool to export data to any format of file
7. mongoimport - tool to import data from a file into document
8. mongosniff - tool to get know the status of command send to DB server

### Basic Factors

32 bit version support only 2gb data.

* its written in C++
* internally it store data in Binary JSON
* it has stored in a collection \( like Table in SQL DB \)
* index in MongodB implemented as B-Tree Structure
* 
* 
* 
* it provide offcial drivers for java, node.js, javascript, c\# and etc.

### Factors - 2

* No Transaction,

* No Schema\/ Table \/ Row

* No Join \/ foreign key

* it is good for Web application like blog or any complex data structure

* it use its own standard \(BSON\) to store data, it is Binary JSON. it is fast to traverse and indexing

* 

