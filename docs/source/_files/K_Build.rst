==============================================
Build the thing right
==============================================

Coding Standards
https://www.jamesshore.com/v2/books/aoad1/coding_standards
Coding standards in software development are agreed rules and guidelines that define how code should be written and maintained so that it’s consistent, readable, and easier to review and change. They typically cover both “style” and “practices.” 
Of course, they are not exclusive to Agile, as any project following any methodology does have some form of standards. Yet, as we have seen, striving for technical excellence and high quality is necessary for an agile project to work. One can think of it in this way: with a bad up-front design, the solution might not be optimal but there are chances to finally build something. If the team writes messy code, without even a bad up-front design, the mess will quickly bury the project.
Common areas that the standards cover, are:
Code style & formatting: naming conventions, indentation, whitespace, line length, file/class organization.
Naming conventions: how to name variables, functions, classes, constants, and files (e.g., camelCase vs snake_case).
Code structure & readability: consistent patterns for structure, avoiding deeply nested logic, clear method sizes.
Refactoring practices: what, when, and how to refactor.
Comments & documentation: when to document, how to document public APIs, and what kinds of comments are allowed/required.
Error handling: how to handle exceptions, return values, and logging practices.
Security practices: avoiding common vulnerabilities (e.g., injection, unsafe deserialization), safe handling of secrets, input validation requirements.
Testing expectations: what tests to write, minimum coverage expectations, and how to structure test code.
Use of libraries/frameworks: preferred ways to do common tasks, banned/legacy patterns, dependency rules.
Tooling enforcement: linters, formatters (auto-format), static analysis (SAST), unit test runners, and CI checks.
Version control habits: branching/commit message conventions and review requirements (sometimes included as “engineering standards”).
On a technical level, coding standards are team and project specific. They have a certain degree of subjectivity and in many cases tie with the language / library / software paradigm used. Is camelCase any better than snake_case? The important issue is for the standards to be agreed upon and accepted by the team, and they should be followed; that’s all that matters.


Code review
As per wikipedia:
Code review (sometimes referred to as peer review) is a software quality assurance activity in which one or several people check a program mainly by viewing and reading parts of its source code, and they do so after implementation or as an interruption of implementation. At least one of the persons must not be the code's author. The persons performing the checking, excluding the author, are called "reviewers".
It is common that the review takes place before merging branches, or deploying code to production. The feedback is usually given by colleagues, either other developers, a manager, or a tech lead. One of the most familiar forms of code review is the Github pull request, in which developers leave comments on specific lines of code and, ultimately, approve or reject the proposed changes.

Companies that perform code reviews, spend the extra effort for the following benefits, as reviews help with:
finding defects while the code is in development. Not only outright bugs - which mostly are being caught by tests, but also issues with the overall code quality, the architecture, etc. A stitch in time, saves nine...
transferring knowledge between the participants, which helps individual developers learn new skills and improve.
breaking down possible barriers and create common ownership of the code base for the whole team.
A usual way to perform a code review is with a pull request - when a developer finishes the task being developed, asks a designated team member or the lead developer to merge the changes into the code base. Then either other developers, asynchronously, leave comments on specific lines of code and, ultimately, approve or reject the proposed changes, or do the same synchronously with all the participants present.

Assuming that the code has been developed as a task which is part of a story then there should be the definition of what Done actually means. This definition provides the basis for a list of points to consider when performing the review - passing the various tests, being documented, conforming to the agreed coding standards, etc.

In this way, the review is less subjective. If the participants are also attentive with language and communication, like not being offending in their comments, the whole review process can be fruitful and constructive for all participants.
Pair programming with rotating pairs / Mob programming
Having more pair of eyes, usually lead to better results when solving problems, or writing code. 
A practice coming from eXtreme Programming is pair programming. It consists of two programmers sharing a single workstation (one screen, keyboard, and mouse among the pair). The programmer at the keyboard is usually called the “driver”, the other, also actively involved in the programming task but focusing more on overall direction is the “navigator”; it is expected that the programmers swap roles frequently. 
It is commonly used during tasks like implementing features, refactoring risky code, or tackling complex parts of a user story. It is used because of the perceived benefits that include the following:
Better code quality: “programming out loud” leads to a clearer articulation of the complexities and hidden details in coding tasks, reducing the risk of error or going down blind alleys
Better diffusion of knowledge among the team, in particular when a developer unfamiliar with a component is paired with one who knows it much better.
Better transfer of skills, as junior developers pick up micro-techniques or broader skills from more experienced team members.
The technique of Mob programming, turn the pairing knob to 11. Instead of pairs, we have the whole team working together on a task. Although that might seem like a waste there are benefits that might actually worth it.
There is no time lost to other separate communication channels, like meetings and emails, as everything is decided on the spot.
The code produced is up to, or close to, the level of the most competent team member on a certain issue, while at the same time different people with different skills contribute to the solution. Better quality translated to fewer bugs, easier code to maintain, etc.
The team as a whole is familiar with the codebase, so the work is more stable no matter the individual team members’ rotation. Also there is no need for extra code review time and other knowledge transfer activities.
The caveats are that this is an intense activity and should be used in fixed intervals, plus the fact that some people just prefer to work it alone. So, use with caution.
Red-Green-Refactor
The RGR in, in narrow terms, an approach to Test-Driven-Development, but it extends to the test first approach, in more general terms. What do the terms stand for? In the context of a unit-test we have:
Red: Write some tests for the desired behaviour first, and run it. They should fail (that’s the “red”) because the feature isn’t implemented yet.
Green: Write the minimum amount of production code to make those tests pass. Run tests again, and they should go “green.” For as long the code hasn’t changed, the test should go green.
Refactor: Improve the code’s structure/quality without changing its external behaviour. Keep running tests to ensure everything stays green.
This way of thinking is not only about TDD, but it extends to other kinds of tests, like acceptance testing. Since a user story should be testable, and the acceptance criteria defined along for the rest of the story to be Ready to development, the resulting acceptance tests can be written before the story has even started being implemented.
Effectively, the RGR is the short feedback loop idea applied to testing

Code smells
A code smell is a sign that something in the code may be poorly written or headed toward problems—like bugs, poor maintainability, or technical debt—even if the code still “works.” One way to look at smells is with respect to principles and quality: Code smells are usually not bugs; they are not technically incorrect and do not prevent the program from functioning. Instead, they indicate weaknesses in design that may slow down development or increase the risk of bugs or failures in the future.
There is a certain degree of subjectivity, as different programming languages, frameworks, programming paradigms, do things differently. The term was popularized by Kent Beck on WardsWiki in the late 1990s, and the usage of the term increased after it was featured in the 1999 book Refactoring: Improving the Design of Existing Code by Martin Fowler, so you might want to take a look at these sources.
Example of code smells are:
The Shotgun surgery. This happens when trying to introduce a change in one place, and you have to make changes in other, unrelated places in the code. That might be because a piece of code is copied all over the place, instead of properly abstracted in a class or function. Or because there is no proper interface between two ‘modules’, so when we change the specific implementation in one, we also have to change the specifics in the other.
Or the too many parameters in a function. This is an indication that possibly the function does many things at the same time.
A code smell, is a symptom that might come from different causes. There are tools that help us spot the smells. For example, the Python library Pylint does static code analysis of source code and identifies certain code smells.
Once we know there is something fishy, the cure is in changing the code, and for doing so we use the following technique.
Code Refactoring
Simply put, code refactoring is the process of restructuring existing source code — changing the factoring — without changing its external behaviour. Refactoring is intended to improve the design, structure, or implementation of the software (its non-functional attributes), while preserving its functionality.
Typically, a refactoring is related to a code smell, and it is applied in a series of standardized basic micro-changes, each of which is (usually) a tiny change in a computer program's source code that preserves the behaviour of the software
Let’s see the example of Constant and Magic Numbers. This is an identified code smell that happens often, and where there is a literal value embedded in some computation, like total_value * 0.1, where the literal stands for a discount rate. What happens if the rate changes? In how many places have we inserted this number? Is 0.1 somewhere else, still the discount rate or something else? The code works but things could easily go wrong, so this is definitely a code smell.
How do we solve that? Well, there is a recipe for that! (https://refactoring.com/catalog/replaceMagicLiteral.html) ‘Replace Magic Literal’ by Fowler which instructs us to replace the literal with a named constant, and use the constant instead. Extra points for getting all the named constants that have business meaning defined at the very beginning of that code section, or even in a configuration file.
The point is clear; whenever there a smell, there is also a solution – refactoring to the rescue!
Design principles
First of all, what is software design? It is the structure of the implementation of a software solution so it works well and is maintainable. It translates requirements into concrete choices at the level of code structure and behaviour. For example, how to decompose the system into modules and what should their responsibilities be.
Up to now we have gotten to the point where we write the tests, write the code to make the tests pass, check for code smells, and fix these using refactoring recipes. But, how do we know that the overall design will be ok? There are different approaches that help us with that. The common theme is that if we apply certain rules or principles, then we should be ok.
One approach, Domain-Driven Design by Eric Evans (https://fabiofumarola.github.io/nosql/readingMaterial/Evans03.pdf), places emphasis on using concepts from the specific domain in order to model and code the system. In Evans’ words:
1. For most software projects, the primary focus should be on the domain and domain logic.
2. Complex domain designs should be based on a model.

Another approach, which is rather diffused, is known by the acronym SOLID, proposed by Robert C. Martin. The acronym consists of the 5 principles
Single responsibility principle states that there should never be more than one reason for a class to change.
Open–closed principle states that software entities should be open for extension, but closed for modification.
Liskov substitution principle states that functions that use pointers or references to base classes must be able to use pointers or references of derived classes without knowing it.
Interface segregation principle states that clients should not be forced to depend upon interface methods that they do not use.
Dependency inversion principle states that one should depend upon abstractions, not concretes.
(Take a look at this article (https://medium.com/@doogwoo/what-are-the-solid-principles-795faedf5298) for a nice discussion on the principles, with code examples; really useful)

In contrast, Dan North criticised SOLID and instead proposed CUPID:
Composable: plays well with others
Unix philosophy: does one thing well
Predictable: does what you expect
Idiomatic: feels natural
Domain-based: the solution domain models the problem domain in language and structure

Without getting bogged down in the details and since we don’t want to take sides with any one approach, it is enough to say that if you chose to follow and apply certain principles, then as the codebase grows, the consistent application of these principle with be reflected on the code base. If is it the SRP or the Unix philosophy, the code base will have entities, be it classes or functions, that will be smaller in size and scope. Slowly, there will be an emergent design visible in the codebase.


Incremental architecture
Up to this point we have talked about the design, so it is now time to tackle the issue of architecture.
Software architecture is the high-level structure of a software system; how its main parts are organized and how they interact in order to meet requirements like performance, reliability, security, and maintainability. A useful way to think about it: architecture is the “blueprint” for how you build and evolve the system. Architecture is the big-picture organization (major components, interactions, deployment structure), while design is the detailed implementation structure for those components (how they’re built internally, and how they collaborate through interfaces).

definition by Grady Booch: 'Architecture represents the significant decisions, where significance is measured by cost of change' It’s about the decomposition of a product into a collection of components/modules and interactions. Usually, we refer to the components that comprise the software system and the interactions between them. Define component Architecture must fulfil the business and technical requirements while considering quality attributes such as performance and security. the decisions made regarding software architecture significantly impact how the system evolves and achieves its objectives.
Architecture as a picture/model is used as a blueprint of what are going to, or have already, built. It is both an analytical tool, by looking at the blueprint we can reason about the system, and also as a communication tool so that everyone involved knows what the team builds
Types of architecture application architecture is inherently about the lower-level aspects of software design and is usually only concerned with a single technology stack system architecture is one step up in scale from application architecture, since most software systems are actually composed of multiple applications across a number of different tiers and technologies. In other words, you also have the overall structure of the end-to-end software system at a high-level.


Architecture vs design A system's design shapes things more at the code level - the way each component works, the purpose of each element, and concern of this kind. Significant decisions are architecture; the rest is design.

The relation between architecture and design: Architecture is design at a higher level of abstraction while design is architecture at a lower level of abstraction. For hexagonal architecture, with the core at the centre and ports on the outside layers, if one does not observe the 'D' (dependency inversion) in 'SOLID', will get rigid system where every change in the UI will have to be propagated all the way to the business logic.

example of horrible architecture and design: Call scrappy from within flask and display the scrapped data. The code will work (verify that), but:

any change to any part either scrapy of flask will be difficult because the other part will have to change too
testing will be more difficult, because if the page does not show what we expect, we should check two conceptual blocks together rather than each separately
scalability will most probably be an issue, because when you bundle things together and one part is not performing well/fast enough, it becomes a bottleneck for all the bundle.
examples of architectural decisions:

the programming language
technologies and frameworks and libraries
type of architecture as in monolith vs microservices
Code that does not compile/run is a serious but obvious problem. The risk with code that does compile/run is that it might be a non-obvious problem.

Five things every programmer should know about software architecture as per Simon Brown:
1.software architecture isn't about big design upfront
2.every software team needs to consider software architecture
3.the software architecture role is about coding, coaching and collaboration
4.UML is not necessary
5.good architectures enables agility
qualities of good architecture. the application should be:
testable
secure
performant
scalable
usable
reliable
A way to capture architecture and design, by Simon Brown, is the C4 model:
Context
Containers
Components
Code (or Classes)
Examples of Architectures: - layered - package by feature - ports and adapters (the core is the domain and is technology agnostic, while the outside is the infrastructure, the technology specific. There is one rule, the outside depends on the inside) - package by component

Note: make sure that the codebase reflects the architectural intent. For example, without encapsulation and information hiding, with all classes being public, every section of the code can access any other section, which can destroy any architecture.

IMPORTANT: Criterion of good architecture: It enables agility - the ability to respond as quick and as easy as possible to external stimuli. It usually comes with modularity.

https://www.infoq.com/articles/architecture-five-things/ Software architecture isn’t about big design up front The upfront design process should therefore be about understanding the significant decisions that influence the shape of a software system rather than, for example, understanding the length of every column in a database. In real terms, I’d like teams to really understand what they are going to build, how they are going to build it (at a high-level, anyway) and whether what they’ve designed will have a good chance of actually working. This can be achieved by identifying the highest priority risks and mitigating them as appropriate, writing code if necessary. In summary, up front design should be about stacking the odds of success in your favour.


Version Control and branching strategies
On git branching: each branching strategy is suitable for a specific context. For example, working with feature branches makes sense for open-source projects where people are not fully on project so while they might work on something other should be able to move ahead. In projects with a dedicated full-time team, given the presence of an automated testing suite, maybe it does not make sense.

Context always matters.

Patterns for Managing Source Code Branches https://martinfowler.com/articles/branching-patterns.html


Branching Strategy
Semantic Commits
## On git message formatting

A well-crafted Git commit message is the best way to communicate context about an individual code change to fellow developers (and indeed to their future selves). A diff will tell you what changed, but only the commit message can properly tell you why. Overall, a clean and well formatted commit history can help someone understand what happened, and why it happened that way, years ago. Since a project’s long-term success rests (among other things) on its maintainability, it would be a waste for a developer not to use one of the more powerful tools: the project’s log.

As with many written forms of communication, we can break our suggestions down to three aspects: - Style. Markup syntax, capitalization, punctuation, etc. The point is to create a consistent log that will be easy to read. - Content. What kind of information should the body of the commit message (if any) contain? What should it not contain? - Metadata. How should issue tracking IDs, pull request numbers, etc. be referenced?

### Style With respect to style, these are some initial suggestions: - Use a concise subject message less than 50 characters (the usual convention) - Utilise the body to explain what and why vs how - Be consistent with formatting like capitalisation, punctuation, etc

### Content With respect content, the idea of Semantic Commit Messages is quite useful.

Semantic Commits are committed messages with human and machine-readable meaning, which follow particular conventions
In more detail: - The commit messages are semantic - because these are categorized into meaningful types, indicating the essence of the commit - The commit messages are conventional - because these are formatted by a consistent structure and well-known types, both for developers and tools

The Conventional Commits specification is a lightweight convention on top of commit messages. It provides an easy set of rules for creating an explicit commit history; which makes it easier to write automated tools on top of.

It features a specific structure

<type>[optional scope]: <description>

[optional body]

[optional footer(s)]

An example

fix(client-logo): correct capitalisation in file path

The client logo would not show up in the deployed version, although it worked locally. The actual filename and the path provided had different capitalisation. The local Windows env read it just fine, while the Linux deployment env did not read the file

closes issue #543

And here is another one

fix: fix foo to enable bar

This fixes the broken behaviour of the component by doing xyz.

BREAKING CHANGE Before this fix foo wasn't enabled at all, behaviour changes from <old> to <new>

Closes D2IQ-12345

Let us take a closer look

First, we start with the list of commit types. Feel free to create the types that suite your project:

feat : a new feature is introduced with the changes
data : any change related to data - preparation, exploration, etc
fix : a bug fix has occurred
chore : changes that do not relate to a fix or feature and don't modify src or test files (for - example updating dependencies)
refactor : refactored code that neither fixes a bug nor adds a feature
docs : updates to documentation such as a README or other markdown files
style : changes that do not affect the meaning of the code, likely related to code formatting such as white-space, line length, and so on.
test : including new or correcting previous tests
perf : performance improvements
deploy : deployment / continuous-integration related
revert : reverts a previous commit
The types may be followed by the scope of the commit, a noun that describes the relevant section of the codebase - for example a feature tied up to a specific section of the project.

Then, there is the short description of the changes - it's like a header to the body that, optionally, follows next. In the body one has the opportunity to explain WHAT the change is, but especially WHY the change was needed.

In the end, the optional footer mention consequences which stems from the change - such as announcing a breaking change, linking closed issues, mentioning contributors and so on.

### Metadata As we saw, the footer is the place for useful metadata like issues referenced, PullRequests, etc. Depending on the way the project works, one should establish consistent rules for referencing the relevant project management artifacts, like reported bugs, PullRequests, etc. With consistent rules metadata referencing rules the Git log history can be easily connected to the rest of the project like for example which are the corresponding commits for a certain user story.

Ideas adopted from: - [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0-beta.4/) - [Semantic Commit Messages](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716) - [How to Write a Git Commit Message](https://cbea.ms/git-commit/) - [How to write better git commit messages](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)
Test Automation
First of all we have to stress a key difference between testing in Agile and waterfall. The activity might be the same, but the role is different. In waterfall, testing is a quality control activity. Someone wrote the code, and then someone else controls that the code lives up to the specification. In Agile, testing is part of development. The developer writes the tests, because the developer uses the tests’ output to guide development. Same activity, different role.
From the Agile perspective automation is the effort to make the feedback look as short as possible and therefore learn as fast as possible. It is the use of software (separate from the software being tested) for controlling the execution of tests and comparing actual outcome with predicted. Test automation supports testing the system under test (SUT) without manual interaction which can lead to faster test execution and testing more often.
Writing tests takes time, and creating an automated test suite takes even more time! The point from the Agile perspective is that all this is necessary. 
Build Automation
Build automation is the practice of building software systems in a relatively unattended fashion. The build is configured to run with minimized or no software developer interaction and without using a developer's personal computer. Build automation encompasses the act of configuring the build system and the resulting system.
What it typically includes:
Build steps: compile source code, resolve dependencies, bundle assets
Testing: run unit/integration tests, linting, static analysis
Packaging/artifacts: create versioned outputs (jars, docker images, installers, etc.)
Release/deploy (sometimes): push artifacts to registries/environments
Repeatability: same process runs reliably across developer machines and CI servers
Build automation speeds up development, reduces mistakes, and makes builds consistent and traceable, all of which is a required step for implementing continuous integration and continuous delivery (CI/CD), which nowadays are considered best practices for software development.
CI/CD pipeline
The CI/CD paradigm is a workflow for delivering software changes frequently and reliably by automating two stages:
CI (Continuous Integration): every time code is committed, the system automatically builds the project and runs checks like unit tests (and often linting/static analysis). The goal is to catch problems early and keep the main branch healthy.
CD (Continuous Delivery / Continuous Deployment):
Continuous Delivery: automation builds and tests every change and prepares a releasable artifact, so it can be deployed to production when approved.
Continuous Deployment: automation not only prepares but also deploys automatically to production after passing tests.
Typical CI/CD pipeline looks like:
Code commit / pull request
Automated build
Automated tests (unit → integration → sometimes end-to-end)
Build artifacts (package or container)
Deploy to staging (and possibly production)
Monitoring/feedback
Key idea: reduce manual release work and shrink the time between “code change” and “running software,” while keeping quality gates (tests) in the pipeline
These practices implement the ideal of Agile since the early 2000 but have grown in significance with the software as a service paradigm and especially with large companies that maintain products with millions of active users daily.  
