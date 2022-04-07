# OpenTelemetry Demo
## Product Feedback Service
![Banner](https://github.com/riki-nitdgp/OpenTelemetryDemo/blob/main/banner.png?raw=true)

### Service Details 
- **OtelApiGateway:** : It is written in  Python(FastAPI). It acts as a reverse proxy to accept all application programming interface (API) calls, aggregate the various services required to fulfill them, and return the appropriate result. (Port: 8006)

- **user-service:** It is written in Python(FastAPI). Used for storing user data, authorization and authentication. (Port: 8005)
- **inventory-service:** It is written in Java(Spring Boots), Used for storing all products and its availability  status. (Port: 8009)
- **rating-review-service:**  It is written in Java(Spring Boots). Used for storing review and rating for different products. (Port: 8002)

### Service Architecture 
![ServiceArchitecture](https://github.com/riki-nitdgp/OpenTelemetryDemo/blob/main/MicroServivce.jpg?raw=true)


### Deployment Steps 
- Clone the repository `git clone https://github.com/riki-nitdgp/OpenTelemetryDemo.git`
- Build Java Services
- - **For Rating and Review Service:**
- - - `cd rating_review_service`
- - - `mvn clean install`
- - **For Inventory Service:**
- - - `cd inventory`
- - - `mvn clean install`
- Now run `docker-compose up --build`
- It spins up all the services, opentelemetry collector, Jaeger.
- Now You can play with the service using api, find the postman collection [here](https://www.getpostman.com/collections/ac35fe0a9bb14a4bc572 "here")

### OpenTelemetry Trace Flow
![OtelTraceFlow](https://github.com/riki-nitdgp/OpenTelemetryDemo/blob/main/OtelArchitecture.jpg?raw=true)

### Find Your Traces
- Open Jaeger `http://localhost:16686`

### Service Map

![ServiceMap](https://github.com/riki-nitdgp/OpenTelemetryDemo/blob/main/Screenshot%202022-04-07%20at%205.24.35%20PM.png?raw=true)
