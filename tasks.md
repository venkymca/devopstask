**Install Nginx on a server**


sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx


**Install Docker**


sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common -y
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo systemctl start docker
sudo systemctl enable docker

**Install Git**


sudo apt-get update
sudo apt-get install git -y

**Install Java (OpenJDK)**

sudo apt-get update
sudo apt-get install openjdk-11-jdk -y

**Install Python**


sudo apt-get update
sudo apt-get install python3 python3-pip -y

**Check Disk Space Usage**

df -h

**Monitor CPU Usage**


top


**Check System Load Average**


uptime

**List Running Processes**


ps aux

**Check Free Memory**


free -h

**Check for Available Updates**


sudo apt-get update
sudo apt-get upgrade -y

**Check System Logs**


tail -f /var/log/syslog

**Backup a Directory**


tar -czvf backup.tar.gz /path/to/directory

**Unzip a Tarball**


tar -xzvf backup.tar.gz

**Create a User**


sudo useradd -m username
sudo passwd username

**Delete a User**


sudo deluser username

**Change User Password**


sudo passwd username

**Create a New Directory**


mkdir /path/to/directory

**Delete a Directory**


rm -r /path/to/directory

**Check Running Services**


systemctl list-units --type=service

**Start a Service**


sudo systemctl start nginx

**Stop a Service**


sudo systemctl stop nginx

**Restart a Service**


sudo systemctl restart nginx

**Check the Status of a Service**


sudo systemctl status nginx

**Enable a Service on Boot**


sudo systemctl enable nginx

**Disable a Service on Boot**


sudo systemctl disable nginx

**Install Apache2**


sudo apt-get install apache2 -y

**Start Apache2**


sudo systemctl start apache2

**Stop Apache2**


sudo systemctl stop apache2

**Create a Cron Job**


crontab -e
# Add a line: 
0 0 * * * /path/to/script.sh

**Check Network Interface Configuration**


ifconfig

**Display Network Connections**


netstat -tuln

**Display Routing Table**


netstat -r

**Check Available Disk Space**


df -h

**Find Large Files**


find / -type f -size +100M

**Install MySQL**


sudo apt-get install mysql-server -y

Start MySQL


sudo systemctl start mysql
Stop MySQL


sudo systemctl stop mysql
Install PostgreSQL


sudo apt-get install postgresql postgresql-contrib -y
Start PostgreSQL


sudo systemctl start postgresql
Stop PostgreSQL


sudo systemctl stop postgresql
Install Redis


sudo apt-get install redis-server -y
Start Redis


sudo systemctl start redis
Stop Redis


sudo systemctl stop redis
Check for Zombie Processes


ps aux | grep 'Z'
Check the Last Login Time


last
Update a System


sudo apt-get update && sudo apt-get upgrade -y
Check System Information


uname -a
Monitor Memory Usage


free -m
Change Hostname


sudo hostnamectl set-hostname new-hostname
Install Node.js


sudo apt-get update
sudo apt-get install nodejs -y
sudo apt-get install npm -y
Install Ruby


sudo apt-get install ruby-full -y
Install Composer (PHP Dependency Manager)


curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
Check Available Ports


sudo lsof -i -P -n | grep LISTEN
Find Top 10 Largest Files in Directory


find . -type f -exec du -h {} + | sort -rh | head -n 10

Automate Server Reboot


sudo shutdown -r +10
Send Email from Terminal

bash
Copy
echo "Subject: Test" | sendmail youremail@example.com

Create a Backup of MySQL Database

bash
Copy
mysqldump -u username -p database_name > backup.sql
Restore MySQL Database from Backup


mysql -u username -p database_name < backup.sql
Install Kubernetes (kubeadm)


sudo apt-get update && sudo apt-get install -y apt-transport-https curl
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
sudo apt-get update
sudo apt-get install -y kubeadm

Check Kubernetes Cluster Nodes


kubectl get nodes
Set Up AWS CLI


pip install awscli
aws configure
Install Terraform


wget https://releases.hashicorp.com/terraform/1.0.0/terraform_1.0.0_linux_amd64.zip
unzip terraform_1.0.0_linux_amd64.zip
sudo mv terraform /usr/local/bin/
Deploy a Simple Docker Container


docker run -d -p 80:80 nginx
Check Docker Version


docker --version
List Docker Containers


docker ps
Stop a Docker Container


docker stop container_id
Start a Docker Container


docker start container_id
Remove a Docker Container


docker rm container_id
Build Docker Image


docker build -t my-image .
Push Docker Image to Docker Hub


docker login
docker push my-image
Run Docker Compose


docker-compose up
Install Jenkins


sudo apt-get update
sudo apt-get install openjdk-11-jdk
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian/jenkins.io.repo > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
Start Jenkins


sudo systemctl start jenkins
Get Jenkins Status


sudo systemctl status jenkins
Check Disk Usage


du -sh /path/to/directory
Generate SSH Key Pair


ssh-keygen -t rsa -b 4096 -f ~/.ssh/id_rsa
Copy SSH Key to Server


ssh-copy-id user@remote_server
Test SSH Connection


ssh user@remote_server
Create a Swap File


sudo dd if=/dev/zero of=/swapfile bs=1M count=2048
sudo mkswap /swapfile
sudo swapon /swapfile
Setup Firewall with UFW


sudo ufw enable
sudo ufw allow 22
sudo ufw allow 80
sudo ufw allow 443
Install Ansible


sudo apt-get install ansible -y
Run Ansible Playbook


ansible-playbook -i hosts my-playbook.yml
Generate SSL Certificate


openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout server.key -out server.crt
Monitor System Performance with htop


sudo apt-get install htop
htop
List All Installed Packages


dpkg --get-selections
Install VMware Tools


sudo apt-get install open-vm-tools
Create a System Snapshot


sudo rsync -a / /path/to/backup
Check Firewall Status


sudo ufw status
Enable SSL for Nginx


sudo apt-get install certbot python3-certbot-nginx
sudo certbot --nginx
Configure SSL in Apache


sudo a2enmod ssl
sudo service apache2 restart
Install Virtualenv


sudo apt-get install python3-venv
python3 -m venv myenv
Activate Virtualenv


source myenv/bin/activate
Install Dependencies in Virtualenv


pip install -r requirements.txt
Deploy Static Website Using Nginx


sudo cp -r /path/to/website/* /var/www/html/
sudo systemctl restart nginx
Set up SFTP


sudo apt-get install openssh-server
sudo systemctl enable ssh
Enable Apache Mod_Rewrite


sudo a2enmod rewrite
sudo systemctl restart apache2
Add SSH Key to Server


cat ~/.ssh/id_rsa.pub | ssh user@remote_server 'cat >> ~/.ssh/authorized_keys'
