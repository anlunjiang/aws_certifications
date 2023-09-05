# Introduction - Monitoring and Analytics

Monitoring - observing systems, collecting metrics, and then using data to make decisions

# Cloudwatch
Enables you to monitor and manage various metrics and configure alarm actions based on data from those metrics.

CloudWatch uses metrics to represent the data points for your resources.
AWS services send metrics to CloudWatch. CloudWatch then uses these metrics to create graphs automatically 
that show how performance has changed over time. 

e.g. EKS monitor graphs - this is part of cloud watch ! 

We can create metrics and alert when this metric's trigger is hit - e.g. ec2 cpu usage 
This is called a **Cloudwatch Alarm** - integrated with SNS for alerting 

## Dashboard feature
to aggregate these metrics to a single pane 

* Access to all your metrics from central location
* Visibility across apps, infra and services - gaining insights 

Reduces/improves
* MTTR - mean time to resolution 
* TCO - total cost of ownership

# Cloud Trail

Records API calls for your account. 
The recorded information includes the identity of the API caller, the time of the API call, 
the source IP address of the API caller, and more. 

You can think of CloudTrail as a “trail” of breadcrumbs (or a log of actions) that someone has left behind them.

Secure API logs indefinitely in S3 - Vault Lock can prevent them from deletion or edits
* Events are typically updated in CloudTrail within 15 minutes after an API call.

## Cloudtrail insights
Optional feature that allows cloudtrail to auto detect unusual api activities in your aws account
e.g. high number of ec2 launched in short space of time 