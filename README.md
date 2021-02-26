# CS Basics
Covers basic computer science ideas in brief

## Functional programming

TODO

Subset of declarative

Possibly [this](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)?

## SOLID

The goal of SOLID is the creation of mid-level software structures that tolerate change, are easy to understand, and are easily used for multiple purposes.

* ***S**ingle Responsibility Principle:* Each piece of software in any corporation is overseen by one individual, so that each module has one, and only one, reason to change. (The best way to make this possible is for the software to reflect the org's social structure). Corollary to [Conway's law](https://en.wikipedia.org/wiki/Conway%27s_law).
* ***O**pen-Closed Principle:* Add new code instead of changing existing code. This is "extensibility".
* ***L**iskov substitution principle:* Software modules must adhere to a common contract in order to have interchangeable parts.
* ***I**nterface Segregtion Principle:* Software modules shouldn't depend on things they don't use.
* ***D**ependency Inversion Principle:* High-level policy code should dictate low-level details, not vice versa (like in the old days).

## Types of programming

* Imperative: statements change a program's state ([src](https://en.wikipedia.org/wiki/Imperative_programming)).
  * Golang is imperative and pro ([link]()
* Procedural: the language makes use of sets of commands, called procedures, which can be invoked in any order the programmer pleases. These are an extension of imperative languages, since procedures are just reusable sets of imperative statements.
* Declarative: the programmer uses the language to specify **what** should be done, as opposed specifying **how** it should be done.
  * SQL, HTML, React are declarative
    * SQL declares what information should be retrieved, not how the DB engine should retrieve it 
    * React declares what should be done to the DOM, not how it should be done
  * Great article [here](https://ui.dev/imperative-vs-declarative-programming/) and [here](https://codeburst.io/declarative-vs-imperative-programming-a8a7c93d9ad2).
* Functional: a form of declarative programming, except that all calls are done via [pure functions](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976) and all state is immutable.
  * Functional programming leverages a set of expressions that map values to other values ([source](https://en.wikipedia.org/wiki/Functional_programming)).
  * Advantages of functional programming are listed [here](https://medium.com/@geisonfgfg/functional-go-bc116f4c96a4).
