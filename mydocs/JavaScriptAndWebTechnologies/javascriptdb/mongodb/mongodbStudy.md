
## MogonDB 3.2

 1. dbpath - variable point to location, where all the data are stored
 2. db - variable, is a handle for current DB.

32 bit version support only 2gb data. 
* internally it store data in Binary JSON
* it has stored in a collection ( like Table in SQL DB )
* index in MongodB implemented as B-Tree Structure
* Secondary index is another feature. upto 64 possible per collection