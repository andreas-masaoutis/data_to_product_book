

************************
Develop
************************


Daily stand-up meeting
==============================

MVP (Spike) (Walking Skeleton)
==============================

Red-Green-Refactor
==============================

Code smells
==============================

Refactoring recipes
==============================

SOLID principles
==============================

Pair/Mob coding
==============================

Rotating Pairs
==============================

Test Automation
==============================

CI/CD pipeline
==============================


Implementing a CI/CD pipeline:

- Version Control (git):

    On git branching: each branching strategy is suitable for a specific context. For example, working with feature branches makes sense for open source projects where people are not fully on project so while they might work on something other should be able to move ahead. In projects with a dedicated full-time team, given the presence of an automated testing suite, maybe it does not make sense.

Context always matters.

Patterns for Managing Source Code Branches https://martinfowler.com/articles/branching-patterns.html


- Jenkins(?)
- Docker
- Heroku
- Etc
- Dora (or any other) Metrics https://dev.to/linearb/how-to-use-dora-engineering-metrics-to-improve-your-dev-team-1hkc:
    As Goodhart's Law states, “When a measure becomes a target, it ceases to be a good measure.” Metrics can be gamed. Simple example of paying bonuses for bugs found, creates incentive to create bugs.

Deployment Frequency
Deployment Frequency measures the number of times that code is deployed into production. It’s usually reported in “Deployments Per Day”.
Mean Lead Time for Changes
Mean Lead Time for Changes is the average time it takes from code being committed to that code being released into production.
Some organizations begin tracking the time from the first commit of the project’s code, while others measure it beginning from merging the code to the main branch.
Mean Time to Recovery (MTTR)
This metric measures the average time it takes the team to recover from a failure in the system.
“Failure” can mean anything from a bug in production to the production system going down.
Change Failure Rate
Change Failure Rate measures how often a code change results in a failure in production. Changes that result in a rollback, in production failing, or in production having a bug all contribute to this metric.

The first two metrics — Deployment Frequency and Mean Lead Time for Changes — measure the velocity of a team. MTTR and Change Failure rate are a measure of the quality and stability of a project. All four metrics can be derived from mining the tools that you are currently using.

When the purpose for metrics is misunderstood, serious issues can occur. We are increasingly seeing DORA metrics used as goals, complete with OKRs (objectives and key results) where the objective is “improve DORA metrics.” But improving metrics should never be your goal.
Related to this is the idea of using DORA metrics to compare delivery performance between teams. Every team has its own context. The product is different with different delivery environments and different problem spaces.
Another common problem is the growth of “vanity radiators,” metric dashboards that display numbers but give no obvious clue about what action to take. “We deployed 436 times!” OK, but how big is the organization? Was that 436 times in a week, a day, or a year? Is that number improving or degrading? 



Branching Strategy
==============================

Semantic Commits
==============================

## On git message formatting

A well-crafted Git commit message is the best way to communicate context about an individual code change to fellow developers (and indeed to their future selves). A diff will tell you what changed, but only the commit message can properly tell you why. Overall, a clean and well formatted commit history can help someone understand what happened, and why it happened that way, years ago. Since a project’s long-term success rests (among other things) on its maintainability, it would be a waste for a developer not to use one of the more powerful tools: the project’s log.

As with many written forms of communication, we can break our suggestions down to three aspects:
- Style. Markup syntax, capitalization, punctuation, etc. The point is to create a consistent log that will be easy to read.
- Content. What kind of information should the body of the commit message (if any) contain? What should it not contain?
- Metadata. How should issue tracking IDs, pull request numbers, etc. be referenced?

### Style
With respect to style, these are some initial suggestions:
- Use a concise subject message less than 50 characters (the usual convention)
- Utilise the body to explain what and why vs how
- Be consistent with formatting like capitalisation, punctuation, etc

### Content
With respect content, the idea of `Semantic Commit Messages` is quite useful.

    Semantic Commits are commit messages with human and machine readable meaning, which follow particular conventions

In more detail:
- The commit messages are semantic - because these are categorized into meaningful types, indicating the essence of the commit
- The commit messages are conventional - because these are formatted by a consistent structure and well-known types, both for developers and tools


The Conventional Commits specification is a lightweight convention on top of commit messages. It provides an easy set of rules for creating an explicit commit history; which makes it easier to write automated tools on top of.

It features a specific structure 

    <type>[optional scope]: <description>

    [optional body]

    [optional footer(s)]


An example


    fix(client-logo): correct capitalisation in file path

    The client logo would not show up in the deployed version, 
    although it worked locally. The actual filename and the 
    path provided had different capitalisation. The local
    Windows env read it just fine, while the Linux 
    deployment env did not read the file

    closes issue #543

And here is another one

    fix: fix foo to enable bar

    This fixes the broken behaviour of the component by doing xyz. 

    BREAKING CHANGE
    Before this fix foo wasn't enabled at all, behaviour changes from <old> to <new>

    Closes D2IQ-12345


Let us take a closer look

First we start with the list of commit types. Feel free to create the types that suite your project:

- **feat** : a new feature is introduced with the changes
- **data** : any change related to data - preparation, exploration, etc
- **fix** : a bug fix has occurred
- **chore** : changes that do not relate to a fix or feature and don't modify src or test files (for - example updating dependencies)
- **refactor** : refactored code that neither fixes a bug nor adds a feature
- **docs** : updates to documentation such as a README or other markdown files
- **style** : changes that do not affect the meaning of the code, likely related to code formatting such as white-space, line length, and so on.
- **test** : including new or correcting previous tests
- **perf** : performance improvements
- **deploy** : deployment / continuous-integration related
- **revert** : reverts a previous commit 

The types may be followed by the scope of the commit, a noun that describes the relevant section of the codebase - for example a feature tied up to a specific section of the project.

Then, there is the short description of the changes - it's like a header to the body that, optionally, follows next. In the body one has the opportunity to explain WHAT the change is, but especially WHY the change was needed.

In the end, the optional footer mention consequences which stems from the change - such as announcing a breaking change, linking closed issues, mentioning contributors and so on.


### Metadata
As we saw, the footer is the place for useful metadata like issues referenced, PullRequests, etc. Depending on the way the project works, one should establish consistent rules for referencing the relevant project management artifacts, like reported bugs, PullRequests, etc. With consistent rules metadata referencing rules the Git log history can be easily connected to the rest of the project like for example which are the corresponding commits for a certain user story.



Ideas adopted from:
- [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0-beta.4/)
- [Semantic Commit Messages](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716)
- [How to Write a Git Commit Message](https://cbea.ms/git-commit/)
- [How to write better git commit messages](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)


Metrics (Lead-time, etc)
==============================

Software Security
==============================

Different kinds of testing
==============================

Exploratory/Innovation days
==============================

Code quality
==============================

Code review
==============================

As per wikipedia:
    Code review (sometimes referred to as peer review) is a software quality assurance activity in which one or several people check a program mainly by viewing and reading parts of its source code, and they do so after implementation or as an interruption of implementation. At least one of the persons must not be the code's author. The persons performing the checking, excluding the author, are called "reviewers".


It is common that the review takes place before merging branches, or deploying code to production. The feedback is usually given by colleagues, either other developers, a manager, or a tech lead. One of the most familiar forms of code review is the Github pull request, in which developers leave comments on specific lines of code and, ultimately, approve or reject the proposed changes.


Companies that perform code reviews, spend the extra effort for the following benefits, as reviews help with:
    - finding defects while the code is in development. Not only outright bugs - which mostly are being caught by tests, but also issues with the overall code quality, the architecture, etc. A stitch in time, saves nine...
    - transferring knowledge between the participants, which helps individual developers learn new skills and improve.
    - breaking down possible barriers and create common ownership of the code base for the whole team.


A usual way to perform a code review is with a pull request - when a developer finishes the task being developed, asks a designated team member or the lead developer to merge the changes into the code base. Then either other developers, asynchronously, leave comments on specific lines of code and, ultimately, approve or reject the proposed changes, or do the same synchronously with all the participants present.

Assuming that the code has been developed as a task which is part of a story then there should be the definition of what Done actually means. This definition provides the basis for a list of points to consider when performing the review - passing the various tests, being documented, conforming to the agreed coding standards, etc. 

In this way, the review is less subjective. If the participants are also attentive with language and communication, like not being offending in their comments, the whole review process can be fruitful and constructive for all participants.


Retrospective (Sprint review)
==============================

