# Elastic Load Balancing (ELB) & Auto Scaling.

---

Elastic Load Balancing (ELB) and Auto scaling are quite different services. I have listed out some of the paramount differences between them

1. Elastic Load Balancer is used to balance load between EC2 instances however auto scaling is used to span and remove instances as per load.

2. ELB has url end point via which we can communicate with our application (i.e. a group of EC2 instances) however as per Load or CPU utilization auto scaling add or remove instances to the Target Group (i.e. set of EC2 instances).

3. Auto Scaling is responsible for the number of instances behind ELB however ELB is responsible for distributing traffic within the EC2 instances.


![ELB+AS](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/ElasticLoadBalancing%2BAutoScaling.PNG)
---
### What is Elastic Load Balancing (ELB) & Auto Scaling

- Elastic Load Balancing (ELB)

Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets and virtual appliances in one or more Availability Zones (AZs).

The load balancer will forward the request to one of the servers in the fleet, and relay the response back to the client.
Additional info

- Auto Scaling 

One of the main advantages of the cloud is that you don’t need to guess how much capacity you need. You can always scale up and down with on-demand services. One of the services that enables this is called Auto Scaling.

With websites, it often happens that few visitors visit the pages during the day and a lot of visitors visit the pages in the evening. 

During the day, the utilization is therefore low and there are too many servers available. In the evening, on the other hand, the number of servers is not sufficient and this results in performance problems. With autoscaling, the number of servers is automatically reduced during the day when the number of visitors is low, in order to use as many servers as necessary in the evening when the number of visitors is high.

### Key terminology

- ### AWS ELB

![LoadBalancer](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/LoadBalancer.PNG)

AWS ELB is a managed service that provides load balancing to a fleet of instances. There are four types of ELBs:

- ### Application Load Balancer: 

This ELB works using HTTP and HTTPS protocols (layer 7 of the OSI stack).

- ### Network Load Balancer: 

This ELB works using TCP and UDP (layer 4 of the OSI stack).

- ### Classic Load Balancer: 

This ELB is outdated and not recommended for use. AWS has (so far) never stopped supporting any services. The reason for this is that it can harm existing applications.

- ### Gateway Load Balancer: 

This ELB acts as a gateway into your network, as well as a load balancer. It will first route traffic to a (3rd party) application that checks the traffic, like an IDS/IPS or Firewall. After the packet has been inspected, the Gateway Load Balancer acts like a NLB routing to your application. GWLB act on layers 3 and 4 of the OSI stack.

- ### Cloudwatch: 

CloudWatch collects monitoring and operational data in the form of logs, metrics, and events, and visualizes it using automated dashboards so you can get a unified view of your AWS resources, applications, and services that run on AWS and on premises.

- Autoscaling 

Autoscaling is a built-in feature that automatically adjusts how your AWS setup reacts to loads. Autoscaling is the service you use to make your RDS setup autoscale within limits that you specify.
When you see the term autoscaling, think of the generic use of a feature (not necessarily a service) to make applications, services, and other AWS features add and remove resources as needed to make applications scale better and provide a consistent user experience. The Auto Scaling feature enables your EC2 instances to handle loads without a lot of human intervention.

![AutoScaling](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/AutoScaling.PNG)

- ## Exercise

Requirements:

Your AWS environment

## Exercise 1

Launch an EC2 instance with the following requirements:

Region: Frankfurt (eu-central-1)

AMI: Amazon Linux 2

Type: t3.micro

User data:

#!/bin/bash
#Install Apache Web Server and PHP
yum install -y httpd mysql php
#Download Lab files
wget https://aws-tc-largeobjects.s3.amazonaws.com/CUR-TF-100-RESTRT-1/- 80-lab-vpc-web-server/lab-app.zip
unzip lab-app.zip -d /var/www/html/
#Turn on web server
chkconfig httpd on
service httpd start

Security Group: Allow HTTP

Wait for the status checks to pass.

Create an AMI from your instance with the following requirements:

Image name: Web server AMI   

## Exercise 2

 Create an application load balancer with the following requirements:

Name: LabELB

Listener: HTTP on port 80

AZs: eu-central-1a and eu-central-1b

Subnets: must be public

Security Group: 
Name: ELB SG
Rules: allow HTTP access

Target Group:
Name: LabTargetGroup
Targets: to be registered by Auto Scaling
  
## Exercise 3

Create a launch configuration for the Auto Scaling group. It has to be identical to the server that is currently running.
Create an auto scaling group with the following requirements:
Name: Lab ASG
Launch Configuration: Web server launch configuration
Subnets: must be in eu-central-1a and eu-central-1b
Load Balancer: LabELB
Group metrics collection in CloudWatch must be enabled
Group Size:
Desired Capacity: 2
Minimum Capacity: 2
Maximum Capacity: 4
Scaling policy: Target tracking with a target of 60% average CPU utilisation


## Exercise 4

Verify that the EC2 instances are online and that they are part of the target group for the load balancer.

Access the server via the ELB by using the DNS name of the ELB.

Perform a load test on your server(s) using the website on your server to activate auto scaling. There might be a delay on the creation of new servers in your fleet, depending on the settings on your Auto Scaling Group.



### Sources

[A Brief Note...](https://medium.com/programmingnotes/aws-auto-scaling-and-load-balancing-b1c6eeb4d074)

[Amazon](https://aws.amazon.com/blogs/aws/new-aws-load-balancing-automatic-scaling-and-cloud-monitoring-services/)

[Amazon2](https://docs.aws.amazon.com/index.html?nc2=h_ql_doc_do)

[YouTube-Video1](https://www.youtube.com/watch?v=z59TDrLSFx4)

[YouTube-Video2](https://www.youtube.com/watch?v=4EOaAkY4pNE) - 
Not the best sound quality but interesting!

[Jayendra's Cloud Certification Blog](https://jayendrapatil.com/aws-auto-scaling/)


### Overcome challanges

Besides looking for relevant information (see the Sources), I also encountered several pitfalls that I tried to avoid.

I was not aware of how important the F5 key can be!

- ## [F5](https://docs.digicert.com/certificate-tools/Certificate-lifecycle-automation-index/automation-user-guide/install-automation-agentless-loadbalancer/high-availability-f5-big-ip-load-balancer/) ![Robot](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Robot.PNG)


### Results

E1

![Exc.1.0](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-1-1.0.PNG)

![Exc.1.1](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-1-1.1.PNG)

![Exc.1.2](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-1-1.2.PNG)

![Exc.1.3](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-1-1.3.PNG)

![Exc.1.4](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-1-1.4.PNG)

![Exc.1.5](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-1-1.5.PNG)

E2

![Exc.2.0](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-2-1.0.PNG)

![Exc.2.1](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-2-1.1.PNG)

E3

![Exc.3.0](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-3-1.0.PNG)

![Exc.3.1](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-3-1.1.PNG)

E4

![Load](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Load4.1.png)
![Exc.4.0](../00_includes/AWS-11%20ELB%20%26%20Auto%20Scaling/Exc.-4-1.0-1.png)
