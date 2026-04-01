# Lab 8 — DOM (Document Object Model)

**Total: 100 pts**

---

## Part 1 - Entry Survey [20 PTS]

> **IMPORTANT:** This survey must be completed, as you will select the topic for your final presentation. Please complete it in a timely manner.

👉 **[ENTRY SURVEY LINK HERE](https://forms.cloud.microsoft/r/Z7BYdpUeyG)**

---

### Prepare Your Environment

1. Go to the **COMI-2010** folder.
2. Open VS Code and open the folder (**File > Open Folder...**).
3. Create a new folder inside COMI-2010 named exactly **Lab8**.
4. Add the lab files/content to the **Lab9** folder.

---

## Part 2 - Build a Table

An HTML table is built with the following tag structure:

```html
<table>
  <tr>
    <th>name</th>
    <th>height</th>
    <th>place</th>
  </tr>
  <tr>
    <td>Kilimanjaro</td>
    <td>5895</td>
    <td>Tanzania</td>
  </tr>
</table>
````

Each `<table>` contains rows defined by `<tr>` elements. Inside each `<tr>`, you can include either header cells (`<th>`) or regular cells (`<td>`).

Given a dataset of mountains (an array of objects with `name`, `height`, and `place` properties), generate a DOM structure for a table that displays the data.

* The table should have one column per key.
* The table should have one row per object.
* Include a header row with `<th>` elements listing the column names.

Write your solution so that the columns are automatically derived from the objects by using the property names of the first object in the dataset.

Display the resulting table in the document by appending it to the element with the id `"mountains"`.

Once your table is working, right-align cells that contain numeric values by setting their `style.textAlign` property to `"right"`.

Create a file named `table.html` and complete the following assignment (use the provided stencil code):

```html
<!doctype html>

<h1>Mountains</h1>

<div id="mountains"></div>

<script>
  const MOUNTAINS = [
    {name: "Kilimanjaro", height: 5895, place: "Tanzania"},
    {name: "Everest", height: 8848, place: "Nepal"},
    {name: "Mount Fuji", height: 3776, place: "Japan"},
    {name: "Vaalserberg", height: 323, place: "Netherlands"},
    {name: "Denali", height: 6168, place: "United States"},
    {name: "Popocatepetl", height: 5465, place: "Mexico"},
    {name: "Mont Blanc", height: 4808, place: "Italy/France"}
  ];

  // Your code here
</script>
```

> **[HINT]**
>
> * Use `document.createElement` to create elements.
> * Use `document.createTextNode` to create text nodes.
> * Use `appendChild` to add nodes to the DOM.
> * Use `Object.keys()` to extract property names from the first object.
> * Use `document.getElementById` or `document.querySelector("#mountains")` to find the container element.

---

## Part 3 - Elements by Tag Name

The `document.getElementsByTagName` method returns all descendant elements with a given tag name.

Implement your own version of this method as a function that:

* Takes a node and a tag name (string) as arguments.
* Returns an array of all descendant element nodes with that tag name.
* Does **not** use built-in methods like `querySelectorAll`.

To find the tag name of an element, use its `nodeName` property. Note that it returns uppercase values, so use `toLowerCase()` or `toUpperCase()` to normalize comparisons.

Create a file named `tag.html` and complete the following assignment (use the provided stencil code):

```html
<!doctype html>

<h1>Heading with a <span>span</span> element.</h1>
<p>A paragraph with <span>one</span>, <span>two</span>
  spans.</p>

<script>
  function byTagName(node, tagName) {
    // Your code here.
  }

  console.log(byTagName(document.body, "h1").length);
  // → 1
  console.log(byTagName(document.body, "span").length);
  // → 3
  let para = document.querySelector("p");
  console.log(byTagName(para, "span").length);
  // → 2
</script>
```

> **[HINT]**
>
> * The solution is best implemented using recursion.
> * You can call the function recursively and combine results.
> * Alternatively, define an inner recursive function that collects results in an array.
> * Only process nodes of type `Node.ELEMENT_NODE` (type 1).
> * For each element:
>
>   * Check if it matches the tag name.
>   * Recursively inspect its children.

---

## Part 4 - The Cat's Hat

Extend the animation so that both the cat and its hat (`<img src="img/hat.png">`) move dynamically.

Options:

* Make the hat orbit on the opposite side of the ellipse.
* Make the hat circle around the cat.
* Create your own unique animation.

To position multiple objects more easily, use **absolute positioning**. This means `top` and `left` are relative to the top-left corner of the document.

To avoid negative coordinates (which would move elements off-screen), add offsets to your position values.

Create a file named `cat.html` and complete the following assignment:

```html
<!doctype html>

<style>body { min-height: 200px }</style>
<img src="img/cat.png" id="cat" style="position: absolute">
<img src="img/hat.png" id="hat" style="position: absolute">

<script>
  let cat = document.querySelector("#cat");
  let hat = document.querySelector("#hat");

  let angle = 0;
  let lastTime = null;

  function animate(time) {
    if (lastTime != null) angle += (time - lastTime) * 0.001;
    lastTime = time;

    cat.style.top = (Math.sin(angle) * 40 + 40) + "px";
    cat.style.left = (Math.cos(angle) * 200 + 230) + "px";

    // Your extensions here

    requestAnimationFrame(animate);
  }

  requestAnimationFrame(animate);
</script>
```

> **Note:** Download PNG images of a cat and a hat, place them in an `img` folder, and ensure they have transparent backgrounds.

> **[HINT]**
>
> * `Math.sin` and `Math.cos` use radians.
> * A full circle is `2π`.
> * The opposite side of a circle can be calculated by adding `Math.PI`.

---

## Part 5 — Exit Survey [5 PTS]

👉 **[EXIT SURVEY LINK HERE](https://forms.cloud.microsoft/r/NYHu2FcS1J)**

---

## Part 6 - Submission [5 PTS]

Upload a zip file named `lastname_lab8.zip` to Blackboard.

Your file structure should look like this:

```
- Lab8
| - table.html
| - tag.html
| - cat.html
| - img/
|     - cat.png
|     - hat.png
```

---

## Resources

* [The Document Object Model](https://eloquentjavascript.net/14_dom.html)


