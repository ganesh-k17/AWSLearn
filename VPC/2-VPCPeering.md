# VPC Peering

* Connects one VPC to another
* Many possible scenarios, 
    - Management VPC > Production VPC
    - Devlopment VPC > Prodcution VPC
    - Corporate VPC > Partner VPC
    - VPC peering is not trasitive
        - VPC1 peered with VPC2 and VPC2 peered with VPC3 doesn't mean VPC1 peered with VPC3.  If VPC1 and VPC3 wants to communicate they both should be peered.
* Creating VPC peers:
    - Initiating VPC sends a request to the receiving VPC
    - Receiving VPC accespts the request
    - Owner role required for both sending and receiving.
    - IP CIDR blocks in each VPC must not overlap
    - Each VPC needs a defined route to the other VPC
        - May require routing table modifications
    - Security group rules
        - May require modification for the VPC peers

## VPC peering Lab



