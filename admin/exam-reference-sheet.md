<frontmatter>
title: "Exam Reference Sheet"
</frontmatter>

<include src="uml-reference-sheet.md#main" />

# Software Engineering

* Pros: 1. joy of making things 2. pleasure of making things that are useful to other people 3. fascination of fashioning complex puzzle-like objects of interlocking moving parts 4. joy of always learning 5. delight of working in such a tractable medium.
* Cons: one must perform perfectly 2. other people set one's objectives, provide one's resources, and furnish one's information 3. designing grand concepts is fun; finding nitty little bugs is just work 4. debugging has a linear convergence, or worse 5.the product over which one has labored so long appears to be obsolete quickly

# OOP

* Objects in OOP is an abstraction mechanism because it allows us to abstract away the lower level details and work with bigger granularity entities
* An object is an encapsulation of some data and related behavior in terms of two aspects
* Inheritance: defining a new class based on an existing class
* Polymorphism: The ability of different objects to respond, each in its own way, to identical messages.

associations: connections between objects/classes

navigability: unidirectional, bidirectional

a dependency is a need for one class to depend on another without having a direct association in the same direction.

A composition is an association that represents a strong whole-part relationship. Composition implies 1. delete cascading 2. no cyclical links

Aggregation represents a container-contained relationship.

An association class represents additional information about an association.

Inheritance: A superclass is said to be more general than the subclass.

Multiple Inheritance is when a class inherits directly from multiple classes.

Method overriding is when a subclass changes the behavior inherited from the parent class.
Method overloading is when there are multiple methods with the same name but different type signatures.

An interface is a behavior specification.

An abstract class is a class that merely a representation of commonalities among its subclasses in which case it does not make sense to instantiate objects of that class. An abstract method is a method signature without a method implementation.

Substitutability: Every instance of a subclass is an instance of the superclass, but not vice versa.

Dynamic binding (aka late binding): method calls resolved at runtime.
Static binding (aka early binding): method calls resolved at compile time.

# Requirements

Projects can be greenfield or brownfield.
Projects have stakeholders

Functional requirements:  what the system should do.
Non-functional requirements: the constraints under which the system is developed and operated. easier to miss, but critical to success.

Requirements should be

Unambiguous
Testable (verifiable)
Clear (concise, terse, simple, precise)
Correct
Understandable
Feasible (realistic, possible)
Independent
Atomic
Necessary
Implementation-free (i.e., abstract)

Consistent
Non-redundant
Complete

* Gathering: Brainstorming (to generate a large number of diverse and creative ideas), user surveys, observation, interviews, focus groups, prototyping, product surveys
* Specifying: prose, feature lists, user stories, use cases, glossary, supplementary requirements

Example user story

Example use case

# Design

* Abstraction: establishing a level of complexity we are interested in, and suppressing the more complex details below that level.<br>
  data abstraction, control abstraction

* Coupling: degree of dependence. X is coupled to Y if a change to Y can potentially require a change in X
* Cohesion: how strongly-related and focused the various responsibilities of a component are

# Architecture

Architecture styles: n-tier (layered), client-server, transaction processing, service-oriented, event-driven

Design patters: Singleton, Facade, Command, Model-view-controller, Observer

Design approaches: top-down, bottom-up, agile

Code quality guidelines:

* Avoid long methods, deep nesting, complicated expressions, magic literals.
* Make the code 'obvious'. Structure code logically. Do not trip up the reader. Keep-It-Simple-Stupid.
* Avoid premature optimisations.
* Use SLAP (Single Level of Abstraction Principle).
* Make the happy path prominent.
* Follow a standard.
* Naming: Use nouns for things and verbs for actions. Use standard words. Use name to explain. Not too long, not too short. Avoid misleading names.
* Avoid 'unsafe' practices: Use a default branch. Don't recycle variables/parameters. Avoid empty catch blocks. Delete dead code. Minimise scope of variables. Minimise code duplication.
* Comments: Don't state the obvious. Write to the reader. Explain WHAT and WHY, not HOW.

Refactoring: restructuring code in small steps without modifying its external behaviour.

Documentation: Go top-down, not bottom-up. Favour for comprehensibility over comprehensiveness. Document minimally but sufficiently.

Error Handling:

Exception: An event that disrupts the normal flow of the program's execution. Caused by user behavior or issues in the environment. Recover if possible.

Assertions: Assumptions about the program state so that the runtime can verify them. Assertions fail due to programmer errors. Should terminate the execution.

Defensive programming: if you leave room for things to go wrong, they _will_ go wrong.

Integration:
* Late-and-one-time vs early-and-frequent (preferred)
* big-bang vs incremental (preferred)
* Continuous Integration (CI) vs Continuous Deployment (CD)

Reuse: API vs Library vs Framework (follows the hollywood principle) vs Platform (has a runtime)


# Quality Assurance

Quality Assurance = Validation (are you building the right system?) + Verification (are you building the system right?)

* Static analysis: Static analysis is the analysis of code without actually executing the code.
* Dynamic analysis requires the code to be executed to gather additional information about the code.

Formal verification uses mathematical techniques to prove the correctness of a program.

* Regression testing: the re-testing of the software to detect regressions.
* Unit testing: testing individual units.
* Integration testing: testing whether different parts of the software work together.
* System testing: take the whole system and test it against the system specification. Includes testing against non-functional requirements. Can also test that the system fails 'gracefully' when pushed beyond its specified limits.
* Alpha testing is performed by the users, under controlled conditions set by the software development team.
* Beta testing is performed by a selected subset of target users of the system in their natural work setting.
* Dogfooding is when creators use their own product in order to experience how end users experience the product.
* Acceptance testing: test the system to ensure it meets the user requirements.

Stubs can isolate the SUT from its dependencies. Dependency injection can be used to replace dependencies with stubs. Developers often use a hybrid of unit+integration tests to minimize the need for stubs.
A test driver is the code that ‘drives’ the SUT for the purpose of testing

* Scripted testing: perform testing based on pre-defined set of test cases.
* Exploratory testing: design test cases on-the-fly.

Test-Driven Development(TDD): evolving functionality and tests in small increments, while writing the test before the functinal code.

Coverage:

* Function/method coverage: based on functions executed e.g., testing executed 90 out of 100 functions.
* Statement coverage: based on the number of lines of code executed e.g., testing executed 23k out of 25k LOC.
* Decision/branch coverage: based on the decision points exercised e.g., an if statement evaluated to both true and false with separate test cases during testing is considered 'covered'.
* Condition coverage: based on the boolean sub-expressions, each evaluated to both true and false with different test cases. Condition coverage is not the same as the decision coverage.
* Path coverage measures coverage in terms of possible paths through a given part of the code executed.
* Entry/exit coverage measures coverage in terms of possible calls to and exits from the operations in the SUT.

Testing should be effective (find a high percentage of bugs) and efficient (a high rate of bugs found/test cases)