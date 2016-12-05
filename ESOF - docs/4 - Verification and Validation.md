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
4. [Bug Report Solution](#bug-report)

<a name="introduction"/>
## Introduction
Software testing is a process of executing a program or application with the intent of finding software bugs or to validate and verify that the software does what we expect.

Firstly we are going to study how tests are made on atom and discuss how easy is to set up a test. Then we are going to present some test statistics and finally we are going to talk about a bug that we found on atom.

<a name="testability"/>
##Degree of Testability

<a name="controllability"/>
###Controllability
Atom contains a directory to test the application software, that directory is call specs. Atom uses [Jasmine](https://jasmine.github.io/1.3/introduction.html) as its spec framework. Jasmine is a behaviour-driven development framework for testing javascript code. Its super easy to set up tests. Just create a file, where the filename has the component to test plus a "-spec" on the end, and there set up the tests of that component. If we analyse specs directory, on atom source code, we can see more than 50 files of tests created, the filename says which component is tested. This proves that the components under test ( CUT ) only depend on them. Even AtomEnvironment, the component that most relates to others has their own tests.

<a name="observability"/>
###Observability
The tests in the specs directory can be tested:
  - locally - running via the command line, if a test failed we cannot see what was the reason to fail;
  - when doing a commit or a pull request - there is 3 websites ( travis ci, circleci and appveyor ) that automatically will test the code, they make different types of tests. After running the tests all the websites provide a detailed report, something that can be very helpful in case of failure to understand what went wrong.

So, we can conclude that the observability of the results of the tests are excellent, because it is easy to interpret and because of the detailed reports it is easy to understand the origin of possible failures.

<a name="isolateability"/>
###Isolateability
The isolateability of a concern it's a consequence of a good code organization and file separation. Since atom has positive aspects in the Separation of concerns module, it was expected to have good results in this module too.

Isolateability allows components to be tested in isolation. In a well-design system, a component has a single responsibility, and its interface with other components are simple and clear.

Atom contains a specific directory to test the application software, that directory is call specs. Atom also makes it possible to do single unit tests. For example to create a spec for Atom core it is necessary to add sample-spec.coffee to the spec directory.

<a name="separation-of-concerns"/>
###Separation of concerns
Atom has a concrete and distinct project organization/division. Separation of Concerns is responsible for divide an application into distinct features with as little overlap in functionality as possible. The important factor is minimization of interaction points to achieve high cohesion.

The separation of concerns is keeping the code for each of the concerns (aspects of software functionality) separate, which means that the component under test (CUT) has a single, well defined responsibility.

Since this project is well organized, the tests effectiveness is considerably big.

<a name="understandability"/>
###Understandability

Atom is a well structured repository because it is very well documented and has instructions for every step you need to take. It starts when you open the repository and you have an introduction about what you can do and how to do it as well as explaining what Atom is and its major specifications.
When looking at the repository itself it can seen right away that there is a big number of folders, all with identifying names so anyone can choose directly the main files of what they are looking for and then, after selecting a source file, it's possible to see that each function running on Atom has a description, documentation, before its definition. Also, on the opening of each folder, there is a description of the contents of the folder.
The proof of the easy understanding of this project is right on the number of contributors and external developers. Since it's easy, anyone willing to help can pass by the repository and implement its idea.

<a name="heterogeneity"/>
###Heterogeneity

The Atom project is probably one of the most heterogeneity projects because of its package system. It means it has a massive external content that helps to the complementation of the project and it can read various programming languages.
The main, Atom accepted packages, languages and build status are all in [here] (https://github.com/atom/atom/blob/master/docs/build-instructions/build-status.md).
In the shown page it is possible to see the list of the dependencies that Atom requires thus getting knowledge of its heterogeneity. As said before there is a vast list of the different languages that Atom can support which we highlight:

-C/C++

-JavaScript

-HTML

-CSS

-Python

In the library section we highlight the [TextBuffer] (https://github.com/atom/text-buffer) because it stores all the text written on Atom so the test can run headless.

And finally we highlight the only tool used by this project, [AtomDoc] (https://github.com/atom/atomdoc) because it has the parser with JavaScript / CoffeScript.

<a name="test-statistics"/>
## Test Statistics and analytics
The statistics related to Atom's tests are available in the ReadMe of Atom. As explained before Atom uses Jasmine as its spec framework, and 3 online platforms (CircleCi, Travis Ci and AppVeyor) to perform the build and run its tests.

Atom tests run in 3 phases:
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

Atoms design strategy for test running is black-box testing, meaning that it only cares about the software's behaviour and not about what happens internally. Due to this, Atom doesn't perform mutation nor coverage tests.

<a name="#bug-report"/>
## Bug Report Solution

In order to further enhance our experience with the testing of Atom, our group started to work in the issue #6082 which discusses how useful would be having a warning message before quitting because, sometimes when multiple buffers and multiple windows are opened, user wants to close current buffer in current window by pressing Ctrl+W. Unfortunately, they inadvertently pressed Ctrl+Q and everything disappears.
Atom's community manager opposed this warning message, he said:
>I philosophically disagree with quit confirmations because I believe that quit confirmations are solving a real problem with red tape. The real problem is "I don't want to lose data accidentally".

So we decide a different approach, we changed the keymap 'ctrl-q', to first save all documents and only after it would quit the program.
We did this by altering the following files:

![Image](https://raw.githubusercontent.com/MariaJoaoMiraPaulo/language-html/master/ESOF%20-%20docs/res/keymaps.png)

![Image](https://raw.githubusercontent.com/MariaJoaoMiraPaulo/language-html/master/ESOF%20-%20docs/res/safeQuit.png)

Since we coulnd't build Atom and therefore test the change in the default files we tested that our code worked in another way. Atom allows custom functions and keymaps to be loaded when Atom opens, so we added the above 'safeQuit' function to the init.coffee and the keymap to keymaps.cson, this files overide the default keymap, that allowed us to test that our keymap was working proprelly even though we couldn't build atom to test the default keymaps.

We submited a Pull Request with our solution. We're waiting for a response but for now it passed all the tests.

![Image](https://raw.githubusercontent.com/MariaJoaoMiraPaulo/language-html/master/ESOF%20-%20docs/res/PRtests.png)



## Contributions

  Maria João Mira Paulo : 25%;

  Nuno Ramos : 25%;

  Pedro Costa : 25%;

  Ricardo Neves : 25%;
