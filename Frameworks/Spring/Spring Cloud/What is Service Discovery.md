## What is Service Discovery?
Suppose you have two microservices A and B. A need to communicate to B. It's logical that A need to know the location of B(url). Now, if you don't use Service Discovery you need to store the information in a static manner. 

The url and internet address of microservice B can be changed frequently because of load balancing, failure, upgrade etc.

There are two main service discovery patterns: client-side discovery and server-side discovery. 

**Client-side discovery** 
Principle: client queries a service registry, which is a database of available service instances. The network location of a service instance is registered with the service registry when it starts up.

It is removed from the service registry when the instance terminates.

**Server-side discovery** 
The client makes a request to a service via a load balancer. The load balancer queries the service registry and routes each request to an available service instance. As with client‑side discovery, service instances are registered and deregistered with the service registry.
