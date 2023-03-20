# CHAPTER 9 - DESIGNING COST-EFFECTIVE TESTS

## INTRODUCTION -----------------------

- Writing changeable code requires 3 different skills:

    1. Understanding Object-Oriented Design
        - Poorly designed code is difficult to change
        - Changeability is the only design metric that matters

    2. Good Refactoring Skills
        - Process of changing a software system in such a way that it does not alter the external behavior of the code yet improves the internal structure
        - Does not alter the external behavior
        - Does not add new behavior - improves existing structure
        - Morphs the current code structure into one that accommodates new requirements
        - New features added only after successful refactoring

    3. Writing High-Value Tests
        - Gives you confidence to refactor constantly
        - Prove that altered code continues to behave correctly without raising overall costs
        - Changes to the code do not force rewrites of the tests

## INTENTIONAL TESTING -----------------------

- Common arguments for having tests:
  - Reduce bugs
  - Provide documentation
  - Writing tests first improves application design
        These are proxies for a deeper goal! ***

- True purpose for writing tests --- REDUCE COSTS.
  - IF writing, maintaining, and running tests takes more time than fixing bugs, writing documentation, and design applications -- tests are not needed!
  - Common for programmers new to writing tests to write tests that cost more than the value the tests provide

- Writing high-value tests requires clarity of intention and knowing what, when, and how to test.

### INTENTIONAL TESTING: Knowing Your Intentions -----------------------

FINDING BUGS

- Easier to find and fix a bug nearer in time to its creation
- Knowing you can or can't do something early on may cause you to choose alternatives in the present which alter design options available in the future
- Embedded bugs acquire dependencies
- Fixing bugs late in process require changing a lot of dependent code

SUPPLYING DOCUMENTATION

- Provide reliable documentation of design
- Story told remains true long after paper documents become obsolete and human memory fails
    *Write tests as if you expect your future self to have amnesia!*

DEFERRING DESIGN DECISIONS

- Allow you to safely defer design decisions
- Better served by code that handles many cases as a single abstraction, even if you DON'T know have enough information to anticipate what the abstraction will be
- Refactor with reckless abandonment when tests depend on interfaces
- Tests verify the continued good behavior of the interface
- Changes to implemented code do not force rewrites of the tests
    *Depending on interfaces lets you use test to defer design decisions safely w/o penalty*

***KEY TERM:*** LEVELS OF ABSTRACTION

- Degree of detail or complexity in a system's design
- The more abstract an object is, the less it depends on the details of other objects or its surrounds to function

SUPPORTING ABSTRACTIONS

- Change the code to increase levels of abstraction when more information arrives
- Abstractions are flexible design components, but improvements provided come at a cost:
- Each individual abstraction may be easily understood, but there is no single place in code that makes obvious the behavior of the whole
- Code base expands --- # of abstractions grows & tests become increasingly necessary
- Allow you to put off design decisions and create abstractions to any useful depth

EXPOSING DESIGN FLAWS

- If a test requires painful setup --- code expects too much context
- If testing one object drags other tests into the mix --- code has too many dependencies
- If test is hard to write --- other objects will find the code difficult to reuse
- When design is bad, testing is hard
    *The inverse isn't guaranteed to be true*
- For tests to lower your costs, both the underlying application and tests must be well-designed

### INTENTIONAL TESTING: Knowing What To Test -----------------------

- Removing duplication from testing lowers cost of changing tests in reaction to application changes
- Putting tests in the right place guarantees they're be forced to change only when necessary
- Have a very clear idea about what you intend to test
- Well-designed objects have strong boundaries
  - Nothing on the outside can see in
  - Nothing on the inside can see out
  - Only a few explicitely agreed upon messages can pass through pre-defined airlocks
        *Willful ignorance of the internals of every other object is at the core of design.*
- Treat objects as if they are only and exactly the messages to which they respond to design changeable applications.
- Design principles being enforced in application should apply to tests as well
- Each test = another appplication object that uses an EXISTING class
  - The more a test is coupled to a class, the more entangled they become.
        *Test becomes more vulnerable to being unnecessarily forced to change.*
  - Limit couplings to a few and allow them to be stable
- Tests you write should be for messages defined in public interfaces

***KEY TERM:*** COUPLING

- The degree of interdependence between software modules;
- A measure of how closely connected two routines or modules are;
- The strength of the relationship between modules

--- STOPPING POINT --- PAGE 196 (03/20/2023) ---
