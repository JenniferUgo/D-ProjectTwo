# LEMP STACK IMPLEMENTATION DOCUMENTATION
## First we set up a LEMP STACK using EC2
## We start by creating an account on AWS.


1. Start by creating an instance (virtual machine) by selecting “ubuntu server 20.04 LTS” from Amazon Machine Image(AMI)(free tier).
2. Then select “t2.micro”, go to the security group and select “an existing security group” review and launch instance.

### This launches the instnce and takes you to the Instances dashboard

![lemp instance](./images/LEMP-instance.png)

3. Then open a terminal on your system and enter the folder where your previously downloaded PEM file is located.

### In this case we use the Git Bash Terminal
![terminal](./images/gitbash-terminal.png)

4. Connect to the instance from ubuntu terminal using this command:
>`ssh -i "Jennee-EC2.pem" ubuntu@ec2-18-130-68-79.eu-west-2.compute.amazonaws.com`

![connect with ssh](./images/Instance-ubuntu-connect-ssh.png)


### This automatically connects to the instance when you click Enter
![connect to instance](./images/connect-to-instance.png)

## Step 1 – Installing the Nginx Web Server
### Install the Nginx Web Server, to display web pages to site visitors.

### We first update the server's package, before we download the nginx web server, using thsis command:
>`sudo apt update`

![update server's package](./images/update-package-server.png)

### Then install Nginx with this command:
>`sudo apt install nginx`
![installing nginx](./images/nginx-installation.png)

### Verify that nginx was successfully installed and is running as a service in Ubuntu, using this command:
>`sudo systemctl status nginx`

### if it's green and says "active (running)", then it was successfully installed. Like so:
![verify it's successful](./images/verify-nginx-is-running.png)

### Test how our Nginx server can respond to requests from the Internet.
### Open a web browser of your choice and try to access following url run:
>`http://<Public-IP-Address>:80`

![test nginx on webserver](./images/welcome-to-nginx.png)



