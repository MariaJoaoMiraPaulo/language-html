# Assignment 4

<a name="index"/>
## Index
1. [Introduction](#introduction)
2. [Degree of Testability](#testability)
  1. [Controllability](#controllability)
  2. [Observability](#observability)
  3. [Isolateability](#isolateability)
  4. [Separation of concerns](#separation-of-concerns)
  5. [Understandability](#understandability)
  6. [Heterogeneity](#heterogeneity)
3. [Test Statistics and analytics](#test-statistics)

<a name="introduction"/>
## Introduction

<a name="testability"/>
##Degree of Testability

<a name="controllability"/>
###Controllability
Atom contains a directory to test the application software, that directory is call specs. Atom uses [Jasmine](https://jasmine.github.io/1.3/introduction.html) as its spec framework. Jasmine is a behavior-driven development framework for testing javascript code. Its super easy to set up tests. Just create a file, where the filename has the component to test plus a "-spec" on the end, and there set up the tests of that component. If we analyze specs directory, on atom source code, we can see more than 50 files of tests created, the filename says which component is tested. This proves that the components under test ( CUT ) only depend on them. Even AtomEnvironment, the component that most relates to others has their own tests.

<a name="observability"/>
###Observability

<a name="isolateability"/>
###Isolateability

<a name="separation-of-concerns"/>
###Separation of concerns
Atom has a concrete and distinct project organization/division. Separation of Concerns is responsible for divide an application into distinct features with as little overlap in functionality as possible. The important factor is minimization of interaction points to achieve high cohesion.
Concerns are the different aspects of software functionality. The separation of concerns is keeping the code for each of these concerns separate.
For Example, in Atom, changing the interface don’t require changing the logic code, and vice versa.

<a name="understandability"/>
###Understandability

<a name="heterogeneity"/>
###Heterogeneity

<a name="test-statistics"/>
## Test Statistics and analytics
The statistics related to Atom's tests are available in the ReadMe of Atom. As explained before Atom uses Jasmine as its spec framework, and 3 online platforms (CircleCi, Travis Ci and AppVeyor) to perform the build and run its tests.

Atom tests run in 3 fases:
- First it runs a system and regression testing, executes core main process tests (console log show bellow):
```
  AtomApplication
    launch
      ✓ can open to a specific line number of a file (7091ms)
      ✓ can open to a specific line and column of a file (4158ms)
      ✓ removes all trailing whitespace and colons from the specified path (3628ms)
      ✓ positions new windows at an offset distance from the previous window (6579ms)
      ✓ reuses existing windows when opening paths, but not directories (7752ms)
      ✓ adds folders to existing windows when the --add option is used (4329ms)
      ✓ persists window state based on the project directories (5600ms)
      ✓ shows all directories in the tree view when multiple directory paths are passed to Atom (4244ms)
      ✓ reuses windows with no project paths to open directories (3474ms)
      ✓ opens a new window with a single untitled buffer when launched with no path, even if windows already exist (7460ms)
      ✓ does not open an empty editor when opened with no path if the core.openEmptyEditorOnStart config setting is false (4620ms)
      ✓ opens an empty text editor and loads its parent directory in the tree-view when launched with a new file path (3762ms)
      ✓ adds a remote directory to the project when launched with a remote directory (7256ms)
      ✓ reopens any previously opened windows when launched with no path (11798ms)
      ✓ does not reopen any previously opened windows when launched with no path and `core.restorePreviousWindowsOnStart` is false (9707ms)
      when closing the last window
        ✓ leaves the application open (3747ms)
    before quitting
      ✓ waits until all the windows have saved their state and then quits (7458ms)
  FileRecoveryService
    ✓ doesn't create a recovery file when the file that's being saved doesn't exist yet
    when no crash happens during a save
      ✓ creates a recovery file and deletes it after saving
      ✓ creates only one recovery file when many windows attempt to save the same file, deleting it when the last one finishes saving it
    when a crash happens during a save
      ✓ restores the created recovery file and deletes it
      ✓ restores the created recovery file when many windows attempt to save the same file and one of them crashes
      ✓ emits a warning when a file can't be recovered (52ms)
  23 passing (2m)
  ```

- Secondly it runs Unit testing, executes core render process tests:
  - [CircleCi](https://circleci.com/gh/atom/atom/2092#tests/containers/0) finished in 319.954 seconds 2027 tests, 7730 assertions, 0 failures, 0 skipped;
  - [AppVeyor](https://ci.appveyor.com/project/Atom/atom/build/job/2y4kak3pr4npq0cg) took 194.545 seconds to run 2013 tests, resulting in 7645 assertions and 0 failures;
- Executes benchmark tests;

Atoms design strategy for test running is black-box testing, meaning that it only cares about the software's behavior and not about what happens internally. Due to this, Atom doesn't perform mutation nor coverage tests.

## Contributions

  Maria João Mira Paulo : 25%;

  Nuno Ramos : 25%;

  Pedro Costa : 25%;

  Ricardo Neves : 25%;
