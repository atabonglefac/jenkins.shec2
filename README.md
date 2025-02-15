# Jenkins Installations Process
testing

We will describe the process using scripts for install Jenkins.

## Description

- Install Jenkins in __Centos 7__ Using Vagrant Provision
- Install Jenkins in __AWS EC2__ using __EC2 Red Hat Enterprise__

## Getting Started

### Dependencies

+ prerequisites:
    * Know how to create an EC2 Instances (__EC2 Red Hat Enterprise__)
    * Know how remote connexion using __ssh command__
    * Know remote copy using __scp__

Note: for all config, please change my ip address and put your own

### A- Installing Jenkins in Centos 7 using vagrant
1. enter in the __vagrant_jenkins__ folder (in there you have 2 files)
2. make the __vagrant up__ command
3. after some minutes, copy __192.168.56.37:8080__ and paste in you're favorite browser

```bash
cd vagrant_jenkins
vagrant up
```

### A- Installing Jenkins AWS EC2 using Red Hat Enterprise
1. open you're AWS account then creat and Instance
2. make a copy (__using scp__) of the __jenkins_ec2__ folder to this EC2 instance that have created
3. connect you in you're EC2 instance and enter in this folder 
4. make the __bash__ command using the __install_jenkins_ec2.sh__ file like argument
3. after some minutes, copy __your_public_ip_address:8080__ and paste in you're favorite browser
#### then continue the UI interface config of jenkins 

```bash
cd C:\Users\hermann90\Downloads\

scp -i jenkins_keys.pem -r jenkins_ec2 ec2-user@54.161.173.21:/home/ec2-user/
ssh -i "jenkins_keys.pem" ec2-user@ec2-54-161-173-21.compute-1.amazonaws.com 
cd jenkins_ec2
sudo bash install_jenkins_ec2.sh
```

## Help

open the ticket for any issues, describe you issues and let some Utrains member can helpe

## Authors

Utrains Teams.

## Version History

* 1.0 : test and approve

## License

This project is licensed under the __Utrains__ License. you can use it only as a student at Utrains.
