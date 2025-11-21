# Basic Web Server on EC2

## Project Overview
Built a simple web server on an AWS EC2 instance to learn about:
- EC2 instance management
- Security groups
- Basic server configuration
- Budgeting alerts (zero spend, custom $10 budget with a alert at 50%)
- Getting familiar with a similar service (Amplify)

## What I Built
A simple web server environment. Placed an EC2 instance in a public subnet accessible from the internet, installed Apache HTTP Server using a script. The page displayed "It works!". Also deployed a AWS Amplify serverless static website as an alternative approach to EC2.

## Steps Taken
1. Made a VPC
2. Made a EC2 instance:
    - Selected AMI: `Amazon Linux 2023`
    - Instance Type: `t3.micro`
    - Key Pair: `No key` SSH not needed for this project
    - configure security group to only allow HTTP (port 80)
    - User Data script so it would install Apache HTTP server on startup.
    - Script i used:
        ```
            #!/bin/bash
            yum update -y
            yum install -y httpd
            systemctl start httpd
        ```
    - Displayed a simple "it works!" page
3. Made a Amplify App
    - uploaded pre-prepared HTML files.

## AWS Services Used
- EC2 (t3.micro - free tier)
- VPC
- Amplify
- AWS Budgets
  
## What I Learned
- How to make a VPC
- How to launch and configure EC2 instances
- How to make a Amplify App
- How to make budgeting alerts
- Always terminate instances when done
- There are multiple ways to achieve one goal
- Its important to select appropriate services according to requirements

## Resource Cleanup
- ✅ EC2 Instance terminated
- ✅ VPC deleted
- ✅ Amplify App deleted

## Screenshots

### VPC Dashboard
![VPC Dashboard](screenshots/vpc-dashboard.png)

### EC2 Instance Dashboard  
![EC2 Dashboard](screenshots/ec2-dashboard.png)
*EC2 instance running with Apache HTTP server*

### Apache "It Works!" Page
![It Works Page](screenshots/it-works.png)
*Default Apache page confirming successful server deployment*

### Amplify Dashboard
![Amplify Dashboard](screenshots/amplify-overview.png)

### Amplify "Hello World" Page
![Hello World Page](screenshots/amplify-page.png)
*Static website hosted with Amplify, demonstrating a serverless alternative to EC2*

## Date
November 19, 2025
