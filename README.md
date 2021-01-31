# Programming Church - 2021 JavaEdition
## Overall Goals
The main goal is to expand our ability to build stuf in Java using modern practices for 2021 and have some fun along the way. We've keeping the irreverant 'Programming Church' moniker because we meet on Sunday morning for and there's a whole lot of preaching and teaching going on.   He're is a list of concepts we'll take on:
1. Java language basics
2. OO Design - making the leap to Objects rather than funtions
3. Dependancy Management (package mangement) with Maven and Gradle
4. Spring and Spring boot
5. Enterprise Patters for Java
  - Source Control
  - CI/CD patterns
6. Enterprise Architecture
  - Databases / schema change management
  - Config management
  - Security
  - End Point Management
  - Messaging Systems
  - Caching patters
7. Various Cloud Deployments
  - Docker and K8s
  - Azure
  - GCP native
  - Amazon native

# Assignments and Discussions for our Sunday Java Coding Sessions

## First Assignment 01/17/21
- Do all the modules in the [w3schools program Java Totorial](https://www.w3schools.com/java/default.asp) up to the Java Classes section
- Read [Introdution to the Java Environment](https://www.oreilly.com/library/view/java-in-a/9781492037248/ch01.html)
- Do the first 10 modules of [Mike Dane's Java Programming Language Tutorial](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpPpdR_9IQBUDLjYalvdrGGb)
- Do stage 1 of jetbrains academy java material on [Mindsweeoper project](https://hyperskill.org/curriculum)
### Notes from our 1/24/2021 live discussion
- Java Compiler, JVM, and basics of the Classloader and Packages
- Building and running 'hello world' without a package and inside a package - Related Article: [Introduction to Default Package in Java](https://www.educba.com/default-package-in-java/)
### Notes from 1/31/21 live discussion
* type casting 
  * The example below calculates the slope using int math, then casts it to a double
    * To properly complete the math, we could either cast the scanner ints to doubles, or cast each side of the division to double 
  * When doing math, it's a good idea to avoid `int`s

```java
  int x1 = scanner.nextInt();
  int y1 = scanner.nextInt();
  int x2 = scanner.nextInt();
  int y2 = scanner.nextInt();

   double slope = Math.abs(y1 - y2) / Math.abs(x1 - x2);
```
* Object Oriented Programming
  * Passing messages between objects for it to handle the message - don't care how outside the object
  * Diagrams - describe code, use as a plan for writing code, UML (Unified Modeling Language)
    * Sequence diagram
    * Package diagram
    * State diagram
  * Principles of Object Oriented Design - SOLID
    * Single Responsibility - each class should have a single responsibility
    * Open-Closed - open for extension, closed for modification
    * Liskov Substitution Principle - coding to the interface not the base class
    * Interface Segregation - create an Object that's a composit of other Objects
    * Dependency Injection 
