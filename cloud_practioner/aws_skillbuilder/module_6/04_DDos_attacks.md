# Denial of Service Attacks 
DDos shuts down apps ability to function by overwhelming the system

## UDP Flood 
Requesting large amounts of data from an app but giving itself as the return address - this is a low level brute force
attack 

This is solved with SGs! Only allow the proper request traffic - and blanket denies all others. Design request protocl 
to be differn to your return protocol to differentiate 

SGs operate on an AWS network level despite being attached to a resource - so its denied by the entire regions capacity
not the ec2 capacity 
## HTTP level attacks 
Look like normal requests - but repeatedly from multiple machines. They overwhelm actual real requests
* Slow Loris Attack
  * Attacker pretends to have a really slow connection    
  * until a thread gets the entire packet - it cant move to the next packet

This is solved by ELBs - it can handle all the other good requests and send to server- whislt waiting for the slow loris
to give all the packets - and its scalable regionally so its difficult to overwhelm


## AWS Shield Advanced with AWS WAF (Web Application Firewall)
For strongest most sophisticated attacks
WAF filters traffic from signatures of malicious packets - powered by ML and is constantly learning  
* Can have custom rules to mitigate complex DDoS attacks

NOTE: Shield standard is enabled for all aws customers at no cost by default.


WAF is the firewall that lets you monitor network requests that come into your web apps. Works with cloudfront and ALBs. 
WAF works like NACLs to block or allow traffic. But it uses a Web Access Control List instead (list of IPs) operating
on the web level - NACl is only subnet level


## Additional Security Services

### KMS - key management store
ensures data is secure when in storage and when in transit
* Encryption at rest
* Encryption in transit

Uses cryptographic keys to decrypt data - keys are managed by you and can be used by many resources 
* Can specify which users and roles are able to use keys
* Can disable keys
* never leaves KMS

e.g. DynamoDB has server side encryption at rest on all data - or redshift using SSL to transport encrypted data
and use certs to validate and auth client. SQS, RDS S3 etc all have this 

### AWS Inspector 
Helps improve security and compliance of deployed apps - running automated security assessments 
* Checks deviations of security best practices 
Consists of 3 parts
* Network config reachability 
* Amazon agent - installed on EC2 instances 
* Security assessment service 

Provides recommendations on how to fix too - and findings can be retrieved via API 


### AWS Guard Duty
Threat detection service - analyses continuous steams of metadata and network activity from your account from cloud trail
events, VPC flow logs and DNS logs

* integrated threat intelligence to detect known malicious IPs
* ML 
* Anomaly detection 

Runs independently from other AWS services - so won't affect performance or availability 