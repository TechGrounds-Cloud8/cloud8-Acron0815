# Subnetting

[Peter Packet Subnetting Video](https://www.youtube.com/watch?v=VcVz6Lwxe2c)


Subnetting is the formation of subnets within a contiguous address space of IP addresses. A subnet is a physical segment of a network that uses IP addresses with the same network address.

With subnetting, a network is divided into several small networks. Subnetting is important because the number of IP addresses is scarce. The scarcity is due to the IP address being only 4 bytes long.

## Key terminology

Gateway:

A gateway is an active network node that can be addressed from both sides. It can also couple more than two networks together. Gateways handle different protocols on both sides up to layer 7. In particular, routing across network boundaries (correct addressing!) is an important task of the gatewaywant to delve too far into why or when subnetting is needed, as this article will focus primarily on computation. In short, subnetting brings the following benefits:

NAT-Gateway:

A NAT gateway allows cloud resources without public IP addresses to access the Internet without exposing those resources to incoming Internet connections.

Public subnet - Private subnet

The instances in the public subnet can send outbound traffic directly to the internet, while the instances in the private subnet cannot. Instead, the instances in the private subnet can access the internet through a network address translation (NAT) gateway located in the public subnet. The database servers can connect to the Internet using the NAT gateway, but the Internet cannot connect to the database servers.

CIDR-Classless Inter-Domain Routing

Classless Inter-Domain Routing (CIDR), sometimes also called supernetting, is a method that allows Internet addresses in inter-domain routing to be assigned and specified much more flexibly than the Internet Protocol (IP) actually allows. With the help of CIDR, the number of available addresses can be significantly increased. CIDR is currently used as a routing system by almost all gateway hosts in the backbone network of the Internet. Internet regulators assume that almost all Internet service providers will use CIDR for routing tasks in the future.

![CIDR-Chart](../cloud8-Acron0815%20map%20met%20mijn%20afbeldingen/00_includes/)

### Why is subnetting so important?

The series of numbers, binary conversions and logical comparisons have a deterrent effect. Especially in the context of the approaching changeover to IPv6, some might ask themselves: Is it worth it at all? The answer is quite clear: Yes! This is why subnetting will remain useful in the future.

Extension of the address range within a network: With subnetting, the network administrator can decide for himself how large his networks will be.
Fast connection between hosts in a subnet: data packets go directly from the sender to the recipient and are not routed through the entire network first via the router.
Better logical organization of the network participants: In order to have a better overview of the hosts, it makes sense to segment them according to local criteria (different buildings or floors) or according to departments.
More security: If a participant in the network is attacked from outside, the entire network is quickly threatened. Subnetting makes it easier for network administrators to isolate the subnets from each other.



 - Subnetting in practice

 Let's say we have the following IP address 192.168.0.15/24. In this example, the subnet mask would be 255.255.255.0 because 24 bits of the subnet mask are set to 1. 
 The subnet mask then looks like this: 11111111.11111111.11111111.00000000

All bits in the subnet mask that are set to 1 describe the network part of the IP address. All bits that are set to 0, the host part. The host portion determines how many IP addresses can be accommodated in a (sub)net. So in this example 28 because 8 bits are set to 0. So we have 8 host bits. However, if we want to further subdivide our network, for example because we want to form four subnets for, for example, four departments in a company, we have to "steal" bits from the host part and add them to the network part. The subnet mask therefore determines which subnet an IP address is in and how many IP addresses there are per subnet. Here's an example:

Searched number of subnets: 4
Question: How many bits do we have to take from the host part so that we can form 4 subnets?
Calculation method: 2n >= 4
Solution: 22 >= 4

So we need to add two bits from the host part to the network part. In our example, the subnet mask /24 becomes the new subnet mask /26 or 255.255.255.192 or in binary 11111111.11111111.11111111.11000000.

## Exercise

- Create a network architecture that meets the following requirements:
1 private subnet that can only be reached from within the LAN. This subnet must be able to accommodate at least 15 hosts.
- 1 private subnet that has internet access through a NAT gateway. This subnet must be able to place at least 30 hosts (the 30 hosts does not include the NAT gateway).
- 1 public subnet with an internet gateway. This subnet must be able to place at least 5 hosts (the 5 hosts is excluding the internet gateway).



### Sources

[YouTube video - IP addressing and Subnetting](https://www.youtube.com/watch?v=OqsXzkXfwRw)

[Subnetting for dummies](https://community.spiceworks.com/networking/articles/2489-subnetting-for-dummies)

[A COMPLETE BEGINNER'S GUIDE TO SUBNETTING](https://www.networkfuntimes.com/a-complete-beginners-guide-to-subnetting/)

[YouTube video - Subnetting For Dummies - IP Addresses and Subnetting](https://www.youtube.com/watch?v=4sDd8QLCLc8)

[IP Subnet Calculator](https://www.calculator.net/ip-subnet-calculator.html)


### Overcome challanges
Finding the right information.

I bought the book "Networking for Dummies" at Amazon,and have read it.

Read into the matter

### Results
The series of numbers, binary conversions and logical comparisons have a deterrent effect. Especially in the context of the approaching changeover to IPv6, some might ask themselves: Is it worth it at all? The answer is quite clear: Yes! This is why subnetting will remain useful in the future.