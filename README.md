# Cloud-Security-with-AWS-IAM
Identity and Access Management is an AWS Service which authenticates [signed user] and authorized users  (has permissions) to which level of access in your AWS account for Users or User Group. 

IAM will restrict the usage of resouces if they dont have required permission.

#  JSON Policy
This JSON (JavaScript Object Notation) Policy is useful for granting access to the users. It plays a important role in giving least privilege principle what the user should have that much access it grants.

![Screenshot 2025-07-03 154416](https://github.com/user-attachments/assets/f4fea610-901b-4e3b-a44e-499397564f8b)

#  IAM Users and User Groups
**Users**
---
 IAM users are people or entities that can access or login to AWS account . These are for
 individual member they have certain set of required access to perform activities like getting access to use S3, EC2 Instances, Database, Network, Servers etc.

![IAM User](https://github.com/user-attachments/assets/3c950fd8-65a6-437f-896c-25c0fb075481)

 
 
 **User Groups**
 ---
 IAM user groups are set of permissions for IAM Users where every user have same
 type of access level. IAM is a folder in which it contain users to get access resouces
 permissions instead of applying individual User.
 
 I attached the policy I created to this user group, which means any user inside this
 user group will automatically get permissions attached to DevEnvironment Policy
 ---
# User Group Tags
 Tags are tools that use for labelling our resources . They are used for grouping
 resources, cost allocation and applying policies for all resources with the same tag.
 
 The tag i had used on my EC2 instances is called Env which is "Envionment". The
 value i have assigned for my instances are "production" and "development"


 ![Tags of user group](https://github.com/user-attachments/assets/566c9ba5-c585-416b-9015-4b9b26736a67)

# Testing IAM Policies
I tested my JSON IAM policy by stopping the development and production
 environment.
 
# Stopping the production instance
 When I tried to stop the production instance it denies and we get an error. This is
 because our production is outside of the scope of permission policy which is "Dev
 Environment"only can launch EC2 and cannot delete or create resources of
 production

 ![Testing IAM policy for stopping production ](https://github.com/user-attachments/assets/5f06e1e3-e4d0-490e-8018-124977658032)

 #  Stopping the development instance
 when I tried to stop the development instance i had successfully stop the
 instance state. This was because policy allows the dev environment to stop insatnce.
 
 ![Testing stop of development instance](https://github.com/user-attachments/assets/5ea7159c-5a13-4d47-8e06-877c43de23cd)



