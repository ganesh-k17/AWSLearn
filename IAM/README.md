# IAM

Identity and Access Management, Global service

## Users and Groups

* Root account created by default, shouldn't be used or shared
* Users are people within your organization,  and can be grouped.
* Groups only contain users not other groups
* Users don't need to have to belong to a group and user can belong to multiple groups.

## Permissions

* Users or Groups can be assigned JSON documents called policies. (Sample in IAM-Policy_Permission-sample-template.json)
* These policies define the permissions of the users
* In AWS you apply the least privilege principle: don't give more permissions than a user needs.

## IAM Policy structure

* Consists of
    * Version: policy language version always include "2012-10-17"
    * Id: and identifier for the policy (optional)
    * Statement: one or more individual statements (required)

* Statements consists of,
    * Sid: and identifier for the statements (optional)
    * Effect: whether the statement allows or denies access (Allow, Deny)
    * Principal: account/user.role to which this policy applied to
    * Action: list of actions this policy allows or denies
    * Resource: list of resources to which the actions applied to.
    * Condition: conditions for when this policy is in effect.

    ```json
    {
    "Version" : "2012-10-17",
    "Id": "S3-Account-Permissions",
    "Statement" : [       
        {
            "Sid": "1",
            "Effect": "Allow",
            "Principal": {
                "AWS":["arn:aws:iam::1234567:root"]
            },
            "Action": [
                "cloudwatch:ListMetrics",
                "cloudwatch:GetMetricStatistics",
                "cloudwatch:Describe*"
            ],
            "Resource": ["arn:aws:s3:::mybucket/*"]
        }
    ]
    }
    ```

## Password policy

* Strong passwords = higher security for the account
* In AWs below password policy can be setup,
    - Set a minimum password length
    - Require specific character types:
        - includeing uppercase letters
        - lowercase letters
        - numbers
        - non-alphanumeric characters
    - Allow all IAM users to change their own passwords
    - Require users to change their password after some time (password expiration)
    - Prevent password re-use

## Multi Factor Authentication (MFA)

* Account => My credentials
* Users have access toyhour account and can possibly change configurations or delete resources in yhour AWS Account
* You want to protect atleast the root accounts and IAM users as well as.
* MFA = password + security device you own.
* Benefit:  if a password is stolen or hacked, the account is not compromised.
* MFA options:
    - Virtual MFA device (eg: google authenticator)
    - Universal 2nd Factor (U2F) security Key (thrid party device)
    - Hardware Key Fob MFA device (third party device)

## How can users access AWS

* AWS Management Console (protected by password + MFA)
* AWS Command Line Interface (CLI) : protected by Accesskeys
* AWS Software Developer Kit (SDK) - for code: protected by access keys.
* Users manage their own access keys.
* Access keys are secret, just like a password. Dont share them. (or dont expose in public github repositories.)
* Access Key Id ~= username, Secret Access Key ~= password
* CLI - tool that enables you to interact with AWS services using commands in commandline shell. Alternative to AWS Console.
* SDK - Language specific APIS which also enables you to access and manage AWS servics. suupports many different languages like python, c#, golang.

## IAM Roles for Services:

* Some AWS service will need to perform actions on your behalf.
* Tod so, We will assign permissions to AWS services with IAM roles.
* Common roles:
    - EC2 instance Roles
    - Lambda function Roles
    - Roles for cloudformations
* AWS Console -> IAM -> Roles -> Attach permissions

## IAM Security Tools

* IAM Credentials Report (account-level)
    - a report that lists all your account's users and the status of their various credentials.
    - AWS Console -> IAM -> Credential Reports.
* IAM Access Advisor (user-level)
    - Access advisor shows the service permissions granted to a user and when those services were last accessed.
    - AWS Console -> IAM -> Users -> select users -> select tab Access Advisor

## IAM Guidelines and Best Practices

* Dont use the root account except for AWS account setup
* One phyisical user = One AWS user
* Assign users to groups and assign permissions to groups
* Create a strong password policy
* Use and enforce the user of MFA
* Create and use Roles for giving permissions to AWS services.
* Use Access Keys for programmatic access (CLI/SDK)
* Audit permissions of your account with the IAM Credentials Report.
*  Never share IAM users & Access keys.

## Summary

* Users: mapped to a physical user, has a password for AWS Console.
* Groups: contains users only
* POlicies: JSON document that outlines permissions for users or groups.
* Roles: for EC2 instances or AWS services
* Security: MFA + Password policy
* Access Keys: Access AWS using the CLI or SDK
* Audit: IAM Credential Reports & IAM Access Advisor
