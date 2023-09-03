# Messaging and Queueing

Apps send messages to each other to communicate
* Tightly coupled architecture - has apps communicating directly with each other - if a single component fails - the
chain fails
* Loosely couple architecture can use queues to make sure a single failure in a component doesnt cascade. The queue
acts as a buffer

## SQS and SNS


SQS - Simple Queue System
* Send, store, receive messages between components at any volume
* Each message has a payload
* This is a managed service by AWS - the infra is provisioned and scaled for you and is reliable

SNS - Simple Notification System
* Send messages to end users - using a PubSub Model. Just create an SNS Topic which clients are subscribed to
* These subscribers dont have to be end users, can be sqs queues - lambdas, https webhooks
* Can do email and text messages too

# Additional Compute Services 
EC2 requires you setup and manage your instances over time - you can responsible for security, patches, scaling etc

Serverless - You cannot access or see the underlying infra of a service - AWS will provision, scale and maintain the 
infra for you  

## Lambda

Your code will be uploaded to a lambda function - you just need to **configure a trigger**. THe code is then run in 
a managed environment. 

Even if you have 1 or 1000 triggers - lambda will scale your function to meet demand. Designed to run code under 15 min
NOT for long running processes. More for a web backend or handling requests 

## ECS and EKS

If you need access to the underlying env - but want efficiency and portability. These are container orchestration tools
Containers will run on EC2 instances - and run in isolation from each other 

Fargate is the serverless option for ECS and EKS


# Summary

EC2 - Traditional apps with full access to OS
Lambda - Short running functions, service oriented apps or event driven - no management of infra
ECS/EKS - Container based workloads
    * Fargate - serverless
    * EC2 - managed by you

