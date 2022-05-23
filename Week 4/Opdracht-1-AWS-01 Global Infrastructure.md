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

For starters, it's enough to know that there are multiple AWS Regions on almost every continent that are independent and isolated from each other. Traffic between regions always runs over the public internet. The overview of the global AWS infrastructure always provides the current number of regions and the availability zones (AZ) and edge locations available per region.

AWS has the concept of a Region, which is a physical location around the world where we cluster data centers. We call each group of logical data centers an Availability Zone. Each AWS Region consists of multiple, isolated, and physically separate AZs within a geographic area. Unlike other cloud providers, who often define a region as a single data center, the multiple AZ design of every AWS Region offers advantages for customers. Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks. AWS customers focused on high availability can design their applications to run in multiple AZs to achieve even greater fault-tolerance. AWS infrastructure Regions meet the highest levels of security, compliance, and data protection.

In Europe there are currently 4 regions Dublin, London, Frankfurt and Paris with a different number of availability zones. In Frankfurt there are three. Only in Africa, Greenland and Russia does AWS not have its own regions. All traffic within a region flows over AWS-owned networks.

AWS provides a more extensive global footprint than any other cloud provider, and to support its global footprint and ensure customers are served across the world, AWS opens new Regions rapidly. AWS maintains multiple geographic Regions, including Regions in North America, South America, Europe, China, Asia Pacific, South Africa, and the Middle East.

Even if you only want to book simple resources such as virtual machines or storage with Amazon Web Services, you should understand how this global cloud infrastructure is structured. Their structure and networking has a significant impact on data security, availability and performance.

Replication within regions
AWS uses the distributed infrastructure of data centers and AZs for internal replication and thus implements the guaranteed availability of services with built-in availability, for example for S3 or ELB (Elastic Load Balancing).

AWS will never replicate resources out of a particular Region without the knowledge or consent of the customer, unless the customer explicitly does so, such as when copying a snapshot or AMI to another region.



The table of regions shows which services are available where.

Service availability: Because AWS is gradually building up its global infrastructure, a new service is not immediately available in every region at all times. The table of regions provides information on this.

### Sources

[AWS Regions](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/#:~:text=the%20Middle%20East.-,Availability%20Zones,connectivity%20in%20an%20AWS%20Region.)

[Globale AWS-Infrastruktur](https://www.windowspro.de/thomas-drilling/globale-aws-infrastruktur-regionen-availability-zonen-edge-standorte-verstehen)

3. ### What is an Edge Location?





### Overcome challanges
[Give a short description of your challanges you encountered, and how you solved them.]

### Results
[Describe here the result of the exercise. An image can speak more than a thousand words, include one when this wisdom applies.]
