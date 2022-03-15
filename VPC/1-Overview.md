# VPC:  

* A VPC is like a data center in the cloud 

* Connections to the VPC can be secured with VPN protocols. 

* Subnets can be created within the VPC and made private or public 

* Multiple VPCs can be interconnected with VPC peering 

* All AWS accounts start with a default VPC 

* Amazon recommends not deleting default VPC 

* Multiple additional VPCs can be created with subnets in each. 

## DHCP: 

* Dynamic Host Configuration Protocol 

* Every computer on a network has to have an I.P. address. 

* 2 ways that a computer can be assigned an I.P address. 

    - Static IP 

    - Dynamic IP 

* A Static IP is where a user a assigns an IP address manually. 

* All the IP addresss must be unique and should not be any conficts. 

* Dynamic IP , a computer gets an IP address from a DHCP server 

* A DHCP Server automatically assigns a computer an,  

    - IP address 

    - Subnet mask 

    - Default gateway 

    - DNS server 
  

* When in Internet options in computer is to set by Optain an IP address automatically.  The computer requests the DHCP server to get an IP address and DHCP Server provide and assign an IP for the computer. can be checked by ipconfig/all command in commandprompt. 

* DHCP server provide ip address based on the scope assigned to the DHCP (IP range). 

* The DHCP server assigns the IP address as  a lease. 

* A lease is the amount of time an IP address is assingned to a computer. 

* The lease is to help make sure the DHCP server does not run out of IP addresses. 

* Once ending the lease the computer requests the DHCP will requests the DHCP server to renew the IP address and DHCP server ackonwledge and renew it. 

* DHCP settings reserve the mapping of the IP address and devices (mac addresses). 
  
* DHCP options for the VPC are configured in DHCP option sets 

* The DNS domain name can be configured in the option set 

* DHCP will be used to provide dynamic addresses where required within the VPC. 

## Elastic IP addresses: (EIPs) 

  
* PUblic IP addresses from the VPC region 

* Permanantly allocated to your account until released 

* ACcount is charged until relese 

* Managing EIP is very important for cost saving 

* Network interfaces consume EIPs 

* EIPs can be moved between instances in the same region 

* VPC console => Elastic IPs => Allocate new address => 

* Public IP addresses, routable on the internet, are created via Elastic IP (EIP) addresses 

* EIPs results in account charges until they are released 

* Elastic Network Interfaces (ENIs) use the EIPs 

* Remember, wehn creating an EIP, it must be released to remove charges and it willnot be released automatically. 

## Elastic network interfaces (ENIs): 

* Virtual network interface attached to an instance 

* Only avaiable within a VPC 

* Associated with a subnet 

* Uses: 

    - Allows dual-homing 

    - One public addresses and multiple private addresses 

* Al Elastic network interface is a virtual network card or adapter attached to an AWS EC2 instance 

* Multiple ENIs connected to a single instances allows for dual-homing 

* Each ENI is associated with a subnet within the VPC just as a physical network interface would be associated with a subnet on a local network. 

 

 

 