# C. Python: Simple Demo

Python is a **high-level, general-purpose programming language**.

## What does this mean?

- **High-level:** It hides most implementation details.
- **General-purpose:** It can be used for a wide variety of scenarios, from:
  - Web applications
  - Automation scripts
  - Data science
  - Machine learning

---

## Build a "Guess the Number" Game

### Plan

- The computer secretly picks a number between `1` and `20`.
- The user keeps guessing until they get it right.
- The computer tells the user whether their guess is **too low** or **too high**.

### Random Numbers

Python provides the `random.randint()` method, which returns a random integer within the specified bounds.

Example:

```python
random.randint(1, 20)
```

This returns a random number between `1` and `20`.

> **Note:** In programming, loops or iterations allow us to execute the same lines of code multiple times.

---

## The Code

```python
import random

MIN_NUMBER = 1
MAX_NUMBER = 20

secret = random.randint(MIN_NUMBER, MAX_NUMBER) # 1 <= secret <= 20

tries = 0
guess = 0 # Start with a value that cannot be the secret

print("I'm thinking of a number between", MIN_NUMBER, "and", MAX_NUMBER)

# Repeat until the user guesses the secret number

while guess != secret:

    text = input("Take a guess: ")
    if not text.isdigit():   # If the user didn't type digits, avoid crashing and ask again
        print("Please type a whole number.")
    else:
        guess = int(text)
        tries = tries + 1  # increases the number of attempts by 1

        # Give a hint using if/elif/else
        if guess < MIN_NUMBER or guess > MAX_NUMBER:
            print("That number is out of range. Try again.")
        elif guess < secret:
            print("Too low, try again.")
        elif guess > secret:
            print("Too high, try again.")
        else:
            print("You got it in", tries, "tries!")
```

### Key Concepts Used

- `import random` → imports Python's random-number tools.
- `random.randint()` → generates a random integer within a specified range.
- `input()` → gets text input from the user.
- `.isdigit()` → checks whether the input contains only digits.
- `int()` → converts text into an integer.
- `while` → repeats a block of code while a condition is true.
- `if / elif / else` → makes decisions based on conditions.
