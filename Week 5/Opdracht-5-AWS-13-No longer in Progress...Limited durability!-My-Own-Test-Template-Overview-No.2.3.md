# Files,AppServices,CDN,DNS,Database


## Study:

- Elastic Beanstalk

- Cloud Front

- Route 53

- EFS

- RDS and Aurora

# Elastic Beanstalk

![Elastic-Beanstalk](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Elastic-Beanstalk.PNG)

Elastic Beanstalk is an application lifecycle management platform that enables organizations to monitor, autoscale, and track performance of CPU utilization, latency, and response codes.

Also is AWS Elastic Beanstalk a service from Amazon that provides web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers like Apache, Nginx, Passenger, and IIS and scaled.

-AWS Elastic Beanstalk is brilliant for offering PaaS in terms of application code management and deployments.

-It helps me by focusing more on the coding standards and not the underlying infrastructure.

-Also it provides great levels of flexibility, ease of usage for deploying & scaling web based application in AWS Platform based on the client specifications.

- Here are a few advantages of Elastic   Beanstalk

-It offers a variety of programming languages compatibility. 

-It has a very simple setup procurement and hence even people who are new to use Elastic Beanstalk find it very easy.

-Also, it gives me the comfort of manage my application with other AWS product services such as EC2, S3, SNS, etc.

-It works very well with other AWS product services like EC2, S3, SNS, etc.

- Here are a few downsides of Elastic Beanstalk

-Its cost is not definitive and it depends on the number of EC2 Instances and S3 Bucket size.

-Although it has dedicated CLI for operability, most of the convenient features present in AWS CLI is not available.


![Elastic-Beanstalk2](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Elastic-Beanstalk2.PNG)

In this diagram, the environment is shown within the top-level solid line. When you create an environment, Elastic Beanstalk provisions the resources required to run your application. AWS resources created for an environment include one elastic load balancer (ELB in the diagram), an Auto Scaling group, and one or more Amazon Elastic Compute Cloud (Amazon EC2) instances.

- Elastic Beanstalk in association with EC2

When Elastic Beanstalk analyses my application and selects the resources that will be required. When I deploy an application, Beanstalk will offer an EC2 instance. It will also allow me to step in and select alternative resources that may be better suited to anticipated use cases it may not know about. For example I could select a higher spec EC2 instance type that better suits my needs.

## ! 
Since Elastic Beanstalk is built on top of existing services like EC2, you can also use the underlying resources (though be careful here!).

## Exercise

Learn and try to understand Elastic Beanstalk.


## Sources

[YouTube Video: Elastic Beanstalk Tutorial](https://www.youtube.com/watch?v=jnMUp2c9AzA)

[Amazon AWS Document - AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/?sc_channel=EL&sc_campaign=Anim_Explainer_2020_vid&sc_medium=YouTube&sc_content=Video7757&sc_detail=COMPUTE&sc_country=US)

[Amazon AWS Document - AWS Elastic Beanstalk FAQs](https://aws.amazon.com/elasticbeanstalk/faqs/)

## Summary

Elastic Beanstalk is one of the most useful AWS services.

If you're starting with Amazon Web Services like me, it's easier to get started than with, for example, EC2 or CloudFormation.

---

## Overcome challanges

AWS interface is a bit overwhelming and daunting at first.

Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.

I tried to use what I had learned so far as much as possible in order to achieve a satisfactory result.

# CloudFront

![Cloudfront](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Cloud-Front.PNG)

 CloudFront is a Content Delivery Network (CDN) service that makes it possible to deliver applications, data, videos and APIs in a developer-friendly environment.

 - Here are a few advantages of CloudFront

 -It uses HTTP or HTTPS protocols for quick delivery of content.

-It's easy to start to use the CDN service once you host your website on Amazon

-Users get lower latency (the time it takes to load the first byte of the file) and higher data transfer rates.


- Here are a few downsides of CloudFront

-Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.

-The pricing is not so transparent.

-I (you) will need a specialist to manage it.

## What can I do with Amazon CloudFront?

Amazon CloudFront provides a simple API that lets you:

Distribute content with low latency and high data transfer rates by serving requests using a network of edge locations around the world.
Get started without negotiating contracts and minimum commitments.

## Exercise

Learn and try to understand Cloud Front.

## Sources

[Everything You Need to Know](https://www.simplilearn.com/tutorials/aws-tutorial/aws-cloudfront)

[What is Amazon CloudFront?](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)

[YouTube Video: AWS Cloud Front](https://www.youtube.com/watch?v=sQNONcj0cvc)

[Storage and AWS](https://www.cloudcomputing-insider.de/storage-in-aws-kostenlos-nutzen-a-1062343/)

## Results

Setting up a CDN (Content Delivery Network) is quick and easy with the help of CloudFront. Thanks to a CDN, a website can deliver static data to an incalculable number of users, regardless of the server. The website is therefore always available and will in all probability not suffer any failure, the server cannot overload!

## Summary

I find that CloudFront is very flexible and works well with other Amazon services, as is the case with most things on AWS.

Amazon CloudFront claims to be a fast content delivery service that securely delivers data, video, applications, and APIs to customers around the world with low latency and high transfer speeds - all within a developer-friendly environment. Benefits of using it include the provision of the highly resilient Amazon backbone network, network and application layer protection, custom programmability, and tight integration with AWS. The pricing model is usage-based; the free version includes 50 GB data transfer out and 2 million HTTP and HTTPS requests per month for one year.

---

## Overcome challanges

AWS interface is a bit overwhelming and daunting at first.

Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.

I tried to use what I had learned so far as much as possible in order to achieve a satisfactory result.


 # Route 53

![Route-53-1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Route-53-2.PNG)

 ![Route-53](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Route-53.PNG)

 "Route 53" is a DNS service that runs entirely in the Amazon cloud. It allows you to manage and deliver your own DNS zones. The DNS servers in the cloud are highly available and, according to Amazon, have a very low response latency.

 Amazon Route 53 effectively connects user requests to infrastructure running in AWS – such as Amazon EC2 instances, Elastic Load Balancing load balancers, or Amazon S3 buckets – and can also be used to route users to infrastructure outside of AWS.

 - Here are a few advantages of Route 53

 -Route 53 is designed to automatically handle large volume queries without the user’s interaction.

 -Distributed Route 53 DNS servers around the globe provide a low-latency fast service.

 -You only pay for what you use, for example, the hosted zones managing your domains, the number of queries which are answered per domain, etc.

 - Here are a few downsides of Route 53

 -No DNSSEC support. AWS Route 53 does not support the DNSSEC standard. DNSSEC can prevent man in the middle (MITM) attacks and other types of DNS attacks.

 -Route 53 with non-AWS endpoints/services, is expensive. The visual editor in particular is costly; it is $50/month in addition to the cost of queries for each record type to which you apply a visual editor policy.

 ## Terminology and attempts at explanation.

 - DNS - What is a Domain Name System (DNS) service?

 DNS is a globally distributed service that translates human-readable names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers use to network with each other. The Internet's DNS system works much like a phone book: it manages the mapping between names and numbers. With DNS, the names are domain names (www.example.com) that are easy to remember, and the numbers are IP addresses (192.0.2.1) that indicate the location of the computers on the Internet. DNS servers translate name requests into IP addresses, thereby controlling which server an end user reaches when they type a domain name into their web browser. These prompts are referred to as "requests".

 - CDN (Content Delivery Network)

A Content Delivery Network refers to a geographically distributed group of servers which work together to provide fast delivery of Internet content. A CDN allows for the quick transfer of assets needed for loading Internet content.

- EFS (Elastic File System) 

Amazon Elastic File System (Amazon EFS) automatically grows and shrinks as you add and remove files with no need for management or provisioning.

- RDS (Relational Database Service) 

Amazon Relational Database Service (RDS) is a collection of managed services that makes it simple to set up, operate, and scale databases in the cloud. Choose from seven popular engines.

- Aurora

Amazon Aurora is a relational database management system (RDBMS) built for the cloud with full MySQL and PostgreSQL compatibility.

 ## Sources

[What Is AWS Route 53?](https://www.youtube.com/watch?v=BtiS0QyiTK8)

[Cloudflare DNS](https://www.cloudflare.com/learning/dns/what-is-dns/)

[Cloudflare CDN](https://www.cloudflare.com/learning/cdn/what-is-a-cdn/)

[Amazon EFS features](https://aws.amazon.com/efs/features/)

[What is Amazon Relational Database Service (Amazon RDS)?](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html)

[What is Amazon Aurora?](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html)


## Exercise

Learn and try to understand Route 53.

 ---

 ## Overcome challanges

AWS interface is a bit overwhelming and daunting at first.

Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.

I tried to use what I had learned so far as much as possible in order to achieve a satisfactory result.

# EFS 

Amazon Elastic File System (Amazon EFS) automatically grows and shrinks as you add and remove files with no need for management or provisioning.

Amazon EFS is an NFS file system service offered by AWS. An Amazon EFS file system is excellent as a managed network file system that can be shared across different Amazon EC2 instances. Amazon EFS works like NAS devices and performs well for big data analytics, media processing workflows, and content management. EFS can be accessed by multiple instances at a time through NFS protocol. It is used as a clustered database and document sharing.

- Benefits of EFS

-With EFS you need not worry about  managing file servers or storage, updating hardware, configuring software, or performing backups as EFS is a fully managed service.

-The distributed architecture of Amazon EFS provides data protection from an AZ outage, system and component failures, and network connection errors.

-Network Access to the files can be controlled using Virtual Private Cloud security group rules and with Identity Access Management policies and EFS access points you can control the access to your files.

-Amazon EFS is designed to provide the throughput, IOPS, and low latency needed for a broad range of workloads.

-With Amazon EFS, storage capacity is elastic, growing and shrinking automatically as you add and remove files, dynamically providing the storage capacity to applications as they need it.

-AWS EFS provides encryption of data both at rest and in transit so that your data is secure.

![EFS Architecture](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/EFS.PNG)

## Exercises

### Amazon Elastic File System (Amazon EFS)
	In this exercise I create a Amazon EFS file system.

- Sources

[Dutch Cloud Community](https://dutchcloudcommunity.nl/)

[YouTube Video: Amazon Elastic File System (EFS)](https://www.youtube.com/watch?v=OyMqALRqG6s)

[AWS News Blog](https://dutchcloudcommunity.nl/nieuws/wire/aws-news-blog-new-lower-cost-storage-classes-for-amazon-elastic-file-system/)

[AWS EFS, EBS and S3: Best AWS Storage Option](https://k21academy.com/amazon-web-services/difference-between-aws-efs-ebs-and-s3/)

[Was ist EFS?](https://www.howtoforge.de/anleitung/was-ist-efs-elastic-file-system-in-aws-und-wie-benutzt-man-es/)

[Amazon EFS features](https://aws.amazon.com/efs/features/)

[Are you a first-time user of Amazon EFS?](https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html#welcome-first-time-user)


For this exercise I will use the Amazon Aws User Guide "Getting started with Amazon Elastic File System" for the link please click here --> [Getting started with Amazon Elastic File System](https://docs.aws.amazon.com/efs/latest/ug/getting-started.html)

![Create-EFS1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Create-EFS1.PNG)

![Create-EFS2](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Create-EFS2.PNG)

Here I see the Network information.

![Create-EFS3](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Create-EFS3.PNG)

In the next step I create a new Amazon EC2 instance running Amazon Linux 2, and configure it to automatically mount the EFS file system i just created in Step 1

![Step2-1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Create-EFS-Step2-1.PNG)

![Step2-2](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Create-EFS-Step2-2.PNG)

---

At my first login attempt on my newly created EC2 Instance, I was unable to access it.
After some searching on the internet and in the security tab it turned out that I had to change/adjust the Inbound rules.

![Terminal-1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Terminal1.PNG)

---

## Exercise

Learn and try to understand the Amazon Elastic File System (EFS).

## Overcome challanges

What is MySQL?

AWS interface is a bit overwhelming and daunting at first.

Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.

I tried to use what I had learned so far as much as possible in order to achieve a satisfactory result.

PS  Probably too late found explanation what MySQL is.

[What is MySQL? All I probably need to know.](https://www.talend.com/resources/what-is-mysql/)


# Amazon Relational Database Service (RDS)

Amazon RDS is a managed relational database service capable of taking the stress out of the management tasks you might have to deal with otherwise. It’s easy to work with and provides more flexibility than managing your own servers. Instead of bundling CPU, memory, storage, and throughput like a typical server, for example, Amazon RDS allows you to scale each of these features independently and allocate them as necessary. It also includes tools to create backups, carry out software patching processes, and set up automatic failure detection and recovery.

-Amazon RDS stores data as tables, records, and fields.

-Values from one table, can have a relationship to values in other tables. Relationships are a key part of relational databases.

-Relational databases are often used for storing transactional and analytical data.

-Relational databases provide stability and reliability for transactional databases.

![RDS](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/RDS.png)

## Amazon RDS features and functionality

### Amazon RDS features and functions are:

- Six different database engines (Amazon Aurora, MySQL, PostgreSQL, MariaDB, Oracle and Microsoft SQL Server).

- Real-time scalable disk space with maximum size dependent on database engine (maximum 64 or 16 terabytes).

- Scale read traffic and increase read throughput across replicas.

- Automatic backup of database instances (databases and transaction logs) with user-defined retention time.

- User-initiated database snapshots.

- Deployment of Amazon RDS in multiple Availability Zones (Multi-AZ deployment) to realize high availability.

- Automatic host replacement in case of hardware failures.

- Encryption of data at rest and in transit including support for transparent data encryption in SQL Server and Oracle.

- Isolation of database instances in their own virtual networks.

- Controlling access via firewalling.

- Granting permissions for actions on RDS resources to users or groups through AWS Identity and Access Management (IAM).

- Monitoring of the operational metrics of the database instances via Amazon CloudWatch and management console (including Enhanced Monitoring with access to more than 50 key performance metrics).

- Automatic notification of database events via SMS or email.

- Management of Amazon RDS via AWS Management Console, AWS Command Line Interface, or Amazon RDS APIs.

- Automatic recording of all changes to database instances.

## Sources

[Introduction to Amazon Aurora](https://www.youtube.com/watch?v=FzxqIdIZ9wc)

[What is Amazon Relational Database Service (Amazon RDS)?](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html)

[Was ist Amazon RDS?](https://www.cloudcomputing-insider.de/was-ist-amazon-rds-a-1013070/)

[Amazon RDS](https://aws.amazon.com/rds/?nc=sn&loc=3&dn=1)

# Amazon Aurora

Amazon Aurora is a relational database management system (RDBMS) built for the cloud with full MySQL and PostgreSQL compatibility.

Aurora is therefore a MySQL and PostgreSQL managed compatible relational database engine. You can use existing MySQL and PostgreSQL databases with Aurora. However, Aurora can have up to five times the throughput of MySQL.

The fundamental building block of Amazon RDS is called the “DB instance.” A DB instance is a database environment in the cloud, and it can contain multiple databases. Each DB instance runs a DB engine, and with Amazon RDS, you can choose between various DB engines, including Aurora.
You can access RDS and Aurora through Amazon Web Services (AWS), but they have slightly different intended uses. Essentially, the AWS Aurora database is a custom engine for Amazon RDS and is optimized for performance in the cloud.
Aurora is compatible with MySQL and PostgreSQL, and it’s intended to combine the availability and performance of traditional database engines with the cost-effectiveness and straightforwardness of open source. RDS can be used with various engines, while Aurora is a special engine developed for use with RDS.

![Aurora DB Clusters](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Aurora.PNG)

## Sources

[What is Amazon Aurora?](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html)

[Amazon Aurora](https://www.computerweekly.com/de/definition/Amazon-Aurora)

[TouTube Video: Aws Aurora Db tutorial with Practical Example for beginners](https://www.youtube.com/watch?v=n_QplvENyLY)

[YouTube Video: Top 50+ AWS Services Explained in 10 Minutes](https://www.youtube.com/watch?v=JIbIYCM48to)

- ### Amazon Aurora vs. Amazon Relational Database Service (RDS)

The main benefits of Amazon RDS are its preconfigured parameters, automatic software patching capabilities, and robust tools for monitoring and metrics.

As a custom engine for RDS, Amazon Aurora has additional features to make it faster and more modern. Aurora has high throughput, storage auto-scaling, and a self-healing, fault-tolerant storage system. It also provides point-in-time recovery and continuous backup, and it offers replication across three availability zones to keep your data secure.

The performance of Aurora and RDS depends on the engine you use with RDS, as some are optimized for availability instead of speed or to fit in with existing code.

## Exercise

I create a Database (DB) in my AWS Console (RDS--> Databases)

![Database1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Database1.PNG)

![Database2](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Database2.PNG)

---

## Exercise 2

Amazon Relational Database Service (RDS) and also Amazon Aurora to learn and try to understand.

## Overcome challanges

AWS interface is a bit overwhelming and daunting at first.

Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.

I tried to use what I had learned so far as much as possible in order to achieve a satisfactory result.