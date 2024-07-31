# vpc-case-study
# Production Network:

1.Design and build a 4 tier architrcture

create vpc 4 tier

vpc-4tier-arch "10.0.0.0/16"

2.create 5 subnets out of  which 4 should be private and 1 should be public

create four private  subnets :

*app1 "10.0.128.0/20"

*app2 "10.0.144.0/20"

*db cache "10.0.176.0/20"

*db "10.0.160.0/20"

create one public subnets :

*web "10.0.0.0/20"

create internetgateways and attach to vpc-4tier-arch

create route attach route to public web subnet

3.launch instances in all subnets private and public app1,app2,dbcache,dband web

4.Allow dbcache instance and app1 subnet to send internet requests

5.Manage security groups and NACLs

#Development Network:
1.Design and build 2 tier architecture with two subnets named web and db

 create new vpc
 *vpc-2tier "10.1.0.0/16

 create subnets one should be public and another private

create web as a public subnet "10.1.0.0/20"

create db as a private subnet "10.1.16.0/20"

create internetgateway and attached to vpc-2tier

launch ec2 instance in both web and db subnets

create natgatway to websubnet and send internet request

3. Create peering connection between production network and development network










