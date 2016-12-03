# Assignment 4

<a name="index"/>
## Index
1. [Introduction](#introduction)
2. [Test Statistics and analytics](#test-statistics)
<a name="introduction"/>
## Introduction


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

Atoms design strategy for test running is black-box testing, meaning that it only cares about the software's behavior and not about what happens internally.

## Contributions

  Maria João Mira Paulo : 25%;

  Nuno Ramos : 25%;

  Pedro Costa : 25%;

  Ricardo Neves : 25%;
