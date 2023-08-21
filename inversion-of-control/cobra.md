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

## Motivation for Cobra 

- Clean, expressive syntax (Python, Ruby)
- Run-time performance (C#, C++)
- Static and dynamic typing (Objective-C,VB)
- Contracts (Eiffel, Spec#)
- Nil tracking (Spec#, iihtdioa.C#)
- Productivity boosters are scattered across languages
- Not mutually exclusive! Yet, must decide per project.

## Origin

Quoting  **_Chuck Esterbrook_**  , the man who designed Cobra

I was bouncing between various languages depending on their strengths and a given project. On the surface, that sounds alright, but in reality it was silly because many of the strengths of these languages are not mutually exclusive. For example, having clean syntax does not require poor performance. Having static types does not exclude dynamic message passing. And so on.
The last straw for me was a financial analysis program originally written in Python. The coding was very fast, but I had to wait over twenty minutes to get the results. This made the cycle of ‘think-code-run’ very slow. Next I tried C#. Using the same classes, methods and algorithms, execution time dropped to twenty seconds, although coding time increased substantially.

Some of the more interesting projects actually require good performance from the start. Examples include simulation, bio-informatics, games, financial analysis, artificial intelligence and some business applications. Sometimes you’re lucky and you can offload the performance issue to a library, or write your code a little smarter in order to get the performance you need. But that’s not always the case, and getting kicked out of Python (or Ruby or Smalltalk) over performance is a sour experience.

The C-based languages offer sufficient performance for a much wider range of applications, but just because I want my programs to execute reasonably fast doesn’t mean that I don’t want to code like the wind.

Along the way, I also became interested in the quality problems that plague applications. Programs are just too buggy. Consequently, Cobra offers first class support for unit tests, contracts, ‘informative’ asserts and compile-time nil/null tracking. I now consider these features an essential part of Cobra.

### Language features adapted in Cobra 
1. **Python** confirmed the suspicion that curly braces, semicolons and parenthesis were wasting time and cluttering the code. Cobra takes many ideas from Python including clean syntax, collection literals and ‘no hassle’ local variables. Python was influenced by SETL by way of ABC, and Cobra takes this a bit further by offering set literals.

2. **C#** is the flagship language for .NET which was the first back-end for Cobra. Its use of static types and generics with fast method dispatch make it feasible for applications where Python and Ruby are too slow. By incorporating high level features such as garbage collection and generators, C# shows that fast execution doesn’t require the developer to use a low level language

3. **Eiffel** was a pleasant discovery while researching languages. Chuck thinks contracts can be powerful on their own and also complementary to unit tests. Both are built into Cobra.

4. **Objective C**  was included as it supported both static and dynamic typing. Chuck enjoyed the benefits of this capability throughout the 1990’s as a NeXTstep developer.


**Must Read**
[Geek Of The Week, Chuck Esterbrook](https://www.red-gate.com/simple-talk/opinion/geek-of-the-week/chuck-esterbrook-geek-of-the-week/)

