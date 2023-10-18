## Introduction
Event Sourcing is a powerful notion in software architecture that may appear complex at first, but we can simplify it. Assume you're creating a time-traveling diary app. Rather than simply preserving the most recent entry, you record each action as a separate "event." These incidents are like glimpses from your diary at various points.
Each event has a timestamp and a description of what occurred. So, if you wish to see the condition of your diary at any point in time, you can repeat these events from the start to reconstruct it. This method enables you to keep a comprehensive history of your data and simply trace changes.
Auditing, debugging, and undoing actions are all made easier with Event Sourcing. It's like having a time machine for your data, ensuring correctness and transparency in your applications.
Event Sourcing simplifies data administration by retaining the history of changes, resulting in more resilient and flexible systems. It is a key notion in modern software architecture.

## EventsStoreDB
An event store is where events are saved. Every change in the domain is tracked in the database. The event store database category is mostly concerned with store events. The event store functions not only as an event database but also as a message broker. It provides an API through which services can subscribe to events. The event shop will deliver each event that is saved in the event store to all interested subscribers.
An event store is not the same as a standard database (graph, document, relational, etc.). It is purpose-built to hold the history of changes, with the state represented by an append-only log of events.

![Alt Text](https://i0.wp.com/i.postimg.cc/YSrhPFVr/Screenshot-from-2022-10-25-18-11-27.png?w=1230&ssl=1)
The event store is the backbone of the event-driven microservices architecture.

## Event-Driven Architecture
The publish-subscribe model is another name for event-driven architecture.

It typically consists of three parts:

* Producer 
* Broker 
* Consumer

Essentially, a producer creates the events that will be steered by a Broker to the appropriate consumers. Consumers will respond to this occurrence and take the necessary actions.

## When to use Event-Driven Architecture
There are numerous applications for this architecture-
When scalability is more critical than performance, we employ this architecture. Also when data replication is required. Because you need the same information in numerous systems, you can utilise events instead of calling distinct systems to convey the information or having all of these services access the same database. As a result, these systems duplicate information from the same source.
Also when parallel processing is used. If you need to perform many services at the same time.
When decoupling is critical when you have a number of heterogeneous systems that you wish to be decoupled.

## Benefits of Event Sourcing
* Data is stored in an event-sourced system as a series of immutable events that occur over time. It offers one of the most powerful audit log solutions accessible.
* All state changes are saved, allowing systems to be moved back and forth in time, which is incredibly useful for debugging.
* Business events can be linked to their parent event, allowing for traceability and visibility of the complete workflow from beginning to end.
* EventStoreDB is a fault-tolerant distributed database solution. If an event processing node fails, the second will take its place and the first will be eliminated.
* To update or read information in CQRS/Event-sourced systems, data flows through a one-way independent model.

## References
1. https://www.youtube.com/watch?v=yFjzGRb8NOk
2. https://www.youtube.com/watch?v=rJHTK2TfZ1I&t=306s
3. https://www.youtube.com/watch?v=Rlzcj3szsso
4. https://blog.knoldus.com/introduction-to-event-sourcing/




