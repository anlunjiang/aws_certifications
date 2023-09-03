# Networking

Virtual Private Clouds (VPCs) provisions a logically isolated section of the AWS Cloud where you launch resources in a 
virtual network you define - It is **your own private network in AWS** can define your own private ip range

These resources can be public facing or private (no internet access). In the coffee shop analogy, the cashier will 
be in the public subnet, and db in the private. 

ELBs EC2 resources etc can live all inside a VPC.

## Subnets
Subnets live in VPCs - and they are chunks of ip addresses in your VPC that allow you to group your resources together. 
Along with networking rules control whether resources are publically or privately available 


## Internet GW 
In order for traffic to flow at all IN OR OUT of your VPC - You need to attach an **INTERNET GATEWAY** to your VPC. 
Like a doorway to the internet. 
* If a VPC doesnt have a IGW - then no-one can reach it 

## Virtual Private Gateway
Private GW only allows in traffic from an approved network - not the public internet.
* It allows you to create a VPN connection between a private network (on prem) to your VPC. 
* Coffee analogy. Like a private route to the shop which authenticates you first

## AWS Direct Connect
This VPN connection however - still uses the regular connection with shared bandwidth - so can be slowed down.
If you want fibre, private, low latency, dedicated and unshared connection - you can use **AWS Direct Connect**

This is straight from your data center to AWS. This is a physical line installed by AWS.

The private connection that AWS Direct Connect provides helps you to reduce network costs
and increase the amount of bandwidth that can travel through your network.


Note that VPC can have multiple gateways attached for multiple resources - just in different subnets 
