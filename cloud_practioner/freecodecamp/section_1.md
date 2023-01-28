## Evolution of Cloud Hosting
* Dedicated Server - One physical machine dedicated to a single business
  * Expensive
  * High Maintenance
  * High Security
* Virtual Private Server - One machine dedicated to a single business but can run multiple web apps / sites
  * Better utilisation and isolation of resources
* Shared Hosting - One physical machine - shared by many businesses 
  * Relies on tenants underutilising their resources
  * Very cheap
  * limited functionality
  * Poor isolation
* Cloud Hosting - Multiple machines that act as one system - abstracted into multiple cloud services
  * Flexible
  * Scalable
  * Secure
  * Cost effective
  * Configurable

## Services
The four most common types of services:
* Compute
  * Elastic Compute Cloud (EC2)
  * AWS Infrastructure - GPU and AI workloads - like GCP Tensorflow
  * AWS Bracket - Quantum Computing
* Networking
  * VPC Private Cloud Network
* Storage
  * Simple Storage Service (S3)
* Databases
  * RDS SQL Databases

There are many others but these are the 4 main core services 
* Simple Queue Service (SQS)



## What is a Cloud Service Provider (CSP)
* Provides multiple cloud services e.g. 10s-100s of services
* Those services can be chained together to create cloud architectures 
* Services are accessible via a Single Unifire API e.g. AWS API
* Uses metered billing based on usage
* Monitoring builtin - e.g. AWS CloudTrail
* IaaS Offering - Networking, Storage Compute etc
* Automation via Infrastructure as Code (IaC)

(Route 53) Domain Name ---> (ELB) Load Balancer ---> (EC2) Webserver ---> (RDS) Postgres DB
                                                                     ---> (SES) Send Emails
                                                                     ---> (QuickSight) Analytics
                                                                     ---> (S3) Stores images

If a company offers multiple cloud services under a single UI but do not meet most or all of these requirements
then it is a cloud platform -e.g. Twilio, Hashicorp, Databricks


## Serverless Compute or Functions
Managed VMs running managed containers 
* Upload a piece of code - choose the amount of memory and duration
* Very cost-effective and only pay for the time code is running = VMs only run when there is code to be executed
* BUT - Cold starts are a side effect - where VMs need to spin up at the beginning and be slow at first 

## Types of Cloud computing
* SaaS - a product run and managed by the service provider - no need to worry about how it is maintained - CUSTOMERS
  * It just works and remains available
  * Office 365, Gmail
* PaaS - Deployment and management of apps - no need to worry about provisioning, configuring or understanding hardware - DEVELOPERS
  * Elastic Beanstalk, Heroku, Google App Engine
* Iaas - Basic blocks for cloud IT - access to networking features, compute and storage - ADMINS
  * Dont worry about IT staff, data centers and hardware

## AWS Account
There are two main accounts types
* Root - unrestricted including billing
* IAM - restricted - recommended to always login with this usually

## Billing Alerts
There are billing alerts - which you can set in your billing dashboard and will tell you when you go over a certain 
spend

* Cloudwatch is a collection of services that can monitor all sorts of metrics, with logging - kind of like stackdriver
  * Can monitor billing as well and can send email alerts when charges exceet your defined threshold

## Youtube Time bookmark
1:03:21

