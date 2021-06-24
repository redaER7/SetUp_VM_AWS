# Create VM on AWS
* [Go to Control Panel](#Go-to-Control-Panel)
* [Setup](#Setup)

Linux-Remote Server are Linux-based virtual machines (VMs) that run on top of virtualized hardware
VMs are managed using a terminal and SSH. You’ll need to have an SSH client and, optionally, an SSH key pair. Clients generally authenticate either using passwords (which are less secure and not recommended) or SSH keys (which are very secure and strongly recommended).
We recommend you use SSH keys to connect to your VM.

## Go to Control Panel
Create AWS account from https://aws.amazon.com/resources/create-account/

1.	Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/


## Setup
2.	Choose Launch Instance.
3.	In Step 1: Choose an Amazon Machine Image (AMI), find an Amazon Linux 2 AMI at the top of the list and choose Select.
4.	In Step 2: Choose an Instance Type, choose Next: Configure Instance Details.
5.	In Step 3: Configure Instance Details, provide the following information:
- Leave Number of instances at one.
- Leave Purchasing option at the default setting.
- For Network, choose the entry for the same VPC that you noted when you created your EFS file system in Step 1: Create your Amazon EFS file system.
- For Subnet, choose a default subnet in any Availability Zone.
- For File systems, make sure that the EFS file system that you created in Step 1: Create your Amazon EFS file system is selected. The path shown next to the file system ID is the mount point that the EC2 instance will use, which you can change.
- The User data automatically includes the commands for mounting your Amazon EFS file system.
6.	Choose Next: Add Storage.
7.	Choose Next: Add Tags.
8.	Name your instance and choose Next: Configure Security Group.
9.	In Step 6: Configure Security Group, set Assign a security group to Select an existing security group. Choose the default security group to make sure that it can access your EFS file system.
10.	Choose Review and Launch.
11.	Choose Launch.
12.	Select the check box for the key pair that you created, and then choose Launch Instances.

