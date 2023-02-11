# The fundamentals of building software

## The software development life cycle
No matter what the prefered software engineering methodoogy is, all of them are organised efforts to address a set of fundamental questions with respect to the development of a software. In other words, no matter in which way, when delivering a software system we are going to plan for, design, build, test, and deliver. Let's see:

- What should we build? How will this piece of software address our needs? Does it make sense to build it ourselves, or would it be better to buy it on the market?
    These are all managerial questions, that should be addressed way before a single line of code is written. Consider this example: If the company that wants to build a Time Recording system wants to only use it internally, the said system should be able to support users up to the company's growth rate; say maximum 500 employees after 10 years. In contrast, if the aim is to make the system available on the market, then the developer team should consider scalability from the very beginning. On a technical level the system will provide the same functionality in both scenarios, but under the hood, most of the technical aspects, from architecture to libraries used and beyond, will be different.

- Given the general idea/vision on what we want to build, we have to move to the specifics of designing the system, from the architecture all the way to functions, classes and their specifications.

- The process of writing the actual code is where we put flesh around the bones/structure.

- We also have to make sure that the system does what is intended to do; we have to test it

- Any system should be deployed and made available to its actual users although it would be great if there no bugs discovered, or no changes in technology stacks that would warranty major changes to a system just to keep it running, the world is not like that. Therefore, maintanance is necessary for any system that will be deployed and used for some time.
