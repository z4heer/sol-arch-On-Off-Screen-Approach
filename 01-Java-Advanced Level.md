### 📘 Definitions & Concepts

```markdown
## Java Advanced - Key Definitions

### 1. Multithreading
Enables concurrent execution of two or more threads. Helps in maximum CPU utilization.

### 2. Synchronization
Controls access to shared resources in multithreading. Prevents data inconsistency.

### 3. Executor Framework
High-level replacement for managing threads using `Executors`, `ExecutorService`, and thread pools.

### 4. Lambda Expression (Java 8)
Concise way to represent a method using `() -> {}` syntax. Used with functional interfaces.

### 5. Stream API (Java 8)
Functional-style operations on collections, like `map()`, `filter()`, `reduce()`.

### 6. Optional Class (Java 8)
Prevents `NullPointerException`. Wraps a value that may or may not be present.

### 7. Reflection API
Inspects and modifies runtime behavior of classes and objects.

### 8. Serialization
Converting an object to a byte stream for storage or transmission.

### 9. Garbage Collection (GC)
Automatic memory cleanup in JVM. Removes unused objects from heap.

### 10. Design Patterns (Selected)
- **Singleton**: One instance per JVM.
- **Factory**: Creates object without exposing instantiation logic.
- **Builder**: Builds complex objects step-by-step.
```

---

### 🖼 Architecture Descriptions (for Diagrams)

```markdown
## Java Advanced - Architecture Descriptions

### 1. Thread Lifecycle
[NEW] → [RUNNABLE] → [RUNNING] → [WAITING/BLOCKED] → [TERMINATED]

### 2. JVM Memory Model
- **Heap**: Object storage
- **Stack**: Method calls and local variables
- **Method Area**: Class structure
- **PC Register**: Current executing line
- **Native Method Stack**: JNI code execution

### 3. GC Process (Simplified)
- Mark: Identify objects in use
- Sweep: Clear unused objects
- Compact: Reorganize memory

### 4. Stream API Pipeline
[Collection] → [Stream] → `filter()` → `map()` → `collect()`

### 5. Class Loader Hierarchy
[Bootstrap ClassLoader]  
→ [Extension ClassLoader]  
→ [Application ClassLoader]
```

---

### 📄 Cheat Sheet

```markdown
## Java Advanced - Syntax & Quick Reference

### Lambda Syntax
```java
(interface) () -> { // logic }
(x) -> x * x;
```

### Stream API
```java
List<String> list = Arrays.asList("a", "b", "c");
list.stream()
    .filter(s -> !s.isEmpty())
    .map(String::toUpperCase)
    .forEach(System.out::println);
```

### Optional Usage
```java
Optional<String> name = Optional.ofNullable(null);
System.out.println(name.orElse("default"));
```

### Creating Threads
```java
// Using Thread class
class MyThread extends Thread {
    public void run() {
        System.out.println("Running thread");
    }
}

// Using Runnable
Runnable r = () -> System.out.println("Runnable running");
new Thread(r).start();
```

### Synchronization
```java
synchronized void printData() {
    // only one thread at a time
}
```

### ExecutorService
```java
ExecutorService executor = Executors.newFixedThreadPool(2);
executor.submit(() -> System.out.println("Task running"));
executor.shutdown();
```

### Reflection
```java
Class<?> cls = Class.forName("java.lang.String");
Method[] methods = cls.getDeclaredMethods();
```

### Serialization
```java
ObjectOutputStream out = new ObjectOutputStream(new FileOutputStream("data.ser"));
out.writeObject(myObject);
```
```

---

### 🃏 Flashcards (Q&A + CLI)

```markdown
## Java Advanced - Flashcards

### 📌 Conceptual Q&A

**Q:** What is the difference between `Runnable` and `Callable`?  
**A:** `Runnable` returns void and can't throw checked exceptions; `Callable` returns a value and can throw exceptions.

**Q:** What does the `synchronized` keyword do?  
**A:** It prevents thread interference by allowing only one thread at a time to access a block/method.

**Q:** How does GC work in Java?  
**A:** It automatically deletes unreachable objects in the heap using algorithms like Mark-and-Sweep.

**Q:** What’s the benefit of using Optional?  
**A:** Avoids null checks and prevents NullPointerExceptions.

**Q:** What is reflection in Java?  
**A:** Runtime inspection and manipulation of classes, methods, fields, etc.

---

### 💻 CLI Flashcards

| Command                 | Description                          |
|------------------------|--------------------------------------|
| `jps`                  | List Java processes                  |
| `jstack <pid>`         | Thread dump of a process             |
| `jmap -heap <pid>`     | Heap memory details                  |
| `jstat -gc <pid>`      | Garbage collection stats             |
| `jcmd <pid> GC.run`    | Force garbage collection             |
```

---

### 🧠 Bonus: Design Pattern Summary

```markdown
## Design Patterns Summary

| Pattern    | Use Case                                     |
|------------|----------------------------------------------|
| Singleton  | Global access to one instance                |
| Factory    | Encapsulate object creation                  |
| Builder    | Build complex objects step-by-step           |
| Observer   | Event handling system (e.g., UI updates)     |
| Decorator  | Add features without changing base class     |
```

---

This concludes the **Advanced Java Section** — all in clean, Markdown format and interview-optimized.

---

### ✅ Recap: You now have full Markdown-structured content for:

- ✅ Beginner Java
- ✅ Mid-Level Java
- ✅ Advanced Java

Each includes:  
➡ Definitions & Concepts  
➡ Architecture Descriptions  
➡ Cheat Sheets  
➡ Flashcards (Conceptual + CLI)

---
