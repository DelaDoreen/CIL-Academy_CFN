# Description
This project contains an AWS infrastructure that employs CloudFormation for stack creation. This process triggers the deployment of an EC2 instance ( t2.micro), running the Amazon Linux 2 AMI, along with the provisioning of an S3 bucket.

# Project Details
* Create a CloudFormation (CFN) Stack that launches a t2.micro EC2 instance (Amazon Linux 2 AMI) and an S3 bucket.
* Assign a role to the EC2 instance to access it via Amazon Systems Manager (SSM) rather than SSH with key-pairs.
* Set up the EC2 instance to act as a backup for images uploaded to the S3 bucket. The backup should be done to a folder /home/user/mys3backup.
* Write a Python Script that copies the S3 content to the backup directory on execution.
* Set up a cronjob that runs the Python script at least once daily at any time of choice.


# Project Stages

* The CloudFormation template is used to create the stack, which then triggers the deployment of the specified resources, the EC2 and S3 Bucket.
* Some images and files are then uploaded into the S3 bucket that was deployed earlier.
* The Python script is then used to download the images and files from the S3 Bucket into the EC2 Instance, which acts as backup storage. 
* Then comes the cronjob, which is used to schedule the time the backups will occur.
   
# Architecture
![architecture](https://github.com/DelaDoreen/CIL-Academy_CFN/assets/142509085/f9a7a32b-7738-4375-8372-7b5792decdc8)
 


# AWS CloudFormation


# Resources created by CloudFormation stack


# Python Script


# Cronjob


# Challenges Encountered
* Understanding CloudFormation was daunting in the beginning, but with extensive research and collaboration, I was able to grasp the concept and implement it.
* I encountered a challenge when I had to run the crontab. I needed to run "which python" to establish the path to my Python interpreter.  







