## Beginner Level - Core Spring & REST Basics

### 🔹 Dependency Injection (DI)
- **Concept:** Design pattern where objects are provided their dependencies from an external source.
- **Types of DI in Spring:**
  - Constructor Injection
  - Setter Injection
  - Field Injection (not recommended)
- **Annotation-Based Configuration:**
  - `@Component`, `@Service`, `@Repository`, `@Controller`
  - `@Autowired`, `@Qualifier`, `@Value`

### 🔸 Application Context
- Spring container that manages beans and their lifecycle.
- Interfaces: `ApplicationContext`, `BeanFactory`

### 🔹 Bean Lifecycle
1. Instantiation
2. Dependency Injection
3. Initialization (`@PostConstruct`)
4. Destruction (`@PreDestroy`)

### 🔸 REST API Development
- **Annotations:**
  - `@RestController`, `@RequestMapping`, `@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping`
- **Example:**
```java
@RestController
@RequestMapping("/api")
public class UserController {
    @GetMapping("/users")
    public List<User> getAllUsers() {
        return userService.getUsers();
    }
}
```
- **Data Binding:** `@RequestBody`, `@PathVariable`, `@RequestParam`

### 🔹 Spring Boot Basics
- `@SpringBootApplication` = `@Configuration + @EnableAutoConfiguration + @ComponentScan`
- Embedded servers: Tomcat, Jetty

---

## Mid Level - Spring Boot Features & Security

### 🔹 Spring Boot Actuator
- Provides production-ready features:
  - Health check: `/actuator/health`
  - Metrics: `/actuator/metrics`
  - Environment: `/actuator/env`
- Configuration: `management.endpoints.web.exposure.include=*`

### 🔸 Spring Security Basics
- Authentication & Authorization
- Default login page from Spring Boot
- In-Memory User Configuration:
```java
@Bean
public UserDetailsService users() {
    return new InMemoryUserDetailsManager(
        User.withUsername("user")
            .password(passwordEncoder().encode("password"))
            .roles("USER")
            .build()
    );
}
```
- `SecurityFilterChain` and `PasswordEncoder`
- `@PreAuthorize`, `@Secured`

### 🔹 Configuration & Profiles
- `application.properties` or `application.yml`
- Profile specific: `application-dev.yml`, `application-prod.yml`
- Activate profile: `--spring.profiles.active=dev`

### 🔸 Testing in Spring
- `@SpringBootTest`, `@WebMvcTest`, `@DataJpaTest`
- `MockMvc`, `TestRestTemplate`

### 🔹 JPA & Spring Data
- `CrudRepository`, `JpaRepository`, `PagingAndSortingRepository`
- `@Entity`, `@Table`, `@Id`, `@GeneratedValue`
- Query methods: `findByUsername()`, `findByEmailContaining()`

---

## Advanced Level - Microservices & Reactive Programming

### 🔹 Microservices Architecture
- **Principles:**
  - Decentralization, Loose coupling, Domain-driven design
- **Spring Cloud Modules:**
  - Config Server, Eureka (Discovery), Feign Client, Gateway
- **API Gateway:**
  - Spring Cloud Gateway, filters, routing

### 🔸 Inter-Service Communication
- **REST + Feign Client:**
```java
@FeignClient(name = "user-service")
public interface UserClient {
    @GetMapping("/users/{id}")
    User getUser(@PathVariable("id") Long id);
}
```
- **Circuit Breakers:** Resilience4j, Hystrix (deprecated)
- **Service Discovery:** Eureka Server, Consul

### 🔹 Spring Cloud Config
- Centralized configuration management
- Client connects via REST API to config server
- Supports Git backend

### 🔸 Reactive Programming
- **WebFlux Module:** Based on Project Reactor
- `Mono` and `Flux` types
- `@RestController` + `@GetMapping` returning `Mono<String>`
```java
@GetMapping("/hello")
public Mono<String> sayHello() {
    return Mono.just("Hello World");
}
```
- Non-blocking I/O with Netty

### 🔹 Kafka & Messaging
- Spring Kafka: `@KafkaListener`, `KafkaTemplate`
- RabbitMQ via Spring AMQP

### 🔸 CI/CD and Observability
- **Dockerize Apps**
- **Deploy on Kubernetes**
- **Observability:** Zipkin, Sleuth, Prometheus, Grafana

---

This material is tailored for deep interview prep and printable off-screen study formats like flashcards, architecture diagrams, and cheat sheets.
