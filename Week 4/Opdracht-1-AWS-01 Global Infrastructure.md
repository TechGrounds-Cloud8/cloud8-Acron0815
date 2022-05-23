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
### - CloudFront
### - Regional Edge Caches.


# Study

1.What is an AWS Availability Zone?

2.What is a Region?

3.What is an Edge Location?

4.Why would you choose one region over another? (e.g. eu-central-1 (Frankfurt) over us-west-2 (Oregon)


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


Service availability: Because AWS is gradually building up its global infrastructure, a new service is not immediately available in every region at all times.

### Sources

[AWS Regions](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/#:~:text=the%20Middle%20East.-,Availability%20Zones,connectivity%20in%20an%20AWS%20Region.)

[Globale AWS-Infrastruktur](https://www.windowspro.de/thomas-drilling/globale-aws-infrastruktur-regionen-availability-zonen-edge-standorte-verstehen)

3. ### What is an Edge Location?

- How do I take advantage of edge locations?
Here’s the great news: You don’t need to do anything to take advantage of edge locations.

If you’re an AWS customer and you use services like CloudFront or Route 53, you’re automatically using edge locations and getting all of the associated benefits. You don’t have to do any configuration or opt-in—it’s all part of the package.

But even if you’re not an AWS customer, you still benefit. CloudFront serves thousands of websites, including ones you visit. And guess what? You saw them that much faster, all thanks to edge locations.

Edge locations are AWS data centers designed to deliver services with the lowest latency possible. Amazon has dozens of these data centers spread across the world. They’re closer to users than Regions or Availability Zones, often in major cities, so responses can be fast and snappy. A subset of services for which latency really matters use edge locations, including:

- CloudFront is the most commonly discussed use of edge locations. It’s a content delivery network that caches content in edge locations. Content can be served directly from the cache, so it gets to users faster. CloudFront is often used to serve static assets, speed up websites, and stream video.
- Route 53 is purportedly a managed DNS service with name servers spread across Amazon’s edge locations. DNS responses come directly from the edge locations, so they’re as fast as possible.
- Web Application Firewall and AWS Shield provide a firewall and DDoS protection, respectively. These services filter traffic in edge locations so malicious or unwanted traffic can be discarded as close to source as possible. This, in turn, reduces congestion on Amazon’s global network and the public internet.
- AWS Global Accelerator allows you to route requests for key resources through  Amazon’s global network—even if the request is going halfway round the world. The request is initially routed to the closest edge location and then travels through Amazon’s network—often with lower latency and higher throughput than the public internet.
You can’t run your workloads directly in edge locations; they’re only used by Amazon’s managed services.

Some edge location services return a fast response directly to the user. For example, CloudFront caches content in edge locations, and that content can be served directly from the cache. Since the edge location is physically much closer to the user than the origin server, it has lower latency.

Other edge location services route traffic onto the AWS network. AWS has a global network backbone of high-bandwidth, redundant fiber links. Traffic sent over this network is often faster and more reliable than the public internet, especially over long distances. For example, if you download an object using S3 Transfer Acceleration, that object travels from S3 over the AWS global network to your nearest edge location, and it only uses the public internet for the final hop.

There are many more edge locations than Regions. This means users are more likely to be close to an edge location, and get those low latency responses. Amazon adds new edge locations regularly, and users who live nearby will see an automatic improvement in performance. For example, Amazon recently added their first edge location in Thailand. If your application was using AWS Global Accelerator, it would have become faster for Thai users—with no effort required on your part.

Note that not every edge location supports every service; check the per-service documentation to see exactly which edge locations are used by whatever service you’re using.

### Sources

[What is an Edge Location in AWS?](https://www.lastweekinaws.com/blog/what-is-an-edge-location-in-aws-a-simple-explanation/)

4. ### Why would you choose one region over another? (e.g. eu-central-1 (Frankfurt) over us-west-2 (Oregon)

Which AWS Region Should You Choose?

Data pricing is a big part of AWS, and something that changes by region

AWS data centers anywhere in the world. To complicate your pricing further, each region has different pricing for specific products. Which region is the cheapest? Which one should you build your network architecture?

US-East is usually the cheapest

If you take a look at this pricing chart from Concurrency Labs, it's clear that the two US-East regions, us-east-1 (N. Virginia) and us-east-2 (Ohio), are very cheap compared to the other.


 us-west-2 (Oregon) is also very low, but the us-west-1 suffers from Silicon Valley pricing and is much more expensive. Mumbai (India) is also surprisingly quite cheap when compared to the rest of the world.


 As for all other regions, they are all more expensive than these four. European regions are typically around 10% more expensive, with Stockholm being the cheapest of them all—just 6% more expensive than the cheapest US regions. The Asian market is around 20-25% more expensive, with Seoul being the cheapest this side of the world only 10% more than the eastern US.

 
Data from CloudFront to North America and Europe is the cheapest and the same prices. For the rest of the world, it's a bit more expensive, with South America again topping the list. Anyway, with CloudFront, you're paying for that data as long as you have South American visitors, so there's not much you can do about it.

For internal data transfer, most regions are the same. Search S3 prices, data from S3 to any range $0.02 per GB. However, if you transfer from us-east-1 to east-usa-2 or vice versa, the fee is only $0.01. This doesn't apply, however, if you're broadcasting within the same region, so it only really matters if you have servers in both Ohio and Northern Virginia.


When picking a region based on pricing alone, Northern Virginia and Ohio should be your first picks on the east coast, with Oregon for the west. Avoid Northern California if you can as it is over 20% more expensive.

If you need servers around the world, Stockholm and Seoul are the cheapest options for the European and Asian markets, respectively, and they cover most of the world, taking those two points alone.

No matter which region you choose to stay in, that region and always be in the same Availability Zone as there are fees for transferring data across it. Despite being part of the same region, Availability Zones are physically separate data centers and data between them must still travel over common internet wires.

Choose More Regions for Better Latency
Given how expensive some of the AWS Regions are, the only real reason to choose a more expensive region is if location is more important than price.

For example, if you're a startup working out of Silicon Valley and you really want low latency, you may be fine with paying a 20% premium. For services like Uber that rely on minimal latency to major metropolitan areas, being located in Northern California is simply the cost of doing business.

For many applications though, latency doesn't matter too much unless your site or service is extremely optimized. Looking at this map of AWS regions, many places don't have data centers in their backyard. There's no us central region (yet) because more people live closer to the coasts, and the latency isn't really over 50ms to either coast or Ohio anyway.

If you want to cover most of the world with relatively low latency overall while minimizing costs, you should build your infrastructure across four or five locations:

Ohio as it is closer to central United States than Virginia and equidistant from most of the east coast. Virginia would also be a good option here.
Oregon to cover the west coast.
Stockholm (Sweden) on Europe.
Seoul (South Korea) on the Pacific and Asia region.
Mumbai (India) is almost as cheap as the United States, so with servers here would be a better idea for the South Pacific region compared to Singapore or Bahrain (Middle East) regions.
Really, if you care a lot about latency, use a CDN like AWS CloudFront anyway. A CDN stores your website on servers around the world, and serves your website from that cache instead of traveling to it. This relieves some of the stress from your primary web server, and also gives you the benefit of having your network edge physically closer to a specific user. This speeds up the loading times and reduces the time

### Sources

[Which AWS Zone?](https://stackovercoder.com.de/server/466588/which-aws-zone-to-choose-if-website-traffic-will-be-from-india-only)

[Choosing your AWS Region wisely](https://www.concurrencylabs.com/blog/choose-your-aws-region-wisely/)

[Welche AWS-Region Sollten Sie Wählen?](https://allinfo.space/2020/08/11/die-aws-region-sollten-sie-wahlen)


### Overcome challanges
It was not easy to find and filter the large amount of information


