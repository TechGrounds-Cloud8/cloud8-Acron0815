# Security Groups

Security Groups are AWS's firewall system.

An AWS Security Group acts as a virtual firewall for your EC2 instances to control incoming and outgoing traffic. 

Both inbound and outbound rules control the flow of traffic to and traffic from your instance, respectively.

----

## Key terminology

- VPC Flow logs

VPC Flow Logs is a feature that you can use to collect information about IP traffic to and from network interfaces in your VPC.

- Stateful firewall

Stateful firewalls are capable of monitoring and detecting states of all traffic on a network to track and defend based on traffic patterns and flows.

- Protocol. 

Network protocols the rule will allow, such as TCP and User Datagram Protocol.

- Port range. 

A specific port or a port range to allow traffic on.

- Source. 

A specific IP, IP range or other security groups that will be allowed access.

----

## Exercise

### Study (Security Groups and Network Access Control Lists in AWS)
----

### Security Groups

- ### Security Groups in AWS (see above)

### Network Access Control Lists in AWS

- ### A Network Access Control List (NACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. 

### Network Access Control Lists (NACL) are sometimes confused with Security Groups. 

### But they are not identical.

### Difference AWS Network ACL and Security Group.

![Difference](../00_includes/AWS-08%20Security%20Groups/Difference.PNG)

![Difference2](../00_includes/AWS-08%20Security%20Groups/Difference2.PNG)



## Sources

[VPC SecurityGroups](https://docs.aws.amazon.com/de_de/vpc/latest/userguide/VPC_SecurityGroups.html)

[Aws Cloud Training](https://acloudguru.com/content/aws-cloud-training-b2b?utm_campaign=16247388924&utm_source=google&utm_medium=cpc&utm_content=582724892537&utm_term=p_aws%20security&adgroupid=133878634736&gclid=CjwKCAjwyryUBhBSEiwAGN5OCLh8vjqUO8tjAL5qPZGwCfc9Z6PUpNchgpYUPGN6Rs-YXMrgK5igmhoCarUQAvD_BwE)

[Questions tagged with ...](https://repost.aws/tags/TATGuEiYydTVCPMhSnXFN6gA?forumID=58)

[2e Questions tagged with ...](https://repost.aws/search/questions?globalSearch=Security+Groups)

[Search Results for: Network Access Control Lists](https://repost.aws/search/questions?globalSearch=Network+Access+Control+Lists)

[YouTube Video: The differences between Security Groups and NACLs in AWS](https://www.youtube.com/watch?v=Oge3ZfOL0jk)

[Difference NACL/Security Groups](https://premaseem.wordpress.com/2021/03/05/difference-between-aws-network-acl-and-security-group/)