
************************
Pre Develop
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

