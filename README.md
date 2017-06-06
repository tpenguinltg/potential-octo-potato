# potential-octo-potato
What would happen if we let developers decide?

This project, named "potential-octo-potato" because that is what GitHub suggested, has no stated goals. You will decide what direction this project will take, choosing what it will do, what language to use, how the code will be formatted, the branching strategy, even right down to the license! Think of it like [/r/place](https://www.reddit.com/r/place/) but for GitHub. Make full use of issues and the wiki.

So what are you waiting for? Read the rules and send in a pull request today!

## Rules

You may only have at most one pull request active at a time (excluding pull requests for portions of the README above the horizontal line).

Pull requests should consist of only a single commit containing a minimal change. A minimal change ideally does not change more than one line, including comments, possibly excluding blank lines for readability. For changes to the README (make them below the horizontal line), try to keep changes to one "unit of thought", which is often one sentence. Changes to the README above the horizontal line are exempt and can be as large as necessary. The definition of a "minimal change" is under the discretion of the project maintainers and they have the right to reject non-conforming pull requests.

Unless the community decides on further restrictions, all pull requests that conform to the above format will be merged. Multiple pull requests that are ready for merging will be merged in ascending order of their IDs.

A change should not break the build, so you will have to think about how to introduce your feature using only minimal changes while still being able to run the project.

### Minimal Change

Although the definition is somewhat vague, the following sections will attempt to outline the general idea of a "minimal change". These examples are in JavaScript, but the concept should apply to any language and these examples should be updated when the language for the project has been decided.

#### Control structures

Control structures with conditions should be introduced with an empty body and `false` as the condition. Changing a simple statement to a compound statement, even if empty, counts as a minimal change. As an arbitrary example, here's a possible evolution of an `if` statement in 7 steps:

```javascript
if (false);

if (false) {}

if (false) {
  x;
}

if (false) {
  x += 2;
}

if (false) {
  x += 2;
  y;
}

if (false) {
  x += 2;
  y -= 3;
}

if (x < 5) {
  x += 2;
  y -= 3;
}
```

Introduce `if` statements like this: `if (false);`.

`while` loops should be introduced similarly: `while (false);`.

`for` loops should have empty initializors and post-conditions: `for (;false;);`

### Variables

Variables should be introduced as simply as possible. This means introducing just a declaration without initialization if the language supports it. Otherwise, variables should be initialized with the default value. In Javascript, this means initializing the variable `x` to `3` is the following is three steps:

```javascript
var x;

var x = 0;

var x = 3;
```

#### Strings

Strings should be empty when inserted where possible. Strings should be populated one unit of thought at a time after insertion.

### Comments

A comment introduced should only be roughly one unit of thought, which is often one sentence. Avoid building code in comments.

### Files

Files should be created empty whenever possible.

(Project README should go below this line)
* * *
