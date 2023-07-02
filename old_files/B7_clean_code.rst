===========
Clean Code
===========

What Clean Code is about:

- Definition
- Main sources
- Central ideas

Note that the ideals below pertain to design more than anything else. Still they have synergies with clean code as an overall concept.
Five things that matter in making the code easy to change:
1.Modularity
2.Cohesion
3.Separation of concerns
4.Abstraction / information hiding
5.Loose coupling



The secret for good design is simplicity. Your code has the following properties:
it works
it communicates clearly
there is no duplication
there are no extra pieces 



### Simple code

Python tools for measuring code metrics

https://radon.readthedocs.io/en/latest/index.html#
Radon is a Python tool which computes various code metrics. Supported metrics are:

        raw metrics: SLOC, comment lines, blank lines, &c.
        Cyclomatic Complexity (i.e. McCabe’s Complexity)
        Halstead metrics (all of them)
        the Maintainability Index (a Visual Studio metric)


pytest-mccabe 2.0 (just the Cyclomatic complexity)
https://pypi.org/project/pytest-mccabe/
