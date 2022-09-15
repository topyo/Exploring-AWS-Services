# Exploring-AWS-Services
This project aims at documenting the capabilities of different AWS Services (Architecting in the Cloud)
Introduction



To explore the AWS Services, you will need an AWS Account. You can create an account by using the <a href="https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all">link</a>. You can also watch this video

<a href="https://www.youtube.com/watch?v=KkWQuSwuGFc">video</a>

For this project, I will be using Amazon free tire account. Before you a free tier account, please note the following free tier account conditions:
1. Amazon Elastic Cloud computer EC2 Linux t2.micro 750Hours per month
2.  750 Hours t2.micro windows instance per month
3. 2000 Put requests of Amazon S3 (single PUT Request max 5GB)
4.  20000 Get requests of Amazon S3 (Each request Get request)
5. Amazon RDS MySQL DB instance with t2.micro 5GB storage
6. MSSQL Express version t2.micro with 20GB GP-SSD Free
Also, note that you will need the following in order to create a free tier Account:

Email address

Telephone number


Credit card

The credit card will not be charged for usage below AWS Free Tier limits. AWS will temporarily hold $1 USD/EUR as a pending transaction for 3-5 days for identity verification.
Below are the snapshots of how I created mine
1. Clicked on this <a href="https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all">URL</a>.

2. Clicked on

![](Images/AW1.png)


3. Entered my details into
![](Images/AW2.png)
and clicked verify email address

4. Confirmed my identity
![](Images/aw3.png)
 and completed all other steps as required by AWS. Since I have an AWS Account, I recieved the below message from AWS

![](Images/AWS4.png)

We will start this project by Setting a billing alert .
To create a billing alarm using the CloudWatch on the console

1. On the search tab, you type CloudWatch and select CloudWatch on Services

![](Images/AWS5.png)

2. If necessary, change the region to US East (N. Virginia). However, the billing metric data is stored in US East(N. Virginia) and it  represent the worldwide charges.
![](Images/AWS6.png)

2. On the CloudWatch dashboard, under Alarms, click Billing and then  Create Alarm.

![](Images/AWS7.png)
3. Specify metric and conditions
![](Images/AWS8.png)

4. Configure actions
** Errors to note
a. Select new topic and while creating a new topic names, spaces are not allowed

![](Images/E1.png)

![](Images/AWS9.png)


5. Add name and description
![](Images/AWS10.png)

6. Preview and create
![](Images/AWS11.png)

![](Images/AWS12.png)

Now that we have set the billing alert, let us get our hand dirty by launching Amazon Elastic Compute Cloud (EC2) and installing an Apache Server

#### Project Objective
This project shows how to launch and configure a virtual machine on Amazon cloud. The AWS region is US East (N. Virginia) us-east-1
### Introduction
What is EC2?
Amazon Elastic Compute Cloud (Amazon EC2) offers the broadest and deepest compute platform, with over 500 instances and choice of the latest processor, storage, networking, operating system, and purchase model to help you best match the needs of your workload.

### Project steps
## 1. launch the Lab Environment
Tasks:
1.  Login to AWS Management Console
2. Click on the AWS Management Console


## 2.  Launching an EC2 Instance



3. SSH into EC2 Instance
4. Install an Apache Server
5. Create and publish page
6. Validation of the lab
