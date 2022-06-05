# Files,AppServices,CDN,DNS,Database





## Study:

- Elastic Beanstalk

- Cloudfront

- Route 53

### Elastic Beanstalk

![Elastic-Beanstalk](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Elastic-Beanstalk.PNG)

Elastic Beanstalk is an application lifecycle management platform that enables organizations to monitor, autoscale, and track performance of CPU utilization, latency, and response codes.

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

### Cloudfront

![Cloudfront](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Cloud-Front.PNG)

 Cloudfront is a Content Delivery Network (CDN) service that makes it possible to deliver applications, data, videos and APIs in a developer-friendly environment.

 - Here are a few advantages of Cloudfront

 -It's easy to start to use the CDN service once you host your website on Amazon

- Here are a few downsides of Cloudfront

-Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.

-The pricing is not so transparent.

-I (you) will need a specialist to manage it.


 ### Route 53

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


## Key terminology

### CDN: 

A content delivery network refers to a geographically distributed group of servers which work together to provide fast delivery of Internet content. A CDN allows for the quick transfer of assets needed for loading Internet content.

### DNS: 

Short for Domain Name System, connects your domain name to your web server. It is often referred to as the "phone book of the internet".

DNS supports direct traffic on the Internet by connecting domain names to actual web servers. Essentially, it takes a user-friendly request - a domain name such as thelostboys.nl - and translates that into a computer-friendly server IP address - such as 216.3.128.12.

### EFS: 

Amazon Elastic File System (Amazon EFS) automatically grows and shrinks as you add and remove files with no need for management or provisioning.

### RDS: 

Amazon Relational Database Service (RDS) is a collection of managed services that makes it simple to set up, operate, and scale databases in the cloud. Choose from seven popular engines.

### Aurora: 

Amazon Aurora is a relational database management system (RDBMS) built for the cloud with full MySQL and PostgreSQL compatibility.


## Exercises

### Amazon Elastic File System (Amazon EFS)
	In this exercise I create a Amazon EFS file system.

- Sources

[Was ist EFS?](https://www.howtoforge.de/anleitung/was-ist-efs-elastic-file-system-in-aws-und-wie-benutzt-man-es/)

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
After some searching on the internet and in the security tab it turned out that I had to change/adjust the Inbound rules!

![Terminal-1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Terminal1.PNG)



- ### Amazon Relational Database Service (RDS)

Amazon RDS is a managed relational database service capable of taking the stress out of the management tasks you might have to deal with otherwise. It’s easy to work with and provides more flexibility than managing your own servers. Instead of bundling CPU, memory, storage, and throughput like a typical server, for example, Amazon RDS allows you to scale each of these features independently and allocate them as necessary. It also includes tools to create backups, carry out software patching processes, and set up automatic failure detection and recovery.

-Amazon RDS stores data as tables, records, and fields.

-Values from one table, can have a relationship to values in other tables. Relationships are a key part of relational databases.

-Relational databases are often used for storing transactional and analytical data.

-Relational databases provide stability and reliability for transactional databases.

- ### Amazon Aurora

The fundamental building block of Amazon RDS is called the “DB instance.” A DB instance is a database environment in the cloud, and it can contain multiple databases. Each DB instance runs a DB engine, and with Amazon RDS, you can choose between various DB engines, including Aurora.
You can access RDS and Aurora through Amazon Web Services (AWS), but they have slightly different intended uses. Essentially, the AWS Aurora database is a custom engine for Amazon RDS and is optimized for performance in the cloud.
Aurora is compatible with MySQL and PostgreSQL, and it’s intended to combine the availability and performance of traditional database engines with the cost-effectiveness and straightforwardness of open source. RDS can be used with various engines, while Aurora is a special engine developed for use with RDS.

- ### Amazon Aurora vs. Amazon Relational Database Service (RDS)

The main benefits of Amazon RDS are its preconfigured parameters, automatic software patching capabilities, and robust tools for monitoring and metrics.

As a custom engine for RDS, Amazon Aurora has additional features to make it faster and more modern. Aurora has high throughput, storage auto-scaling, and a self-healing, fault-tolerant storage system. It also provides point-in-time recovery and continuous backup, and it offers replication across three availability zones to keep your data secure.

The performance of Aurora and RDS depends on the engine you use with RDS, as some are optimized for availability instead of speed or to fit in with existing code.

## Exercise

I create a Database (DB) in my AWS Console (RDS--> Databases)

![Database1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Database1.PNG)

![Database2](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Database2.PNG)
---









[Subject]

[Give a short summary of the subject matter.]

Key terminology

[Write a list of key terminology with a short description. To prevent duplication you can reference to previous excersizes.]

Exercise

Sources

[List your sources you used for solving the exercise]

Overcome challanges

[Give a short description of your challanges you encountered, and how you solved them.]

Results

[Describe here the result of the exercise. An image can speak more than a thousand words, include one when this wisdom applies.]