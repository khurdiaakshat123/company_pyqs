# Object-Oriented Programming (OOPS) Cheatsheet 🧩

## 1. The Four Pillars of OOP
- **Encapsulation:** Bundling data (attributes) and methods that manipulate that data into a single unit (class), while restricting direct access via access specifiers (`private`, `protected`, `public`).
- **Abstraction:** Hiding complex implementation details and showing only the essential interface to the user (via abstract classes and interfaces).
- **Inheritance:** Mechanism where a child class derives attributes and behavior from a parent class, promoting code reusability (`is-a` relationship).
- **Polymorphism:** Ability of an entity to take multiple forms:
  - **Compile-time (Static):** Method Overloading, Operator Overloading.
  - **Run-time (Dynamic):** Method Overriding using virtual functions/late binding.

## 2. SOLID Design Principles
- **S - Single Responsibility Principle (SRP):** A class should have one, and only one, reason to change.
- **O - Open/Closed Principle (OCP):** Software entities should be open for extension, but closed for modification.
- **L - Liskov Substitution Principle (LSP):** Subtypes must be substitutable for their base types without altering system correctness.
- **I - Interface Segregation Principle (ISP):** Clients should not be forced to depend upon interfaces they do not use (prefer small, role-specific interfaces).
- **D - Dependency Inversion Principle (DIP):** High-level modules should not depend on low-level modules; both should depend on abstractions.

## 3. Common Design Patterns
- **Creational:**
  - Singleton: Ensures only one instance of a class exists (e.g., Database connection pool).
  - Factory Method: Creates objects without exposing instantiation logic to the client.
  - Builder: Constructs complex objects step by step.
- **Structural:**
  - Adapter: Bridges incompatible interfaces.
  - Decorator: Dynamically attaches additional responsibilities to an object.
- **Behavioral:**
  - Observer: One-to-many dependency where state change notifies all subscribers (Pub/Sub).
  - Strategy: Encapsulates interchangeable algorithms and makes them selectable at runtime.
