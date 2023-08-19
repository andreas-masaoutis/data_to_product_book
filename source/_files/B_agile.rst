


************************
What is Agile?
************************

Agile
======

Let us start with a short and simple definition of what Agile is. It is the iterative and incremental creation of software, led by continuous feedback from users and stakeholders. That's all there is to it. 

Agile means different things to different people. Actually, it came about as a point of convergence for various practices like RAD, XP and Scrum among others that were developed in the 1990's. The Agile Manifesto was put forward in 2001 and we can interpret it, in a sense, as the common denominator of the various practices that were circulating in the software engineering market at that time. Agile is what disciplined people had already been practicing in the wild. For that reason we will start with the Manifesto itself.  Here `Agile manifesto <https://agilemanifesto.org/>`_ one can find the original publication from 2001. 

  Manifesto for Agile Software Development

  We are uncovering better ways of developing software by doing it and helping others do it.
  Through this work we have come to value:

  - Individuals and interactions over processes and tools
  - Working software over comprehensive documentation
  - Customer collaboration over contract negotiation
  - Responding to change over following a plan

  That is, while there is value in the items on the right, we value the items on the left more.

Although this is short, there is a lot to unpack.

First, we should note that the signatories of the manifesto had already developed various ideas during the 1990's :
Sutherland and Schwaber had proposed scrum
Beck, Jeffries and Cunningham had developed the eXtreme Programming practices
Cockburn had proposed the Crystal family of methods
Beck had proposed the test first methods
Fowler had worked on Design patterns and refactoring
Martin had worked on patters and the concept of Clean Code


The next thing to note is how the Agile Manifesto is a contraposition against the then prevailing software engineering practices in the corporate world. There would be two parties, that would create a detailed plan with the full requirements, captured in the extensive documentation and the Gantt Chart with the milestones, that should then be followed, with the hand-offs and sign-offs and the subsequent litigation in case something did not worked as planned.
Of course, we should not interpret the manifesto as an 'a priori' argument against the Waterfall approach but rather as one about its suitability in the new market conditions. It might have been ok to build software in that way for space missions in the past, but it is not suitable anymore in the kinds of projects the developers had to deal with. There are at least two changes that had rendered the heavy-weight project management processes of the past unsuitable.

First, time-to-market mattered in a disruptive environment. Instead of taking longer to build a perfect piece of software, it was a great competitive advantage to be the first to offer something - even if that was not perfect.
In relation to that, the requirements captured and the contract signed some time ago, was not ideal; rather it would be far better to have the customer involved.

It doesn't seem a coincidence then that the 17 participants chose the word agile to describe their movement; everything revolves around the ability to respond to changes, fast. 



In the next sections we are going to take a look at some of the approaches that led to the Agile Manifesto.

Interesting resources

Engineering Software Products: An Introduction to Modern Software Engineering, 2020, by Ian Sommerville.
In chapter 1, Sommerville gives a short historical explanation on why the concept of Project dominated the software engineering field since the 1970's and how the focus have changed to Product. These changes provide the canvas for the Agile movement.

Practices of an Agile developer, 2006, by Subramaniam and Hunt.
This book is somewhat old, but not dated, in that it provides a lot of practical considerations of what agile software development is in practice.


eXtreme Programming (XP)
=========================


What eXtreme Programming is about:

Using test first, was a change in that the developer was taking full responsibility for the quality of the code, rather than just passing it over to the QA team.
In the end of the day everything is about thw working program. 

Beck uses the triad values, principles, practices to explain XP.
values:
communication
simplicity 
feedback 
courage 
respect

principles:
incremental improvement 
principle of flow 

practices:
pair programming
TDD
continuous integration 


Historical remark
XP, late 90's, seems to have splintered / grown into various directions:
DEVOPS, with the focus on automation
Craftsmanship, with the focus on quality
LEAN, with the focus on delivering value
XP is not just the agile technical practices, it contains the seeds of later 'movements'. Nowadays that some of the early XP practices have grown into their own 'fields' it is easy to think that XP is just TDD and refactoring.
Out of the original proposed practices, some thinks caught on and are todays common ground, like 40 hour week and the short releases, some practices did not do so well like the on-site customer, and others have evolved into their own like continuous integration anf the CI/CD paradigm.


list of XP practices (1999 version - include graph for the relations between them )
on-site customer
metaphor
planning game
short releases
continuous integration
collective ownership
coding standards
pair Programming
testing
refactoring
simple design
40 hour week

What modern XP looks like
traditional practices:
- site customer
- user stories
- test first
- pairing
- design improvements
- collective ownership
- continuous integration
- velocity
recent additions:
- domain driven 
- UX
- support 
- learning 20%
- story prioritisation
- mobbing
- retrospectives
- continuous deployment 
- infrastructure

In other words, simultaneous continuous everything,

Continuous integration means trunk based development with feature toggles, or feature branches or minimal duration

- Definition



Main sources:
- `eXtreme Programming <https://www.digite.com/agile/extreme-programming-xp/>`_






LEAN
=====


What Lean is about:

- Definition: lean manufacturing rested on a deep understanding of what creates value, why rapid flow is essential, and how to release the brainpower of the people doing the work.

Lean is a pull model, rather than a push one (toyota vs ford)

The question in not can we build that, but rather should we do so?

Many agile practices like short cycles, non-negotiable quality, regular retrospectives, pulling work from a "backlog," come from Lean.

In this book we hope to change the software development paradigm from process to people, from disaggregation to aggregation, from speculation to data-based decision making, from planning to learning, from traceability to testing, from cost-and-schedule control to delivering business value. Mary Poppendieck



(the project paradigm is based on the assumption that what we plan to build is the correct/valuable thing to do. at Amazon, for example, it is a common practice to evaluate every new feature, yet the success rate is below 50%. Online Experimentation at Microsoft. Kohavi at all. https://ai.stanford.edu/~ronnyk/ExPThinkWeek2009Public.pdf)
## The biggest waste in software development is to build things that do not contribute value to the product
Building things that do not bring value is wasteful in 3 ways:
- The opportunity cost of not building something of value
- The maintenance cost for the zero value features, 
- plus the added complexity to the overall design that makes it more difficult to add valuable features

  

What we should do by Jez Humble 

don't optimise for the case where we are right, as most of the times the features that we plan to build do not bring value
focus on value instead of cost, since as Douglas Hubbard showed in The IT Measurement Inversion https://www.cio.com/article/274975/it-organization-the-it-measurement-inversion.html the single most important factor is whether a project will be cancelled and whether people will actually use it.
create feedback loops to validate assumptions
make it economics to work in small batches
enable and experimental approach to product development


- Doing your user research
  Two axis: quantitative vs qualitative and generative vs evaluative
  quantitative and generative: run a customer/product survey to find out about something related to your customers / products
  quantitative and evaluative: a/b testing, user/product analytics, key metrics
  qualitative and generative: Follow-Me-Home
  qualitative and evaluative: usability testing



What the Lean movement has used for years in process improvement, can be used in software engineering. This is possible because software, in contrast to, say, buildings, can be valuable even if not complete. 

The HP example

in order to change you need clearly defined and measurable goals, along with a well established experimental approach. Try X, assess whether it took you closer to your goal, recalibrate, and then rinse and repeat. This not only works for software, it also works for processes.



Eric Ries with the 'Lean Startup' did not just focus on the programmers but described cycles of learning for everybody that is involved in building software. 


Jez Humble the water-scrum-fall https://www.youtube.com/watch?v=2zYxWEZ0gYg


Scrum
======


What Scrum is about:

Scrum is a process not an engineering methodology 

The central tenet of Scrum is to produce a Done increment in a sprint.

The definition of Done is actually defines the way the whole of the project moves on:

Dumb definition from a purely technical perspective
Pair programming
TDD
Refactoring 
user acceptance testing 
continuous integration ( unit, deployment, build, integration, and regression tests )
performance testing

Done definition from the product perspective 
Clean code base 
Valuable functionality only 
Architectural conventions respected 
according to design/style/usability guide 
Documented 
Service levels guaranteed



Main parts
Product backlog
Iteration 
valuable increment potentially releasable
feedback

Three artifacts
product backlog
sprint backlog
and done increment

Four events
sprint planning once per iteration:
- sprint goal
- The Sprint Goal, the Product Backlog items selected for the Sprint, plus the plan for delivering them are together referred to as the Sprint Backlog.
- sprint plan: how the work is going to be done
    
daily scrum one per day:
- 15 minute meeting
- what have we done, what we are going to do, impediments
- actionable plan for the rest of the day
(backlog refinement) as necessary:
- during the sprint, and given the work done and the feedback that might arrive, the PO and possibly the team, elaborate the items of the product backlog, and the sprint backlog if necessary

sprint review once per iteration:
- inspect the outcome
- demonstrate the outcome
- adjust product backlog

sprint retrospective:
- assess the work of the team
- look for ways to improve quality and team effectiveness


In the end, if you adopt Scrum as a process, without the engineering methodology, it will not do much.



Kanban
=======

What Kanban is about:

By managing queues, limiting work-­‐in progress and batch sizes and building a cadence through a pull system (limited WIP) versus push system (non-­‐limited WIP) we were able to expose more defects and execute more timely resolutions. On the other hand “pushing” a large batch of requirements and/or starting too many requirements delays discovery of defects and other issues; as defects are hidden in incomplete requirements and code.



************************
The core concepts
************************
The goal here is to present some fundamental ideas/concepts that shed light to thw whole topic. These ideas underlie both the Agile concepts we presented in the previous section, and at the same time teh actual implementation of Agile that we will present in subsequent sections.


************************
A brief description
************************
From vision to CI/CD 
Two main questions:
- How to build the right thing
- How to build the thing right

Different lifecycles; it's not one size fits all


Principles we should adhere to:
 - Customer value is business value
 - Work in short cycles instead of trying to predict the future. Shorter cycles means lower investment, lower costs, lower risk
 - Evidence based decision making (MVPs, experiments). 1-What is the next most important thing we need to learn - where lies the highest risk of ignorance? That might be something technical or user related. 2- What is the least amount of work we need to do so that we learn that?
 - Retrospectives: improve the product, improve the process
 - Go and See. Find the amplify the good patterns that work. 
 - Test high-risk hypothesis
 - Do less, more often
 - Work as a balanced team. Small, dedicated, co-located, cross-functional, autonomous, empowered 
 - Transparency: what do we work, why, how are we doing, what success looks like. It can come up with rituals like stand-ups, and demos. Access to data, from the company side
 - Bring learning part of the backlog

The technical core 

Example of the time - money - scope (- quality) triangle (pyramid)
Why it does not work like that in software engineering
How the price mechanism works to get things done
Agile is bringing engineering to the core of decision and organisation rather than using financial accounting.
How it works in practice: for this functionality it will take so much time
Saving on the key engineering practices that all developer should know and strive for (e.g, continuous integration ) will actually do much more harm than anything else.


Create the vision
Set up a road-map
Build a team, if not already in place, or modify existing one
Collect user stories (while the stories are being developed, keep adding new ones and elaborate the existing ones )
From enough user stories, figure out the following

    all the non functional requirements that are implied rather than explicitly stated in the stories
    the suitable architecture, as a rough sketch
    the coding standards, and everything else the determines the project, like language, frameworks, etc

    the test plan with
        the user acceptance tests from the user stories
        the integration tests that should follow the architecture and fit at the seems of the modules
        the unit tests at the lowest level possible
        the performance tests

Start out with an architectural spike and place all the 'modules' in place

work with the Red-Green-Refactor cycle
    write some failing tests, according to the testing plan
    write the code to make the tests pass, trying to follow the principles like DRY, SOLID, etc
    refactor the code: detect code smells and try to rectify them using the specific patterns available
    refactor the architecture: whenever needed modify the architecture

use the definition of DONE ta make sure that each story is up the selected standards, like with documentation written 
use the ci/cd pipeline to integrate and deploy the code
collect feedback from the users using metrics and other techniques
periodically, inspect and adapt, both the processes and the direction of the project



****************************
The institutional framework
****************************
Compatibility and incompatibility between the Business Model and Agile development


************************
Places that work Agile
************************
A list of places that use Agile and how they do it.



************************
Criticism of Agile
************************

 Why Agile Fails in Large Enterprises - Large Scale Agile Transformation 
 https://www.youtube.com/watch?v=Oo3zlOTbN2E

http://www.my-project-management-expert.com/the-advantages-and-disadvantages-of-agile-scrum-software-development.html


************************
Internal divisions
************************
martin fowler - the Agile Industrial Complex https://martinfowler.com/articles/agile-aus-2018.html

What Scrum forget was that you cannot have speed without quality. You cannot have speed while you are carrying technical debt. And the more technical debt you will carry, the slower you will go. And this is a horrible wicked circle, because the slower you go, the more technical debt you will acquire.

Because of this, another movement was born – the Software Craftsmanship movement. This is an evidence of a split in the community. A group of us felt it was necessary to re-assert the values of eXtreme Programming into this world that was now dominated by Project Manager Scrum Master Scrum. We hope that is a reawakening of Kent’s vision. I’m not sure there is any evidence to this effect.
https://www.aaron-gray.com/a-criticism-of-scrum/

