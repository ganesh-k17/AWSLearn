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
