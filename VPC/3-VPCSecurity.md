# Security Group:

* Security groups are not for user management in AWS
* Security groups work like a firewall assigned to an EC2 instance
* Traffic flows can be defined for inbound traffic (ingress) and outbound traffic (egress)
* Security groups are applied at the instance level and not that subnet level

* Acts like a firewall
	- Assigned to an instance in a VPC
	- Applied to instances not to subnets
* Defines allowed traffic flows
	- Ingress (entrance)
	- Egress (exit)
* Supports only allow rules - deny is implicit (closed means not allowed)
* Stateful processing is used.

# Network access controls lists (NACLs)

* Applied on subnets
* Stateless processing
* Supports both allow and deny rules. 
* Rule number defines precedence
* Lowest numbered rules first
* First match applies

# NAT: (Network Address Translation)

* is used to interconnect Point private networks and public networks
* An Elastic IP (EIP)  is associated with the NAT instance for the public-facing side.
* Instances in the private subnet of the VPC use the NAT to connect to the internet
* NAT can be implemented using a ddicated NAT instance or using an AWS NAT Gateway

# Gateways

* AWS supports gateways to connect to the VPC from the local networks
* Gateways are effectively VPN endpoints.

* VPG (Virtual Private Gateway) - is implemented in the Cloud
* CGW (Customer Gateway) - is implemented in the customer network

# VPG (Virtual Private Gateway)

* Connects local network to the VPC
* VPG is the VPN concntrator

# CGW: (Customer Gateway)

* Physical device or software application.
* Anchor on the customer side
	- Connects to the VPG

# Alternative connections

* AWS hardware VPN
* AWS Direct Connect
* VPN CloudHub
* Software VPN (L2TP - Layer 2 Tunneling Protocol, ipSec)

# VPN configuration options

* Split-tunnel gives flexibility for ruouting traffic aross the Virtual Private Network (VPN), specifically for traffic going directly out to the Internet
* AWS has now enabled certificates for authentication to the VPN
* Direct Connect bypasses traditional Internet Service Provider (ISP) Internet connection and connects straight into AWS.
