# Amazon Elastic File System (EFS)

* Create and configure shared file systems simply and quickly for AWs compute services. (no provisioning, deploying, patching or maintenance required.)

* Scale your file system automatically as files are added, removed and burst to highter throughput levels.

* Pay only for the storage you use and reduce consts up to 92 percent by automatically moving infrequently accessed files.

* Securely and reliably access your files with a fully managed file system designed for 99.9999999 percent durabilty and upto 99.99 percent of availability.

* https://aws.amazon.com/efs/

## Steps to create:

Create EFS => Mount on EC2/ECS/EKS/Fargate/Lambda => Test and optimize => Move data to file systme from cloud or other data sources => Share and further protece file data with AWS backup and EFS replication.

## General

* Shareable
* Hierarchical
* Can be accessed through NFSv4
	- but EBS volumes are dedicated to an instance
	- EBS is bound to an instance, EFS is free to be accessed by many different instances.
	- EC2 instances can use EFS shares
* EFS is not supported on windows instances, windons instancces cannot share directly EFS files but unix instances.

## Features:

    - EFS is like NAS storage within the cloud for the cloud.
	- EFS can be accessed through the NFSv4 protocol.
	- EC2 instances can connect to EFS shares, but it is not supported on windows instances.