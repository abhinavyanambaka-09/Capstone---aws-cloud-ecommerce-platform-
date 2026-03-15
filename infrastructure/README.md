# AWS Infrastructure Deployment

## Overview

This project deploys a cloud-based e-commerce ordering platform using Amazon Web Services (AWS). The infrastructure was designed to simulate a real-world cloud environment with networking, containerized services, database storage, and event-driven integrations.

The infrastructure components were configured manually in AWS to demonstrate understanding of cloud architecture and service configuration.

---

## Core AWS Components

The platform uses several AWS services working together to deliver the application.

Main services used:

- Amazon VPC
- Amazon ECS (Elastic Container Service)
- Amazon RDS MySQL
- Amazon EC2
- Amazon SQS
- Security Groups
- Internet Gateway

These services provide compute, networking, database, and messaging capabilities for the application.

---

## Virtual Private Cloud (VPC)

A Virtual Private Cloud was configured to isolate all application resources.

Key components of the VPC include:

- Public subnets
- Route tables
- Internet gateway
- Security groups

The VPC ensures that services communicate securely while allowing controlled internet access.

---

## Internet Gateway

An Internet Gateway was attached to the VPC to allow internet connectivity for public-facing services.

This allowed:

- API services to be accessed externally
- EC2 instances to connect to the internet
- Application traffic to flow between users and the system

---

## Security Groups

Security groups were configured to control inbound and outbound traffic between services.

Example rules include:

- Allow HTTP traffic (port 80)
- Allow API traffic from the web server
- Allow database access from the application layer
- Allow SSH access for EC2 management

These rules ensured secure communication between system components.

---

## Amazon ECS (Elastic Container Service)

The backend application was deployed as a containerized service using Amazon ECS.

Key components include:

- ECS Cluster
- ECS Service
- ECS Task Definitions
- Container images running the API

The ECS service runs the API responsible for processing orders and communicating with other components.

---

## Amazon RDS (MySQL)

The application stores persistent data in an Amazon RDS MySQL database.

Data stored includes:

- Customer orders
- Delivery preferences
- Order status updates

Using RDS provides a managed relational database without needing to manage database servers manually.

---

## Amazon EC2

Amazon EC2 instances were used during the deployment process to test infrastructure connectivity and validate networking configuration.

Tasks performed on EC2 included:

- SSH access verification
- Testing API connectivity
- Validating network routes and security group rules

---

## Amazon SQS Integration

Amazon SQS was used to simulate event-driven communication between the ordering system and external systems such as inventory management.

When an order is placed:

1. The API processes the order
2. An event message is published to the queue
3. Downstream services simulate inventory updates

This demonstrates asynchronous system communication.

---

## Infrastructure Challenges

During deployment several challenges were encountered:

- Incorrect security group rules blocking API access
- VPC routing configuration issues
- Internet Gateway attachment confusion
- ECS service connectivity troubleshooting

These issues were resolved through debugging AWS networking and updating security group configurations.

---

## Deployment Outcome

The final infrastructure successfully deployed the application with:

- Containerized backend services
- Managed relational database
- Event-driven messaging
- Secure cloud networking

This infrastructure design demonstrates real-world cloud architecture patterns commonly used in production systems.