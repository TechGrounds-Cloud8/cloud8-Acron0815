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