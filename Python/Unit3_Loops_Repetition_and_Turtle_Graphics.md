# Python Programming for Kids: Lesson Plans & Worksheets
## Unit 3: Loops, Repetition & Turtle Graphics (Sessions 13–18)

### Unit Overview
Unit 3 transforms students from learners who can write a single instruction into programmers who can command the computer to repeat work thousands of times in a fraction of a second. Building on the `while` loops introduced in Unit 2, this unit establishes the **definite `for` loop** with `range()`, then moves into the four canonical loop patterns explicitly named in Cambridge IGCSE 0478 §10 and Singapore O-Level 7155 Module 4: **totalling, counting, finding maximum/minimum, and computing averages**. Students then layer loops inside loops to produce grids and tables, master `break` and `continue` for early termination and skipping, and finally make iteration *visible* with the Turtle graphics module — drawing squares, polygons, spirals and stars where each side of the shape corresponds to one pass through the loop. The unit closes with a creative project: a **Geometric Art Generator** that combines user input, random colour choice, and nested loops to produce one-of-a-kind artwork. By the end of these six sessions, students will be able to read a problem, decide whether iteration is required, choose between `for` and `while`, write a correct loop, and trace its execution on paper — all of which are mandatory skills on both the Cambridge IGCSE 0478 paper and the Singapore O-Level 7155 paper.

---

### Session 13: For Loops & range()

---

#### SESSION 13 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 13 of 48 |
| **Title** | For Loops & range() |
| **Unit** | Unit 3: Loops, Repetition & Turtle Graphics |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | Lower Secondary Computing 0860 — Programming strand: count-controlled loops; IGCSE 0478 §10 Programming: iteration (FOR…NEXT, count-controlled), standard algorithms |
| **Singapore Alignment** | O-Level 7155 Module 4: Iteration constructs (count-controlled FOR loops), pseudocode-to-code translation |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Write** a Python `for` loop using `range(stop)`, `range(start, stop)` and `range(start, stop, step)` with at least 90% syntactic accuracy across five worksheet items.
2. **Predict** the exact output of a `for` loop containing up to 8 iterations using a written trace, with correct values for the loop variable in every row.
3. **Decide** whether a given problem should use a `for` loop or a `while` loop by applying the rule "known number of repetitions → for; condition-controlled → while" in at least 4 of 5 scenarios.
4. **Convert** a simple count-controlled `while` loop into an equivalent `for` loop, preserving identical output.

##### Materials Needed
- Thonny IDE (Python 3.11+) on each student computer
- Projector with teacher's Thonny session visible
- Printed Worksheet 13 (one per student, 4 pages)
- Whiteboard with three pre-drawn columns: `for variable`, `iterable`, `body`
- "Decision Card" handouts: 10 small cards listing scenarios (e.g. "print numbers 1 to 100", "keep asking until correct password")
- Pencil and ruler for trace tables

##### Procedure

**0–5 min: Warm-Up — "How many times?"**
Teacher writes on the board: *"Print HELLO 50 times."* Students whisper to a neighbour how they would do this with the `while` loop they learned in Unit 2. Teacher takes 2 quick answers, then writes:

```python
count = 0
while count < 50:
    print("HELLO")
    count += 1
```

Then says: *"This is correct — but Python has a faster, cleaner way. Today you'll learn it, and it's the one Cambridge and Singapore exam papers ask you to use whenever you know how many times to repeat."*

**5–15 min: Introduction — Anatomy of a `for` loop**
Teacher displays and reads aloud:

```python
for i in range(5):
    print("HELLO", i)
```

Annotate live on the projector:
- `for` — keyword, starts a count-controlled loop.
- `i` — the **loop variable**, takes a new value each pass.
- `in` — keyword, "draw the next value from".
- `range(5)` — produces the sequence `0, 1, 2, 3, 4` (note: **starts at 0, stops *before* 5**).
- `:` — required colon, like `if`.
- The indented `print(...)` — the **loop body**, runs once per value.

Run it. Output:
```
HELLO 0
HELLO 1
HELLO 2
HELLO 3
HELLO 4
```

Then introduce the three forms of `range`:

```python
# Form 1: range(stop) — start at 0
for i in range(4):
    print(i)        # 0, 1, 2, 3

# Form 2: range(start, stop) — start at 'start'
for i in range(2, 6):
    print(i)        # 2, 3, 4, 5

# Form 3: range(start, stop, step) — jump by 'step'
for i in range(0, 20, 5):
    print(i)        # 0, 5, 10, 15
```

Stress the **off-by-one rule**: `range(a, b)` produces `b - a` numbers; the value `b` itself is **never** included.

**15–35 min: Guided Practice — Building intuition through demos**

*Demo 1 — Iterating a string:*

```python
word = "PYTHON"
for letter in word:
    print(letter)
```

Run live. Ask students to predict the output before pressing F5. Confirm: each character on its own line.

*Demo 2 — Iterating a list (preview of Unit 4):*

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print("I like", fruit)
```

*Demo 3 — Counting backwards:*

```python
for i in range(10, 0, -1):
    print(i)
print("BLAST OFF!")
```

Pause: ask "what does the `-1` do?" Confirm: negative step counts down.

*Demo 4 — When NOT to use `for`:*

```python
# This problem has no known count — use while
password = ""
while password != "open":
    password = input("Password? ")
print("Welcome!")
```

Teacher draws the **decision tree** on the board:

```
Do I know HOW MANY times to repeat?
        |
   YES --+-- NO
    |         |
   for       while
   loop      loop
```

Students copy this into the back of their worksheet.

*Demo 5 — Convert a `while` to a `for`:*

```python
# Before (while)
n = 1
while n <= 5:
    print(n * n)
    n += 1

# After (for) — same output!
for n in range(1, 6):
    print(n * n)
```

Ask: "Why is the `for` version safer?" Elicit: no chance of forgetting the `n += 1` (the most common Unit 2 bug — the infinite loop).

**35–50 min: Independent Practice — Worksheet 13**
Students work through Parts 1, 2 and 3 of Worksheet 13. Teacher circulates, watching for two common errors:
- Writing `range(1, 5)` and expecting `1, 2, 3, 4, 5` (off-by-one).
- Forgetting indentation in the loop body — Thonny will underline this in red.

**50–55 min: Sharing & Discussion**
Two students share the output of their "convert while-to-for" answer on the projector. Class checks: are the outputs identical? Then a quick whole-class vote: scenario card — *"Print a multiplication table for 7 from 1 to 12"*: hands up for `for`, hands up for `while`. Discuss why `for` wins (count is known: 12).

**55–60 min: Closure & Preview**
Exit ticket on a sticky note: *"Write the one line that would print every even number from 2 to 20."* Expected answer: `for i in range(2, 21, 2): print(i)`. Preview Session 14: *"Tomorrow we'll use loops to add up numbers, count things, and find the biggest — these are the four patterns Cambridge exams ask about every year."*

##### Differentiation
- **Support:** Provide a "range-card" reference: a printed strip showing the output of `range(5)`, `range(2, 6)`, and `range(0, 10, 2)` side by side. Allow the student to use `print(list(range(...)))` to *see* what range produces before writing the loop.
- **Extension:** Challenge fast finishers with: "Use one `for` loop and `range` to print the sequence `100, 95, 90, …, 5`." Then: "Print only the multiples of 3 between 1 and 50 using a single `range` call (no `if`)."

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Syntax** | Misses `:` or indents incorrectly | One minor syntax error | Loops run with no errors | Loops run; chooses cleanest `range` form |
| **range() understanding** | Confuses start/stop | Off-by-one on stop value | Correct on all three forms | Uses negative step confidently |
| **for vs while choice** | Always picks the same one | 2/5 scenarios correct | 4/5 scenarios correct | 5/5 with verbal justification |
| **Trace accuracy** | Cannot list iteration values | Lists ≥ half of values | Lists all values correctly | Lists values + identifies last printed value |

##### Teacher Notes
- The off-by-one error on `range(stop)` is the single most common mistake — anticipate it and pre-empt it on the board: "stop *before* — you never reach stop."
- If a student types `for i in range(5,)` (extra comma), Thonny will accept it because `(5,)` is a tuple — confusing! Just remind them: one number, no comma.
- `range()` returns a *range object*, not a list; show `print(list(range(5)))` only briefly — the rabbit hole leads to lazy evaluation, which is a Year 11 topic.
- Praise students who say "I'll use a `for` because I know it loops 10 times" — verbalising the decision tree is a Cambridge mark-scheme phrase.
- Keep the keyword `for` and the variable name distinct: never use `for for in range(...)`. Suggest `i`, `n`, `count` or a meaningful name like `step`.

---

#### SESSION 13 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Predict the Output

For each code block, write what Python will print. **Do not run the code first** — predict, then check in Thonny.

**Q1.**
```python
for i in range(4):
    print(i)
```
Output: __________________________________________________

**Q2.**
```python
for i in range(2, 7):
    print(i, end=" ")
```
Output: __________________________________________________

**Q3.**
```python
for i in range(0, 20, 4):
    print(i)
```
Output: __________________________________________________

**Q4.**
```python
for i in range(10, 0, -2):
    print(i)
```
Output: __________________________________________________

**Q5.**
```python
for letter in "CODE":
    print(letter, "!")
```
Output: __________________________________________________

##### Part 2: Range Puzzles

Fill in the **`range(...)`** call so the loop produces exactly the output shown.

**Q6.** Output: `0 1 2 3 4 5 6 7 8 9`
```python
for i in range(__________):
    print(i, end=" ")
```

**Q7.** Output: `5 6 7 8 9 10`
```python
for i in range(__________, __________):
    print(i, end=" ")
```

**Q8.** Output: `1 3 5 7 9`
```python
for i in range(__________, __________, __________):
    print(i, end=" ")
```

**Q9.** Output: `20 15 10 5`
```python
for i in range(__________, __________, __________):
    print(i, end=" ")
```

**Q10.** Output: `100`
```python
for i in range(__________, __________):
    print(i)
```

##### Part 3: Convert `while` to `for`

Rewrite each `while` loop as a `for` loop that produces **exactly the same output**.

**Q11.**
```python
n = 1
while n <= 6:
    print("Bell rings", n)
    n += 1
```
Your `for` version:
```python
_______________________________________________________________
_______________________________________________________________
```

**Q12.**
```python
total = 0
n = 0
while n < 5:
    total += 10
    n += 1
print(total)
```
Your `for` version:
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

**Q13. Decision Tree.** Tick `for` or `while` for each scenario:

| # | Scenario | for | while |
|---|----------|-----|-------|
| a | Print "Happy Birthday" 3 times | ☐ | ☐ |
| b | Keep asking the user until they enter "yes" | ☐ | ☐ |
| c | Print every page number from 1 to 250 | ☐ | ☐ |
| d | Repeatedly roll a dice until you get a 6 | ☐ | ☐ |
| e | Print each letter of your school's name | ☐ | ☐ |

##### Reflection

1. What does `range(7)` produce? Write the actual sequence. _______________________________
2. In your own words, when do you choose a `for` loop over a `while` loop? _______________
3. Which question in Part 2 was hardest? Why? _________________________________________

##### Bonus / Stretch Challenge

Write a single `for` loop using one `range(...)` call (no `if`) that prints exactly:
```
3 6 9 12 15 18 21 24 27 30
```

Your code:
```python
_______________________________________________________________
_______________________________________________________________
```

**Super-bonus:** Write a `for` loop that prints the first 10 letters of `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` — but in **reverse** (so `J I H G F E D C B A`). *Hint: `range(start, stop, -1)` and string indexing.*

---

### Session 14: Loop Patterns — Totalling, Counting, Min/Max/Average

---

#### SESSION 14 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 14 of 48 |
| **Title** | Loop Patterns: Totalling, Counting, Min/Max/Average |
| **Unit** | Unit 3: Loops, Repetition & Turtle Graphics |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | IGCSE 0478 §10 Programming: standard algorithms — totalling, counting, max, min, average; pseudocode in section 11.2 |
| **Singapore Alignment** | O-Level 7155 Module 4: standard programming patterns; pseudocode `Total ← Total + value` |

##### Learning Objectives (SMART)
1. **Implement** the totalling pattern in Python to sum any list of numbers, achieving correct output on at least 3 different test datasets.
2. **Implement** the counting pattern to count items meeting a condition (e.g. scores ≥ 70), with correct counter initialisation and increment logic.
3. **Implement** the max-finding and min-finding patterns using the "first-element-as-initial-best" technique, correctly handling edge cases of one-element and all-equal lists.
4. **Combine** totalling and counting to compute an **average** (`total / count`) and explain in writing why dividing by zero must be avoided.

##### Materials Needed
- Thonny IDE
- Projector
- Printed Worksheet 14 (4 pages)
- Pre-printed handout titled *"The Four Standard Loop Patterns — Cambridge & Singapore reference"* (one per student)
- A class-survey "data set" written on the board (10 test scores: `78, 92, 65, 88, 73, 91, 60, 85, 79, 94`)

##### Procedure

**0–5 min: Warm-Up — "By Hand"**
Teacher writes on the board: *"Add these numbers in your head: 78, 92, 65, 88, 73."* Give 30 seconds. Ask: *"Now do 100 of them — and tell me how many are above 80, the highest, the lowest, and the average."* Wait for groans. *"Today the loop will do all of that for us — and these exact patterns are on Cambridge and Singapore exams every single year."*

**5–15 min: Introduction — Pattern 1: Totalling**

Display the canonical pattern:

```python
# Totalling pattern
nums = [78, 92, 65, 88, 73, 91, 60, 85, 79, 94]
total = 0                   # 1. start the accumulator at zero
for n in nums:              # 2. loop over every number
    total = total + n       # 3. add each one to the accumulator
print("Total:", total)
```

Teach the **three-line ritual**:
1. Initialise the accumulator (`total = 0`).
2. Loop.
3. `total = total + n` (or shorthand `total += n`).

Show the pseudocode side-by-side (the form they will see on Cambridge papers):

```
Total ← 0
FOR each n IN nums
    Total ← Total + n
NEXT n
OUTPUT Total
```

Run it. Output: `Total: 805`. Confirm by adding on a calculator.

**15–35 min: Guided Practice — Patterns 2, 3, 4**

*Pattern 2 — Counting*

```python
# How many scores are 80 or higher?
nums = [78, 92, 65, 88, 73, 91, 60, 85, 79, 94]
count = 0
for n in nums:
    if n >= 80:
        count += 1
print("Scores ≥ 80:", count)
```

Stress: **counter is separate from the loop variable**. Loop variable changes; counter only goes up when the condition is met.

*Pattern 3 — Finding Maximum*

```python
nums = [78, 92, 65, 88, 73, 91, 60, 85, 79, 94]
largest = nums[0]           # assume first is the biggest
for n in nums:
    if n > largest:
        largest = n         # found a bigger one — update
print("Largest:", largest)
```

Trace on the board: `largest` starts at 78. When `n` is 92, `92 > 78` → update. When `n` is 65, `65 > 92` is False → no update. Continue.

**Common bug to flag:** `largest = 0` (starts the variable at zero). Why is this wrong? *Because if all numbers are negative, `0` would wrongly remain the "largest". Always start with the first element of the data.*

*Pattern 4 — Finding Minimum*

```python
nums = [78, 92, 65, 88, 73, 91, 60, 85, 79, 94]
smallest = nums[0]
for n in nums:
    if n < smallest:
        smallest = n
print("Smallest:", smallest)
```

*Combine — Average*

```python
nums = [78, 92, 65, 88, 73, 91, 60, 85, 79, 94]
total = 0
count = 0
for n in nums:
    total += n
    count += 1
average = total / count
print("Average:", average)
```

Or, more concisely with `len()`:

```python
average = total / len(nums)
```

**Critical safety lesson — ZeroDivisionError:**

```python
# DANGEROUS!
nums = []                   # empty list
total = 0
count = 0
for n in nums:
    total += n
    count += 1
average = total / count     # CRASH: divide by zero
```

Show the error in Thonny live. Then fix:

```python
if count > 0:
    average = total / count
    print("Average:", average)
else:
    print("No data — cannot compute average.")
```

**35–50 min: Independent Practice — Worksheet 14**

**50–55 min: Sharing & Discussion**
A volunteer projects their Q5 (mini exam-stats calculator). Class checks the output against the board's dataset of 10 scores: total = 805, average = 80.5, highest = 94, lowest = 60, count ≥ 80 = 6.

**55–60 min: Closure & Preview**
Exit ticket: *"Write the three lines that find the largest of a list called `data`."* Expected:
```python
largest = data[0]
for n in data:
    if n > largest: largest = n
```
Preview Session 15: *"Now we put loops INSIDE loops — and we draw multiplication tables and rectangles of stars."*

##### Differentiation
- **Support:** Provide a fill-in-the-blank scaffold for each pattern (just the keyword, the rest blank). Allow students to first sum 3 numbers by hand on the trace table, then write code.
- **Extension:** Compute the **range** (`largest - smallest`) and the **count of below-average** scores in the same pass. Then: write a function `def stats(nums):` that returns all four values as a tuple (preview Unit 5).

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Totalling pattern** | Forgets to initialise `total = 0` | Initialises but forgets `+=` | Correct on all datasets | Uses `+=` shorthand fluently |
| **Counting pattern** | Confuses counter and loop var | Counts but condition wrong | Correct counter logic | Adds explanation of when to increment |
| **Max/Min** | Initialises with `0` (bug!) | Picks correct initial element on trivial cases | Always uses `nums[0]` | Discusses negative-numbers edge case |
| **Average / safety** | Forgets division entirely | Computes but ignores zero-div | Computes; guards with `if count > 0` | Explains zero-division in writing |

##### Teacher Notes
- These four patterns are the single highest-yield content of the entire course for exam preparation. Reinforce vocabulary: "accumulator", "counter", "running maximum".
- Watch for `total = total + n` typed *outside* the loop (not indented) — it will only execute once. Thonny's red squiggles help.
- The `largest = 0` bug is a brilliant teaching moment. Pre-plan a list of all-negative numbers: `[-5, -8, -2, -10]` — running with `largest = 0` returns 0, which clearly is not in the list. Eureka.
- Singapore O-Level pseudocode uses `←` (left-arrow) for assignment. Mention it once; Python uses `=`. Don't confuse but don't hide.
- If time allows, show the built-in shortcuts `sum(nums)`, `max(nums)`, `min(nums)` at the very end — but say firmly: *"You must be able to write the loop yourself for the exam."*

---

#### SESSION 14 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Implement the Patterns from Pseudocode

Translate each piece of pseudocode into working Python. Use the dataset `prices = [12, 8, 15, 22, 9, 30, 7, 18]`.

**Q1. Totalling**
```
Total ← 0
FOR each p IN prices
    Total ← Total + p
NEXT p
OUTPUT Total
```
Your Python:
```python
prices = [12, 8, 15, 22, 9, 30, 7, 18]
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```
Expected output: `121`

**Q2. Counting**
```
Count ← 0
FOR each p IN prices
    IF p > 15 THEN
        Count ← Count + 1
    ENDIF
NEXT p
OUTPUT Count
```
Your Python:
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```
Expected output: `3`

**Q3. Maximum**
Write Python that prints the largest item in `prices`. Use the `largest = prices[0]` pattern.
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

**Q4. Average**
Write Python that prints the average of `prices`, **safely guarded** against an empty list.
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

##### Part 2: Find the Bug

Each program below has **one bug**. Circle it and write a correction.

**Q5. Bug A**
```python
nums = [4, 7, 2, 9, 5]
total = 0
for n in nums:
total = total + n
print(total)
```
Bug: ____________________________________________________
Fix: ____________________________________________________

**Q6. Bug B**
```python
nums = [-3, -7, -1, -8]
largest = 0
for n in nums:
    if n > largest:
        largest = n
print("Largest:", largest)
```
What does this print? __________   What *should* it print? __________
Bug: ____________________________________________________
Fix: ____________________________________________________

**Q7. Bug C**
```python
scores = [50, 60, 70, 80, 90]
count = 0
for s in scores:
    if s > 70:
        count = 1
print("Above 70:", count)
```
Bug: ____________________________________________________
Fix: ____________________________________________________

**Q8. Bug D**
```python
nums = []
total = 0
for n in nums:
    total += n
average = total / len(nums)
print(average)
```
Bug: ____________________________________________________
Fix: ____________________________________________________

##### Part 3: Mini Project — Exam Stats Calculator

Using the class dataset `scores = [78, 92, 65, 88, 73, 91, 60, 85, 79, 94]`, write **one program** that prints all of the following:

1. Total of all scores
2. Number of scores
3. Average (rounded to 1 decimal place — use `round(average, 1)`)
4. Highest score
5. Lowest score
6. Number of scores ≥ 80
7. Number of scores below 70

Your full program (use the space, additional sheet allowed):
```python
scores = [78, 92, 65, 88, 73, 91, 60, 85, 79, 94]

# Your code here
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

**Trace Table — first 4 iterations of finding the largest:**

| Iteration | n | n > largest? | largest after |
|-----------|---|--------------|---------------|
| 1 | 78 | 78 > 78? No | 78 |
| 2 | 92 | _________ | _________ |
| 3 | 65 | _________ | _________ |
| 4 | 88 | _________ | _________ |

##### Reflection

1. Why must we initialise `total = 0` *before* the loop, not inside it? __________________
2. Why is `largest = nums[0]` safer than `largest = 0`? _____________________________
3. What happens if you try to compute an average of an empty list, and how do you guard against it? ________________________________________________________________

##### Bonus / Stretch Challenge

Add to your exam-stats program: **count how many scores are *exactly* equal to the highest**. (For our dataset that should be 1, but if 94 appeared twice, the answer would be 2.) Write a *second* loop after you find `largest`:
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

**Super-bonus:** Compute the **median** (middle value when sorted). *Hint:* Python's `sorted(scores)` gives a sorted copy; for 10 numbers, the median is `(sorted_scores[4] + sorted_scores[5]) / 2`.

---

### Session 15: Nested Loops

---

#### SESSION 15 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 15 of 48 |
| **Title** | Nested Loops |
| **Unit** | Unit 3: Loops, Repetition & Turtle Graphics |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | IGCSE 0478 §10: nested iteration; ability to dry-run nested algorithms with a trace table |
| **Singapore Alignment** | O-Level 7155 Module 4: nested loops; tracing programs with multi-variable trace tables |

##### Learning Objectives (SMART)
1. **Construct** a nested `for` loop with an outer loop variable and a separate inner loop variable, ensuring correct indentation in Thonny.
2. **Trace** a nested loop with outer range 3 and inner range 3 producing all 9 iteration pairs in a complete trace table without omission.
3. **Generate** a multiplication table (1×1 to 10×10) printed as an aligned grid, demonstrating mastery of `print(..., end="\t")` and the empty `print()` line break.
4. **Diagnose** at least two indentation-related bugs (inner statements at wrong level) and explain in writing how Thonny's red squiggles helped locate them.

##### Materials Needed
- Thonny IDE
- Projector
- Printed Worksheet 15 (4 pages)
- Trace-table sheet pre-printed with 9 empty rows for the warm-up
- Optional: physical objects (counters, coins) to physically simulate outer/inner

##### Procedure

**0–5 min: Warm-Up — "Outer and Inner"**
Teacher holds two stacks of coloured counters. *"Imagine I have 3 plates (outer) and on each plate I put 4 cookies (inner). How many cookies?"* (12.) *"Today loops will do exactly this — for every plate, run through every cookie."*

**5–15 min: Introduction — Loop inside a loop**

Display:

```python
for i in range(3):              # outer loop: 3 times
    for j in range(2):          # inner loop: 2 times PER outer
        print("i =", i, "j =", j)
```

Run it. Output:
```
i = 0 j = 0
i = 0 j = 1
i = 1 j = 0
i = 1 j = 1
i = 2 j = 0
i = 2 j = 1
```

Crucial observation: the inner loop runs to completion **for every single value of the outer loop**. Total iterations = `3 × 2 = 6`.

Annotate on the projector:
- The outer `for` is at column 0 (no indent).
- The inner `for` is at column 4 (one indent).
- The body `print` is at column 8 (two indents).

Stress: *"In Thonny, indentation is not optional. The number of spaces tells Python which loop a line belongs to."*

**15–35 min: Guided Practice — Three classic uses**

*Use 1 — Times-table generator*

```python
# Times tables 1 to 10
for row in range(1, 11):
    for col in range(1, 11):
        product = row * col
        print(product, end="\t")    # \t = tab, aligns columns
    print()                          # newline after each row
```

Run it. The output is a beautifully aligned 10×10 grid. Discuss `\t` (tab character) and the bare `print()` to break the line.

*Use 2 — Drawing a rectangle of stars*

```python
height = 4
width = 7
for r in range(height):
    for c in range(width):
        print("*", end="")
    print()
```

Output:
```
*******
*******
*******
*******
```

Then a triangle:

```python
for r in range(1, 6):
    for c in range(r):
        print("*", end="")
    print()
```

Output:
```
*
**
***
****
*****
```

Pause. Ask the class to predict why the inner range is `range(r)` not `range(5)`. Confirm: as `r` grows, more stars print.

*Use 3 — Full trace table for a 3×3 nested loop*

```python
for i in range(3):
    for j in range(3):
        print(i, j)
```

Teacher fills in on the board (students copy):

| Step | i | j | output |
|------|---|---|--------|
| 1 | 0 | 0 | 0 0 |
| 2 | 0 | 1 | 0 1 |
| 3 | 0 | 2 | 0 2 |
| 4 | 1 | 0 | 1 0 |
| 5 | 1 | 1 | 1 1 |
| 6 | 1 | 2 | 1 2 |
| 7 | 2 | 0 | 2 0 |
| 8 | 2 | 1 | 2 1 |
| 9 | 2 | 2 | 2 2 |

*Common bug demo:*

```python
# WRONG — print is at outer level, runs only 3 times
for i in range(3):
    for j in range(3):
        pass
    print(i, j)
```

This prints `0 2`, `1 2`, `2 2` — only 3 lines, and `j` keeps the value 2 from the last inner iteration! Show in Thonny so students see the consequence of indentation.

**35–50 min: Independent Practice — Worksheet 15**

**50–55 min: Sharing & Discussion**
Two students share their multiplication-table output. Discuss how `\t` produces the tab alignment. Then the class votes on which star pattern (Q4, Q5, Q6) was hardest.

**55–60 min: Closure & Preview**
Exit ticket: *"How many lines does a nested loop with `for i in range(4): for j in range(5): print(...)` print?"* (20.) Preview Session 16: *"Sometimes we want to STOP a loop early or SKIP one iteration — that's `break` and `continue`."*

##### Differentiation
- **Support:** Reduce dimensions: ask for a 2×3 grid before a 10×10 table. Provide a half-filled trace table.
- **Extension:** Draw a hollow rectangle (stars only on the border, spaces inside). This requires combining nested loops with `if` conditions on `r` and `c`.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Indentation** | Inner statements at wrong level | Mostly correct, occasional drift | Always correct | Uses Thonny's auto-indent confidently |
| **Trace table** | Misses ≥ 3 rows | Misses 1–2 rows | All 9 rows correct | Adds total-iterations comment |
| **Times table** | No alignment | Misaligned but all 100 products | Aligned via `\t` | Adds row/column headers |
| **Star pattern** | One pattern correct | Two patterns correct | All three patterns correct | Designs a 4th pattern of own choice |

##### Teacher Notes
- The single biggest hazard is mis-indentation. Encourage students to always use Thonny's Tab key, never spaces by hand.
- Reinforce vocabulary: "outer loop", "inner loop". Write both on the board and label the live demo.
- Multiplication tables are a Singapore O-Level favourite — be sure students can produce one **without** consulting notes by end-of-session.
- If students ask "can I have three nested loops?": yes, but the trace table grows by orders of magnitude. Demo `range(2)` × 3 = 8 iterations briefly, then warn that human-traceable code rarely nests deeper than 2.
- The `print(end="")` trick (no newline) is essential for in-row printing and worth a 30-second tangent if any student doesn't recognise it from earlier units.

---

#### SESSION 15 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Trace the Nested Loop

**Q1.** Complete every row of the trace table:
```python
for i in range(2):
    for j in range(4):
        print(i, j)
```

| Step | i | j | Output line |
|------|---|---|-------------|
| 1 | 0 | 0 | 0 0 |
| 2 | 0 | _ | _____ |
| 3 | 0 | _ | _____ |
| 4 | 0 | _ | _____ |
| 5 | _ | _ | _____ |
| 6 | _ | _ | _____ |
| 7 | _ | _ | _____ |
| 8 | _ | _ | _____ |

Total lines printed: ________

**Q2.** How many iterations of the **inner** loop run in total? __________
How many iterations of the **outer** loop run? __________

##### Part 2: Predict the Star Pattern

For each program, draw the exact output in the box.

**Q3.**
```python
for r in range(3):
    for c in range(5):
        print("*", end="")
    print()
```
Output:
```
________________________________________
________________________________________
________________________________________
```

**Q4.**
```python
for r in range(1, 5):
    for c in range(r):
        print("#", end="")
    print()
```
Output:
```
________________________________________
________________________________________
________________________________________
________________________________________
```

**Q5.**
```python
for r in range(4, 0, -1):
    for c in range(r):
        print("@", end="")
    print()
```
Output:
```
________________________________________
________________________________________
________________________________________
________________________________________
```

**Q6. Predict the output WITHOUT running:**
```python
for i in range(3):
    for j in range(3):
        if i == j:
            print("X", end="")
        else:
            print(".", end="")
    print()
```
Output:
```
________________________________________
________________________________________
________________________________________
```

##### Part 3: Build the Multiplication Table

**Q7.** Write a program that prints the multiplication table for 1 × 1 up to 12 × 12, separated by tabs (`\t`), with each row on a new line. Add a header row showing column numbers 1 through 12.

Your code:
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

**Q8. Indentation Bug Hunt.** This program is supposed to print a 3×3 grid of letters, but it doesn't. Identify the bug:
```python
for r in range(3):
    for c in range(3):
        print("A", end="")
        print()
```
Bug description: ____________________________________________________________
Fix (rewrite correctly):
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

##### Reflection

1. Explain in your own words: when the outer loop runs once, how many times does the inner loop run? ____________________________________________________________
2. What does an **empty** `print()` (no arguments) do at the end of an inner loop? ________
3. Why is indentation so important in nested loops? __________________________________

##### Bonus / Stretch Challenge

**Hollow square:** Print a 5×5 square where the **border** is `*` and the **inside** is a space `' '`. Use one nested loop and one `if`.
Expected:
```
*****
*   *
*   *
*   *
*****
```
Your code:
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

**Super-bonus:** Print a multiplication grid of just the prime products under 50 — for each pair `(i, j)` where `i*j` is prime, print the product; otherwise print `.`. (Hint: 2 is the only even prime.)

---

### Session 16: Loop Control — break & continue

---

#### SESSION 16 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 16 of 48 |
| **Title** | Loop Control: break & continue |
| **Unit** | Unit 3: Loops, Repetition & Turtle Graphics |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | IGCSE 0478 §10: early termination of iteration; standard search algorithm with break |
| **Singapore Alignment** | O-Level 7155 Module 4: control flow within loops; linear search algorithm |

##### Learning Objectives (SMART)
1. **Use** `break` to terminate a loop the moment a target is found, applying the standard linear-search pattern correctly.
2. **Use** `continue` to skip a single iteration without exiting the loop, with at least 95% accuracy on the worksheet's predict-the-output items.
3. **Decide** whether `break`, `continue` or neither is appropriate for a given problem, justifying the choice in writing.
4. **Refactor** a `break`-based loop into a clean equivalent without `break` (using a flag variable) and compare readability.

##### Materials Needed
- Thonny IDE
- Projector
- Printed Worksheet 16 (4 pages)
- "Search-and-stop" demo dataset on the board: `[5, 12, 8, 21, 3, 17, 9]` and target `21`

##### Procedure

**0–5 min: Warm-Up — "Find My Pen"**
Teacher hides a pen in one of 7 boxes on the desk. *"You're checking each box. The moment you find the pen — what do you do?"* Class: *"Stop checking!"* *"Exactly. Today the keyword is `break`."*

**5–15 min: Introduction — `break`**

Naïve search:
```python
nums = [5, 12, 8, 21, 3, 17, 9]
target = 21
for n in nums:
    if n == target:
        print("Found!")
```

This works — but Python keeps checking every single number after finding 21. Wasteful. Now the standard pattern:

```python
nums = [5, 12, 8, 21, 3, 17, 9]
target = 21
for n in nums:
    if n == target:
        print("Found!")
        break               # exit the loop NOW
```

Run with a `print("Checking", n)` inserted to show the difference: with `break`, only checks 5, 12, 8, 21 — then stops.

Teach the **search-and-stop pattern** (Cambridge mark scheme exact wording):
```
FOR each item IN list
    IF item = target THEN
        OUTPUT "Found"
        EXIT FOR
    ENDIF
NEXT item
```

`break` is Python's `EXIT FOR`.

Now `continue`:

```python
# Print all numbers EXCEPT multiples of 3
for n in range(1, 11):
    if n % 3 == 0:
        continue            # skip THIS one, go to next n
    print(n, end=" ")
```

Output: `1 2 4 5 7 8 10`. Note: `continue` does NOT exit the loop — it jumps to the next iteration.

**15–35 min: Guided Practice — When to use which**

*Scenario 1 — Search (use `break`):*
```python
names = ["Aiden", "Mei", "Rafi", "Siti", "Daniel"]
search = "Rafi"
found = False
for name in names:
    if name == search:
        found = True
        break
if found:
    print(search, "is in the list")
else:
    print(search, "is NOT in the list")
```

*Scenario 2 — Filter (use `continue`):*
```python
# Only print positive numbers
nums = [4, -2, 7, -5, 0, 9, -1]
for n in nums:
    if n <= 0:
        continue
    print(n)
```

*Scenario 3 — Refactor `break` away (with a flag):*

The `break` version:
```python
nums = [10, 20, 30, 40, 50]
for n in nums:
    if n > 25:
        print("Found one bigger than 25:", n)
        break
```

The `while`+flag refactor:
```python
nums = [10, 20, 30, 40, 50]
i = 0
found = False
while i < len(nums) and not found:
    if nums[i] > 25:
        print("Found one bigger than 25:", nums[i])
        found = True
    i += 1
```

Discuss: which is easier to read? Most students will prefer `break`. *"That's the case where `break` wins. But sometimes — when the condition is part of `while` — using a flag is cleaner."*

*Caution (mention briefly, do not dwell):* Overusing `break`/`continue` can make code hard to follow. Rule of thumb: at most one of each per loop, near the top of the body.

*Trace exercise — done together:*
```python
for i in range(5):
    if i == 2:
        continue
    if i == 4:
        break
    print(i)
```

Trace:

| i | i==2? | i==4? | print? | output |
|---|-------|-------|--------|--------|
| 0 | No | No | Yes | 0 |
| 1 | No | No | Yes | 1 |
| 2 | Yes → continue | — | No | — |
| 3 | No | No | Yes | 3 |
| 4 | No | Yes → break | No | — |

Final output: `0`, `1`, `3`.

**35–50 min: Independent Practice — Worksheet 16**

**50–55 min: Sharing & Discussion**
A student reads aloud their refactor of `break` into a flag-based `while`. Class votes on which is easier to read.

**55–60 min: Closure & Preview**
Exit ticket: *"What is the difference between `break` and `continue`, in one sentence?"* Expected: *"`break` exits the whole loop; `continue` skips just one iteration."* Preview Session 17: *"Tomorrow we draw with the Turtle — and every shape is a loop in disguise."*

##### Differentiation
- **Support:** Provide a "decision card" with two scenarios per side, students physically point to "break" or "continue".
- **Extension:** Implement a **bounded linear search** that returns the *index* of the found item (preview Unit 4): `for i in range(len(nums)): if nums[i] == target: print(i); break`.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **break usage** | Confuses with continue | Uses but in wrong place | Uses correctly in search | Adds `else` clause to for-loop (extension) |
| **continue usage** | Skips wrong iteration | Mostly correct | Correct on all worksheet items | Combines with `break` cleanly |
| **Decision making** | Cannot articulate when | 1/3 scenarios correct | 3/3 scenarios correct | Justifies in writing |
| **Refactor** | Cannot refactor | Refactor compiles but bug | Refactor produces same output | Compares readability with insight |

##### Teacher Notes
- A clean test of understanding: after the trace exercise, ask "what would happen if we swapped lines 2–3 with lines 4–5?" (i.e., put the `break` first.) Some students will see immediately, others will need to trace.
- Some Python authors discourage `break` in favour of structured loops. For exam preparation, both Cambridge and Singapore explicitly include `EXIT FOR` / break — so we teach it confidently.
- `break` only exits the **innermost** loop. If a student wants to exit a nested loop entirely, they need a flag or a function `return`. Mention briefly only.
- Watch for `continue` followed by code under the same `if` — that code never runs. Thonny will warn with "Unreachable code" in some versions.
- The `for…else:` clause (else runs if the loop completes without `break`) is Python-specific and useful — show only as enrichment.

---

#### SESSION 16 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Trace `break` and `continue`

**Q1.** Predict the output:
```python
for i in range(6):
    if i == 3:
        break
    print(i)
```
Output: __________________________________

**Q2.** Predict the output:
```python
for i in range(6):
    if i == 3:
        continue
    print(i)
```
Output: __________________________________

**Q3.** Complete the trace table:
```python
for n in range(1, 8):
    if n % 2 == 0:
        continue
    if n > 5:
        break
    print(n)
```

| n | n%2==0? | n>5? | print? | output |
|---|---------|------|--------|--------|
| 1 | _____ | _____ | _____ | _____ |
| 2 | _____ | _____ | _____ | _____ |
| 3 | _____ | _____ | _____ | _____ |
| 4 | _____ | _____ | _____ | _____ |
| 5 | _____ | _____ | _____ | _____ |
| 6 | _____ | _____ | _____ | _____ |
| 7 | _____ | _____ | _____ | _____ |

Final output: __________________________________

##### Part 2: Search-and-Stop

**Q4.** A list `students = ["Ali", "Bea", "Cai", "Devi", "Eshan"]`. Write a `for` loop that **stops as soon as** it finds `"Cai"` and prints `Found Cai!`. Use `break`.
```python
students = ["Ali", "Bea", "Cai", "Devi", "Eshan"]
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

**Q5.** Modify Q4 to also print `Searched for Z, not in list.` when the target is `"Zoe"`. (Hint: use a `found` flag.)
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

##### Part 3: Refactor & Compare

**Q6.** Here is a loop using `break`:
```python
nums = [3, 7, 11, 15, 19, 23, 27]
for n in nums:
    if n > 12:
        print("First bigger than 12:", n)
        break
```
Rewrite this **without `break`**, using a `while` loop and a `found` flag. Output must be identical.
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

Which version do you find easier to read, and why? __________________________________

**Q7.** Decision time — for each scenario, write `break`, `continue` or `neither`:

| # | Scenario | Choice |
|---|----------|--------|
| a | Print all numbers from 1–20 except the multiples of 4 | _______ |
| b | Find a missing book in a list of 50 books and stop searching | _______ |
| c | Sum every number in a list — no skipping, no stopping | _______ |
| d | Print every word in a sentence except the word "the" | _______ |
| e | Check passwords until the correct one is entered | _______ |

##### Reflection

1. In one sentence, what does `break` do? __________________________________________
2. In one sentence, what does `continue` do? _______________________________________
3. Why might overusing `break` make code harder to read? __________________________

##### Bonus / Stretch Challenge

**Q8.** Use `for…else` (Python's special construction):
```python
nums = [2, 4, 6, 8]
for n in nums:
    if n == 5:
        print("Found 5!")
        break
else:
    print("5 not in list")
```
Predict output: ____________________________

Now change `nums` so that the **`else` does NOT** run, and write the new list:
`nums = [_______________________________]`

**Super-bonus:** Write a single `for` loop that prints the first 5 prime numbers from a list of 100 candidates, then stops. Use both `continue` (to skip non-primes) and `break` (to stop after 5 found).

---

### Session 17: Turtle Graphics with Loops

---

#### SESSION 17 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 17 of 48 |
| **Title** | Turtle Graphics with Loops |
| **Unit** | Unit 3: Loops, Repetition & Turtle Graphics |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0860 / IGCSE 0478 §10: iteration applied to a problem domain; visualising algorithm execution |
| **Singapore Alignment** | O-Level 7155 Module 4: applying iteration to graphical problems; parameterising procedures |

##### Learning Objectives (SMART)
1. **Initialise** a `turtle` Screen and Turtle object correctly, and end the program with `screen.exitonclick()` so the window stays open until clicked.
2. **Draw** a square, equilateral triangle, regular hexagon and regular pentagon using a `for` loop and the formula `exterior angle = 360 / sides`, with each shape closing exactly back to the start.
3. **Combine** loops with colour and pen-size commands to produce at least two creative patterns (spiral, star), choosing parameters appropriately.
4. **Generalise** a square-drawing routine into a function/loop that accepts any number of sides and any side length (preview of Unit 5 functions).

##### Materials Needed
- Thonny IDE with `turtle` module (built-in)
- Projector
- Printed Worksheet 17 (4 pages, includes drawing-grid templates)
- Coloured pencils for sketching predicted shapes

##### Procedure

**0–5 min: Warm-Up — "Walk a Square"**
Teacher asks a student volunteer to walk a square shape across the front of the room. Class chants the instructions: *"Forward 5 paces. Turn right 90°. Forward 5. Turn right 90. Forward 5. Turn right 90. Forward 5."* Notice — same two instructions repeated 4 times. **That's a loop.**

**5–15 min: Introduction — Meet the Turtle**

```python
import turtle

screen = turtle.Screen()
screen.bgcolor("white")

t = turtle.Turtle()
t.shape("turtle")
t.color("blue")
t.pensize(3)

# Draw a square — the long way
t.forward(100)
t.right(90)
t.forward(100)
t.right(90)
t.forward(100)
t.right(90)
t.forward(100)
t.right(90)

screen.exitonclick()
```

Run together. Watch the turtle move. Then refactor with a loop:

```python
import turtle

screen = turtle.Screen()
t = turtle.Turtle()
t.color("blue")
t.pensize(3)

for _ in range(4):
    t.forward(100)
    t.right(90)

screen.exitonclick()
```

Note the `_` (underscore) — Pythonic convention for "I don't care about the loop variable."

**Core commands recap (write on board):**
- `t.forward(n)` / `t.backward(n)` — move n pixels.
- `t.right(deg)` / `t.left(deg)` — turn in place.
- `t.penup()` / `t.pendown()` — stop / start drawing while moving.
- `t.color("red")` — change line colour. Strings: red, blue, green, orange, purple, pink, black, white, etc.
- `t.pensize(n)` — line thickness.
- `t.goto(x, y)` — jump to coordinate.
- `screen.exitonclick()` — keep window open until user clicks.
- `turtle.done()` — alternative ending.

**15–35 min: Guided Practice — Polygons by formula**

The **key formula**: for a regular polygon with `n` sides, the turtle must turn through the **exterior angle** = `360 / n` at each corner.

```python
# Equilateral triangle: 360/3 = 120°
for _ in range(3):
    t.forward(100)
    t.right(120)
```

```python
# Regular pentagon: 360/5 = 72°
for _ in range(5):
    t.forward(100)
    t.right(72)
```

```python
# Regular hexagon: 360/6 = 60°
for _ in range(6):
    t.forward(100)
    t.right(60)
```

```python
# Regular octagon: 360/8 = 45°
for _ in range(8):
    t.forward(100)
    t.right(45)
```

**Parameterise with variables** (preparation for Unit 5):

```python
sides = 12
length = 60
angle = 360 / sides
for _ in range(sides):
    t.forward(length)
    t.right(angle)
```

Change `sides = 50` and re-run — the result is almost a circle! Discuss: as sides → infinity, polygon → circle. (The Greeks knew this.)

*Spiral:*
```python
t.speed(0)                  # 0 = fastest
length = 5
for _ in range(60):
    t.forward(length)
    t.right(91)             # 91 not 90 — this gives the spiral effect
    length += 3
```

*Five-pointed star:*
```python
t.color("gold")
for _ in range(5):
    t.forward(100)
    t.right(144)            # 144° turn → 5-pointed star
```

*Coloured polygon — `random.choice`:*
```python
import random
colours = ["red", "blue", "green", "orange", "purple"]
for _ in range(6):
    t.color(random.choice(colours))
    t.forward(80)
    t.right(60)
```

**35–50 min: Independent Practice — Worksheet 17**

**50–55 min: Sharing & Discussion**
Each student turns their screen to face their neighbour for a 90-second "gallery walk". Pick 2–3 to project on the board. Discuss: which polygon was hardest? Why does `91` produce a spiral but `90` produce a square forever?

**55–60 min: Closure & Preview**
Exit ticket: *"What is the exterior angle for a regular polygon with 9 sides?"* (40°.) Preview Session 18: *"Tomorrow you design and build your own art generator — pseudocode first, code second."*

##### Differentiation
- **Support:** Provide a starter file with the `import` and screen setup already written. Allow students to copy and paste the pentagon code and modify only the `sides` and `angle`.
- **Extension:** Draw a **flower** by drawing 12 squares each rotated 30° from the last (a nested loop: outer = 12 squares, inner = 4 sides per square). Add `t.circle(50)` at the end as a centre.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Setup** | Forgets `import` or `exitonclick` | One missing element | Setup runs cleanly | Adds bgcolor, speed, shape |
| **Square via loop** | Cannot loop, draws by hand | Loop draws but doesn't close | Square closes correctly | Uses `_` and parameterises length |
| **Polygon formula** | Random angles | Two of {tri, hex, oct} correct | All four polygons correct | Generates n-sided polygon from variable |
| **Creative pattern** | None attempted | Spiral or star, single colour | Spiral AND star, with colour | Designs an original pattern |

##### Teacher Notes
- The turtle window can sit *behind* Thonny on macOS — show students how to find it (Cmd-Tab or click in dock).
- If multiple students keep reopening the turtle window, performance drops. Encourage `screen.exitonclick()` at the end every time.
- `t.speed(0)` is the fastest; `t.speed(1)` is the slowest. Default is `3`.
- Some students will discover `t.circle(r)` — fine, but redirect to polygon-via-loop as the learning goal.
- The exterior-angle formula `360 / n` is a powerful generaliser; some Year 7 students will recognise it from maths. Make the cross-curricular link explicit.
- Save students' files as `session17_<name>.py` so they can return to them in Session 18.

---

#### SESSION 17 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Predict the Shape

For each program, draw what the turtle produces in the grid box. Put a small dot where the turtle starts, and an arrow showing where it ends up.

**Q1.**
```python
for _ in range(4):
    t.forward(80)
    t.right(90)
```
Drawing:
```
+----------------+
|                |
|                |
|                |
|                |
+----------------+
```
Shape name: ________________

**Q2.**
```python
for _ in range(3):
    t.forward(80)
    t.right(120)
```
Drawing:
```
+----------------+
|                |
|                |
|                |
|                |
+----------------+
```
Shape name: ________________

**Q3.**
```python
for _ in range(6):
    t.forward(60)
    t.right(60)
```
Shape name: ________________   Number of sides: ____

**Q4.**
```python
for _ in range(5):
    t.forward(80)
    t.right(144)
```
Shape name: ________________   (Hint: not a polygon — a famous shape!)

##### Part 2: Polygon Formula

**Q5.** Complete the table using the formula `exterior angle = 360 / sides`:

| Shape | Sides | Exterior angle |
|-------|-------|----------------|
| Triangle | 3 | _____ |
| Square | 4 | _____ |
| Pentagon | 5 | _____ |
| Hexagon | 6 | _____ |
| Octagon | 8 | _____ |
| Decagon | 10 | _____ |
| 12-gon | 12 | _____ |
| 36-gon | 36 | _____ |

**Q6.** Write a complete program (with `import` and `exitonclick`) that draws a regular **nonagon** (9 sides). Each side should be 70 pixels.
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

##### Part 3: Parameterise the Shape

**Q7.** Rewrite the polygon code so the **number of sides** and **side length** are variables at the top. Then test with three combinations: (3, 100), (8, 50), (20, 30).
```python
import turtle
screen = turtle.Screen()
t = turtle.Turtle()

sides = ______
length = ______
angle = ______________________

_______________________________________________________________
_______________________________________________________________
_______________________________________________________________

screen.exitonclick()
```

**Q8.** Change `sides` to `100`. Describe what the result looks like and why:
________________________________________________________________________________
________________________________________________________________________________

##### Reflection

1. Why is `for _ in range(4)` better than writing four `forward/right` pairs by hand? ____
2. What is the relationship between the number of sides and the turn angle? __________
3. What does `screen.exitonclick()` do, and why is it essential? _____________________

##### Bonus / Stretch Challenge

**Q9. Coloured spiral.** Use `random.choice` to pick a colour for each segment from `["red","blue","green","gold","purple"]`. Draw 50 segments, each one 5 pixels longer than the last, turning 91° each time.
```python
import turtle, random
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

**Super-bonus: rosette.** Use a nested loop: the outer loop runs 18 times. Inside, draw a square (inner loop of 4). Between squares, turn 20°. The result is a flower of 18 squares.

---

### Session 18: Project 3 — Geometric Art Generator

---

#### SESSION 18 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 18 of 48 |
| **Title** | Project 3: Geometric Art Generator |
| **Unit** | Unit 3: Loops, Repetition & Turtle Graphics |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0860 / IGCSE 0478: design (pseudocode + flowchart), implementation, testing of an iterative algorithm; review and refinement |
| **Singapore Alignment** | O-Level 7155 Module 4: program design and implementation; structured programming with iteration; design documentation |

##### Learning Objectives (SMART)
1. **Design** a geometric art piece by writing pseudocode and drawing a flowchart that includes user input, at least one loop, and at least one decision/random choice.
2. **Build** a working Python program (≥ 25 lines) that takes user input (number of shapes, sides, palette), uses `random.choice` for colours, and uses **nested loops** to compose a pattern.
3. **Test** the program with at least three different input sets, recording each result with a screenshot or sketch in the project log.
4. **Critique** a peer's work using the rubric provided, giving one specific praise and one specific suggestion for improvement.

##### Materials Needed
- Thonny IDE
- Projector
- Printed Worksheet 18 (project planning template, 5 pages)
- Coloured pencils, blank paper for sketches
- Optional: phones to take screenshots; a class folder to drop them in

##### Procedure

**0–5 min: Warm-Up — Gallery of inspiration**
Teacher displays 4 pre-made art examples on the projector: a rosette (18 squares rotating), a coloured spiral, a star field (random small stars), a polygon-stack (concentric polygons of growing size). *"Today you design YOUR own — but first, you plan."*

**5–15 min: Introduction — The design phase**

Whiteboard the planning ritual:

1. **Title** — name the artwork.
2. **Sketch** — pencil drawing of intended output.
3. **Inputs** — what does the user provide? (e.g. number of shapes, side length range, palette choice 1–3.)
4. **Pseudocode** — high-level steps in plain English.
5. **Flowchart** — the canonical Cambridge symbols (oval = start/end, parallelogram = input/output, rectangle = process, diamond = decision).
6. **Code** — only after 1–5.

Demo planning a "Random Polygon Burst":

```
Title: Random Polygon Burst
Inputs:
  - num_shapes (integer, e.g. 12)
  - sides (integer, e.g. 5)
  - palette: list of 5 colours
Pseudocode:
  Set up screen and turtle
  Ask user for num_shapes and sides
  REPEAT num_shapes times:
      Pick a random colour from palette
      Set turtle colour
      REPEAT sides times:
          Forward 60
          Right (360 / sides)
      Turn turtle by (360 / num_shapes)
```

Sketch the flowchart on the board. Reinforce: loops in flowcharts use a back-arrow and a decision diamond.

Now show the **starter code** the students will adapt:

```python
import turtle
import random

screen = turtle.Screen()
screen.bgcolor("black")
t = turtle.Turtle()
t.speed(0)
t.pensize(2)

palette = ["red", "yellow", "cyan", "magenta", "orange", "lime"]

num_shapes = int(input("How many shapes? "))
sides = int(input("How many sides per shape? "))

shape_angle = 360 / sides
rotate = 360 / num_shapes

for shape in range(num_shapes):
    t.color(random.choice(palette))
    for side in range(sides):
        t.forward(60)
        t.right(shape_angle)
    t.right(rotate)

screen.exitonclick()
```

Walk through it line by line. Note the **nested loop** (outer = shapes, inner = sides) and the `random.choice(palette)`.

**15–35 min: Build phase**

Students:
1. Open Worksheet 18 and complete Part 1 (planning) — sketch + pseudocode + flowchart. **No code allowed for the first 8 minutes.**
2. Then open a new Thonny file and code their design.
3. Test with 3 different inputs, recording results in Part 2.

Teacher circulates, prompting: *"Show me your sketch first" / "Where does the loop start in your flowchart?" / "What's the variable for your colour?"*

**35–50 min: Independent Practice — Worksheet 18 (continued)**

Students complete Part 2 (build log) and Part 3 (testing). Strong students try a stretch goal: nested-nested loops (a grid of small shapes).

**50–55 min: Sharing & Discussion — Gallery walk + peer review**
3-minute gallery walk: each student visits 3 other students' screens. Using the peer-review section in the worksheet, write one **specific praise** and one **specific suggestion** on a sticky note attached to the neighbour's monitor.

Teacher selects 2–3 to project to the whole class. Highlight the variety: the same starter code, but personal colour choices and parameter tweaks produce wildly different art.

**55–60 min: Closure & Preview — Unit reflection**
Whole class: 30-second answer to *"What's the most surprising thing you learned in Unit 3?"* Save files. Next unit: **Lists, Strings & Data Collections** — *"You'll learn how Python stores collections of data, like the lists we used today, and you'll build a quiz game and a grade book."*

##### Differentiation
- **Support:** Provide the starter code printed; students change only the palette and the variables `num_shapes`, `sides`. They still complete the full planning sheet.
- **Extension:** Add a **menu** (Unit 2 review): ask the user to pick from "burst / spiral / rosette / star field" and run different code paths with `if`/`elif`. OR: save the design as a function (preview Unit 5).

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Design phase** | No sketch / pseudocode | Sketch but no pseudocode | Sketch + pseudocode | Sketch + pseudocode + flowchart |
| **Code correctness** | Crashes / no output | Runs but doesn't match design | Runs and matches design | Runs, matches, parameters tunable |
| **Iteration use** | Single loop only | Two separate loops | Nested loops | Nested + random + input combined |
| **Testing & review** | No record | 1 test recorded | 3 tests recorded | 3 tests + thoughtful peer review |

##### Teacher Notes
- The single most common pitfall is jumping to code before sketching. Enforce the 8-minute "no code" rule strictly.
- Some students produce art so successful they want to save it. Show `screen.getcanvas().postscript(file='myart.eps')` only as enrichment.
- Make this celebratory — the unit ends in pride, not pressure. Project 2–3 favourites and applaud.
- File naming convention: `unit3_project_<firstname>.py`. Save to a shared folder if available.
- Take a class photo of the gallery wall — useful for parent reports and for the start of Session 19 ("look what you made!").
- If a student's design genuinely needs three nested loops (e.g. grid of polygons), support them — that's mastery. But warn the rest: deeply nested loops are slow and hard to debug.

---

#### SESSION 18 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Project Planning

**1.1 Title of your artwork:** ___________________________________________________

**1.2 Sketch — draw your intended output (pencil only, 5 minutes):**
```
+----------------------------------+
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
+----------------------------------+
```

**1.3 Inputs your program will ask the user for:**

| Input name | Type (int/str) | Example value |
|------------|----------------|---------------|
| ____________ | ____________ | ____________ |
| ____________ | ____________ | ____________ |
| ____________ | ____________ | ____________ |

**1.4 Colour palette (3–6 colours):**
1. _____________  2. _____________  3. _____________
4. _____________  5. _____________  6. _____________

**1.5 Pseudocode (write the steps in plain English, indented to show loops):**
```
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

**1.6 Flowchart (use Cambridge symbols: oval, rectangle, diamond, parallelogram):**
```
+----------------------------------+
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
|                                  |
+----------------------------------+
```

##### Part 2: Build Checklist

Tick each box once you've completed the step. Do not skip ahead.

- [ ] I imported `turtle` and `random`.
- [ ] I created `screen` and `t` (Turtle).
- [ ] I set the screen background colour.
- [ ] I defined a list called `palette` with at least 3 colours.
- [ ] I asked the user for at least one input using `int(input(...))`.
- [ ] I wrote the **outer** loop.
- [ ] I wrote the **inner** loop.
- [ ] I used `random.choice(palette)` somewhere.
- [ ] I ended with `screen.exitonclick()`.
- [ ] My program runs without errors.
- [ ] My output looks like (or better than!) my sketch.

**Code (paste/print here, or attach printout):**
```python
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
```

##### Part 3: Testing Log

Run your program with **three different sets of inputs**. Record each result.

**Test 1**

| Input | Value |
|-------|-------|
| _______________ | _______________ |
| _______________ | _______________ |

Quick sketch of output:
```
+----------------+
|                |
|                |
|                |
|                |
+----------------+
```
Did it match expectation? ☐ Yes ☐ No  Notes: __________________________

**Test 2**

| Input | Value |
|-------|-------|
| _______________ | _______________ |
| _______________ | _______________ |

Sketch:
```
+----------------+
|                |
|                |
|                |
|                |
+----------------+
```
Match? ☐ Yes ☐ No  Notes: __________________________

**Test 3 — extreme values (try a very small or very large number)**

| Input | Value |
|-------|-------|
| _______________ | _______________ |
| _______________ | _______________ |

Sketch:
```
+----------------+
|                |
|                |
|                |
|                |
+----------------+
```
Match? ☐ Yes ☐ No  What broke (if anything)? __________________________

##### Peer Review (fill out for ONE classmate)

Reviewer name: ____________________  Reviewing: ____________________

| Rubric Criterion | 1 | 2 | 3 | 4 |
|------------------|---|---|---|---|
| Design (sketch + pseudocode) | ☐ | ☐ | ☐ | ☐ |
| Code runs cleanly | ☐ | ☐ | ☐ | ☐ |
| Uses nested loops | ☐ | ☐ | ☐ | ☐ |
| Creative palette / parameters | ☐ | ☐ | ☐ | ☐ |

**One specific praise:** ____________________________________________________

**One specific suggestion for improvement:** ___________________________________

##### Reflection

1. What was the hardest part of designing your art generator? ______________________
2. Which loop pattern did you use the most — `for`, nested, or with `random.choice`? Why?
________________________________________________________________________________
3. If you had another hour, what one thing would you add to your project? ______________

##### Bonus / Stretch Challenge

**A. Menu mode.** Wrap your program so the user first picks from a menu:
```
1. Burst
2. Spiral
3. Rosette
```
Use `if` / `elif` to run different code for each. (Review of Unit 2 + this unit.)

**B. Save the canvas.** Add this *just before* `exitonclick()` to save your art:
```python
screen.getcanvas().postscript(file="myart.eps")
```
Open the `.eps` file — you've created a real vector image!

**C. Triple-nested.** Replace your single shape with a **grid** of small shapes (e.g. 4×4 grid of 5-pointed stars). You will need three nested loops: rows, columns, sides-of-each-shape. Plan it on paper first!

---
