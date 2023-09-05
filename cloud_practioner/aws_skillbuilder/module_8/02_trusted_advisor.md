# Trusted Advisor
Automated advisor 
Web service that inspects your AWS env and provides RT recommendations in accordance with AWS best practices

Evaluates across 5 pillars:
* Cost optimisation - underutilised EC2 / resources
* Performance  - EBS vs EC2 compatibility - no point using fast EC2 for IO is the EBS is slow
* Security - MFA, passwords, SGs
* Fault tolerance - EBS not backed up, dist of AZs or resources
* Service limits - VPC limit - e.g. regional limit of 5 

Can view the reports in the console - some checks are free and others depend on your support plan

Can have alerts to advise when you are close to a limit or have red issues recommended for action

For each category:

The green check indicates the number of items for which it detected no problems.

The orange triangle represents the number of recommended investigations.

The red circle represents the number of recommended actions.