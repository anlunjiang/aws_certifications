# DynamoDB
DynamoDB is a serverless NOSQL Key VALUE DB

Where you can just create tables. Table is where you can store and query data.
The Data in DynamoDB is organised into items - which has attributes which are features of your data

It will manage storage for you depending on how many items you have in the DB - so no need to worry about scaling
up or down 

Being serverless - it replicates and mirrors data across multiple AZs in multiple drives 

## Performance 
Being NoSQL it is very performant - and has ms response time - good coupled with scalability for millions of users to
access 

## Benefits of NoSQL - Non Relational DBs
RDBMS being traditional can have performance or scaling issues when under stress - think of transactions - which under
constraint mean no variation of data is allowed 

NoSQL swaps that rigidity for access at a high rate. So like NoSQL it has a simple flexible schema:
* Not every item in the table has to have the same attributes - in RDBMS this is not the case!
* You can run complex SQL on it - but on a small subset of attrs that are designated as KEYS  
* Not for a lot of complex joins - mostly query items from a single table 
* Granular API access as well


# RDS vs Dynamo DB 
* RDS
  * Complex Relational Joins and BI
  * A lot of overhead for updating data
* DynamoDB
  * Anything else 
  * Dont need complex joins and eliminates the overhead in RDBMS - makes it very fast 