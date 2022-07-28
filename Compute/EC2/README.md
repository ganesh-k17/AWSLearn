# EC2

* Elastic Compute Cloud (EC2) is Infrastructure as a Service.
* It mainly consists in the capability of:
    1. Renting virtual machines (EC2)
    2. Storing data on virtual drives (EBS)
    3. Distributing load across machines (ELB)
    4. Scaling the services using an auto-scaling group (ASG)

## EC2 sizing and configuration options

* OS - Linux, Windows or Mac OS
* How much compute power & cores (CPU)
* How much random-access memory (RAM)
* How much storage space:
    1. Network-attached (EBS & EFS)
    2. hardware (EC2 Instance Store)
* Network card: Speed of the card, Public IP address
* Firewall rules: security group
* Bootstrap script (configure at first launch): EC2 user data

## EC2 User Data

* It is possible to bootstrap our instances using an **EC2 User data** script.
* Bootstrapping means launching commands when a machine starts
* That script is **only run once** at the instance **first start**
* EC2 user data is used to automate boot tasks such as,
    1. Installing updates
    2. Installing software
    3. Downloading common files from the internet
    4. Anything you can think of
* The EC2 User Data Script runs with the root user (sudo user.)

## EC2 Instance types

* t2.micro (part of AWS free tier (upto 750 hours per month))
* t2.xlarge
* c5d.4xlarge
* r5.16xlarge
* m5.8xlarge
