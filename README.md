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

# VPC official documents in AWS 
https://docs.aws.amazon.com/vpc/latest/userguide/how-it-works.html \
https://learn.acloud.guru/course/certified-solutions-architect-associate/learn/e895e0dc-ee49-4a4e-9252-6018c96def38/2451d7b5-b7c5-4e72-960c-5e759c97dc23/watch \
VPC, subnet, route table, gateway(internet,...), NACL(network access list, block/allow specific IP addresses), security group \
1 Block IP address using NACL, not security group \
Please read https://learn.acloud.guru/course/certified-solutions-architect-associate/learn/e895e0dc-ee49-4a4e-9252-6018c96def38/2451d7b5-b7c5-4e72-960c-5e759c97dc23/watch, at 7:00. \
2 When create a VPC, create 3 components automatically: security group, route tables, NACL. \,
https://learn.acloud.guru/course/certified-solutions-architect-associate/learn/e895e0dc-ee49-4a4e-9252-6018c96def38/d33bb8d7-8a9d-4f15-baed-f5d5c69bf71d/watch, at 5:15. \
aws ec2 describe-vpcs
