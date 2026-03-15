# System Architecture

## Overview

This project implements a cloud-native e-commerce ordering platform deployed on Amazon Web Services (AWS). The system simulates a food distribution ordering system where customers can place orders, customize delivery options, and track order status.

The architecture follows a multi-tier cloud design separating presentation, application logic, and data storage layers.

---

## Architecture Layers

### 1. Presentation Layer

The presentation layer represents the user interface where customers interact with the system.

Responsibilities:
- Display products
- Accept customer orders
- Allow delivery preference selection
- Show order status

This layer communicates with the backend API through HTTP requests.

---

### 2. Application Layer

The application layer contains the core business logic of the platform.

Components:
- Containerized REST API
- Order processing logic
- Inventory update events
- Order status tracking

The API service runs inside **Amazon ECS (Elastic Container Service)**.

---

### 3. Data Layer

The data layer stores application data such as:

- Orders
- Delivery preferences
- Order status
- Inventory updates

This project uses **Amazon RDS (MySQL)** as the managed relational database service.

---

### 4. Integration Layer

The system demonstrates an event-driven architecture where system events are communicated through messaging services.

Events include:
- Order creation
- Inventory updates
- Delivery status updates

These events are published to **Amazon SQS queues** to simulate communication with external systems.

---

## AWS Services Used

The following AWS services were implemented in this project:

- Amazon ECS (containerized application deployment)
- Amazon RDS MySQL (database)
- Amazon VPC (network isolation)
- Security Groups (traffic control)
- Amazon SQS (event messaging)
- Amazon EC2 (testing connectivity and infrastructure validation)

---

## Architecture Benefits

This architecture demonstrates several modern cloud design principles:

- Scalable containerized workloads
- Event-driven integration
- Managed database services
- Network isolation through VPC
- Secure communication using security groups

These design patterns are commonly used in real-world cloud-native applications.