# anti-solid-essays
https://dannorth.net/cupid-the-back-story/

# Solid is not solid book annotations

We are told that the SOLID Principles are the cornerstone of good
object-oriented design. But they were developed, in part, as defense mechanisms against the lack of object-oriented features
in C++ and Java. If Smalltalk had won the language wars, there
would be no SOLID.6 

______________________________

Let’s see what is going on with these principles and try to figure
out what they are teaching us. But let’s also keep in mind that they
are not presented as guidelines, patterns, or suggestions, but as
principles. A principle is: a fundamental truth or proposition that serves as the foundation for a system of belief or behavior or for a chain of
reasoning.

Fundamental truths, these are not. Pretty much all they say is
this:
• Single Responsibility Principle: don’t write too much code
in one place, in fact just make single method classes that
have only one line of code in them.
• Open/Closed Principle: make code so flexible you don’t
have to write it, because you aren’t allowed to change it
anyway.
• Liskov Substitution Principle: don’t base logic on run-time
types and also there is a CS paper that is not really related to
this written by a Turing Award Winner! Legit!
• Interface Segregation Principle: use Java interfaces to
mask the bloated API of your classes.
• Dependency Inversion Principle: write all your code in
XML configuration files.

______________________________

## Single Responsability
### What responsability is?
### And why is “two responsibilities” too much?

. In fact, any code review
where the Single Responsibility Principle is invoked makes this
problem plainly clear, because the developers stop talking about
the code and start talking what a responsibility actually is.

We did it because Uncle Bob says we must have only one reason to
change, but he did not define what a reason is, so we made a very
reasonable assumption and created a set of pure nonsense that
junior developers will copy and senior developers will curse and
all because we did what some principle said because principles are there for us to follow and not guidelines which would invite
thinking through nor are they design patterns which are usually
clear about when and how they should be applied so that we can
make sure we are balancing all the right tradeoffs and not just
appealing to authority.

We could’ve prevented this with two simple questions:
• Does the method implement a complete concept? If yes,
don’t touch it.
• Does the proposed change affect cohesion? If not, the
change is fine as it is.

The thing is, software design isn’t about counting up things and
deciding the design is good or bad. Our code can, and should, be
evaluated for cohesion, and this is a necessarily fuzzy concept.
If you think your code is cohesive, don’t mess with it! If it’s not,
refactor it so that it is. But when discussing what to do, stay close
to the code and the problem it solves. Avoid making a decision by
counting things.

When you think about cohesion, understand that this is rooted
in the concepts of your business domain and not about the code.
Code can’t be cohesive just on its own. It has to have the context
of the domain. And when that context changes, the code might
suddenly lose cohesion

# Liskov
The paper, after outlining the problems with basing logic on runtime types, goes seriously off the rails with a convoluted example
using a Square class that extends Rectangle and in the end there
is no actual advice on what problem we were solving or what to
do.
While the Open/Closed Principle was a test of how well one questions authority in the face of utter nonsense, this principle exists
to provide the “L” needed to make the SOLID acronym work. Poor
Wing never had a chance

# What’s wrong with SOLID and Test Driven Development | Dan North - https://www.youtube.com/watch?v=_h2JF1KZQhI
## S
Current cost of change is low (fast compilation, testing), easy to refactor code and change file structures, easy to navigate
Premature optimization of code structure
When i start code, why should i have an arbitrary separation of my thinking?  (responsability is arbitrary)
