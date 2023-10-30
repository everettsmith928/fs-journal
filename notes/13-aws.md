October 30th 2023

Hosting our own portfolios and servers

AWS & Remote MYSQL

Setting up an EC2 instance

security group rule ADD MYSQL / AURORA at port 3306 protocol TCP

once launched connect with ssh -i '~/source/aws/filename.pem' ubuntu@ipaddress

apt - install for linux
sudo apt update
sudo apt upgrade

rebooting on a ubuntu

sudo systemctl enable mysql
sudo systemctl status

mysql> this shows that you are in the mysql instance on the ubuntu

ALTER USER 'root'@'local'

if you have something that runs it has a .d in the configure file

sudo nano = text editor mysqld.cnf

change bind address - 

^LETTER this is control for commands

connection is our public IP address on the AWS host port-3306
username - whatever we setup in the linux 'banana'
