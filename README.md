
\f0\fs24 \cf0 # AWS Cloud E-Commerce Platform (Capstone Project)\
\
## Overview\
\
This project demonstrates the design and deployment of a cloud-native e-commerce ordering system using Amazon Web Services (AWS). The system simulates a food distribution ordering platform where customers can place orders, choose delivery preferences, and track order status.\
\
The goal of the project was to demonstrate practical cloud architecture, networking configuration, containerized application deployment, and event-driven integration workflows.\
\
---\
\
## Architecture\
\
Main AWS services used:\
\
- Amazon ECS (Fargate)\
- Amazon RDS (MySQL)\
- Amazon EC2\
- Amazon VPC\
- Security Groups\
- Amazon SQS / SNS / EventBridge\
\
System Architecture Flow\
\
User  \
\uc0\u8595   \
Web Interface  \
\uc0\u8595   \
NGINX Web Server  \
\uc0\u8595   \
Amazon ECS Containerized API  \
\uc0\u8595   \
Amazon RDS MySQL Database\
\
Event Driven Flow\
\
Order Created  \
\uc0\u8595   \
API publishes event  \
\uc0\u8595   \
Amazon SQS Queue  \
\uc0\u8595   \
Inventory System (simulated)\
\
---\
\
## Features Implemented\
\
- Order placement system\
- Delivery customization\
- Pickup or delivery selection\
- Special instructions for delivery\
- Order status tracking\
- Event-driven order integration\
- Containerized API deployment\
- Cloud networking configuration\
\
---\
\
## Challenges Faced\
\
During development several infrastructure issues were encountered:\
\
- VPC networking configuration\
- Internet Gateway routing\
- ECS task security group misconfiguration\
- API connectivity failures due to blocked ports\
\
Resolving these issues required troubleshooting AWS networking and adjusting security group rules.\
\
---\
\
## Lessons Learned\
\
This project provided hands-on experience with:\
\
- Deploying containerized services on AWS ECS\
- Configuring VPC networking and security groups\
- Designing event-driven cloud systems\
- Troubleshooting cloud connectivity issues\
- Building real-world cloud architecture\
\
---\
\
## Author\
\
Abhinav S. Yanambaka  \
Bachelor\'92s in Cloud Computing and Solutions}