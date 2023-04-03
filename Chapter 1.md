# CHAPTER 1 - OBJECT-ORIENTED DESIGN

- Activities in life can be modeled using procedural software
- Knowing the order of events allows you to write code to do each thing and then quite deliberately string the things together, one after another
- The *world* is object-oriented and can be viewed as a series of spontaneous interactions between objects

    > "OOD requires that you shift from thinking of the world as a collection of predefined procedures to modeling the world as a series of messages that pass between objects."
    > "Failures of OOD might look like failures of coding technique, but are actually failures of *perspective*."

- First requirement of OOD = immerse self in objects; acquire an object-oriented perspective

## OOP - CASE FOR DESIGN, WHEN TO DO IT, AND HOW TO JUDGE IT

### IN PRAISE IN DESIGN

- OOD techniques solve the moral and technical dilemmas of programming
- OOD techniques also produce cost effective software using code that is pleasurable to work on

**The Problem Design Solves:**

- Design does not matter in situations where an applications never needs to change
    > Unfortunately, something will *always* change! Change is unavoidable, ubiquitous, omnipresent, and inevitable.
- Changing requirements introduce forces that apply sudden and unexpected pressures that work against best-laid plans
- The need for change is *why* design matters
- Easy-to-change applications = pleasure to write, joy to extend, flexible, and adaptable
- Hard-to-change applications = high cost, unpleasant to work with

**Why Change Is Hard:**

- Object-oriented apps are made of parts that interact to produce the behavior of the whole
- Parts = objects & Interactions = messages passed between objects
- To get the correct *message* to the target object requires for the sender to know things about the receiver
    > Dependencies are created between the sender and receiver, here
- The goal of OOD is to properly manage dependencies
    > OOD is a set of coding techniques that arrange dependencies such that objects can tolerate change!
- When objects know *too much* about their environment on a full-scale, they are picky, and need things to be concrete which causes constraint

**Practical Definition of Design:**

- Every application is a **collection of code** and it's arrangement is the **design**
- Design is an art - the art of arranging code
- Every problem has two components:
  1. Write code for the feature to deliver
  2. Create code that is amenable to being changed later
- Combine overall understanding of application requirements with knowledge of the costs and benefits of design alternatives
- Devise an arrangement of code that is cost effective in the present and continues to be so in the future

    > "Design is not an assembly line where similarly trained workers construct identical widgets; it’s a studio where like-minded artists sculpt custom applications."
- Practical design DOES NOT ANTICIPATE what will happen to your application - it ACCEPTS that something *will* and that, in the present, you cannot know what
- Practice design preseves your options for accomodating the future
- Purpose of design: to allow you to do design *later* and reduce the cost of change

## THE TOOLS OF DESIGN

### DESIGN PRINCIPLES

**S.O.L.I.D.:**

- coined by Michael Feathers; popularized by Robert Martin

1. Single-Responsibility
2. Open-Closed
3. Liskov Substitution
4. Interface Segregation
5. Dependency Inversion

**D.R.Y.:**

- by Andy Hunt; Dave Thomas

**Law of Demeter (LoD):**

- Demeter Project by Northeastern University

**History of Quantifying Code:**

- 1990s Chidamber, Kemerer, Basili study

> "A metrics suite for object-oriented design"

*What were the relative factors that contributed to the results of their research?*

- size of classes
- entaglements classes have with one another
- depth and breadth of inheritance hierarchies
- number of methods invoked as a result of any message sent

*How were the factors used in the quantification of the code?*

- significant code arrangements were picked
- formulas were devised to count the code arrangements
- found that resulting metrics correlated to the quality of the enclosing application

*What are the caveats of these studies?*

- only examined very small applications written by graduate students
- code in the studies not repreresentative of real-world OO applications

**Additional Research:**

- 2001 Laing, Coleman - *Principal Components of Orthogonal Object-Oriented Metrics*
- 'NASA Goddard Space Flight Center' application study
- intention of finding the "a way to produce ch (1,617 classes; 500,000 lines of code)
- research supports earlier studies and confirms that design principles matter
- principles of good design represent measurable truths and following them will improve your code

**Design Patterns:**

> "...object-oriented design involves patterns."

Design Patterns book describes patterns as...

> "simple and elegant solutions to specific problems in object-oriented software design that you can use to make your own designs more flexible, modular, reusable and understandable"

- give an entire generation of programmers the means to communicate and collaborate
- pattern misapplication results in complicated and confusing code but this result is not the fault of the pattern itself

> A tool cannot be faulted for its use, the user must master the tool.

### THE ACT OF DESIGN

- designing software can get hard

**How Design Fails:**

1. Lack of design.

- it is possible to produce working applications without knowing the first thing about design
  - true of any OO language but some languages are more susceptible than others and an approachable languages
  - especially true for an approachable language like `Ruby`
  - a friend's language that permits anyone to create scripts to automate repetitive tasks and an opinionated framework like Ruby on Rails

- successful, but undesigned applications carry the seeds of their own destruction
  - easy to write but gradually become impossible to change
  - early promise of painless development gradually fails and optimism turns to despair

- the trap of overdesign
  - little knowledge is dangerous
  - as knowledge increases + hope returns - results in relentless design!

- when the act of design is separated from the act of programming
  - process of progressive discovery that relies on a feedback loop
    - feedback loop - timely and incremental
- use iterative techniques of the Agile software movement
  - allows design to adjust regularly and to evolve naturally

**When To Design:**
...  
