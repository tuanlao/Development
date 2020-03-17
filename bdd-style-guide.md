# BDD Style Guide

Behavior-Driven Development (BDD) is a practice in software development, which
defines behavioral specification of software to be developed, and implements the
specification as automated test cases, before starting to develop the software.

This guide defines how BDD should be carried my in our developments.

The following is high-level workflow in my BDD style:

Specification:

1.  Design classes and functions

1.  Create application skeletons of the classes and functions

1.  Describe behavioral specification in brief as JSDoc of the classes and
    functions in the application skeletons

1.  Create test skeletons for the classes and functions

1.  Implement tests for the test skeletons

Implementation:

1. Implement application for the application skeletons
1. Fix application until all tests passed
1. Refactor application to fix code quality issues
1. Repeat steps 2 and 3 until all code quality issues solved

## Classes / Functions Design

### Classes

- Name concrete classes as noun, abstract classes as adjective or noun

### Class Properties

- Name as noun
- Initialize all at construction
- Never mutate after construction (no setter)

### Class Methods, Functions

- Name as verb clause
- Always use arrow function (no `function`)
- Make pure as much as possible (return side-effect as function)

### Objects, Variables

- Name as noun

- Define as `const` as much as possible (limit scope minimal if `let` is used,
  no global `let`)

## Application Skeletons

- Define all globals: classes, class properties, class method signatures,
  function signatures, objects, constants

- Class method and function signature should contain only return with trivial
  value (`0`, `''`, `false`, `[]`, `{}`, `null`), or function returning
  trivial value

## Application Source Code Documentation (optional)

- Declare as JSDoc

- All `@param`, `@returns`, and `@throws` tags should be documented (use flow
  for types)

- Function body should be empty at this time (use JSDoc if you need to declare
  brief processing steps, instead of declaring them as inline comments in
  function body: note that, however, JSDoc should be on specification, but not
  implementation details)

## Test Skeletons

- Test skeleton file should be created per application skeleton file

- Test skeletons should be written in the following form:
  ```javascript
  // file specification
  // test target file path should be the same as from clause content of test target import
  // e.g. `import target from 'foo/bar'` => `describe('foo/bar', () => { ... })`
  describe('<test target file path'>), () => {
    // function specification
    // test target function name should not include anything other than its name
    describe('<test target function name>', () => {
      test('[<expected side-effect> and] return <expected value> [if <condition>]', () => {
        // test codes
      });
      test('[<expected side-effect> and] throw <expected error> [if <condition>]', () => {
        // test codes
      });
    });
    // dynamically computed global constant or property specification
    // test target constant/property name should not include anything other than its name
    describe('<test target constant/property name>' => {
      // nest `describe` as necessary for object
      test('set <expected value> [if <condition>]', () => {
        // test codes
      });
    });
    // global object specification
    // test target object name should not include anything other than its name
    describe('<test target object name>', () => {
      // dynamically computed property specification
      // function specification
    });
    // class specification
    // test target class name should not include anything other than its name
    describe('<test target class name>', () => {
      // dynamically computed property specification
      // function specification
    });
  });
  ```

## Test Implementation

- All tests should have `expect` to assert return, throw, and/or side-effect

- All classes/functions should be mocked other than declared in the target
  application skeleton file and third-party frameworks/libraries

- Avoid testing/mocking third-party frameworks/libraries

- Use mock library for third-party frameworks/libraries which requires
  external connection (e.g. mockgoose for mongoose)

- If mock library for third-party frameworks/libraries which requires external
  connection does not exist, define boundary class/function only contains the
  framework/library calls but no application business logic

- Boundary classes/functions and exceptional cases hard to setup (e.g. wrong
  system time) may be excluded from code coverage under strict review

- On bug fixes, test reproducing the bug and checking expected result should
  be implemented

## Application Implementation

- Make codes correct English clause/sentence

- Never use inline comments (code should be readable only by JSDoc and the
  code itself, code needs inline comment smells and should be refactored)

- If non-boundary code or case can be setup is not covered, back to
  application/test skeletons step to revise design

## Application Refactoring

- Refactoring should not change the specification

  - The documentation may be revised

  - Codes in a function may be broken into small sub functions as long as
    they can be covered by the original tests

- If needed to change the specification, back to the first step to revise
  design
