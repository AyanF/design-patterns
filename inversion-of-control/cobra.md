## Cobra

There are plenty of object-oriented programming languages in existence including C#, Python and Ruby. So why use Cobra? 

What if you want static and dynamic binding? Use Objective-C or Boo. What if you want expressiveness and quick coding? Use Python, Ruby or Smalltalk. What if you want runtime performance? Use C#, Java, C++, etc. What if you want first class language support for unit tests? Use D.

But what if you want all of those? ... You can't get them! And that's frustrating because none of those productivity-boosting features are incompatible with each other. You shouldn't have to choose between C++'s speed and Python's expressiveness. There's no theoretical reason that you can't have it all. There's "just" a lot of work required to make it happen.

One way to characterize Cobra is with these high level points:

Quick, expressive coding
Fast execution
Static and dynamic binding
Language level support for quality
Cobra achieves 1 by following Python and Ruby (but not religiously). It achieves 2 by favoring static typing ("i = 5" means "i" is an integer and always will be) and leveraging .NET|Mono for machine code generation. It does 3 by using the .NET typing system at compile-time for static types, and using the .NET run-time for dynamic binding. It takes language features for 4 from multiple sources including Eiffel, Python and its own compile-time nil tracking.
