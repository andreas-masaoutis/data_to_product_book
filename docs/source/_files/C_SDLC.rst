========================================================
Phases of software development lifecycle
========================================================

Creating software that does the right thing, that does that thing right, and being built in a reasonable timeframe, is all but easy!

No matter what the preferred software engineering methodology is, all of them are organised efforts to address a set of fundamental questions with respect to the development of a software. In other words, no matter in which way, when delivering a software system, we are going to do the following. Let's see:

Software development is fundamentally about the following: The identification and definition of the problem from the social/user perspective The understanding of the problem that we need to solve from a technical perspective (requirements) The development of the software system that solves that problem (development) The checks that make sure that the problem we needed to solve has indeed been solved (testing/quality assurance) The transfer of the software solution to the end user The maintenance of it

The above can be further analysed into separate phases, Wikipedia has the example of a ten-phase version of the cycle, but that level of abstraction is good enough for our purpose.

The purpose of this work is to present a way to organise activities, that span all these different phases, in a coherent and effective way.

Let us take a closer look.
 
No matter what methodology is being used, the list below has the main steps that have to be followed. Note that we present them in a linear fashion, that is essentially the waterfall model. It is not that Agile does different things; it simply does all these things in a different succession. So, let us take a look at the different phases of the Software Development Lifecycle (SDLC), and then we’ll slowly see haw agile tackles these problems.
Usually, we start with an initial idea about a product, and we have to define the problem and success criteria.
- Identify stakeholders and goals
- Estimate scope, timeline, and budget
- Set up governance (processes, roles, risk management)
Given the idea and a rough plan for implementing it, we can do a deeper analysis of the requirements. It is time to clarify what the software must do and under what constraints.
- Gather requirements (functional + non-functional)
- Model processes/data (user stories, use cases, diagrams)
- Define acceptance criteria and priorities
- Assess feasibility and risks

Up to now, we have a list of requirements or user stories, that describe what the product will do. It is then time to decide how the system will be built.
- Architecture (components, services, data flows)
- Data design (schemas, models)
- API/interface design
- UI/UX design 
- Create plans for security, performance, and testing strategies
The natural net step is to actually build the software according to the design.
- Set up environments and tooling
- Write the code (feature by feature)
- Perform code reviews and ensure quality
It is now time to verify and validate what we have created. We use various levels of test to ensure the software works as intended and meets requirements.
- Validate with different test levels (unit, integration, system, regression)
- Perform non-functional tests (performance, security, usability as needed)
- Fix defects and re-test
- Confirm traceability to requirements/acceptance criteria
Any piece of software that is not accessible by its intended audience is a good as non-existent. So, we have to make the software available for users.
- Prepare release builds and release notes
- Configure production (or relevant target environments)
- Run deployment/rollout steps (manual or automated)
- Do smoke/health checks after release
Finally, we must keep the system running and improve it over time.
- Monitor logs/metrics, respond to incidents
- Patch vulnerabilities and fix bugs
- Improve performance and add enhancements
- Manage end-of-life and migrations when necessary
Let us re-iterate that Agile has not re-invented the wheel of software engineering. It rather proposes a different way of performing all these standard tasks. We will see how.

