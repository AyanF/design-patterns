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

## History and Origin 

### Avalon

Inversion of Control, as a term, was popularised in 1998 by  Stefano Mazzocchi  as consequence of trying to engineer a ‘Java Apache Server Framework’ for the growing set of server side Java components and tools at  Apache . Sun were just starting to protect the word Java when used for branding/naming of software and computing functions, so Apache had to look for alternative names. Avalon was chosen as a project name.

To the Avalon team, it was clear that components receiving various aspects of  _component assembly_  ,  _configuration_  and  _lifecycle_  was a superior design to those components going at getting the same themselves.

It is important to point out that The Open Services Gateway (OSGi) initiative was also started around the same time as the Avalon framework and was similar to a degree. It was born in Europe and specified/controlled by a foundation formed around it.

Latterly this type of IoC has been given a new name - Contextualized Dependency Lookup.

Avalon was cancelled as an Apache project in 2004, by the Apache Software Foundation.

### Setter Injection

Joe Walnes, Mike Cannon Brookes and others found themselves writing  [XWork](http://www.opensymphony.com/xwork/)  and  [WebWork2](http://www.opensymphony.com/webwork/)  to support their forthcoming book,  Java Open Source Programming. Joe pointed out that the concepts were very much like those from IoC/Avalon that Paul had been trying to convince Joe to adopt for a couple of years, but that dependencies were passed into the component via setters. The need for those dependencies was declared in some accompanying XML.

Paul who worked with Joe at an energy trading company in London, suggested this was a “second type” of Inversion of Control. Type two IoC, as a term, has been obsoleted for “Setter Injection” of course.

Rod Johnson, lead for the  Spring Framework wrote a book  Expert One-on-One J2EE Design and Development that also discussed the concepts of setter injection, and introduced the codeline that ultimately became the  Spring Framework at SourceForge in February of 2003.

Martin Fowler has suggested that it may be better to have such dependency resolving methods prefixed with init rather than setter. With init or set prefixes to dependency receiving methods, a container could automatically assemble SDI components without the manifest. SDI, under container control, works best with the manifest though. Without a container, SDI Components are very much like simple Java beans to use:

A downside of direct bean user of an SDI component is that it is possible to instantiate a component without setting all the dependencies. As mistakes, these should be quite quick to catch post-compile with a simple test of that application. Months later though, when a jar of components is replaced in an application with a latter version of the same, a new dependency may be missed, and a non-functioning application may be shipped to live. Again, that could be caught with diligent testing.

### Constructor Injection

Rachel Davies, as one of the enthusiastic reviewers of Joe’s book, left a margin note for the paragraphs that discussed the elegance of type two. The margin-note simply suggested that resolving dependencies by constructor was more elegant. Latterly we are inclined to agree. At that moment in time (the spring of 2003) there were no implementation of the constructor injection idea, so it seemed logical for the initial PicoContainer leads (Paul Hammant and Aslak Hellesoy) who liked the idea, to kick off the project.

The added advantage is that CDI Components cannot be instantiated with missing dependencies. Thus the compiler or IDE will catch mismatches between any constructor and the parameters passed into the class on instantiation.

[ATG Dynamo](http://www.atg.com/en/company/dynamo.jhtml)  was a commercial product that was successful in the market place in the late 90’s. It also used constructors for dependency resolution. Dynamo’s commercial success yielded a little when Apache made Struts, but it should not be forgotten that Dynamo casually used constructors for dependencies in web-applications first.

### Types 1, 2&3 renamed

In 2003, Paul was referring to the Avalon style of IoC as “type 1”, setter as “type 2” and constructor as “type 3”. He went as far as publishing an article (**Inversion Of Control Rocks**) on it in Java Developer Journal.

_December 2003_  ; Rod Johnson of the Spring Framework team, Paul Hammant (former Avaloner, and co-lead of PicoContainer), Mike Royle, with Martin Fowler say down and played with some of the language of Martin’s forthcoming article. Martin had drafted this article entirely independently of this team but had be kind enough to show a draft to them. The problem the team had was with the naming of the patterns related to Inversion of Control, and the examples of use that Martin had shown. Rod had been using the injection phrase before so it was felt that the component resolving style being “Dependency Injection” would be a good thing.

Thus when Dependency Injection rightly took over:

Type 1 becomes Contextualized Dependency Lookup

Type 2 becomes Setter Dependency Injection

Type 3 becomes Constructor Dependency Injection

Type 4 was Field Injection or getter injection depending on who you spoke to.

## Implementation in Moqui 

Apache Moqui follows the Inversion of Control (IoC) design pattern to achieve loose coupling, modularization, and maintainability in its architecture.
Here are a few ways in which the IoC design pattern is present in Apache Moqui:

1.  **Service Facade:** Moqui's central service facade is a key component that embodies IoC principles. Services in Moqui are standalone units of functionality that can be invoked by different parts of the application. When you invoke a service, the control of execution is passed to the service facade, which handles the execution of the requested service. This approach helps in achieving loose coupling between different parts of the application.
    
2.  **Entity Facade:** Similar to services, Moqui's Entity Facade abstracts the data access layer, allowing you to interact with the underlying data store without tightly coupling your application code to the database operations. The Entity Facade follows IoC principles by handling the data access and allowing you to focus on the business logic.
    
3.  **Screen Flow:** Moqui's screen flow capabilities, implemented using the Screen Widget System, allow you to define complex user interactions and logic flows. These flows can be orchestrated to follow IoC principles, where the framework manages the flow based on user interactions and events.
    

While Apache Moqui doesn't implement IoC in the same manner as some dedicated IoC frameworks, its design choices and architectural principles promote the separation of concerns, modularization, and flexibility that are core to the Inversion of Control design pattern. This approach helps in creating maintainable and adaptable business applications.

### Appendix
- _**Shutdown of Avalon**_
The Avalon effort was intended to produce an Inversion of Control (IoC) framework for container programming, with the container controlling components that pass lifecycle and dependency functions between each other. Initially focused on Java, the project eventually added C# as a target platform, according to Aaron Farr, who was chairman of the Apache Avalon project committee and now is on the Apache Excalibur project management committee. Excalibur has emerged as one offshoot of Avalon.
Avalon was formally dissolved in November after parallel development projects had emerged within it, Farr said. "Basically, there had been disagreements about the direction the project should take," he said.
"We eventually decided rather than waste resources on infighting, there was more than enough space for the projects to exist within their own project spaces," Farr said.

- [**Inversion Of Control Rocks**](https://paulhammant.com/files/JDJ_2003_12_IoC_Rocks-final.pdf)
- **https://paulhammant.com/blog/000128.html**
- [**Understanding Inversion Of Control**](https://medium.com/@amitkma/understanding-inversion-of-control-ioc-principle-163b1dc97454)

