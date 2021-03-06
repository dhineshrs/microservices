# microservices

microservices‑based applications often use a mixture of SQL and NoSQL databases, the so‑called **polyglot persistence** approach.

## API Gateways ##
1. Apigee
2. CA Layer 7
3. Mulesoft
4. Kong
5. Tyk
6. gravitee (https://gravitee.io/)

An **API Gateway** is a server that is the single entry point into the system. It is *similar to the Facade pattern* from object‑oriented design. The API Gateway encapsulates the internal system architecture and provides an API that is tailored to each client. It might have other responsibilities such as authentication, monitoring, load balancing, caching, request shaping and management, and static response handling.

## About API Gateway: ## 

- It acts as a router. It is the only entry point to our collection of microservices. This way, microservices are not needed to be public, anymore, but are behind an internal network and API Gateway is responsible for making requests against a service or another one (Service Discovery).

- It acts as a data aggregator: API Gateway fetches data from several services and aggregates it to return a single rich response. Depending on the API consumer, data representation may change according to the needs, and here is where Backend For Frontend (BFF) comes into play.

- It is a protocol abstraction layer: API Gateway can be exposed as a REST API or GraphQL or whatever, no matter what protocol or technology is being used internally to communicate with the microservices.

- Error management is centralized: When a service is not available, is getting too slow or something like that, API Gateway can provide data from cache, default responses or make smart decisions to avoid bottlenecks or fatal errors propagation. This keeps the circuit closed (Circuit Breaker) and makes the system more resilient and reliable.

### Drawbacks of an API Gateway ###
The API Gateway also has some drawbacks. It is yet another highly available component that must be developed, deployed, and managed. There is also a risk that the API Gateway becomes a development bottleneck. Developers must update the API Gateway in order to expose each microservice’s endpoints. It is important that the process for updating the API Gateway be as lightweight as possible. Otherwise, developers will be forced to wait in line in order to update the gateway. Despite these drawbacks, however, for most real‑world applications it makes sense to use an API Gateway.

## event-driven-data-management-microservices ##

In a microservices architecture, each microservice has its own private datastore. Different microservices might use different SQL and NoSQL databases. While this database architecture has significant benefits, it creates some distributed data management challenges. The first challenge is how to implement business transactions that maintain consistency across multiple services. The second challenge is how to implement queries that retrieve data from multiple services.

For many applications, the solution is to use an event‑driven architecture. One challenge with implementing an event‑driven architecture is how to atomically update state and how to publish events. There are a few ways to accomplish this, including using the **database as a message queue** , transaction log mining, and event sourcing.
