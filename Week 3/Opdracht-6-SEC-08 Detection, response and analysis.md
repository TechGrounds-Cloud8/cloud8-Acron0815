# Detection,response and analysis


## Key terminology

- 0.- Malware (malicious software)

- 1.- Detection 

- 2.- Response

- 3.- Analysis phase

- 4.- IDS (Intrusion detection systems)

- 5.- IPS (Intrusion prevention systems)

- 6.- Disaster recovery plan

- 7.- RPO (Recovery Point Objective)

- 8.- RTO (Recovery Time Objective)


- ### Malware (malicious software)
Malware is an umbrella term for any type of "malicious software" designed to infiltrate your device without your knowledge. There are many types of malware, and each uses different methods to achieve its goal. However, all malware variants share two key characteristics: they are insidious and aim to harm you.

- ### Detection
In this phase you detecting a attempted attack. Detecting an (attempted) attack is the first step to stopping an attack and to preventing future attempts.
Cyber ​​criminals try to smuggle malware onto a system as unnoticed as possible. If you suspect that something is wrong - e.g. e-mails are being sent in your name - first scan your device with an up-to-date virus protection program. In any case, you should subject your system to a thorough check.

- ### Response
If an incident is detected, a quick and effective response must be taken.
The first thing to do in response to a detected attack is trying to contain the damage.The way you do this (depending on the kind of attack) might differ. After the attack is contained, you can try to figure out the root cause of the attack, so that you can stop it.


## Exercise 1

A Company makes daily backups of their database. The database is automatically recovered when a failure happens using the most recent available backup. The recovery happens on a different physical machine than the original database, and the entire process takes about 15 minutes. What is the RPO of the database?

- The Company makes daily backups (they backup every 24 hours)
The RPO is 24 ours, in the worst-case they will lose 24 hours of data.

## Exercise 2

An automatic failover to a backup web server has been configured for a website. Because the backup has to be powered on first and has to pull the newest version of the website from GitHub, the process takes about 8 minutes. What is the RTO of the website?

- The RTO for the site is 8 minutes, 8 minutes is the time needed to start up again the newest version from GitHub.