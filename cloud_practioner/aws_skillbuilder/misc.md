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
* EBS is AZ only and on the same AZ as EC2 - EFS is regional - though ebs snapshots are regional 
* Encryped both root and non root volumes

* Redshift ML trains ML modeuls using SQL commands and utilise the trained model in DW for data forecasting
* Dynamo DB Accelerator DAX - in mem cache for dynamo db
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
* AppStream - secyre reliable scalable app streaming adn low cost vdi
* Athena - Serverless interactive sql query service for data analysis directly in s3 - results stored in s3
  * Supports json, csv, orc, avro,pq - commonly used in quicksight - allows federated queries in lambda
* Artifact - central resource for compliance related info
* Aurora - pg and mysql - serverless aws rds - cheap - 6 times data backup across 3 azs, autoback up to s3, 128tb storage upto 15 replicas
  * Separate storage and compute
* `Backup` - cost effective fully managed policy based service that simplifies data protection at scale
* `Billing Conductor` - Simplifies process of billing and reporting - NO ML Capabilities
* Cloudfront - Global CDN built for high performance security. uses shield and waf to mitigate ddos -
* CloudEndure - tool to minimise downtime and data loss - provides recovery of servers in cloud DR
* Code Build - CI
* Code Commit - private git repos
* Code Deploy - fully managed deployment service that automates deployments to ec2 fargate lambda **on prem etc**
* Code Guru - developer tool that provides ML recommendations to code quality and expensive lines of code
* Code Pipeline - CD
* Code Star - start developing in minute sin one place securely - full cicd 
* Cognito - serverless frictionless customer IAM - user pool and identity pool - id enables access to credentials 
* Comprehend - derive and understand valuable insifhts from text within docs using NLP
* `Config` - Assess audit and evaluate configs of your resources against desired cfgs
* Connect - customer service contact ceter
* `Control Tower` - a way for customers to send instructions to an aws account on how to deploy popeular tech
* Compute Optimiser - Analyses config and utilisation metrics of resources
* `Cost Anomaly Detection` - ML to monitor your cost and usage to detect unusual spending
* `Detective` - helps security teams conduct faster and more effective investigations using ML - identifioes security vulnerabilityies
* Eventbridge - serverless maanged event bud that integrates aws services
* `Forecast` - Provide accurate forecasts on app using ML.
* FSx - File server - fully managed windows 
* `Glue` - serverless to do ETL to convert data between formats - bookmarks prevent you processing old data
* GuardDuty - intelligent threat detection - ML - Continuous monitoring of network and account activity - independent runs
* HSM - Cloud HSM - manage single tenant hardware modules to generate crypto keys - can offload SSL from web servers
* Inspector - automated security assessments - ec2
* IQ - enables customers to quickly find, engage and pay aws certified 3rd party experts for on demand projec towrk
* `Kendra` - LLMs
* Kinesis - stream RT Data - streams, firehost, analytics video
* `Launch Wizard` - guides the way of sizing, configuring and deployinh resources for 3rd party apps
* Lightsail - VPS instances container storage - can migrate to EC2  - includes everything needed to lauch the project quickly
* `Lookout for Metrics` - Only finds anomalies in your system data for your apps - uses ML
* Macie - fully managed data security and data privacy service that uses ML and pattern matching to protect sensitive data
* Opensearch - query any field in a db  - used to be elastic search
* Ops hub - manager for snow family
* `ops works` - cfg management service to provide instances of chef and puppet - to control **cloud/onprem resources**
* outposts - extend aws infra to a mini region on your on prem center
* Personalise - personalised content and recommendations ML
* Personal Health Dashboard- provides alerts when event may impact a compays resources - planned maintenance etc
* `Pinpoint` - AWS’s digital user engagement service that enables AWS customers to effectively communicate with their end users and measure user engagement across multiple channels including email, Text Messaging (SMS) and Mobile Push Notifications.
* Polly - text to speech
* Rekognition - analysis of video and images for recognition and inappropriate content
* service catalog - centrally manage cloud resources to achieve governance  - written in tf or cloud formation
* Step function - serverless low code visual workflow service that developer use to build distreibuted apps , can integrate human approval
  * CLICK AND DRAG alike alteryx
* Storage GW - allows on prem servers to connect bvia on prem caching gateway to access s3 efs
* SWF - simple workflow - coordinate work across multiple distributed compoennts
* Timestream - fast serverless times eries db auto scaling
* Transcribe - speech to txt - multiple langauge- redact PII
* Transfer - data to and from s3/efs over ftp,sftp etc
* Transit Gateway - connects your VPC and on prem networks through a central hub - cloud router - data encyrpted
  * never crosses the internet - across regions accounts - jp standard public subnet connected to TGW to a proxy then internet
* VPC Endpoints - entry point to VPC that enables you to connect privately - removes need for nat gw and igw 
* VPC Peering - connect 2 vpcs to the aws network - cross region or account
* VPC Private Link - private connections between vpcs = without exposing data to traffic on Internet
* Security Hub - improve security posture by providing view of sec and compliance 
* Systems Manager - Secure e2e management solution for aws resources
* `Wavelength` - embeds AWS compute and storage iwthin 5 g networks - mopbile edghe computing
* `X ray`  - makes it easy for devs to analyse behaviour of distributed apps - with e2e tracing capabilities - preinstalled with beanstalk
  * troubleshoot an issue through multiple resources
  * Although you can troubleshoot the issue by checking the logs, it is still better to use AWS X-Ray as it enables you to analyze and debug your serverless application more effectively.

# Networking
ALB - operates osi layer 7- distributes traffic across multiple targets in multiple AZs supports http and https
  Context aware and direct requests based on any variable 
CLB - Classic Load Balancer - operates osi 4 and 7 legacy offering works with ec2
NLB - level 4 only - static ips
GLB - 3 and 4 - ip filtering

NACL - they process rules in order - starting with the loweest numbered rule when deciding to allow traffic

VPC is region level 
# Misc
Beanstalk USES Cloud formation under the hood
Customer Gateway device - physcial or softwar appliant you own or mange in on prem network - site to site vpm

trusted advisor - 5 pillars - cpsfs
cost optimisaton
performance
securuity
fault tolerance
serfice limits


sessions manager - under ssm - logs every time someone creates a sessions


6 r of cloud adoption
rehost
replatform
repurchase
retain 
retire 
refcator



Gov cloud regions - allow customers to host sensitive controlled unclassified ifno and regulated workloads 
  operated on by us entitiesand employees who are us citizens


Support plan - onlt business and above have api access
developer plan - technical support queries - unlimited

cloud trail - are spanned across all regions by default
Shared Responsibility MOdel - shared is awareness and trainign

ROUTE 53 is AZ level not regional  but GLOBAL!!


business support plan has well architected and operations reviews


iam policy simulator - not config - which asses and audits cfgs in your resources


instance metadata for ec2 for instance ID, instance profile permissions, and kernel information o

aws will charge you for data transferred between two regions

MFA delete on s3 
multipart load api for faster upload on s3 - single object as a set of parts - in any order, s3 will then assemble again
  over 100mb you should consider using multi part api upload in parallel too

youre allowed to do pen testing on 
RDS, ec2, cloudfron, aurora, api gw, lamdba lightsail and beanstalk


S3 only pay for data out 

security groups only accept ip addresses, cidr or other sg ids are destination and source
sqs messages are stored redundantly across azs


Only oracle db offers BYOL model

aurora is a self healing db

systems manager can centralise operational data and automate tasks - patch ec2 without edp