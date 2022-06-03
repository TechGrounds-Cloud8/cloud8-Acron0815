# Route 53

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