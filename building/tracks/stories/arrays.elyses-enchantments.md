# Elyse's Enchantments

## Story

As a magician-to-be, Elyse needs to practice some basics. She has a stack of cards that she wants to manipulate.

To make things a bit easier she only uses the cards 1 to 10.

> <!-- not part of the story -->
>
> We limit the card values from 1 to 10, as to only have to deal with numbers,
> so that exercises that use this story only need to rely on numbers.

## Tasks

These are examples of tasks that fit the story of Elyse being a beginner:

- Retrieve a card from a stack
- Exchange a card in the stack
- Insert a card at the of top the stack
- Remove a card from the stack
- Remove the top card from the stack
- Insert a card at the bottom of the stack
- Remove a card from the bottom of the stack
- Check the size of the stack

This story can be continued to also teach array analysis:

- Find the position of a card
- Determine if a card is present
- Determine if each card is even
- Check if the stack contains an odd-value card
- Get the first odd card from the stack
- Determine the position of the first card that is even

This story can be continued to also teach array transformations:

- Double every single card
- Create multiple copies of every 3 found in the deck
- Find two cards from the exact middle of the deck
- The outside two cards will reappear in the middle of the deck
- Every card that isn't 2 disappears
- Convert a shuffled deck into a perfectly ordered deck
- Change every card to the total number of cards

This story can be continued to also teach array destructuring:

- Get the first card (without conventional methods, e.g indexer or methods)
- Get the second card (without conventional methods, e.g indexer or methods)
- Swap the first two cards (without conventional methods, e.g indexer or methods)
- Discard the top card (without conventional methods, e.g indexer or methods)
- Insert face cards (without conventional methods, e.g indexer or methods)

## Terminology

These are recommendations, not rules, for recurring terminology in the instructions (including stub commentary)

- The main character is **Elyse** and her pronouns are **she/her**. If you need to indicate the character, use the name or refer to her by her pronoun(s).
- Instead of `array` (or equivalent data type), use the word **stack** or **card stack**
- Instead of `element`, use the word **card**
- Instead of `length`, use **size of the stack**
- The **top card** is the _first element_
- The **bottom card** is the _last element_

## Implementations

- [JavaScript: elyses-enchantments][implementation-javascript] (reference implementation)
- [JavaScript: elyses-analytic-enchantments][implementation-javascript-2] (reference implementation)
- [JavaScript: elyses-destructured-enchantments][implementation-javascript-3] (reference implementation)
- [JavaScript: elyses-transformative-enchantments][implementation-javascript-4] (reference implementation)
- [Swift: arrays][implementation-swift]

## Alternative version

An alternative version of the story uses **you** (the student) as the actor and focuses on re-arranging the deck only.

### Story

You're a magician and you handle a deck of cards. In order to correctly execute your magic trick, you need to be able to move a card from one position to another position. That is, you need to be able to rearrange the deck. Naturally, you want to be able to move cards in both directions and be able to say "from the top of the deck" or "from the bottom of the deck".

### Tasks

These are examples of tasks that fit the story of you wanting to re-arrange cards:

- Implement a function arrange that moves a card in a stack from one given position to another, returning a new stack
- Implement a function rearrange that does the same, mutating the original stack

### Implementations

- [JavaScript 1-a (research)][implementation-javascript-research-1-a]
- [JavaScript 2-a (research)][implementation-javascript-research-2-a]

## Reference

- [`types/array`][types-array]

[types-array]: https://github.com/exercism/v3/blob/main/reference/types/array.md
[implementation-javascript]: https://github.com/exercism/javascript/blob/main/exercises/concept/elyses-enchantments/.docs/instructions.md
[implementation-javascript-2]: https://github.com/exercism/javascript/blob/main/exercises/concept/elyses-analytic-enchantments/.docs/instructions.md
[implementation-javascript-3]: https://github.com/exercism/javascript/blob/main/exercises/concept/elyses-destructured-enchantments/.docs/instructions.md
[implementation-javascript-4]: https://github.com/exercism/javascript/blob/main/exercises/concept/elyses-transformative-enchantments/.docs/instructions.md
[implementation-javascript-research-1-a]: https://github.com/exercism/research_experiment_1/tree/master/exercises/javascript-1-a
[implementation-javascript-research-2-a]: https://github.com/exercism/research_experiment_1/tree/master/exercises/javascript-2-a
[implementation-swift]: https://github.com/exercism/swift/blob/main/exercises/concept/magician-in-training/.docs/instructions.md
