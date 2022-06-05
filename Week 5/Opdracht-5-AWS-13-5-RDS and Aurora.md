# Amazon Relational Database Service (RDS)

Amazon RDS is a managed relational database service capable of taking the stress out of the management tasks you might have to deal with otherwise. It’s easy to work with and provides more flexibility than managing your own servers. Instead of bundling CPU, memory, storage, and throughput like a typical server, for example, Amazon RDS allows you to scale each of these features independently and allocate them as necessary. It also includes tools to create backups, carry out software patching processes, and set up automatic failure detection and recovery.

-Amazon RDS stores data as tables, records, and fields.

-Values from one table, can have a relationship to values in other tables. Relationships are a key part of relational databases.

-Relational databases are often used for storing transactional and analytical data.

-Relational databases provide stability and reliability for transactional databases.

![RDS](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/RDS.png)

## Amazon RDS features and functionality

### Amazon RDS features and functions are:

- Six different database engines (Amazon Aurora, MySQL, PostgreSQL, MariaDB, Oracle and Microsoft SQL Server).

- Real-time scalable disk space with maximum size dependent on database engine (maximum 64 or 16 terabytes).

- Scale read traffic and increase read throughput across replicas.

- Automatic backup of database instances (databases and transaction logs) with user-defined retention time.

- User-initiated database snapshots.

- Deployment of Amazon RDS in multiple Availability Zones (Multi-AZ deployment) to realize high availability.

- Automatic host replacement in case of hardware failures.

- Encryption of data at rest and in transit including support for transparent data encryption in SQL Server and Oracle.

- Isolation of database instances in their own virtual networks.

- Controlling access via firewalling.

- Granting permissions for actions on RDS resources to users or groups through AWS Identity and Access Management (IAM).

- Monitoring of the operational metrics of the database instances via Amazon CloudWatch and management console (including Enhanced Monitoring with access to more than 50 key performance metrics).

- Automatic notification of database events via SMS or email.

- Management of Amazon RDS via AWS Management Console, AWS Command Line Interface, or Amazon RDS APIs.

- Automatic recording of all changes to database instances.

## Sources

[Introduction to Amazon Aurora](https://www.youtube.com/watch?v=FzxqIdIZ9wc)

[What is Amazon Relational Database Service (Amazon RDS)?](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html)

[Was ist Amazon RDS?](https://www.cloudcomputing-insider.de/was-ist-amazon-rds-a-1013070/)

[Amazon RDS](https://aws.amazon.com/rds/?nc=sn&loc=3&dn=1)

# Amazon Aurora

Amazon Aurora is a relational database management system (RDBMS) built for the cloud with full MySQL and PostgreSQL compatibility.

Aurora is therefore a MySQL and PostgreSQL managed compatible relational database engine. You can use existing MySQL and PostgreSQL databases with Aurora. However, Aurora can have up to five times the throughput of MySQL.

The fundamental building block of Amazon RDS is called the “DB instance.” A DB instance is a database environment in the cloud, and it can contain multiple databases. Each DB instance runs a DB engine, and with Amazon RDS, you can choose between various DB engines, including Aurora.
You can access RDS and Aurora through Amazon Web Services (AWS), but they have slightly different intended uses. Essentially, the AWS Aurora database is a custom engine for Amazon RDS and is optimized for performance in the cloud.
Aurora is compatible with MySQL and PostgreSQL, and it’s intended to combine the availability and performance of traditional database engines with the cost-effectiveness and straightforwardness of open source. RDS can be used with various engines, while Aurora is a special engine developed for use with RDS.

![Aurora DB Clusters](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Aurora.PNG)

## Sources

[What is Amazon Aurora?](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html)

[Amazon Aurora](https://www.computerweekly.com/de/definition/Amazon-Aurora)

[TouTube Video: Aws Aurora Db tutorial with Practical Example for beginners](https://www.youtube.com/watch?v=n_QplvENyLY)

[YouTube Video: Top 50+ AWS Services Explained in 10 Minutes](https://www.youtube.com/watch?v=JIbIYCM48to)

- ### Amazon Aurora vs. Amazon Relational Database Service (RDS)

The main benefits of Amazon RDS are its preconfigured parameters, automatic software patching capabilities, and robust tools for monitoring and metrics.

As a custom engine for RDS, Amazon Aurora has additional features to make it faster and more modern. Aurora has high throughput, storage auto-scaling, and a self-healing, fault-tolerant storage system. It also provides point-in-time recovery and continuous backup, and it offers replication across three availability zones to keep your data secure.

The performance of Aurora and RDS depends on the engine you use with RDS, as some are optimized for availability instead of speed or to fit in with existing code.

## Exercise

I create a Database (DB) in my AWS Console (RDS--> Databases)

![Database1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Database1.PNG)

![Database2](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Database2.PNG)

---

## Exercise 2

Amazon Relational Database Service (RDS) and also Amazon Aurora to learn and try to understand.

## Overcome challanges

AWS interface is a bit overwhelming and daunting at first.

Be ready for a ton of tech jargon that you are definitely not going to understand if you are new to this.

I tried to use what I had learned so far as much as possible in order to achieve a satisfactory result.