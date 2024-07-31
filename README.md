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

![WhatsApp Image 2024-08-01 at 00 54 04](https://github.com/user-attachments/assets/6d20a0be-6350-45f4-9daf-83cb2e85109f)

create internetgateways and attach to vpc-4tier-arch

![WhatsApp Image 2024-08-01 at 01 01 48](https://github.com/user-attachments/assets/021a797e-c286-4aab-b703-c18212a5904b)

create route attach route to public web subnet

![WhatsApp Image 2024-08-01 at 00 55 46](https://github.com/user-attachments/assets/a45de047-ba64-463a-b3c1-0d4131d22f8e)

3.launch instances in all subnets private and public app1,app2,dbcache,dband web

![WhatsApp Image 2024-08-01 at 01 06 49](https://github.com/user-attachments/assets/72dfadb9-f671-4b33-a9f1-234cfec35f62)


4.Allow dbcache instance and app1 subnet to send internet requests
create nat gateways and add to internet requests app1 and dbcache

![WhatsApp Image 2024-08-01 at 01 16 07](https://github.com/user-attachments/assets/ec56a706-2660-407a-b784-bc8990465723)


5.Manage security groups and NACLs

![WhatsApp Image 2024-08-01 at 00 47 55](https://github.com/user-attachments/assets/61243df8-ea69-498a-a415-0c787cbadf7b)

![WhatsApp Image 2024-08-01 at 00 51 46](https://github.com/user-attachments/assets/8f30f24f-cbc7-429e-b643-8f5201a49864)

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

 ![WhatsApp Image 2024-08-01 at 01 11 31](https://github.com/user-attachments/assets/db7f2b45-ed0a-4d99-8900-5b460d907c87)










