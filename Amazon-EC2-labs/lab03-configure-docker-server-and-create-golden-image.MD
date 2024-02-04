## Lab 3 : Install the Docker in EC2 instance and create a golden image from it

•	Launch an instance
		AMI – Amazon Linux
		Instance type – t2.micro (free tier)
•	back to EC2 dashboard and select the Instance.
•	Verify Instance state – Running & Status check – 2/2 checks passed
•	connect with Instance

Commands used to install docker on AWS EC2 Instance

- Update the system

```console
sudo yum update
```
- Install Docker

```console
docker info
sudo yum install docker
```
- Start Docker

```console
sudo service docker start
sudo usermod -aG docker ec2-user
sudo service docker start
docker info 
```
- If error still remains then  reinstall docker

```console
sudo yum install docker
sudo reboot
docker info
sudo service docker start
docker info 
```

# Create an Image

•	Select your instance, and then choose
•	 Actions  Image and templates Create Image.
•	In the Create Image dialog box, specify the following information, and then choose Create Image.
		Image name – A unique name for the image.
		Image description – An optional description of the Image
		No reboot – This option is not selected by default. Amazon EC2 shuts down the instance, takes snapshots of any attached volumes, creates and registers the AMI, and then reboots the instance. Select No reboot to avoid having your instance shut down.
•	To view the status of your AMI while it is being created, in the navigation pane, choose AMIs. Initially, the status is pending but should change to available after a few minutes.

We just created a golden image that we can now use to launch more instances. 
A golden image is , in simple terms an image that you have customized to with liking with data/configuration of your choice. It's saved as a personal AMI from which you can launch instances.
 
