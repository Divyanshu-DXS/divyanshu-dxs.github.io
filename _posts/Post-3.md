---
layout: post
title: Event Driven Systems: How Communication Patterns Shape System Architecture
date: 2026-03-09
---

# Moving to Event-Driven Architecture: It's a Mindset, Not Just a Tech Stack

After a decade in software, I’ve realized that the hardest part of moving to **Event-Driven Architecture (EDA)** isn’t the tech stack—it’s the shift in how you view service boundaries.

<!--more-->

Most of us grow up on **Synchronous APIs**. It’s intuitive:

> Service A calls Service B, waits, and gets a result.  
> It’s a straight line.  

It’s simple, intuitive, and works well for many systems.

---

## The Mental Shift

In an Event-Driven world, that mental model breaks.

Instead of thinking:  

> "Which service should I call to get this done?"  

You start thinking:  

> "What event should be published so the right systems can react?"  

In an Event-Driven system, services don’t care who is listening. They just announce facts:

- `Order_Created`  
- `Payment_Succeeded`  
- `Shipment_Dispatched`  

This creates a different kind of architecture, and it matters because:

### Benefits of Event-Driven Systems

- **True Decoupling:** Producers don't need to know their consumers exist.  
- **Extensibility:** You can add a "Rewards Service" to the flow without touching a single line of code in the "Checkout Service."  
- **Resiliency:** If a downstream consumer is down, the event stays in the queue. The system doesn't crash; it just pauses.  

---

## New Challenges

Event-Driven systems introduce new considerations:

- **Eventual consistency:** Is the data correct right now, or will it be correct in 2 seconds?  
- **Idempotency:** Handling the same event twice without breaking the world.  
- **Observability:** Distributed tracing becomes a mandatory skill, not an elective.  

---

## REST vs Event-Driven Systems

REST and event-driven systems, although similar, aren’t competing ideas. They solve different kinds of problems:

> "Synchronous APIs are great when you need immediate answers."  
> "Events are powerful when systems need to react, evolve, and scale independently."  

---

## The Bigger Picture

Beyond tech stacks, APIs, or messaging platforms, how **systems communicate** and how **responsibilities are distributed** is an integral factor in system architecture.

Sometimes, changing the communication model changes how you think about the entire system.