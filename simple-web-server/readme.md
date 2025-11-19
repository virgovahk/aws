# Basic Web Server on EC2

## Project Overview
Built a simple web server on an AWS EC2 instance to learn about:
- EC2 instance management
- Security groups
- Basic server configuration

## What I Built
A simple web server environment. Placed an EC2 instance in a public subnet accessible from the internet, installed Apache HTTP Server using a script. The page displayed "It works!".

## Steps Taken
1. Made a VPC
2. Made a EC2 instance.
    - Selected AMI: `Amazon Linux 2023`
    - Instance Type: `t3.micro`
    - Key Pair: `No key` to only allow HTTP
    - confgure security group to only allow HTTP (port 80)
    - User Data script so it would install Apache HTTP server on startup.
    script i used:
        ```#!/bin/bash
            yum update -y
            yum install -y https
            systemctl start https

4. Installed Node.js/Apache/Nginx (whatever you used)
5. Deployed simple "Hello World" page

## AWS Services Used
- EC2 (t3.micro - free tier)
- VPC
- Security Groups

## What I Learned
- How to launch and configure EC2 instances
- Security group configuration is critical
- Always terminate instances when done!

## Resource Cleanup
✅ EC2 Instance terminated
✅ VPC deleted


## Date
November 19, 2025