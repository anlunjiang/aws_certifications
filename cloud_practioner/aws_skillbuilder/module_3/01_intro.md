# Introduction

# Global Infrastructure and Reliability
 High availability and Fault tolerance comes with AWS with regional infrastructure
 
## Regions
* AWS Builds Data Centers in large groups called Regions 
* Inside each region are multiple data centers that have all the compute, storage and the other services to run apps.
* Each region is connected to other regions through high speed fibre network

Customers can choose which region you want to run your business from. Each region is isolated - your data does not 
go out of that region without explicit permission for that data to be moved.
* This is good for government compliance requirements for data

Region examples:
* us-east (Ohio) -------------> us-east-2
* us-east (N.Virginia) -------> us-east-1
* us-west (N.California) -----> us-west-1
* Asia Pacific (Melbourne) ---> ap-southeast-4
* Europe (Stockholm) ---------> eu-north-1

Each AZ will have a suffix letters attached - e.g. us-east-1a

Each region will have AT LEAST 3 AZs


## Choosing a Region

4 main factors goes into picking a region:

* Compliance
* Proximity
* Feature Availability - Some regions may not have all the services you want. New services need new hardware
  * e.g. AWS Braket - for Quantum computing - not all regions have the hardware required yet 
* Price - some regions are more costly to operate in e.g. Brazil with its Tax structure 

## Availability Zones
A single Data center, or group of data centers close to each other, an AZ. Each AZ has redundant power, networking and 
connectivity.

AZs can be 10s of miles from each other and still achieve single digit ms latency

* AWS BEST PRACTICE - Always runs your services across at least TWO AZs in a region.
  * This means redundantly deploying your infra in two difference AZs
* Many AWS Services are operating regionally, meaning they run across AZs without effort from you, e.g.
  * ELB - This is a regional construct - running on all AZs in a region 
    * Regional services by definition are highly available with not effort from you