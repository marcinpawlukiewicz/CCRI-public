# Lab 2 — Values, Types, Operators

**Total: 100 pts**

---

## Part 1 - Before We Begin (10 pts)

### Entry Survey (7 pts) 

Please complete the short entry survey before beginning the lab:

👉 [ENTRY SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVUOEhVV085RVpaMlk4RDU1NkI0RFc2NjJDQS4u)

---

### Prepare Your Environment (3 pts)

1. Go to the **COMI-2010** folder.
2. Open VS Code and open the folder (File > Open Folder ...)
3. Create a new folder inside COMI-2010 named exactly Lab2. You can do that using VS Code or the terminal, as we did last week.
4. Add the lab files/content to the Lab2 folder.

---

## Part 2 (25 pts) — Type

In this part of the lab, you will focus on understanding outputs and types. You can use any browser and its console to generate output. Document everything in the part2.txt file.

For each expression: (1) predict the result, (2) run it, (3) write the actual result, (4) write typeof of the result, (5) explain in ONE sentence.

List of expressions:
```
8 * null
"5" - 1
"5" + 1
"five" * 2
true == 1
false == 0
null == undefined
null == 0
"" == false
NaN == NaN
0 || 100
0 ?? 100
null ?? 100
"2" + "2" - "2"
```

Use the following template in your text file:
```
Expression:
Predicted: 
Actual:
typeof:
Why? (1 sentence): 
```

### Tip:
```javascript
console.log(8 * null, typeof (8 * null));
```
---

## Part 3 — Operator Gym (30 pts) 

For this part of the lab you have been given two files: `lab2-3.html` and `lab2-3.js`. You will be working only in `lab2-3.js` file.
> DO NOT EDIT `lab2-3.html`!

To see results of your work, open `lab2-3.html` (double-click the file in your directory). As you save changes in your `lab2-3.js` file, you need to refresh the page to see the changes.
> You are only allowed to edit the **TODO** section of the code.

### Task:
Write code that produces the requested results.
- **Precedence (5 pts):** compute two different results by adding parentheses. Expression: **2 + 3 * 4**. The expected outputs are: **14** and **20**.
- **MODULO (7 pts):** (a) check whether n is divisible by 3, the program should output **true** or **false**, (b) return the last digit of n.
- **Comparisons (9 pts):** create 3 comparisons that evaluate to true and 2 that evaluate to false. At least one must use **===** and at least one must use **!==**.
- **Ternary (9 pts):** create score, then resultText is 'pass' if score >= 60 else 'fail'. Test with score = 59 and 60.

Save the file.

📸 Take a screenshot of your `lab2-3.html` output visible in the browser and save it in the Lab2 folder.

## Part 4 - Poem (25 pts)

For this part of the lab you have been given two files: `lab2-4.html` and `lab2-4.js`. You will be working only in `lab2-4.js` file.
> DO NOT EDIT `lab2-4.html`!

To see results of your work, open `lab2-4.html` (double-click the file in your directory). As you save changes in your `lab2-4.js` file, you need to refresh the page to see the changes.
> You are only allowed to edit the **TODO** section of the code.

> **Definition — Prime Number**  
> A natural number greater than 1 that has exactly two distinct factors: 1 and itself. These numbers cannot be formed by multiplying two smaller natural numbers, making them the fundamental building blocks of integers. The smallest prime number is 2, which is the only even prime.


### Task:
- You are given a poem. You need to make it look exactly the same, but using variables and literals.
- Create number variables for NON-primes (1,4,6,8,9) using only prime numbers, e.g., const four = 2 * 2;
- Make one FULL line a variable (for example, the “7 bugs…” line).
- "so I await—and smile 🙂." needs to be separated into two variables: a string + the emoji.
- You need to create at least one line using **\n**.

### Poem:
```javascript
const EXPECTED = `In JavaScript, I count: 1, 2, 3—
"let" whispers: "be."
Arrays dance in [4, 5, 6] with glee,
and 7 bugs flee when tests agree.
I chase 8 truths in strict === light,
then log 9 dreams into the night.
Promises hum, "soon," not "now,"
	so I await—and smile 🙂.`;

```

📸 Take a screenshot of your `lab2-4.html` output visible in the browser and save it in the Lab2 folder.

## Part 5 — Submission (10 pts)

### Zip Your Lab Folder (3 pts)

#### Mac

```bash
zip -r Lab2.zip Lab2
```

#### Windows (PowerShell inside VS Code)

```powershell
Compress-Archive -Path Lab2 -DestinationPath Lab2.zip
```

Upload the Lab2.zip file to Blackboard.

---

### Exit Survey (7 pts)

Please complete the exit survey after finishing:

👉 [EXIT SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVURUlKWklZR1NTMVFLU1BTUk1TMzlONUtGMC4u)
