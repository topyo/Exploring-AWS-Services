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
2. Search for EC2 in the management console

Make sure you are in US East (N. Virginia) us-east-1 Region.
![](Images/AWS13.png)


## 2.  Launching an EC2 Instance
![](Images/AWS14.png)
![](Images/AWS15.png)
![](Images/AWS16.png)
Key Pair : Create a new key pair, enter EC2Key, click on , and store it on your local machine.
![](Images/AWS17.png)
Launch Status: THE instance is now launching, Click on the instance ID and wait for complete initialization of instance till status change to Running.
![](Images/AWS17.png)

3. SSH into EC2

You can SSH into the EC2 instance by following the steps
<a href="https://play.whizlabs.com/site/task_support/ssh-into-ec-instance"> here </a>


I will SSH into EC2 using Microsoft  windows and below are the steps I completed

1. Downloaded putty and putty gen from

<a href="https://putty.org/"> here!</a>
2. Converted key pair .pem to .ppk:
  a. Opened  puttygen
  b. Clicked on Load
  c. Clicked  on All files to show the .pem file and selected the .pem keypair file.
 I recieved a success message that the conversion was successful.

![](Images/AWS19.png)

d. Clicked on the Save Private Key button and enter the keypairname and saved.
The keypairname.ppk file was  saved to my local machine.
![](Images/AWS20.png)
![](Images/AWS21.png)
![](Images/AWS22.png)
![](Images/AWS23.png)
![](Images/AWS24.png)

## 4.Install an Apache Server
To install an Apache Server, the following steps was completed
a. Switch to root user: sudo su
b. Run an updates using the following command:
yum -y update
c. Once updates are completed, I installed and ran apache server with the command:
 yum install httpd
When prompted, typed "Y" to confirm. Started the web server with the command
systemctl start httpd
and enabled the httpd using the command
systemctl enable httpd
 Checked the webserver status with:
 systemctl status httpd

![](Images/AWS25.png)
![](Images/AWS26.png)
![](Images/AWS27.png)
![](Images/AWS28.png)


You can test that your web server is properly installed and started by entering the public IP address of your EC2 instance in the address bar of a web browser. If your web server is running, then you see the Apache test page. If you don't see the Apache test page, then verify whether you followed the above steps properly and check your inbound rules for the security group that you created

![](Images/AWS30.png)
![](Images/AWS31.png)

5. Create and publish page

Navigate to the HTML folder where we will create an HTML page to test.
 cd /var/www/html/
Create a sample test.html file using nano editor:
nano test.html

3. Enter sample HTML content provided below in the file and save the file with Ctrl+X and press "y" to confirm the save. Then press "Enter" to confirm the file name.
<HTML> Welcome to My Quad Page! We are Live!!! </HTML>
![](Images/AWS29.png)
4. Restart the webserver by using the following command:
 systemctl start httpd
5. Now enter the file name after the public IP which you got when you created the ec2 instance in the browser, and you can see your HTML content.
 Sample URL: http://52.90.196.54/test.html

![](Images/AWS32.png)
6. If you can see the above text in the browser, then you have successfully completed the Project

## Allocating Elastic IP and Associating it to EC2 Instance

![](Images/AWS33.png)

Thanks for viewing this page!
