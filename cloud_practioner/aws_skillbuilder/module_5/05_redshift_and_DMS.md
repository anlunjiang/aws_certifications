# Amazon Redshift

Sometimes we need db for not - what is happening now, but what did happen historically - a data warehouse can handle 
when data becomes too complex to query historically in RDBMS 
 
Data Warehouses are for historical analytics, BI - THE KEY THING **The data is now set - no more changes to what we want to query**

DWs still have a lot of undifferentiated heavy lifting for maintaining the warehouse tuned, resilient and scaling etc

# Redshift Benefits
Redshift is basically Data warehousing as a service. Nodes in PB sizes are common
* Can handle massively large datasets - but also allows up to 10x higher performance than normal traditional dbs 

### Spectrum
Can run a single SQL query against exabytes of unstructured data in data lakes 


# DMS Data Migration Service 
For when you have a DB already that's on-prem or on the cloud. With DMS when you move to AWS you don't have to start from
scratch - helps you move your existing DB to AWS securely and safely 
* Source DB remains fully operational during migration - minimising downtime to apps 
  * Source and Target don't even need to be the same type 
  * Source can be EC2, On prem or on RDS already 
* Target can be EC2 or RDS
 
* Homogeneous migrations are easier - e.g. MySQL to RDS MySQL - since schema, types and code is the same basically

* Heterogeneous migrations where db source and target are different types 
  * Use SCT schema conversion tool 
    * Converts source schema and code like stored procs and functions 
  * Then use DMS to migrate the data 
Other use cases:
* dev and test migrations - when you want a copy of prod data for testing without affecting real prd db 
* consolidation and replication (DR or geographical reasons)


# Additional DBs
* DocumentDB (MongoDB compatible) - for content management, user profiles, catalogs 
* Neptune - Graph database - social networks and recommendation engines 
* Managed Blockchain - immutable financial ledger  - but is decentralised
* Quantum Ledger Database QLDB - immutable ledger - any entry can never be removed for audits 

Database Accelerators:
* Caching layers on top of dbs - **Elasticache** provides caching layers without worrying about launching uplift and maintenance.
  * comes in two flacours:  Memcached and Redis 
* DAX for dynamoDB - native caching layer - to improve read times for non relational data 