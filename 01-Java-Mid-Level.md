### 📘 Definitions & Concepts
## Java Mid-Level - Key Definitions

### 1. Polymorphism
Ability to take many forms. 
- **Compile-time**: Method overloading
- **Runtime**: Method overriding

### 2. Inheritance
A class (child) can inherit fields and methods from another class (parent) using `extends`.

### 3. Abstraction
Hiding internal details and showing only the functionality.
- Achieved via **abstract classes** and **interfaces**.

### 4. Interface vs Abstract Class
| Feature              | Interface         | Abstract Class       |
|----------------------|------------------|----------------------|
| Keyword              | `interface`      | `abstract class`     |
| Method Types         | abstract (default)| abstract + concrete |
| Multiple Inheritance | Yes              | No                   |

### 5. Exception Handling
- `try` → code block to monitor
- `catch` → handles exception
- `finally` → always runs
- `throw` → throws exception manually
- `throws` → declares exception

### 6. Collections Framework
Java API for managing groups of objects (List, Set, Map, Queue).

---

### 🖼 Architecture Descriptions (for Diagrams)
## Java Mid-Level - Architecture Descriptions

### 1. Exception Handling Flow
[ try ] → [ catch (Exception e) ] → [ finally ]
Optional: Use `throws` to declare exceptions in method signature.

### 2. Java Collections Hierarchy
- **List** (Ordered, duplicates allowed)
  - ArrayList
  - LinkedList
- **Set** (Unique elements)
  - HashSet
  - LinkedHashSet
  - TreeSet
- **Map** (Key-value pairs)
  - HashMap
  - LinkedHashMap
  - TreeMap
- **Queue**
  - PriorityQueue
  - Deque

### 3. OOP Structure Diagram
[Object Class] ← [Custom Class] ← [Child Class]
[Interface] → [Implements] → [Class]

---

### 📄 Cheat Sheet

## Java Mid-Level - Syntax & Shortcuts

### Method Overloading
```java
int sum(int a, int b) { return a + b; }
double sum(double a, double b) { return a + b; }
```

### Method Overriding
```java
class Animal {
    void sound() { System.out.println("Sound"); }
}
class Dog extends Animal {
    @Override
    void sound() { System.out.println("Bark"); }
}
```

### try-catch-finally
```java
try {
    int a = 5 / 0;
} catch (ArithmeticException e) {
    System.out.println("Can't divide by zero");
} finally {
    System.out.println("Cleanup");
}
```

### Interface & Abstract Class
```java
interface Shape {
    void draw();
}

abstract class Animal {
    abstract void makeSound();
    void eat() { System.out.println("eating..."); }
}
```

### Common Collection Initialization
```java
List<String> list = new ArrayList<>();
Set<Integer> set = new HashSet<>();
Map<Integer, String> map = new HashMap<>();
```
---

### 🃏 Flashcards (Q&A + CLI)

## Java Mid-Level - Flashcards

### 📌 Conceptual Q&A

**Q:** What is method overloading?  
**A:** Defining multiple methods with the same name but different parameters.

**Q:** What’s the difference between HashMap and TreeMap?  
**A:** HashMap is unordered; TreeMap maintains sorted keys.

**Q:** Why use an interface?  
**A:** To achieve full abstraction and multiple inheritance.

**Q:** What’s the root class of all Java classes?  
**A:** `java.lang.Object`

---

### 💻 CLI Flashcards

| Command                           | Description                            |
|----------------------------------|----------------------------------------|
| `jar cf MyApp.jar *.class`       | Creates a JAR file                     |
| `java -cp MyApp.jar MainClass`   | Runs a class from JAR                  |
| `javadoc -d doc/ MyClass.java`   | Creates JavaDocs in the `doc/` folder |
| `javap -c MyClass`               | Disassembles class bytecode           |
---

### 🛠 Bonus: Useful Concept Comparisons

## Interface vs Abstract Class Summary

| Feature           | Interface     | Abstract Class  |
|------------------|---------------|-----------------|
| Constructors     | No            | Yes             |
| Fields           | Constants only| Variables allowed|
| Multiple Inherit.| Yes           | No              |

## List vs Set

| Feature         | List           | Set            |
|----------------|----------------|----------------|
| Order          | Maintains order| Unordered      |
| Duplicates     | Allowed        | Not allowed    |
