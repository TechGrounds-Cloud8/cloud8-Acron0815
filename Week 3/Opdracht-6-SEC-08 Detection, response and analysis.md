# Detection,response and analysis

![DRA](../00_includes/SEC-08%20Detection%2C%20response%20and%20analysis/Detection-Response.PNG)


## Key terminology

- 1.- Malware (malicious software)

- 2.- Detection 

- 3.- Response

- 4.- Analysis 

- 5.- IDS - Intrusion Detection Systems

- 6.- IPS - Intrusion Prevention Systems

- 7.- Disaster Recovery Plan

- 8.- RPO (Recovery Point Objective)

- 9.- RTO (Recovery Time Objective)

---


- ### 1.-Malware (malicious software)
Malware is an umbrella term for any type of "malicious software" designed to infiltrate your device without your knowledge. There are many types of malware, and each uses different methods to achieve its goal. However, all malware variants share two key characteristics: they are insidious and aim to harm you.

- ### 2.-Detection
In this phase you detecting a attempted attack. Detecting an (attempted) attack is the first step to stopping an attack and to preventing future attempts.
Cyber ​​criminals try to smuggle malware onto a system as unnoticed as possible. If you suspect that something is wrong - e.g. e-mails are being sent in your name - first scan your device with an up-to-date virus protection program. In any case, you should subject your system to a thorough check.

- ### 3.-Response
If an incident is detected, a quick and effective response must be taken.
The first thing to do in response to a detected attack is trying to contain the damage.The way you do this (depending on the kind of attack) might differ. After the attack is contained, you can try to figure out the root cause of the attack, so that you can stop it.

- ###  4.-Analysis phase
In this phase you analyse what has happened and you document what you learned and do the necessary thing to prevent this from rehappening.

- ### 5.-IDS - Intrusion Detection Systems
The Intrusion Detection System (IDS) is a monitoring system that detects suspicious activities and generates alerts when they are detected. Based upon these alerts, a security operations center (SOC) analyst or incident responder can investigate the issue and take the appropriate actions to remediate the threat.

- ### 6.-IPS - Intrusion Prevention Systems
The Intrusion Prevention System (IPS) is a network security tool (which can be a hardware device or software) that continuously monitors a network for malicious activity and takes action to prevent it, including reporting, blocking, or dropping it, when it does occur. It is more advanced than an intrusion detection system (IDS), which simply detects malicious activity but cannot take action against it beyond alerting an administrator.

- ### 7.-Disaster Recovery Plan
A Disaster recovery plans (DRP) seek to quickly redirect available resources into restoring data and information systems following a disaster. A disaster can be classified as a sudden event, including an accident or natural disaster, that creates wide scoping, detrimental damage. Response and analysis are part of the disaster plan.

- ### 8.-RPO (Recovery Point Objective)
A Recovery Point Objective (RPO) generally refers to the amount of data that can be lost within a period most relevant to a business, before significant harm occurs, from the point of a critical event to the most preceding backup.

- ### 9.-RTO (Recovery Time Objective)
A Recovery Time Objective (RTO) often refers to the quantity of time that an application, system and/or process, can be down for without causing significant damage to the business as well as the time spent restoring the application and its data.

---


## Exercise 1

A Company makes daily backups of their database. The database is automatically recovered when a failure happens using the most recent available backup. The recovery happens on a different physical machine than the original database, and the entire process takes about 15 minutes. What is the RPO of the database?

- The company creates daily backups (they back up every 24 hours).

  The RPO is 24 hours, in the worst case the company lost 24 hours of data.

## Exercise 2

An automatic failover to a backup web server has been configured for a website. Because the backup has to be powered on first and has to pull the newest version of the website from GitHub, the process takes about 8 minutes. What is the RTO of the website?

- The RTO for the site is 8 minutes, 8 minutes is the time needed to start up again the newest version from GitHub.

---


## Sources

[DEFINITIONS](https://www.kaspersky.com/resource-center/definitions/)

[Malware](https://www.paloaltonetworks.com/cyberpedia/what-is-malware)

[Malware protection](https://www.cisco.com/c/en/us/products/security/advanced-malware-protection/)

[IDS (intrusion detection system](https://www.barracuda.com/glossary/intrusion-detection-system)

[IDS vs. IPS: What is the Difference?](https://www.varonis.com/blog/ids-vs-ips)

[RPO and RTO: Understanding the Differences](https://www.enterprisestorageforum.com/management/rpo-and-rto-understanding-the-differences/)

[Secure The Network](https://www.checkpoint.com/cyber-hub/network-security/)

[Making the Connected World a Safer Place](https://www.cisecurity.org/insights/spotlight/)


[Different Types of Disaster Recovery Plans](https://sados.com/blog/types-of-disaster-recovery-plans/)

---

## Overcome challanges

### It was not easy to find and filter the large amount of information