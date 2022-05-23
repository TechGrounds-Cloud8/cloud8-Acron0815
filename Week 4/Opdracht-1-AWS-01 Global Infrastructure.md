### What does the abbreviation AWS mean?

Amazon Web Services (AWS) is the world's most comprehensive and widely used cloud platform with more than 200 services that offer extensive functions and are deployed in globally distributed data centers.



# AWS Global Infrastructure
In the cloud, everything from servers to networking is virtualized. As an AWS customer, you don’t have to worry about the underlying physical infrastructure. That being said, the physical location of an application in the cloud can be important.

AWS has a global infrastructure made up of the following components:
Regions
Availability Zones
Edge Locations

As a customer, you have different amounts of control over where your stuff is located depending on the service you use.
For example, IAM is a global service, so you get no control over where its information is stored. In contrast, you can select specific Availability Zones for RDS instances.


# Key terminology of AWS Global Infrastructure
### - Availability Zones (AZs)
### - Regions.
### - Edge Locations.
### - Regional Edge Caches.


# Study

1.What is an AWS Availability Zone?

2.What is a Region?

3.What is an Edge Location?

4.Why would you choose one region over another? (e.g. eu-central-1 (Frankfurt) over us-west-2 (Oregon)).


1. ### What is an AWS Availability Zone?

An Availability Zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity in an AWS Region. AZs give customers the ability to operate production applications and databases that are more highly available, fault tolerant, and scalable than would be possible from a single data center. All AZs in an AWS Region are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZs. All traffic between AZs is encrypted. The network performance is sufficient to accomplish synchronous replication between AZs. AZs make partitioning applications for high availability easy. If an application is partitioned across AZs, companies are better isolated and protected from issues such as power outages, lightning strikes, tornadoes, earthquakes, and more. AZs are physically separated by a meaningful distance, many kilometers, from any other AZ, although all are within 100 km (60 miles) of each other.

Availability Zones (AZs) are isolated environments within data center regions from which public cloud services are operated. Regions are geographic locations where cloud providers' data centers operate. Businesses choose one or more Availability Zones for their services around the world depending on their business needs.

The choice of availability zones is based on various reasons, for example compliance requirements or proximity to end customers can play a role. Cloud administrators can also replicate services across multiple availability zones to reduce latency or protect resources. In the event of a service failure, resources can also be moved to another availability zone. Certain cloud services can also be restricted to specified regions or availability zones.

Amazon divides the data centers of its AWS cloud (Amazon Web Services) into the regions of North, Central and South America, Europe/Middle East/Africa and Asia-Pacific. Each region in turn comprises several availability zones that are geographically separated from each other. Regions are connected to each other via the Internet. Each availability zone includes one or more data centers. In Germany, Amazon operates its own AWS data center in Frankfurt.

### Sources

[Availability Zones](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/#:~:text=the%20Middle%20East.-,Availability%20Zones,connectivity%20in%20an%20AWS%20Region.)

[Verfügbarkeitszonen (Availability Zones, AZs)](https://www.computerweekly.com/de/definition/Verfuegbarkeitszone-Availability-Zone)


2. ### What is a Region?


### Overcome challanges
[Give a short description of your challanges you encountered, and how you solved them.]

### Results
[Describe here the result of the exercise. An image can speak more than a thousand words, include one when this wisdom applies.]
