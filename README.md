#CUSTOM-AMI#

Welcome to the Custom-AMI wiki!

What is a custom AMI?

Is a template contains O.S and pre-configured tools[ex..linux and ubuntu] pre configured tools like Java,GIT and etc.
AMI's are used for launching EC2 instances.
Every AWS accounts have AMI managed accounts.
AWS offers its own AMI for launching and we can create our own custom images according to our requirements.
Server Patching.
We do it to keep server secure. Every 3 -6 months companies do server patching. We use Ansible or Chef to do server patching. Amazon is also have its own service called AWS SSM.

<h3>TOOLS USED IN THIS TASK ARE</h3>

1.AWS EC2 service.

2.AWS Amazon Linux image. 

3.Git & GitHub.

4.Apache server(httpd)

Create Custom Amazon Machine Image.
1.Launch EC2 instance by choosing existing image. 

2.Install Required tools on the instance.


a. For the sake of example i want to install and configure Apache Web Server.

3.SSH on to EC2 & install apache.

a. sudo yum install httpd -y 

b. To host a dummy web application place index.html file in the path /var/www/html/.

c. Sudo vi /var/www/html/index.html 

e. Enable apache server.

i.sudo systemctl enable httpd (This is used whenever server starts httpd automatically starts by itself.) 
ii. sudo systemctl start httpd. (This isto start httpd)
iii. sudo systemctl status httpd. (This is to know whether httpd started or not.)

<h3>Create </h3>

1.Select instance--> Actions -->Image and Templates-->Create Image -->Provide name.
2.Delete the instance with which we created AMI.

Launch EC2 Instance using that image.

EC2 dashboard --> AMI's --> Select AMI -->Launch instance from AMI.

