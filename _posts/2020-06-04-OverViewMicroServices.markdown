---
layout: blog
title: "Big picture microservices" 
permalink: /:title
categories: "microservices"
---

##### Understanding micro services from 10,000 feet level

Why Micro services ?
   - lets see the SDLC for a normal project with out microservices
the time taken to get a complete value to production is quite late
   - large team - more time - long life cycle
   - with micro service parallel teams - short life cycle - fast feed back  

What is Micro service ?
- Micro + Service
- "Supposed to one thing"
- independently deployed
- identify - subdomains (each sub domain can be a microservice)
- autonomus services thatwork together
- Bounded context
- Exchange messages for communication

----
#### Designing a MONOLITH
```
                            Front End 
```
```
        user ----------- order              Suppliers
          |                 |               
          |                 |               Category
        Address             |                   |
                        /------------------\    |
                       /                    \   |
                    invoice                  product ------  Media  
  |-------------|
  |  data base  |
  |-------------|           Back End
```

| **Pros** | **Cons** |
| Simple to develop | New team members productivity |
| Simple to Build | Growing teams |
| Simple to test | Code harder to understand |
| Simple to deploy | No emerging technologies |
| Simple to scale | Scale for bad reasons |
| | Overloaded container |
| | Huge database |

----

#### Building Micro services way

##### DDD

````
         user                order               product

        User            user ---- order          Supplier
         |                          |               
         |                         / \           Category
      Address                     /   \             |
         |                   Invoice  Product       |
         |                         |                 Product ----> Media 
         |                         |                       |
         |                         |                       | 
      data base               data base               data base                                             
````
 
 - Using a common db is antipattern
 - because each microservice is independent "Versioning" is important
 - Having different data Storage leads to "Data Synchronization"

Because of different Data bases their might be 
- immediate consistent
- Eventual consistent
- By event sourcing mechanism

#### Comminucation 
    1. RPC (Request <--> reply) (sync or async)
    2. Messaging
      ---- publish a message to Broker
      ---- subscribe to Broker

      make async --------- losely couple


#### How to invoke an external mcro service

> API's & Contracts
Micro Service expose the contracts which allows the other services to call it 

-----
#### Service registry  => phone book of services

Why ?
 - Number of instances cange dynamicaly

Self registration ----s-> Registry
third party serice -------> Registry

When a microservices What to talk to other first need to request
the registry find the physical address with logical address and the query 

----
Because of different micorservices things need to be taken care

##### Cross Origin Resource Sharing

=> Use http headers
 
##### Circuit Breaker Problem 

=> Domino effect 

##### Gateway - single entry point
- Cross cutting concerns
- API translation

##### Security 
    extra care need to be taken Authorization & Authentication

    (Identity and access management system)

How the Services know they are Authenticated ?
- Aceess Token  -> Once Authenticated it uses access token or cookie

----
#### Scalability
            |
           / \
    vertical Horizontal

When Scaled Horizontal it should a load balance in the registry

Availabiity -> 
- if we have single point of failure like gateway, registry, 
should be horzontally scaled

#### Monitoring & Dashboard 
 - Quick viualise

log aggretor, Metircs, Rate limiting,  Alerts. --- Prevet Dos 

Distributed tracing ----- object id






