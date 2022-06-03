# Elastic Beanstalk

![Elastic-Beanstalk](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Elastic-Beanstalk.PNG)

Elastic Beanstalk is an application lifecycle management platform that enables organizations to monitor, autoscale, and track performance of CPU utilization, latency, and response codes.

Also is AWS Elastic Beanstalk a service from Amazon that provides web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers like Apache, Nginx, Passenger, and IIS and scaled.

-AWS Elastic Beanstalk is brilliant for offering PaaS in terms of application code management and deployments.

-It helps me by focusing more on the coding standards and not the underlying infrastructure.

-Also it provides great levels of flexibility, ease of usage for deploying & scaling web based application in AWS Platform based on the client specifications.

- Here are a few advantages of Elastic   Beanstalk

-It offers a variety of programming languages compatibility. 

-It has a very simple setup procurement and hence even people who are new to use Elastic Beanstalk find it very easy.

-Also, it gives me the comfort of manage my application with other AWS product services such as EC2, S3, SNS, etc.

-It works very well with other AWS product services like EC2, S3, SNS, etc.

- Here are a few downsides of Elastic Beanstalk

-Its cost is not definitive and it depends on the number of EC2 Instances and S3 Bucket size.

-Although it has dedicated CLI for operability, most of the convenient features present in AWS CLI is not available.


![Elastic-Beanstalk2](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Elastic-Beanstalk2.PNG)

In this diagram, the environment is shown within the top-level solid line. When you create an environment, Elastic Beanstalk provisions the resources required to run your application. AWS resources created for an environment include one elastic load balancer (ELB in the diagram), an Auto Scaling group, and one or more Amazon Elastic Compute Cloud (Amazon EC2) instances.

- Elastic Beanstalk in association with EC2

When Elastic Beanstalk analyses my application and selects the resources that will be required. When I deploy an application, Beanstalk will offer an EC2 instance. It will also allow me to step in and select alternative resources that may be better suited to anticipated use cases it may not know about. For example I could select a higher spec EC2 instance type that better suits my needs.

## ! 
Since Elastic Beanstalk is built on top of existing services like EC2, you can also use the underlying resources (though be careful here!).


## Sources

[YouTube Video: Elastic Beanstalk Tutorial](https://www.youtube.com/watch?v=jnMUp2c9AzA)

[Amazon AWS Document - AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/?sc_channel=EL&sc_campaign=Anim_Explainer_2020_vid&sc_medium=YouTube&sc_content=Video7757&sc_detail=COMPUTE&sc_country=US)

[Amazon AWS Document - AWS Elastic Beanstalk FAQs](https://aws.amazon.com/elasticbeanstalk/faqs/)

