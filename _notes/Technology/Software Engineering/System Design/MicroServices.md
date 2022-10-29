---
title : MicroServices
notetype : feed
date : 29-10-2022
---

Its an architecture used by large teams to build scalable services
	- Loosely coupled
	- blast radius or impact is less when services go down
	- scale up independently
	- deploy independently

![microservices|400](microservices.png)

- individual services are called domains
- Interact via surface areas
![surface areas|400](ms_surface_areas.png)


- communicate with gRpc, message brokers and message streaming
- logical components for DB but burden of moving data integrity to application layer
![db|400](ms_db.png)

- API gateway deals with authentication service and talks to service registry to find the micro service address
- Monitoring tools that reports health of each micro service
- Costly and suitable for large teams who want to deploy and manage independently 

Principles used for [MicroServices]
	
	- Independent and autonomous services
	- Scalability
	- Decentralisation
	- Availability
	- Resilient services
	- Isolation from failures
	- CD through devops integration
	- Real time load balancing
	- Auto provisioning


- [ ] Micro services design patterns - https://www.edureka.co/blog/microservices-design-patterns

**Saga Pattern**
- Saga is series of local transaction to complete a business transaction
- Architectural pattern to implement distributed transactions in a microservices architecture 
- Each local transaction should have reversible transaction in case one of the saga event fails

- `Uses`  It enables an application to maintain data consistency across multiple services without using distributed transactions
- `Cons`  The programming model is more complex. For example, a developer must design compensating transactions that explicitly undo changes made earlier in a saga.

![[Pasted image 20221025173657.png]]

Two ways to implement saga

- **Choreography based saga**
![[Pasted image 20221025174252.png]]

- **Orchestration based saga**
![[Pasted image 20221025174300.png]]

Response can be given by 
- Either waiting until transaction across MSs are completed
- Let client poll after giving an order id
- Update client once order is processed

**TODO**
- [ ] https://www.baeldung.com/cs/saga-pattern-microservices
- [ ] 2PC Two phase commit protocol

Reference:
https://www.youtube.com/watch?v=lTAcCNbJ7KE
https://www.edureka.co/blog/microservices-design-patterns
https://microservices.io/patterns/data/saga.html