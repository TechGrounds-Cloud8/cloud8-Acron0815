# VPC

The best of both worlds: 

A Virtual Private Cloud (VPC) offers me the flexibility and cost-effectiveness of the public cloud together with the security of a private cloud. With the Amazon Cloud, setting it up is a basic requirement as a basic security measure for the use of almost all cloud resources. Each user receives at least one VPC.

A VPC lets me build my own private environment on top of a shared, public cloud infrastructure. This gives me an area isolated from everyone else using the public cloud—a private, secure space for data.

![VPC](../00_includes/AWS-10%20VPC/VPC-1.PNG)

Each Amazon account comes with a default VPC that is pre-configured for you to start using immediately. A VPC can span multiple availability zones in a region. This is a diagram of a default VPC:

![VPC Diagram](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/VPC.PNG)



---

## Key terminology (a few)

- Virtual Private Cloud compared to a Private Cloud

A virtual private cloud is an alternative to the private cloud. It offers an environment within a public cloud that is strictly separated from other users' areas. For example, imagine the infrastructure of a cloud provider as a restaurant with tables. In a public cloud, users share resources - that is, they take a seat at the free tables. A virtual private cloud is like a reserved table where only certain guests are allowed to sit.

A virtual private cloud from Amazon AWS offers a number of advantages over a self-operated and managed private cloud.

Agility: 

I can adjust the size of my virtual network to my needs at any time and dynamically scale the resources used.

Availability: 

With redundant resources and highly fault-tolerant architectures, Amazon AWS can ensure availability for applications and workloads that most individuals or organizations cannot match.

Affordability: 

VPC customers can take advantage of the cost efficiencies of a public cloud, such as savings in hardware costs.

- Subnet - A range of IP addresses in my VPC.

- Network ACL's - This optional security feature for my VPC, acts as a firewall and
checks the incoming and outgoing traffic on my subnet.

- Internet gateway - A gateway that I attach to my VPC to enable communication between
resources in my VPC and the internet.

- Security Groups - Act as a virtual firewall to block inbound and outbound traffic
for an AWS resource, such as an EC2 instance. Each VPC has one
Default security group and you can create additional security groups. One
Security group can only be used in the VPC for which it is created.
---

 - VPC management is typically done through my provider's (e.g. Amazon AWS) control panel . 
 
 
   This access to my VPC allows me to easily make and track changes as needed.

 ---

## Exercise 1

- Allocate an Elastic IP address to your account.

- Use the Launch VPC Wizard option to create a new VPC with the following requirements:

  Region: Frankfurt (eu-central-1)

  VPC with a public and a private subnet

  Name: Lab VPC

  CIDR: 10.0.0.0/16

- Requirements for the public subnet:
  Name: Public subnet 1

  CIDR: 10.0.0.0/24

  AZ: eu-central-1a

- Requirements for the private subnet:

  Name: Private subnet 1

  CIDR: 10.0.1.0/24

  AZ: eu-central-1a

  ---


### I Allocate an Elastic IP address to my account.

![Allocate Elastic IP](../00_includes/AWS-10%20VPC/Elastic-ip.PNG)

### I Use the Launch VPC Wizard option to create a new VPC.

![Create a new VPC](../00_includes/AWS-10%20VPC/Exc.-1-1.PNG)

![Create a new VPC](../00_includes/AWS-10%20VPC/Exc.-1-2.PNG)

---

## Exercise 2

- Create an additional public subnet without using the wizard with the following requirements:

 VPC: Lab VPC

 Name: Public Subnet 2

 AZ: eu-central-1b

 CIDR: 10.0.2.0/24

- Create an additional private subnet without using the wizard with the following requirements:

VPC: Lab VPC

Name: Private Subnet 2

AZ: eu-central-1b

CIDR: 10.0.3.0/24

- 1.View the main route table for Lab VPC. It should have an entry for the NAT gateway. Rename this route table to Private Route Table.

- Explicitly associate the private route 
table with your two private subnets.

- 2.View the other route table for Lab VPC. It should have an entry for the internet gateway. Rename this route table to Public Route Table.

- Explicitly associate the public route table to your two public subnets.


### I Create an additional Public Subnet without using the wizard.

![Create Public Subnet](../00_includes/AWS-10%20VPC/Exc.-2-1-Create-Public-Sub2.PNG)

### I Create an additional Private Subnet without using the wizard.

![Create Private Subnet](../00_includes/AWS-10%20VPC/Exc.-2-1-Create-Private-Sub2.PNG)

### I Create an additional Public / Private Subnet without using the wizard.

![Create Public/Private Subnet](../00_includes/AWS-10%20VPC/Exc.-2-1-Create-Public-en-Private-Sub2.PNG)

### 1.View the main route table for Lab VPC.

![2.3.-view-1](../00_includes/AWS-10%20VPC/Exc.-2-3-View1.PNG)

### 2.View the other route table for Lab VPC.

![2.4.-view-1](../00_includes/AWS-10%20VPC/Exc.-2-4-View1.PNG)

---

## Exercise 3

- Create a Security Group with the following requirements:

Name: Web SG

Description: Enable HTTP Access

VPC: Lab VPC

Inbound rule: allow HTTP access from anywhere

Outbound rule: Allow all traffic

### 1.1 Create a Security Group

![1.1 Create a Security Group](../00_includes/AWS-10%20VPC/Exc.-3-1-Creating-Security-Group.PNG)


### 1.2 Create a Security Group (Inbound)

![Create a Security Group (Inbound)](../00_includes/AWS-10%20VPC/Exc.-3-1-Creating-Security-Group-In.PNG)

### 1.3 Create a Security Group (Outbound)

![Create a Security Group (Outbound)](../00_includes/AWS-10%20VPC/Exc.-3-1-Creating-Security-Group-Out.PNG)

---

## Exercise 4

- Launch an EC2 instance with the following requirements:

AMI: Amazon Linux 2

Type: t3.micro

Subnet: Public subnet 2

Auto-assign Public IP: Enable

User data:
#!/bin/bash
#Install Apache Web Server and PHP
yum install -y httpd mysql php
#Download Lab files
wget https://aws-tc-largeobjects.s3.amazonaws.com/CUR-TF-100-RESTRT-1/80-lab-vpc-web-server/lab-app.zip
unzip lab-app.zip -d /var/www/html/
#Turn on web server
chkconfig httpd on
service httpd start

Tag:
Key: Name
Value: Web server

Security Group: Web SG

Key pair: no key pair

- Connect to your server using the public IPv4 DNS name.

---

Exercise 4.0

![Exercise 4.0](../00_includes/AWS-10%20VPC/Exc.-4.0.PNG)


Exercise 4.1

![Exercise 4.1](../00_includes/AWS-10%20VPC/Exc.-4.1.PNG)

Exercise 4.2

![Exercise 4.2](../00_includes/AWS-10%20VPC/Exc.-4.2.PNG)

Exercise 4.3

![Exercise 4.3](../00_includes/AWS-10%20VPC/Exc.-4.3.PNG)

Exercise 4.4

![Exercise 4.4](../00_includes/AWS-10%20VPC/Exc.-4.4.PNG)

---

## Sources

[Everything You Need to Know](https://www.simplilearn.com/resources/cloud-computing)

[What is Virtual Private Cloud (VPC)?](https://docs.aws.amazon.com/vpc/latest/userguide/configure-your-vpc.html)

[YouTube Video: Amazon/AWS VPC (Virtual Private Cloud) Basics](https://www.youtube.com/watch?v=7_NNlnH7sAg)

[Storage and AWS](https://www.cloudcomputing-insider.de/suche/?k=VPC)

[How to...](https://www.middlewareinventory.com/blog/aws-vpc-peering-tutorial/)

## Overcome challanges

AWS interface is a bit overwhelming and daunting at first.

Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.

I tried to use what I had learned so far as much as possible in order to achieve a satisfactory result.

---