## Ingress Controller
* Every system whether its a single application or a bunch of microservices has an entrypoint for recieving traffic.
* This entrypoint can accept traffic in the form of a URL, a protocol, hostnme or dns, a Path & port as well. 
* This endpoint is usually identified by a DNS or IP Address, so traffic comes in. 
* Now some calls there is a Proxy/loadBalancer/API gateway but it doesnt matter there always an Ingress Controller.

An **Ingress Controller** is resposible for few potential things like 
1.) Accepting or Denying a http traffic  
2.) SSL termination - we can accept traffic on port 443 via tls, but then we may not need tls and route to different port to reach private applications
3.)	Routing  - Basically deciding where traffic should go
4.)	URL Routing - Basically deciding where traffic should go based on the URL Path
5.) LoadBalancing - We can decide whether we want 60% traffic to service A or 40% to Service B.

Ingress Controllers can be provided by many products which are having there own syntax and Configurations.
Nginx
HA-Proxy
Envoy
Kong
Traefix ....


Main Configurations:- In Ingress we simply describe the host dns we expect traffic on, Ssl, Path we want to route based on and Where we would like the traffic to go.
Ingress may provide load balancing, SSL termination and name-based virtual hosting.
Ingress exposes HTTP and HTTPS routes from outside the cluster to services within the cluster. Traffic routing is controlled by rules defined on the Ingress resource.
