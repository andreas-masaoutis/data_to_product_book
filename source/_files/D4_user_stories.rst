=========================
The User Stories
=========================

What are the User Stories, how to write them, and use them:

- What are they
A user story, as a placeholder for discussion, facilitates it by describing the problem we want to solve with the software, who will use it, why and how they will use it. The discussion then is about arriving at a solution to the problem while at the same time creating a shared understanding among the participants.
Stories help us separate WHAT the system should do from HOW is will do it.
- How to write them
Writing stories just passively formulating requested solutions is a practice that dangerously nears Henry Ford's paradox: "If I had asked people what they wanted, they would have said faster horses".

The traditional user story framework is focused on capturing requirements for what we want to build and for whom, to enable the user to receive a specific benefit from the system. It has the following format:

As A…. <role>
I Want… <goal/desire>
So That… <receive benefit>


- How to use then

- Common mistakes with user stories https://www.youtube.com/watch?v=0HMsh459h5c
1.Direct translation from traditional 'requirements': A user story is a description of the problem we are trying to solve from the perspective of the user - it is not a tecnical specification. If the story only conveys the technical part and not the user need and context, the developers cannot do a good job even if the have good technical skills, as they will not understand what they are trying to solve.  The job of a software developer is not to write code, is to solve problems; in order to do so one needs to understand it. 
2.Too detailed stories that read as a contract. A story instead should be like a placeholder for a conversation. As the story is being born out of the realisation of a need, it should focus on the exactly that: the need of the user. It will later be used for the discussion between the product owner and the developers where the latter will contribute on the technical aspects of the solution. A too detailed story that goes all the way down to the details stiffles the discussion and the possibility to innovate. Instaed, it is the discussion that will lead the team to figure out the best way to implement the story
3.Too large stories. Good user stories identify a useful unit of work. For story to represent easily and rapidly produced new functionallity it should be a small increment in the behaviour of the system. Maximum time for story completion should be within a sprint, something like a week or two. Ideally, they should be shorter, like a day or two.
4.Value vs invaluable. Stories represent value to the user. They do not have to be the killer feature that does everything and even more. As with the large stories, invaluable stories tend to be overcomplicated, while as we said before it is far easier to work with smaller and simpler ones. First story could be create simple login, then require more secure password, address lost passwords, periodically reset passwords, etc.
5.Dependent stories. Ideally, stories should be implementable in any order, although some might more difficult to implement than others



Enter validation and we have Hypothesis-Driven Development:
Practicing it is thinking about the development of new ideas, products and services – even organizational change – as a series of experiments to determine whether an expected outcome will be achieved. The process is iterated upon until a desirable outcome is obtained or the idea is determined to be not viable.

An extension to the traditional user story with the structure to support Hypothesis-Driven Development would be the following

We believe that <this feature> <for these users>

Will result in <this outcome>

And We will know we have succeeded when <we see a measurable signal>


What functionality we will develop to test our hypothesis? By defining a ‘test’ capability of the product or service that we are attempting to build, we identify the functionality and hypothesis we want to test.

What is the expected outcome of our experiment? What is the specific result we expect to achieve by building the ‘test’ capability?

What signals will indicate that the capability we have built is effective? What key metrics (qualitative or quantitative) we will measure to provide evidence that our experiment has succeeded and give us enough confidence to move to the next stage.