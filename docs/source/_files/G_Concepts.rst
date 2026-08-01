##########
Concepts
##########

The goal here is to present some fundamental ideas/concepts that shed light to the whole topic. These ideas underlie both the Agile concepts we presented in the previous section, and at the same time the actual implementation of Agile that we will present in subsequent sections.

Team empowerment
========================================
There is a standard wording about empowered teams in agile: Team empowerment is the practice of giving teams the trust, context, support, and authority they need to make decisions, take ownership of their work, and improve how they deliver value.
Beyond the specifics of how this translates into practice, I believe the that the most important thing to say, is that the whole agile proposition will not work without team empowerment. There is a really simple reason for that.

The team sits at the centre of the feedback loop – we try something, see how it works, we adjust course, try something more, etc. If the team cannot respond to this learning experience, then it cannot implement agile at all! For example, it is problematic to have to wait for months, for 4 permissions to install a large white-board in main work room.
Obviously, team empowerment does not mean that a team does whatever it wants. The requests will go through some organisational processes. But the organisation should be receptive and responsive to these requests; that is a prerequisite for agile to work

Whole team approach
========================================
The standard definition of the whole-team approach is that of a collaborative approach where all the team members with necessary skills and knowledge will do their best to accomplish the goal thus contributing to the success of the project.

Again, there is a simple reason why agile would not work without this approach. Since different activities like analysis, coding, testing, take place at the same time and in conjunction, without formal hand-offs in between, without the whole team approach we would get a mess instead of a working product. For example, if the team does not collaborate on how the user story can be tested, then the testers task might become impossible. Vice versa, if the tester sees a potential problem right at the time of user story analysis, there is no point in wating until the bug has been created.

Customer Involvement
========================================
In our case the term customer means the end user of what the team builds, but usually it refers to corporate settings. It is considered important because it keeps the team on track building the right thing. It would be much harder to achieve that objective without the customers being involved.
There are different ways in which customers help with this objective.
It is much easier for the team to understand what matters most right now, so work is focused on the highest-value outcomes. It is also much easier for the customers to make decisions about scope, quality, and timing, especially when priorities conflict.

From the perspective of the team, it improves requirements clarity: Needs often start fuzzy. Customer input turns them into clear, testable acceptance criteria that the team can implement.
Communication is much faster when customers assess the product frequently, so that any misunderstandings are caught early instead of after months of development. An extra benefit of regular feedback on working software is that with it the team avoids building features that don’t match expectations.
Overall, when the customers are part of the team, having influenced the outcomes and seeing the progress being made, alignment and buy-in from the business side increases dramatically.
Incremental and iterative development with short feedback loops

There is a lot to unpack here. Incremental and iterative development means that we build small pieces of software, often. That wouldn’t work though without short feedback loops; let us see why.
Even waterfall can be iterative, if we assume that an iteration takes years. That is not good enough though in a fast-changing environment. Therefore, we have shorter iterations, and consequently smaller increments. How do we know we are on the right path? Imagine for a moment that we build small increments, many times over, but the stakeholders and users will not see the product until after a year. Well, this is as good as the waterfall approach, because in the meantime, without feedback, we don’t know how we are doing.
Therefore, the shorter the feedback, the fastest we can adapt to the reality. Without some software to show to the users, there can be no feedback, and thus the need for the incremental and iterative development.

eXtreme programming ( wikipedia.org/wiki/Extreme_programming ) has taken this idea to the maximum with short feedback loops from the lowest level of coding, with test driven development, to the short releases.

Prototyping
====================
We saw that short feedback loops are essential, and that in order to get these loops, we build small increments. There is an extension to this idea in the form of prototyping. The first thing that comes to mind, is the Minimum Viable Product (more on that, below) that can get us started with development. But the idea of prototyping extends to any phase of the project.

The core insight behind this idea, is to get the maximum amount of information with the least amount of effort. We can prototype any feature, at any point in time. A prototype might be a simple UI sketch that can help us validate some of our assumptions about the users. We don’t have to build the whole thing coded all the way to the database to find out the user didn’t like the UI.

The thesis is clear: prototyping is not a phase before agile, it is a practice within agile. Teams that embed prototyping into sprint rhythms catch design flaws before they become engineering debt. They move faster overall because they waste less time building the wrong things. Does this mean the team “slows down”? Yes, in the sense that the team performs an extra task. Does this mean prototyping slows you down? No, the team moves faster overall because they waste less time building the wrong things.


Shift left
====================
We have already seen how the sequential progress in waterfall, from requirements, to design, to development, to testing, to deployment, gets compressed into shorter cycles where all these activities take place almost simultaneously. In order to create a simple mvp and get feedback from users, the team needs to be a bit of everything all the way to deployment. Shifting left, with respect the linear progression of waterfall, is the practice of performing an activity as early (left) as possible.

For example, with testing the team does not simply wait until a piece of code gets written. Rather, already with the user story the team decides on the acceptance criteria and test (more details below), the developers might use test-driven development and write their unit tests before the code, and testers write integration tests as the code is being developed.

Test First
====================
This practice came out of eXtreme Programming (although https://en.wikipedia.org/wiki/Test-driven_development it seems that it was also practiced in the past), and it an implementation of the idea of short feedback loops. The main idea is that if one forces oneself to write a test before the code, then once the code is written, executing the test against the code, gives immediate feedback about the code. That’s it, in a nutshell. This practice has then taken a life of its own, with different frameworks that address different situations.

Initially, we had Test-Driven Development that dealt with unit-tests, that is small individual pieces of code like the methods of a class, and that can best be described through its 3 rules:
    • Do not write any production code without a failing test first.
    • Write only enough test code as is sufficient enough to fail.
    • Only implement a minimal code that makes the failing test pass.

Unit tests run fast. If they don't run fast, they aren't unit tests.
What we should add here is the difference with waterfall, where we start writing code without detailed technical descriptions of what we should build. In that situation, writing the test upfront works like a design workshop where we make clear what the requirements are. That leads to the idea that tests are executable requirements that lead to less fear of breaking things, easier changes, increased transparency, etc.

A technical note: how can one test something that does not exist yet? Well, we assume it exists and we mock it. Mock objects are a popular tool for isolating classes for unit testing. When using mock objects, your test substitutes its own object (the "mock object") for an object that talks to the outside world. In doing so, it avoids time-consuming communication to a database, network socket, or other outside entity.

But not all test are unit-tests. Acceptance test-driven development is the same idea, applied to acceptance tests. What is the difference? Acceptance tests are from the user's point of view – the external view of the system. They are written, ideally, along with the user story that describes the system from the perspective of the user. It is a collaborative effort by requirement requester (product owner, business analyst, customer representative, etc.), developer, and tester.

There are other variations that place emphasis on various aspects of the process, like ‘Behaviour-driven development’ that places more emphasis on the language used; it should be closely related to the domain of the system. ‘Specification by example’ puts the emphasis on using realistic examples instead of abstract statements about the system.

Overall, having the test from the very beginning has many advantages. Tests are (or they should be) deterministic, they either pass or fail. They capture requirements in a clear way; we can agree (or disagree) that this test captures the intent of the user story, but it’s clear. Having the tests and executing them often takes away the fear of introducing errors in other places than the one we work at.

The main issue is the cost of creating the infrastructure for running the tests, preferably automatically.

Just barely good enough
========================================
“Just barely good enough” in Agile is the idea of meeting the minimum level of quality needed to deliver value, rather than aiming for perfection upfront.
It is not excuse for sloppiness, like doing a poor-quality job because quality is in the eye of the beholder! It is the purpose for an artifact that determines if it is sufficient, not the creator of it. If the specific purpose requires an excellent, detailed artifact then it is JBGE when it reaches that point of being excellent and detailed, and not before that.

What it is, is an optimisation strategy where the point is to maximise the reward and minimise the effort. Think of it as the middle point in the spectrum between two opposites: 
analysis paralysis on the one end, where we get stuck endlessly on a phase trying to make it perfect
and putting no effort at all

That might seem trivial, but it has powerful impact on the how the project runs. For example, how much time do we have to spend in deciding the architecture? Well, enough to allow us to build a “Minimum Valuable Product” get feedback and keep moving on. If we fix before-hand a specific amount of time, we run a double risk: either move on before we are ready or just waste time dotting the i’s and crossing the t’s.

Instead, we have a powerful tool to optimise locally the time spent on each activity. If, for every task, I know that I did what was necessary for me to move on and not more than that, then I know that I have globally optimised the time I have spent in all the different phases, without having to enter complicated optimisation routines. 
https://agilemodeling.com/essays/barelygoodenough.htm

Clean Code
====================
How to write for others, in order to read, understand, and modify. It helps with transparency, communication, trust, etc.

What Clean Code is about:

Definition
Main sources
Central ideas
Note that the ideals below pertain to design more than anything else. Still, they have synergies with clean code as an overall concept. Five things that matter in making the code easy to change: 1.Modularity 2.Cohesion 3.Separation of concerns 4.Abstraction / information hiding 5.Loose coupling

The secret for good design is simplicity. Your code has the following properties: it works it communicates clearly there is no duplication there are no extra pieces

Technical Debt
====================
Ward Cunningham coined the term technical debt in 1992. He devised this debt metaphor to explain to his boss the need to refactor the financial product they were working on::

	“Shipping first time code is like going into debt. A little debt speeds development so long as it is paid back promptly with a rewrite.... 
	The danger occurs when the debt is not repaid. Every minute spent on not-quite-right code counts as interest on that debt. 
	Entire engineering organizations can be brought to a stand-still under the debt load of an unconsolidated implementation, object-oriented or otherwise”
	
	https://c2.com/doc/oopsla92.html

How do we know that are going deep into technical debt? Usual signs are: 

* Slower development because changes are harder
* More bugs in new releases
* Longer build/test/deploy times
* Needing more coordination to safely modify code

All the above are signs that although our product meets its requirements and the project still runs, it is highly probable that we will face problems in the future. 
There are various ways in which technical debt builds up. We might build a quick and dirty implementation that skips refactoring or thinking about a better design, because of a deadline. We might skip writing tests and as a result poor test coverage will make future changes more prone to subtle issues that will go on slowing us down.
Messy architecture (tight coupling, unclear boundaries)
Duplicated code, inconsistent patterns, lack of documentation
Ignoring performance/security needs until problems appear

Obviously getting into debt might be a valid business decision. We borrow to build a business, or add capacity, or whatever else. For as long as we have a valid plan to repay the debt, we are fine. It is similar with technical debt. We might choose to leave a piece of code as is, and just add more code to our system. That is fine for as long this is a conscious business decision; we might for example have a deadline coming up. But we have to repay the debt down the road with some interest; in that case it will take us longer to clean the code since it is now longer and more complex.
How do we pay it down, then?

Spend some time to assess the whole architecture and identify sore spots, like why is this module creating so much more errors than the rest, and what can we do about it?
Then we have to put the time and effort to refactor and improve the structure. Break a function into smaller functions here, reorganise the logic there, can take us a long way.
Adding new test and strengthening existing ones is also helpful. By doing so we leave less space for bugs to creep-in and we make the whole structure more transparent.

The main point here is that one cannot reduce the cost of software by cutting corners. The cost of a piece of software depends on the scope, and the productivity of the team. When we cut corners, we reduce the cash flow, we pay less, but shift payments of the rest of the cost in the future; payments that will be made with interest.

Last responsible moment
==========================
Delay important decisions up to the last responsible moment, until you really need to make them
As we said previously, everything revolves around the ability to respond to changes, fast. Since the work is being done incrementally in small batches, without a detailed upfront plan, some rework is inevitable. For that reason, minimizing rework while maximizing feedback is the central concern of the agile team. The last responsible moment is the sweat spot; too early and the team risks to make decisions without validation; too late and there will be a lot of rework.

Rework is, at its core, caused by having to undo decisions that have been made in the past.
Rework is triggered by learning new things that invalidate prior decisions

Sustainable pace
====================
The Agile mindset views recourse to overtime, other than on an exceptional basis, as detrimental to productivity rather than enhancing it. Overtime tends to mask schedule, management, or quality deficiencies; the Agile approach favours exposing these deficiencies as early as possible and remedying their underlying causes, rather than merely treating the symptoms.

This observation ties in with the rest of the mindset; we need a team that will perform many functions of the SDLC at the same time, and they have to do it at a high level of quality. An overworked team will not produce great quality, but simply more bugs, that will take more time to fix. In a sense, overworking is not increasing output; it produces the same with worse conditions for the team (longer hours) and the company (overtime payments). 
There is no reason for a team to work like that.
