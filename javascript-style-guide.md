# JavaScript Style Guide

- Follow to [Prettier](https://prettier.io) + [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)

- Always use ES6 syntax

  - No `var`, `const`/`let` instead
  - No `function`, `=>` instead, unless required by framework

## Naming

- No words other than English
- No Hungarian notation
- Name functions as verb or verb phrase
- Name constants, variables, objects, classes, symbols as noun or noun phrase

## Modularization

- Files and directories should be considered as modules
- Independent codes should not be declared in the same file
- Top-level source modules should be considered as independent packages, i.e. `<source directory>/a` => `a` (build system should be configured to make this possible)

## Airbnb Styles without ESLint Rules

The following styles need to be checked **manually**:

### Types

- 1.1 [Primitives](https://github.com/airbnb/javascript#types--primitives)
- 1.2 [Complex](https://github.com/airbnb/javascript#types--complex)

### References

- 2.3 [Block Scope](https://github.com/airbnb/javascript#references--block-scope)

### Objects

- 3.2 [ES6 Computed Properties](https://github.com/airbnb/javascript#es6-computed-properties)
- 3.5 [Grouped Shorthand](https://github.com/airbnb/javascript#objects--grouped-shorthand)
- 3.8 [Rest Spread](https://github.com/airbnb/javascript#objects--rest-spread)

### Arrays

- 4.2 [Push](https://github.com/airbnb/javascript#arrays--push)
- 4.3 [ES6 Array Spreads](https://github.com/airbnb/javascript#es6-array-spreads)
- 4.4 [From Iterable](https://github.com/airbnb/javascript#arrays--from-iterable)
- 4.5 [From Array Like](https://github.com/airbnb/javascript#arrays--from-array-like)
- 4.6 [Mapping](https://github.com/airbnb/javascript#arrays--mapping)
- 4.8 [Bracket Newline](https://github.com/airbnb/javascript#arrays--bracket-newline)

### Destructuring

- 5.3 [Object over Array](https://github.com/airbnb/javascript#destructuring--object-over-array)

### Strings

- 6.2 [Line Length](https://github.com/airbnb/javascript#strings--line-length)

### Functions

- 7.4 [Note on Blocks](https://github.com/airbnb/javascript#functions--note-on-blocks)
- 7.5 [Arguments Shadow](https://github.com/airbnb/javascript#functions--arguments-shadow)
- 7.7 [ES6 Default Parameters](https://github.com/airbnb/javascript#es6-default-parameters)
- 7.8 [Default Side Effects](https://github.com/airbnb/javascript#functions--default-side-effects)
- 7.9 [Defaults Last](https://github.com/airbnb/javascript#functions--defaults-last)

### Arrow Functions

- 8.3 [Paren Wrap](https://github.com/airbnb/javascript#arrows--paren-wrap)

### Constructors

- <a name="constructors--use-class">**IMPORTANT**</a> - 9.1 [Use Class](https://github.com/airbnb/javascript#constructors--use-class)
- <a name="constructors--extends">**IMPORTANT**</a> - 9.2 [Use Extends](https://github.com/airbnb/javascript#constructors--extends)
- 9.3 [Chaining](https://github.com/airbnb/javascript#constructors--chaining)
- 9.4 [ToString](https://github.com/airbnb/javascript#constructors--tostring)

### Modules

- <a name="modules--use-them">**IMPORTANT**</a> - 10.1 [Use Them](https://github.com/airbnb/javascript#modules--use-them)
- <a name="modules--no-wildcard">**IMPORTANT**</a> - 10.2 [No Wildcard](https://github.com/airbnb/javascript#modules--no-wildcard)
- 10.3 [No Export from Import](https://github.com/airbnb/javascript#modules--no-export-from-import)

### Iterators and Generators

- 11.2 [Generators Nope](https://github.com/airbnb/javascript#generators--nope)

### Properties

- 12.2 [Bracket](https://github.com/airbnb/javascript#properties--bracket)

### Variables

- 13.3 [Const Let Group](https://github.com/airbnb/javascript#variables--const-let-group)
- 13.4 [Define Where Used](https://github.com/airbnb/javascript#variables--define-where-used)

### Hoisting

- 14.1 [About](https://github.com/airbnb/javascript#hoisting--about)
- 14.2 [Anon Expressions](https://github.com/airbnb/javascript#hoisting--anon-expressions)
- 14.3 [Named Expressions](https://github.com/airbnb/javascript#hoisting--named-expresions)
- 14.4 [Declarations](https://github.com/airbnb/javascript#hoisting--declarations)

### Comparison Operators & Equality

- 15.2 [If](https://github.com/airbnb/javascript#comparison--if)
- 15.3 [Shortcuts](https://github.com/airbnb/javascript#comparison--shortcuts)
- 15.4 [More Info](https://github.com/airbnb/javascript#comparison--moreinfo)

### Control Statements

- 17.1 [Control Statements](https://github.com/airbnb/javascript#control-statements)
- 17.2 [Value Selection](https://github.com/airbnb/javascript#control-statements--value-selection)

### Comments

- 18.1 [MultiLine](https://github.com/airbnb/javascript#comments--multiline)
- 18.2 [SingleLine](https://github.com/airbnb/javascript#comments--singleline)
- 18.4 [ActionItems](https://github.com/airbnb/javascript#comments--actionitems)
- 18.5 [FixMe](https://github.com/airbnb/javascript#comments--fixme)
- 18.6 [ToDo](https://github.com/airbnb/javascript#comments--todo)

### Whitespace

- 19.7 [After Blocks](https://github.com/airbnb/javascript#whitespace--after-blocks)

### Type Casting & Coercion

- 22.1 [Explicit](https://github.com/airbnb/javascript#coercion--explicit)
- 22.4 [Comment Deviations](https://github.com/airbnb/javascript#coercion--comment-deviations)
- 22.5 [Bitwise](https://github.com/airbnb/javascript#coercion--bitwise)

### Naming Conventions

- 23.5 [Self This](https://github.com/airbnb/javascript#naming--self-this)
- <a name="naming--filename-matches-export">**IMPORTANT**</a> - 23.6 [Filename Matches Export](https://github.com/airbnb/javascript#naming--filename-matches-export)
- <a name="naming--camelCase-default-export">**IMPORTANT**</a> - 23.7 [CamelCase Default Export](https://github.com/airbnb/javascript#naming--camelCase-default-export)
- <a name="naming--PascalCase-default-export">**IMPORTANT**</a> - 23.8 [PascalCase Singleton](https://github.com/airbnb/javascript#naming--PascalCase-singleton)
- <a name="naming--Acronyms-and-Initialisms">**IMPORTANT**</a> - 23.9 [Acronyms and Initialisms](https://github.com/airbnb/javascript#naming--Acronyms-and-Initialisms)
- <a name="naming--uppercase">**IMPORTANT**</a> - 23.10 [Uppercase](https://github.com/airbnb/javascript#naming--uppercase)

### Accessors

- 24.1 [Not Required](https://github.com/airbnb/javascript#accessors--not-required)
- <a name="accessors--no-getters-setters">**IMPORTANT**</a> - 24.2 [No Getters/Setters](https://github.com/airbnb/javascript#accessors--no-getters-setters)
- <a name="accessors--boolean-prefix">**IMPORTANT**</a> - 24.3 [Boolean Prefix](https://github.com/airbnb/javascript#accessors--boolean-prefix)
- <a name="accessors--consistent">**IMPORTANT**</a> - 24.4 [Consistent](https://github.com/airbnb/javascript#accessors--consistent)

### Events

- 25.1 [Hash](https://github.com/airbnb/javascript#events--hash)

### ECMAScript 6+ (ES 2015+) Styles

- <a name="tc39-proposals">**IMPORTANT**</a> - 28.2 [TC39 Proposals](https://github.com/airbnb/javascript#tc39-proposals)

### Testing

- 30.2 [For Real](https://github.com/airbnb/javascript#testing--for-real)

  - <a name="testing--pure-functions">**IMPORTANT**</a> - Strive to write
    many small pure functions, and minimize where mutations occur.

  - <a name="testing--regression-test">**IMPORTANT**</a> - Whenever you fix
    a bug, write a regression test. A bug fixed without a regression test is
    almost certainly going to break again in the future.
