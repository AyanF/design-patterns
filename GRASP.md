### GRASP: Designing Objects with Responsibilities
Chapter 15 of the book "Applying UML and Patterns" is titled "GRASP: Designing Objects with Responsibilities." In this chapter, the authors discuss a set of principles and techniques called GRASP that can help developers design object-oriented systems that are well-structured, maintainable, and flexible.

The authors begin by explaining that object-oriented design is all about assigning responsibilities to objects. By doing so, we can create a system in which each object has a clear and specific purpose. This leads to better encapsulation, modularity, and reusability, among other benefits.

To help us assign responsibilities to objects, the authors introduce a set of nine GRASP patterns. These patterns are not rules or algorithms; rather, they are a set of heuristics that can guide us in making good design decisions.

#### Creator
The first GRASP pattern is called "Creator." This pattern helps us decide which object should be responsible for creating other objects. The authors recommend that we assign this responsibility to an object that has the most information required to create the new object, or an object that is closely related to the new object in the system.

#### Information Expert
The second pattern is "Information Expert." This pattern helps us decide which object should be responsible for performing a particular task or providing a particular piece of information. The authors recommend that we assign this responsibility to an object that has the most information required to perform the task or provide the information.

#### Controller
The third pattern is "Controller." This pattern helps us decide which object should be responsible for coordinating and controlling the flow of information between other objects. The authors recommend that we assign this responsibility to an object that is responsible for a use case, or to a separate object that is dedicated to this task.The Controller class is responsible for handling user input, delegating tasks to other objects, and managing the flow of information between objects. This pattern helps to reduce the complexity of the system and makes it easier to maintain and modify.

#### Low Coupling
Low Coupling is not a pattern, but rather a principle that should be applied throughout the design process. Low Coupling means that objects should have minimal knowledge of each other. This helps to reduce the complexity of the system and makes it easier to maintain and modify.

#### High Cohesion
The fifth pattern is "High Cohesion." This pattern helps us design objects that are highly cohesive, meaning that their internal elements are related and work together to achieve a common purpose. The authors recommend that we group related responsibilities together into cohesive objects.


#### Polymorphism
Polymorphism is a principle that suggests that objects of different classes should be able to respond to the same message in different ways. This allows for greater flexibility and adaptability in the system.It helps us design objects that can take on multiple forms or behaviors. The authors recommend that we use polymorphism to create flexible and extensible systems.

#### Pure Fabrication
The Pure Fabrication pattern is used to assign responsibilities to classes that do not represent real-world concepts. These classes are used to perform tasks that do not fit naturally into any other class. This helps to maintain a high level of cohesion and reduces the complexity of the system, create objects that don't have a natural place in the system but are necessary for some functionality. The authors recommend that we create these objects as separate, non-domain-specific classes.

#### Indirection
The Indirection pattern is used to introduce an intermediary between two objects. This intermediary can be used to decouple the two objects, provide an additional layer of abstraction, or to provide a way to modify the interaction between the two objects without modifying either object directly.This pattern helps us design objects that can act as intermediaries between other objects. The authors recommend that we use indirection to reduce dependencies and increase flexibility.

#### Protected Variations
The Protected Variations pattern is used to protect a system from the impact of changes in external systems or technologies.It helps us design objects that can handle changes in the system without affecting other objects. The authors recommend that we encapsulate the parts of the system that are likely to change behind interfaces or abstract classes.


#### Conclusion
In conclusion, GRASP patterns provide a set of heuristics that can guide developers in making good design decisions when designing object-oriented systems. By assigning responsibilities to objects in a clear and well-structured way, we can create systems that are easy to maintain, flexible, and extensible.


