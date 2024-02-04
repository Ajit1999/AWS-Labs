

## Lab 05 : Host your personal site on AWS EC2 Instance

•	Launch an instance
		AMI – Amazon Linux
		Instance type – t2.micro (free tier)
•	back to EC2 dashboard and select the Instance.
•	Verify Instance state – Running & Status check – 2/2 checks passed
•	connect with Instance

Use following Linux Command . 
```console
sudo su – 
yum update -y
yum install -y httpd
systemctl status httpd 
mkdir temp 
cd temp 
wget https://www.free-css.com/assets/files... 
unzip complex.zip 
cd complex 
ls -lrt 
mv * /var/www/html 
systemctl enable httpd 
systemctl start httpd

```

