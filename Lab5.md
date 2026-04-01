# Lab 5 — Functions

**Total: 100 pts**

---

## Part 1 - Before We Begin [10 PTS]

### Entry Survey [10 PTS]

Please complete the short entry survey before beginning the lab:

👉 **[ENTRY SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVUQVhMUkYxTjFSM1Y5UklVTk1LN0Q2UVU1VS4u)**

---

### Prepare Your Environment

1. Go to the **COMI-2010** folder.
2. Open VS Code and open the folder (**File > Open Folder...**).
3. Create a new folder inside COMI-2010 named exactly **Lab4**.
4. Add the lab files/content to the **Lab5** folder.

---

## Part 2 - Practice [30 PTS]

Open `lab5.html` and follow the instructions below to complete Exercises 1–3.

---

### Exercise 1 - Minimum [10 PTS]

Research the built-in function `Math.min` and then write a function `min` that takes two arguments and returns their minimum value. Use `prompt()` to obtain the arguments and print the returned result using `console.log`. Use the test cases provided in your environment.

**[Math.min()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/min)**

```javascript
// Your code here.

console.log(min(0, 10));
// → 0
console.log(min(0, -10));
// → -10
```

**Provide a screenshot of the output along with the code.**

---

### Exercise 2 - Recursion [15 PTS]

In previous lectures we used `%` (the remainder operator). We can test whether a number is even or odd by using `% 2` to see whether it is divisible by two. Here is another way to define whether a positive whole number is even or odd:

- Zero is even.
- One is odd.
- For any other number N, its evenness is the same as N − 2.

Define a recursive function `isEven` corresponding to this description. The function should accept a single parameter (a positive whole number) and return a Boolean.

```javascript
// Your code here.

console.log(isEven(50));
// → true
console.log(isEven(75));
// → false
console.log(isEven(-1));
// → ??
```

**Provide a screenshot of the output along with the code.**

---

### Exercise 3 - Bean Counting [15 PTS]

You can get the Nth character from a string by writing `[N]` after the string (for example, `string[2]`). The resulting value will be a string containing only one character (for example, `"b"`). The first character has position 0, which means the last one is found at position `string.length - 1`.

Write a function called **countBs** that takes a string as its only argument and returns a number indicating how many uppercase **B** characters appear in the string.

Next, write a function called **countChar** that behaves like `countBs`, except it takes a second argument indicating the character to count (instead of counting only uppercase B characters). Rewrite `countBs` to use this new function.

**Provide a screenshot of the output along with the code.**

---

## Part 3 - Fibonacci Sequence [30 PTS]

When learning programming, one of the classic exercises related to recursion is the Fibonacci sequence. The goal of this exercise is to demonstrate that recursion can sometimes be replaced by something simpler, such as loops learned in previous weeks, and that the loop solution may be more efficient. Both approaches have advantages and disadvantages. Today you will compare them and observe how the computer performs the task and how many steps it requires.

To learn more: [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_sequence)

Write your solution in `lab5.html` under `Fibonacci` tab.

### Definition

- F[0] = 1
- F[1] = 1
- F[n] = F[n-1] + F[n-2]

### Example

```
F[5] = F[4] + F[3]
F[4] = F[3] + F[2]
F[3] = F[2] + F[1]
F[2] = F[1] + F[0]

Hence,
F[2] = 1 + 1 = 2
F[3] = 2 + 1 = 3
F[4] = 3 + 2 = 5
F[5] = 5 + 3 = 8
```

### Your task

Write two functions for the Fibonacci sequence:

- **FibRec** — a recursive function that returns the correct value for a positive integer. If the value is not an integer or is smaller than 0, show an `invalid input` alert.
- **FibIter** — a function that uses loops only to compute the Fibonacci sequence. The function should return the correct result for a positive integer. If the value is not an integer or is smaller than 0, show an `invalid input` alert.

To compare them in terms of time, write another function called `timeIt`:

- Use `performance.now()`
- The function should take two arguments: `label` and `function`. `label` should be a string, and `function` should be a function.
- Test both recursive and iterative functions with the following inputs: **5, 7, 13, 29, 37, 40, 45**
- All tests should be conducted by calling the functions one after another so all results appear in the output window.
- The function should output the following `console.log`. Adjust variable names if needed. Use `toFixed(3)`.

**[Click here to learn more about toFixed().](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed)**

```javascript
console.log(`${label}: result=${value}, time=${(end - start).toFixed(3)}ms`);
```

**Provide a screenshot of the output along with the code.**

---

## Part 4 - Reflection [10 PTS]

Write a short reflection about the Fibonacci sequence exercise (Part 3). Explain which function performed better and why. Consider how many steps the program needed to complete the task.

---

## Part 5 — Submission [10 PTS]

### Zip Your Lab Folder

The folder should include:

- the **JSON file** from `lab5.html`
- **4 screenshots** named `program1`, `program2`, `program3`, and `program4`
- `reflection.txt`

Acceptable screenshot extensions: `.png`, `.jpg`, `.jpeg`

Any additional file or folder will result in **−1 point per extra file/directory**.
Name your zip file using your last name.

---

### Exit Survey [10 pts]

👉 **[EXIT SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVUMjNVMUJRTzY3Vk80TThES1lISUFEQjRCVy4u)**
