## Outcome
The outcome of this project is to deploy a scalable ,highly available and secure application on 3-tier application access to the internet to users from public internet.

## Pre-Requisites
- Create a free Tier AWS account at https://portal.aws.amazon.com/gp/aws/developer/registration/index.html?nc2=h_ct&src=header_signup&refid=99f831a2-d162-429a-9a77-a89f6b3bd6cd

- An IDE or text editor of your choice

## Overview
![Architecture diagram](https://miro.medium.com/v2/resize:fit:1400/1*9YQ9JIRKpsKj02PQA02ubw.png)


## Steps
- Log in to AWS management console
- Navigate to VPC and create one
- Enable host name on the "Actions" tab
- Edit VPC settings ,scroll down and enable DNS hostnames if its not checked and save
- Navigate to Internet gateways on the VPC tab,create VPC only,give it a name and give it an IPv4 address set it to 10.0.0.0/16 and tenacy is default
- Select in the VPC created ,and scroll the dropdown to edit VPC settings and enable DNS hostnames
- Create internet geteway and attach to VPC created
- Navigate to subnet ,we need 9 subnets,3 each for every tier(web,application and data tier)
- Select availabilty zone i go with us-east-1a and IPV4 is 10.0.0.0/24 and create another subnet below it while following naming conventions and select availability zone and the same for the third subnet
- Repeat the process upto 9 subnets and auto enable the public subnet
- Navigate to route table and create a public route table