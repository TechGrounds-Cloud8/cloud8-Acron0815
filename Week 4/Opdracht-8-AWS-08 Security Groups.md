# Cron jobs

## Key terminology

### - CronTab

Cron uses special configuration files called Cron Tab files that contain a list of jobs to run.

CronTab stands for Cron Table.

Each line in the Cron Tab file is called a CronJob.

## What is a Cron job?


" A Cron Job running a system service is called a daemon (background process) "

The Cron-Daemon runs in the background of the system and gives time impulses so that automated tasks (jobs) are executed at specified times. Cron Jobs are recurring tasks that are automated as resource-saving as possible.

## Each CronJob consists of three components:

- Script to run
- Command that runs the script periodically
- Action or output of the script

## Possible uses of Cron Jobs.

Cron Jobs can be used for individual commands or for the automated execution of periodically recurring and sequential commands.

A practical example of use:

Sending my Newsletter to Abdeslam, Archana, Aurèl, Ben, Casper, Ismail, Killian, Patrick, Quincy, Rolf, Shikha, Tom and to kscheng (whoever that is).

The most common area of ​​application for CronJobs is data backup. 

For example, if you want to create a backup at regular intervals to archive data, CronJobs are ideal for this. The cleaning of databases and the processing of visitor statistics on websites are also typical areas of application for CronJobs.
