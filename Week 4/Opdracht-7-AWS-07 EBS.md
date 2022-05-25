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

