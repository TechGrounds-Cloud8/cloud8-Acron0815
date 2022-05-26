# EBS

## Elastic Block Store (EBS)

Amazon EBS (Elastic Block Store) is a cloud-based block storage system provided by Amazon Web Services (AWS) and is best suited for storing data that is not normally accessed and rarely modified.

## Key terminology

### EBS Provisioned IOPS SSD (io1) 
- Offers high IOPS per volume and high maximum throughput per volume, ideal for database workloads.

### EBS General Purpose SSD (gp2) 
- The standard EBS volume. Offers high IOPS per volume but at a lower rate and cost than io1 and is intended for dev test workloads, virtual desktops and low latency applications.

### Throughput Optimized HDD (st1) 
- Offers high throughput per volume and large volume size and is ideal for data warehouses and log processing.

### Cold HDD (sc1) 
- Is intended for workloads that are accessed less frequently, and offers the lowest IOPS per volume at the lowest price of any EBS volume.

### IOPS 
- Short for Input/Output Operations Per Second, is a measure of the performance of storage media such as hard drives.

## Sources

[What is AWS EBS?](https://intellipaat.com/blog/what-is-aws-ebs-in-amazon/)

[AWS EBS - Elastic Block Store Essentials](https://www.w3schools.com/aws/aws_cloudessentials_awsebs.php)

[Ultimate Amazon EC2 (Elastic Compute Cloud) & EBS (Elastic Block Store) Guide](https://letmetechyou.com/ultimate-amazon-ec2-elastic-compute-cloud-ebs-elastic-block-store-guide/)

[DevCon Linux Basics](https://devconnected.com/category/linux-administration/basics/)

[Amazon EBS (Elastic Block Store)](https://www.computerweekly.com/de/definition/Amazon-EBS-Elastic-Block-Store#:~:text=Amazon%20Elastic%20Block%20Store%20ist,die%20Speicherung%20persistenter%20Daten%20eignet.)

[YouTube Video: AWS EBS Storage Tutorial For Beginners](https://www.youtube.com/watch?v=j_hiz9-kbeY)
Tip! Watch with
subtitles...

[YouTube Video: Amazon EBS Explained](https://www.youtube.com/watch?v=_edxeLGnJpg)


## Exercise 1
- Navigate to the EC2 menu.

- Create a t2.micro Amazon Linux 2 machine with all the default settings.

- Create a new EBS volume with the following requirements:

  Volume type: General Purpose SSD (gp3)

  Size: 1 GiB

  Availability Zone: same as your EC2


- Wait for its state to be available.

  
### Navigate to the EC2 menu.
![Navigate](../00_includes/AWS-07%20EBS/Exercise-1-1-Navigate.PNG)

### Create a t2.micro Amazon Linux 2 machine with all the default settings.

![Create a t2.micro](../00_includes/AWS-07%20EBS/Exercise-1-2-Create-a-t2.micro.PNG)

### Create a new EBS volume with the following requirements:
- Volume type: General Purpose SSD (gp3)

- Size: 1 GiB

-  Availability Zone: same as your EC2

- Wait for its state to be available.

![Create EBS en wait for the state](../00_includes/AWS-07%20EBS/Exercise-1-3en4-Create-a-new-EBS.PNG)



## Exercise 2
- Attach your new EBS volume to your EC2 instance.

- Connect to your EC2 instance using SSH.

- Mount the EBS volume on your instance.

- Create a text file and write it to the mounted EBS volume.



![Attach your new EBS](../00_includes/AWS-07%20EBS/Exercise-2-1-Attache-your-new-EBS-volume.PNG)

![Connt-Mout](../00_includes/AWS-07%20EBS/Exercise-2-2-3.PNG)

![TXT](../00_includes/AWS-07%20EBS/Knipsel.PNG)



## Exercise 3
- Create a snapshot of your EBS volume.

- Remove the text file from your original EBS volume.

- Create a new volume using your snapshot.

- Detach your original EBS volume.

- Attach the new volume to your EC2 and mount it.

- Find your text file on the new EBS volume.

![Snapshot](../00_includes/AWS-07%20EBS/Knipsel3.PNG)

![Mountpoint](../00_includes/AWS-07%20EBS/Knipsel2.PNG)

