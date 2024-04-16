# Jenkins

## Introduction

In this course, you will learn with demos at each step for better visualization of the concepts about what CI/CD is, why we should use Jenkins, how to create pipelines, use of different plugins, Jenkins security and much more along with the hands-on practice for these concepts to give you a solid foundation of Jenkins.

To view this course, click the following [link](https://kodekloud.com/courses/jenkins/)

## Contents

1. Installing Jenkins

### Installing Jenkins

To install Jenkins, first we need to install the java. Currently using `Java 11`. We can install it by the following command: `sudo yum install -y java-11-openjdk` \
After which, we need to add the jenkins repo, and then install jenkins application. Follow the following steps:

```bash
# install extra release package
sudo yum install -y epel-release
# Adding jenkins repository
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
# Adding key
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
# install the jenkins
sudo yum install -y jenkins
# update the service file
sudo vi /lib/systemd/system/jenkins.service
# now update Environment="JENKINS_PORT=8090"
# Now start the jenkins service
sudo systemctl start jenkins
# to get the admin password
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
