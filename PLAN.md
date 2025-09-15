**Open Telemetry Node JS**
*This project is to exhibit the Open Telemetry and to showcase its usage on distributed tracing*

*Project Requirements*
1. Node JS
2. Postgre
3. nginx
4. Kafka
5. Redis
6. Idempotency
7. Open Telemetry Collector
8. Jaeger tracing
9. Prometheus

 


**Chapters**
*each item can be a branch to document and to isolate every chapter or feature*

0. Make an architectural diagram for all the components to have a solid design and to map the integration of all the required modules and visualize any possible challenges and opportunities. 
    a. sequence diagram for SERVICE_A > SERVICE_B > Kafka > DB
    b. design for CQRS
    c. design plan for load balancing
    d. design plan for containerized components
    e. design plan for Idempotency
    f. design plan for Distributed tracing (service >> OTLP collector >> Kafka >> Prmoetheus >> Jaeger)
1. Create two microservices in Node JS.
    a. SERVICE_B service that adds and fetches item to database. Must have internal and external API
    b. SERVICE_A service that calls SERVICE_B to store the data. Must have internal and external API
    c. Postgre database to store the data
    d. test service call through postman
2. Dockerize the services
    a. create a docker compose to put all the services.
3. Setup Kafka
    a. setup a broker to communicate SERVICE_A to SERVICE_B
4. Setup Load Balancer
    a. setup nginx
    b. expose public endpoints
    c. test public endpoints
    d. perform load testing
5. Setup Redis
    a. Setup a cache for temp storage for avoiding abusive DB calls
5. Implement Idempotency to SERVICE_A
    a. use redis to temp cache the transctionID from the request header within the session
    b. This will ensure that the client communication to server is reliable.
6. Implement CQRS for Service to Service calling
    a. explore applying CQRS from SERVICE_B to Kafka to Database call to separate read from write
7. Implement Open Telemetry and use its collector to trace network spans created by app
    a. use trace
    b. use metrics
    c. use logs
    d. test the collector
8. Add Prometheus to store the log data
    a. integrate OTLP collector to Prometheus through Kafka
9. Add Jaeger tracing for logs and trace visualization
    a. explore different patterns like (cache then display), (network, display then cache), etc



