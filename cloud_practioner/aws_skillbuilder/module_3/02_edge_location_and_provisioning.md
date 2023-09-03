# Edge Locations

What if you have customers all over the world - what region do you pick? You can use an edge location - Edge location
is an example of a CDN - **CONTENT DELVIERY NETWORKS** in AWS this is called Cloudfront

Amazon Cloudfront CDN uses Edge locations, which are sites that use to store copies fo your data closer to customer for faster
delivery. Data can video, apps apis etc anything - with low latency delivery.

* Edge locations are separate from REGIONS. Can push content from inside region to a collcection of edge locations across the world 
* Edge location arent limited to Cloudfront - Route53 for DNS is also possible 

## AWS Outposts
For customers who want to use AWS services inside their own building. AWS will install a fully operationl mini region inside
your OWN data center. **This is owned and operated by AWS** but isolated in your own building

# Provisioning AWS Resources 
In AWS everything is an API - there are different ways to interact with the APIs
* AWS Management Console 
  * Good for test envs - viewing bills and monitoring 
* AWS CLI 
  * Better for prod as it avoids human error
* AWS SDK 
  * E.g. for python Boto3
* Other tools like AWS Cloud Formation for creating requests to manage infra and resources

# Beanstalk and Cloud Formation 

## Beanstalk
A service to provision EC2 based environments. 
* Given application code and desited end config - beanstalk will build your env for you. You can save your env cfg
  * Can be redeployed easily 

You can adjust capacity, load balance, scale and monitor

## Cloud Formation 
IaaC tool like Terraform - you can use JSON or YAML to create cloud formation templates.
Like terraform this is declarative in format - then AWS will figure out how to provision.

* CF, unlike beanstalk isnt limited to just EC2 deployments - storage, dbs, ML etc all can be deployed.
  * All resources will be deployed in parallel - It will call AWS backend APIs for you to create the specified infra 
* Can run the same templates across regions or AZs and the environments created will be identical 