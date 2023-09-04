# Relational Database Service RDS

RDBMS provisioning:
* MySQL
* PostgreSQL
* Oracle
* MSSqlServer
* MariaDB
* Aurora - databse engine

Can do lift and shift for existing databases - using **Database Migration Service DMS** to EC2 - this essentially
take your current db and shift everything including os, memory, compute etc to EC2 like for like no diff.

## RDS
The other way is to use RDS - which is a more managed service.
* RDS offers encryption at rest (protecting data when stored)
* Encryption in transit (protecting data while being sent and received)
* 

RDS provides the following with AWS which is done for you - removing need to maintain:
* Automated patching
* Backups
* Redundancy 
* Failover
* DR

## Aurora
If you want even more of a managed service - you can migrate or deploy to Amazon Aurora. AWS offers this as the
**MOST managed** relational database option offering as:
* MySQL 5x faster than standard MySQL databases
* PostgresSQL 3 x faster than standard

Boasts 1/10th of the cost of commercial databases - by reducing unnecessaru IO operations
* Data is replicated 6 times at any time
* Can deploy up to 15 read replicas - offloading reads and scales performance 
* Continuous backups to S3 - always have a point to restore  
  * This goes hand in hand with Point in Time recovery too 

Use if your workloads require high availability - (kind of like spanner for GCP). It replicates 6 copies across
3 AZs and backs up data all the time to S3
