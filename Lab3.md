# Lab 3 — Conditionals and Loops

**Total: 100 pts**

---

## Part 1 - Before We Begin [10 pts]

### Entry Survey [7 pts]

Please complete the short entry survey before beginning the lab:

👉 [ENTRY SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVURDVQQVIwMjdVUVVXNEdGQkJQMURRN0VXSC4u)

---

### Prepare Your Environment [3 pts]

1. Go to the **COMI-2010** folder.
2. Open VS Code and open the folder (File > Open Folder ...)
3. Create a new folder inside COMI-2010 named exactly Lab3. You can do that using VS Code or the terminal.
4. Add the lab files/content to the Lab3 folder.

---

## Part 2 - Dive In Programming [60 PTS]

In this lab, I prepared the environment for you. Open the `lab3.html` file to start the programming exercises. There are five of them. After completing each one, take a screenshot of your code and output (one screenshot capturing both input and output). Save each screenshot with the name of the exercise, e.g., `exercise1.png`, to the `Lab3` folder. In this lab, you are only writing the code inside the input and using `console.log` to produce the output in the output log. You may also be required to use prompts to retrieve input from the user. Remember to press the `Save` button before proceeding to the next exercise. After completion of all the exercises, click `Download Submission` and save it to the `Lab3` folder.

[prompt()](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt)

---

### Exercise 1 - Triangle

#### Goal

Prompt the user for a triangle size and print a left-aligned triangle made of `*`.

#### Instructions

1. Prompt the user for a triangle size.
2. Validate the input:

   * Must be an **integer**.
   * Must be between **3 and 20** (inclusive).
3. If valid, use a loop to print rows from 1 to `size`.
4. Each row prints the correct number of `*` characters.

#### Requirements

* Use `prompt()` for input.
* Use `console.log()` for output.
* Minimum size: **3**
* Maximum size: **20**
* If input is:

  * **Non-integer** → print a message: must be an integer in range.
  * **Out of range** → print a message that includes min and max.

#### Examples:

* input: 3

```
*
**
***
```

* input 5

```
*
**
***
****
*****
```

---

### Exercise 2 - Prompt-driven Receipt

#### Goal

Collect receipt items via prompts and compute subtotal, tax, and total.

#### Instructions

1. Start `subtotal` at 0.
2. Repeatedly prompt for an item name:

   * If the item name is **blank**, stop.
3. For each item, prompt for the price.
4. Immediately print the item name and the price.
5. Add the price to `subtotal`.
6. After the loop ends, compute:

   * `tax = subtotal * 0.07`
   * `total = subtotal + tax`
7. Print subtotal, tax, and total.

#### Requirements

* Use `prompt()` for input and `console.log()` for output.
* Tax rate is **7%** for all items.
* Stop when the item name is an **empty string**.
* **No storage of item names** (don’t use arrays/objects to save all items).
* If the price is invalid (blank, text, NaN, etc.), treat it as **0**.
* Prices should not be negative (if negative, treat as **0**).
* Must use a loop to keep collecting items.

---

### Exercise 3 - Number Guessing Game

#### Goal

The program picks a random number, and the user keeps guessing until correct.

#### Instructions

1. Generate a random integer between **1 and 100**.
2. Create a counter for attempts.
3. Repeatedly:

   * Prompt the user to guess a number (1–100).
   * Validate the guess.
   * If the guess is too low → print “Too low.”
   * If the guess is too high → print “Too high.”
   * If correct → print a success message and the number of attempts, then stop.

> **Hint:**
>
> ```
> const target = Math.floor(Math.random() * 100) + 1;
> ```

> **Hint 2:** If you use `prompt()`, don’t rely on `console.log()` for “Too high / Too low” messages—**the browser may not show console/output updates until the prompts are finished**. Instead, **put feedback directly in the next `prompt()` message** (e.g., `"Too low. Guess again:"`).

#### Requirements

* Use `prompt()` and `console.log()`.
* The guess must be an **integer from 1 to 100**.
* If input is invalid, print an error message and re-prompt.
* Count only valid guesses as attempts (or state clearly if you count invalid too—pick one and be consistent).
* When correct, print:

  * the target number
  * attempts taken

#### Resources

* [Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)
* [Math.floor()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor)

---

### Exercise 4 - Input Validator

#### Goal

Keep prompting until the user enters a valid integer score, then print a letter grade.

#### Instructions

1. Prompt the user for an exam score.
2. Input is valid only if it is an **integer from 0 to 100**.
3. If invalid, print a clear error message and prompt again.
4. When valid, compute and print the letter grade:

   * 90–100: A
   * 80–89: B
   * 70–79: C
   * 60–69: D
   * 0–59: F

#### Requirements

* Use a loop that continues until valid input is entered.
* Use `prompt()` and `console.log()`.
* Must validate:

  * not blank
  * integer only
  * range 0–100 inclusive
* Must use `if / else if / else` for grade logic.

---

### Exercise 5 - FizzBuzz

#### Goal

Prompt for `N`, then print from 1 to N with FizzBuzz rules.

#### Instructions

1. Prompt the user for `N`.
2. Validate that `N` is an integer between **1 and 100**.
3. If invalid, print an error message and stop.
4. If valid, loop from 1 to N:

   * If the number is divisible by 3 → print `"Fizz"`
   * If divisible by 5 → print `"Buzz"`
   * If divisible by both 3 and 5 → print `"FizzBuzz"`
   * Otherwise, print the number

#### Requirements

* Use `prompt()` and `console.log()`.
* `N` must be an integer between 1 and 100.
* Use a loop to count from 1 to N.
* Use the modulo operator `%` to test divisibility.

---

## Part 3 - Reflection [8 PTS]

For exercises 1–4 from Part 2, create a short reflection in `reflection.txt` located in the `Lab3` folder.
Copy and paste below into `reflection.txt` and then fill it out.

```
Exercise 1
What is the best loop for this problem?:
Why?:

Exercise 2
What is the best loop for this problem?:
Why?:

Exercise 3
What is the best loop for this problem?:
Why?:

Exercise 4
What is the best loop for this problem?:
Why?: 
```

---

## Part 4 - Worksheet [12 PTS]

#### Instructions

1. Start with the **initial values** of `a`, `b`, and `i` before the loop runs.
2. The loop runs **while `i < 4`**.
3. For each iteration, update the variables **in this exact order**:

   1. `b = b + a`
   2. `a = a - 1`
   3. `i = i + 1`
4. After each iteration, record the **new values** of `a`, `b`, and `i` in the table.
5. Stop when the condition `i < 4` becomes false.

#### Code to trace

```js
let a = 4;
let b = 1;
let i = 0;

while (i < 4) {
  b = b + a;
  a = a - 1;
  i = i + 1;
}
```

#### Trace Table (fill in)

|         Iteration # | a (after) | b (after) | i (after) |
| ------------------: | --------: | --------: | --------: |
| Start (before loop) |         4 |         1 |         0 |
|                   1 |           |           |           |
|                   2 |           |           |           |
|                   3 |           |           |           |
|                   4 |           |           |           |
|                   5 |           |           |           |
|                   6 |           |           |           |
|                   7 |           |           |           |
|                   8 |           |           |           |

> You can create the same table using any tool of your choosing. Save it in the `Lab3` folder as a table.

> Allowed formats: **PDF/PNG** ONLY!

---

## Part 5 — Submission [10 pts]

### Zip Your Lab Folder [3 pts]

#### Mac

```bash
zip -r Lab3.zip Lab3
```

#### Windows (PowerShell inside VS Code)

```powershell
Compress-Archive -Path Lab3 -DestinationPath Lab3.zip
```

Upload the Lab3.zip file to Blackboard.

Your folder should include all the required screenshots, the JSON file, the worksheet (PDF/PNG ONLY), and `reflection.txt`.

---

### Exit Survey [7 pts]

Please complete the exit survey after finishing:

👉 [EXIT SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVUQkRUWFNLOVgzM1RWVTk0SEsxNzdKR05UNS4u)
