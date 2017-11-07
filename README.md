WIP

# Documentation-Driven-Development

## sales pitch
### Introduction
mixture of documentation, development, and testing. The process of developing code is often very abstract 
and dependent on the way a developer mentally breaks down a task. When a feature is submitted, it is up to the reviewer to
review/understand the architecture of the feature and then review the code for efficentcy. Sometimes, two developers dont agree 
on the archecture implementation where neither developer is incorrect, however rewriting archtecture takes time and may 
need another complete reivew of all code! 

This version DDD aims to solve the issue archetecture agreement by breaking a feature into multiplue logically different PRs: 
documentation, development, testing. This being said, this DDD is implemented through a PR, and is at will enforced.

### Documentation phase:
1) All files are created via 'File Creation'.
2) All classes and constructors are created.
3) All functions are created and return a default value.
4) All imports are defined.
5) Documentation behind functions are given, using inline annotations /** **/
6) All unit tests are witten and should pass.

#### Development phase:
1) Implement all the default functions.
2) Add unit tests as nessicary.
3) Tests should continue to pass.

#### Test phase:
1) Implement integration tests.

#### File Creation:
When a file is created it must state
1) Purpose - why is this file needed

### Benifits
1) There is no waste with this implementation, the documentation is inline with the code and all abstract code will be implemented; 
and at the end a living document will be produced.
2) Architecture is reviewed through a documentation PR before any implementation, which saves time and gets any dissagreements out of the way.
3) Breaks a feature down further into phases, showing progress.
4) The development phase is transparent, because we are just implementing prototypes.

### Disadvantage
1) multipule PR's and reviews

## Implementation Flow Example
1) Plan
2) Branch master. Give this branch name <ticket#>-<ticket name> ex: 123-new-feature
3) Branch newly created branch into a documentation branch. ex: 123-new-feature-doc
4) Follow Documentation Phase (above).
5) Submit PR, reviewer focuses on architecture integration with existing code,
suggests changing architecture that would result in reusible logical grouped modules, or 
suggests reusing existing modules.
6) After approved, merge into the main feature branch. That would be back into '123-new-feature'
7) Branch the main feature branch (123-new-feature) appending 'dev' to the branch name. ex '123-new-feature-dev'
8) Follow Development Phase (above).
9) Submit a PR, reviewer focuses on coding efficentcy and size.
10) After approved, merge into the main feature branch. That would be back into '123-new-feature'
11) Branch the main feature branch (123-new-feature) appending 'test' to the branch name. ex '123-new-feature-test' 
12) Write integration tests and submit them for approval
.... follow your own flow

## Case Study
TODO
