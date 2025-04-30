## 🟢 **Java - Beginner Level**

### 📘 Definitions & Concepts

## Java Beginner - Key Definitions

### 1. JVM (Java Virtual Machine)
JVM is the engine that runs Java bytecode. It allows Java programs to be platform-independent.

### 2. JDK (Java Development Kit)
The complete toolkit that includes JRE + tools like `javac`, `javadoc`, `javap`.

### 3. JRE (Java Runtime Environment)
Environment required to run Java applications. Contains JVM + runtime libraries.

### 4. Class & Object
- **Class**: Blueprint for creating objects.
- **Object**: An instance of a class.

### 5. Method
A block of code which performs a specific task when called.

### 6. Variable
Container to store data. Types: local, instance, static.

### 7. Data Types
- Primitive: `int`, `double`, `boolean`, `char`
- Reference: Arrays, Objects

### 8. Control Flow
- Conditional: `if`, `else`, `switch`
- Loops: `for`, `while`, `do-while`

### 9. OOP Principles (Intro)
- Encapsulation
- Inheritance (Basics)
- Abstraction (Intro)
- Polymorphism (Concept)
```

---

### 🖼 Architecture Descriptions (for Drawing/Visual Mapping Tools)

## Java Beginner - Architecture Descriptions

### 1. JVM Architecture
- **Class Loader**: Loads `.class` files into memory.
- **Method Area**: Stores class-level data.
- **Heap**: Stores objects and instance variables.
- **Stack**: Stores method calls and local variables.
- **PC Register**: Current executing instruction.
- **Execution Engine**: Executes bytecode.
- **Native Method Interface**: Access native (C/C++) code.
- **Native Libraries**: Platform-specific DLLs or .so files.

### 2. Java Program Flow
1. Write code → `Hello.java`
2. Compile using `javac Hello.java` → generates `Hello.class`
3. Run with `java Hello` → JVM executes bytecode
```

---

### 📄 Cheat Sheet

## Java Beginner - Syntax & Quick Reference

### Class Structure
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

### Data Types
| Type     | Size     | Example            |
|----------|----------|--------------------|
| int      | 4 bytes  | `int a = 10;`      |
| double   | 8 bytes  | `double pi = 3.14;`|
| char     | 2 bytes  | `char c = 'A';`    |
| boolean  | 1 bit    | `boolean b = true;`|

### Loops
```java
for (int i = 0; i < 5; i++) {}
while (condition) {}
do {} while (condition);
```

### If-Else & Switch
```java
if (a > b) {
    System.out.println("A is greater");
} else {
    System.out.println("B is greater");
}

switch(day) {
    case 1: System.out.println("Mon"); break;
    default: System.out.println("Other day");
}
```
```

---

### 🃏 Flashcards (Q&A + CLI)

## Java Beginner - Flashcards

### 📌 Conceptual Q&A

**Q:** What is JVM?  
**A:** Java Virtual Machine, executes bytecode and enables platform independence.

**Q:** What is a class in Java?  
**A:** A blueprint to create objects.

**Q:** What is the difference between JDK and JRE?  
**A:** JDK = JRE + Development Tools (like compiler, debugger, etc.)

---

### 💻 CLI Flashcards

| Command              | Description                   |
|----------------------|-------------------------------|
| `javac Hello.java`   | Compiles Java source file     |
| `java Hello`         | Runs compiled bytecode        |
| `java -version`      | Shows installed Java version  |
| `javadoc Hello.java` | Generates documentation       |
| `javap Hello`        | Bytecode disassembler         |
```

---
