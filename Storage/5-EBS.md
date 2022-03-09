# Elastic Block Storage:

* Used for durable (persistent) storage with EC2 instances
* Block level storage from one AWS service to another

## EBS Volume types

* Magnetic (slowest and cheapest)
* SSD (Solid state drive) (fast and )
    - General purpose (low IOPS)
    - Provisioned IOPS
        - PIOPS (provisioned input/output operations per second) (provisioned IOPS)
    - EBS Optimised instance should be used. (for best performance SSD)

## Protecting EBS data

* Snapshots (save it and use it later with exact same configurations)
* Volume recorvery (Attaching volumes from one instacne to another)
* Encryption methods
