# Amazon Relational Database Service (RDS)

Amazon RDS is a managed relational database service capable of taking the stress out of the management tasks you might have to deal with otherwise. It’s easy to work with and provides more flexibility than managing your own servers. Instead of bundling CPU, memory, storage, and throughput like a typical server, for example, Amazon RDS allows you to scale each of these features independently and allocate them as necessary. It also includes tools to create backups, carry out software patching processes, and set up automatic failure detection and recovery.

-Amazon RDS stores data as tables, records, and fields.

-Values from one table, can have a relationship to values in other tables. Relationships are a key part of relational databases.

-Relational databases are often used for storing transactional and analytical data.

-Relational databases provide stability and reliability for transactional databases.

# Amazon Aurora

The fundamental building block of Amazon RDS is called the “DB instance.” A DB instance is a database environment in the cloud, and it can contain multiple databases. Each DB instance runs a DB engine, and with Amazon RDS, you can choose between various DB engines, including Aurora.
You can access RDS and Aurora through Amazon Web Services (AWS), but they have slightly different intended uses. Essentially, the AWS Aurora database is a custom engine for Amazon RDS and is optimized for performance in the cloud.
Aurora is compatible with MySQL and PostgreSQL, and it’s intended to combine the availability and performance of traditional database engines with the cost-effectiveness and straightforwardness of open source. RDS can be used with various engines, while Aurora is a special engine developed for use with RDS.

- ### Amazon Aurora vs. Amazon Relational Database Service (RDS)

The main benefits of Amazon RDS are its preconfigured parameters, automatic software patching capabilities, and robust tools for monitoring and metrics.

As a custom engine for RDS, Amazon Aurora has additional features to make it faster and more modern. Aurora has high throughput, storage auto-scaling, and a self-healing, fault-tolerant storage system. It also provides point-in-time recovery and continuous backup, and it offers replication across three availability zones to keep your data secure.

The performance of Aurora and RDS depends on the engine you use with RDS, as some are optimized for availability instead of speed or to fit in with existing code.

## Exercise

I create a Database (DB) in my AWS Console (RDS--> Databases)

![Database1](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Database1.PNG)

![Database2](../00_includes/AWS-13%20Files%2CApp%20Services%2CCDN%2CDNS%2CDatabase/Database2.PNG)
---