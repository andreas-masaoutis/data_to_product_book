###############
Documenting
###############

I thought Agile did away with documentation! “Working software over comprehensive documentation” is one of the 4 tenets, so what are we talking about?
The misconception is about documentation in waterfall, which details what the code should be doing way before a single line of code gets written. That does not mean that the actual should be documented!

There are different levels and kinds of documentation that serve different purposes, yet there is overarching aim: the documentation provides the context for what the code does (or how it is structured). It is aimed at conveying all the necessary info to the consumer of the documentation, be it a developer, a stakeholder, or a user, when this person is trying to understand something related to the software product. As with any kind of writing, the motto ‘know your audience’ fully applies here as well.

On the technical side, we start with all the artifacts that define what is to be build (user stories, etc) which should can be considered as a form of documentation.
Inline documentation within code, should be about the why something is written the way it is, while the how is the code itself.

Different languages use different mechanisms, but then almost all use some kind of documentation at the level of a function/class and module. Python has dockstrings and Java has document comments.
As we move at higher levels of code, Architectural Decision Records are a useful tool. ADRs are a form of documentation that record any architecturally significant decisions that impact a project. For an impact to be considered architecturally significant within a software project context, it should affect the structure, non-functional characteristics, dependencies, interfaces, or construction techniques.

One can automatically create UML diagrams of a given code base and document its structure. Although these tend to be rather messy, so some form of simplification is needed for them to be correct and informative at the same time. 

Then on the user side there are all sorts of user documentation. The main thing is to be able to define what the reader needs and pass the necessary pieces of information in a clear and concise way. A simple README.md file is the usual entry point for any project. Then we can have detailed documentation deployed at readthedocs.

A really good guide on documentation can be found at - https://www.writethedocs.org/guide/
