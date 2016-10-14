
## MogonDB 3.2

 1. dbpath - variable point to location, where all the data are stored
 2. db - variable, is a handle for current DB.
 3. mongod - executable file for Core Server
 4. mongos - for routing request process
 5. mongo - javascript shell to work with mongodb

32 bit version support only 2gb data. 
* its written in C++
* internally it store data in Binary JSON
* it has stored in a collection ( like Table in SQL DB )
* index in MongodB implemented as B-Tree Structure
* Secondary index is another feature. upto 64 possible per collection
* Replication Set
* Speed and Durability
* Designed for Horizantal scaling rather than Vertical scale (sharding)