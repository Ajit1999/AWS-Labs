## Lab01 Configure and Launch a simple Linux EC2 instance

1.	Login to AWS console
2.	Select EC2 service
•	Go to Instances
•	Click on Launch Instance
•	Launch an instance
		Instance name
		ChooseAMI - Amazon Linux (free tier)
		Instance type – t2.micro
		Select key pair
		Network setting – Create security group
			 Allow SSH, HTTP, HTTPS traffic
		Launch Instance
		
•	back to EC2 dashboard and select the Instance.
•	Verify Instance state – Running & Status check – 2/2 checks passed
•	Click on Connect
•	Use Aws direct Connect or ssh client eg. MobaXterm to connect with Instance

You should now be logged into the EC2 linux instance!

