# EC2
* Types of EC2 instances 
  * General Purpose - Web servers or code repos, small medium dbs
  * Compute Optimised - Compute intensive tasks - like gaming servers - Scientific modelling or RT processing, batch
  * Memory Optimised - large datasets in memory - high ram - large data to be preloaded before running for RT processing
  * Accelerated Computing - Floating point number calculations - Graphics processing - Utilise hardware accelerators
  * Storage Optimised - high sequential read and write access to large db on local storage - fast IO - DW

* EC2 pricing has on demand and savings plan (which saves up to 72%)
  * Also applies to lambda and fargate
  * On-demand, savings, dedicated host (single tenancy), reserved instances, spot instances  
  * Dedicated hosts retain software license 

# Storage and DBs
* EBS is AZ only and on the same AZ as EC2 - EFS is regional 
* Redshift ML trains ML modeuls using SQL commands and utilise the trained model in DW for data forecasting

# IAM
temp permissions - look for roles - not policies or groups
prohibited actions are listed in the acceptable use documentation by aws

# Support
aws professional service org is a global team of experts to help accelr ate cloud adoption
APN Consulting Partners are professional services firms that help customers of all types and sizes design, 
architect, build, migrate, and manage their workloads and applications on AWS, accelerating their journey to the cloud.”


# Cloud Concepts
Billy pe gi prov se or ...
* 6 Perspectives of Cloud Adoption Framework 
  * Business - ensure that your cloud investments deliver business outcomes CFO, CTO
  * People - Bridge between tech and business - CIO COO - organisational and leadership structure
  * Governance - minimise risks and maximise benefit - CTO, CFO, CDO
  * Platform - Helps build scalable platform - modernise workloads and cloud native solutions - CTO, tech managers, engineers
  * Security - Achieve security - CISO, CCO, Audit 
  * Operations - ensures cloud services are delivered at a level that meets business - infra leaders ,SRE, etc


Oscar Securely Rides Perfumed cu sus...
* 6 Pillars of a well architected framework
  * Operational Excellence
    * Operations as code
    * small frequenct reversible changes
    * refine operations procedures frequenctly
    * anticipate failure
    * learn from all operational failures
  * Security
    * Shared Responsibility Model
    * IAM
    * Detective Controls - Cloudtrail, GuardDuty
    * Infra Protection - VPC - CloudFront AWS Shield, WAF
    * Data Protection
    * Incident Response
  * Reliability
    * Foundations
    * Change Management - cloudtrail autoscaling etc
    * Failure Management - Cloud formation s3
  * Performance efficiency
    * Review Monitoring - Cloudwatch
    * Autoscale
  * Cost Optimisation
    * Cost Explorer
  * Sustainability
    * Region Selection

# Other Services
* Cost Anomaly Detection - ML to monitor your cost and usage to detect unusual spending
* Billing Conductor - Simplifies process of billing and reporting - NO ML Capabilities
* Lookout for Metrics - Only finds anomalies in your system data for your apps - uses ML
* Forecast - Provide accurate forecasts on app using ML. 
* Compute Optimiser - Analyses config and utilisation metrics of resources
* Launch Wizard - guides the way of sizing, configuring and deployinh resources for 3rd party apps