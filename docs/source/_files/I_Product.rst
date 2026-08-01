####################################
The right thing to build
####################################


Product vision
======================
The Product Vision is a clear, high-level statement of what you’re building and why—the long-term direction for the product. It helps everyone align on the goal without getting stuck in the details. A good Product Vision expresses the value the Product should deliver and to whom that value is delivered. It is effective when people connect with the vision emotionally and practically. When a Product Vision is both aspirational and actionable, it inspires creativity within the Scrum Team allowing them to collaboratively work with Stakeholders on how they might work toward the vision.

Roadmaps, epics, and user stories translate the vision into nearer-term plans and work.

Roadmap
======================
A product roadmap is a shared source of truth that outlines the vision, direction, priorities, and progress of a product over time. It's a plan of action that aligns the organization around short- and long-term goals for the product or project, and how they will be achieved. It is a high-level plan that shows the product’s direction over time—typically what major goals, themes, or epics you expect to work on next and when (or roughly in what time range).
It’s not a detailed, fixed commitment like a traditional project plan. Agile roadmaps are meant to be flexible and updated as you learn.

What a roadmap usually includes:

* Themes or goals (e.g., “Improve onboarding,” “Increase reliability”)
* Epics/features at a summary level (not every task)
* Time horizons (often near-term vs. later-term, like “next 1–3 months” and “next quarter”)
* Expected outcomes (what success should look like)
* Sometimes dependency notes or major milestones

User story - INVEST
======================
What are the User Stories, how to write them, and use them:

What are they:
A user story, as a placeholder for discussion, facilitates it by describing the problem we want to solve with the software, who will use it, why and how they will use it. The discussion then is about arriving at a solution to the problem while at the same time creating a shared understanding among the participants.
Stories help us separate WHAT the system should do from HOW is will do it. - How to write them Writing stories just passively formulating requested solutions is a practice that dangerously nears Henry Ford's paradox: "If I had asked people what they wanted, they would have said faster horses".

The traditional user story framework is focused on capturing requirements for what we want to build and for whom, to enable the user to receive a specific benefit from the system. It has the following format::

	As A…. <role> I Want… <goal/desire> So That… <receive benefit>

INVEST (mnemonic)

Letter Meaning Description:

 I Independent the PBI should be self-contained. 
 
 N Negotiable PBIs are not explicit contracts and should leave space for discussion. 
 
 V Valuable A PBI must deliver value to the stakeholders. 
 
 E Estimable You must always be able to estimate the size of a PBI. 
 
 S Small PBIs should not be so big as to become impossible to plan/task/prioritize within a level of accuracy. 
 
 T Testable the PBI or its related description must provide the necessary information to make test development possible.

For more info take a look at - https://en.wikipedia.org/wiki/INVEST_(mnemonic)

How to use then

Common mistakes with user stories https://www.youtube.com/watch?v=0HMsh459h5c:

1. Direct translation from traditional 'requirements': A user story is a description of the problem we are trying to solve from the perspective of the user - it is not a technical specification. If the story only conveys the technical part and not the user need and context, the developers cannot do a good job even if they have good technical skills, as they will not understand what they are trying to solve. The job of a software developer is not to write code, is to solve problems; in order to do so one needs to understand it. 
2. Too detailed stories that read as a contract. A story instead should be like a placeholder for a conversation. As the story is being born out of the realisation of a need, it should focus on the exactly that: the need of the user. It will later be used for the discussion between the product owner and the developers where the latter will contribute on the technical aspects of the solution. A too detailed story that goes all the way down to the details stifles the discussion and the possibility to innovate. Instead, it is the discussion that will lead the team to figure out the best way to implement the story 
3. Too large stories. Good user stories identify a useful unit of work. For story to represent easily and rapidly produced new functionality it should be a small increment in the behaviour of the system. Maximum time for story completion should be within a sprint, something like a week or two. Ideally, they should be shorter, like a day or two. 
4. Value vs invaluable. Stories represent value to the user. They do not have to be the killer feature that does everything and even more. As with the large stories, invaluable stories tend to be overcomplicated, while as we said before it is far easier to work with smaller and simpler ones. First story could be created simple login, then require more secure password, address lost passwords, periodically reset passwords, etc. 
5. Dependent stories. Ideally, stories should be implementable in any order, although some might more difficult to implement than others

Enter validation and we have Hypothesis-Driven Development: Practicing it is thinking about the development of new ideas, products and services – even organizational change – as a series of experiments to determine whether an expected outcome will be achieved. The process is iterated upon until a desirable outcome is obtained or the idea is determined to be not viable.

An extension to the traditional user story with the structure to support Hypothesis-Driven Development would be the following

We believe that <this feature> <for these users>

Will result in <this outcome>

And We will know we have succeeded when <we see a measurable signal>

What functionality we will develop to test our hypothesis? By defining a ‘test’ capability of the product or service that we are attempting to build, we identify the functionality and hypothesis we want to test.

What is the expected outcome of our experiment? What is the specific result we expect to achieve by building the ‘test’ capability?

What signals will indicate that the capability we have built is effective? What key metrics (qualitative or quantitative) we will measure to provide evidence that our experiment has succeeded and give us enough confidence to move to the next stage.

Requirements (Functional et al)
## Things to do before coding Regardless of the process that you follow (traditional and plan-driven vs lightweight and adaptive), there’s a set of common things that really drive, influence and shape the resulting software architecture. 1. Functional requirements. In order to design software, you need to know something about the goals that it needs to satisfy. 2. Quality Attributes. Quality attributes are represented by the non-functional requirements and reflect levels of service such as performance, scalability, availability, security, etc. 3. Constraints. 4. Where constraints are typically imposed upon you, principles are the things that you want to adopt in order to introduce consistency and clarity into the resulting codebase. Keep note of the fact that Technology is not an implementation detail- technology choices should be included on architecture diagrams. Technology isn’t just an “implementation detail” and the technology decisions that you make are as important as the way that you decompose, structure and design your software system.

Functional requirements are captured through techniques such as user stories

Examples of non-functional requirements:

Performance (e.g. Response time, Latency)

Scalability. The ability for your software to deal with more users, requests, data, messages, etc.

Availability. It is about the degree to which your software is operational and, for example, available to service requests.

Security. It covers everything from authentication and authorisation through to the confidentiality of data in transit and storage.

Disaster Recovery. What would happen if you lost a hard disk, server or data centre that your software was running on?

Accessibility usually refers to things like the W3C accessibility standards, which talk about how your software is accessible to people with disabilities such as visual impairments.

Monitoring Some organisations have specific requirements related to how software systems should be monitored to ensure that they are running and able to service requests.

Management Monitoring typically provides a read-only view of a software system and sometimes there will be runtime management requirements too.

Audit. There’s often a need to keep a log of events (i.e. an audit log) that led to a change in data or behaviour of a software system, particularly where money is involved.

Definition of Ready and Definition of Done
============================================
These two definitions are two important quality filters maintaining the quality of work in an agile project.

Definition of Ready (DoR) is a checklist or set of conditions that a work item must meet before it can be pulled into a team’s next work phase. It’s about ensuring the item is clear enough to start. Usually this is about the conditions for a task is ready to leave the backlog and enter the development phase. It's a checklist that might include criteria, like dependencies identified and resolved, designs completed, having been through a refinement session, clear acceptance criteria and possibly acceptance tests already written. It ensures that work is sufficiently prepared, clear, and feasible before the team can consider to move it to the next stage of development.

Definition of Done (DoD) is a checklist or set of criteria that must be satisfied for the work item to be considered complete. It’s about what “finished” means (including quality, testing, acceptance, documentation, etc.)

Effectively, these two definitions function as quality contracts between the different stakeholders and team members. A developer that starts working with the tasks of a user story expects that these are well defined or even that the acceptance tests are already written. A stakeholder knows that when something is presented as finished product, it has the relevant documentation.

Persona, epic, user story
============================================
Roman Pichler (https://www.romanpichler.com/blog/personas-epics-user-stories/) has a really nice description of how to connect the product vision and roadmap to the user story, as there are some important links in between; the personas and the epics.

The first step towards writing the right user stories is to understand your target users and customers and their relation to your product.
Personas offer a great way to capture the users and the customers with their needs. They are fictional characters that have a name and picture; relevant characteristics such as a role, activities, behaviours, and attitudes; and a goal, which is the problem that has to be addressed or the benefit that should be provided.

From the persona to the epic, we use the personas’ goals to identify the product functionality. Ask yourself what the product should do to address the personas’ problems or to create the desired benefits for them. We start with our primary persona and capture the functionality as epics, as coarse-grained, high-level stories. Write all the epics necessary to meet the persona goals but keep them rough and sketchy at this stage.

With a holistic but coarse-grained description of our product in place we start progressively breaking the epics into smaller stories. Rather than detailing all epics and writing all user stories upfront, we derive the stories step by step just in time for what we want to build next.

Product backlog
======================
A product backlog is a prioritised list of the new features, changes to existing features, bug fixes, infrastructure changes, or other activities that a team may deliver in order to achieve a specific outcome.

The product backlog is the single authoritative source for things that a team works on. That means that nothing gets done that isn’t on the product backlog. Conversely, the presence of a product backlog item on a product backlog does not guarantee that it will be delivered since it might be side-lined by other more tasks. It represents an option the team has for delivering a specific outcome rather than a commitment.
Depending on the methodology we use for a project we might use different ways to choose the work to be done, yet the backlog is the place where we pick our work from.

Prototype
======================
As we have already seen, one of the ways to figure out what is that we should build, is to create prototypes, get feedback, and validate (or not) our ideas. There are different tools to implement prototyping that cover different needs

Spike (research spike / technical spike): a short, time-boxed investigation to reduce uncertainty—e.g., proving a technical approach, estimating effort, evaluating feasibility, or validating an architecture/algorithm. A spike may produce notes, prototypes, benchmarks, or experiments; it’s not mainly meant to become the final product.

Skeleton (a.k.a. app skeleton / UI skeleton / scaffolding): the basic framework of the system or screen set—routes/navigation, folder structure, app bootstrapping, empty components, placeholder UI, and stubbed services—so the team has a working “shell” they can build on. It’s meant to establish structure and integration points early.

Minimum Viable (Valuable) Product (MVP): the smallest version of a product that still delivers the core value to users and lets you test key assumptions in the real world (or with real users). It’s “viable” because it can actually be used, not because it’s feature-complete.

In practice, these tools might be used together in a progression from a spike, to a walking skeleton that morphs into an MVP and eventually into a final product.
