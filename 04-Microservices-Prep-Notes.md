## Beginner Level - Concepts & Basics

### 🔹 What Are Microservices?
- Architecture style that structures an application as a collection of loosely coupled services.
- Each service is independently deployable, scalable, and testable.

### 🔸 Characteristics
- Decentralized
- Independently deployable
- Organized around business capabilities
- Technology-agnostic

### 🔹 Monolith vs Microservices
| Aspect         | Monolith                          | Microservices                     |
|----------------|-----------------------------------|----------------------------------|
| Deployment     | Single unit                       | Independently deployed services  |
| Scalability    | Limited (scale whole app)         | Fine-grained (scale individual)  |
| Technology     | Uniform                           | Polyglot                         |

### 🔸 Basic Components
- **Service Discovery**
- **API Gateway**
- **Central Config Server**
- **Client Communication** (REST/gRPC)

### 🔹 Tools & Tech Stack
- Spring Boot, Spring Cloud
- Eureka, Ribbon, Feign, Zuul/Gateway
- Docker, Kubernetes

---

## Mid-Level - Patterns, Tools, Spring Integration

### 🔹 Spring Cloud Modules
- **Eureka Server** – Service discovery
- **Feign Client** – Declarative REST client
- **Spring Cloud Config** – Centralized config
- **Spring Cloud Gateway** – API Gateway
- **Hystrix / Resilience4j** – Circuit breaker

### 🔸 API Gateway
- Central entry point
- Handles routing, filtering, rate limiting
- Replaces older Zuul with Spring Cloud Gateway
```yaml
spring:
  cloud:
    gateway:
      routes:
        - id: user-service
          uri: lb://USER-SERVICE
          predicates:
            - Path=/users/**
```

### 🔹 Inter-Service Communication
- **REST (via Feign):** Simpler
- **gRPC:** Faster, but complex setup

### 🔸 Load Balancing
- Client-Side: Ribbon (now deprecated)
- Server-Side: Kubernetes Ingress or Service Mesh (Istio/Linkerd)

### 🔹 Configuration Management
- **Spring Cloud Config Server**
- Supports Git, Vault backends

### 🔸 Security Basics
- OAuth2 / JWT with Spring Security
- API Gateway as Auth Provider
- `@EnableResourceServer`, `@EnableAuthorizationServer`

### 🔹 Database Strategies
- **Database per service** (preferred)
- **Shared database** (not recommended)
- **Sagas / Eventual Consistency** for transactions

---

## Advanced Level - Architecture, Observability, CI/CD

### 🔹 Microservices Architecture Patterns
- **Strangler Fig Pattern**
- **Saga Pattern (Choreography vs Orchestration)**
- **CQRS** (Command Query Responsibility Segregation)
- **Event Sourcing**

### 🔸 Service Mesh
- Transparent service-to-service communication
- Common tools: Istio, Linkerd
- Features: retries, tracing, fault injection

### 🔹 Observability
- **Distributed Tracing**: Zipkin, Sleuth, Jaeger
- **Metrics**: Prometheus + Grafana
- **Logs**: ELK stack (Elasticsearch, Logstash, Kibana)

### 🔸 Fault Tolerance
- **Circuit Breakers**: Resilience4j, Hystrix (deprecated)
- **Retries**, **Timeouts**, **Rate Limiting**

### 🔹 Docker & Kubernetes
- Containerize each microservice with Docker
- Use Kubernetes for orchestration:
  - Deployments, Services, Ingress
  - ConfigMaps and Secrets

### 🔸 CI/CD Pipeline
- Tools: Jenkins, GitLab CI, GitHub Actions
- Auto-build → test → dockerize → deploy

### 🔹 Testing Strategies
- **Unit Tests** for services
- **Integration Tests** with containers (TestContainers)
- **Contract Testing** with Pact
- **End-to-End Testing** using Postman/Newman or Selenium

### 🔸 Security Deep-Dive
- OAuth2, OpenID Connect
- JWT token validation in Gateway
- Mutual TLS between services (Service Mesh)

### 🔹 Anti-Patterns
- Shared Database
- Wrong service granularity
- Too much synchronization

---

This comprehensive microservices guide is structured for off-screen learning with flashcards, diagrams, cheat sheets, and architecture overviews.

Would you like a printable PDF, visual diagram set, or flashcard deck next?
