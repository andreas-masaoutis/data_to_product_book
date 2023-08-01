FROM DATA TO PRODUCT
^^^^^^^^^^^^^^^^^^^^^


#################
PART 1: The core
#################

***********
Preface
***********

Hello there.

This piece of work aims at being sort of an introduction to software engineering - or in simple terms how software is being built. It is thought of as a one-stop solution to the question: how can I build a software application? Obviously, you cannot expect any zero-to-hero solution from a ebook - besides, it being offered for free, means there is no incentive for sales-increasing catch phrases. What you have on your screen is more like a manual or a practical introduction to the subject; a survey of themes on concepts, tools and processes that comprise software engineering.

Why would someone need such a book? Well, I can tell you how I felt the need for it. After being introduced to programming during my PhD studies, and having spent some years learning things, I started having the feeling that I need to pass to the next level: how do I build a complete software system? It is like learning any new language; it's one thing to learn it and completely another to compose an essay in that language. You need to know the language, but composing an essay is much more than just knowing the syntax. In a similar manner, after having learnt the fundamental concepts of programming, and the syntax in Python, and having worked with some libraries, and having built toy projects, it was about time to build something for real. I went through books and various online sources on software engineering, on specific topics and frameworks, on tools, but I would still be at a loss. How can I put all this together? How do people actually build software? That's what this book is about. An exposition of all the necessary preconditions, tools, processes that should posses and use in order to build a piece of useful real-word software. 
Additionally, the books that I started with, the standard academic textbooks on Software Engineering were describing something that was not suitable for me. How was I supposed to do all this comprehensive and extensive analysis beforehand, when I wasn't even really sure of what I wanted to build. That's what got me into Agile.

Who could possibly benefit from the book? There are a couple of `personas` which would, hopefully, find this book useful:
   - A recent graduate from a computer science related program, than knows how to program and the fundamental of software engineering and would benefit from seeing how everything fits together. Possibly a final year student doing a final project that entails building an application.
   - A self-taught programmer, or an aspiring one, could get an idea of the array of concepts and tools that has to master in order to deliver an application.
   - An experienced software engineer leading a team, that won't learn anything new per se, but could use this as a source for helping junior colleagues get on-board and up to speed.
   - A manager responsible for a team of developers or an entrepreneur with an idea and the funds, but lacking the technical skills. Both would benefit from an understanding of the subject, when dealing with developers.


You could think of this work as a seed. A team can use it to 'plant' a small software product, and use the instructions to make it grow. Of course, being faithful to the Agile spirit, the team can change any of the 'prescriptions' offered; actually the team should spend the time to modify and improve the way the team works. the value of this work is that offers every little part that is needed to make and grow a software product, just like a seed.

*************
Introduction
*************

# The fundamentals of building software 

## The Software Development Life Cycle (SDLC)

No matter what the preferred software engineering methodology is, all of them are organised efforts to address a set of fundamental questions with respect to the development of a software. In other words, no matter in which way, when delivering a software system we are going to do the following. Let's see:

Software development is fundamentally about the following:
The identification and definition of the problem from the social/user perspective
The understanding of the problem that we need to solve from a technical perspective (requirements)
The development of the software system that solves that problem (development)
The checks that make sure that the problem we needed to solve has indeed been solved (testing/quality assurance)
The transfer of the software solution to the end user
The maintenance of it

The above can be further analysed into separate phases, `Wikipedia <https://en.wikipedia.org/wiki/Systems_development_life_cycle>`_ has the example of a ten-phase version of the cycle, but that level of abstraction is good enough for our purpose.

The purpose of this work is to present a way to organise activities, that span all these different phases, in a coherent and effective way.

In a nut shell, the Agile with its proposal for an iterative and incremental approach tried to challenge the sequential way in which software was being built until the late 90's.

We'll start by noting tht Agile came as a reaction to the prevailing practices in the software industry at that time. 

The main characteristic was the plan-driven, sequential approach known as the waterfall method. The waterfall grew out of the need to have a structured way of producing software, around the 1970's. We are talking of an era of the mainframe computer, where the software and hardware were produced in tandem, owned and operated by a few large institutions, and relatively few software engineers worked with computing languages that were closer to the 'metal' with less abstractions and tools. In that framework, the argument for detailed upfront specification made perfect sense. On the business side, we should keep in mind that these software systems tended to be about the internal processes of their owners, such as payroll systems for large corporations. Usually, these systems were built by external contractors that had the engineering knowledge to do so.

At the turn of the century many things had changed. The internet connected personal computer had substituted the mainframe, it became ubiquitous meaning the span of applications moved towards the average consumer, the new Operating Systems handled most of the interactions with the hardware thus freeing the software applications from having to deal with it. And of course, on the business side, we should keep in mind that the software systems started to be the product itself, be it in the form of an application or service. And these systems were now more often built and maintained by a mixture of internal teams and external contractors.

Bob Martin in of his conference talks[https://www.youtube.com/watch?v=FedQ2NlgxMI] claims that one of the reasons for the introduction and widespread use of the waterfall model, from the early 1970's to the turn of the century,  was the change in the composition of the developers workforce with the influx of many young university graduates that lacked professional experience and consequently had to be managed in a strict way.


Deloitte’s Agile Tube Map
The Agile Landscape - v3, by Deloitte
One of the problems with the Agile landscape is the vast assortment of frameworks, techniques, processes, and ideas that fall under the rubric of Agile. There is a 2016 interesting infographic by Deloitte that represents the Agile landscape as a London Tube map, where lines represent frameworks like Lean, tube stations are specific techniques and concepts like refactoring, while 'geographic' areas represent phases in the Software Development Life Cycle like Release. It is quite massive with 6 'geographic' areas, 25 different lines, and around 300 techniques and concepts. That gives an idea of how Agile is more like an umbrella concept; and a quite big one. 

.. figure:: images/agile_landscape_v3.jpg
    :width: 715px
    :align: center
    :height: 550px
    :alt: alternate text
    :figclass: align-center

    The Agile Landscape v3, by Deloitte, 2016 

What becomes immediately obvious is that it is not possible to summarise such a field with an introductory work. To be honest, I believe that, if any, there will be just handful of people around the world that are proficient will all of these ideas. For that reason we will limit ourselves to identifying some of the core concepts, and follow them all the way to practical application. This will not be any kind of definitive guide on Agile, it will be a humble and simple exposition of some core ideas.



************************
Terms and their history
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


####################
PART 2: The concepts
####################



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


####################
PART 3: The people
####################

************************
The Agile mentality
************************
proactive, independent, empathetic, etc.

Mastery, Autonomy & Purpose
To motivate employees who work beyond basic tasks, Pink believes that supporting employees in the following areas will result in increased performance and satisfaction:

    Autonomy – A desire to be self directed, it increases engagement over compliance.
    Mastery – The urge to get better skilled.
    Purpose – The desire to do something that has meaning and is important. Businesses that only focus on profits without valuing purpose will end up with poor customer service and unhappy employees.[5]
https://techbeacon.com/app-dev-testing/organizing-your-agile-teams-think-autonomy-mastery-purpose


************************
The skill set
************************
T-shaped individuals for cross functional teams


************************
Self-organising Teams 
************************
Whatever that means
How the team could be organised.

https://www.youtube.com/watch?v=IDKJJDiK3Gw
Rachel Davies at Unruly GOTO 2015
https://unruly.co/

One of the ways to organise the team is to have a set of broadly skilled people, that have collective ownership of the code and the product. Everyone can commit to the main which means they should be accountable. There are no separate groups of people that do the testing or maintain the infrastructure; the teams do that. And there is no layering of people and access to data.
Also these is no buffering between the business and the developers. The connection is immediate with the business and the product. There are no dedicated business analysts, product owners, or testers. these are all functions covered by the team members, and as a result there is no need for large teams 4-6 people is enough. Each team member does a certain amount of story research; they talk to the business and try to figure out what the needs are, and then they do the technical research on the available options, that will finally be presented to the rest of the team and stakeholders for decision to be made. The team's time is split between new story development, maintenance/technical improvement of the existing system. The teams are not entirely collocated and therefore there is the need for online boards to keep track of the work planned and done. All developers in the team can spent one day per week for learning, not necessarily on the immediate needs of the product. The team is tracking its activities, since there are no project managers to manage things around, so that the team can then inspect and adapt. With the retrospective the team has the 'ability' to decide what to track, how to measure the performance and what steps to take in order to improve. Collective ownership also extends to processes. The team makes things happen without relying onto any kind of specialist. The team does have specialists, but they are there to work with the teams and teach the teams. It's not a case of the specialist does a special thing. With cross-functional teams there are fewer bottlenecks. Additionally the teams are fluid with team members rotating between the various teams, every x number of months. In the end, 1. the teams deliver value in a sustainable manner, so that the management can be reassured that things do work without having to manage things closely. Also, 2. the teams build change tolerant systems that are easier to modify. Finally, 3. the choice over what to do, makes it easier for team members to relate to the business needs, it means that people acquire more skills of greater variety by constantly learning, that makes their work more fulfilling, and as a result they stick with the team for far longer.


The team is the locus of business problems, technical solutions, and organisational processes
Why Agile Fails in Large Enterprises - Large Scale Agile Transformation 
https://www.youtube.com/watch?v=Oo3zlOTbN2E 15:59

************************
The roles
************************

- Stakeholders
- Product Owner
- Developers
- Scrum Master
- Tech Lead


############################
PART 4: Tools and Processes
############################


************************
Pre-Coding
************************


Product Vision
==============================

Business Model Canvas
==============================

Roadmap
==============================

Persona
==============================

User Story
==============================


What are the User Stories, how to write them, and use them:

- What are they:
    A user story, as a placeholder for discussion, facilitates it by describing the problem we want to solve with the software, who will use it, why and how they will use it. The discussion then is about arriving at a solution to the problem while at the same time creating a shared understanding among the participants.

Stories help us separate WHAT the system should do from HOW is will do it.
- How to write them
Writing stories just passively formulating requested solutions is a practice that dangerously nears Henry Ford's paradox: "If I had asked people what they wanted, they would have said faster horses".

The traditional user story framework is focused on capturing requirements for what we want to build and for whom, to enable the user to receive a specific benefit from the system. It has the following format:

As A…. <role>
I Want… <goal/desire>
So That… <receive benefit>


- How to use then

- Common mistakes with user stories https://www.youtube.com/watch?v=0HMsh459h5c:
    1.Direct translation from traditional 'requirements': A user story is a description of the problem we are trying to solve from the perspective of the user - it is not a tecnical specification. If the story only conveys the technical part and not the user need and context, the developers cannot do a good job even if the have good technical skills, as they will not understand what they are trying to solve.  The job of a software developer is not to write code, is to solve problems; in order to do so one needs to understand it. 
    2.Too detailed stories that read as a contract. A story instead should be like a placeholder for a conversation. As the story is being born out of the realisation of a need, it should focus on the exactly that: the need of the user. It will later be used for the discussion between the product owner and the developers where the latter will contribute on the technical aspects of the solution. A too detailed story that goes all the way down to the details stiffles the discussion and the possibility to innovate. Instaed, it is the discussion that will lead the team to figure out the best way to implement the story
    3.Too large stories. Good user stories identify a useful unit of work. For story to represent easily and rapidly produced new functionallity it should be a small increment in the behaviour of the system. Maximum time for story completion should be within a sprint, something like a week or two. Ideally, they should be shorter, like a day or two.
    4.Value vs invaluable. Stories represent value to the user. They do not have to be the killer feature that does everything and even more. As with the large stories, invaluable stories tend to be overcomplicated, while as we said before it is far easier to work with smaller and simpler ones. First story could be create simple login, then require more secure password, address lost passwords, periodically reset passwords, etc.
    5.Dependent stories. Ideally, stories should be implementable in any order, although some might more difficult to implement than others



Enter validation and we have Hypothesis-Driven Development:
Practicing it is thinking about the development of new ideas, products and services – even organizational change – as a series of experiments to determine whether an expected outcome will be achieved. The process is iterated upon until a desirable outcome is obtained or the idea is determined to be not viable.

An extension to the traditional user story with the structure to support Hypothesis-Driven Development would be the following

We believe that <this feature> <for these users>

Will result in <this outcome>

And We will know we have succeeded when <we see a measurable signal>


What functionality we will develop to test our hypothesis? By defining a ‘test’ capability of the product or service that we are attempting to build, we identify the functionality and hypothesis we want to test.

What is the expected outcome of our experiment? What is the specific result we expect to achieve by building the ‘test’ capability?

What signals will indicate that the capability we have built is effective? What key metrics (qualitative or quantitative) we will measure to provide evidence that our experiment has succeeded and give us enough confidence to move to the next stage.



Feature
==============================

Backlog
==============================

INVEST (mnemonic)

Letter 	Meaning 	Description
I 	Independent 	The PBI should be self-contained.
N 	Negotiable 	PBIs are not explicit contracts and should leave space for discussion.
V 	Valuable 	A PBI must deliver value to the stakeholders.
E 	Estimable 	You must always be able to estimate the size of a PBI.
S 	Small 	PBIs should not be so big as to become impossible to plan/task/prioritize within a level of accuracy.
T 	Testable 	The PBI or its related description must provide the necessary information to make test development possible.

https://en.wikipedia.org/wiki/INVEST_(mnemonic)


Tasks
==============================

Optimal batch size
==============================

Kanban Board
==============================

WIP 
==============================

Definition of Ready
==============================

Definition of Done
==============================

Estimation (task)
==============================

Architectural Diagram
==============================

What is architecture:
-1 structure of the software: building blocks and relationships
-2 vision: from requirements to technical solution to documenting it

definition by grady booch: 'Architecture represents the significant decisions, where significance is measured by cost of change'
It’s about the decomposition of a product into a collection of components/modules and interactions.
Usually we refer to the components that comprise the software system and the interactions between them. Define component
Architecture must fullfil the business and technical requirements while considering quality attributes such as performance and security. the decisions made regarding software architecture significantly impact how the system evolves and achieves its objectives.

Architecture as a picture/model is used as a blueprint of what are going to, or have already, built. It is both an analytical tool, by looking at the blueprint we can reason about the system, and also as a communication tool so that everyone involved knows what the team builds

Types of architecture
application architecture is inherently about the lower-level aspects of software design and is usually only concerned with a single technology stack
system architecture is one step up in scale from application architecture, since most software systems are actually composed of multiple applications
across a number of different tiers and technologies. In other words, you also have the overall structure of the end-to-end software system at a high-level.

## This part should go at the roles
The role of software architect:

 - Architectural drivers. Understanding the goals, capturing, refining and challenging the requirements and constraints.
 - Designing software. Creating the technical strategy vision and roadmap
 - Technical risks. Identifying, mitigating and owning the technical risks to ensure that the architecture works.
 - Architecture evolution. Continuous technical leadership and ownership of the architecture through out the software delivery
 - Coding. Involvement in the hands-on elements of the software delivery
 - Quality assurance. Introduction and adherence to standards, guidelines, principles, etc.

The reason we need the role, not necessarily emboded in one person is that if everybody on the team is basically left to their own devices. The resulting codebase will be a mess. Introducing control on this sort of project is really hard work but it needs to be done if the team is to have any chance of delivering a coherent piece of software that satisfies the original drivers.

Architecture vs design
A system's design shapes things more at the code level - the way each component works, the purpose of each element, and concern of this kind. Significant decisions are architecture; the rest is design.

The relation between architecture and design:
Architecture is design at a higher level of abstraction while design is architecture at a lower level of abstraction.
For hexagonal architecture, with the core at the centre and ports on the outside layers, if one does not observe the 'D' (dependency inversion) in 'SOLID', will get rigid system where every change in the UI will have to be propagated all the way to the business logic.

example of horrible architecture and design:
Call scrappy from within flask and display the scrapped data. The code will work (verify that), but:

 - any change to any part either scrapy of flask will be difficult because the other part will have to change too
 - testing will be more difficult, because if the page does not show what we expect, we should check two conceptual blocks together rather than each separately
 - scalability will most probably be an issue, because when you bundle things together and one part is not performing well/fast enough, it becomes a bottleneck for all the bundle.

examples of architectural decisions:

 - the programming language
 - technologies and frameworks and libraries
 - type of architecture as in monolith vs microservices
 
 Code that does not compile/run is a serious but obvious problem. The risk with code that does compile/run is that it might be a non obvious problem.
 
 
Five things every programmer should know about software architecture as per `Simon Brown <https://www.youtube.com/watch?v=z1xLDzx7hgw&t>`_ :
 - software architecture isn't about big design upfront
 - every software team needs to consider software architecture
 - the software architecture role is about coding, coaching and collaboration
 - UML is not necessary
 - good architectures anables agility


qualities of good architecture. the application should be:
 - testable
 - secure
 - performant
 - scalable
 - usable
 - reliable
 
A way to capture architecture and design, by Simon Brown, is the C4 model:
 - Context
 - Containers
 - Components
 - Code (or Classes)

 
 Examples of Arcitectures:
 - layered
 - package by feature
 - ports and adapters (the core is the domain and is technology agnostic, while the outside is the infrastructure, the technology specific. There is one rule, the outside depends on the inside)
 - package by component
 
 Note: make sure that the codebase reflects the architectural intent. For example, without encapsulation and information hiding, with all classes being public, every section of the code can access any other section, which can destroy any architecture.
 
 IMPORTANT: Criterion of good architecture: It enables agility - the ability to respond as quick and as easy as possible to external stimuly. It usually comes with modularity.
 
 
https://www.infoq.com/articles/architecture-five-things/
Software architecture isn’t about big design up front
The up front design process should therefore be about understanding the significant decisions that influence the shape of a software system rather than, for example, understanding the length of every column in a database. In real terms, I’d like teams to really understand what they are going to build, how they are going to build it (at a high-level, anyway) and whether what they’ve designed will have a good chance of actually working. This can be achieved by identifying the highest priority risks and mitigating them as appropriate, writing code if necessary. In summary, up front design should be about stacking the odds of success in your favour.


https://www.infoq.com/articles/agility-architecture/
Agility and Architecture: Balancing Minimum Viable Product and Minimum Viable Architecture 
we do not view a software architecture as a set of components and connectors, but rather as the composition of a set of architectural design decisions - Jan Bosch and Anton Jansen (IEEE 2005) 




Requirements (Functional et al)
===============================


## Things to do before coding
Regardless of the process that you follow (traditional and plan-driven vs lightweight and adaptive), there’s a set of common things that really drive, influence and shape the resulting software architecture.
1. Functional requirements. In order to design software, you need to know something about the goals that it needs to satisfy.
2. Quality Attributes. Quality attributes are represented by the non-functional requirements and reflect levels of service such as performance, scalability, availability, security, etc.
3. Constraints. 
4. Where constraints are typically imposed upon you, principles are the things that you want to adopt in order to introduce consistency and clarity into the resulting codebase.
Keep note of the fact that Technology is not an implementation detail- technology choices should be included on architecture diagrams. Technology isn’t just an “implementation detail” and the technology decisions that you make are as important as the way that you decompose, structure and design your software system.

Functional requirements are captured through techniques such as user stories

Examples of non functional requirements:
 - Performance (e.g. Response time, Latency)
 - Scalability. The ability for your software to deal with more users, requests, data, messages, etc.
 - Availability. It is about the degree to which your software is operational and, for example, available to service requests.
 - Security. It covers everything from authentication and authorisation through to the confidentiality of data in transit and storage.
 - Disaster Recovery. What would happen if you lost a hard disk, server or data centre that your software was running on?
 - Accessibility usually refers to things like the W3C accessibility standards, which talk about how your software is accessible to people with disabilities such as visual impairments.
 - Monitoring Some organisations have specific requirements related to how software systems should be monitored to ensure that they are running and able to service requests.
 - Management Monitoring typically provides a read-only view of a software system and sometimes there will be runtime management requirements too.
 - Audit. There’s often a need to keep a log of events (i.e. an audit log) that led to a change in data or behaviour of a software system, particularly where money is involved.
 -  Extensibility is also overused and vague, but it relates to the ability to extend the software to do something it doesn’t do now, perhaps using plugins and APIs.
 - Maintainability. Is about the ability to maintain the code in the future - fix bugs, do necessary updates, etc.
 - Legal, Regulatory and Compliance. Some industries are strictly governed by local laws or regulatory bodies, and this can lead to additional requirements related to things like data retention or audit logs.
 - Internationalisation. Many software systems, particularly those deployed on the Internet, are no longer delivered in a single language.
 - Localisation. Related to internationalisation is localisation, which is about presenting things like numbers, currencies, dates, etc in the conventions that make sense to the culture of the end-user.
 -
 
 
Examples of constraints
 
technology constraints
 - Existing systems and interoperability: Most organisations have existing systems that you need to integrate your software with and you’re often very limited in the number of ways that you can achieve this.
 - Approved technology lists: Many large organisations have a list of the technologies they permit software systems to be built with.
 - Target deployment platform: The target deployment platform is usually one of the major factors that influences the technology decisions you make when building a greenfield software system.
 - Technology maturity: Some organisations are happy to take risks with bleeding edge technology, embracing the risks that such advancements bring.
 - Open source: Likewise, some organisations still don’t like using open source unless it has a name such as IBM or Microsoft associated with it
 
people constraints
 - Size of team for the task, available skills

 
 examples of principles
  - Development principles: Coding standards and conventions, Automated unit testing, Static analysis tools
  - Architecture principles: Layered, hexagonal, etc
  
  
 In the end of the process of examining all the above, the team should have an architectural diagram including technological choices, along with a document with all the choices to the questions above and the rationale for these choices.




Test plan
==============================

You should not wait until you have a complete system before you start system testing. Testing should start on the day you start writing code. You should test as you implement code, so that even a minimal system with hardly any features is tested. As more features are added, the develop/test cycle continues until a finished system is available. This develop/test cycle is simplified if you develop automated tests so that you can rerun tests whenever you make code changes.

How to Break Software (with examples) Jorgensen et Whittaker
https://www.researchgate.net/publication/315700027_How_to_Break_Software_with_examples

Coding Standards
==============================



Exception handling
https://www.toptal.com/abap/clean-code-and-the-art-of-exception-handling


Team Setup
==============================

Software Licence
==============================

Service-Level-Agreement (SLA)
==============================

Budgeting 
==============================
Software Application Discovery As The Best Method For Estimating The Application Software Development Budget

Discovery is a process where a project team discovers all technical requirements related to a given project, so they can prototype the application and estimate the budget. So, not only can you discover all the technical requirements, but you can also see how an app would look like and figure out how much the entire process is going to cost.

Thanks to the prototype, clients love this Agile approach because they get to see how an app looks and feels like. A prototype is a semi-functional graphical representation of a potential product that offers an overall look and user flow for examination before any real development begins. Prototypes often look so natural and complete that they can be handed off to a potential user for the feedback!

By the end of the discovery cycle, the following items are delivered to the client:

    Requirements definition and analysis: These elements offer a review of key aspects, critical functionality, and core technical features. The project team, to achieve this, dives into the initial requirements, making them more coherent and tying the various proposed elements to each other.
    Recommended technological stack: An outline of the programming languages and technologies that will best suit the requirements. Often, a comparative table is used to present the pros and cons of each recommended approach.
    Functional and nonfunctional requirements: This captures the details of the potential product, including vision, scope, and a description of user functionality.
    Project plan: A step-by-step plan for how the project should run to achieve on-time and on-budget delivery.
    Cost estimation: Detailed cost estimates that provide granular analysis. Usually, at this point, estimates are so precise that budget overruns rarely happen.

From a business perspective, discovery helps uncover new opportunities and/or verify a business idea. The results of this process might influence or even shift the direction of any further product development. This method provides invaluable insights at a very early stage.
By investing time in discovery, you can minimize the project risks associated with cost and schedule overruns.

Given the capacity, one can enumerate the cost of a team.
There are at least three reason to do something.
Strategic. For example, we anticipate that the language/technology we use will have to change, because it is getting inefficient. There will be no immediate gain, but we know should spent the effort and time to do so.
cost reduction. In many cases, we can reduce the costs of operation by using software.
revenue creation. new features, or products, that translate to more customers/revenue.
If we can estimate the above, then we can make sound financial decisions, even without a traditional budgeting approach.


Legal Considerations
==============================



************************
Coding
************************


Daily stand-up meeting
==============================

MVP (Spike) (Walking Skeleton)
==============================

Red-Green-Refactor
==============================

Code smells
==============================

Refactoring recipes
==============================

SOLID principles
==============================

Pair/Mob coding
==============================

Rotating Pairs
==============================

Test Automation
==============================

CI/CD pipeline
==============================


Implementing a CI/CD pipeline:

- Version Control (git):

    On git branching: each branching strategy is suitable for a specific context. For example, working with feature branches makes sense for open source projects where people are not fully on project so while they might work on something other should be able to move ahead. In projects with a dedicated full-time team, given the presence of an automated testing suite, maybe it does not make sense.

Context always matters.

Patterns for Managing Source Code Branches https://martinfowler.com/articles/branching-patterns.html


- Jenkins(?)
- Docker
- Heroku
- Etc
- Dora (or any other) Metrics https://dev.to/linearb/how-to-use-dora-engineering-metrics-to-improve-your-dev-team-1hkc:
    As Goodhart's Law states, “When a measure becomes a target, it ceases to be a good measure.” Metrics can be gamed. Simple example of paying bonuses for bugs found, creates incentive to create bugs.

Deployment Frequency
Deployment Frequency measures the number of times that code is deployed into production. It’s usually reported in “Deployments Per Day”.
Mean Lead Time for Changes
Mean Lead Time for Changes is the average time it takes from code being committed to that code being released into production.
Some organizations begin tracking the time from the first commit of the project’s code, while others measure it beginning from merging the code to the main branch.
Mean Time to Recovery (MTTR)
This metric measures the average time it takes the team to recover from a failure in the system.
“Failure” can mean anything from a bug in production to the production system going down.
Change Failure Rate
Change Failure Rate measures how often a code change results in a failure in production. Changes that result in a rollback, in production failing, or in production having a bug all contribute to this metric.

The first two metrics — Deployment Frequency and Mean Lead Time for Changes — measure the velocity of a team. MTTR and Change Failure rate are a measure of the quality and stability of a project. All four metrics can be derived from mining the tools that you are currently using.

When the purpose for metrics is misunderstood, serious issues can occur. We are increasingly seeing DORA metrics used as goals, complete with OKRs (objectives and key results) where the objective is “improve DORA metrics.” But improving metrics should never be your goal.
Related to this is the idea of using DORA metrics to compare delivery performance between teams. Every team has its own context. The product is different with different delivery environments and different problem spaces.
Another common problem is the growth of “vanity radiators,” metric dashboards that display numbers but give no obvious clue about what action to take. “We deployed 436 times!” OK, but how big is the organization? Was that 436 times in a week, a day, or a year? Is that number improving or degrading? 



Branching Strategy
==============================

Semantic Commits
==============================

## On git message formatting

A well-crafted Git commit message is the best way to communicate context about an individual code change to fellow developers (and indeed to their future selves). A diff will tell you what changed, but only the commit message can properly tell you why. Overall, a clean and well formatted commit history can help someone understand what happened, and why it happened that way, years ago. Since a project’s long-term success rests (among other things) on its maintainability, it would be a waste for a developer not to use one of the more powerful tools: the project’s log.

As with many written forms of communication, we can break our suggestions down to three aspects:
- Style. Markup syntax, capitalization, punctuation, etc. The point is to create a consistent log that will be easy to read.
- Content. What kind of information should the body of the commit message (if any) contain? What should it not contain?
- Metadata. How should issue tracking IDs, pull request numbers, etc. be referenced?

### Style
With respect to style, these are some initial suggestions:
- Use a concise subject message less than 50 characters (the usual convention)
- Utilise the body to explain what and why vs how
- Be consistent with formatting like capitalisation, punctuation, etc

### Content
With respect content, the idea of `Semantic Commit Messages` is quite useful.

    Semantic Commits are commit messages with human and machine readable meaning, which follow particular conventions

In more detail:
- The commit messages are semantic - because these are categorized into meaningful types, indicating the essence of the commit
- The commit messages are conventional - because these are formatted by a consistent structure and well-known types, both for developers and tools


The Conventional Commits specification is a lightweight convention on top of commit messages. It provides an easy set of rules for creating an explicit commit history; which makes it easier to write automated tools on top of.

It features a specific structure 

    <type>[optional scope]: <description>

    [optional body]

    [optional footer(s)]


An example


    fix(client-logo): correct capitalisation in file path

    The client logo would not show up in the deployed version, 
    although it worked locally. The actual filename and the 
    path provided had different capitalisation. The local
    Windows env read it just fine, while the Linux 
    deployment env did not read the file

    closes issue #543

And here is another one

    fix: fix foo to enable bar

    This fixes the broken behaviour of the component by doing xyz. 

    BREAKING CHANGE
    Before this fix foo wasn't enabled at all, behaviour changes from <old> to <new>

    Closes D2IQ-12345


Let us take a closer look

First we start with the list of commit types. Feel free to create the types that suite your project:

- **feat** : a new feature is introduced with the changes
- **data** : any change related to data - preparation, exploration, etc
- **fix** : a bug fix has occurred
- **chore** : changes that do not relate to a fix or feature and don't modify src or test files (for - example updating dependencies)
- **refactor** : refactored code that neither fixes a bug nor adds a feature
- **docs** : updates to documentation such as a README or other markdown files
- **style** : changes that do not affect the meaning of the code, likely related to code formatting such as white-space, line length, and so on.
- **test** : including new or correcting previous tests
- **perf** : performance improvements
- **deploy** : deployment / continuous-integration related
- **revert** : reverts a previous commit 

The types may be followed by the scope of the commit, a noun that describes the relevant section of the codebase - for example a feature tied up to a specific section of the project.

Then, there is the short description of the changes - it's like a header to the body that, optionally, follows next. In the body one has the opportunity to explain WHAT the change is, but especially WHY the change was needed.

In the end, the optional footer mention consequences which stems from the change - such as announcing a breaking change, linking closed issues, mentioning contributors and so on.


### Metadata
As we saw, the footer is the place for useful metadata like issues referenced, PullRequests, etc. Depending on the way the project works, one should establish consistent rules for referencing the relevant project management artifacts, like reported bugs, PullRequests, etc. With consistent rules metadata referencing rules the Git log history can be easily connected to the rest of the project like for example which are the corresponding commits for a certain user story.



Ideas adopted from:
- [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0-beta.4/)
- [Semantic Commit Messages](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716)
- [How to Write a Git Commit Message](https://cbea.ms/git-commit/)
- [How to write better git commit messages](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)


Metrics (Lead-time, etc)
==============================

Software Security
==============================

Different kinds of testing
==============================

Exploratory/Innovation days
==============================

Code quality
==============================

Code review
==============================

Your Code Review Checklist: 14 Things to Include
https://www.codementor.io/blog/code-review-checklist-76q7ovkaqj


Retrospective (Sprint review)
==============================


************************
Post-Coding
************************

User Support
==============================

Maintenance
==============================

Bug reporting
==============================

User feedback
==============================



************************
Documentation
************************

Project Log
==============================

Decision Records
==============================

Technical Docs
==============================

User Docs
==============================

Documented code
==============================

Project Docs
==============================


############################
PART 5: Example
############################


On software tools and libraries used for implementing the aforementioned principles, mostly in Python.


############################
PART 6: A summary
############################
One of the arguments of Agile, is that there is an unobservable theoretical limit of minimum cost, which can be approached by using sound engineering principles.

############################
PART 7: Interesting links
############################

https://holub.com/heuristics
Heuristics for Effective Software Development Organizations: A continuously evolving list.*

One of the manifestations of the lack of agility is that one needs to understand everything in the codebase in order to change anything, at which point what you have is rigidity rather than agility.