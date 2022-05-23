# AWS Pricing

![AWS Pricing](../00_includes/AWS-02%20Pricing/AWS-Pricing.PNG)

### Introduction:

One of the main reasons for moving to the cloud is cost. If done well, public cloud infrastructures can reduce costs significantly compared to traditional data centers. This is done by adopting a pay-as-you-go pricing model and economies of scale.

You pay only for the compute capacity, storage, and outbound data transfer that you use. You never pay for inbound data transfer and data transfer between services within the same region.

AWS lists four advantages of their pricing model:
Pay-as-you-go
Save when you commit
Pay less by using more
Benefit from massive economies of scale

When creating a new AWS account, you automatically get a free-tier account for the first 12 months. Some services are free up to a certain limit with a free-tier account.
Other services are always free. However, those services might be integrated with other services for which you have to pay.

The Total Cost of Ownership (TCO) is used to measure how much an infrastructure would cost if it were hosted the traditional way. This is done by measuring capital expenditures (capex). The cloud pricing model allows you to trade capex for variable expenditure. This can reduce cost by not spending money on capacity you don’t need.


## AWS pricing is calculated similar to your water and electricity bills. You only pay for the services you use. If you stop using it, there are no additional costs or cancellation fees!

# Study
1. The four advantages of the AWS pricing model.

2. AWS free tier for:
S3,
EC2,
Always free services

3. Understand the differences between capex and opex


## The four advantages of the AWS pricing model

Source

[AWS Pricing](https://aws.amazon.com/pricing/)

[Understanding the AWS Pricing](https://www.techmagic.co/blog/aws-pricing-model-overview/)

[AWS Pricing Calculator](https://calculator.aws/#/)

When you use the right pricing model for your workload resources, you pay the lowest price for those resources.

There are no upfront costs or long-term contracts with AWS, AWS only charges for the resources you use. AWS offers web hosting options with pay-as-you-go pricing or fixed monthly pricing. So it's always important to spend your money on the things that make your business different.

All services offered by the company are affordable and billed on a per-use basis. There are no upfront payments or contracts. This is as easy as it gets.

### 1. On-Demand Pricing

With on-demand pricing, you pay by the hour for usage of an AWS instance. This is the benchmark pricing for AWS instances—meaning that you compare other pricing models with this one when deciding which is best for you. The benefit of on-demand pricing is that you don’t have to plan in advance how many instances you need. This gives you maximum flexibility. However, it comes at a cost. On-demand pricing is the highest of the lot.

Pros

You aren’t obliged to make a long-term commitment

This model is good when you expect that the working load on the cloud may change
 
This is the most flexible pricing approach
 
Cons
   
Your saving opportunities are limited 
 
You may quickly run out of budget, and in this case, this model can turn into the most expensive one, even despite its flexibility
### 2. Spot Instances

With Spot Instances, users bid for the price of spare Instances. There’s a market price for spare instances, and only if this market price meets your instance will you be allotted the instance. Similarly, when the market price reduces, you’ll automatically lose your instance so your charge doesn’t shoot up. This model is a bit more complex than on-demand pricing, but it could save 50-90% of your total costs.

Pros

This is the cheapest AWS pricing model

The approach is suitable for failure-resistant operations, for example, for web servers or CI/CD

Cons

Following this model is challenging, especially if you are just getting started with cloud management

Your instance may be terminated at any time

### 3. Reserved Instances

Finally, if you can reliably predict approximately how much compute resources your applications need in advance, you should consider Reserved Instances (RIs)

AWS instances for a span of 1 or 3 years, get a significant discount as compared to on-demand prices. Reserved Instances are assigned to specific Availability Zones, so if you need control over your app’s performance globally, this may be a drawback.

If your concern is that your compute requirements may change over 3 years, AWS allows you to choose convertible Reserved Instances, so you can switch between instance types. However, you can shift down to a small instance like a T2.

You can even opt for scheduled RIs, so you reserve instances only during specific hours or days, depending on your usage. This gives you more flexibility with RIs.

Pros

Your costs are predictable

You may save up to 72% by making a long term commitment

This model is more user-friendly compared to Spot Instances

Cons

You have to make a long-term commitment

You have to pay for an instance regardless of the actual usage

### 4. Savings Plans

The saving plans pricing model was developed and launched in 2019. In this case, you have to choose the computing capacity you need (measured in a fixed price per hour) and make an instant commitment for 1-3 years. That’s, this model is an even more advanced embodiment of an on-demand approach, which in this case, is better predictable.

Pros

The easiest model to get started and proceed with
Your expenses are predictable

Cons

You have to make a long-term commitment

If you are using the resources that go beyond the chosen capacity, it will be charged according to an on-demand model

## AWS Free Tier

Source: 
[AWS Free Tier](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Categories=categories%23compute&trk=815440c9-b761-4d2b-b531-fe1ee8275a5a&sc_channel=ps&sc_campaign=acquisition&sc_medium=ACQ-P|PS-GO|Brand|Desktop|SU|Websites|EC2|BEN|EN|Text&s_kwcid=AL!4422!3!495073147331!b!!g!!%2Bfree%20%2Bec2%20%2Bhosting&ef_id=CjwKCAjw4ayUBhA4EiwATWyBrhhBmy_0DbISgV_xWCpT5sfplo_oYfAMyHjsyOl-PkjeWffqJ3ZOuxoC62sQAvD_BwE:G:s&s_kwcid=AL!4422!3!495073147331!b!!g!!%2Bfree%20%2Bec2%20%2Bhosting&awsf.Free%20Tier%20Types=*all)

The AWS Free Tier provides customers the ability to explore and try out AWS services free of charge up to specified limits for each service. The Free Tier is comprised of three different types of offerings, a 12-month Free Tier, an Always Free offer, and short term trials.

Services with a 12-month Free Tier allow customers to use the product for free up to specified limits for one year from the date the account was activated.

What is AWS S3?

Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. You can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere.

Is S3 included in AWS free tier?

No, the AWS Free Tier does not include Amazon S3 RRS storage. The AWS Free Tier includes 5 GB of Amazon S3 standard storage, which offers the highest Amazon S3 durability.

What is AWS EC2?

Amazon Elastic Compute Cloud (EC2) is the web service that providing resizable compute capacity in the cloud.

Does EC2 have a free tier?

Your free usage under the AWS Free Tier is calculated each month across all regions and automatically applied to your bill. For example, you will receive 750 Amazon EC2 Linux Micro Instance hours for free across all of the regions you use, not 750 hours per region.

Which AWS services are always free?

Always free offers can be used up to a certain extent for (for example) AWS Lambda, AWS Storage Gateway, Amazon Dynamo DB, Amazon Glacier, Amazon CloudWatch and many other services.

### The differences between capex and opex

![CAPEX vs OPEX](../00_includes/AWS-02%20Pricing/CAPEX-vs-OPEX.PNG)

Sources:

[Head to Head Comparison Between Capex VS Opex](https://www.educba.com/capex-vs-opex/)

[YouTube Video: CapEx vs OpEx explanation](https://www.youtube.com/watch?v=na4jbAh_vkQ)

Capex and Opex differ in the method of payment. While capex means one-off payments in advance, opex refers to monthly, annual or generally recurring and usually smaller expenses.

CapEx (Capital expenditures ): The one-time payment

Business expensens made up front in order to create long term benefits for the future. Specifically in IT this could mean hardware like servers, printers and scanners. Maintenance of particular hardware is also considered CapEx.

OpEx (Operating expenses): The recurring costs

Operating expenses,the expenses to run day-to-day business such as services like website hosting or domain registrations.

Some examples of CAPEX are:  Machinery, plant, land, building, patents and more. 

Examples of OPEX are:  Wages, rent, insurance, maintenance and repair of machinery and more.