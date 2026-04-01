# Lab 6 — Arrays, Objects, Strings, Math

**Total: 100 + [5 BONUS] pts**

---

## Part 1 - Before We Begin [10 PTS]

### Entry Survey [15 PTS]

#### Survey Options

In this lab, you have two options for submitting your assignment based on your response in the survey.

**Option 1:**
Similar to the previous lab, download the ZIP file from Blackboard and complete all the exercises contained in the HTML file. Save your work to the provided JSON file and submit it along with screenshots — one screenshot per exercise, including both your code and the output.

**Option 2:**
You may use your own environment or any online compiler (e.g., [Programiz](https://www.programiz.com/javascript/online-compiler/)). Submit a ZIP file containing each program as `program1.js`, `program2.js`, and so on. See the Submission section below for more details. Screenshots are optional, but it is your responsibility to ensure that your submitted code runs correctly.

Please complete the short entry survey before beginning the lab:

👉 **[ENTRY SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVUNjJHMk9XTVRCMk0zOUU0MkhQRVlVNEswNS4u)**

---

### Prepare Your Environment

1. Go to the **COMI-2010** folder.
2. Open VS Code and open the folder (**File > Open Folder...**).
3. Create a new folder inside COMI-2010 named exactly **Lab6**.
4. Add the lab files/content to the **Lab6** folder.

---

## Part 2 - Practice [70 PTS]

Open `lab6.html`, or use your chosen environment, and follow the instructions below to complete Exercises 1–4.

---

### Exercise 1 - The Sum of a Range [15 PTS]

Write a `range` function that takes two arguments, `start` and `end`, and returns an array containing all the numbers from `start` up to and including `end`.

Next, write a `sum` function that takes an array of numbers and returns the total sum of those numbers. Run the example program to verify that it returns 55.

```javascript
// Your code here.

console.log(range(1, 10));
// → [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
console.log(range(5, 2, -1));
// → [5, 4, 3, 2]
console.log(sum(range(1, 10)));
// → 55
```

**[Option 2: Optional] Provide a screenshot of the output along with the code.**

---

### Exercise 2 - Reversing an Array [15 PTS]

Arrays have a `reverse` method that changes the array by reversing the order of its elements. For this exercise, write two functions: `reverseArray` and `reverseArrayInPlace`.

* `reverseArray` should take an array as its argument and return a new array containing the same elements in reverse order.
* `reverseArrayInPlace` should modify the original array by reversing its elements.

Neither function may use the built-in `reverse()` method.

```javascript
// Your code here.

let myArray = ["A", "B", "C"];
console.log(reverseArray(myArray));
// → ["C", "B", "A"]
console.log(myArray);
// → ["A", "B", "C"]

let arrayValue = [1, 2, 3, 4, 5];
reverseArrayInPlace(arrayValue);
console.log(arrayValue);
// → [5, 4, 3, 2, 1]
```

**[Option 2: Optional] Provide a screenshot of the output along with the code.**

---

### Exercise 3 - A List [20 PTS]

Objects can be used to build many types of data structures. One common structure is a list (not to be confused with arrays). A list is a nested set of objects, where each object holds a reference to the next one.

Example:

```javascript
let list = {
  value: 1,
  rest: {
    value: 2,
    rest: {
      value: 3,
      rest: null
    }
  }
};
```

These objects form a chain.

A useful feature of lists is that they can share parts of their structure. For example, if you create `{ value: 0, rest: list }` and `{ value: -1, rest: list }`, both lists share the same final three elements.

Write the following functions:

* `arrayToList` — builds a list from an array
* `listToArray` — converts a list back into an array
* `prepend` — adds an element to the front of a list
* `nth` — returns the element at a given position (zero-based) or `undefined` if it does not exist

Also write a recursive version of `nth`.

```javascript
// Your code here.

console.log(arrayToList([10, 20]));
// → {value: 10, rest: {value: 20, rest: null}}

console.log(listToArray(arrayToList([10, 20, 30])));
// → [10, 20, 30]

console.log(prepend(10, prepend(20, null)));
// → {value: 10, rest: {value: 20, rest: null}}

console.log(nth(arrayToList([10, 20, 30]), 1));
// → 20
```

**[Option 2: Optional] Provide a screenshot of the output along with the code.**

---

### Exercise 4 - Deep Comparison [20 PTS]

The `==` operator compares objects by identity. However, sometimes you need to compare their actual property values.

Write a function `deepEqual` that takes two values and returns `true` only if they are:

* the same value, or
* objects with the same properties whose values are also equal (checked recursively using `deepEqual`).

Use the `typeof` operator to determine whether values should be compared directly (`===`) or recursively.

Note: Because of a historical quirk, `typeof null` returns `"object"`, so you must handle that case carefully.

The `Object.keys()` function will be useful for comparing object properties.

```javascript
// Your code here.

let obj = { here: { is: "an" }, object: 2 };

console.log(deepEqual(obj, obj));
// → true

console.log(deepEqual(obj, { here: 1, object: 2 }));
// → false

console.log(deepEqual(obj, { here: { is: "an" }, object: 2 }));
// → true
```

**[Option 2: Optional] Provide a screenshot of the output along with the code.**

---

## Part 3 - Reflection [5 PTS]

Returning to Exercise 2 and the discussion of side effects and pure functions (additional resources: [CLICK HERE](https://eloquentjavascript.net/03_functions.html)):

* Which version do you think is more useful in practice?
* Which one runs faster?

Write your reflection in a file named `reflection.txt` (you must create this file — it is not provided).

---

## Part 4 - OPTIONAL: Improving The Sum of a Range [5 PTS]

As a bonus, modify your `range` function to accept an optional third argument representing the step value used when building the array.

If no step is provided, the function should increment by 1 (the original behavior).

Example:

```javascript
range(1, 10, 2);
// → [1, 3, 5, 7, 9]
```

Make sure your function also works with negative step values:

```javascript
range(5, 2, -1);
// → [5, 4, 3, 2]
```

To receive extra credit:

* Copy your current code from Exercise 1.
* Implement this improved version in a separate file (or in the “Improving The Sum of a Range” section inside `lab6.html`).

**[Option 2: Optional] Provide a screenshot of the output along with the code.**

---

## Part 5 — Submission [10 PTS]

### Exit Survey [10 PTS]

👉 **[EXIT SURVEY LINK HERE](https://forms.cloud.microsoft/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVUNzQwTkUwUTBLTk0xUlVNWTQ4TFRFMEdQVy4u)**

---

### Zip Your Lab Folder

#### Option 1:

The folder must include:

* the **JSON file** from `lab6.html`
* **4 screenshots** named `program1`, `program2`, `program3`, and `program4`
* `program5` (optional, if completing the bonus)
* `reflection.txt`

#### Option 2:

The folder must include:

* the **JS files** named `program1.js`, `program2.js`, `program3.js`, and `program4.js`
* `program5.js` (optional, if completing the bonus)
* OPTIONAL: screenshots named `program1`, `program2`, `program3`, `program4`, and `program5`
* `reflection.txt`

#### Additional information (applies to both options):

* Acceptable screenshot extensions: `.png`, `.jpg`, `.jpeg`
* Any additional file or folder will result in **−1 point per extra file/directory**
* Name your ZIP file using your last name

---

Resources: [Data Structures: Objects and Arrays](https://eloquentjavascript.net/04_data.html)
