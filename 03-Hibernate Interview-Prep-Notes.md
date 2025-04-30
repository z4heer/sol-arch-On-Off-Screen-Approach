## Beginner Level - ORM & CRUD Basics

### 🔹 What is Hibernate?
- ORM (Object-Relational Mapping) framework for Java.
- Maps Java objects to database tables.
- Reduces boilerplate JDBC code.

### 🔸 Core Concepts
- **Entity:** Java class mapped to a database table
- **SessionFactory:** Produces sessions, thread-safe
- **Session:** Used to perform CRUD operations
- **Transaction:** Manages atomic database operations

### 🔹 Annotations
- `@Entity`, `@Table`, `@Id`, `@GeneratedValue`, `@Column`
- Example:
```java
@Entity
@Table(name = "users")
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @Column(name = "username")
    private String username;
}
```

### 🔸 Hibernate Configuration
- **hibernate.cfg.xml** for native config
- Or Java-based config using `StandardServiceRegistryBuilder`

### 🔹 Basic CRUD Operations
```java
Session session = sessionFactory.openSession();
Transaction tx = session.beginTransaction();
session.save(new User());
tx.commit();
session.close();
```

### 🔸 Hibernate CLI Flashcards
- `session.save(entity)` → Insert
- `session.get()` / `session.load()` → Read
- `session.update(entity)` → Update
- `session.delete(entity)` → Delete

---

## Mid-Level - Mapping, Querying, Performance

### 🔹 Relationships
- **One-to-One**: `@OneToOne`
- **One-to-Many / Many-to-One**: `@OneToMany`, `@ManyToOne`
- **Many-to-Many**: `@ManyToMany`
- Cascade types: `PERSIST`, `MERGE`, `REMOVE`

### 🔸 Fetching Strategies
- **Lazy Loading**: Load when accessed
- **Eager Loading**: Load immediately

### 🔹 HQL (Hibernate Query Language)
- Object-oriented query language (not SQL)
```java
String hql = "FROM User WHERE username = :username";
List<User> users = session.createQuery(hql)
                          .setParameter("username", "john")
                          .list();
```

### 🔸 Criteria API (for dynamic queries)
```java
CriteriaBuilder cb = session.getCriteriaBuilder();
CriteriaQuery<User> cq = cb.createQuery(User.class);
Root<User> root = cq.from(User.class);
cq.select(root).where(cb.equal(root.get("username"), "john"));
```

### 🔹 Caching
- **First-Level Cache:** Per session, enabled by default
- **Second-Level Cache:** Across sessions, e.g., Ehcache, Redis
- Enable with `@Cache(usage = CacheConcurrencyStrategy.READ_WRITE)`

### 🔸 Transactions & Isolation
- Use `@Transactional` in Spring
- Isolation levels: `READ_COMMITTED`, `REPEATABLE_READ`, etc.

---

## Advanced Level - Optimization, Integration, and JPA

### 🔹 JPA vs Hibernate
- **JPA**: Specification (interface)
- **Hibernate**: Implementation
- Annotations overlap but Hibernate offers extended features

### 🔸 Advanced Mappings
- Inheritance strategies:
  - `SINGLE_TABLE`
  - `JOINED`
  - `TABLE_PER_CLASS`
- Embedded Types: `@Embeddable`, `@Embedded`
- Composite Keys: `@IdClass`, `@EmbeddedId`

### 🔹 Performance Tuning
- **Batch processing**: `hibernate.jdbc.batch_size`
- **Query Plan Cache**
- **Connection Pooling**: Use HikariCP, C3P0
- **Lazy Initialization Exception**: Solve with DTO projection or fetch joins

### 🔸 Audit & History
- Hibernate Envers: versioning and history of entities
- `@Audited`

### 🔹 Event System & Interceptors
- `PreInsertEventListener`, `Interceptor`, and entity lifecycle callbacks

### 🔸 Spring Boot + Hibernate Integration
- `spring.jpa.hibernate.ddl-auto=update`
- Auto-config via `spring-boot-starter-data-jpa`
- Logging SQL: `spring.jpa.show-sql=true`

### 🔹 Native SQL & Stored Procedures
- `@NamedNativeQuery`, `session.createNativeQuery()`
- Call stored procedures using `NamedStoredProcedureQuery`

---

This structured content supports visual learning (diagrams, mappings), cheat sheets, and mock interview review. Use it to create mind maps, flashcards, or printable review pages.

Would you like the formatted PDF version or diagram set next?

