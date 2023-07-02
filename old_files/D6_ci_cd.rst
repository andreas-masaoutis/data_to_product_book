=========================
The CI/CD toolset
=========================

Implementing a CI/CD pipeline:

- Version Control (git)
On git branching: each branching strategy is suitable for a specific context. For example, working with feature branches makes sense for open source projects where people are not fully on project so while they might work on something other should be able to move ahead. In projects with a dedicated full-time team, given the presence of an automated testing suite, maybe it does not make sense.
Context always matters.

Patterns for Managing Source Code Branches https://martinfowler.com/articles/branching-patterns.html


- Jenkins(?)
- Docker
- Heroku
- Etc
- Dora (or any other) Metrics https://dev.to/linearb/how-to-use-dora-engineering-metrics-to-improve-your-dev-team-1hkc
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
