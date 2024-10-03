* [Return to table of contents](../../README.md)
# Pre-knowledge
## Health checks
- Health checks are used to ensure that the load balancer can handle

# Load Balancer
## General knowledge
- Load balancers optimize:
  - the performance
  - the availability
  - the security 

  of your applications by:
  - distributing traffic.
  - managing failures.
  - providing centralized access points.

- Features:
  - Spread load across multiple downstream instances: distribute incoming
    traffic across multiple servers or EC2 instances. This ensures that no
    single server is overwhelmed and improves the overall performance and
    responsiveness of your application.
  - Expose a single point of access (DNS) to your application: load balancers
    provide a single DNS entry point for your application. This simplifies the
    access for users and clients, abstracting the complexity of managing
    multiple server addresses.
  - Do regular health checks to your instances: perform regular health
    checks to determine the status of each downstream instance. If an
    instance is found to be unhealthy, the load balancer can take it out of
    rotation, preventing it from receiving traffic until it is healthy again.
  - Provide SSL Termination (HTTPS) for your websites: load balancers can
    handle SSL termination, offloading the task of decrypting HTTPS traffic
    from the downstream instances. This helps in reducing the
    computational load on the instances, improving overall performance.
  - Enforce stickiness with cookies: can enforce session stickiness by
    associating a user with a specific server based on a cookie or other
    session-related information. This ensures that subsequent requests from
    the same user are directed to the same backend server, maintaining
    session state.
  - High Availability across zones: load balancers can be configured to
    operate across multiple Availability Zones (AZs). This enhances the high
    availability of your application by distributing traffic across
    geographically separated data centers.
  - Separate public traffic from private traffic: load balancers can be used to
    separate public-facing traffic from private or internal traffic. This helps
    in securing and managing different types of communication within your
    architecture.

# Elastic Load Balancer (ELB)
## Introduction (ELB)
- Elastic Load Balancer (ELB) is a fully managed load balancing service provided by AWS.
It distributes incoming application or network traffic across multiple targets (EC2 instances),
in multiple Availability Zones (AZs).
- Amazon Elastic Load Balancer (Amazon ELB) is a load balancing service that distributes incoming 
application traffic across Amazon EC2 instances, Amazon ECS containers, AWS Lambda functions & IP addresses.
- ELB helps to ensure that your application is highly available and scalable by distributing incoming
traffic across multiple resources.