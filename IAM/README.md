# IAM

Identity and Access Management, Global service

## Users and Groups:

* Root account created by default, shouldn't be used or shared
* Users are people within your organization,  and can be grouped.
* Groups only contain users not other groups
* Users don't need to have to belong to a group and user can belog to multiple groups.

## Permissions

* Users or Groups can be assigned JSON documents called policies. (Sample in IAM-Policuy_Permission-sample-template.json)
* These policies define the permissions of the users
* In AWS you apply the least privilege principle: don't give more permissions than a user needs.