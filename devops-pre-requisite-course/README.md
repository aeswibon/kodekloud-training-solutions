# DevOps Pre Requisite course

## Introduction

As a DevOps or Cloud Engineer it is important to have these basics cleared. And that’s why we built this course to bridge that gap. With this course anyone can kick start their DevOps or Cloud Journey. This is the course you must take before you start with any of the DevOps or Cloud courses out there. This course helps you get your basics right, so the rest of the journey is smooth.

To view this course, click the following [link](https://kodekloud.com/courses/devops-pre-requisite-course/)

## Contents

1. Introduction
2. Lab Setup
3. Linux Basics
4. Networking Basics
5. Application Basics
6. Source Control Management (SCM)
7. Web Server
8. Database Basics
9. Security
10. General Pre-Requisites
11. 2 Tier Application
12. Conclusion

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
