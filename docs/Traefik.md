# Traefik
#### 1. What is Traefik?

A modern open-source HTTP reverse proxy and load balancer that makes deploying microservices easy. 
Traefik integrates with existing infrastructure components and configures itself automatically.

    Reverse Proxy: A server that sits in front of web servers and forwards client requests to those web servers.
    Typically implemented to help increase security, performance, and reliability. 

    Load Balancer: Distributes client requests or network load efficiently across multiple servers 
    (No overworked server & automatic redirection of requests if a server goes down) 

#### 2. Why do we need Traefik?

Traefik gives developers greater visibility and reliability concerning the interactions between services by
providing a way to control this communication. Debugging application problems without this dedicated layer of control
can be very complicated and time-consuming. In contrast to competing products like Nginx Traefik can use formats
like YAML, JSON or TOML for configurations instead of a custom one. 


#### 3. Benefits
* Traefik automatically discovers the right configuration for your services.
* Enables HTTPS for microservices (Let's Encrypt certificates)
* Continuously updates its configuration (No restarts!)
* Is very fast
* Clean & Dynamic Web UI
* Can provide metrics
* It is packaged as a single binary file and available as a official docker image (https://hub.docker.com/_/traefik)


#### 4. Drawbacks
* Complicated Documentation
* Does not support logging tools natively; (they need to be installed and configured separately)

