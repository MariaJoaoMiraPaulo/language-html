# Assignment 4

<a name="index"/>
## Index
1. [Introduction](#introduction)
2. [Software Testability and Reviews](#testability)
  1. [Controllability](#controllability)
  2. [Observability](#observability)
3. [Test Statistics and analytics](#test-statistics)
<a name="introduction"/>
## Introduction

<a name="testability"/>
## Software Testability and Reviews

<a name="controllability"/>
### Controllability
Atom contains a directory to test the application software, that directory is call specs. Atom uses [Jasmine](https://jasmine.github.io/1.3/introduction.html) as its spec framework. Jasmine is a behavior-driven development framework for testing javascript code. Its super easy to set up tests. Just create a file, where the filename has the component to test plus a "-spec" on the end, and there set up the tests of that component. If we analyze specs directory we can see more than 50 files of tests created, the filename says which component is tested. This proves that the components under test ( CUT ) only depend on them. Even AtomEnvironment, the component that most relates to others has their own tests.

<a name="observability"/>
### Observability

<a name="test-statistics"/>
## Test Statistics and analytics
The statistics related to Atom's tests are available in the ReadMe of Atom. As explained before Atom uses Jasmine as its spec framework, and 3 online platforms (CircleCi, Travis Ci and AppVeyor) to perform the build and run its tests.

Atom tests run in 3 fases:
- Executes core main process tests:
  23 passing tests.
- Executes core render process tests:
  - [CircleCi](https://circleci.com/gh/atom/atom/2092#tests/containers/0) finished in 319.954 seconds 2027 tests, 7730 assertions, 0 failures, 0 skipped;
  - [AppVeyor](https://ci.appveyor.com/project/Atom/atom/build/job/2y4kak3pr4npq0cg) took 194.545 seconds to run 2013 tests, resulting in 7645 assertions and 0 failures;
- Executes benchmark tests;



## Contributions

  Maria João Mira Paulo : 25%;

  Nuno Ramos : 25%;

  Pedro Costa : 25%;

  Ricardo Neves : 25%;
