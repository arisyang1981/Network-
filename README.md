# Network and AWS network 

# SSL vs TLS
https://www.ssl2buy.com/wiki/ssl-vs-tls \
https://www.youtube.com/watch?v=J7fI_jH7L84 \
They are almost the same, but TLS is more secure, and updated. Use TLS if possible.

# Network CIDR block 
https://whatismyipaddress.com/cidr \
https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation \
#Internet CIDR visular \ 
https://cidr.xyz/

# AWS network 
https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/5hCsp/reading-2-5-networking-on-aws
https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/qjatI/reading-2-6-introduction-to-amazon-vpc 

# VPC
https://docs.aws.amazon.com/vpc/latest/userguide/how-it-works.html \
https://learn.acloud.guru/course/certified-solutions-architect-associate/learn/e895e0dc-ee49-4a4e-9252-6018c96def38/2451d7b5-b7c5-4e72-960c-5e759c97dc23/watch \
VPC, subnet, route table, gateway(internet,...), NACL(network access list, block/allow specific IP addresses), security group \
1 Block IP address using NACL, not security group \
Please read https://learn.acloud.guru/course/certified-solutions-architect-associate/learn/e895e0dc-ee49-4a4e-9252-6018c96def38/2451d7b5-b7c5-4e72-960c-5e759c97dc23/watch, at 7:00. \
2 When create a VPC, create 3 components automatically: security group, route tables, NACL. \
https://learn.acloud.guru/course/certified-solutions-architect-associate/learn/e895e0dc-ee49-4a4e-9252-6018c96def38/d33bb8d7-8a9d-4f15-baed-f5d5c69bf71d/watch, at 5:10. \
3 CIDR range, 16 to 28, means the count of IP range is 65536 to 16.\
4 IP v4 vs IP V6. https://docs.aws.amazon.com/vpc/latest/userguide/how-it-works.html \
5 Internet gateway \
https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html \
An internet gateway enables resources in your public subnets (such as EC2 instances) to connect to the internet.
Attach the internet gateway to VPC, and edit non-default route, add internet gateway into route, allow the route can access the internet.
# Subnet 
1 One subnet is always in one AZ, can't span AZs. \
2 Available IP range for subnet, 10.0.1.0/24, allocates 256 IP addresses, but 251 available IP ranges for business, between 4 and 254, other 5 are reserved. \
https://learn.acloud.guru/course/certified-solutions-architect-associate/learn/e895e0dc-ee49-4a4e-9252-6018c96def38/d33bb8d7-8a9d-4f15-baed-f5d5c69bf71d/watch, 7:35. \
https://cidr.xyz/ \ 
https://docs.aws.amazon.com/vpc/latest/userguide/configure-subnets.html#subnet-sizing \
10.0.0.0: Network address. \
10.0.0.1: Reserved by AWS for the VPC router. \
10.0.0.2: Reserved by AWS. The IP address of the DNS server is the base of the VPC network range plus two. For VPCs with multiple CIDR blocks, the IP address of the DNS server is located in the primary CIDR. We also reserve the base of each subnet range plus two for all CIDR blocks in the VPC. For more information, see Amazon DNS server. \
10.0.0.3: Reserved by AWS for future use. \
10.0.0.255: Network broadcast address. We do not support broadcast in a VPC, therefore we reserve this address. \
3 In defualt, private subnet can't access the public internet. But NAT serice can allow private subnet to acccess the internet, but the internet can't access private subnet. https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html \ 
4 Subnet has two componets: route table, and network ACL, can change after create subnet.
# Subnet: route table, NACL vs security group
https://docs.aws.amazon.com/vpc/latest/userguide/configure-subnets.html \
Route table, which specifies the allowed routes for outbound traffic leaving the subnet. Outbound, subnet can access what. Control what IP/DNS can be accessed. \
Network ACLs control inbound and outbound traffic for your subnets. NACL has the ability to block IP, security groups hasn't. Inbound and outbound, subnet can be accessed by what\
Security groups control inbound and outbound traffic for your instances. Inbound and outbound, instance can be accessed by what. Control network protocol, port.\
aws ec2 describe-vpcs
