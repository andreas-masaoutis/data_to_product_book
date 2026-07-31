============================
Frameworks
============================

Let us now take closer look at the various frameworks that have been developed over the years, that put the core ideas in action.


Design Thinking
Design Thinking was popularised by the IDEO agency and Stanford University in the 2000s and presented by Tim Brown in his book ‘Change by Design’. It was not initially part of the technical agile movement, but touched upon specific issues that are central to agile.
It is a problem-solving methodology that places the user at the centre of the design process, and in that way resonates with the agile manifesto. It borrows from industrial design methods and applies them to all domains: digital products, services, organisational processes, and even business strategy.
Unlike purely analytical approaches that start from data and technical constraints, Design Thinking starts from human needs. It begins by deeply understanding users, their frustrations, motivations, and context, before seeking solutions. This perspective inversion is what makes the method so powerful: it avoids building technically brilliant solutions that address no real need.
Why Design Thinking Matters
In software development, it's tempting to rush toward the technical solution without properly framing the problem. Design Thinking imposes a beneficial pause that ensures you're solving the right problem before figuring out how to solve it.
Reduced failures: 70% of IT projects fail partly due to poor requirements understanding (Standish Group). Design Thinking attacks this problem at its root by placing the user at the centre.
Authentic innovation: By exploring the problem from multiple angles and encouraging creative divergence, Design Thinking surfaces solutions that conventional approaches miss.
Stakeholder alignment: Collaborative workshops involve all stakeholders (client, users, developers, designers) and create a shared vision of the product to build.
Rapid validation: Rapid prototyping and user testing validate hypotheses before investing heavily in development.
Empathy as compass: By understanding user emotions and context, design decisions are guided by real needs rather than assumptions.
Design thinking starts from the central premise that often what stakeholders think is valuable for their clients, turns out not to be so. By using techniques such as ideation the effort is put into figuring out what the users really consider valuable and a priority. By quickly prototyping the team can have feedback, cross-validate its assumptions, and continue building what comes up as valuable.
Implementation
Build a cross-functional team: Design Thinking works best with varied perspectives: developers, designers, sales staff, and if possible, end-users.
Plan empathy workshops: Schedule user interviews (5 to 12 interviews are enough to identify patterns) and field observation sessions.
Frame the problem: Use techniques like empathy maps, persona canvas, and "How Might We" questions to synthesise insights and clearly formulate the problem.
Organise ideation sessions: Plan 2 to 4 hours of structured brainstorming with techniques like crazy 8s or brainwriting to generate maximum ideas.
Prototype quickly: Build prototypes in 1 to 3 days maximum. Use tools like Figma for interfaces or quick code for technical prototypes.
Test and iterate: Test prototypes with 5 to 8 users, collect feedback, and iterate. 2 to 3 test cycles are generally enough to validate the direction.

LEAN

What the Lean movement has used for years in process improvement, can be used in software engineering. This is possible because software, in contrast to, say, buildings, can be valuable even if not complete.
L manufacturing rested on a deep understanding of what creates value, why rapid flow is essential, and how to release the brainpower of the people doing the work.
Lean is a pull model, rather than a push one (Toyota vs Ford). The question in not can we build that, but rather should we do so?
Many agile practices like short cycles, non-negotiable quality, regular retrospectives, pulling work from a "backlog," come from Lean.
According to Mary Poppendieck, what they hoped to achieve with their work was to change the software development paradigm from process to people, from disaggregation to aggregation, from speculation to data-based decision making, from planning to learning, from traceability to testing, from cost-and-schedule control to delivering business value. 
One of the main insights is that while the project paradigm is based on the assumption that what we plan to build is the correct/valuable thing to do, in many cases this is not so. The biggest waste in software development is to build things that do not contribute value to the product Building things that do not bring value is wasteful in 3 ways: - The opportunity cost of not building something of value - The maintenance cost for the zero value features, - plus the added complexity to the overall design that makes it more difficult to add valuable features.
There are 7 principles that capture the main ideas:
1. Eliminate waste
2. Amplify learning
3. Decide as late as possible
4. Deliver as fast as possible
5. Empower the team
6. Build integrity in
7. Optimize the whole
 

The single most important factor is whether a project will be cancelled and whether people will actually use it. As we have seen again, the objective is to create feedback loops to validate assumptions, make it possible to work in small batches, and enable an experimental approach to product development. Do your user research: run a customer/product survey to find out about something related to your customers / products and build on that, rather than just assume what the user need.
eXtreme Programming (XP)

Kent Beck developed extreme programming during his work with Chrysler around 1996. While working on a project there as a team leader he had his team use techniques that seemed sensible, like testing and code reviews. He then began to refine the development methodology used in the project and wrote a book on the methodology ‘Extreme Programming Explained’, published in October 1999. These techniques form the technical core of what agile came to be.

We have to note that although some of the techniques are not novel in the software industry, nonetheless are used in different ways. For example, by writing software tests first, there was a change in that the developer was taking full responsibility for the quality of the code, rather than just passing it over to the QA team. In the end of the day everything is about the working program, and the responsibility for that lies with the whole team.

The values of eXtreme Programming are:
1. communication, so that all team members have the necessary information to play their role
2. feedback, so that everyone has the opportunity to draw the appropriate lessons from their activities
3. simplicity, so that we only do what is necessary and not more than that
4. and finally, courage, to be able to say the truth and even outright say no even when this is not easy to do so.

Principles are applications of these ideas in practice, like incremental improvement principle of flow

Practices are then the application of the principle to a specific project, where the value of simplicity, translates to team colocation so that face-to-face communication, which is the easiest form, suffices, or 
The value or feedback becomes test-driven development, as these tests provide immediate feedback.

Exactly because eXtreme Programming has been quite successful, many of the practices and ideas of the late 90's, seems to have splintered / grown into various directions: DEVOPS, with the focus on automation, Craftsmanship, with the focus on quality, LEAN with the focus on delivering value. The point is that eXtreme Programming is not just the agile technical practices, it contains the seeds of later 'movements'. Nowadays that some of the early X eXtreme Programming P practices have grown into their own 'fields' it is easy to think that eXtreme Programming is just TDD and refactoring. Out of the original proposed practices, some thinks caught on and are today’s common ground, like 40-hour week and the short releases, some practices did not do so well like the on-site customer, and others have evolved into their own like continuous integration and the CI/CD paradigm.

list of XP practices (1999 version - include graph for the relations between them) on-site customer metaphor planning game short releases continuous integration collective ownership coding standards pair Programming testing refactoring simple design 40-hour week

What modern XP looks like traditional practices: - site customer - user stories - test first - pairing - design improvements - collective ownership - continuous integration - velocity recent additions: - domain driven - UX - support - learning 20% - story prioritisation - mobbing - retrospectives - continuous deployment - infrastructure

In other words, simultaneous continuous everything,
Agile Modelling
Agile modelling (AM) is a methodology for modelling and documenting software systems based on best practices. It grew out Scot Ambler’s work in the early to mid 90’s, and it essentially captured the way in which some teams at the time did their modelling using whiteboards and sketches, and post-it notes; something that would be considered heretical at that time. 
It is a collection of values and principles that can be applied on an (agile) software development project. This methodology is more flexible than traditional modelling methods, making it a better fit in a fast-changing environment. It is part of the agile software development tool kit.
In the spirit of Agile, it is a lightweight, iterative approach to creating models (like diagrams, sketches, or other documentation) to help people understand and communicate about a software system—just enough to support development as it evolves.
It is meant to be tailored into other, methodologies such as XP, Scrum, Kanban, and be used along them. It focuses on common artifacts that include simple UML sketches, user stories with acceptance criteria, CRC cards, system context diagrams, wireframes, and architecture sketches—often created informally and updated regularly.
Core practices include ‘document late’, ‘document continuously’, ‘iteration modelling’, and more.
https://agilemodeling.com/essays/introductiontoam.htm
Crystal
Crystal (the Crystal agile methodology, more precisely Crystal methods) is a family of agile approaches for software development created by Alistair Cockburn that emphasizes people and their interactions over rigid processes and heavy documentation.
One particular triplet showed up repeatedly: colocation of the team, frequent delivery, and access to an expert user. 
Crystal is a family of methodologies with a common genetic code, one that emphasizes frequent delivery, close communication and reflective improvement. 
Key ideas:
Tailor the method to the project: the “right” process depends on your team and context (especially team size and project criticality).
Lightweight and adaptive: teams use only the practices that help them deliver and learn.
Frequent delivery + reflection: keep producing working software and regularly adjust based on what’s learned.
Communication is central: often with close, low-friction information flow (e.g., “osmotic communication” in co-located teams).
Crystal is often described with a color spectrum (e.g., Crystal Clear, Yellow, Orange, Red, etc.), where, each colour corresponds to a team size.
Core Concepts 
The crystal framework in agile development is characterized by its focus on:
Frequent delivery of working software
Close communication within the team
Continuous improvement through reflection and adaptation
Minimal bureaucracy and documentation
With respect other frameworks Crystal focuses more on team dynamics and communication. It is not prescriptive with respect the actual tools used, such as the Kanban board, or the specific roles such as the Scrum Master. Rather it is more adaptable to different project types, but for that reason more difficult to implement.
Scrum

Scrum is an Agile framework for building products iteratively by organizing work into short cycles and emphasizing transparency, inspection, and adaptation. Scrum is a process rather than an engineering methodology per se. Its definitive characteristic that sets it apart from other agile frameworks, is time-boxing everything. Probably, it was this characteristic that made it so popular in the corporate world, since everything is accounted for. 
At the centre of these time-boxes, is the Sprint, a two-week period where development takes place. Let’s see how the process revolves around a sprint. The central tenet of Scrum is to produce a Done increment, in a sense working software, during a sprint.
In order to understand Scrum, we’ll start with its main artifacts. There are 3 of them: the product backlog, sprint backlog, and increments.
The product backlog is a list of new features, enhancements, bug fixes, tasks, or work requirements needed to build a product. It’s compiled from input sources like customer support, competitor analysis, market demands, and general business analysis.

The sprint backlog is the subset of the product backlog, with tasks that have been promoted to be developed during the next product increment. Sprint backlogs are created by the development teams to plan deliverables for future increments and detail the work required to create the increment.

The product increment is the customer deliverables that were produced by completing product backlog tasks during the Sprint, where done is judged according to the “Definition of Done”. For example, are we done without unit-tests, or without documentation? If something is not done, then we cannot move on, we first have to get it done. So, this is really regulating how the whole project runs.

Events (time-boxed activities)
Sprint Planning taking place before a sprint: decide what to deliver in the sprint and how.
Daily Scrum taking place, usually, every morning for 15 minutes max: short daily coordination to adjust the plan toward the sprint goal. I tell my team what I worked on, if there any problems that stop me from working on my next tasks, etc. It is the main daily communication 
The Sprint Review is where the team demonstrates the increment that has been built during the sprint and gets feedback from the stakeholders.
At the Sprint Retrospective after the sprint’s conclusion, the team inspect the process, identifies problems, and drafts proposal for improving it for the next sprint.

Scrum has three main roles:
The Product Owner (PO) that defines and prioritizes the product backlog (what to do next).
Developers: the people who build the increment (code/test/release-ready work).
Scrum Master: helps the team follow Scrum, removes impediments, and coaches the process.

In the end, if you adopt Scrum as a process, without the engineering methodology, it will not do much.

Software Craftsmanship
martin fowler - the Agile Industrial Complex https://martinfowler.com/articles/agile-aus-2018.html
What Scrum forget was that you cannot have speed without quality. You cannot have speed while you are carrying technical debt. And the more technical debt you will carry, the slower you will go. And this is a horrible wicked circle, because the slower you go, the more technical debt you will acquire.
Because of this, another movement was born – the Software Craftsmanship movement. This is evidence of a split in the community. A group of us felt it was necessary to re-assert the values of eXtreme Programming into this world that was now dominated by Project Manager Scrum Master.

Kanban
It is a workflow management system, rather than a full-blown software engineering methodology like say, eXtreme Programming. That is why it can, and should, effectively be used together with other frameworks.
The main characteristic of Kanban is that it is a pull, rather than a push system, born in Japanese manufacturing after WWII. Instead of setting a production target and then feed the necessary materials into the production line with the aim of producing goods that stockpile to cover future demand, work only starts when a request arrives with work ‘pulling’ what is necessary for its successful completion. This change, creates a different, continuous, flow.
This idea adapted to software engineering works through the main instrument, that is the Kanban board. This can be deceptively simple, like a table with four columns ‘To do’, ‘Developing’, ‘Testing’ ‘Deployed’. An individual or a team, picks a task from the ‘To do’ column when they have the capacity. The crucial concept here is the ‘Work-In-Progress’ (WIP) limit. There is no point in pulling multiple tasks at the same time and work on, say, 10 different ones; 2 or 3 is fine. Once a task is ready, moves to the next column. That’s it.
If it is that simple, why do we bother? By managing queues, limiting work‐in progress and building a cadence through a pull system (limited WIP) versus push system (non-­‐limited WIP) we have a faster, steadier delivery by reducing multitasking. Also, we are able to expose bottlenecks and find more timely solutions. On the other hand, “pushing” a large batch of requirements and/or starting too many requirements delays discovery of defects and other issues; as defects are hidden in incomplete requirements and code.
Simple, yet if done correctly, can be really powerful. My personal favourite way to organise work.
Dev-Ops
In the initial ideas of Agile, development and operations stood somewhat apart. Obviously, organising frequent demos and receiving feedback from clients, meant that the software had to be running. But not necessarily properly deployed to the end-user. DevOps, as it grew in 2000 is the principle of creating close feedback loops for large products. This is shift left (see below) on steroids, but this is necessary for service-oriented software that runs client server architecture.
Again, we see here all the traits of Agile, applied in this specific context:
Collaboration across teams: Developers and ops work together instead of throwing changes “over the wall.”
Automation: Build, test, and deployment are automated as much as possible.
Continuous delivery of change: Changes can be released frequently, with confidence.
Infrastructure as code: Environments are defined in code (so they’re repeatable and versioned).
Monitoring & feedback loops: Systems are observed in production and those signals drive improvements.
Nowadays, most large software products are run this way.
Overall on frameworks
The frameworks we have seen here, share a characteristic; they have grown organically out of the actual software engineering daily practise and have evolved alongside it.
Each one of these, address some issues and proposes solutions. eXtreme Programming brought most of the core development practices, Scrum tried to organise the project, DevOps covered the modern era of continuously evolving software as a service products.
The fields might seem chaotic, but it isn’t really. Once one follows the timeline many things fall into their place.
What we are going to do next is talk more on the main concepts, some of which we have referred to already.
