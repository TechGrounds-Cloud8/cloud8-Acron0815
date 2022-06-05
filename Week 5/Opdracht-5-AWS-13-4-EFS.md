# EFS: 

Amazon Elastic File System (Amazon EFS) automatically grows and shrinks as you add and remove files with no need for management or provisioning.

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
After some searching on the internet and in the security tab it turned out that I had to change/adjust the Inbound rules.

![Terminal-1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Terminal1.PNG)

---

## Overcome challanges

AWS interface is a bit overwhelming and daunting at first.

Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.