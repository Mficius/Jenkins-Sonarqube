# Jenkins-Sonarqube

Installation of Jenkins on Ubuntu EC2

Connect to Ec2 instance and enter this command:

sudo apt install openjdk-11-jre

Enter this command

sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins


INSTALL SONARQUBE ON EC2 instance

Connect to Sonarqube instance and: 

sudo hostnamectl set-hostname sonarqube
sudo apt install openjdk-17-jre

wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.3.0.82913.zip

sudo apt install unzip

unzip sonarqube-10.3.0.82913.zip

cd sonarqube-10.3.0.82913/bin/linux-x86-64/

./sonar.sh

