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
![architecture](https://github.com/DelaDoreen/CIL-Academy_CFN/assets/142509085/51cd39f8-b36d-4ba5-80cd-6b6644eada11)

# AWS CloudFormation
<img width="700" alt="CFN" src="https://github.com/DelaDoreen/CIL-Academy_CFN/assets/142509085/4306d2e9-29d6-4890-bfbd-695561efe7bb">

# Resources created by CloudFormation stack
<img width="695" alt="Resources created with CFN" src="https://github.com/DelaDoreen/CIL-Academy_CFN/assets/142509085/7c10c29b-f424-4b1a-a138-6333d2dcd54c">

# Python Script
<img width="545" alt="Python script" src="https://github.com/DelaDoreen/CIL-Academy_CFN/assets/142509085/f59822b4-1ce7-4dbc-ab3d-00ca25d0cd9b">

# Cronjob
<img width="355" alt="Cronjob" src="https://github.com/DelaDoreen/CIL-Academy_CFN/assets/142509085/3fad8b6d-999c-4234-97cf-74281ab51afe">

# Challenges Encountered
* Understanding CloudFormation was daunting in the beginning, but with extensive research and collaboration, I was able to grasp the concept and implement it.
* I encountered a challenge when I had to run the crontab. I needed to run "which python" to establish the path to my Python interpreter.  







