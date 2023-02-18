# The fundamentals of building software

Software development is fundamentaly about 
knowing the problem that we need to solve (requirements)
writing the code that solves that problem (development)
checking that the problem that we needed to solve has indeed been solved (testing/quality assurance)

## The software development life cycle
No matter what the prefered software engineering methodoogy is, all of them are organised efforts to address a set of fundamental questions with respect to the development of a software. In other words, no matter in which way, when delivering a software system we are going to plan for, design, build, test, and deliver. Let's see:

- What should we build? How will this piece of software address our needs? Does it make sense to build it ourselves, or would it be better to buy it on the market?
    These are all managerial questions, that should be addressed way before a single line of code is written. Consider this example: If the company that wants to build a Time Recording system wants to only use it internally, the said system should be able to support users up to the company's growth rate; say maximum 500 employees after 10 years. In contrast, if the aim is to make the system available on the market, then the developer team should consider scalability from the very beginning. On a technical level the system will provide the same functionality in both scenarios, but under the hood, most of the technical aspects, from architecture to libraries used and beyond, will be different.

- Given the general idea/vision on what we want to build, we have to move to the specifics of designing the system, from the architecture all the way to functions, classes and their specifications.

- The process of writing the actual code is where we put flesh around the bones/structure.

- We also have to make sure that the system does what is intended to do; we have to test it

- Any system should be deployed and made available to its actual users although it would be great if there no bugs discovered, or no changes in technology stacks that would warranty major changes to a system just to keep it running, the world is not like that. Therefore, maintanance is necessary for any system that will be deployed and used for some time.


## Things to do before coding
Regardless of the process that you follow (traditional and plan-driven vs lightweight and adaptive), there’s a set of common things that really drive, influence and shape the resulting software architecture.
1. Functional requirements. In order to design software, you need to know something about the goals that it needs to satisfy.
2. Quality Attributes. Quality attributes are represented by the non-functional requirements and reflect levels of service such as performance, scalability, availability, security, etc.
3. Constraints. 
4. Where constraints are typically imposed upon you, principles are the things that you want to adopt in order to introduce consistency and clarity into the resulting codebase.
Keep note of the fact that Technology is not an implementation detail- technology choices should be included on architecture diagrams. Technology isn’t just an “implementation detail” and the technology decisions that you make are as important as the way that you decompose, structure and design your software system.

Functional requirements are captured through techniques such as user stories

Examples of non functional requirements:
 - Performance (e.g. Responce time, Latency)
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
  
  
 In the end of the process of examing all the above, the team should have an architectural diagram including technological choices, along with a document with all the choices to the questions above and the rationale for these choices.






