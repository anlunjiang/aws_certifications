# Amazon Elastic File System

EFS is a managed file system - like shared file systems across their applications. e.g. multiple servers running analytics
and storing data on a shared file system 

EFS is this solution - but is managed by AWS for scaling and replication of data.
* Multiple instances can access the data in EFS at the same time
* It scales up and down as needed automatically 

## Difference between EBS and EFS 
* EBS attach to EC2 instances and are an **AZ level resource** only. EC2 and EBS **NEED** to be in the same AZ
  * Essentially just a hard drive - not proper file system - DOES NOT SCALE to give you more storage 

* EFS - is a **regonal resource** across multiple AZs - automatically scales 
  * True network file system for linux - so can be scaled horizontally - but more expensive than EBS
  * Duplicate storage enables concurrent access to data from all AZs in the region
  * Good for when users have multiple instances reading and writing to it simultaneously
  * Available also with Direct Connect 
