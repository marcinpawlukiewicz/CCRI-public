# Lab 4 — More Loop Practice 
**Total: 100 pts**

---

## Part 1 - Before We Begin [13 pts]

### Entry Survey [13 pts]

Please complete the short entry survey before beginning the lab:

👉 **[ENTRY SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVUQ1U0UTBCSVczTFFTTFhGSFBaTFBJTUFORi4u)**

---

### Prepare Your Environment 

1. Go to the **COMI-2010** folder.
2. Open VS Code and open the folder (**File > Open Folder...**).
3. Create a new folder inside COMI-2010 named exactly **Lab4**.
4. Add the lab files/content to the **Lab4** folder.

---

## Part 2 - Dive In Programming [77 pts]

In this lab, open `lab4.html` to start the programming exercises.
After completing **each** exercise:

* Take **one screenshot** that captures both your **code** and the **output** (alert and/or console).
* Save screenshots in your `Lab4` folder as: `exercise1.png`, `exercise2.png`, etc.
* Click **Save** before moving on.
* After finishing all exercises, click **Download Submission** and save the JSON file into `Lab4`.

### Rules for this lab

* Use [`prompt()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt) to get input from the user. 
* Use [`alert()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/alert) for exercises that require an alert output. 
* You may also use `console.log()` to help debug.
* For numeric input:

  * use [`Number.parseFloat(...)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/parseFloat) (decimals allowed). 
  * use [`Number.isNaN(...)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isNaN) to validate numeric input.
  * use [`Number.isInteger(...)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isInteger) to validate whether passed value is an integer.

---

### Exercise 1 — Largest of Two Integers [5 pts]

#### Goal

Prompt for **two integers** and display the **largest** one.

#### Requirements

* Use `prompt()` twice
* Validate: must be integers (no decimals)
* Output using `alert()`

---

### Exercise 2 — Sign of the Product (3 numbers) [5 pts]

#### Task

Write a JavaScript conditional statement to find the sign of the product of **three numbers** entered via `prompt()`.

Sample numbers: `3, -7, 2`
Output: `The sign is -`

#### Requirements

* Inputs come from prompts
* You must decide the sign **without multiplying into a huge number**

  * (hint: count how many negatives)
* Show result in an `alert()`

---

### Exercise 3 — Largest of Five Numbers [7 pts]

#### Task

Prompt for **five numbers** and find the **largest**.

Sample: `-5, -2, -6, 0, -1`
Output: `0`

#### Requirements

* Use prompts
* Use conditionals (`if / else if / else`)
* Output using `alert()`

---

### Exercise 4 — Happy Numbers (First 5) [10 pts]

#### Task

Print the **first 5 happy numbers** (starting from 1 upward).

Definition (summary):

* Replace a number by the **sum of squares of its digits**
* Repeat until it becomes **1** (happy) or loops forever (unhappy)

#### Constraints (to avoid infinite loops)

* For each candidate number, stop if either:

  * you reach `1`, OR
  * you have done **100 iterations**, OR
  * you detect a repeat sum (cycle)

#### Output

Use `console.log()` to print:

* each happy number found
* stop after printing 5 happy numbers

---

### Exercise 5 — GCD of Two Numbers [10 pts]

#### Definition

The **Greatest Common Divisor (GCD)** of two positive integers is the **largest integer that divides both** with no remainder.

#### Task

Prompt for two positive integers and compute the GCD.

#### Requirements

* Use a loop (Euclid’s algorithm recommended but not required) [LINK](https://www.khanacademy.org/computing/computer-science/cryptography/modarithmetic/a/the-euclidean-algorithm)
* Output with `alert()`

---

### Exercise 6 — Sum of Multiples of 3 and 5 under 1000 [10 pts]

#### Task

Compute the sum of all numbers **below 1000** that are multiples of **3 or 5**.

#### Requirements

* Use a loop
* Output with `alert()`

---

### Exercise 7 — 5x5 Grid [10 pts]

Print a 5x5 grid of `#` characters to the console:

```
#####
#####
#####
#####
#####
```

Requirements:

* Must use **two loops** (nested)
* Use `console.log()`

---

### Exercise 8 —  Multiplication Table [10 pts]

Prompt for an integer `N` (1–12). Print an `N x N` multiplication table.

Example for N=4:

```
1  2  3  4
2  4  6  8
3  6  9 12
4  8 12 16
```

Requirements:

* Nested loops
* Print rows as a single line (string building)

---

### Exercise 9 — Harder Nested Loops: Hollow Rectangle [10 pts]

Prompt for:

* width (integer 4–30)
* height (integer 4–30)

Print a hollow rectangle of `*` to the console.

Example width=8 height=5:

```
********
*      *
*      *
*      *
********
```

Requirements:

* Nested loops
* Only borders are `*`, inside is spaces
* Validate width/height ranges

---

## Part 3 — Submission [10 pts]

### Zip Your Lab Folder [3 pts]

#### Mac

```bash
zip -r Lab4.zip Lab4
```

#### Windows (PowerShell inside VS Code)

```powershell
Compress-Archive -Path Lab4 -DestinationPath Lab4.zip
```

Upload **Lab4.zip** to Blackboard.

Your folder must include:

* screenshots `exercise1.png` ... `exercise10.png`
* the downloaded submission JSON

### Exit Survey [7 pts]

👉 **[EXIT SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVUN1g0Qzg5NjhLQk9RQzMwVVJFWFE1RjA0US4u)** 
