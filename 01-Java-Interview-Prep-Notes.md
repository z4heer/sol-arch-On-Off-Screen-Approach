## Beginner Level

### 🔹 Key Concepts & Definitions

- **JVM (Java Virtual Machine):** Executes bytecode and allows Java's platform independence.
- **JRE (Java Runtime Environment):** Contains JVM + libraries to run Java applications.
- **JDK (Java Development Kit):** Complete toolkit (JRE + development tools like compiler).
- **Class & Object:** Class is a blueprint; Object is an instance of a class.
- **Data Types:**
  - Primitive: `int`, `char`, `double`, `boolean`, etc.
  - Reference: Arrays, Objects.
- **Methods:** Blocks of code performing specific tasks.
- **Variables:** Store data. Types: local, instance, static.
- **Control Structures:** `if`, `switch`, `for`, `while`, `do-while`

### 🔸 Program Execution Flow

1. Write Java file (e.g., `Hello.java`)
2. Compile: `javac Hello.java`
3. Run: `java Hello`

### 🔸 JVM Architecture (Short Description)
- **Class Loader** → **Method Area** → **Heap** → **Stack** → **PC Register** → **Execution Engine**

### 🔹 CLI Flashcards

- `javac FileName.java` → Compile
- `java FileName` → Run
- `java -version` → Check version
- `javap ClassName` → Disassemble bytecode

---

## Mid-Level

### 🔹 Object-Oriented Programming (OOP)

- **Encapsulation**: Using private variables and public getters/setters
- **Inheritance**: Using `extends` to acquire properties/methods
- **Polymorphism**:
  - Compile-time (Method Overloading)
  - Runtime (Method Overriding)
- **Abstraction**: Using interfaces (`interface`) and abstract classes (`abstract`)

### 🔸 Exception Handling

```java
try {
    // code
} catch (Exception e) {
    // handler
} finally {
    // cleanup
}
```

- `throw` vs `throws`

### 🔹 Collections Framework

- **List** (`ArrayList`, `LinkedList`)
- **Set** (`HashSet`, `TreeSet`)
- **Map** (`HashMap`, `TreeMap`)

### 🔸 Wrapper Classes

- `int` → `Integer`, `char` → `Character`
- Use in generics & collections

### 🔹 String Handling

- `String`, `StringBuilder`, `StringBuffer`
- Immutability

### 🔸 CLI Commands

- `javadoc MyClass.java` → Generate documentation
- `jar cf MyApp.jar *.class` → Create JAR file

---

## Advanced Level

### 🔹 Multithreading

- `Thread` class vs `Runnable` interface
- Lifecycle: New → Runnable → Running → Waiting/Blocked → Dead
- `synchronized`, `wait()`, `notify()`

### 🔸 Lambda Expressions & Functional Interfaces

```java
(a, b) -> a + b
```
- Functional Interfaces: `Runnable`, `Callable`, `Predicate`, etc.

### 🔹 Streams API

- `filter`, `map`, `collect`, `forEach`

```java
list.stream().filter(n -> n > 5).collect(Collectors.toList());
```

### 🔸 File I/O (NIO & Legacy)

- `FileReader`, `BufferedReader`, `FileInputStream`
- `Files.walk()`, `Paths.get()` in `java.nio`

### 🔹 Design Patterns (Java Specific)

- **Singleton**
- **Factory**
- **Builder**
- **Observer**

### 🔸 Annotations

- `@Override`, `@Deprecated`, `@FunctionalInterface`
- Custom annotations

### 🔹 Garbage Collection

- Generations: Young, Old, Permanent
- GC types: Serial, Parallel, G1

### 🔸 Java Memory Model (JMM)

- Visibility, atomicity, and ordering of variables in multithreaded apps

---

This content is structured for printable cheat sheets, interview review decks, and visual memory tools like mind maps, diagrams, and flashcards.

Let me know if you want formatted versions for Anki, Notion, or PDFs.

