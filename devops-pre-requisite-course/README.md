# DevOps Pre Requisite course

## Introduction

As a DevOps or Cloud Engineer it is important to have these basics cleared. And that’s why we built this course to bridge that gap. With this course anyone can kick start their DevOps or Cloud Journey. This is the course you must take before you start with any of the DevOps or Cloud courses out there. This course helps you get your basics right, so the rest of the journey is smooth.

To view this course, click the following [link](https://kodekloud.com/courses/devops-pre-requisite-course/)

## Contents

1. Networking Basics
2. Application Basics

### Networking Basics

To add the IP address for the different servers, run the follwing command in each app node:

For app01: `sudo ip addr add 172.16.238.15/24 dev eth0` \
For app02: `sudo ip addr add 172.16.238.16/24 dev eth0` \
For app03: `sudo ip addr add 172.16.239.15/24 dev eth0` \
For app04: `sudo ip addr add 172.16.239.16/24 dev eth0`

To get access to app node, use `ssh {name}` command. Like for app01, command would be `ssh app01`

To enable access to `app03` and `app04`, we need to add the network range to our host. \
This can be done by the following command: `sudo ip addr add 172.16.239.10/24 dev eth0`

To add the router so that the app node can ping each other, run the following in each app node:

For app01: `sudo ip route add 172.16.239.0/24 via 172.16.238.10` \
For app02: `sudo ip route add 172.16.239.0/24 via 172.16.238.10` \
For app03: `sudo ip route add 172.16.238.0/24 via 172.16.239.10` \
For app04: `sudo ip route add 172.16.238.0/24 via 172.16.239.10`

### Application Basics

To download `Java 20`, you can use the following command: `sudo curl https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz -o /opt/openjdk-20_linux-x64_bin.tar.gz`. \
Then you can just uncompress the file using the following command: `sudo tar -xf /opt/openjdk-20_linux-x64_bin.tar.gz -C /opt`.\
You can append the dir to path varible using the following command: `export PATH=$PATH:/opt/jdk-20/bin`
