# System Integrations

## Overview

This project demonstrates how modern cloud systems integrate with external services using an event-driven architecture. Instead of direct communication between systems, events are published to messaging services which allows systems to process information asynchronously.

The integration layer simulates how an ordering system would communicate with external systems such as inventory management, delivery services, and analytics platforms.

---

## Event Driven Architecture

Event-driven architecture allows systems to react to events as they occur.

Example workflow:

Customer places order  
↓  
API processes order  
↓  
Order event is published  
↓  
Message is sent to queue  
↓  
External systems process event

This approach allows systems to remain loosely coupled and scalable.

---

## Amazon SQS Integration

Amazon Simple Queue Service (SQS) was used to simulate communication between the ordering platform and downstream services.

When an order is created, the API publishes an event message to an SQS queue.

Example event flow:

Order Created  
↓  
API publishes message  
↓  
Message stored in SQS queue  
↓  
Inventory update simulated

This allows the system to demonstrate asynchronous communication.

---

## Example Order Event

An example event message might look like:


{
"eventType": "OrderCreated",
"orderId": 1045,
"product": "Fresh Produce Package",
"quantity": 2,
"deliveryWindow": "10AM - 12PM"
}


This message represents an order being created and sent to downstream systems.

---

## Simulated Inventory Updates

Because this project focuses on demonstrating cloud architecture rather than implementing a full inventory system, inventory updates are simulated.

When an order event is received:

1. The inventory system reads the message from the queue
2. Inventory levels are updated
3. Order processing continues

This demonstrates how microservices typically communicate in modern distributed systems.

---

## Benefits of Event Driven Systems

Using messaging systems like Amazon SQS provides several advantages:

- Loose coupling between services
- Improved scalability
- Fault tolerance
- Asynchronous processing
- Improved system reliability

These patterns are widely used in modern cloud-native applications.

---

## Real World Application

In a production environment this integration layer could communicate with systems such as:

- Inventory management systems
- Warehouse management systems
- Delivery scheduling platforms
- Payment processing services
- Analytics and monitoring systems

This project demonstrates the architectural pattern used to support these