# Cloud Overview - Regions
Lke GCP, AWS is split into regions - e.g. us-east-1, eu-west-3 - each number is an 

* However, a lot of services are region scoped - not all services are available in all regions
  * When starting a service in a new its like a new instance / setup
* Choosing a region depends on your app and uses:
  * Compliance of data and legal requirements
  * Latency 
  * Available services within a region - especially new services
  * Pricing

## Availability Zones
* Each region is split into zones - 2-6 e.g.
  * ap-southeast-2a
  * ap-southeast-2b
* Each AZ is one or more discrete data centers with redundant power networking and connectivity
  * Separate from each other

You can have a look at global infrastructure to see the lists of services by region and their availability