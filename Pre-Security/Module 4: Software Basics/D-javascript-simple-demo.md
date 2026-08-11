# D. JavaScript: Simple Demo

JavaScript is used in most of the web pages that we visit on a day-to-day basis. Consequently, when we think of JavaScript engines, web browsers come to mind.

In fact, JavaScript was initially developed to run on client machines, in particular, within a web browser. However, this has changed with the release of **Node.js**, which enables developers to build web applications with JavaScript.

Consequently, as Node.js spread, JavaScript was no longer just a client-side programming language but also a server-side one.

JavaScript files can be executed in various ways:

- One way is to use your web browser.
- Another way is to use Node.js.
- Node.js makes it easy to download JavaScript files and run them from the command line.

---

## Notes

- `let` is used to declare variables whose value can change throughout the program. However, we use `const` to declare a constant.

- `Math.random()` gives a random decimal number between `0` and `1`.

- `Math.floor()` removes the decimal part by rounding down.

- `console.log()` can be used to display output on the screen.

- `parseInt()` takes user input and converts it from text into an integer value.

---

## Build a "Guess the Number" Game

### Plan

- The computer picks a secret number.
- The player keeps guessing until they find it.
- The computer tells the player whether the guess is too low or too high.

---

## The Code

```javascript
import * as readline from "node:readline/promises";
import { stdin as input, stdout as output } from "node:process";

const MIN_NUMBER = 1;
const MAX_NUMBER = 20;

const rl = readline.createInterface({ input, output });

try {
    const secret =
        Math.floor(
            Math.random() * (MAX_NUMBER - MIN_NUMBER + 1)
        ) + MIN_NUMBER;

    // MIN_NUMBER <= secret <= MAX_NUMBER

    let tries = 0;
    let guess = 0;

    // Start with a value that cannot be the secret.
    // Since secret is between 1 and 20, 0 cannot be the secret.

    console.log(
        "I'm thinking of a number between",
        MIN_NUMBER,
        "and",
        MAX_NUMBER
    );

    // Repeat until the user guesses the secret number.
    while (guess !== secret) {
        const text = await rl.question("Take a guess: ");

        // If the user didn't type digits, avoid crashing and ask again.
        if (!/^\d+$/.test(text)) {
            // True only if all characters are digits.
            console.log("Please type a whole number.");
        } else {
            guess = parseInt(text, 10);

            // Convert the text to a number.
            tries = tries + 1;

            // Give a hint using if / else if / else.
            if (guess < MIN_NUMBER || guess > MAX_NUMBER) {
                console.log("That number is out of range. Try again.");
            } else if (guess < secret) {
                console.log("Too low, try again.");
            } else if (guess > secret) {
                console.log("Too high, try again.");
            } else {
                console.log("You got it in", tries, "tries!");
            }
        }
    }
} finally {
    rl.close();
}
```

### Key Concepts Used

- `const` → declares a variable whose value cannot be reassigned.
- `let` → declares a variable whose value can change.
- `Math.random()` → generates a random decimal between `0` and `1`.
- `Math.floor()` → rounds a number down to the nearest integer.
- `console.log()` → displays output on the screen.
- `parseInt()` → converts text into an integer.
- `await rl.question()` → gets input from the user.
- `while` → repeatedly executes code while a condition is true.
- `if / else if / else` → performs different actions depending on conditions.
- `!==` → checks whether two values are not equal.
- `||` → represents the logical OR operator.
- `/^\d+$/` → checks whether the input contains only digits.
