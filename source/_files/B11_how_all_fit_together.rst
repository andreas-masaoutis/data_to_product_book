=====================
Summary
=====================

Principles we should adhere to:
 - Customer value is business value
 - Work in short cycles instead of trying to predict the future. Shorter cycles means lower investment, lower costs, lower risk
 - Evidence based decision making (MVPs, experiments). 1-What is the next most important thing we need to learn - where lies the highest risk of ignorance? That might be something technical or user related. 2- What is the least amount of work we need to do so that we learn that?
 - Retrospectives: improve the product, improve the process
 - Go and See. Find the amplify the good patterns that work. 
 - Test high-risk hypothesis
 - Do less, more often
 - Work as a balanced team. Small, dedicated, co-located, cross-functional, autonomous, empowered 
 - Transparency: what do we work, why, how are we doing, what success looks like. It can come up with rituals like stand-ups, and demos. Access to data, from the company side
 - Bring learning part of the backlog

The technical core 

Example of the time - money - scope (- quality) triangle (pyramid)
Why it does not work like that in software engineering
How the price mechanism works to get things done
Agile is bringing engineering to the core of decision and organisation rather than using financial accounting.
How it works in practice: for this functionality it will take so much time
Saving on the key engineering practices that all developer should know and strive for (e.g, continuous integration ) will actually do much more harm than anything else.


Create the vision
Set up a road-map
Build a team, if not already in place, or modify existing one
Collect user stories (while the stories are being developed, keep adding new ones and elaborate the existing ones )
From enough user stories, figure out the following:
    all the non functional requirements that are implied rather than explicitly stated in the stories
    the suitable architecture, as a rough sketch
    the coding standards, and everything else the determines the project, like language, frameworks, etc
    the test plan with:
        the user acceptance tests from the user stories
        the integration tests that should follow the architecture and fit at the seems of the modules
        the unit tests at the lowest level possible
        the performance tests
Start out with an architectural spike and place all the 'modules' in place
work with the Red-Green-Refactor cycle
    write some failing tests, according to the testing plan
    write the code to make the tests pass, trying to follow the principles like DRY, SOLID, etc
    refactor the code: detect code smells and try to rectify them using the specific patterns available
    refactor the architecture: whenever needed modify the architecture
use the definition of DONE ta make sure that each story is up the selected standards, like with documentation written 
use the ci/cd pipeline to integrate and deploy the code
collect feedback from the users using metrics and other techniques
periodically, inspect and adapt, both the processes and the direction of the project

