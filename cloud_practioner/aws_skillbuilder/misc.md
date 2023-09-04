
# Intro
* Hypervisor in VMs is the software layer that lets you run the VMs on a host and manages multitenancy
* Hybrid cloud deployment - using private and public cloud together

# Compute in the cloud
* Types of EC2 instances 
  * General Purpose
      * Good balance of compute, memoery and networking resources
      * Diverse workloads
      * Web servers or code repos, small medium dbs
  * Compute Optimised
      * Compute intensive tasks - like gaming servers
      * HPC - High performance computing
      * Scientific modelling or RT processing
      * Batch workloads
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

* EC2 pricing has on demand and savings plan (which saves up to 72%)
  * Also applies to lambda and fargate
  * On-demand, savings, dedicated host (single tenancy), reserved instances, spot instances  




**ebs is az only
efs is regional**
