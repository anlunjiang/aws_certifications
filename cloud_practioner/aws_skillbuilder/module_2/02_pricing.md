# Pricing Compute in Cloud

Multiple billing options are available for EC2 instances

* On-demand - Only pay for the duration that your instance runs for - no long term or upfront payments needed
  * Most popular option - good for playing around and getting started 
* Savings Plan - Lower prices in exchange for a commitment of consistent usage - measured in dollars per hour
  * This is for a one or three year term 
  * Can save up to 72% off your compute usage cost 
  * !!Also applies to fargate or lambda usage as well!!
  * Any usage above the commitment is on demand price 
* Reserved Instances
  * Steady state workloads - or predictable usage - up to 75% savings
  * One to three year term 
    * Can pay partially, all upfront, or no upfront 
    * end of contract you go back to on demand price until you renew 
  * **Standard reserved instances**
    * If you know the EC2 type and size you need for your steady state apps and which region you want 
  * **Convertable Reserved Instance**
    * In different AZ zones or different instance types. You trade in a deeper discount when you require flex
* Spot Instances
  * Spare EC2 instance capacity for up to 90% off on demand price 
  * AWS can reclaim the instance at any time - with 2 min warning - good for workloads that can handle downtime
    * e.g. batch workloads  
* Dedicated Hosts
  * For meeting compliance requirements - nobody will share tenancy of the host
  * Expensive!