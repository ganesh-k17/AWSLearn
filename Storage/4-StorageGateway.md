# Tape Gateway:

* Storage Gateway -> Tape gateway
* Backup our data to Amazon S3 and archive in Amazon Glacier using our existing type-based processes.
* Tape gateway reduces the burder and cost of tape backup
* Backup data as virtual tapes to AWS
* Tape Gateway moves tape backups to the cloud.
* local tapes to Archives in S3 Glacier or S3 Glacier Deep Archive using Amazon S3 Tape Library
* Tapes replicated across 3 availability zones with 11 9s of durability
* Automatic error checking whether data is available by amazon
* Encryption and reduced security risk
* No more broken tapes and no worry to get wrong data
* Save money on Backups
* 1$ per month for 1 GB and 12$ per year for 1 TB of data  to store

## Quick Review:

* Tape Gateway can be used with systems that only allow for backing up tapes.
* 3 types of storage gateways => file, volume, and tape
* Tape gateway can be configured as public or VPC
* A virtual Tape Library (VTL) is a library of backup "tapes" that are actually just objects stored in an S3 bucket.

## Lab:

Storage Gateway => TapeGateway => Select host Platform => 


