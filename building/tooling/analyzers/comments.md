# Writing Analyzer Comments

This document provides information and guidelines on how to write comments produced by the analyzer.

## Contents

The contents for analyzer comments are stored as a Markdown document in the [exercism/website-copy][git-website-copy] repo.
Comments contain a pointer-string, formatted as `<track-slug>.<exercise-slug>.<comment-slug>`, that links to a specific Markdown document in the `website-copy` repo.

For example, `ruby.two-fer.string-interpolation` refers to https://github.com/exercism/website-copy/blob/main/analyzer-comments/ruby/two-fer/string_interpolation.md.

```exercism/note
If a comment is language-specific and _not_ exercise-specific, replace `<exercise-slug>` with `general`.
E.g. `ruby.general.string-explicit_return`
```

## Wording

- Avoid unnecessarily wordy comments. Be concise.
- Be neutrally observational; avoiding charged statements and blanket statements.
- Make the recommendation explicit.
- When possible, put the recommendation first, then the explanation.
- Avoid "me", "I", "we", etc, since the bot is not a person.
- Avoid "you" and "your code", because it can sometimes come across as judging
  the person rather than the code.
- Avoid words like "just", "simply", and "obviously", which can come across as
  condescending: if the comment is necessary, it was _obviously_ not _obvious_.
- Avoid making assumptions about what people know and don't know. The only
  exception is knowledge from already completed _core_ exercises. Avoid
  "as you know", "as you remember", "as you learned", "now that we all
  understand x", because even though something was said, the person doesn't
  necessarily understand it.

## Guidance

- **Aim for fluency, not proficiency**: the goal of a language track on Exercism is to give people a way to achieve a high level of [fluency](/docs/using/product/fluency) at a low level of proficiency.
  We're aiming for fluency in the syntax, idioms, and the standard library of the language.
- **Suggest idiomatic code** when possible, where idiomatic is code that would be written by nearly all developers (non-hobbyists) who write code in that language.
  If a non-idiomatic suggestion is made, mention this and explain why the suggestion might still be useful.
- **Name the difference** between what the person is doing, and what is 'idiomatic' in the language.
- **Use the proper terms** and nomenclature, so people can recognize those concepts elsewhere, and also can research them by themselves.
- **Don't give the solution** as general advice for all Exercism mentoring.
  Learning sticks when people discover the answer for themselves. That's a tremendously exhilarating experience, and the emotional kick makes it memorable.
  However, if the discovery **doesn't** trigger a dopamine hit, it makes total sense to show what it looks like.
  For example, we might choose to provide a small improvement on an approved solution will be a lot less exciting than giving someone a learning point on a solution that is being disapproved and therefore may warrant an example rather than a link.
- **Order comments by importance**, the first comment being the most important, and the last comment being the least important.
- **Keep the number of comments manageable**.
  Aim for one to three comments per iteration.
- **Don't add the same comment twice** in one analysis.
  Adding the same comment with different parameters attached to it is _not_ considered a duplicate.
- **Consider only commenting on formatting** if formatting or linting is integral to the language.
  When possible, guide students towards tools for auto-formatting and/or link to any official style guide.

### First few exercises

For the first few exercises of a track, the following is _extra_ important:

- **Keep it relatively short**, avoiding a wall of text or overwhelming them
  with advice. If they have a great experience in the first exercise, they'll
  come back and you'll have many more opportunities to provide feedback on all
  of the things that you noticed.
- **Don't overly explain a concept**: don't go in-depth about the underlying
  mechanisms of compilers and things. In this case, it's more about this being
  one of the first exercises in the language track, and at this stage, feedback
  is more helpful if it's shorter and more directive.
- **Give a link** that shows exactly how to do the concept, in a **tutorial**
  kind of way. Meaning: showing how to do things, not discussing why. This might
  mean that the official docs of the language don't suffice, as these are often
  a code reference and don't show you how to use it and how it works. _However_,
  you should provide a link only for more in-depth exploration. The person
  should be able to understand what you mean from the answer directly, without
  following the link.

### Examples

In JavaScript, a student has written a top-level constant with `let`.

```markdown
<!-- not following these guidelines -->

As you know, everyone uses const, you shouldn't use let or var.
```

This comment does not follow these guidelines for the following reasons:

- The action comes after the "explanation".
- "As you know": we don't know if the student does.
- "you shouldn't": you don't need the "you" to make this statement.
- "everyone uses const": this isn't true _and_ can make the student feel as if
  they did something horribly wrong.
- Lacks an actual explanation of _why_ the advice is given.

```markdown
<!-- better -->

Prefer `const` and `let` over `var`. The `const` declaration stops a variable
from being accidentally reassigned, which provides safety, and reduces
cognitive load for someone reading the code. [This article](https://medium.com/javascript-scene/javascript-es6-var-let-or-const-ba58b8dcde75)
explains the difference between the three.
```

In Go, a student has created a custom error instead of using the built-in ones:

```markdown
<!-- not following these guidelines -->

I see you are creating a custom `error`. This is perfectly fine! If you did not
know about `errors.New` and `fmt.Errorf` have a look at them as they are much
simpler ways to create an error. Custom errors are helpful if you want to check
if an error is of a certain type later.
```

This comment does not follow these guidelines for the following reasons:

- "I see": the analyzer is not a person: avoid I.
- "This is perfectly fine!": Apparently, it's not otherwise the reassuring wasn't
  necessary. This probably can be left out altogether; if you want to give a
  generic tip about something existing, you can say exactly that: "An
  alternative, equally valid way of doing x is y."
- "If you did not know about": Leave this overly wordy word group out.

```markdown
<!-- better -->

A custom `error` is typically used to provide custom behavior, or to distinguish
on type later. For simpler cases, it's more common to rely on `errors.New` or
`fmt.Errorf`. This [in-depth article](https://golangbot.com/custom-errors/) about
custom errors might be interesting.
```

## CI

Because the comments don't live in the same repository as the analyzer, each
analyzer should have CI that checks if the comments used in that specific
analyzer (those that can become output), are comments on the `main` branch, on
the [`exercism/website-copy`][git-website-copy] repository.

At the moment of writing, [this issue][issue-ci-comments] tracks the status of any
generalization of this CI, if any.

[git-website-copy]: https://github.com/exercism/website-copy/tree/main/analyzer-comments
[issue-ci-comments]: https://github.com/exercism/automated-mentoring-support/issues/51
[git-website-copy-label]: https://github.com/exercism/website-copy/pulls?q=is%3Aopen+is%3Apr+label%3Atype%2Fanalyzer-comments
