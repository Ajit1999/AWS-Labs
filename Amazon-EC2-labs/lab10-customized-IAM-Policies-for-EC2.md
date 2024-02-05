EC2 Instance permissions with IAM Role

Step 1:
•	Launch Ubuntu Instance
•	Connect 
•	Install mysql server on it
•	Create Database

Step 2 : 
•	Go to IAM Dashboard
•	Click on Policies in the left navigation pane
•	Create Policies -  JSON
•	Write Policies

```console
{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Effect": "Allow",
			"Action": [
				"ec2:DescribeInstances",
				"ec2:DescribeInstanceStatus",
				"ec2:DescribeSecurityGroups"
			],
			"Resource": "*"
		},
		{
			"Effect": "Allow",
			"Action": [
				"ec2:RunInstances",
				"ec2:TerminateInstances",
				"ec2:StartInstances",
				"ec2:StopInstances"
			],
			"Resource": "arn:aws:ec2:Region:Root_account_id:instance/Instance_id"
		},
		{
			"Effect": "Allow",
			"Action": "ec2-instance-connect:SendSSHPublicKey",
			"Resource": [
				"Resource": "arn:aws:ec2:Region:Root_account_id:instance/Instance_id",
				"arn:aws:ec2:Region:Root_account_id:key-pair/Key_pair_name"
			]
		}
	]
}
```

•	Add Policies details & create policies

Step 3:
•	Create IAM User & attach customer managed policies to them.

Step 4:
•	Login into IAM User
•	Go to EC2 Dashboard
•	Connect with Instance

-	Check the Status of MySql (Active or Inactive) 
```console
sudo systemctl status mysql
```
- Login into SQL
```console
mysql -u root -p
```
- Access Database
```console
use test;

select * from table1;
```

