# CodeBreaker

A simple command-line code-breaking game where your objective is to guess a randomly generated sequence of letters. After each guess, the game provides feedback to help you deduce the correct code.

## How to Play

When the game starts, a random letter combination (the **code**) is generated. Your goal is to discover the code by entering letter-only guesses. Letter case is ignored, so uppercase and lowercase inputs are treated the same.

After every guess, the game displays feedback that reveals how close your attempt was.

### Feedback Rules

The feedback consists of two parts:

* **Correctly positioned letters** are revealed in their exact locations, while unknown positions remain as underscores (`_`).
* **Correct letters in incorrect positions** are listed on the right side of the feedback. Each matching letter appears **only once**, even if it occurs multiple times in your guess or is already shown in the correct position. *(This behavior is disabled in Hardcore mode.)*

### Example

**Secret code**

```text
ccab
```

**Your guess**

```text
abcd
```

**Feedback**

```text
____  |  abc
```

This indicates that:

* No letters were guessed in the correct positions.
* The letters `a`, `b`, and `c` all exist somewhere in the code.

## Special Commands

During the game, you can enter the following commands:

| Command      | Description                       |
| ------------ | --------------------------------- |
| `hint!`      | Receive a (totally helpful) hint. |
| `i give up!` | Reveal the code and end the game. |

## Goal

Use the feedback from each guess to gradually narrow down the possibilities until you correctly identify the secret code.

Good luck!
