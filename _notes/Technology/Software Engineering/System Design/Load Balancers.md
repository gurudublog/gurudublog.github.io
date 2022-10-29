---
title : Load Balancers
notetype : feed
date : 29-10-2022
---

AWS -> two types: Classic Load balancer, Application load balancer

CLB operates at layer 4 of OSI Model
ALB operates at layer 4 of OSI Model

#### subnets
#### vpc


- vpc can span across availability zones
- one subnet should be within a single availability zone
- private subnet and public subnet

![VPC](https://docs.aws.amazon.com/vpc/latest/userguide/images/vpc-diagram.png)


![VPC](https://docs.aws.amazon.com/vpc/latest/userguide/images/subnet-diagram.png)

??? 
- [x] subnets
- [ ] how data will send be sent back to client via LB - read http requests
- [x] how LB translates /getUsersData to ip address/getUsersData
	- [x] rules, targets and target groups
- [x] internal and internet-facing ALB
- [x] Auto scaling in load balancer or not - yes
- [ ] Network load balancer, clb





