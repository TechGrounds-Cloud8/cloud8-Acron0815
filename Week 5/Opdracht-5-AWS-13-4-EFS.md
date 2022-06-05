# EFS: 

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