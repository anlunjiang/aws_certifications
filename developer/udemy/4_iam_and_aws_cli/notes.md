# IAM - Users and Groups
Identity and Access Management

* In AWS you first create a root account - this shouldnt be used or shared
  * Instead you should create IAM users within your org and they can be grouped
    * Good for say grouping by function and teams
    * Each will have their own permissions that can be assigned via **JSON policies**
    * Like in most cloud practices use the principle of the least privilege needed.
* IAM users can have tags that define their role - metadata essentially


## IAM Policies Structure
* Policy JSON Structure:
  * Version: poloicy language version usually 2012-10-17
  * ID: and identifier for the policy
  * statement: one or more individual statements
    * Each consists of
      * SID: identifier for the statement
      * Effect: allow or deny access
      * Principle: account/user/role applied to
      * Action: lists of actions this policy allows or denies
      * Resources: list of resources to which the actions are applied to
      * Condition: conditions for when this policy should be applied
e.g.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow", 
      "Action": "ec2:Describe*", 
      "Resource": "*"
    }, 
    {
      "Effect": "Allow", 
      "Action": "elasticloadbalancing:Describe*", 
      "Resource": "*"
    }, 
    {
      "Effect": "Allow", 
      "Action": [
        "cloudwatch:ListMetrics", 
        "cloudwatch:GetMetricStatistics", 
        "cloudwatch:Describe*"
      ], 
      "Resource": "*"
    }
  ]
}
```

## IAM MFA & password policies

IN AWS you can setup a password policy where there are
* minimum password lengths
* requires specific character types
  * uppercase, numbers, non-alphanumeric etc
* Allow all IAM users to change their own passwords
* Password expiration
* no password reuse

There is also **MFA - multi factor authentication** - good to use on root accounts
