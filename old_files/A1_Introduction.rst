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

[insert infographic]

What becomes immediately obvious is that it is not possible to summarise such a field with an introductory work. To be honest, I believe that, if any, there will be just handful of people around the world that are proficient will all of these ideas. For that reason we will limit ourselves to identifying some of the core concepts, and follow them all the way to practical application. This will not be any kind of definitive guide on Agile, it will be a humble and simple exposition of some core ideas.





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






