## Inversion Of Control

### What is Inversion Of Control ?
  
The Inversion of Control (IoC) design pattern is a software development principle that promotes the decoupling of components in a system by inverting the control of their dependencies. In simpler terms, instead of a component directly creating and managing its dependencies, the responsibility for creating and providing these dependencies is shifted to an external entity or framework.

### Why Ioc ? 
In the traditional approach, components are tightly coupled together, which can lead to several issues:

1.  Code becomes difficult to modify: When components are tightly coupled, any changes to one component might require changes in many other components.
    
2.  Code is less reusable: Components that are closely tied to specific implementations cannot be easily reused in different contexts.
    
3.  Testing becomes challenging: It is challenging to test individual components in isolation, as they depend on other components.
    
In contrast, the Inversion of Control design pattern addresses these issues by promoting loose coupling between components. This is achieved by introducing an intermediary entity (often referred to as a container or framework) responsible for managing the dependencies between components.

### Key Concepts

1.  Dependency Injection (DI): DI is a common technique used in IoC to provide the required dependencies to a component from the outside. Instead of the component creating its dependencies, they are "injected" into the component by the framework or container.
    
2.  Service Locator: In some IoC implementations, a service locator pattern is used, where components request their dependencies from a centralized service locator. The service locator manages the actual instances of the dependencies and provides them when requested.
    
3.  Event Handling: IoC can also be implemented using events, where components publish events and subscribe to events. The framework handles the event publishing and distribution to relevant subscribers.
