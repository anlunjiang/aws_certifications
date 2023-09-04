# Introduction - Storage and DBs

# Instance Stores and Amazon Elastic Block Store 
* Block level Storage - essentially just normal harddrives and ssds
  * bytes stored in blocks on disc - when a block is updated - the whole series of blocks arent overwritten, but instead just the parts that need to be.
    * This is really good for databases or file systems
   
    
When you create an EC2 instance - it will create **instance store volumes** physically attached to the host.
BUT if you stop of terminate the EC2 instance, all data written to the instance store volume will be deleted.
**Instance store volumes should not store important data** - instead use EBS

# Amazon Elastic Block Store EBS
Create virtual hard drives called **EBS Volumes** not attached to EC2 instances - separate drives from host drives - so if EC2 goes down - your data persists 
You can configure the:
* Size up to 16tb each
* Type - SSD by default but HDD option is available
* Configuration 

You can back up your data using **snapshots** - recommended to be taken regularly - this way all data is backed up. 
Snapshots are incremental - meaning that the first backup takes all data - but subsequent backups only the blocks of data that changed since the most recent snapshot are saved



# S3 - Simple Storage Service 
Bucket data - blob/object storage, regionally scoped and unlimited storage (5tb per object). Each object consists of data, metadata and a key
* Metadata contains size, what the data is and how used
* Key is the unique identifier


* Max size of an object is 5TB
* Can version objects to protect from deletion
* Limit permissions to who can see and access objects
* Good also for static website hosting - html and webassets into a bucket and host as a website 
 
## Different tiers of storage for how often data is accessed 
S3 objects can go through lifecycle policies that span across tiers automatically given time: (common/important tiers in bold)

* **S3 Standard** - 11 9s of durability - 99.999999999% chance object is intact after one year
  * Data is stored in at least 3 facilities - so can sustain concurrent loss of data in two separate storage facilities
  * Higher cost compared to others due to high availability
 
* **S3 Standard Infrequent Access (IA)**
  * For data accessed less frequently but can be rapidly accessed when needed - higher retrieval price but lower storage price 
  * Good for backup, DR files etc

* S3 One Zone Infrequent Access (One Zone IA)
  * only in one AZ compared to usual min 3 - lower storage price than standard IA
  * Good for savings and can easily reproduce data in the event of AZ failure

* S3 Intelligent Tiering
  * Ideal for data with unknown or changing access patterns - requires small monthly monitoring and automation fee per object
  * Monitors usage patterns and automatically moves it across the tiers - like a dynamic object lifecycle

* S3 Glacier Instance Retrieval
 * Good for archived data that requires immediate access - within a few ms
 * same ms retrieval as S3 standard - but probably a lot more expensive

* **S3 Glacier Flexible Retrieval**
  * For archive data or audit data that doesnt need to be retrieved
  * Created with vaults populated with archives
  * can lock for an amount of time
  * WORM - write once read many - can lock data from future edits
  * Options for retrieval - minutes to hours

* S3 Glacier Deep Archive
  * Long term retention - lowest cost that is ideal for archiving. Retrieval within 12 to 48 hours.
  * All objects ar replicated and stored across 3 AZs

* S3 Outposts
  * S3 buckets on outposts - easier to retrieve store and access data  on your on prem environment.
  * Not in multiple AZs obviously but stored durable across redundant devices within your on prem outposts
  * Good for data with local data residency requirements that must be close for latency purposes
 

# EBS vs S3
S3 - Good for satic files that are accessed by may at once like static files or websites - no need to think about durability too and is cheaper and serverless
EBS - large video files - if you are updating very often or want local db - you can do delta updates. S3 cannot do that. 
