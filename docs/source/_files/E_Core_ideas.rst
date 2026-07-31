================================
Core ideas of Agile
================================

Two main questions: - How to build the right thing - How to build the thing right
Let us start with a short and simple definition of what Agile is. It is the iterative and incremental creation of software, led by continuous feedback from users and stakeholders. That's all there is to it.

Agile means different things to different people. Actually, it came about as a point of convergence for various practices like RAD, XP and Scrum among others that were developed in the 1990's. The Agile Manifesto was put forward in 2001 and we can interpret it, in a sense, as the common denominator of the various practices that were circulating in the software engineering market at that time. Agile is what disciplined people had already been practicing in the wild. For that reason, we will start with the Manifesto itself. Here Agile manifesto one can find the original publication from 2001.

Manifesto for Agile Software Development (https://agilemanifesto.org/)

We are uncovering better ways of developing software by doing it and helping others do it. Through this work we have come to value:

Individuals and interactions over processes and tools
Working software over comprehensive documentation
Customer collaboration over contract negotiation
Responding to change over following a plan
That is, while there is value in the items on the right, we value the items on the left more.

Principles behind the Agile Manifesto (https://agilemanifesto.org/principles.html)
We follow these principles:
Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.
Welcome changing requirements, even late in development. Agile processes harness change for the customer's competitive advantage.
Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.
Business people and developers must work together daily throughout the project.
Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.
The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.
Working software is the primary measure of progress.
Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.
Continuous attention to technical excellence and good design enhances agility.
Simplicity--the art of maximizing the amount of work not done--is essential.
The best architectures, requirements, and designs emerge from self-organizing teams.
At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behaviour accordingly.

Although this is short, there is a lot to unpack.

First, we should note that the signatories of the manifesto had already developed various ideas during the 1990's : Sutherland and Schwaber had proposed scrum Beck, Jeffries and Cunningham had developed the eXtreme Programming practices Cockburn had proposed the Crystal family of methods Beck had proposed the test first methods Fowler had worked on Design patterns and refactoring Martin had worked on patters and the concept of Clean Code

The next thing to note is how the Agile Manifesto is a contraposition against the then prevailing software engineering practices in the corporate world. There would be two parties, that would create a detailed plan with the full requirements, captured in the extensive documentation and the Gantt Chart with the milestones, that should then be followed, with the hand-offs and sign-offs and the subsequent litigation in case something did not work as planned. Of course, we should not interpret the manifesto as an 'a priori' argument against the Waterfall approach but rather as one about its suitability in the new market conditions. It might have been ok to build software in that way for space missions in the past, but it is not suitable anymore in the kinds of projects the developers had to deal with. There are at least two changes that had rendered the heavy-weight project management processes of the past unsuitable.

First, time-to-market mattered in a disruptive environment. Instead of taking longer to build a perfect piece of software, it was a great competitive advantage to be the first to offer something - even if that was not perfect. In relation to that, the requirements captured and the contract signed some time ago, was not ideal; rather it would be far better to have the customer involved.

It doesn't seem a coincidence then that the 17 participants chose the word agile to describe their movement; everything revolves around the ability to respond to changes, fast.

In the next sections we are going to take a look at some of the approaches that led to the Agile Manifesto.

The Agile mentality is to be proactive, independent, empathetic, etc.

Mastery, Autonomy & Purpose To motivate employees who work beyond basic tasks, Pink believes that supporting employees in the following areas will result in increased performance and satisfaction:

Autonomy – A desire to be self-directed, it increases engagement over compliance. Mastery – The urge to get better skilled. Purpose – The desire to do something that has meaning and is important. Businesses that only focus on profits without valuing purpose will end up with poor customer service and unhappy employees.[5] https://techbeacon.com/app-dev-testing/organizing-your-agile-teams-think-autonomy-mastery-purpose
The skill set
T-shaped individuals for cross functional teams

Self-organising Teams
Whatever that means How the team could be organised.

https://www.youtube.com/watch?v=IDKJJDiK3Gw Rachel Davies at Unruly GOTO 2015 https://unruly.co/

One of the ways to organise the team is to have a set of broadly skilled people, that have collective ownership of the code and the product. Everyone can commit to the main which means they should be accountable. There are no separate groups of people that do the testing or maintain the infrastructure; the teams do that. And there is no layering of people and access to data. Also, these is no buffering between the business and the developers. The connection is immediate with the business and the product. There are no dedicated business analysts, product owners, or testers. these are all functions covered by the team members, and as a result there is no need for large teams 4-6 people is enough. Each team member does a certain amount of story research; they talk to the business and try to figure out what the needs are, and then they do the technical research on the available options, that will finally be presented to the rest of the team and stakeholders for decision to be made. The team's time is split between new story development, maintenance/technical improvement of the existing system. The teams are not entirely collocated and therefore there is the need for online boards to keep track of the work planned and done. All developers in the team can spent one day per week for learning, not necessarily on the immediate needs of the product. The team is tracking its activities, since there are no project managers to manage things around, so that the team can then inspect and adapt. With the retrospective the team has the 'ability' to decide what to track, how to measure the performance and what steps to take in order to improve. Collective ownership also extends to processes. The team makes things happen without relying onto any kind of specialist. The team does have specialists, but they are there to work with the teams and teach the teams. It's not a case of the specialist does a special thing. With cross-functional teams there are fewer bottlenecks. Additionally, the teams are fluid with team members rotating between the various teams, every x number of months. In the end, 1. the teams deliver value in a sustainable manner, so that the management can be reassured that things do work without having to manage things closely. Also, 2. the teams build change tolerant systems that are easier to modify. Finally, 3. the choice over what to do, makes it easier for team members to relate to the business needs, it means that people acquire more skills of greater variety by constantly learning, that makes their work more fulfilling, and as a result they stick with the team for far longer.

The team is the locus of business problems, technical solutions, and organisational processes Why Agile Fails in Large Enterprises - Large Scale Agile Transformation https://www.youtube.com/watch?v=Oo3zlOTbN2E 15:59
