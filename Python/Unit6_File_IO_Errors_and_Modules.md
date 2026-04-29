# Python Programming for Kids: Lesson Plans & Worksheets
## Unit 6: File I/O, Errors & Built-in Modules (Sessions 31–36)

### Unit Overview
Unit 6 transforms students from "programs that forget" into "programs that remember." Across six 60-minute sessions, learners read and write text files with the safe `with open(...)` idiom, defensively handle errors using `try`/`except`, and harness Python's standard library — `random`, `math`, and `datetime` — to write shorter, smarter, more realistic programs. The unit directly addresses Cambridge IGCSE 0478 §10 (file handling, library routines, MOD/DIV/ROUND) and Singapore O-Level 7155 Module 4 (built-in functions, structured data persistence). It closes with a project-based capstone: a fully functional console **Journal Application** that persists entries between runs, supports searching and filtering, and gracefully recovers from missing files.

---

### Session 31: Reading from Text Files

---

#### SESSION 31 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 31 of 48 |
| **Title** | Reading from Text Files |
| **Unit** | Unit 6: File I/O, Errors & Built-in Modules |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — file handling (read text files); Lower Secondary 0860 strand 3.4 — input/output beyond the keyboard |
| **Singapore Alignment** | O-Level 7155 Module 4 — built-in functions; reading external data |

##### Learning Objectives (SMART)
By the end of the session, students will be able to:
1. **Open** a text file in read mode using the `with open(filename, "r") as f:` idiom and explain in one sentence why `with` is safer than a bare `open()`.
2. **Compare** the four reading patterns — `f.read()`, `f.readline()`, `f.readlines()`, and `for line in f:` — and choose the most appropriate one for at least three different scenarios.
3. **Apply** `.strip()` correctly to remove trailing newline characters and predict the output of read operations on a given sample file with at least 80% accuracy.
4. **Build** a working "favourite-quotes" reader program that prints all lines of a file numbered 1, 2, 3, … and counts the total number of lines.

##### Materials Needed
- Thonny IDE (Python 3.11+) installed on each student laptop
- Sample data file `students.txt` (provided below) pre-placed in each student's working folder
- Sample data file `quotes.txt` (provided below)
- Printed Worksheet 31 (one per student)
- Projector for live coding
- Whiteboard for the "memory vs. file" anchor diagram

**Sample file 1 — `students.txt`** (place in same folder as the student's `.py` file):
```
Aisha Tan
Bryan Lim
Chloe Goh
Daniel Wong
Eunice Sim
Faizal Rahman
Grace Ng
Hadi Yusof
```

**Sample file 2 — `quotes.txt`**:
```
The only way to learn a new programming language is by writing programs in it. — Dennis Ritchie
First, solve the problem. Then, write the code. — John Johnson
Talk is cheap. Show me the code. — Linus Torvalds
Programs must be written for people to read. — Harold Abelson
Simplicity is the soul of efficiency. — Austin Freeman
```

##### Procedure

**0–5 min: Warm-Up — "What does your program forget?"**
Teacher asks: "Yesterday you wrote a quiz program. You closed Thonny. Today you open it again. Does it remember the high score?" Take three answers. Reveal: "No — variables live only in RAM. When the program ends, they vanish. Today we learn how to make programs that **remember**."

Quick anchor sketch on the whiteboard:
```
RAM   (forgets when program ends)  →  variables, lists, dicts
DISK  (remembers forever)          →  files (.txt, .csv, .json)
```

**5–15 min: Introduction — Opening and Reading Files**

Live-code with narration:

```python
# The simplest possible read
f = open("students.txt", "r")   # "r" = read mode
contents = f.read()
print(contents)
f.close()                       # MUST close, or file may be locked
```

Teacher: "This works… but if `f.read()` crashes, `f.close()` never runs. The file stays locked. We need a safer way."

Introduce the `with` statement:

```python
# The SAFE idiom — auto-closes even if something goes wrong
with open("students.txt", "r") as f:
    contents = f.read()
print(contents)   # f is automatically closed here
```

Explain mode strings on the board:
| Mode | Meaning |
|------|---------|
| `"r"` | Read (default) — file must exist |
| `"w"` | Write — overwrites existing file! |
| `"a"` | Append — adds to end of file |
| `"r+"` | Read and write |

**15–35 min: Guided Practice — Four Ways to Read**

Demo each, projecting Thonny:

**(1) `f.read()` — everything as one big string:**
```python
with open("students.txt", "r") as f:
    text = f.read()
print(type(text))   # <class 'str'>
print(len(text))    # number of characters, including \n
```

**(2) `f.readline()` — one line at a time:**
```python
with open("students.txt", "r") as f:
    first  = f.readline()
    second = f.readline()
    third  = f.readline()
print(first)   # "Aisha Tan\n"  ← note the \n
print(second)  # "Bryan Lim\n"
```

**(3) `f.readlines()` — a list of lines:**
```python
with open("students.txt", "r") as f:
    lines = f.readlines()
print(lines)
# ['Aisha Tan\n', 'Bryan Lim\n', 'Chloe Goh\n', ...]
print(lines[0])
print(len(lines), "students")
```

**(4) `for line in f:` — the Pythonic way (memory-friendly):**
```python
with open("students.txt", "r") as f:
    for line in f:
        print(line)        # double-spaced! Why?
```

Pause. Ask: "Why are the names double-spaced?" Elicit: "Each line already ends with `\n`, then `print` adds another."

The fix — `.strip()`:
```python
with open("students.txt", "r") as f:
    for line in f:
        clean = line.strip()
        print(clean)       # single-spaced, clean
```

**Numbering the output (mini-walkthrough):**
```python
with open("students.txt", "r") as f:
    for number, line in enumerate(f, start=1):
        print(f"{number}. {line.strip()}")
```
Expected output:
```
1. Aisha Tan
2. Bryan Lim
3. Chloe Goh
4. Daniel Wong
5. Eunice Sim
6. Faizal Rahman
7. Grace Ng
8. Hadi Yusof
```

**Counting lines (a common interview question):**
```python
count = 0
with open("students.txt", "r") as f:
    for line in f:
        count += 1
print("Total students:", count)
```

**35–50 min: Independent Practice — Worksheet**
Distribute Worksheet 31. Students complete Parts 1–3 individually using `students.txt` and `quotes.txt`. Teacher circulates, watching for the two main bugs:
1. Forgetting `.strip()` → double spacing
2. Calling `f.read()` then `f.readlines()` on the same handle → second call returns empty (cursor already at end-of-file)

**50–55 min: Sharing & Discussion**
Two volunteers project their Quote Reader. Class discusses: "When would `readlines()` be a bad choice?" (huge files — loads everything into memory). "When would `for line in f:` be best?" (large files, line-by-line processing).

**55–60 min: Closure & Preview**
Exit ticket on a sticky note: *"Write one sentence: what does `with open(...) as f:` do that plain `open(...)` does not?"* Preview: "Tomorrow — writing files. And the scariest mode of all: `'w'`."

##### Differentiation

**Support:**
- Pre-write the `with open(...)` template on a printed reference card.
- Pair with a stronger peer for Part 3 of the worksheet.
- Provide a smaller, 3-line `students.txt` for predict-the-output exercises.

**Extension:**
- Read the file backwards — print line 8, then 7, then 6… (hint: `reversed()` or list slicing).
- Print only students whose names start with a vowel.
- Print the longest name in the file using `max(lines, key=len)`.
- Read both `students.txt` and `quotes.txt` and report which file has more total characters.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Use of `with` idiom** | Uses bare `open()` without `close()` | Uses `open()` + `close()` correctly | Uses `with open()` consistently | Uses `with`, can explain auto-close in own words |
| **Choosing read method** | Confused about which to use | Uses `read()` for everything | Picks correct method for each scenario | Justifies choice with memory/clarity reasoning |
| **`.strip()` handling** | Output has double spaces | Strips inconsistently | Always strips, output clean | Strips and explains why `\n` exists |
| **Quote-reader program** | Program does not run | Runs but skips lines or crashes | Reads and prints all lines correctly | Numbered, counted, with friendly summary |

##### Teacher Notes
- The single biggest gotcha today is the **invisible `\n`**. Print `repr(line)` once on the board so students literally see the `\n` characters.
- After `f.read()`, the file pointer is at end-of-file; a second read returns `''`. Demonstrate this — many students will hit it on the worksheet.
- File paths: Thonny's working directory is the folder of the saved `.py` file. If students see `FileNotFoundError`, check that they (a) saved their script and (b) put the data file in the **same folder**.
- Do not introduce `try`/`except` yet — that is Session 33. Keep error messages as natural learning moments today.
- Mac/Linux students may see `\r\n` vs `\n` differences if files were authored on Windows. Use `.strip()` (which removes both) rather than `.rstrip("\n")`.

---

#### SESSION 31 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Predict the Output

You have the file `students.txt` with these eight lines:
```
Aisha Tan
Bryan Lim
Chloe Goh
Daniel Wong
Eunice Sim
Faizal Rahman
Grace Ng
Hadi Yusof
```

Predict what each program prints. Write your answer in the box, then run it in Thonny and circle ✅ or ✏️ (correction).

**Q1.**
```python
with open("students.txt", "r") as f:
    print(f.readline())
```
Prediction: ____________________________________________ ✅ / ✏️

**Q2.**
```python
with open("students.txt", "r") as f:
    print(f.readline().strip())
    print(f.readline().strip())
```
Prediction: ____________________________________________ ✅ / ✏️

**Q3.**
```python
with open("students.txt", "r") as f:
    lines = f.readlines()
print(len(lines))
```
Prediction: ____________________________________________ ✅ / ✏️

**Q4.**
```python
with open("students.txt", "r") as f:
    text = f.read()
    again = f.read()
print(repr(again))
```
Prediction: ____________________________________________ ✅ / ✏️

**Q5.**
```python
with open("students.txt", "r") as f:
    for line in f:
        if "a" in line.lower():
            print(line.strip())
```
Prediction (list the names):
________________________________________________________

##### Part 2: Count the Lines

Write a program `count_students.py` that:
1. Opens `students.txt` for reading using the `with` idiom.
2. Uses a `for` loop to count every line.
3. Prints exactly: `There are N students in the file.`

Sketch your code below, then type it into Thonny and test it:

```python
# count_students.py





```

What number did your program print? **N = ______**

Now manually copy `students.txt` and add three more names. Run the program again. New count: **N = ______**

##### Part 3: The Favourite-Quotes Reader

Build a program `quote_reader.py` that:
1. Opens `quotes.txt`.
2. Prints every quote on its own line, **numbered** like this:
   ```
   Quote 1: The only way to learn a new programming language is by writing programs in it. — Dennis Ritchie
   Quote 2: First, solve the problem. Then, write the code. — John Johnson
   ...
   ```
3. After printing, displays: `(N quotes total)`.
4. Uses `.strip()` so output has no extra blank lines.

Write your code below:

```python
# quote_reader.py





```

**Test it.** Then add this stretch feature: prompt the user with `"Show only quotes containing which word? "` and print only the quotes that contain that word (case-insensitive).

```python
# Stretch addition





```

##### Reflection

1. In your own words, why do we use `with open(...)` instead of just `open(...)`?
   _________________________________________________________________________
   _________________________________________________________________________

2. What does `.strip()` actually remove? When have you needed it today?
   _________________________________________________________________________
   _________________________________________________________________________

3. Of the four read methods (`read`, `readline`, `readlines`, `for line in f:`), which feels most natural to you, and why?
   _________________________________________________________________________
   _________________________________________________________________________

##### Bonus / Stretch Challenge

Create a file `numbers.txt` containing one integer per line, e.g.:
```
12
45
7
89
3
56
```
Write a program that reads the file and prints:
- the **sum** of all numbers
- the **average** (rounded to 2 decimal places)
- the **largest** number
- the **smallest** number

Hint: you'll need `int(line.strip())` to convert each line from string to integer.

```python
# numbers_stats.py





```

---

### Session 32: Writing to Text Files

---

#### SESSION 32 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 32 of 48 |
| **Title** | Writing to Text Files |
| **Unit** | Unit 6: File I/O, Errors & Built-in Modules |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — file handling (write text files), append vs overwrite |
| **Singapore Alignment** | O-Level 7155 Module 4 — output to file, structured data |

##### Learning Objectives (SMART)
1. **Distinguish** between `"w"` (write/overwrite) and `"a"` (append) modes and predict the resulting file contents in at least 4 of 5 scenarios.
2. **Use** `f.write()` and `f.writelines()` correctly, including explicit `\n` newlines, to produce files matching a given specification.
3. **Diagnose** and **fix** an "overwrite bug" in a peer's code where data was unintentionally lost.
4. **Build** a working "to-do list" file writer that adds new items to a persistent `tasks.txt` across multiple program runs.

##### Materials Needed
- Thonny IDE (Python 3.11+)
- Empty working folder per student (so files appear cleanly)
- Printed Worksheet 32
- Projector
- Anchor poster: **"`'w'` ERASES. `'a'` ADDS."** (large, colourful)

##### Procedure

**0–5 min: Warm-Up — "Whiteboard Disaster"**
Teacher draws a packed whiteboard ("Yesterday's lesson notes"). Then takes an eraser and wipes the entire board in one stroke. "If your program opens a file in `'w'` mode, **this** is what happens to whatever was inside. Today, we learn the difference between `'w'` (eraser) and `'a'` (extra paper)."

**5–15 min: Introduction — Three Modes Side by Side**

Project the table and code:

```python
# Mode "r" — read only, file must already exist
with open("notes.txt", "r") as f:
    text = f.read()

# Mode "w" — WRITE: creates new file OR ERASES existing one
with open("notes.txt", "w") as f:
    f.write("Hello!\n")          # everything previous is gone

# Mode "a" — APPEND: creates if missing, otherwise adds to the end
with open("notes.txt", "a") as f:
    f.write("Another line.\n")
```

Live demo: write a 3-line file, view it, re-open in `"w"`, write one line, view it again — three lines now gone. Audible gasps are normal.

**The newline gotcha:**
```python
with open("greetings.txt", "w") as f:
    f.write("Hello")
    f.write("World")
    f.write("Goodbye")
```
Open the resulting file. It contains: `HelloWorldGoodbye` — all on one line. `print()` adds `\n` automatically; **`write()` does NOT**.

Fix:
```python
with open("greetings.txt", "w") as f:
    f.write("Hello\n")
    f.write("World\n")
    f.write("Goodbye\n")
```

**15–35 min: Guided Practice — Building Real Files**

**Demo 1 — Save a quiz score:**
```python
name  = input("Your name: ")
score = int(input("Your score: "))

with open("scores.txt", "a") as f:    # append, so we don't erase old scores
    f.write(f"{name},{score}\n")

print("Score saved!")
```
Run the program three times with different names. Open `scores.txt`. Three lines, perfect.

**Demo 2 — `f.writelines()` for a list:**
```python
shopping = ["Eggs\n", "Milk\n", "Bread\n", "Apples\n"]

with open("shopping.txt", "w") as f:
    f.writelines(shopping)        # NOTE: writelines does NOT add \n
```
Common mistake — students forget the `\n`:
```python
shopping = ["Eggs", "Milk", "Bread"]   # MISSING \n
with open("shopping.txt", "w") as f:
    f.writelines(shopping)
# Result: EggsMilkBread (one line!)
```
Show the fixed version with a list comprehension:
```python
shopping = ["Eggs", "Milk", "Bread"]
with open("shopping.txt", "w") as f:
    f.writelines(item + "\n" for item in shopping)
```

**Demo 3 — A simple log file with a timestamp string:**
(We won't use the `datetime` module yet — that's Session 35 — so we use a manual stamp.)
```python
def log(message):
    with open("activity.log", "a") as f:
        f.write(f"[Session 32] {message}\n")

log("Program started")
log("User pressed start")
log("Score saved: 47")
log("Program ended")
```
Open `activity.log` — four entries. Run again — eight entries. Append works.

**Round-trip — write then read:**
```python
# Step 1: write
with open("colors.txt", "w") as f:
    for c in ["red", "green", "blue", "yellow"]:
        f.write(c + "\n")

# Step 2: read it back
with open("colors.txt", "r") as f:
    for line in f:
        print("Color:", line.strip())
```

**35–50 min: Independent Practice — Worksheet**
Students complete Parts 1–3. The to-do list builder (Part 3) is the centerpiece — emphasize that the file must persist across runs (so use `"a"`, not `"w"`).

**50–55 min: Sharing & Discussion**
Show one student's `tasks.txt` opened in a text editor. Ask: "What happens if I delete this file by mistake? Does the program crash?" Yes — `FileNotFoundError`. Foreshadow Session 33: "Tomorrow we learn how to **handle** errors."

**55–60 min: Closure & Preview**
Exit ticket: *"Your friend's program keeps deleting their game's high-score table. Which letter did they use, and which letter should they use?"* Preview: "Tomorrow — when files don't exist, when input isn't a number, when programs crash. We learn `try` and `except`."

##### Differentiation

**Support:**
- Provide a "fill-in-the-blanks" template for the to-do list writer.
- Pre-create `tasks.txt` with two example tasks so the file already exists.
- Reinforce the visual: **`'w'` = whiteboard eraser; `'a'` = extra paper**.

**Extension:**
- Number the tasks as they are saved (`1. Buy milk`, `2. Walk dog`, …). Hint: count current lines first.
- Add a "delete task by number" feature — read all lines, skip the chosen one, rewrite with `"w"`.
- Save tasks with a status flag: `[ ] Buy milk` vs. `[x] Buy milk`.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Mode selection** | Uses wrong mode, loses data | Uses correct mode after teacher hint | Picks `'w'`/`'a'` correctly first try | Justifies choice and warns about pitfalls |
| **Newline handling** | Output is one long blob | Some lines run together | All lines properly separated | Uses `\n` consistently and explains why |
| **`writelines` use** | Cannot use it | Uses but forgets newlines | Uses with newlines added | Uses with comprehension or generator |
| **To-do list app** | Does not save | Saves but overwrites old tasks | Saves and persists across runs | Persists, numbers, displays, and handles empty file |

##### Teacher Notes
- This is the most data-loss-prone session in the unit. Have students **save their `.py` file in a fresh folder** so an accidental `"w"` doesn't nuke something important.
- The newline gotcha is universal — prepare to demo it twice.
- Students often confuse `writelines` with "writes lines for me with newlines added." It does not. Be emphatic.
- If a student's `tasks.txt` keeps getting wiped, they're using `"w"` — and they're using it inside a loop or function called multiple times. Help them see the pattern.
- This is also a good moment to reinforce filename conventions: lowercase, no spaces, descriptive (`scores.txt` ✓, `My Awesome File.TXT` ✗).

---

#### SESSION 32 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Predict-the-File-Contents

For each program, predict what will be inside `data.txt` **after** the program finishes. Assume `data.txt` starts as the file containing:
```
Apple
Banana
Cherry
```

**Q1.**
```python
with open("data.txt", "w") as f:
    f.write("Date\n")
```
Final contents of `data.txt`:
________________________________________________________

**Q2.**
```python
with open("data.txt", "a") as f:
    f.write("Date\n")
```
Final contents of `data.txt`:
________________________________________________________

**Q3.**
```python
with open("data.txt", "a") as f:
    f.write("Date")
    f.write("Eggplant")
```
Final contents of `data.txt` (be careful with newlines!):
________________________________________________________

**Q4.**
```python
fruits = ["Date", "Eggplant", "Fig"]
with open("data.txt", "w") as f:
    f.writelines(fruits)
```
Final contents of `data.txt`:
________________________________________________________

**Q5.**
```python
fruits = ["Date\n", "Eggplant\n", "Fig\n"]
with open("data.txt", "a") as f:
    f.writelines(fruits)
```
Final contents of `data.txt`:
________________________________________________________

##### Part 2: Fix the Overwrite Bug

A student wrote a "save high score" program. Each time they play the game, they call `save_score()`. They are very upset because **only the most recent score is ever in the file**. Find and fix the bug.

```python
# BUGGY VERSION
def save_score(name, score):
    with open("highscores.txt", "w") as f:
        f.write(f"{name}: {score}\n")

save_score("Aisha", 1200)
save_score("Bryan",  950)
save_score("Chloe", 1500)
```

After all three calls, `highscores.txt` contains only:
```
Chloe: 1500
```

**(a)** What is the bug? (one sentence)
_________________________________________________________________________

**(b)** Write the **fixed** version below:

```python
def save_score(name, score):




```

**(c)** After the fix, what should `highscores.txt` contain after all three calls?
```


```

##### Part 3: To-Do List File Writer

Build a program `todo.py` that:

1. Greets the user.
2. Reads the existing `tasks.txt` (if it has any tasks) and shows them numbered.
3. Asks "Add a new task? (y/n): "
4. If `y`, asks "What is the task? " and **appends** it to `tasks.txt` with a trailing newline.
5. Loops back to step 3 until the user says `n`.
6. Says goodbye and shows the final list.

Use `"a"` mode so the file remembers tasks **across program runs**.

```python
# todo.py








```

**Test plan** (tick when done):
- [ ] First run: add 3 tasks. Open `tasks.txt` in Thonny — see 3 lines.
- [ ] Second run (program reopens): see the 3 tasks listed at the start.
- [ ] Add 2 more. Quit. Total in file: 5. ✓

What problem would you have if you used `"w"` instead of `"a"`?
_________________________________________________________________________

##### Reflection

1. Write a one-sentence warning to a younger student about `'w'` mode.
   _________________________________________________________________________

2. Why does `f.write("Hello")` not add a newline, when `print("Hello")` does?
   _________________________________________________________________________

3. When would you intentionally **want** `'w'` mode (i.e. it's the right choice)?
   _________________________________________________________________________

##### Bonus / Stretch Challenge

Extend `todo.py` so that every task is saved with a timestamp string you build manually, like this:
```
[Mon] Buy milk
[Tue] Walk the dog
[Tue] Finish homework
```
You can use `input("Day (Mon/Tue/...): ")` for now. (In Session 35 we'll do this automatically with `datetime`.)

Then add a feature: when the program starts, count how many tasks are tagged with each day and print:
```
Tasks per day:
  Mon: 1
  Tue: 2
```

Hint: read all lines, slice the day out of `[Tue]`, count with a dictionary.

```python
# todo_with_days.py








```

---

### Session 33: Errors & Try / Except

---

#### SESSION 33 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 33 of 48 |
| **Title** | Errors & Try / Except |
| **Unit** | Unit 6: File I/O, Errors & Built-in Modules |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §7.4 — testing (normal/boundary/erroneous data); 0478 §10 — file handling errors |
| **Singapore Alignment** | O-Level 7155 Module 4 — error handling, defensive programming |

##### Learning Objectives (SMART)
1. **Identify** at least six common Python exception types (`ValueError`, `TypeError`, `FileNotFoundError`, `ZeroDivisionError`, `KeyError`, `IndexError`) by reading a traceback within 30 seconds.
2. **Read** a Python traceback and locate the line number, the exception type, and the human-readable message.
3. **Write** a `try`/`except` block that catches a specific exception (not bare `except:`) and produces a user-friendly error message.
4. **Apply** Cambridge IGCSE test-data categories — normal, boundary, invalid — to test their own input-handling code with at least one example of each.

##### Materials Needed
- Thonny IDE
- Printed traceback "crime-scene cards" (provided in worksheet)
- Printed Worksheet 33
- Projector
- Anchor poster: the four-part anatomy of a traceback

##### Procedure

**0–5 min: Warm-Up — "What can go wrong?"**
Teacher writes on the board:
```python
age = int(input("Your age: "))
print("Next year you'll be", age + 1)
```
Asks: "How many ways can a user break this program in 60 seconds? Shout them out." Collect (typically): typing letters, leaving it blank, typing a decimal, typing a negative number, typing `"twenty"`, etc. "Today we learn to **catch** these so the program doesn't crash."

**5–15 min: Introduction — Reading a Traceback**

Run this code live:
```python
n = int("hello")
```
The output:
```
Traceback (most recent call last):
  File "/Users/student/test.py", line 1, in <module>
    n = int("hello")
ValueError: invalid literal for int() with base 10: 'hello'
```

Anatomy lesson on the projector:
- **`Traceback (most recent call last):`** → "Read from the bottom up."
- **File and line number** → where in your code the crash happened.
- **`ValueError`** → the *type* of mistake.
- **`invalid literal for int() with base 10: 'hello'`** → the *details*.

Now show six common exceptions in a table:

| Exception | When it happens | Tiny example |
|-----------|-----------------|--------------|
| `ValueError` | Right type, wrong value | `int("hello")` |
| `TypeError` | Wrong type entirely | `"hi" + 5` |
| `ZeroDivisionError` | Division by zero | `10 / 0` |
| `IndexError` | List index out of range | `[1,2,3][5]` |
| `KeyError` | Dict key not found | `{"a":1}["b"]` |
| `FileNotFoundError` | File doesn't exist | `open("missing.txt")` |

**15–35 min: Guided Practice — `try` / `except` in Action**

**Pattern 1 — basic `try`/`except`:**
```python
try:
    age = int(input("Your age: "))
    print("Next year you'll be", age + 1)
except ValueError:
    print("That wasn't a whole number. Please try again.")
```
Run it. Type `"abc"`. The program prints the friendly message and **does not crash**. Magic!

**Pattern 2 — looping until valid input:**
```python
while True:
    try:
        age = int(input("Your age: "))
        break                           # success — leave the loop
    except ValueError:
        print("Please enter a whole number, like 12.")

print("Got it. You are", age, "years old.")
```

**Pattern 3 — multiple `except` blocks:**
```python
try:
    a = int(input("Numerator:   "))
    b = int(input("Denominator: "))
    print(a / b)
except ValueError:
    print("Both must be whole numbers.")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

**Pattern 4 — handling a missing file:**
```python
try:
    with open("scores.txt", "r") as f:
        for line in f:
            print(line.strip())
except FileNotFoundError:
    print("(No scores yet — be the first to play!)")
```

**Pattern 5 — `else` and `finally` (introduce briefly):**
```python
try:
    n = int(input("Pick a number: "))
except ValueError:
    print("Not a number.")
else:
    # runs ONLY if no exception
    print("Square is", n * n)
finally:
    # ALWAYS runs (used for cleanup)
    print("Thanks for playing.")
```

**Test data revisited (Cambridge IGCSE):**

Code under test:
```python
def get_grade(percent):
    if percent < 0 or percent > 100:
        raise ValueError("Percent must be 0–100")
    if percent >= 70: return "A"
    if percent >= 50: return "B"
    if percent >= 35: return "C"
    return "F"
```

Test data table:
| Type | Input | Expected |
|------|-------|----------|
| Normal | 75 | "A" |
| Normal | 42 | "C" |
| Boundary | 70 | "A" |
| Boundary | 69 | "B" |
| Boundary | 0 | "F" |
| Boundary | 100 | "A" |
| Invalid | -5 | ValueError |
| Invalid | 150 | ValueError |
| Invalid | "fifty" | TypeError (from `<`) |

Have students predict, then run.

**35–50 min: Independent Practice — Worksheet**
Distribute Worksheet 33. Parts 1–3.

**50–55 min: Sharing & Discussion**
"Show me the friendliest error message anyone wrote." Two volunteers project. Class votes for the most user-respectful one.

**55–60 min: Closure & Preview**
Exit ticket: *"Name two exceptions and one situation where each happens."* Preview: "Tomorrow — Python's free libraries. Random numbers, square roots, π, all without writing a single formula yourself."

##### Differentiation

**Support:**
- Provide a "scaffolded" `try`/`except` template they only fill in the body of.
- Reduce the number of exceptions to memorise to three (`ValueError`, `ZeroDivisionError`, `FileNotFoundError`).
- Pair-program for Part 3 (the robust input prompt).

**Extension:**
- Use `except (ValueError, TypeError):` to catch multiple exceptions in one line.
- Catch the exception **and** print its message: `except ValueError as e: print("Error:", e)`.
- Re-raise an exception with `raise` after logging it.
- Write a custom exception class `class TooYoungError(Exception): pass` and `raise` it when age < 5.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Reading tracebacks** | Cannot find line/type | Identifies one of (line/type/message) | Identifies all three | Reads full multi-frame traceback fluently |
| **Specific `except`** | Uses bare `except:` | Catches `Exception` | Catches specific named exceptions | Catches multiple specific exceptions appropriately |
| **User-friendly messages** | Crash propagates | Generic "Error" message | Helpful, kind message | Tells user what to do next |
| **Test-data coverage** | Tests one normal value | Normal + boundary | Normal + boundary + invalid | All three, plus edge cases (empty/very large) |

##### Teacher Notes
- Discourage **bare `except:`** strongly — it hides bugs by catching things like `KeyboardInterrupt`. Always name the exception.
- Many students will try to `try:` only one line. Show that the `try:` block can be many lines, and `except` catches the **first** failing line.
- The boundary/normal/invalid taxonomy is a Cambridge favourite — it will show up on exam papers. Drill it.
- Foreshadow Session 36 (the journal app), where missing-file handling is essential.
- Avoid `try`/`except` as a substitute for control flow (the LBYL/EAFP debate is for later years).

---

#### SESSION 33 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Crime-Scene Tracebacks

For each traceback below, write **(a)** the exception type, **(b)** the line number, **(c)** what the programmer probably did wrong.

**Case A:**
```
Traceback (most recent call last):
  File "game.py", line 14, in <module>
    score = score + bonus
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```
(a) Type: ____________________
(b) Line: ____________________
(c) What went wrong? _________________________________________________

**Case B:**
```
Traceback (most recent call last):
  File "loader.py", line 3, in <module>
    with open("save.dat", "r") as f:
FileNotFoundError: [Errno 2] No such file or directory: 'save.dat'
```
(a) Type: ____________________
(b) Line: ____________________
(c) What went wrong? _________________________________________________

**Case C:**
```
Traceback (most recent call last):
  File "stats.py", line 8, in <module>
    average = total / count
ZeroDivisionError: division by zero
```
(a) Type: ____________________
(b) Line: ____________________
(c) What went wrong? _________________________________________________

**Case D:**
```
Traceback (most recent call last):
  File "menu.py", line 22, in <module>
    print(students[10])
IndexError: list index out of range
```
(a) Type: ____________________
(b) Line: ____________________
(c) What went wrong? _________________________________________________

**Case E:**
```
Traceback (most recent call last):
  File "phonebook.py", line 5, in <module>
    print(contacts["Zoe"])
KeyError: 'Zoe'
```
(a) Type: ____________________
(b) Line: ____________________
(c) What went wrong? _________________________________________________

##### Part 2: Predict the Exception

For each line of code, predict the exception type that will be raised. Write "OK" if it runs without error.

| Code | Exception (or "OK") |
|------|---------------------|
| `int("12.5")` | __________________ |
| `int("12")` | __________________ |
| `int("twelve")` | __________________ |
| `[1, 2, 3][3]` | __________________ |
| `[1, 2, 3][2]` | __________________ |
| `{"a": 1}["a"]` | __________________ |
| `{"a": 1}["b"]` | __________________ |
| `"5" + 5` | __________________ |
| `"5" + str(5)` | __________________ |
| `100 / 0` | __________________ |
| `100 // 0` | __________________ |
| `100 / 0.0` | __________________ |

##### Part 3: Robust Input Prompt

Build a function `ask_for_age()` that:
1. Asks the user for their age.
2. Re-prompts politely if they enter something that isn't a whole number.
3. Re-prompts if the number is less than 0 or greater than 130.
4. Returns the valid age.

Use `try`/`except ValueError` and a `while True:` loop.

```python
def ask_for_age():




age = ask_for_age()
print("Got it:", age)
```

**Test it with this Cambridge-style data:**

| Category | Input | Expected behaviour |
|----------|-------|--------------------|
| Normal | `12` | accept, return 12 |
| Normal | `45` | accept, return 45 |
| Boundary | `0` | accept |
| Boundary | `130` | accept |
| Boundary | `-1` | reject |
| Boundary | `131` | reject |
| Invalid | `abc` | reject (ValueError caught) |
| Invalid | (blank) | reject |
| Invalid | `12.5` | reject |

Did your function pass all 9 tests? **Yes / No**. If no, which failed? _____________

##### Reflection

1. Why is `except:` (with no name) considered bad practice?
   _________________________________________________________________________

2. What is the difference between a **boundary** test and an **invalid** test?
   _________________________________________________________________________

3. Imagine you're using a website and it shows you `Traceback (most recent call last)...`. Whose fault is that — the user's or the programmer's? Why?
   _________________________________________________________________________

##### Bonus / Stretch Challenge

Build a program `safe_division.py` that:
- Asks for two numbers.
- Divides the first by the second.
- Catches `ValueError` (non-number input) and `ZeroDivisionError` (b = 0).
- Uses an `else:` clause to print the result only when no error occurred.
- Uses a `finally:` clause to print "Calculation attempt finished." every time.
- Loops forever until the user types `quit` instead of a number.

```python
# safe_division.py








```

---

### Session 34: random & math Modules

---

#### SESSION 34 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 34 of 48 |
| **Title** | random & math Modules |
| **Unit** | Unit 6: File I/O, Errors & Built-in Modules |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — library routines (random, MOD, DIV, ROUND); 0860 strand 4.2 — using prebuilt code |
| **Singapore Alignment** | O-Level 7155 Module 4 — built-in functions; mathematical operations |

##### Learning Objectives (SMART)
1. **Import** the `random` module and use `randint`, `random`, `choice`, and `shuffle` correctly to model dice, coins, cards, and shuffled lists.
2. **Import** the `math` module and use `sqrt`, `pi`, `floor`, `ceil`, and `pow` to perform mathematical operations.
3. **Apply** the `%` (MOD) and `//` (DIV) operators, and the built-in `round(x, ndigits)`, mapping each to its Cambridge pseudocode equivalent.
4. **Explain** in one sentence what a "library / module" is and why importing is preferable to writing the function yourself.

##### Materials Needed
- Thonny IDE
- Printed Worksheet 34
- Pair of physical dice (for kinaesthetic warm-up)
- Projector
- Reference card: Cambridge ↔ Python operators (MOD/DIV/ROUND)

##### Procedure

**0–5 min: Warm-Up — "Roll the Dice"**
Teacher rolls a real die three times, recording outcomes on the board: e.g. 4, 1, 6. Asks: "If we wanted to simulate this in Python, what would we need?" Most students suggest "random number from 1 to 6." Connect: "Today we don't write the math from scratch — we **import** it."

**5–15 min: Introduction — What is a Module?**

Whiteboard sketch:
```
Your code  ──────  import random  ──────►  Python's random library
                                            (someone else wrote it!)
```

Then live-code:
```python
import random

# Your first random number
n = random.randint(1, 6)
print("Die roll:", n)
```
Run it 5 times — different number each time.

Define **module**: "A file of Python code someone has already written, that you can use by importing it. Python comes with hundreds — `random`, `math`, `datetime`, `turtle`, and many more."

A note on **academic honesty**: "Using a module is not cheating — it's professional. But you must still understand what it does. If a teacher asks 'how does `randint` work?', you should be able to answer: 'It picks a whole number from a to b, both ends included.'"

**15–35 min: Guided Practice — random and math Tour**

**The `random` module — five super-useful functions:**

```python
import random

# 1. Whole number, both ends INCLUSIVE
random.randint(1, 6)        # 1, 2, 3, 4, 5, or 6

# 2. Float between 0.0 and 1.0
random.random()             # e.g. 0.7345...

# 3. Pick one item from a list
fruits = ["apple", "banana", "cherry", "date"]
random.choice(fruits)       # one of those strings

# 4. Shuffle a list IN PLACE
deck = list(range(1, 11))   # [1,2,3,4,5,6,7,8,9,10]
random.shuffle(deck)
print(deck)                 # e.g. [7, 3, 10, 1, 9, 5, 4, 8, 2, 6]

# 5. Pick a sample without replacement
random.sample(fruits, 2)    # 2 distinct fruits
```

**Mini program — Coin Flip 100×:**
```python
import random

heads = 0
tails = 0
for _ in range(100):
    flip = random.choice(["H", "T"])
    if flip == "H":
        heads += 1
    else:
        tails += 1
print(f"Heads: {heads}, Tails: {tails}")
```

**Mini program — Card Draw:**
```python
import random

ranks = ["A", "2", "3", "4", "5", "6", "7", "8", "9", "10", "J", "Q", "K"]
suits = ["♠", "♥", "♦", "♣"]
deck  = [r + s for s in suits for r in ranks]   # 52 cards

random.shuffle(deck)
hand = deck[:5]
print("Your hand:", hand)
```

**The `math` module:**
```python
import math

math.sqrt(25)        # 5.0
math.pi              # 3.141592653589793
math.floor(4.9)      # 4   — round DOWN always
math.ceil(4.1)       # 5   — round UP always
math.pow(2, 10)      # 1024.0
math.factorial(5)    # 120
```

**Pythagoras' theorem in 1 line:**
```python
import math
a, b = 3, 4
c = math.sqrt(a*a + b*b)
print("Hypotenuse:", c)    # 5.0
```

**Area of a circle:**
```python
import math
r = float(input("Radius: "))
area = math.pi * r ** 2
print(f"Area = {round(area, 2)}")
```

**The `%` and `//` operators — Cambridge MOD and DIV:**

Whiteboard table:
| Cambridge pseudocode | Python | Example | Result |
|----------------------|--------|---------|--------|
| `MOD`  (remainder) | `%` | `17 % 5` | `2` |
| `DIV`  (whole-number divide) | `//` | `17 // 5` | `3` |
| `ROUND(x, n)` | `round(x, n)` | `round(3.14159, 2)` | `3.14` |

Classic uses:
```python
# Is n even?
n = 14
print(n % 2 == 0)         # True

# Last digit of a number
print(1234 % 10)          # 4

# Convert seconds to minutes:seconds
total = 257
minutes = total // 60     # 4
seconds = total % 60      # 17
print(f"{minutes}:{seconds:02d}")   # 4:17
```

**Putting it together — a Number Guessing Game (Cambridge classic):**
```python
import random

secret    = random.randint(1, 100)
guesses   = 0

while True:
    try:
        g = int(input("Guess (1-100): "))
    except ValueError:
        print("Enter a whole number.")
        continue
    guesses += 1
    if g < secret:
        print("Higher!")
    elif g > secret:
        print("Lower!")
    else:
        print(f"Correct! In {guesses} guesses.")
        break
```

**35–50 min: Independent Practice — Worksheet**
Students complete Parts 1–3.

**50–55 min: Sharing & Discussion**
"Show your dice-roll histogram" (a worksheet exercise). Class compares — does the distribution look uniform? Why does small N look uneven?

**55–60 min: Closure & Preview**
Exit ticket: *"Name one function from `random`, one from `math`, and explain what each does in your own words."* Preview: "Tomorrow — telling time. The `datetime` module, timestamps, and saving structured data to files."

##### Differentiation

**Support:**
- Provide a function/method "cheat sheet" listing each function and a one-line example.
- Restrict to `randint`, `choice`, `sqrt`, `%`, `//` only.
- Pair students for the guessing game.

**Extension:**
- `random.seed(42)` — explore reproducibility. Why is this useful for testing?
- Use `random.choices(weights=[...])` to make a biased coin.
- Write a program that approximates π using random points in a square (Monte Carlo method).
- Implement Cambridge IGCSE pseudocode `RAND(x)` (returns a float between 0 and x) using only `random.random()`.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **`random` use** | Misuses `randint` bounds | Uses one function correctly | Uses 3+ functions correctly | Picks the most appropriate function for each task |
| **`math` use** | Hard-codes `3.14`/writes own sqrt | Uses one math function | Uses 3+ correctly | Combines several into a multi-step calculation |
| **MOD / DIV** | Confused | Knows operators but inconsistent | Applies correctly to a problem | Can convert between MOD/DIV and Cambridge pseudocode |
| **Module concept** | Confused about `import` | Imports correctly | Explains "what is a module" clearly | Compares Python modules to libraries in other tools |

##### Teacher Notes
- `random.randint(1, 6)` is **inclusive on both ends** — different from `range(1, 6)`. This is a frequent off-by-one bug.
- Mention that there's also `from random import randint` (then call `randint(...)` directly). Both styles are acceptable; consistency matters.
- `math.pow(2, 10)` returns a float (`1024.0`); plain `2**10` returns an int. Mention this so students choose the right one.
- Cambridge pseudocode convention: `MOD` and `DIV` are **operators**, not functions: `a MOD b`. The Python `%` and `//` directly mirror this.
- Reinforce attribution lightly: when students copy a recipe (e.g. Pythagoras) from a book or website, they should note the source in a comment.

---

#### SESSION 34 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Random Number Puzzles

**Q1. Dice roller.** Write a program that rolls TWO dice and prints both values plus the total. Run it 5 times and record the outputs.

```python
# two_dice.py


```
| Run | Die 1 | Die 2 | Total |
|-----|-------|-------|-------|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |

**Q2. Dice histogram.** Roll one die 60 times. Count how many of each face appear. Use a dictionary.

```python
import random

counts = {1: 0, 2: 0, 3: 0, 4: 0, 5: 0, 6: 0}

# loop 60 times, update counts



for face, n in counts.items():
    bar = "*" * n
    print(f"{face} | {bar} ({n})")
```

Paste your histogram output here:
```


```

If a die is fair, what number would you **expect** for each face? ______
Why are your numbers slightly different? __________________________________

**Q3. Random card draw.** Build a 52-card deck, shuffle it, and deal a 5-card hand. Print the hand on one line.

```python
# poker_hand.py





```

Sample output: `Your hand: ['A♠', '7♥', 'K♣', '3♦', 'J♠']`

**Q4. Magic 8-Ball.** A "Magic 8-Ball" gives one of 10 random predictions. Build it.

```python
import random

answers = [
    "Yes, definitely.",
    "Ask again later.",
    "It is certain.",
    "Very doubtful.",
    "Without a doubt.",
    "My sources say no.",
    "Outlook good.",
    "Don't count on it.",
    "Signs point to yes.",
    "Cannot predict now."
]

# Ask the user a yes/no question, then print one random answer.



```

##### Part 2: math Module Exercises

**Q1. Pythagoras.** Ask the user for the two short sides `a` and `b` of a right-angled triangle. Print the hypotenuse rounded to 2 decimal places.

```python
import math





```

**Q2. Circle calculator.** Ask for the radius. Print:
- Circumference (`2 × π × r`)
- Area (`π × r²`)
Both rounded to 2 decimal places.

```python
import math





```

**Q3. Floor vs Ceil.** Predict, then check:

| Code | `math.floor(...)` | `math.ceil(...)` |
|------|-------------------|-------------------|
| `4.0` | _____ | _____ |
| `4.1` | _____ | _____ |
| `4.9` | _____ | _____ |
| `-4.1` | _____ | _____ |
| `-4.9` | _____ | _____ |

##### Part 3: MOD, DIV, ROUND Problems

**Q1. Even or odd?** Use `%` to write a one-line `is_even(n)` function.
```python
def is_even(n):
    return ____________________
```

**Q2. Time conversion.** A program receives `total_seconds = 3725`. Print it as `H:MM:SS` (hours, minutes, seconds).
```python
total_seconds = 3725

hours   = ____________________
minutes = ____________________
seconds = ____________________

print(f"{hours}:{minutes:02d}:{seconds:02d}")
```
Expected output: `1:02:05`

**Q3. Money change.** A user buys an item costing 273 cents and pays 500 cents. Calculate the change in dollars and cents.
```python
paid     = 500
cost     = 273
change   = paid - cost            # 227 cents

dollars  = ____________________   # whole dollars
cents    = ____________________   # leftover cents

print(f"${dollars}.{cents:02d}")
```
Expected output: `$2.27`

**Q4. ROUND.** Predict the output:

| Code | Output |
|------|--------|
| `round(3.14159, 2)` | _________ |
| `round(3.14159, 0)` | _________ |
| `round(3.5)` | _________ |
| `round(2.5)` | _________ |

(Note: Python uses **banker's rounding** at .5 — it rounds to the nearest even number. Surprising!)

##### Reflection

1. What does the word **"module"** mean to you, in your own words?
   _________________________________________________________________________

2. Why is using `math.pi` better than typing `3.14159` yourself?
   _________________________________________________________________________

3. If `randint(1, 6)` includes both 1 and 6, but `range(1, 6)` does not include 6, why are they different? Could you write `randint` using `range`? Sketch the idea.
   _________________________________________________________________________
   _________________________________________________________________________

##### Bonus / Stretch Challenge

**Monte Carlo π.** A circle of radius 1 fits inside a 2×2 square. The ratio of circle-area to square-area is π/4. So if we throw N random "darts" into the square, the proportion that land inside the circle should approximate π/4.

Write a program that:
1. Throws N = 10,000 random darts (use `random.random()` to get x and y in [0, 1], then map to [-1, 1]).
2. Counts how many land inside the unit circle (`x² + y² ≤ 1`).
3. Prints the estimate of π = `4 × inside / N`.

```python
import random

N = 10000
inside = 0

# loop N times, sample (x, y), test, count



estimate = 4 * inside / N
print("Estimated π =", estimate)
print("Real π     =", 3.14159265358979)
```

Run it three times. Are the estimates close to π?

```


```

---

### Session 35: datetime & Simple Data Persistence

---

#### SESSION 35 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 35 of 48 |
| **Title** | datetime & Simple Data Persistence |
| **Unit** | Unit 6: File I/O, Errors & Built-in Modules |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — library routines; data files with structured records |
| **Singapore Alignment** | O-Level 7155 Module 4 — date/time handling, data persistence |

##### Learning Objectives (SMART)
1. **Use** `datetime.now()` and `date.today()` to obtain the current timestamp and format it with `.strftime()` using at least three different format codes (`%Y`, `%m`, `%d`, `%H`, `%M`, `%S`).
2. **Build** a timestamped log file by combining `with open(..., "a")` and a formatted `datetime` string.
3. **Save** a list of dictionaries to a text file using a `|`-delimited format and **load** it back in, parsing with `.split("|")`.
4. **Calculate** the number of days between two dates using `date` objects and subtraction.

##### Materials Needed
- Thonny IDE
- Printed Worksheet 35
- Sample log file `study_log.txt` (provided in worksheet, may be empty initially)
- Projector
- Reference poster: `strftime` format codes

##### Procedure

**0–5 min: Warm-Up — "When?"**
Teacher asks: "If your journal saves an entry today and you re-open it in 6 months, how will you know **when** each entry was written?" Students suggest: write the date by hand, ask the user to type it… "What if Python could just **know**? It can. That's `datetime`."

**5–15 min: Introduction — `datetime` Basics**

```python
from datetime import datetime, date

# What time is it RIGHT NOW?
now = datetime.now()
print(now)                # 2026-04-27 09:14:32.487123

# Just the date — no time
today = date.today()
print(today)              # 2026-04-27

# Pieces of "now"
print(now.year)           # 2026
print(now.month)          # 4
print(now.day)            # 27
print(now.hour)           # 9
print(now.minute)         # 14
```

**Formatting with `strftime` — the "string format time" method:**

Project the format-code reference:

| Code | Meaning | Example |
|------|---------|---------|
| `%Y` | 4-digit year | `2026` |
| `%m` | 2-digit month | `04` |
| `%d` | 2-digit day | `27` |
| `%H` | 24-hour | `09` |
| `%M` | minute | `14` |
| `%S` | second | `32` |
| `%A` | weekday name | `Monday` |
| `%B` | month name | `April` |

```python
from datetime import datetime
now = datetime.now()

print(now.strftime("%Y-%m-%d"))               # 2026-04-27
print(now.strftime("%Y-%m-%d %H:%M:%S"))      # 2026-04-27 09:14:32
print(now.strftime("%A, %B %d, %Y"))          # Monday, April 27, 2026
```

**15–35 min: Guided Practice**

**Demo 1 — A timestamped log function:**
```python
from datetime import datetime

def log(message, filename="activity.log"):
    stamp = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    with open(filename, "a") as f:
        f.write(f"[{stamp}] {message}\n")

log("Program started")
log("User logged in: aisha")
log("Score saved: 1450")
```

Open `activity.log`:
```
[2026-04-27 09:14:32] Program started
[2026-04-27 09:14:33] User logged in: aisha
[2026-04-27 09:14:34] Score saved: 1450
```

**Demo 2 — Days between two dates:**
```python
from datetime import date

birthday = date(2026, 12, 25)
today    = date.today()
diff     = birthday - today           # this is a timedelta!
print("Days until Christmas:", diff.days)
```

**Demo 3 — Storing structured data with `|`-delimiters.**

Why not JSON yet? It would mean introducing the `json` module and dict-string parsing. We keep it simple: each record is one line, fields separated by `|`. This is essentially CSV with a chosen delimiter.

```python
from datetime import datetime

# A list of dictionaries, the typical "table" structure
entries = [
    {"date": "2026-04-25", "mood": "happy",  "text": "Aced my Python quiz!"},
    {"date": "2026-04-26", "mood": "tired",  "text": "Long football practice."},
    {"date": "2026-04-27", "mood": "excited","text": "Started journal app."},
]

# SAVE: dict → "field|field|field" → file
with open("journal.txt", "w") as f:
    for e in entries:
        line = f"{e['date']}|{e['mood']}|{e['text']}\n"
        f.write(line)
```

Open `journal.txt`:
```
2026-04-25|happy|Aced my Python quiz!
2026-04-26|tired|Long football practice.
2026-04-27|excited|Started journal app.
```

**Demo 4 — LOAD it back into a list of dicts:**
```python
loaded = []
with open("journal.txt", "r") as f:
    for line in f:
        parts = line.strip().split("|")
        record = {
            "date": parts[0],
            "mood": parts[1],
            "text": parts[2],
        }
        loaded.append(record)

for r in loaded:
    print(r)
```

**The delimiter problem.** Ask: "What if a journal entry contains the character `|`?" e.g. `"I love coding | drawing"`. The split breaks. Discuss briefly:
1. Choose a delimiter that's unlikely in user text (`|`, tab `\t`, or `~~~`).
2. **Replace** the delimiter on save: `text.replace("|", "/")`.
3. Use real CSV (`csv` module) — beyond today's scope.

**Mention CSV in passing:**
```python
# CSV is the standard. Python has a csv module (later in your journey).
# For now, our "|"-delimited format is conceptually identical.
```

**35–50 min: Independent Practice — Worksheet**
Students complete Parts 1–3, building a study-session log and a date calculator.

**50–55 min: Sharing & Discussion**
"Read out your study-session log so far." Discuss: what would make it more useful (subject? duration? mood?). Foreshadow journal app.

**55–60 min: Closure & Preview**
Exit ticket: *"Write a `strftime` format string to produce `Mon 27 Apr 2026 09:14`."* Preview: "Tomorrow — we put it ALL together. Files, errors, datetime, modules, functions, dictionaries — into one journal application."

##### Differentiation

**Support:**
- Provide the `strftime` format string pre-written; student only fills in the message.
- Pre-create `journal.txt` so they only do the LOAD step.
- Use only `date` (not `datetime`) at first.

**Extension:**
- Compute a person's exact age in days from their birthdate.
- Show only entries from the last 7 days.
- Sort entries newest-first.
- Use `datetime.strptime()` to convert a string back into a `datetime` object.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **datetime use** | Imports incorrectly | Uses `datetime.now()` | Uses + formats with `strftime` | Combines `now()`, `date.today()`, and arithmetic |
| **strftime format** | Format code errors | One format works | Multiple formats produced cleanly | Designs a custom human-friendly format |
| **Save structured data** | Loses fields | Saves but cannot reload | Saves and loads round-trip | Saves, loads, and handles delimiter collisions |
| **Date arithmetic** | Confused | Subtracts but doesn't extract `.days` | Computes day difference | Computes age, deadlines, and date ranges |

##### Teacher Notes
- Time zones: avoid the rabbit hole. `datetime.now()` returns local time, which is fine for journals.
- `strftime` codes are **case-sensitive**: `%M` (minute) ≠ `%m` (month). This trips up everyone at least once.
- The `|`-delimited format is intentional — it's a stepping stone to CSV/JSON. Praise its simplicity.
- If students ask "why not use JSON now?": "Great question — that's a Unit 7 topic. Today we're focused on the *concept* of round-trip persistence."
- The subtraction `date - date` returns a `timedelta`. Many students try to print the timedelta directly and get `5 days, 0:00:00`. Show them `.days`.

---

#### SESSION 35 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: strftime Format Practice

**Q1.** Predict the output of each line. Then run them.

```python
from datetime import datetime
now = datetime.now()
print(now.strftime("%Y-%m-%d"))
print(now.strftime("%H:%M:%S"))
print(now.strftime("%A"))
print(now.strftime("%d %B %Y"))
print(now.strftime("Today is %A, %B %d. Time: %H:%M."))
```

Predictions (assume today is Monday 27 April 2026 at 09:14:32):

| Line | Predicted output |
|------|------------------|
| 1 | __________________________________ |
| 2 | __________________________________ |
| 3 | __________________________________ |
| 4 | __________________________________ |
| 5 | __________________________________ |

**Q2.** Write the `strftime` format string that produces each of these outputs (assume `now` is the same as above):

| Desired output | Format string |
|----------------|---------------|
| `2026/04/27` | `_______________________` |
| `27-04-2026` | `_______________________` |
| `April 27, 2026` | `_______________________` |
| `Mon Apr 27` | `_______________________` |
| `09:14 AM` (use `%I:%M %p`) | `_______________________` |

##### Part 2: Build a Study-Session Log

Build `study_log.py` that:

1. Asks the user: subject (e.g. "Math"), and how long they studied (in minutes).
2. Appends one line to `study_log.txt` in this exact format:
   ```
   2026-04-27 09:14:32 | Math | 45 min
   ```
3. Loops until the user types `done` for the subject.
4. After the loop, opens `study_log.txt` and **reads it back**, printing total minutes studied today.

```python
# study_log.py
from datetime import datetime, date












```

**Test plan:**
- [ ] Run program, log 3 sessions. Open `study_log.txt` — see 3 lines with timestamps.
- [ ] Re-run program, log 2 more. File now has 5 lines.
- [ ] Total-minutes summary at the end is correct.

##### Part 3: Date Arithmetic

**Q1.** Days until your birthday.
```python
from datetime import date

# CHANGE these to your real birth month/day
my_birthday_this_year = date(2026, ___, ___)
today = date.today()

if my_birthday_this_year >= today:
    diff = my_birthday_this_year - today
    print("Days until birthday:", diff.days)
else:
    next_birthday = date(2027, my_birthday_this_year.month, my_birthday_this_year.day)
    diff = next_birthday - today
    print("Days until next birthday:", diff.days)
```

How many days? **______**

**Q2.** Age in days. Given your real birthdate, compute how many days old you are.
```python
from datetime import date

birth = date(____, __, __)        # your birthdate
today = date.today()
age_days = (today - birth).days
print("You are", age_days, "days old.")
```

Days old: **______**

**Q3.** Parse a delimited file. Given this content of `journal.txt`:
```
2026-04-25|happy|Aced my Python quiz!
2026-04-26|tired|Long football practice.
2026-04-27|excited|Started journal app.
```

Write a program that loads it into a list of dictionaries and prints only the entries where the **mood** is `happy` or `excited`.

```python
# parse_journal.py








```

##### Reflection

1. Why do programs need to know the date and time? Give two real-world examples.
   _________________________________________________________________________
   _________________________________________________________________________

2. We chose `|` as our delimiter. What problem could happen if a journal entry contains the character `|`? How could you fix it?
   _________________________________________________________________________
   _________________________________________________________________________

3. What's the difference between a `datetime` and a `date`? When would you use each?
   _________________________________________________________________________

##### Bonus / Stretch Challenge

**Project deadline tracker.** Build `deadlines.py` that:
1. Stores a list of dicts in a file `deadlines.txt`, where each line is `subject|YYYY-MM-DD|description`.
2. On startup, loads the file (handle missing file gracefully — preview of Session 36!).
3. For each deadline, calculates **days remaining** using `date.today()` and `date(...)`.
4. Prints the deadlines sorted by days remaining (smallest first), highlighting any with **fewer than 3 days** in CAPITAL LETTERS.
5. Lets the user add a new deadline interactively.

```python
# deadlines.py
from datetime import date













```

Sample output:
```
Upcoming deadlines:
  Math      | 2026-04-29 |  2 days | URGENT! ALGEBRA HOMEWORK
  English   | 2026-05-04 |  7 days | Essay
  Science   | 2026-05-15 | 18 days | Project poster
```

---

### Session 36: Project 6 — Journal Application

---

#### SESSION 36 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 36 of 48 |
| **Title** | Project 6 — Journal Application |
| **Unit** | Unit 6: File I/O, Errors & Built-in Modules |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §7.1–§7.5 — analysis, design, decomposition, testing; §10 — file handling, library routines |
| **Singapore Alignment** | O-Level 7155 Module 3 (program design) + Module 4 (file I/O, modules) |

##### Learning Objectives (SMART)
1. **Design** a console application using pseudocode and a flowchart **before** coding, including a file-format spec.
2. **Implement** a multi-feature Journal Application that integrates: `try/except`, `with open()`, `datetime`, functions, dictionaries, lists, loops, and a menu.
3. **Test** the application against normal/boundary/invalid data, including a first run when no file exists.
4. **Peer-evaluate** another student's journal using a provided rubric and provide one improvement suggestion.

##### Materials Needed
- Thonny IDE
- Printed Worksheet 36 (project planning template)
- Projector
- Optional: turtle graphics for the stretch bar-chart task
- Each student should have an **empty folder** for the project

##### Procedure

**0–5 min: Warm-Up — "What does a real journal need?"**
Teacher asks: "If you were going to keep a digital diary, what features would you want?" Whiteboard the list. Common answers: write entries, see old ones, search, mood tracker, password (out of scope), pictures (out of scope), date-based view. The teacher circles the four core features for today: **Add, View, Filter-by-date, Search.**

**5–15 min: Introduction — Design Before Code**

**Pseudocode for the main loop:**
```
LOOP forever
    DISPLAY menu
    READ choice
    IF choice = 1 THEN add_entry()
    ELSE IF choice = 2 THEN view_all()
    ELSE IF choice = 3 THEN view_by_date()
    ELSE IF choice = 4 THEN search()
    ELSE IF choice = 5 THEN BREAK
    ELSE
        DISPLAY "Unknown option"
ENDLOOP
DISPLAY "Goodbye!"
```

**Flowchart for `add_entry()` (sketch on board):**
```
   [start]
      ▼
[get current timestamp]
      ▼
[ask user for mood]
      ▼
[ask user for text]
      ▼
[clean | from inputs]
      ▼
[append "ts|mood|text\n" to journal.txt]
      ▼
[print "Entry saved!"]
      ▼
   [end]
```

**File-format spec:**
| Field | Type | Example | Notes |
|-------|------|---------|-------|
| timestamp | string | `2026-04-27 09:14:32` | from `datetime.now().strftime(...)` |
| mood | string | `happy` | one of: happy/sad/tired/excited/calm/angry |
| text | string | `Today I learnt about…` | `\|` characters replaced with `/` |

Each record on its own line, fields separated by `|`. Same format as Session 35.

**15–35 min: Guided Practice — The Skeleton**

Build the skeleton **together** in 20 minutes, then students extend in independent time.

```python
# journal.py
from datetime import datetime

JOURNAL_FILE = "journal.txt"

# ---------------------------------------------------------------
# HELPERS
# ---------------------------------------------------------------
def load_entries():
    """Load all journal entries from file into a list of dicts.
    Handles the case where the file does not exist (first run)."""
    entries = []
    try:
        with open(JOURNAL_FILE, "r") as f:
            for line in f:
                parts = line.strip().split("|")
                if len(parts) == 3:
                    entries.append({
                        "timestamp": parts[0],
                        "mood":      parts[1],
                        "text":      parts[2],
                    })
    except FileNotFoundError:
        # First run — that's fine. Return empty list.
        pass
    return entries


def save_entry(mood, text):
    """Append one new entry to the journal file."""
    timestamp = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    # Defensive: replace delimiter so it can't break our format
    mood = mood.replace("|", "/")
    text = text.replace("|", "/")
    line = f"{timestamp}|{mood}|{text}\n"
    with open(JOURNAL_FILE, "a") as f:
        f.write(line)


def pretty_print(entry):
    """Format one entry for display."""
    print(f"  [{entry['timestamp']}] ({entry['mood']})")
    print(f"    {entry['text']}")
    print()


# ---------------------------------------------------------------
# MENU ACTIONS
# ---------------------------------------------------------------
def add_entry():
    print("\n--- New Entry ---")
    mood = input("How are you feeling? ").strip()
    text = input("What's on your mind? ").strip()
    if not text:
        print("(empty entry — not saved)")
        return
    save_entry(mood, text)
    print("Entry saved!")


def view_all():
    entries = load_entries()
    if not entries:
        print("\n(No entries yet. Add one!)")
        return
    print(f"\n--- All Entries ({len(entries)}) ---")
    for e in entries:
        pretty_print(e)


def view_by_date():
    target = input("Date (YYYY-MM-DD): ").strip()
    entries = load_entries()
    matches = [e for e in entries if e["timestamp"].startswith(target)]
    if not matches:
        print(f"(No entries on {target})")
        return
    print(f"\n--- Entries on {target} ---")
    for e in matches:
        pretty_print(e)


def search():
    keyword = input("Search keyword: ").strip().lower()
    if not keyword:
        return
    entries = load_entries()
    matches = [e for e in entries if keyword in e["text"].lower()]
    if not matches:
        print(f"(No entries containing '{keyword}')")
        return
    print(f"\n--- {len(matches)} match(es) for '{keyword}' ---")
    for e in matches:
        pretty_print(e)


# ---------------------------------------------------------------
# MAIN
# ---------------------------------------------------------------
def main():
    print("=" * 40)
    print("  My Python Journal")
    print("=" * 40)
    while True:
        print("\nMenu:")
        print("  1. Add entry")
        print("  2. View all entries")
        print("  3. View entries by date")
        print("  4. Search entries")
        print("  5. Quit")
        choice = input("Choose 1–5: ").strip()
        if choice == "1":
            add_entry()
        elif choice == "2":
            view_all()
        elif choice == "3":
            view_by_date()
        elif choice == "4":
            search()
        elif choice == "5":
            print("Goodbye! Take care.")
            break
        else:
            print("Unknown option — please pick 1, 2, 3, 4, or 5.")


if __name__ == "__main__":
    main()
```

Walk through it function by function. Emphasise:
- Each function has **one job** (decomposition).
- `load_entries()` uses `try/except FileNotFoundError` for the first-run case.
- `datetime.now().strftime(...)` is used inside `save_entry`.
- `JOURNAL_FILE` is a constant — change it once, change everywhere.

**35–50 min: Independent Practice — Build & Extend**

Students copy or rebuild the skeleton, then **must** add at least one of the following:
- (Required) Validate `mood` against an allow-list `["happy","sad","tired","excited","calm","angry"]` with a `try/except` re-prompt loop.
- (Choose 1) Count entries per mood and display as text.
- (Choose 1) Show the most recent 3 entries first.

**Stretch (optional):** turtle bar chart of mood counts.

```python
# stretch_mood_chart.py
import turtle
from collections import Counter

# load entries (reuse load_entries() from journal.py)
# count moods
# draw bars: x = mood, y = count
```

**50–55 min: Sharing & Peer-Test**
Students pair up and **test each other's** journals using the rubric in the worksheet. They must specifically test:
- First run with no `journal.txt` (delete it!).
- Adding an entry containing the character `|`.
- Searching for a keyword that isn't there.
- Choosing menu option `9` (invalid).

**55–60 min: Closure & Preview**
Whole-class reflection: "What was the hardest part?" Common answers: getting the menu loop right, handling the missing file, parsing back from the file. Preview Unit 7: "Next we step into **graphics, OOP, and bigger projects**."

##### Differentiation

**Support:**
- Provide the full skeleton as a starter file. Student only fills in `view_by_date()` and `search()`.
- Reduce required features: just **Add** and **View all**. Extra features are stretch.
- Pre-create `journal.txt` with 3 sample entries.

**Extension:**
- Add an `Edit entry` feature (load all, modify one, rewrite file with `"w"`).
- Add a `Delete entry` feature with confirmation.
- Save tags per entry: extend the format to `timestamp|mood|tags|text` where `tags` is comma-separated.
- Build the turtle bar chart.
- Encrypt entries with a Caesar-cipher (callback to Unit 4 string manipulation).

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Design artefacts** | No pseudocode/flowchart | Either pseudocode or flowchart | Both, mostly accurate | Both, plus file-format spec, all consistent |
| **Decomposition** | One giant `main()` | A few helper functions | Clean separation: load/save/views/main | Clean + each function has docstring + reusable |
| **Error handling** | No `try/except`, crashes on missing file | Catches one error case | Handles missing file + invalid menu choice | Handles missing file + invalid menu + bad date format + delimiter collision |
| **Persistence** | Entries lost on quit | Saves but cannot reload | Round-trip: save and reload work | Round-trip + filtering + searching all work after restart |

##### Teacher Notes
- Don't let students skip the design phase. The 10 minutes of pseudocode + flowchart saves 30 minutes of tangled code.
- The most common bug is forgetting `\n` at end of `save_entry` — entries pile up on one line. The peer-test rubric catches this.
- Watch for students using `"w"` instead of `"a"` in `save_entry` — they will lose all but their most recent entry.
- The `|`-delimiter in user text bug is **expected** — it's an authentic learning moment about input sanitisation. Praise students who notice it themselves.
- This is a portfolio piece. Encourage students to take a screenshot of their working journal — it's evidence of mastery for Cambridge / O-Level coursework.
- If a pair finishes very early, push the encryption stretch — it's genuinely satisfying.

---

#### SESSION 36 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Project Plan — Pseudocode & Menu Design

Before writing **any** Python code, complete the design below.

**(a) Menu sketch.** Write the exact text your menu will display:
```


________________________________________
| My Python Journal                     |
|---------------------------------------|
| 1. ____________________________       |
| 2. ____________________________       |
| 3. ____________________________       |
| 4. ____________________________       |
| 5. ____________________________       |
________________________________________

Choose 1–5:
```

**(b) Main-loop pseudocode.** Fill in the missing keywords and actions.

```
__________ True
    DISPLAY menu
    __________ choice = INPUT
    __________ choice = "1" __________
        ___________________
    __________ choice = "2" __________
        ___________________
    __________ choice = "3" __________
        ___________________
    __________ choice = "4" __________
        ___________________
    __________ choice = "5" __________
        BREAK
    __________
        DISPLAY "Unknown option"
DISPLAY "Goodbye!"
```

**(c) Flowchart for `add_entry()`.** Sketch in the box below:

```
+-----------------------+
|                       |
|                       |
|                       |
|                       |
|                       |
|                       |
|                       |
|                       |
+-----------------------+
```

##### Part 2: File-Format Specification

Complete the table for the journal file (`journal.txt`):

| # | Field name | Type | Example value | Notes |
|---|------------|------|---------------|-------|
| 1 | timestamp | string | `2026-04-27 09:14:32` | from `datetime.now().strftime(...)` |
| 2 | mood | string | _________________ | allowed values: ________________________________ |
| 3 | text | string | _________________ | `\|` will be replaced with: _____ |

**Delimiter:** ______ (single character)
**Line terminator:** ______ (Python escape sequence)

**Example record:**
```
________________________________________________________________________
```

**(a)** Why did we choose this delimiter and not a comma?
_________________________________________________________________________

**(b)** What does the program do if a user types `|` in their journal text?
_________________________________________________________________________

##### Part 3: Build Checklist & Code

Complete the checklist as you build. Tick ✓ each item only after you have **tested** it.

**Core features**
- [ ] Program imports `datetime` from `datetime`.
- [ ] Constant `JOURNAL_FILE = "journal.txt"` defined at top.
- [ ] Function `load_entries()` returns a list of dicts; uses `try/except FileNotFoundError`.
- [ ] Function `save_entry(mood, text)` appends a `timestamp|mood|text\n` line.
- [ ] Function `pretty_print(entry)` displays one entry nicely.
- [ ] Menu loop with options 1–5.
- [ ] Option 1 (Add) prompts for mood + text and saves.
- [ ] Option 2 (View all) shows every entry.
- [ ] Option 3 (View by date) accepts `YYYY-MM-DD` and shows only those entries.
- [ ] Option 4 (Search) finds case-insensitive matches in `text`.
- [ ] Option 5 (Quit) exits cleanly.

**Robustness**
- [ ] First run (no `journal.txt`) does NOT crash.
- [ ] Empty entry text is rejected (or handled).
- [ ] Invalid menu choice (e.g. `9`, `abc`) gives a friendly message.
- [ ] User typing `|` in their entry does not break the file format.
- [ ] Searching with no matches gives a friendly "no results" message.

**Bonus**
- [ ] Mood is validated against an allow-list.
- [ ] Mood counts are displayed.
- [ ] Most recent entries shown first.

**Paste your final `journal.py` below (or attach a screenshot):**

```python
# journal.py














```

##### Part 4: Peer-Test Rubric

Swap with a partner. Test their journal and tick what works.

**Tester name:** ________________________________ **Author name:** ________________________________

| # | Test | Pass / Fail | Notes |
|---|------|-------------|-------|
| 1 | Run with no `journal.txt` (delete it first) — does not crash | ☐ Pass ☐ Fail | |
| 2 | Add 1 entry, view all — entry appears | ☐ Pass ☐ Fail | |
| 3 | Add 3 entries on different mock dates, view by today's date | ☐ Pass ☐ Fail | |
| 4 | Search for a word that IS in an entry | ☐ Pass ☐ Fail | |
| 5 | Search for a word that is NOT — friendly "no matches" message | ☐ Pass ☐ Fail | |
| 6 | Type `|` in an entry — file format still parseable on next run | ☐ Pass ☐ Fail | |
| 7 | Choose menu option `9` — friendly error, no crash | ☐ Pass ☐ Fail | |
| 8 | Quit, restart program — entries still there | ☐ Pass ☐ Fail | |

**One thing this journal does really well:**
_________________________________________________________________________

**One specific suggestion for improvement:**
_________________________________________________________________________

##### Reflection

1. Compare your design (pseudocode + flowchart) to your final code. Did the design save you time? Where did you have to deviate from it?
   _________________________________________________________________________
   _________________________________________________________________________

2. Which Python skill from earlier units did you use most heavily today? (Functions? Loops? Dictionaries? File I/O?) Why?
   _________________________________________________________________________

3. If you had another 60 minutes to extend this project, what one feature would you add and why?
   _________________________________________________________________________
   _________________________________________________________________________

##### Bonus / Stretch Challenge

**Mood bar chart with turtle.** Add a sixth menu option `6. Mood chart` that:
1. Loads all entries.
2. Counts each distinct mood.
3. Opens a turtle window and draws a bar chart, labelling each bar with the mood and the count.

```python
# Add to journal.py
import turtle
from collections import Counter

def mood_chart():
    entries = load_entries()
    if not entries:
        print("(No entries to chart yet.)")
        return
    counts = Counter(e["mood"] for e in entries)

    screen = turtle.Screen()
    screen.title("Mood chart")
    t = turtle.Turtle()
    t.speed("fastest")

    bar_width = 60
    spacing   = 20
    start_x   = -300

    # ---- Draw bars ----
    for i, (mood, n) in enumerate(counts.items()):
        x = start_x + i * (bar_width + spacing)
        height = n * 20
        t.penup(); t.goto(x, 0); t.pendown()
        t.begin_fill()
        for _ in range(2):
            t.forward(bar_width); t.left(90)
            t.forward(height);    t.left(90)
        t.end_fill()
        t.penup(); t.goto(x + bar_width/2 - 20, -25)
        t.write(f"{mood} ({n})", font=("Arial", 10, "normal"))

    screen.mainloop()
```

Screenshot or describe what your chart looks like:
```


```

---
