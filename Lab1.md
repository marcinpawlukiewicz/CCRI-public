# Lab 1 — Introduction to JavaScript & Environment Setup

**Total: 100 pts**

---

## Part 1 (10 pts) — Entry Survey

Please complete the short entry survey before beginning the lab:

👉 [ENTRY SURVEY LINK HERE](https://forms.office.com/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVURUJTTVJYSFUyTzVTU09YVUFWQTlHMjJUQi4u)

---

## Part 2 (15 pts) — Setting Up Your Environment

### Step 1 — Download VS Code

Download and install Visual Studio Code:

[https://code.visualstudio.com](https://code.visualstudio.com)

Install using default options.

---

### Step 2 — Install Node.js

Node.js allows your computer to run JavaScript files.

1. Go to: [https://nodejs.org](https://nodejs.org)
2. Download the **LTS version**
3. Install with default settings

To verify installation, open VS Code terminal and type:

```bash
node -v
```

You should see a version number.

---

### Step 3 — Install VS Code Extensions

In VS Code, go to Extensions and install:

* Prettier — Code formatter

---

## Part 3 (20 pts) — Writing Your First Program

1. Create a folder named **COMI-2010** anywhere on your computer
2. Open VS Code and open this folder (File > Open Folder ...)
3. Open Terminal in VS Code (Terminal > New Terminal)

Create a new folder inside COMI-2010 named exactly Lab1 (enter the following commands in the terminal):

```bash
mkdir Lab1
cd Lab1
```

Create a new file:

```bash
touch first_program.js
```

Open the file and write:

```javascript
console.log("Hello, world!");
console.log("My name is <enter your name here>");
```

Save the file (Ctrl+S / Cmd+S)

Run the program:

```bash
node first_program.js
```

📸 Take a screenshot of the terminal output and save it inside the Lab1 folder.

---

## Part 4 (35 pts) — Understanding Output

Create another file:

```bash
touch second_program.js
```

Paste:

```javascript
console.log(2 + 2);
console.log("2+2");
console.log("2" + "2" - "2");
```

Run it:

```bash
node second_program.js
```

📸 Take a screenshot and save it in the Lab1 folder.

Now create:

```bash
touch second_program.txt
```

Answer in this file:

> Explain what you think happened and why the outputs were different. Why did JavaScript treat numbers and strings differently? Why did the last line produce 20?

Save the file.

---

## Part 5 (10 pts) — Zip Your Lab Folder

Go one directory up:

```bash
cd ..
```

### Mac

```bash
zip -r Lab1.zip Lab1
```

### Windows (PowerShell inside VS Code)

```powershell
Compress-Archive -Path Lab1 -DestinationPath Lab1.zip
```

Upload the Lab1.zip file to Blackboard.

---

## Part 6 (10 pts) — Exit Survey

Please complete the exit survey after finishing:

👉 [EXIT SURVEY LINK HERE](https://forms.office.com/Pages/ResponsePage.aspx?id=GzV1r-s3BUS_enMnzsOApU4seccofrRIrOEsqPewUGVUNTFKWlgzT1I4NDc5MkpUMkQzT01QRk82WS4u)

