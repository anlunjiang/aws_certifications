# User permissions and Access

When you create an account in AWS - you are given the ROOT user - this is the owner of the aws account - it can do 
anything it wants 

THis is too powerful and is recommneded to:
* turn on MFA 
* use different users specific to what they need

# IAM
You can create IAM users - **by default it has no permissions** it cant even login to the AWS account 
It has to be given permission to do anything - and only the things IT NEEDS TO DO

THis is the **least privileged principle** 

You grant or deny permission using IAM Policies attached to an IAM user - many to one is usual and recommended. 
IAM Policies are JSON documents that describe what API calls the user can or cannot make e.g.

```json
{
  "Version": "2012-10-17",
  "Statement": {
    "Effect": "Allow",
    "Action": "s3:ListBucket",
    "Resource": "arn..."
  }
}
```

A user with this policy can be allowed to view the bucket specified - but nothing else. Effect has two options only
* Allow
* Deny

Action can list ANY AWS API call

## IAM Groups
Users can be organised into IAM Groups - and you can then attach a policy to a group - so all users in the group receive
the same policy 

## Roles
Roles have specific permissions that allow or deny actions - and can be assumed for temporary amounts of time by a user
A user's day to day can change and vary so might need different sets of permissions at different times, at this point
they can assume the role needed with the permissions.

When a role is assumed - all previous permissions are abandoned 

**You can actually just not use IAM users, and federate developers into your account via roles using corporate credentials 
THere will be a mapping of their corporate identities with the IAM Role.**

AWS also recommends creating an IAM user for each person as well if the above is not possible

# Best practice:
Do not use the root user for everyday tasks.
Instead, use the root user to create your first IAM user and assign it permissions to create other users.

Then, continue to create other IAM users, and access those identities for performing regular tasks throughout AWS.
Only use the root user when you need to perform a limited number of tasks that are only available to the root user.
Examples of these tasks include changing your root user email address and changing your AWS support plan.
