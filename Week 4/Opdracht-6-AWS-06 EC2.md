# EC2

![Amazon EC2](../00_includes/AWS-06%20EC2/Amazon%20EC2.PNG)

## EC2 (Elastic Compute Cloud)

EC2 is one of the premier services offered by Amazon Web Services. EC2 is among the 3 introductory services that were offered by AWS when launched in 2006 (the other 2 being S3 and SQS). The EC2 service provides users with a secure, configurable, scalable, and resizable computing capacity. Users can provision any number of instances and any type of instances they want and pay only for the time service is used for.


## Key terminology

- Amazon EC2 is elastic: With EC2, the computing capacity can be precisely adapted to the respective needs and can be reduced or increased depending on the requirements.

- Amazon EC2 can be fully controlled because there is full root access for each server instance

- Amazon EC2 is flexible because you can always choose between different instance types, software packages and operating systems.

- Amazon EC2 is reliable because, according to the EC2 Service Level Agreement, there is almost 100% availability for each Amazon EC2 region.


## Sources

[Amazon Machine Images (AMI)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html)

[How to Create AWS EC2 in 25 Easy Steps](https://www.waferwire.com/blog/how-to-create-aws-ec2-in-25-easy-steps/)

[AWS EC2 Tutorial — A Beginner’s Guide To Amazon EC2](https://medium.com/edureka/aws-ec2-tutorial-16583cc7798e)

[What Should you know About AWS EC2](https://medium.com/swlh/what-should-you-know-about-aws-ec2-e6943dfe73cc)


## Overcome challenges

It was a challenge to find the right place (website) with the right information.

This exercise contained many pitfalls for me and was challenging.

## Exercise 1
1- Navigate to the EC2 menu.

2- Launch an EC2 instance with the following requirements:

- AMI: Amazon Linux 2 AMI (HVM), SSD Volume Type

- Instance type: t2.micro

- Default network, no preference for subnet

- Termination protection: enabled

- User data:

#!/bin/bash

 yum -y install httpd

systemctl enable httpd

systemctl start httpd

 echo '<html><h1Hello From Your Web Server!</h1></html>' > /var/www/html/index.html

Root volume: general purpose SSD, Size: 8 GiB

New Security Group:

Name: Web server SG

Rules: Allow SSH, HTTP and HTTPS from anywhere

### 1

![Navigate](../00_includes/AWS-06%20EC2/Launch-instance.PNG)

### 2

![Launch](../00_includes/AWS-06%20EC2/Instance-summary1.PNG)

## Exercise 2

1- Wait for the Status Checks to get out of the initialization stage. When you click the Status Checks tab, you should see that the System reachability and the Instance reachability checks have passed.

2- Log in to your EC2 instance using an ssh connection.

3- Terminate your instance.

### 1

![Launch](../00_includes/AWS-06%20EC2/Instance-summary2.PNG)

### 2

![Log in](../00_includes/AWS-06%20EC2/3.PNG)

### 3

![Terminate](../00_includes/AWS-06%20EC2/Terminated.PNG)


# Tip

[Why not click here?](https://intellipaat.com/blog/what-is-amazon-ec2-in-aws/)