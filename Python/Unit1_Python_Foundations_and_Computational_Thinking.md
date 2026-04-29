# Python Programming for Kids: Lesson Plans & Worksheets
## Unit 1: Python Foundations & Computational Thinking (Sessions 1–6)

### Unit Overview
Unit 1 is the on-ramp from block-based environments (Scratch, MakeCode, Blockly) into real, text-based Python. Over six 60-minute sessions, students install and tour Thonny, write their first Python programs, master variables and the four core data types, learn how `input()` always hands back a string (and why that matters), explore strings with indexing, slicing and methods, and finally meet the two design artefacts they will use for the rest of the course: pseudocode and flowcharts. The unit closes with a Personal Profile App project where students design first (pseudocode + flowchart) and code second — establishing the design-then-build habit that Cambridge IGCSE 0478 §7 and Singapore O-Level 7155 both reward in their written exams. By the end of Unit 1, every student should be able to write, save, debug and run a small Python program without scaffolding, and be able to describe an algorithm in words before turning it into code.

---

### Session 1: Course Introduction & Thonny Setup

---

#### SESSION 1 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 1 of 48 |
| **Title** | Course Introduction & Thonny Setup |
| **Unit** | Unit 1: Python Foundations & Computational Thinking |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §8 (Programming — basics & environment); 0860 Stage 7/8 — Programming Strand |
| **Singapore Alignment** | O-Level 7155 Module 4 — Programming environment; CFF Secondary Python (Tool Familiarity) |

##### Learning Objectives
By the end of this session, students will be able to:
1. Install or launch Thonny and identify the editor pane, shell pane, and variables view.
2. Write, save, and re-open a Python file (`.py`) that prints a message to the shell.
3. Use `#` to add a single-line comment that explains what a line of code does.
4. Explain in one sentence why text-based languages like Python are used in IGCSE 0478 and O-Level 7155 examinations.

##### Materials Needed
- Laptops with admin/installation rights (one per student)
- Thonny 4.x installer pre-downloaded on a USB or shared drive (in case Wi-Fi is slow)
- Projector connected to the teacher's laptop
- Worksheet: Session 1 (printed or PDF)
- Pen or pencil per student
- A wall poster or slide listing the 8 units of the course
- Sticky notes (one pad per table) for the warm-up

##### Procedure

**0–5 min: Warm-Up — "Block to Text"**
Open the projector to a Scratch-style screenshot showing the blocks: `when green flag clicked → say "Hello, World!" for 2 seconds`. Tell students: "You probably already know how to do this with blocks. Today we're going to do it with letters and punctuation — and by the end of this course, you'll be able to do things blocks can't easily do, like talk to a robot turtle, build a quiz that scores itself, and read data from a file."

Ask: "What's one thing that would be annoying about typing every block as words instead of dragging?" Expect answers like: "We'd misspell things," "We'd forget the order," "It would take longer." Validate all of these and tell them: "You're right — and Python has a special helper called Thonny that catches those mistakes. Let's meet it."

Hand each student a sticky note. Ask them to write their name + one programming language they have heard of (Scratch, Python, Roblox, JavaScript, etc.). Stick them on the board as they enter the room. This becomes a quick visual baseline of prior knowledge.

**5–15 min: Introduction — Why Python, Why Thonny**
Show the unit poster. Walk students briefly through the 8 units — Foundations, Control Flow, Loops, Lists & Dictionaries, Functions, File Handling, OOP basics, and the Capstone Project. Tell them: "By session 48, you will have built a working game, a quiz app, and a small data project." Make the journey visible.

Then explain why Python: "When you sit your IGCSE 0478 exam or your Singapore O-Level 7155 paper, the questions show code that looks like Python — variables, loops, if-statements written in lines of text. So learning Python now isn't just for fun: it's the same skill you'll be tested on later." Write the word **Python** on the board and underline it.

Now introduce Thonny on the projector. Open it. Point out three areas with big arrows:

```
┌──────────────────────────────────────────┐
│  EDITOR  (where we WRITE code)            │
│                                            │
├──────────────────────────────────────────┤
│  SHELL   (where Python TALKS BACK)        │
└──────────────────────────────────────────┘
   VARIABLES VIEW (View → Variables)
```

Type into the shell directly: `2 + 2` and press Enter. The shell shows `4`. "Thonny's shell is like a calculator that also speaks Python. You can try things here without saving them."

**15–35 min: Guided Practice — First Program, Save, Re-open**
Step 1 — Install/launch. Walk around making sure every laptop has Thonny open. For machines without it: download from `thonny.org`, run the installer, accept defaults. Budget 5 minutes max for installs; pair students with installed machines next to those still installing.

Step 2 — Hello, World. In the editor, with everyone watching, type:

```python
# My very first Python program
print("Hello, World!")
```

Save the file. **Critical:** save it to a folder called `Python_Sessions` on the Desktop. Filename: `session01_hello.py`. Press the green Run button (or F5). Show the output appearing in the shell:

```
Hello, World!
```

Make a big deal of the quotation marks. "Python needs the quotes so it knows `Hello, World!` is text — not the names of variables. Forget the quotes and you get a red error message. That red message is your friend, not your enemy — it tells you exactly what to fix."

Step 3 — Comments. Add a second line:

```python
# My very first Python program
print("Hello, World!")
# The next line says hi to my pet
print("Hello, Mochi the cat!")
```

Run it. Two lines of output. Explain: "Anything after a `#` on a line is a comment. Python ignores it. Comments are notes for humans — for you next week, or for your teacher, or for a teammate."

Step 4 — Re-open. Close Thonny entirely. Re-open it. Use **File → Open Recent** to bring back `session01_hello.py`. Show that the code is still there. Tell students: "Real programmers don't memorise their code — they save it. From today, every piece of code you write gets saved."

Walk students through a deliberate mistake: delete the closing `"` and run. Look at the red error together. Read it out loud: `SyntaxError: EOL while scanning string literal`. "Python is saying: I got to the end of the line and you never closed the string." Fix it. Re-run. Celebrate.

**35–50 min: Independent Practice — Worksheet**
Direct students to **Worksheet Part 1 (Thonny scavenger hunt)** and **Part 2 (three first programs)**. Circulate and check:
- Are files being saved (not lost when Thonny closes)?
- Are students typing **straight quotes** `"` not curly quotes `”`? (Curly quotes from word processors are a common pitfall.)
- Are they using `#` for comments (not `//` from JavaScript or `'` from BASIC)?
- Are they reading the **shell** for output rather than expecting a popup window?

Common mistakes to call out gently as you circulate:
- Forgetting parentheses in `print` (Python 2 habit).
- Capitalising `Print` — Python is case-sensitive.
- Saving with `.txt` instead of `.py` — Thonny may then refuse to run it as Python.

**50–55 min: Sharing & Discussion**
Ask three students to project their three programs from Part 2. Prompt the class: "What did the shell show? Was it what you predicted?" Anticipate responses like: "I expected my joke to print but I forgot the quotes," "Mine ran but the second line printed first because I put it at the top," "I changed `print` to `Print` and it crashed." Use each as a teaching moment about case-sensitivity, line order, and quoting.

Ask: "What's one difference between dragging a `say` block in Scratch and typing `print(...)` in Python?" Expect: "Typing is harder but I can do it faster once I know the words," or "I can copy-paste a print line a hundred times — I can't easily do that with blocks."

**55–60 min: Closure & Preview**
Exit-check: "Show me your saved file in the `Python_Sessions` folder before you leave." Then preview: "Next session we learn how to make Python remember things using **variables** — like a labelled box that holds a number or a name. Bring your laptops and your curiosity."

Homework (optional): "Write one more `.py` file at home that prints your three favourite foods on three lines. Save it as `homework01_foods.py`."

##### Differentiation

**Support:**
- Pre-pair stronger and weaker typists; the stronger typist drives the keyboard for the first program, then they swap.
- Provide a printed cheat-sheet with the three things they will type today (`print(...)`, `# comment`, save with `.py`).
- Allow voice-to-text on the warm-up sticky note for students with handwriting difficulties.

**Extension:**
- Challenge: print a 5-line ASCII-art picture of an animal using only `print` statements.
- Investigate the difference between `print("3+4")` and `print(3+4)` and explain in one sentence what's happening.
- Use the Thonny **Variables view** (View menu) to peek at what changes when they assign `x = 5` in the shell — a teaser for next session.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Environment fluency | Cannot open Thonny without help | Opens Thonny, struggles to find shell | Identifies editor, shell, variables view confidently | Uses View menu and shortcuts; helps peers |
| First program runs | Program does not run | Runs only with teacher fix | Runs cleanly first time, saved as `.py` | Runs cleanly + adds extra `print` lines |
| Use of comments | No comments used | Comment present but unrelated | At least one `#` comment that explains a line | Multiple meaningful comments, including a header comment |
| Error recovery | Freezes at red error | Asks for help; doesn't read error | Reads error message and attempts a fix | Diagnoses and fixes independently; can explain the error |

##### Teacher Notes
- **Install gotcha:** On some school-managed Macs, Thonny needs to be opened the first time with right-click → Open to bypass Gatekeeper. Pre-test on one machine before class.
- **Curly quotes from auto-correct** are the #1 silent killer in Session 1. If a student's `print("hi")` mysteriously fails, copy their line into the shell and inspect: if the quotes look like `“ ”` instead of `" "`, that's it. Show them how to disable smart-quotes in their OS or just retype.
- **Filenames:** insist on lowercase, no spaces, ending in `.py`. This habit prevents a flood of "my code won't run" tickets later.
- **Don't teach variables today.** It's tempting because Thonny shows the variables view. Resist — Session 2 needs that "wow" moment.
- **Pace:** if half the class is still installing at the 20-minute mark, abandon the demo and have them shadow a peer's screen. Catch up next session — never punish a slow install.

---

#### SESSION 1 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 1: Course Introduction & Thonny Setup**

---

##### Part 1: Thonny Scavenger Hunt
Open Thonny. Find each item below and tick it off when you can point to it on your screen. For the last column, write a one-sentence description in your own words.

| # | Find this | Tick | What does it do? (one sentence) |
|---|-----------|------|---------------------------------|
| 1 | The **Editor** pane | ☐ | |
| 2 | The **Shell** pane | ☐ | |
| 3 | The green **Run** button | ☐ | |
| 4 | The **Save** button | ☐ | |
| 5 | The **View → Variables** menu | ☐ | |
| 6 | The **File → Open Recent** menu | ☐ | |
| 7 | The Python version number (Help → About) | ☐ | Version I have: ____________ |

Bonus: Find the **debugger** (looks like a small bug icon). Don't click it yet — just point. ☐

---

##### Part 2: Your First Three Programs

Create a folder on your Desktop called `Python_Sessions`. Save all three files there.

**Program 1 — Hello, You!** (filename: `session01_hello.py`)

Type this into the editor and run it:

```python
# Program 1: Saying hello
print("Hello, World!")
print("My name is ___________________")  # <-- put your name here, keep the quotes!
```

**Predict the output before running:**

```
________________________________________________
________________________________________________
```

**Actual output (what the shell showed):**

```
________________________________________________
________________________________________________
```

Did your prediction match? ☐ Yes  ☐ No — what was different? _______________________________

---

**Program 2 — Three Favourites** (filename: `session01_favourites.py`)

Fill in the blanks, then run.

```python
# Program 2: My three favourite things
print("My favourite food is _______________.")
print("My favourite game is _______________.")
print("My favourite subject is _____________.")
```

How many lines did the shell print? __________

---

**Program 3 — A Comment Detective** (filename: `session01_comments.py`)

Type this exactly. Predict what will print **before** you run it.

```python
# print("Line A")
print("Line B")
# print("Line C")
print("Line D")
```

**My prediction (which lines will appear?):**

```
________________________________________________
________________________________________________
```

**What actually printed:**

```
________________________________________________
________________________________________________
```

In your own words, what does the `#` symbol do? _______________________________________________

---

##### Part 3: Independent Challenge — The Joke Machine

Create a new file called `session01_joke.py`. Write a program that prints a knock-knock joke across **at least 4 lines**. Add **at least one comment** that says who the joke is for.

Sketch your joke here before typing:

```
Line 1: ____________________________________________________
Line 2: ____________________________________________________
Line 3: ____________________________________________________
Line 4: ____________________________________________________
```

When it runs, ask the person next to you to read your joke from the shell. Did they laugh? ☐ Yes  ☐ No  ☐ Politely

---

##### Reflection
- What did I learn today?  _________________________________________________________
- What was confusing?  ___________________________________________________________
- One thing I want to try at home: _________________________________________________

##### Bonus / Stretch Challenge
Create a file `session01_ascii.py` that prints a picture of a cat using only keyboard characters. Example output:

```
 /\_/\
( o.o )
 > ^ <
```

You'll need one `print(...)` line per row. Hint: spaces inside the quotes count!

---

### Session 2: Variables, Constants & Data Types

---

#### SESSION 2 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 2 of 48 |
| **Title** | Variables, Constants & Data Types |
| **Unit** | Unit 1: Python Foundations & Computational Thinking |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §8.1 — Variables, constants, data types; 0860 Stage 8 — Data representation |
| **Singapore Alignment** | O-Level 7155 Module 4.1 — Identifiers, constants, data types; CFF Secondary Python |

##### Learning Objectives
By the end of this session, students will be able to:
1. Declare a variable using `=` and inspect it in Thonny's variables view.
2. Identify and produce examples of the four primary Python data types: `int`, `float`, `str`, and `bool`.
3. Convert between data types using `int()`, `float()`, `str()`, and `bool()` and predict the result.
4. Apply naming conventions: snake_case for variables, UPPER_CASE for constants, descriptive names always.

##### Materials Needed
- Laptops with Thonny installed (Session 1 setup confirmed)
- Worksheet: Session 2
- Projector
- A box (literal physical box if possible) labelled `score` with a paper card inside saying "0" — used as a metaphor in the warm-up
- Whiteboard markers in 3 colours

##### Procedure

**0–5 min: Warm-Up — "What's in the Box?"**
Hold up the labelled box. "This box has a label — `score` — and inside it there's a card that says 0. If I score a goal in a game, what should I do to the box?" Expect: "Change the card to 1," "Replace what's inside." Exactly. "The label stays the same, but what's inside can change. That's a **variable** in Python."

Ask: "Could I put a fish inside this `score` box? Would that be sensible?" Expect: "No, score should be a number." Praise that — variables can technically hold anything in Python, but **good programmers** keep the contents matching the label.

**5–15 min: Introduction — Variables and the Four Types**
On the projector, in Thonny's editor, type and run:

```python
# Variables hold values
score = 0
player_name = "Alex"
pi_value = 3.14159
game_over = False

print(score)
print(player_name)
print(pi_value)
print(game_over)
```

Open **View → Variables**. The variables view lights up:

```
score        0
player_name  'Alex'
pi_value     3.14159
game_over    False
```

"Look! Thonny is showing us inside the boxes. The label is on the left, the value on the right." Now introduce the four types explicitly. Write on the board in three colours:

| Type | Example | Plain English |
|------|---------|---------------|
| `int` | `0`, `42`, `-7` | Whole numbers |
| `float`| `3.14`, `0.5`, `-2.0` | Numbers with a decimal point |
| `str` | `"Alex"`, `"hi"` | Text in quotes |
| `bool`| `True`, `False` | Yes/No, on/off (capital T and F!) |

Demonstrate `type()`:

```python
print(type(score))        # <class 'int'>
print(type(pi_value))     # <class 'float'>
print(type(player_name))  # <class 'str'>
print(type(game_over))    # <class 'bool'>
```

Briefly show `id()` — "Every variable has a memory address. You'll meet this again in Unit 7." Don't dwell.

**15–35 min: Guided Practice — Casting and Naming**
**Casting demo.** Ask: "What happens if I add a number and a string?"

```python
age = "12"           # string from a website form
next_year = age + 1  # uh oh
```

Run it. Red error: `TypeError: can only concatenate str (not "int") to str`. "Python is saying: I can't glue a number onto a piece of text. They're different types." Fix it with casting:

```python
age = "12"
age = int(age)        # cast string -> int
next_year = age + 1
print(next_year)      # 13
```

Demonstrate the four casting functions with a small table on the board:

```python
int("7")        # 7
int(3.9)        # 3   (NOTE: truncates, doesn't round!)
float("3.14")   # 3.14
str(42)         # "42"
bool(0)         # False
bool(1)         # True
bool("")        # False  (empty string)
bool("hi")      # True
```

Pause on `int(3.9) → 3`. "It chops off the decimal — it does **not** round. If you wanted 4, you'd use `round(3.9)`. We'll see that next session."

**Naming conventions.** Write three pairs on the board:

| Bad name | Good name | Why |
|----------|-----------|-----|
| `x` | `score` | Tells the reader what it is |
| `MyAge` | `my_age` | Python style: snake_case |
| `pi = 3.14` | `PI = 3.14` | Constants in UPPER_CASE so we don't change them |

Explain: "In Python, **constants** are not enforced by the language. We just agree as a team to write them in UPPER_CASE so everyone knows: don't change this." Show a constant in action:

```python
PI = 3.14159
GRAVITY = 9.81
MAX_PLAYERS = 4

radius = 5
area = PI * radius ** 2     # ** is "to the power of"
print(area)
```

Note: this convention is explicitly required by the Singapore 7155 syllabus. Tell students that examiners look for it.

**35–50 min: Independent Practice — Worksheet**
Direct students to **Worksheet Part 1 (Predict the type)**, **Part 2 (Casting puzzles)**, and **Part 3 (Fix the naming)**. As you circulate, watch for:
- Students writing `True` as `true` (lowercase) — Python rejects this.
- Students using a Python keyword as a variable name (e.g. `print = 5`). Catch this fast: `print` will then break for the rest of the session.
- Confusion about `int("3.5")` — this **errors** because the string isn't a clean integer. Use `int(float("3.5"))` instead. This is an intentional "stretch" trap on the worksheet.
- Curly-quote / smart-quote issues persisting from Session 1.

**50–55 min: Sharing & Discussion**
Project a few students' Part 3 (naming) answers. Discuss: "Why is `temperature_celsius` better than `t`?" Expect: "We don't have to remember what t is," "If we add temperature_fahrenheit later, both names will be clear."

Pose a thinking question: "If I write `is_logged_in = True` and someone reads my code six months later, do they understand it without any comment?" Expect: "Yes, it reads like English." That's the goal.

**55–60 min: Closure & Preview**
Exit-check: "Tell me, in your own words, what `int("42")` does and what `int(42.9)` gives you." Take three quick verbal answers.

Preview: "Next session we let the **user** type things in. Spoiler: whatever they type comes in as a string, even if it looks like a number. We'll learn how to handle that."

Homework (optional): "Write a `.py` file with at least one variable of each type and print all four `type(...)` results. Save as `homework02_types.py`."

##### Differentiation

**Support:**
- Provide a printed "type sticker" reference card to keep on the desk.
- Pre-fill the casting puzzle answers for the first two rows so students see the pattern.
- Pair with a Session-1-confident peer for the typing-heavy parts.

**Extension:**
- Investigate `complex` numbers (`3+4j`) — what does `type(3+4j)` say? Don't teach how to use them; just observe.
- Try `bool([])`, `bool([0])`, `bool({})` — what's the rule? (Empty containers are False.)
- Introduce `f"{score=}"` debug print form — a teaser for Session 4.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Variable assignment | Cannot assign or print | Assigns with help, occasional `=`/`==` confusion | Assigns and prints all four types | Assigns, prints, and re-assigns; uses variables view |
| Type identification | Mixes int and float | Identifies 2–3 types correctly | Identifies all four types from value | Predicts type of expressions (e.g. `5/2`) without running |
| Casting | Cannot cast | Casts with help, errors on edge cases | Casts cleanly between common pairs | Handles `int(float("3.5"))`-style chains |
| Naming conventions | Uses `x`, `y`, single letters | Some descriptive names, mixed case | Consistent snake_case, UPPER_CASE for constants | All names meaningful, constants flagged, no keyword collisions |

##### Teacher Notes
- **`True` vs `true`:** This will trip up students with JavaScript or Scratch backgrounds. Make it explicit on the board.
- **`int = 5`:** If a student types this, all subsequent `int(...)` calls in their shell break with `TypeError: 'int' object is not callable`. To recover: restart the shell (Run → Stop & Restart Backend, or Ctrl+F2). Add this to your "magic recovery move" list — you'll need it again.
- **Mutability is NOT today's lesson.** A student may ask "is the box the same box if I put a new value in?" Answer briefly with "for now, treat each `=` as putting a new card in the box" and move on. Mutability is Unit 4.
- **Avoid `input()` today.** It's reserved for Session 3 so we can give it the attention it deserves.
- **Don't introduce lists.** A keen student may try `score = [1, 2, 3]`. Acknowledge it exists, defer to Unit 4.

---

#### SESSION 2 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 2: Variables, Constants & Data Types**

---

##### Part 1: Predict the Type

For each value, tick the type you think Python will report. Then run `print(type(...))` in the shell to check. Tick the "Correct?" column.

| # | Value | int | float | str | bool | Correct? |
|---|-------|:---:|:-----:|:---:|:----:|:--------:|
| 1 | `42` | ☐ | ☐ | ☐ | ☐ | ☐ |
| 2 | `3.14` | ☐ | ☐ | ☐ | ☐ | ☐ |
| 3 | `"42"` | ☐ | ☐ | ☐ | ☐ | ☐ |
| 4 | `True` | ☐ | ☐ | ☐ | ☐ | ☐ |
| 5 | `"True"` | ☐ | ☐ | ☐ | ☐ | ☐ |
| 6 | `0` | ☐ | ☐ | ☐ | ☐ | ☐ |
| 7 | `0.0` | ☐ | ☐ | ☐ | ☐ | ☐ |
| 8 | `-7` | ☐ | ☐ | ☐ | ☐ | ☐ |
| 9 | `"3.14"` | ☐ | ☐ | ☐ | ☐ | ☐ |
| 10 | `False` | ☐ | ☐ | ☐ | ☐ | ☐ |

How many did you get right on the first guess? ____ / 10

---

##### Part 2: Casting Puzzles

Predict the result of each line **before** running. Write your prediction, then run it in the Thonny shell and write the actual result.

| # | Code | Predicted | Actual |
|---|------|-----------|--------|
| 1 | `int("9")` | _________ | _________ |
| 2 | `int(2.99)` | _________ | _________ |
| 3 | `float("3.14")` | _________ | _________ |
| 4 | `str(100)` | _________ | _________ |
| 5 | `bool(0)` | _________ | _________ |
| 6 | `bool(1)` | _________ | _________ |
| 7 | `bool("")` | _________ | _________ |
| 8 | `bool("False")` | _________ | _________ |
| 9 | `int("3.5")` | _________ | _________ |
| 10 | `int(float("3.5"))` | _________ | _________ |

Question 8 is tricky. Why does `bool("False")` give `True`? Hint: think about whether the string is empty.

Answer: ___________________________________________________________________________

---

##### Part 3: Fix the Naming

Below is a piece of code with poor variable names. Rewrite it using **snake_case** for variables, **UPPER_CASE** for constants, and **descriptive names**.

**Original (don't run, just read):**

```python
x = 3.14159
R = 5
A = x * R ** 2
N = "Bob"
loggedIn = True
print(N, A, loggedIn)
```

**My rewrite (write into Thonny as `session02_naming.py` and run):**

```python
________ = 3.14159        # what should this be called? It's a constant!
________ = 5
________ = ________ * ________ ** 2
________ = "Bob"
________ = True
print(________, ________, ________)
```

Now answer: which of your variables is a **constant**? Why did you choose that name style?

Answer: ___________________________________________________________________________

---

##### Reflection
- What did I learn today?  _________________________________________________________
- What was confusing?  ___________________________________________________________
- One thing I want to try at home: _________________________________________________

##### Bonus / Stretch Challenge
Write a small script `session02_temperature.py` that:

1. Stores `FREEZING_C = 0` as a constant.
2. Stores `boiling_c = 100` as a variable.
3. Casts both to `float` and prints them along with their types.
4. Adds them together and prints the sum.

Predict the type of the sum **before** running. Was it `int` or `float`? Why?

---

### Session 3: Input, Numbers & Arithmetic

---

#### SESSION 3 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 3 of 48 |
| **Title** | Input, Numbers & Arithmetic |
| **Unit** | Unit 1: Python Foundations & Computational Thinking |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §8.2 — Input/Output and arithmetic; 0860 Stage 8 — Programming |
| **Singapore Alignment** | O-Level 7155 Module 4.2 — Operators, expressions, precedence; CFF Secondary Python |

##### Learning Objectives
By the end of this session, students will be able to:
1. Use `input()` to read text from the user and explain why the result is always a string.
2. Cast user input to `int` or `float` to perform arithmetic correctly.
3. Use the seven arithmetic operators `+ - * / // % **` and predict their output.
4. Apply Python's operator precedence (PEMDAS-style) to evaluate compound expressions and use parentheses to control order.

##### Materials Needed
- Laptops with Thonny
- Worksheet: Session 3
- Projector
- A printed PEMDAS poster (or write on whiteboard)
- Calculator app on phone (for cross-checking)

##### Procedure

**0–5 min: Warm-Up — "Mind Reader"**
Tell the class: "I'm going to ask you a question, and Python will read your answer." Open Thonny and type live:

```python
name = input("What's your name? ")
print("Nice to meet you,", name + "!")
```

Run it. The shell prompts. Pick a student volunteer to type their name. Output: `Nice to meet you, Marcus!`. The class gasps a little. Then ask: "How is this different from `print(...)` alone?" Expect: "It waits for me," "It listens." Exactly — input is the program **listening**.

**5–15 min: Introduction — The Input Trap**
Now the trap. Type:

```python
age = input("How old are you? ")
next_year = age + 1
print("Next year you'll be", next_year)
```

Run. Type `12`. Red error: `TypeError: can only concatenate str (not "int") to str`. "What happened? I typed a number!" Pause for student reactions. Then reveal the rule, in big letters on the board:

> **`input()` ALWAYS returns a string. Always. Always. Always.**

Even if the user types `12`, Python receives `"12"`. Fix:

```python
age = int(input("How old are you? "))
next_year = age + 1
print("Next year you'll be", next_year)
```

Run again. Type `12`. Output: `Next year you'll be 13`. "We **wrap** the input in `int(...)` to convert the string to a number. Same trick with `float(...)` for decimals."

Caution them about non-numeric input: `int(input(...))` crashes if the user types `"hello"`. We'll handle that with `try/except` in Unit 2 — for now, assume the user behaves.

**15–35 min: Guided Practice — Operators and a Calculator**
Put up the operator table:

```python
a = 7
b = 2

print(a + b)   # 9    addition
print(a - b)   # 5    subtraction
print(a * b)   # 14   multiplication
print(a / b)   # 3.5  TRUE division (always float!)
print(a // b)  # 3    FLOOR division (drops decimal)
print(a % b)   # 1    MODULUS (remainder)
print(a ** b)  # 49   exponent (power)
```

Stress two surprises:
1. `/` always returns a `float` — even `4 / 2` gives `2.0`, not `2`. Use `//` if you want a whole number.
2. `%` is the **remainder** operator, not percent. `10 % 3 = 1`. It's incredibly useful (test for even/odd: `n % 2 == 0`).

**Operator precedence.** Write on the board, top = first:

```
1. Parentheses ()
2. Exponent **
3. Unary minus -x
4. * / // %
5. + -
```

Demonstrate:

```python
print(2 + 3 * 4)        # 14, not 20 — multiplication first
print((2 + 3) * 4)      # 20 — parentheses force addition first
print(2 ** 3 ** 2)      # 512 — ** is right-to-left: 2 ** (3**2) = 2**9
print(20 - 4 - 3)       # 13 — left-to-right for same-rank
```

**Build a calculator.** Live-code together:

```python
# session03_calculator.py
print("=== Mini Calculator ===")
num1 = float(input("First number: "))
num2 = float(input("Second number: "))

print("Sum:        ", num1 + num2)
print("Difference: ", num1 - num2)
print("Product:    ", num1 * num2)
print("Quotient:   ", num1 / num2)
print("Remainder:  ", num1 % num2)
print("Power:      ", num1 ** num2)
```

Run it together with two volunteer numbers. Watch the divide-by-zero risk: if the second number is 0, `/` crashes. Note that for next session.

**35–50 min: Independent Practice — Worksheet**
Send students to **Worksheet Part 1 (Input-and-cast drill)**, **Part 2 (Operator predictions)**, and **Part 3 (Build three calculators: BMI, tip, and rectangle area)**. As you circulate, watch for:
- Forgetting to cast input — they'll see the same `TypeError` you demoed.
- Using `^` for exponent (it's XOR in Python, not power). Common from maths class.
- Floor-division confusion: `7 // 2 = 3`, not `3.5`.
- Misordering operations: `2 + 3 * 4` evaluated left-to-right gives 20 instead of 14.

**50–55 min: Sharing & Discussion**
Pick a student who built the BMI calculator. Project it. Ask the class: "What units does this assume? What if someone enters their weight in pounds?" Expect: "It would give a wrong number." Excellent — this is a real-world software bug called a **unit error** (the Mars Climate Orbiter crashed because of one).

Discuss: "Why does Python make us cast input? Why not auto-detect numbers?" Expect: "Because `12` could be a number or a name (like a band)," "Because we might want it as text for a phone number." Validate — explicit casting prevents ambiguity.

**55–60 min: Closure & Preview**
Exit-check: "What does `15 % 4` give and why?" Answer: `3`, the remainder when 15 is divided by 4.

Preview: "Next session we dive into **strings** — how to chop them, glue them, and squeeze them. We'll build a username generator."

Homework (optional): Write a `.py` file that asks for a meal price and a tip percentage, then prints the total. Save as `homework03_tip.py`.

##### Differentiation

**Support:**
- Provide a "casting cheat sheet" printout: when do I use `int(...)` vs `float(...)`?
- Pre-fill the input prompts in the BMI starter code so they only fill the formula.
- Use a single-line input pattern: `age = int(input("Age: "))` rather than two-line.

**Extension:**
- Add input validation: ask the user for a positive number; if negative, print a polite warning. (Pre-cursor to Unit 2.)
- Build a **time converter**: enter total seconds, output `H:M:S` using `//` and `%`.
- Investigate `divmod(a, b)` — what does it return? Why might it be more efficient than calling `//` and `%` separately?

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Using `input()` | Cannot read input | Reads input but forgets prompt | Reads input with clear prompt | Reads, casts, validates lightly |
| Casting input | Doesn't cast; gets TypeError | Casts with reminder | Casts confidently to int and float | Chooses int vs float based on context |
| Operators | Uses only `+ -` | Uses 4–5 operators | Uses all 7 correctly | Explains `/` vs `//` vs `%` distinctions |
| Precedence | Ignores order; wrong answers | Sometimes correct, doesn't use parentheses | Uses parentheses to control order | Predicts compound expressions without running |

##### Teacher Notes
- **The single biggest Session-3 error:** student writes `age = input(...)` then `age + 1` and gets confused by the `TypeError`. They will keep doing it for two more sessions. Repeat the rule (input returns a string) every time it happens — eventually it sticks.
- **Floor division on negatives:** `-7 // 2 = -4`, not `-3`. Python rounds toward **negative infinity**, not toward zero. Don't dive into this unless asked, but be ready.
- **Float surprises:** `0.1 + 0.2 = 0.30000000000000004` will catch out a sharp student. Acknowledge ("computers store decimals approximately") and move on; this is a Unit 2/3 topic.
- **Don't teach `if` yet.** Tempting, since validation is natural, but Session 7 is right around the corner.
- **Save first, run second.** Some students will test in the shell and lose their work. Insist that today's calculator code goes in a `.py` file.

---

#### SESSION 3 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 3: Input, Numbers & Arithmetic**

---

##### Part 1: Input-and-Cast Drill

Complete each line so it does what the comment says. Run each in Thonny to verify.

```python
# 1. Ask for the user's age and store it as a whole number
age = ________(input("Your age: "))

# 2. Ask for the user's height in metres and store it as a decimal
height = ________(input("Your height in metres: "))

# 3. Ask for a colour and store it as text
favourite_colour = ________("Your favourite colour: ")

# 4. Ask for a year of birth and store it as a whole number
birth_year = ________(input("Year you were born: "))
```

Trace: if the user types `12` for age, what is the **type** stored in `age`? __________

If we forgot the `int(...)` cast, what would the type be? __________

---

##### Part 2: Operator Predictions

Predict the output of each expression. Then run it in the shell and tick if correct.

| # | Expression | Prediction | Actual | ✓ |
|---|------------|------------|--------|---|
| 1 | `7 + 3 * 2` | _______ | _______ | ☐ |
| 2 | `(7 + 3) * 2` | _______ | _______ | ☐ |
| 3 | `10 / 4` | _______ | _______ | ☐ |
| 4 | `10 // 4` | _______ | _______ | ☐ |
| 5 | `10 % 4` | _______ | _______ | ☐ |
| 6 | `2 ** 5` | _______ | _______ | ☐ |
| 7 | `2 ** 3 ** 2` | _______ | _______ | ☐ |
| 8 | `20 - 4 - 3` | _______ | _______ | ☐ |
| 9 | `15 % 5` | _______ | _______ | ☐ |
| 10 | `(8 + 2) ** 2 // 3` | _______ | _______ | ☐ |

---

##### Part 3: Build Three Calculators

**3A — Rectangle Area** (filename: `session03_area.py`)

```python
# TODO: ask for length and width as floats
length = ________
width  = ________

# TODO: compute area
area = ________

print("The area is", area, "square units.")
```

Test with length=5, width=3. Expected: `15.0`.

---

**3B — Tip Calculator** (filename: `session03_tip.py`)

```python
# TODO: ask for the bill total (float) and tip percent (float)
bill = ________
tip_percent = ________

# TODO: compute tip and total
tip = ________
total = ________

print("Tip:  ", tip)
print("Total:", total)
```

Test with bill=50, tip_percent=15. Expected tip: `7.5`. Expected total: `57.5`.

---

**3C — BMI Calculator** (filename: `session03_bmi.py`)

The Body Mass Index formula: `BMI = weight_kg / (height_m ** 2)`

```python
# TODO: get inputs
weight_kg = ________
height_m  = ________

# TODO: apply the formula
bmi = ________

print("Your BMI is", bmi)
```

Test with weight=60, height=1.65. Expected (approx): `22.04`.

---

##### Reflection
- What did I learn today?  _________________________________________________________
- What was confusing?  ___________________________________________________________
- One thing I want to try at home: _________________________________________________

##### Bonus / Stretch Challenge — Time Converter

Write `session03_time.py` that asks for a total number of seconds and prints how many hours, minutes, and seconds that is. Use `//` and `%`.

Example: 3725 seconds → 1 hour, 2 minutes, 5 seconds.

```python
total_seconds = int(input("Total seconds: "))
hours   = ________
minutes = ________
seconds = ________
print(hours, "hour(s),", minutes, "minute(s),", seconds, "second(s)")
```

---

### Session 4: Strings, Indexing & Slicing

---

#### SESSION 4 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 4 of 48 |
| **Title** | Strings, Indexing & Slicing |
| **Unit** | Unit 1: Python Foundations & Computational Thinking |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — String manipulation; 0860 Stage 8 — Text processing |
| **Singapore Alignment** | O-Level 7155 Module 4.3 — String operations; CFF Secondary Python |

##### Learning Objectives
By the end of this session, students will be able to:
1. Access individual characters of a string using positive and negative indexes.
2. Extract substrings using slicing notation `[start:stop:step]`.
3. Apply common string methods: `len()`, `.upper()`, `.lower()`, `.strip()`, `.replace()`, `.split()`.
4. Format output using f-strings, including expressions inside `{}`.

##### Materials Needed
- Laptops with Thonny
- Worksheet: Session 4
- Projector
- Index strip on the wall: a long paper strip with `P Y T H O N` and indexes `0 1 2 3 4 5` written above and `-6 -5 -4 -3 -2 -1` below.

##### Procedure

**0–5 min: Warm-Up — "Find the Letter"**
Hold up the index strip with `P Y T H O N`. "If I ask for letter number 0, which is it?" Expect: "P." "Letter number 5?" "N." "Letter number minus 1?" Some hesitation. Reveal: "Also N — minus 1 means the **last** one. Minus 2 is the second-to-last." Have them count along negative indexes.

This physical scaffold is invaluable; tape it to the wall above the projector for the rest of the session.

**5–15 min: Introduction — Strings as Sequences**
Open Thonny:

```python
word = "Python"

# Indexing — positive
print(word[0])   # P
print(word[1])   # y
print(word[5])   # n

# Indexing — negative
print(word[-1])  # n  (last char)
print(word[-6])  # P  (first char, counting from right)

# Length
print(len(word)) # 6
```

Big board diagram:

```
 Index:    0   1   2   3   4   5
           P   y   t   h   o   n
 Index:   -6  -5  -4  -3  -2  -1
```

"This is exactly the same idea as Scratch's 'letter N of word' block — but Python lets us count from the right too, with negatives."

Now slicing:

```python
word = "Python"
print(word[0:3])    # 'Pyt'      chars 0, 1, 2 (stop is EXCLUSIVE)
print(word[2:])     # 'thon'     from 2 to end
print(word[:4])     # 'Pyth'     from start to before 4
print(word[::2])    # 'Pto'      every 2nd char
print(word[::-1])   # 'nohtyP'   REVERSED!
```

"The pattern is `[start:stop:step]`. Start is included, stop is **not**. Step defaults to 1. A step of -1 reverses." The reversed string trick always gets a "whoa" — milk the moment.

**15–35 min: Guided Practice — Methods and f-strings**
Demonstrate the six core string methods:

```python
greeting = "  Hello, World!  "

print(len(greeting))            # 17  (with spaces)
print(greeting.upper())         # "  HELLO, WORLD!  "
print(greeting.lower())         # "  hello, world!  "
print(greeting.strip())         # "Hello, World!"  (no spaces)
print(greeting.replace("World", "Python"))  # "  Hello, Python!  "

sentence = "I love coding in Python"
print(sentence.split())         # ['I', 'love', 'coding', 'in', 'Python']
print(sentence.split("o"))      # ['I l', 've c', 'ding in Pyth', 'n']
```

Stress that **methods do not modify the original string** — they return a **new** string. "Strings are immutable. Whatever method you call on `greeting`, the value of `greeting` itself stays the same. If you want the change, you have to assign it back: `greeting = greeting.strip()`."

**f-strings.** Old-style first to show the pain:

```python
name = "Aisha"
age = 12
# Old way — clunky
print("Hi " + name + ", you are " + str(age) + " years old.")
```

Now the modern way:

```python
print(f"Hi {name}, you are {age} years old.")
```

"The `f` before the quote turns it into an **f-string**. Anything in `{}` gets evaluated and placed into the text. No more `+` chains, no more `str()`."

Show expressions inside `{}`:

```python
price = 9.99
quantity = 3
print(f"Total: ${price * quantity:.2f}")   # Total: $29.97
```

The `:.2f` formats to 2 decimal places. Bonus tip — show debug form:

```python
score = 85
print(f"{score=}")    # score=85   — useful for debugging
```

**35–50 min: Independent Practice — Worksheet**
Direct students to **Worksheet Part 1 (Indexing/slicing puzzles)**, **Part 2 (String method playground)**, **Part 3 (Username generator)**. Watch for:
- Off-by-one with the exclusive `stop`. Students often write `word[0:5]` thinking they get all 6 chars.
- Forgetting that `.upper()` returns a new string and getting confused why their variable "didn't change."
- Mixing `len(word)` with `word.length` (JavaScript habit) or `word.len()`.
- Curly-brace pitfall in f-strings: forgetting the `f` prefix → braces print literally.

**50–55 min: Sharing & Discussion**
Project a couple of username generator solutions. Ask: "Whose username is funniest? Whose is most secure-looking?" Discuss what makes a good username generator: short, memorable, no spaces, mix of letters and a number.

Pose: "Why is `word[::-1]` a quick way to check for a palindrome?" Expect: "Because if the reversed string equals the original, it's a palindrome." Mark that idea — it returns in Unit 2.

**55–60 min: Closure & Preview**
Exit-check: "What does `'hello'[1:4]` give?" Answer: `'ell'`. Confirm understanding of inclusive start, exclusive stop.

Preview: "Tomorrow we slow down and learn to **plan** before we code — pseudocode and flowcharts. They look boring, but they're how IGCSE and O-Level questions are written."

Homework (optional): Write a `.py` file that asks for a sentence and prints it (a) reversed, (b) in upper case, (c) with all spaces replaced by underscores. Save as `homework04_strings.py`.

##### Differentiation

**Support:**
- Print the index strip and tape it to the desk for slow processors.
- Give a "method menu" card with the six methods and a 1-line example each.
- Pair-program Part 3 (username generator).

**Extension:**
- Build a Caesar cipher shifter (shift each letter by 1) — a teaser for Unit 5.
- Investigate `.startswith()`, `.endswith()`, `.find()`, `.count()`. Demo how they would help validate user input.
- Use `:>10` and `:<10` and `:^10` in f-strings to align text — useful for Session 6's profile card.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Indexing | Cannot retrieve a char | Retrieves with help; off-by-one errors | Retrieves with positive and negative indexes | Predicts indexes without counting on fingers |
| Slicing | Cannot slice | Slices with start and stop | Uses start, stop, and step | Uses negative step and shorthand `[:n]`, `[n:]` |
| Methods | Doesn't know the methods | Uses 1–2 methods | Uses 4+ methods correctly | Chains methods (e.g. `.strip().lower()`) |
| f-strings | Uses `+` concat only | f-string with simple `{var}` | f-string with expression inside `{}` | f-string with format spec `{val:.2f}` |

##### Teacher Notes
- **Inclusive vs exclusive:** Students will struggle with this for two sessions. Re-show the strip every time it comes up.
- **Strings are immutable** is a big concept. Don't dwell on the word "immutable" — say "strings can't be changed in place; methods give you a new string." That phrasing sticks.
- **Empty slice trap:** `word[5:2]` returns `''` (empty), not an error. Be ready for confused looks.
- **f-string typo:** missing `f` is the #1 bug. The braces will print literally as `{name}`. Train students to scan for the `f`.
- **Don't teach lists yet.** `.split()` returns a list and a sharp student will ask "what's that?" Acknowledge: "It's a list — we meet those in Unit 4 — for now we just use it."

---

#### SESSION 4 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 4: Strings, Indexing & Slicing**

---

##### Part 1: Indexing & Slicing Puzzles

Given `word = "Computing"`:

| # | Expression | Predicted | Actual |
|---|------------|-----------|--------|
| 1 | `word[0]` | _______ | _______ |
| 2 | `word[3]` | _______ | _______ |
| 3 | `word[-1]` | _______ | _______ |
| 4 | `word[-3]` | _______ | _______ |
| 5 | `len(word)` | _______ | _______ |
| 6 | `word[0:4]` | _______ | _______ |
| 7 | `word[3:]` | _______ | _______ |
| 8 | `word[:5]` | _______ | _______ |
| 9 | `word[::2]` | _______ | _______ |
| 10 | `word[::-1]` | _______ | _______ |

Tracing diagram — fill in the indexes:

```
 Index:    __  __  __  __  __  __  __  __  __
           C   o   m   p   u   t   i   n   g
 Index:    __  __  __  __  __  __  __  __  __
```

---

##### Part 2: String Method Playground

```python
text = "  HELLO, python WORLD!  "
```

Predict, then run.

| # | Expression | Predicted | Actual |
|---|------------|-----------|--------|
| 1 | `text.lower()` | _______ | _______ |
| 2 | `text.upper()` | _______ | _______ |
| 3 | `text.strip()` | _______ | _______ |
| 4 | `text.replace("python", "Java")` | _______ | _______ |
| 5 | `text.strip().split()` | _______ | _______ |
| 6 | `len(text)` | _______ | _______ |
| 7 | `len(text.strip())` | _______ | _______ |

After running line 1, what is the value of `text` itself? __________________________

Why? _____________________________________________________________________________

---

##### Part 3: Username Generator (filename `session04_username.py`)

Build this program. Fill in the blanks.

```python
# Username generator
first_name = input("First name: ").________()    # remove leading/trailing spaces
last_name  = input("Last name:  ").________()
fav_number = int(input("Favourite number: "))

# Take first 3 chars of first name + last 2 chars of last name + favourite number
first_part  = first_name[________].________()    # 3 chars, lower case
last_part   = last_name[________].________()     # last 2 chars, lower case

username = f"{________}{________}{________}"
print(f"Your username is: {username}")
```

Test cases — what should the username be?

| First name | Last name | Fav number | Expected username |
|------------|-----------|------------|-------------------|
| Aisha | Tan | 7 | _______________ |
| Marcus | Lim | 42 | _______________ |
| Priya | Kumar | 99 | _______________ |

---

##### Reflection
- What did I learn today?  _________________________________________________________
- What was confusing?  ___________________________________________________________
- One thing I want to try at home: _________________________________________________

##### Bonus / Stretch Challenge — Palindrome Checker

Write `session04_palindrome.py` that asks for a word and tells the user whether it's a palindrome (reads the same forwards and backwards).

Hint: compare the string to its reverse using `[::-1]`.

```python
word = input("Enter a word: ").________()    # lower case to ignore caps
reversed_word = word[________]
if word == reversed_word:
    print(f"'{word}' IS a palindrome!")
else:
    print(f"'{word}' is NOT a palindrome.")
```

(Don't worry that we haven't formally taught `if` — copy this pattern; we'll explain it next unit.)

Test with: `racecar`, `hello`, `madam`, `python`.

---

### Session 5: Pseudocode & Flowcharts

---

#### SESSION 5 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 5 of 48 |
| **Title** | Pseudocode & Flowcharts |
| **Unit** | Unit 1: Python Foundations & Computational Thinking |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §7 — Algorithm design and problem solving; 0860 Stage 8 — Algorithms |
| **Singapore Alignment** | O-Level 7155 Module 1 — Problem analysis and algorithmic thinking |

##### Learning Objectives
By the end of this session, students will be able to:
1. Write a pseudocode algorithm using the Cambridge keywords `INPUT`, `OUTPUT`, `IF/THEN/ELSE`, `WHILE`, `FOR`.
2. Draw a flowchart using the four standard symbols (oval, parallelogram, rectangle, diamond) with arrows.
3. Translate a pseudocode algorithm into working Python code.
4. Justify, in one or two sentences, why designing before coding produces fewer bugs.

##### Materials Needed
- Laptops with Thonny
- Worksheet: Session 5
- Projector
- A4 unlined paper (2 sheets per student) for flowchart drawing
- Coloured pencils or markers (optional but increases engagement)
- A printed "Flowchart Symbol Key" poster — pinned to wall

##### Procedure

**0–5 min: Warm-Up — "Make a Sandwich"**
Tell the class: "I'm a robot. I do exactly what you tell me. Tell me how to make a peanut butter and jelly sandwich." Take instructions one at a time, **literally**. "Put peanut butter on the bread" — pick up the jar and put the **whole jar** on the bread. Laughter. They quickly realise: you have to be precise. "Open jar. Take spoon. Scoop peanut butter. Spread on bread."

Land the lesson: "Programming is exactly this. The computer is even more literal than I am. **Designing the steps before you code** is what saves you from sandwich disasters."

**5–15 min: Introduction — Pseudocode**
Define pseudocode: "**Pseudo** = fake. **Code** = code. So pseudocode is fake-code — it looks like code but it's written in plain English so a human can read and check it. It's the bridge between an idea and Python."

Show the Cambridge keyword set on the board:

```
INPUT, OUTPUT
IF condition THEN ... ELSE ... ENDIF
WHILE condition ... ENDWHILE
FOR variable ← start TO end ... ENDFOR
SET variable ← value     (assignment)
```

Demonstrate with a simple problem: **Print whether a number is even or odd.**

```
INPUT number
IF number MOD 2 = 0 THEN
    OUTPUT "even"
ELSE
    OUTPUT "odd"
ENDIF
```

Point out: this is **language-independent**. We could turn it into Python, JavaScript, C++, Scratch — all from the same pseudocode. That's why exam boards use it.

**Now flowcharts.** Pin up the symbol key poster:

```
   ╭───────╮
   │ Start │      Oval / terminator: start and end
   ╰───────╯

   ╱─────────╲
  ╱  INPUT n  ╲   Parallelogram: input or output
  ╲___________╱

   ┌──────────┐
   │ total = 0│   Rectangle: process / calculation
   └──────────┘

         ╱╲
        ╱  ╲
       ╱ n? ╲      Diamond: decision (Yes/No)
       ╲    ╱
        ╲  ╱
         ╲╱

   ───→         Arrow: flow direction
```

Translate the even/odd pseudocode into a flowchart on the board, drawing live. Students follow along on paper.

**15–35 min: Guided Practice — Pseudocode → Flowchart → Python**
Take a slightly bigger problem and walk all three stages.

**Problem:** Ask the user for a temperature in Celsius. If it's above 30, print "Hot day". If below 15, print "Cold day". Otherwise print "Pleasant day".

**Stage 1 — Pseudocode** (write together on board):

```
INPUT temperature
IF temperature > 30 THEN
    OUTPUT "Hot day"
ELSE IF temperature < 15 THEN
    OUTPUT "Cold day"
ELSE
    OUTPUT "Pleasant day"
ENDIF
```

**Stage 2 — Flowchart.** Draw on the board with shapes. Have students draw their own copy on A4. Three branches out of the diamond — point out that diamonds typically only have two branches (Yes/No), so a 3-way decision means a diamond inside another branch.

**Stage 3 — Python.** Tell students: "We haven't formally learned `if` yet — you'll see it in Unit 2 — but I'm going to translate now so you can see how clean the path is from pseudocode to code."

```python
# session05_temperature.py
temperature = float(input("Temperature in Celsius: "))

if temperature > 30:
    print("Hot day")
elif temperature < 15:
    print("Cold day")
else:
    print("Pleasant day")
```

Run it. Test with 35 (hot), 10 (cold), 22 (pleasant). Compare line-by-line to the pseudocode. "See how the **shape** is identical? That's the point of design — it makes coding the easy part."

Brief note on why this matters: Cambridge IGCSE 0478 Paper 2 explicitly asks students to "Write an algorithm in pseudocode or as a flowchart." Singapore O-Level 7155 Section A includes problem-decomposition diagrams. Today is exam-relevant.

**35–50 min: Independent Practice — Worksheet**
Direct students to **Worksheet Part 1 (Pseudocode-to-Python translation)**, **Part 2 (Draw flowcharts)**, and **Part 3 (Design then code: Pizza price calculator)**. As you circulate:
- Watch for students skipping straight to Python without finishing the design. Politely send them back: "Show me your pseudocode first, then I'll look at the code."
- Check arrow directions — students often draw arrows backwards into a decision diamond.
- Catch students using `=` instead of `==` in their pseudocode IF condition (lift-over from Python; not technically wrong in pseudocode, but coach them toward `=` as Cambridge writes it).

**50–55 min: Sharing & Discussion**
Pick two students with different but valid flowcharts for the pizza problem. Project them. Ask: "Are they both correct? Why might programmers disagree on a flowchart's shape?" Expect: "Different orders of checks," "Different ways to combine the discounts." Validate — there is rarely one "right" flowchart, only correct vs incorrect.

Discuss: "Was it faster to design first and then code, or jump straight in?" Expect mixed answers. Steer toward: "It feels slower at first, but we made fewer mistakes — and on an exam, the marker awards points for the algorithm even if the code is incomplete."

**55–60 min: Closure & Preview**
Exit-check: "Name the four flowchart symbols." Expected: oval (start/end), parallelogram (I/O), rectangle (process), diamond (decision).

Preview: "Tomorrow is your first **project session**. You'll design and build a Personal Profile App — pseudocode + flowchart + working Python — and present it to the class. Bring a notebook."

Homework: "Tonight, write pseudocode for a simple problem of your choice (e.g. 'tip calculator', 'guess my number'). Don't write Python yet — just pseudocode. We'll review at the start of Session 6."

##### Differentiation

**Support:**
- Provide a printed pseudocode template with the keywords pre-filled.
- Pair students for the flowchart drawing — one drives, one checks.
- Use a "fill-in-the-blank" pseudocode skeleton for Part 3 instead of starting from scratch.

**Extension:**
- Translate Part 3 (pizza calculator) pseudocode into actual Python and run it (using the `if/elif/else` pattern shown in the demo).
- Add a loop to the design: "Keep asking until the user types 'quit'." Use `WHILE` in pseudocode.
- Try drawing the same flowchart in a digital tool like draw.io or Lucidchart and export as PNG.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Pseudocode keywords | Doesn't use keywords | Uses INPUT/OUTPUT only | Uses IF/ELSE and INPUT/OUTPUT | Uses IF/ELSE and at least one WHILE/FOR appropriately |
| Flowchart symbols | Uses one shape only | Uses 2 correct symbols | Uses all 4 symbols correctly | Symbols + arrows + clear flow direction |
| Translation to Python | Cannot translate | Translates with help, syntax errors | Translates pseudocode to working Python | Translates and tests with multiple inputs |
| Design discipline | Skips design, jumps to code | Designs after code | Designs before code, follows the plan | Designs, codes, then refines design based on coding insights |

##### Teacher Notes
- **The "skip the design" temptation** is the biggest pitfall today. Students will whisper "I don't need this, I'll just code it." Insist on the design phase. The whole unit hinges on this habit.
- **Pseudocode dialects vary.** Cambridge uses `←` for assignment, BBC uses `=`, others use `:=`. Pick Cambridge style for this course since both 0478 and 0860 use it. Be consistent.
- **Flowchart fatigue:** drawing flowcharts by hand gets old fast. After Unit 1 we mostly use pseudocode unless an exam-style question demands a flowchart. Reassure students.
- **"Why not just code?":** a sharp student will ask. Genuine answer: for tiny programs you don't need design; for anything bigger than a screen of code, you do. Plus — the exam awards marks for the algorithm, not just for code that runs.
- **Don't over-formalise.** Pseudocode is for humans. If a student writes `READ` instead of `INPUT`, accept it and gently point them at the Cambridge keyword.

---

#### SESSION 5 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 5: Pseudocode & Flowcharts**

---

##### Part 1: Pseudocode-to-Python Translation

Translate each pseudocode block to Python. Type each into Thonny and run.

**1A — Greet by name**

```
INPUT name
OUTPUT "Hello, " + name
```

Python:

```python
________ = input("________________")
print("________________" + ________)
```

---

**1B — Square a number**

```
INPUT number
SET result ← number * number
OUTPUT result
```

Python:

```python
________ = ________(input("________________"))
________ = ________ * ________
print(________)
```

---

**1C — Even or odd**

```
INPUT n
IF n MOD 2 = 0 THEN
    OUTPUT "even"
ELSE
    OUTPUT "odd"
ENDIF
```

Python (we haven't formally taught `if` yet — copy carefully):

```python
n = int(input("Enter a number: "))
if n % 2 == 0:
    print("even")
else:
    print("odd")
```

Test with 4, 7, 0, -3. Did all four behave correctly? ☐ Yes ☐ No

---

##### Part 2: Draw Flowcharts

On the back of this sheet (or on a fresh A4), draw flowcharts for the following. Use:

- **Oval** for Start / End
- **Parallelogram** for INPUT / OUTPUT
- **Rectangle** for processes (calculations, assignments)
- **Diamond** for decisions

**2A — Greet by name** (the simplest flowchart — just 4 shapes).

**2B — Even or odd** (one diamond decision; two output paths).

**2C — Largest of two numbers**:
```
INPUT a, b
IF a > b THEN
    OUTPUT a
ELSE
    OUTPUT b
ENDIF
```

Tick when complete: 2A ☐  2B ☐  2C ☐

---

##### Part 3: Design Then Code — Pizza Price Calculator

A pizza shop charges:
- Small pizza: $8
- Medium pizza: $12
- Large pizza: $16

If the user orders 3 or more pizzas, they get a 10% discount on the total.

**Step 1 — Pseudocode** (write here, do not skip!):

```
INPUT ____________________________________
INPUT ____________________________________

IF size = "small" THEN
    SET price ← ________
ELSE IF size = "medium" THEN
    SET price ← ________
ELSE
    SET price ← ________
ENDIF

SET total ← ________ * ________

IF ________________________ THEN
    SET total ← total * ________
ENDIF

OUTPUT total
```

**Step 2 — Flowchart** (draw on A4, attach to this sheet).

**Step 3 — Python** (filename `session05_pizza.py`). Type and run.

```python
size = input("Size (small/medium/large): ").lower()
quantity = int(input("How many pizzas? "))

if size == "small":
    price = 8
elif size == "medium":
    price = 12
else:
    price = 16

total = price * quantity

if quantity >= 3:
    total = total * 0.9   # 10% discount

print(f"Total: ${total}")
```

Test cases:

| Size | Quantity | Expected total |
|------|----------|----------------|
| small | 2 | $16 |
| medium | 3 | $32.40 |
| large | 5 | $72.00 |

---

##### Reflection
- What did I learn today?  _________________________________________________________
- What was confusing?  ___________________________________________________________
- One thing I want to try at home: _________________________________________________

##### Bonus / Stretch Challenge — Loop in Pseudocode

Design (pseudocode + flowchart) a program that:

1. Asks the user to guess a secret number (the secret is 7).
2. Keeps asking **WHILE** the guess is wrong.
3. When they guess right, prints "Correct!".

Hint:

```
SET secret ← 7
INPUT guess
WHILE guess ≠ secret
    OUTPUT "Wrong, try again"
    INPUT guess
ENDWHILE
OUTPUT "Correct!"
```

Try the flowchart. The diamond loops back up — that's how a `WHILE` looks visually.

---

### Session 6: Project 1 — Personal Profile App

---

#### SESSION 6 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 6 of 48 |
| **Title** | Project 1 — Personal Profile App |
| **Unit** | Unit 1: Python Foundations & Computational Thinking |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §7 + §8 — Algorithm design and program implementation; 0860 Stage 8 — Programming project |
| **Singapore Alignment** | O-Level 7155 Module 4 + Module 1 — Problem solving end-to-end; CFF Secondary Python project rubric |

##### Learning Objectives
By the end of this session, students will be able to:
1. Plan a small program by writing pseudocode and drawing a flowchart **before** writing any Python.
2. Implement a multi-step interactive program that uses input, casting, arithmetic, string methods, and f-strings.
3. Format console output as a clear, presentable "card" using string formatting.
4. Give and receive structured peer feedback using a project rubric.

##### Materials Needed
- Laptops with Thonny
- Worksheet: Session 6 (project planning template + checklist + peer rubric)
- Projector
- A4 paper for flowcharts
- Optional: a printed "showcase" border template students can copy to make their card output look like an ID card
- Sticky notes (3 per student) for the showcase peer-feedback step

##### Procedure

**0–5 min: Warm-Up — Homework Review**
Take 3 volunteers from last session's homework (their personal pseudocode). Quickly project and have the class spot one strength and one improvement for each. Do **not** linger — this is a 5-minute energiser, not a lesson.

Then announce: "Today is your first project. By the end of the hour, you will have designed, built, and presented a Personal Profile App. Let's go."

**5–15 min: Introduction — Project Brief & Demo**
Show the finished example on the projector. Run the teacher's reference solution:

```
============================
  PERSONAL PROFILE: AISHA
============================
  Age:           12
  Favourite #:   7
  Fav. Food:     SUSHI
  Dream Job:     Game Designer
----------------------------
  In 10 years you will be 22 years old.
  Your favourite # squared is 49.
  Username suggestion: aissus7
============================
```

Students will instantly want to make their own. Good. Now hand out the **project brief**:

> **Personal Profile App** — Build a Python program that asks the user 5 or more questions (name, age, favourite number, favourite food, dream job — and any extras you like). Use what you've learned in Unit 1: variables, casting, arithmetic, string methods, f-strings. Output a presentable "card" with at least 3 calculated facts (e.g. age in 10 years, favourite number squared, a generated username).

Show the rubric briefly (full version on the worksheet):

| Area | What the marker looks for |
|------|---------------------------|
| Design | Pseudocode + flowchart present and match the code |
| Inputs | At least 5 inputs, all cast appropriately |
| Processing | At least 3 calculated/derived values |
| Output | Card-style format using f-strings; readable and aligned |
| Code quality | snake_case names, comments, no dead code |

Tell students: "You will get 15 minutes to design, 25 minutes to build, and we'll spend the last 15 sharing." Time pressure focuses minds.

**15–35 min: Guided Practice — Design and Build**
**Phase A: Design (15–25 min, 10 min).** Students fill in **Worksheet Part 1 (planning template)**: pseudocode and flowchart. Insist nobody opens Thonny yet. Walk and check designs:
- Does the pseudocode list **at least 5 INPUTs**?
- Is each input cast appropriately (e.g. age → int, favourite number → int)?
- Are there **at least 3 calculations**? (e.g. age + 10, fav_number ** 2, username = first_name[:3] + ...)
- Is the OUTPUT formatted as a card?

**Phase B: Build (25–35 min, 10 min — but really we extend through Independent Practice).** When a student's design is approved, give them a green tick on the worksheet and they may open Thonny. They create `session06_profile.py` and start coding from their pseudocode. They have **template starter code** in the worksheet (Part 2) to keep them moving.

Live-coach as students build:
- "Read your pseudocode line. Now write it in Python. Read the next line. Now write it." This rhythm is the whole point.
- If a student gets a TypeError, ask: "Did you cast the input?" 9 times out of 10 that's it.
- If their card looks plain, suggest f-string padding: `f"  Age: {age:>15}"`.

**35–50 min: Independent Practice — Build & Test**
Students continue building. Most will be in mid-build at this point. Encourage testing with their own data and one fictitious profile (to check that arithmetic and string methods work for any input).

Common bugs to catch as you circulate:
- Building a username from `first_name[:3]` but the name was entered with a capital letter — output looks like `Aisus7` instead of `aissus7`. Coach `.lower()`.
- f-string with no `f` prefix — braces print literally.
- Forgetting `.strip()` on `input()` for the name — extra spaces look ugly in the card.
- Hard-coded values: a student types `print("In 10 years you will be 22")` instead of computing it. Catch them: "What if I'm 11? Will it still say 22?"

**50–55 min: Sharing & Discussion**
**The Showcase.** Each student stands and presents their card output to the class (30 seconds each — keep it tight). The class watches and uses sticky notes to write **one strength + one suggestion** for at least 3 peers. Stick the notes on the presenter's desk.

If time allows, prompt one student: "Talk us through your pseudocode and how it became code." This reinforces design-first.

Anticipated student responses to "what was tricky?": "Getting the discount maths right," "I forgot to cast my favourite number and got a TypeError," "My card looked messy until I used `:>15`."

**55–60 min: Closure & Preview**
Exit-check: students self-assess their project against the rubric on the worksheet — tick the boxes. Submit (paper or upload `.py` file to shared folder).

Preview Unit 2: "We've built our toolbox: variables, types, input, strings, design. Next unit we add **decisions** — making the program do different things based on what the user types. We'll build a quiz that scores itself. See you Session 7."

Homework (optional): polish the project. Add a 6th input. Try the bonus challenge on the worksheet.

##### Differentiation

**Support:**
- Provide a fully fleshed-out pseudocode template with `INPUT name`, `INPUT age`, etc. pre-written; students fill in the calculations only.
- Provide starter Python with `input()` and `print()` lines done; student writes only the calculations and the f-strings.
- Allow pair-projects with shared marking — one drives the keyboard, one drives the design.

**Extension:**
- Add a 7th input that triggers a small conditional output (e.g. if age >= 13, print "You're a teenager!"). This previews Unit 2.
- Use multi-line f-strings with triple quotes to make a really fancy card.
- Save the profile to a text file using `with open(...)` — preview of Unit 6. (Only for genuinely advanced students; do not mainstream.)

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Design artefacts | No pseudocode/flowchart | Pseudocode only or flowchart only | Both present, mostly match code | Both present, fully match code, clean |
| Input handling | <3 inputs or no casting | 3–4 inputs, partial casting | 5+ inputs, all cast appropriately | 5+ inputs with `.strip()`, casting, and clear prompts |
| Processing/calculations | No calculations | 1 calculation | 2 calculations using Unit 1 tools | 3+ calculations using arithmetic AND string methods |
| Output formatting | Plain `print(...)` only | f-strings used, no card layout | f-strings with card-style framing | f-strings with alignment, decoration, professional layout |
| Code quality | Unreadable, no names | Some snake_case, no comments | snake_case, basic comments | Consistent style, header comment, meaningful names |

##### Teacher Notes
- **15 minutes for design feels long.** Some students will fidget. Hold the line — the design phase is the entire pedagogical point of Unit 1's project.
- **Approval gate.** Do not let anyone start coding before you (or a delegated peer assistant) has ticked their pseudocode. This is the single best classroom-management move for project sessions.
- **Showcases are scary** for some kids. Offer the option of "I'll demo on your laptop with you sitting next to me" to anxious students.
- **Save copies.** Have students upload `.py` to a shared folder OR email to themselves. Lost work after a project session is morale-crushing.
- **Rubric grading.** Don't grade in front of the class. Take the worksheets home, return them with comments at the start of Session 7.
- **Celebrate.** This is the first finished project of 8. Acknowledge the milestone — clap, sticker, photo of the showcase board, anything. Sets the tone for the rest of the course.

---

#### SESSION 6 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 6: Project 1 — Personal Profile App**

---

##### Part 1: Project Planning Template

**Step 1 — List your inputs (at least 5).**

| # | Question to ask | Variable name | Type after casting |
|---|-----------------|---------------|--------------------|
| 1 | _______________________________ | _______________ | _________ |
| 2 | _______________________________ | _______________ | _________ |
| 3 | _______________________________ | _______________ | _________ |
| 4 | _______________________________ | _______________ | _________ |
| 5 | _______________________________ | _______________ | _________ |
| 6 (bonus) | __________________________ | _______________ | _________ |

---

**Step 2 — List your calculations (at least 3).**

| # | Description | Pseudocode | Python preview |
|---|-------------|------------|----------------|
| 1 | _______________________________ | ____________________________ | ____________________________ |
| 2 | _______________________________ | ____________________________ | ____________________________ |
| 3 | _______________________________ | ____________________________ | ____________________________ |

---

**Step 3 — Pseudocode** (write the full algorithm):

```
INPUT ____________________________________
INPUT ____________________________________
INPUT ____________________________________
INPUT ____________________________________
INPUT ____________________________________

SET ____________ ← ____________________________________
SET ____________ ← ____________________________________
SET ____________ ← ____________________________________

OUTPUT "===================="
OUTPUT "  PROFILE: " + ____________
OUTPUT "===================="
OUTPUT "  Age: " + ____________
OUTPUT "  ...etc."
OUTPUT "===================="
```

---

**Step 4 — Flowchart** (draw on A4 paper and attach).

Tick when shown to teacher and approved: ☐ **Approved by teacher — OK to code!**

---

##### Part 2: Build Your Profile App (`session06_profile.py`)

Starter template — fill in the blanks, then expand.

```python
# ==========================================
#  Personal Profile App
#  Author: ______________________
#  Date:   ______________________
# ==========================================

# --- Inputs ---
name        = input("Your name: ").________()
age         = ________(input("Your age: "))
fav_number  = ________(input("Your favourite number: "))
fav_food    = input("Your favourite food: ").________()
dream_job   = input("Your dream job: ").________()

# --- Calculations ---
age_in_10   = ________ + 10
fav_squared = ________ ** 2
username    = (________[:3] + ________[:2] + ________).lower()

# --- Output card ---
print("=" * 30)
print(f"  PERSONAL PROFILE: {________.upper()}")
print("=" * 30)
print(f"  Age:           {________}")
print(f"  Favourite #:   {________}")
print(f"  Fav. Food:     {________.upper()}")
print(f"  Dream Job:     {________}")
print("-" * 30)
print(f"  In 10 years you will be {________} years old.")
print(f"  Your favourite # squared is {________}.")
print(f"  Username suggestion: {________}")
print("=" * 30)
```

Tick the build checklist as you go:

| Checkpoint | Done? |
|------------|-------|
| All 5+ inputs work and cast cleanly | ☐ |
| `.strip()` used on text inputs | ☐ |
| At least 3 calculations | ☐ |
| At least 1 string-method calculation (e.g. username) | ☐ |
| Output uses f-strings with `{}` | ☐ |
| Output looks card-shaped (lines of `=` or `-`) | ☐ |
| File saved as `session06_profile.py` | ☐ |
| Header comment with my name | ☐ |
| No red errors when I run it | ☐ |

---

##### Part 3: Self-Assessment Rubric

Tick the level you think you achieved.

| Criterion | 0 — Not yet | 1 — Developing | 2 — Proficient | 3 — Mastery |
|-----------|:-----------:|:--------------:|:--------------:|:-----------:|
| Design artefacts | ☐ | ☐ | ☐ | ☐ |
| Input handling (5+, cast) | ☐ | ☐ | ☐ | ☐ |
| Processing (3+ calculations) | ☐ | ☐ | ☐ | ☐ |
| Output formatting (card, f-strings) | ☐ | ☐ | ☐ | ☐ |
| Code quality (names, comments) | ☐ | ☐ | ☐ | ☐ |

My total: ____ / 15

---

##### Peer-Review Rubric

Get **two** classmates to review your project. They write their name and tick the level for each criterion.

**Reviewer 1 name:** _______________________

| Criterion | 0 | 1 | 2 | 3 |
|-----------|:-:|:-:|:-:|:-:|
| Design | ☐ | ☐ | ☐ | ☐ |
| Inputs | ☐ | ☐ | ☐ | ☐ |
| Processing | ☐ | ☐ | ☐ | ☐ |
| Output | ☐ | ☐ | ☐ | ☐ |
| Code quality | ☐ | ☐ | ☐ | ☐ |

One thing I love about this project: __________________________________________________

One suggestion to make it even better: ________________________________________________

---

**Reviewer 2 name:** _______________________

| Criterion | 0 | 1 | 2 | 3 |
|-----------|:-:|:-:|:-:|:-:|
| Design | ☐ | ☐ | ☐ | ☐ |
| Inputs | ☐ | ☐ | ☐ | ☐ |
| Processing | ☐ | ☐ | ☐ | ☐ |
| Output | ☐ | ☐ | ☐ | ☐ |
| Code quality | ☐ | ☐ | ☐ | ☐ |

One thing I love about this project: __________________________________________________

One suggestion to make it even better: ________________________________________________

---

##### Reflection
- What did I learn building this project? _____________________________________________
- What was the hardest part? _________________________________________________________
- What would I add if I had another hour? ____________________________________________
- One thing I want to try at home: ___________________________________________________

##### Bonus / Stretch Challenge — Conditional Card

Add ONE conditional message to your card based on age (you may copy this pattern even though we haven't formally taught `if` yet — that's Unit 2):

```python
if age < 13:
    print("  Status:        TWEEN")
elif age < 18:
    print("  Status:        TEEN")
else:
    print("  Status:        ADULT")
```

Re-run with three different ages and verify all three branches display correctly. ☐

---
