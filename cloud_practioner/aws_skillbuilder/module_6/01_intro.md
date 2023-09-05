# Introduction

Shared Responsibility Model:
* AWS Controls security of the cloud
  * data centers
  * security of db, network, compute etc
* Customers control security IN the cloud
  * workloads that run in the cloud security 

e.g. EC2 host lives in a physical data center that must be secured and is networked with a hypervisor - this is
managed by AWS
On top of the instance is the OS, application and data managed by the customer. Customer is in charge of the security
inside the EC2, encryption key for root login 

No one can deploy anything but you - even AWS - it can only say your resources are out of date or need patching

Entity responsible	Part of the AWS Environment
Customer	         
* Customer data
* Platform, applications, Identity and Access Management (IAM)
* Operating systems, and network and firewall configuration
* Client-side data encryption, server-side data encryption, and networking traffic protection

Amazon Web Services (AWS)
* Software: Compute, storage, database, networking
* Hardware: Regions, Availability Zones, Edge Locations

