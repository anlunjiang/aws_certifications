# AWS Organisations 
 
A central location to manage multiple AWS accounts 

Can manage billing, security compliance and shared resources across multiple accounts 

* Consolidated billing - primary account to consolidate fees and pay for all the member accounts 
  * Bulk discounts 
* Hierarchical groupings to meet security or compiance regulations 
  * group accounts into organisational units OUs - AWS Organisations is a service to create OUs
  * E.g. an OU will be all accounts that can access highly confidential resources
  * another OU for developers 

## Service Control Policies  
specify the maximum permissions for members accounts in the org - only available for admin accounts in the org   
Can restrict which AWS services, resources and API actions that users/roles in each member account can access - this 
is a blanket restriction 

## Compliance 
AWS already meet compliance in terms of Data center , security and networking - so we inherit all that already/ 
So some compliance is already given when you are with AWS 

**AWS WILL NOT auto replicate data across regions by default - DUE TO DATA REGULATIONS**

You can request from AWS documents that they are following best practices from **AWS Artifact** 

### AWS Artifact
Gain access to compliance reports done by 3rd parties - AWS Compliance center also will show compliant info already out, like
documentation like the risk and security whitepaper. 

* Artifact agreements:
  * Review accept and manage agreements for an account in aws organisations - addresses HIPAA GDPR etc
* Artifact reports:
  * Compliance reports from 3rd parties auditors - which you can provide to your own auditors 

Compliance CENTER is like a hub for resources to help learn about aws compliance