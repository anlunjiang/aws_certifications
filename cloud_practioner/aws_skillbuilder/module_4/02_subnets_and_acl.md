# Subnets and Network Access Control Lists

Reminder - VPCs are a isolated network where data can only come win through gateways. But AWS offers more services to make sure your data and application is secure:
* Network Hardening
* Application Security
* User Identity
* Authentication and Authorisation
* DDoS prevention
* Data Integrity
* Encryption

# Subnets
To control access to the gateways. 
* Public subnets have access to the internet gateway - private subnets do not
HOWEVER:
* Subnets **also** can control traffic permissions

## ACL Access Control Lists
When packets of data enter or exit a subnet boundary - it gets checked against an Network ACL. This check determines if 

