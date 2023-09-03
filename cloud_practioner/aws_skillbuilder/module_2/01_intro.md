# Introduction

## AWS EC2 - Elastic Compute Cloud
* Highly flexible
* Cost-effective
* Quick

* Only pay for running instances - NOT stopped or terminated instances

### Shared Resources 
* EC2 instances are run on host machines - each "instance" is actually just a VM that runs on the host. Many instances 
live on this host machine
* Hypervisor is responsible for sharing the underlying physical resources
  * The idea of sharing hardware is known as `multitenancy` - this is coordinated by the hypervisor
  * Hypervisor isolates the VMs from each other - making instances secure 

### Configuration of the instances
* Choose OS - Windows, Linux
  * Complete control over the software and what runs 
* Resizable - Able to vertically scale the instance 
* Networking control - Control type of request that comes to and from the server 

## Types of instances
Each EC2 instance type is grouped under an instance family - and are optimised for certain tasks. They are usually
a combination of varying cpu, memory, storage and networking capacity

* General Purpose
  * Good balance of compute, memoery and networking resources 
  * Diverse workloads 
  * Web servers or code repos, small medium dbs
* Compute Optimised 
  * Compute intensive tasks - like gaming servers  
  * HPC - High performance computing  
  * Scientific modelling or RT processing 
* Memory Optimised
  * Memory intensive calcs - large datasets in memory - high ram
  * e.g. app that needs large data to be preloaded before running for RT processing
* Accelerated Computing
  * Floating point number calculations
  * Graphics processing
  * Data pattern matching
  * Utilise hardware accelerators
* Storage Optimised
  * Good for workloads that require high performance for locally stored data 
  * Workloads that require high sequential read and write access to large db on local storage
  * fast IO 
  * data warehousing