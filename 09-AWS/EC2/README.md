Point: Create an EC2 instance from scratch...

Amazon Elastic Compute Cloud (EC2)
Creat

Launch instance
To get started, launch an Amazon EC2 instance, which is a virtual server in the cloud.

Launch instance     > just click on button..

inside instance 


.Launch an instance  Info
Amazon EC2 allows you to create virtual machines, or instances, that run on the AWS Cloud. Quickly get started by following the simple steps below.

Name and tags  Info
Name

just enter your EC2 name ( ex. hello instance)

.Application and OS Images (Amazon Machine Image)

chose your ami which is using by EC2 for operate with OS    point > check free tier eligible

ex. of demo detail 

Description
Amazon Linux 2023 (kernel-6.18) is a modern, general purpose Linux-based OS that will be supported until June 2029. It is optimized for AWS and designed to provide a secure, stable and high-performance execution environment to develop and run your cloud applications.

Amazon Linux 2023 AMI 2023.12.20260727.0 x86_64 HVM kernel-6.18
Architecture

64-bit (x86)
Boot mode
uefi-preferred

AMI ID
ami-0cc0615fa97a31072
Creation Date
2026-07-25
Username
ec2-user

. now next step is select instance type but agine check free tier eligible of Instance type 


. Key pair (login)  

create for login it's initial using form of key value pair 


. Network settings  Info  this is an Demo 
Edit
Network
 Info
vpc-0086f9c6e2ca18947

Subnet
 Info
No preference (Default subnet in any availability zone)

Auto-assign public IP
 Info
Enable

Firewall (security groups)
 Info
A security group is a set of firewall rules that control the traffic for your instance. Add rules to allow specific traffic to reach your instance.
Create security group
Select existing security group
We'll create a new security group called 'launch-wizard-1' with the following rules:
Allow SSH traffic from
Helps you connect to your instance

Anywhere
0.0.0.0/0
Allow HTTPS traffic from the internet
To set up an endpoint, for example when creating a web server
Allow HTTP traffic from the internet
To set up an endpoint, for example when creating a web server

always enable http and https for access you website and web applictions

Notice :- Rules with source of 0.0.0.0/0 allow all IP addresses to access your instance. We recommend setting security group rules to allow access from known IP addresses only.


. Configure storage  Info
Advanced
1x
8
GiB

gp3
Root volume,
3000 IOPS,
Not encrypted
Add new volume
Click refresh to view backup information
The tags that you assign determine whether the instance will be backed up by any Data Lifecycle Manager policies.

File systems
S3 Files - new
EFS
FSx
None  this is default selected so choice is your to selete between them 


if you want to add aditional or advanced details so move inside but this is simple EC2 instance launch 

. Summary
Number of instances
 Info
1
Software Image (AMI)
Amazon Linux 2023 AMI 2023.12....read more
ami-0cc0615fa97a31072
Virtual server type (instance type)
t3.micro
Firewall (security group)
New security group
Storage (volumes)
1 volume(s) - 8 GiB

just click on Launch instance....

also check ✔️  number of instance 


Cancel         Launch instance
