# microservices

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
