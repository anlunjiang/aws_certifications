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
* Public subnets have access to the internet gateway - so contain resources that need public access - like a website
* Private subnets do not have IGW access - e.g. databases
HOWEVER:
* Subnets **also** can control traffic permissions

## ACL Access Control Lists
When packets of data enter or exit a subnet boundary - it gets checked against an Network ACL - essentially a virtual firewall. This check determines if a packet has the permission to leave or enter the subnet 
* This is based on
  * Who it was sent from
  * How it is trying to communicate
 

 **By Default - NACLs allow all traffic in and out of the subnet**

You can white list and black list IPs - just because packets are let in - does NOT mean packets can be let out 

NOTE: ACL only control whether a packet can enter a subnet or not - NOT if the packet can go to say, a particular instance of EC2. This is where **Security Groups** come into play 

## Security Groups
Every EC2 instance when launched comes with its own security group - and
* By default - does not allow any traffic into the instance at all - all ports and IP addresses are blocked
* SGs can be modified to accept specific types of traffic e.g. https traffic but not os traffic

If NACLs are like passport control, SGs are like a doorman in a building - you can enter the subnet, but not everywhere in the subnet - its a finer control

Granularity goes Gateway (i/o of VPC) --> NACL (i/o of subnet) ---> SGs (i/o of resource/instance)

**BY DEFAULT - SGs all traffic is allowed out**

## Differences between SGs and NACLs
* Security Groups are STATEFUL
 * Any packet that left already and comes back will be remembered by the SG 
* NACLs are stateless - it remembers nothing
 * checks every packet each time that wants to cross 
 * Doesnt check the packet itself - just that the sender or receiver is on the approved list 
