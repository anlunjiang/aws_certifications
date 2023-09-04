# Global Networking - Route 53
AWS DNS or Domain Name Service - Highly available and Scalable 
It gives developers and businesses a reliable way to route end users to internet applications hosted in AWS. 

* DNS translates website names to ip addresses both in aws (ec2, elb) and outside
* Can transfer existing domains as well from other registrars
* You can even use it to register new domain names - can purchase and manage - like cloudflare 

It can use several different routing policies:
* Latency based routing
* Geolocation DNS
  * Direct traffic based on where the customer is located 
* Geoproximity
* Weighted Round Robin

Cloudfront CDN using Edge locations is an example of speeding up user experience by location - geolocation dns - say to deliver static web assets around the world
