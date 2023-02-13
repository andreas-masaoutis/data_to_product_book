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
Call scrapy from within flask and display the scrapped data. The code will work (verify that), but:
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
 
 
