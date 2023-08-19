

************************
Craftsmanship
************************

What Scrum forget was that you cannot have speed without quality. You cannot have speed while you are carrying technical debt. And the more technical debt you will carry, the slower you will go. And this is a horrible wicked circle, because the slower you go, the more technical debt you will acquire.

Because of this, another movement was born – the Software Craftsmanship movement. This is an evidence of a split in the community. A group of us felt it was necessary to re-assert the values of eXtreme Programming into this world that was now dominated by Project Manager Scrum Master Scrum. We hope that is a reawakening of Kent’s vision. I’m not sure there is any evidence to this effect.

https://www.aaron-gray.com/a-criticism-of-scrum/

Responsibility
===============

Team playing
=============

improvement
============



******************************
Hypothesis-Driven Development
******************************


************************
CI/CD 
************************
Tight feedback loops between conception development deployment



************************
TDD
************************
Tests as executable requirements that lead to less fear of breaking things, easier changes, increased transparency, etc.

3 Rules of TDD

1st Rule of TDD:
Do not write any production code without a failing test first:

2nd Rule of TDD:
Write only enough test code as is sufficient enough to fail 

3rd Rule of TDD:
Only implement a minimal code that makes the failing test pass.


Unit tests run fast. If they don't run fast, they aren't unit tests.

Other kinds of tests often masquerade as unit tests. A test is not a unit test if:

    It talks to a database

    It communicates across a network

    It touches the file system

    You have to do special things to your environment (such as editing configuration files) to run it

Tests that do these things are integration tests, not unit tests.


Mock Objects

Mock objects are a popular tool for isolating classes for unit testing. When using mock objects, your test substitutes its own object (the "mock object") for an object that talks to the outside world. In doing so, it avoids time-consuming communication to a database, network socket, or other outside entity.


Focused Integration Tests

Unit tests aren't enough. At some point, your code has to talk to the outside world. You can use TDD for that code, too.

A test that causes your code to talk to a database, communicate across the network, touch the file system, or otherwise leave the bounds of its own process is an integration test. The best integration tests are focused integration tests that test just one interaction with the outside world.

End-to-End Tests
End-to-end tests exercise large swaths of the system, starting at (or just behind) the user interface, passing through the business layer, touching the database, and returning. Acceptance tests and functional tests are common examples of end-to-end tests.



****************************************
Acceptance test driven development ATDD 
****************************************
"More agile testing" p.149

****************************************
Behaviour driven development BDD 
****************************************
"More agile testing" p.149

****************************************
Specification by example SBE 
****************************************
"More agile testing" p.149


************************
Customer Involvement
************************
Let users speak for themselves



************************
Clean Code
************************
How to write for others, in order to read, understand, and modify. It helps with transparency, communication, trust, etc.

What Clean Code is about:

- Definition
- Main sources
- Central ideas

Note that the ideals below pertain to design more than anything else. Still they have synergies with clean code as an overall concept.
Five things that matter in making the code easy to change:
1.Modularity
2.Cohesion
3.Separation of concerns
4.Abstraction / information hiding
5.Loose coupling



The secret for good design is simplicity. Your code has the following properties:
it works
it communicates clearly
there is no duplication
there are no extra pieces




************************
Technical Debt
************************
As one has to pay for financial debts, so too one has to pay for technical debt.



************************
Last responsible moment
************************
Delay important decisions up to the last responsible moment, until you really need to make them

As we said previously, everything revolves around the ability to respond to changes, fast. Since the work is being done incrementally in small batches, without a detailed upfront plan, some rework is inevitable. For that reason minimizing rework while maximizing feedback is the central concern of the agile team. The last responsible moment is the sweat spot; too early and the team risks to make decisions without validation; too late and there will be a lot of rework. 

Rework is, at its core, caused by having to undo decisions that have been made in the past.

Rework is triggered by learning new things that invalidate prior decisions
