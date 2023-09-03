# Scaling EC2

Two benefits of EC2 on AWS is scalability and elasticity - how capacity can grow or shrink based on needs.

* Scalability - beginning with resources you need and designing infra so that it auto scales by demand. Only pay for 
the resources you use. No need to worry about lack of computing. 

This scaling is done by AWS **EC2 Auto Scaling**
* Dynamic Scaling
  * Response to changing demand - a bit of lag
* Predictive Scaling
  * Auto schedules the right number of instances based on predicted demand

You can use both scaling together to be even faster

## Different ways to scale
* Scaling Up
  * Vertically scaling up 
* Scaling Out
  * Horizontal Scaling

You can decouple your system so they have different scaling groups - each group can have a minimum capacity, desired
and max capacity. `Desired capacity defaults to minimum if none is specified`



# Directing Traffic with ELB

ELB is basically like a host in the coffee shop analogy directing customers (requests) which cashier (instance) to go 
to - simple algo would be to calculate the usage of the CPU/MEM of the instances and direct new requests to the least 
used one - so there is an even dist of requests across the instances 

This is called **LOAD BALANCING** - this is an app that takes requests to route to instances 
* High Performance
* Cost-efficient
* Highly Available
* Auto Scalable

The generic AWS one is Called Elastic Load balancing ELB - undifferentiated load balancing
* Regional Construct - This means it runs on a region level not instance level - making it highly available
* Autoscalable - designed to handle more throughput with no change in the hourly cost! 
  * ASG lets ELB know new instances are online - and so ELB can start sending requests 
  * Once ASG is ready to terminate instances - it lets ELB know to stop new requests to that instance
    * Wait for existing workloads to finish and terminate

* ELB isnt just for front end - it can decouple your infra internally as well between say front and backend
  * The same principle works 
  * As long as your resources are in the same region this can happen 

