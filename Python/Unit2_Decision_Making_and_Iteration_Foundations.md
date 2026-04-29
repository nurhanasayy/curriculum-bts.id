# Python Programming for Kids: Lesson Plans & Worksheets
## Unit 2: Decision Making & Iteration Foundations (Sessions 7–12)

### Unit Overview
Unit 2 introduces the two fundamental control structures of all programming: **selection** (decisions) and **iteration** (loops). Building directly on Unit 1's variables, types, and string handling, learners now teach the computer to *choose* and to *repeat*. They will master booleans, comparison and logical operators, the `if`/`elif`/`else` family, `while` loops with counters and sentinels, and the discipline of input validation with normal/boundary/invalid test data. The unit closes with a Number Guessing Game project that integrates random numbers, loops, conditions, and validation — a complete, playable artifact that maps directly onto Cambridge IGCSE 0478 §7 (algorithm design) and §10 (programming concepts), Cambridge Lower Secondary 0860 Stage 8 (control flow), and Singapore O-Level 7155 Module 1 (algorithms) and Module 2 (programming).

By the end of Unit 2, students will think in terms of *flowcharts and trace tables* (not just code), defend their algorithms with structured test data, and recognise common bugs (off-by-one, infinite loops, missing `else` branches) before running the program. These skills are the bedrock for Units 3–8.

---

### Session 7: Booleans & Comparison Operators

---

#### SESSION 7 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 7 of 48 |
| **Title** | Booleans & Comparison Operators |
| **Unit** | Unit 2: Decision Making & Iteration Foundations |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | IGCSE 0478 §10.1 (data types — Boolean), §7.2 (logic statements); Lower Secondary 0860 Stage 8 — "use logical reasoning to detect and correct errors in algorithms" |
| **Singapore Alignment** | O-Level 7155 Module 2.1 (data types & operators); Module 1.2 (algorithm logic) |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Identify and create** Boolean values (`True`, `False`) in Python with correct capitalisation, achieving 100% accuracy on a 10-item identification quiz.
2. **Apply** all six comparison operators (`==`, `!=`, `<`, `<=`, `>`, `>=`) to numbers and strings, predicting the result of at least 8 of 10 mixed expressions.
3. **Explain** the difference between `=` (assignment) and `==` (equality test) in their own words and in writing.
4. **Compare strings** alphabetically and recognise the case-sensitivity gotcha (`"Apple" != "apple"`), correctly diagnosing 3 of 3 sample bugs.

##### Materials Needed
- Thonny IDE (Python 3.11+) installed on each student device
- Projector for live coding demos
- Printed Worksheet 7 (one per student)
- Whiteboard / digital board for truth-value charts
- "Bool Cards" (optional) — index cards labelled `True` and `False` for the warm-up

##### Procedure

**0–5 min: Warm-Up — "True or False?"**
Teacher reads aloud 6 quick statements; students raise the `True` card or `False` card (or thumbs up / down):
- "Cats have 4 legs." (True)
- "7 is greater than 12." (False)
- "The word 'apple' comes before 'banana' in the dictionary." (True)
- "5 + 5 equals 10." (True)
- "Python is spelled with a capital P at the start of the language name." (True)
- "The number 0 is bigger than the number -1." (True)

Teacher: *"Every one of those statements was either True or False. There was no maybe. Today, we teach Python how to answer these kinds of questions — and the answer is always one of two values."*

**5–15 min: Introduction — Booleans Live**
Open Thonny. Type at the Shell prompt and run each line:

```python
>>> True
True
>>> False
False
>>> type(True)
<class 'bool'>
>>> type(False)
<class 'bool'>
```

Key points written on the board:
- **`bool`** is short for *Boolean*, named after George Boole (1815–1864), an English mathematician.
- Only **two** values: `True` and `False`. Capital T, capital F. `true` (lowercase) is a NameError.
- Every yes/no question in a program produces a Boolean.

Now demonstrate comparison operators producing booleans:

```python
>>> 5 == 5
True
>>> 5 == 6
False
>>> 5 != 6
True
>>> 10 > 3
True
>>> 10 < 3
False
>>> 7 >= 7
True
>>> 7 <= 6
False
```

**Teach the `=` vs `==` distinction explicitly.** Write on the board:

| Symbol | Meaning | Example |
|--------|---------|---------|
| `=`    | Assignment ("put this value into this box") | `score = 10` |
| `==`   | Equality test ("are these two equal?")      | `score == 10`  →  `True` |

Common student bug: `if x = 5:` (Python raises `SyntaxError`). Demo it live so they see the error and remember.

**15–35 min: Guided Practice — String Comparisons & The Case-Sensitivity Gotcha**

Type into a new Thonny file (`booleans_demo.py`):

```python
# String comparisons
print("apple" == "apple")    # True
print("apple" == "Apple")    # False  <-- gotcha!
print("apple" < "banana")    # True   (alphabetical order)
print("banana" < "apple")    # False
print("cat" < "category")    # True   (shorter word that matches start comes first)

# Comparing a name from input
name = input("What is your name? ")
print("Is your name Alex?", name == "Alex")
print("Is your name alex (lowercase)?", name == "alex")
```

Run the program. Students type `Alex`, then run again typing `alex`. They will see the *exact same human name* produce a different Boolean. **This is one of the most common bugs in beginner Python — internalise it now.**

Live discussion: "How could we fix this so the program treats `Alex`, `ALEX`, and `alex` as the same?"
Reveal:

```python
name = input("What is your name? ")
if name.lower() == "alex":
    print("Hi Alex!")
```

Then introduce the `input() == "yes"` pattern:

```python
answer = input("Do you like pizza? (yes/no) ")
likes_pizza = answer.lower() == "yes"
print("likes_pizza is", likes_pizza)
print("Type:", type(likes_pizza))
```

Have students predict each line's output before running. Pair-share: "What is `likes_pizza` after I type `YES`? After I type `Yes`? After I type `nope`?"

**Mini predict-the-bool round (whole class, fingers up for True / down for False):**

```python
>>> 100 > 99
>>> "5" == 5
>>> "5" < "50"
>>> 0 == False
>>> 1 == True
>>> "" == False
```

Discuss the surprises: `"5" == 5` is `False` because they are different *types* (string vs int). `0 == False` and `1 == True` are `True` because of Python's heritage (Booleans are technically a subclass of integers — *teaser for Unit 4*). `"" == False` is `False` (different types again).

**35–50 min: Independent Practice — Worksheet 7**
Students complete Parts 1–3 of the worksheet (predict-the-bool tables, comparison puzzles, expression analysis). Teacher circulates, redirects students who are stuck on capitalisation or `=` vs `==`.

**50–55 min: Sharing & Discussion**
Two students project their solutions to Part 2's "Tricky Pair" puzzle. Class identifies the difference. Teacher seeds: "Where might case-sensitivity bite you in a real game? *(Login screens, command words like `quit`/`Quit`/`QUIT`.)*"

**55–60 min: Closure & Preview**
Exit ticket on a sticky note: *Write one expression that evaluates to `True` and one that evaluates to `False`, both using comparison operators.*
Preview: "Tomorrow, we use these True/False values to make our programs *choose* what to do — `if` statements!"

##### Differentiation
- **Support:** Provide a printed comparison-operator reference card. Pair struggling students with a peer for the predict-the-bool exercise. Allow them to *type and run* each expression in Thonny rather than predict, building confidence first.
- **Extension:** Challenge advanced students with chained comparisons: `5 < 7 < 10` (legal in Python; evaluates left-to-right). Ask them to predict and explain `1 < 2 < 3 < 1`. Introduce the function `bool()` for converting: `bool(0)`, `bool(1)`, `bool("")`, `bool("hi")`, `bool([])` — and prepare them for *truthy/falsy* (Unit 3).

##### Assessment Criteria

| Criterion | Not Yet | Developing | Proficient | Mastery |
|-----------|---------|------------|------------|---------|
| **Recognise booleans** | Confuses `True` with the string `"True"`. | Sometimes capitalises wrongly. | Always uses correct `True`/`False`. | Explains why `bool` is a separate type and gives examples of expressions that produce booleans. |
| **Use comparison operators** | Confuses `=` and `==`. | Uses 4 of 6 operators correctly. | Uses all 6 operators correctly in fresh contexts. | Combines comparisons with string methods (`.lower()`) to write robust comparisons. |
| **Predict expression results** | < 5/10 correct on predict-the-bool. | 5–7/10 correct. | 8–9/10 correct. | 10/10 correct *and* explains the type-mismatch and case-sensitivity surprises. |
| **Diagnose bugs** | Cannot identify the bug. | Spots one of three bugs. | Spots two of three. | Spots all three and proposes a fix in code. |

##### Teacher Notes
- Capitalisation is the #1 error this lesson — leave `True`/`False` written on the board the entire session.
- Don't introduce `if` yet, even if students push for it. Today is *expressions only*. Tomorrow is *statements*.
- The `0 == False` / `1 == True` curiosity is fine to mention but flag it as an edge case students should not rely on.
- If a student types `if name = "Alex":`, celebrate the SyntaxError as "Python protecting you" — don't let it become a source of shame.
- Some students will discover that `"abc" < "abd"` is `True` and ask why. Show them ASCII / Unicode briefly (`ord("a")`, `ord("A")`) — it's a rich detour but only if time allows.

---

#### SESSION 7 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Predict-the-Bool Table
Without running any code, predict the value of each expression. Then run it in Thonny and write the actual result. Circle any that surprised you.

| # | Expression | Your Prediction | Actual (after running) |
|---|------------|-----------------|-------------------------|
| 1 | `7 == 7` |   |   |
| 2 | `7 == 7.0` |   |   |
| 3 | `7 == "7"` |   |   |
| 4 | `10 != 10` |   |   |
| 5 | `5 < 4` |   |   |
| 6 | `5 <= 5` |   |   |
| 7 | `"cat" == "Cat"` |   |   |
| 8 | `"apple" < "banana"` |   |   |
| 9 | `"Banana" < "apple"` |   |   |
| 10 | `"" == "0"` |   |   |
| 11 | `100 > 99 > 1` |   |   |
| 12 | `bool(0)` |   |   |

**Stop and think:** Look at rows 8 and 9. Item 9 is `False` even though *banana* sounds bigger than *apple*. **Why?** (Hint: capital letters come before lowercase in Unicode.)

________________________________________________________________________________

________________________________________________________________________________

##### Part 2: Comparison Puzzles
For each scenario, write a single Python expression that produces the requested Boolean. The first one is done for you.

| # | Scenario | Your Expression |
|---|----------|------------------|
| 1 | True if `age` is exactly 12. | `age == 12` |
| 2 | True if `score` is at least 80. |   |
| 3 | True if `temperature` is below freezing (less than 0). |   |
| 4 | False when `password` equals `"opensesame"`. |   |
| 5 | True if `name` (entered by the user) is `"Alex"` regardless of capitalisation. |   |
| 6 | True if a `hour` is in the afternoon (12 up to but not including 18). |   |
| 7 | True if `lives_remaining` is not zero. |   |
| 8 | True if the string `word` comes alphabetically *before* `"middle"`. |   |

##### Part 3: Tricky Pair
Two students wrote programs that *should* greet anyone named Alex, regardless of capitalisation. **One of them has a bug.** Run both, identify the bug, and fix it.

```python
# Program A
name = input("Name? ")
if name == "alex" or name == "Alex" or name == "ALEX":
    print("Hi Alex!")
```

```python
# Program B
name = input("Name? ")
if name.lower == "alex":
    print("Hi Alex!")
```

**Which program has the bug?** (circle one) **A   /   B**

**What is wrong?** ____________________________________________________________

________________________________________________________________________________

**Write the corrected line of code:**

```python

```

**Why is the *working* program a better solution than typing every capitalisation by hand?**

________________________________________________________________________________

##### Reflection
1. In your own words, what is the difference between `=` and `==`? Give an example of each.

________________________________________________________________________________

________________________________________________________________________________

2. Why does `"5" == 5` evaluate to `False`? (Look back at Unit 1 if you need a hint.)

________________________________________________________________________________

3. What was the most surprising result in Part 1's table? Why did it surprise you?

________________________________________________________________________________

##### Bonus / Stretch Challenge — "The Detective"
A friend shows you this code and says "it always prints YES no matter what I type":

```python
answer = input("Are you happy? ")
if answer = "yes":
    print("YES")
```

(a) What error message will Python actually give? Run it in Thonny and copy the *exact* error.

________________________________________________________________________________

(b) Fix the program in **two different ways** so that it correctly handles `yes`, `Yes`, and `YES`:

```python
# Fix 1


```

```python
# Fix 2


```

(c) Design 3 test inputs and predict the output for each fix:

| Test Input | Expected Output | Fix 1 OK? | Fix 2 OK? |
|-----------|-----------------|-----------|-----------|
|           |                 |           |           |
|           |                 |           |           |
|           |                 |           |           |

---

### Session 8: If / Elif / Else Statements

---

#### SESSION 8 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 8 of 48 |
| **Title** | If / Elif / Else Statements |
| **Unit** | Unit 2: Decision Making & Iteration Foundations |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | IGCSE 0478 §10.2 (selection); §7.1 (program flow); Lower Secondary 0860 Stage 8 (selection control flow, indentation discipline) |
| **Singapore Alignment** | O-Level 7155 Module 2.2 (control structures — selection); Module 1.3 (translating algorithm to code) |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Write** syntactically correct `if`, `if/else`, and `if/elif/else` statements with consistent 4-space indentation, with zero IndentationErrors on a 4-program assessment.
2. **Trace** an `if/elif/else` ladder by hand using a trace table, recording which branch is taken for at least 4 different inputs.
3. **Map** a Scratch *IF-THEN* block to its Python equivalent and explain the indentation difference (Scratch uses C-shaped blocks; Python uses whitespace).
4. **Build** a working grade calculator (A/B/C/D/F) and a "weather suggestion" program from a spec, both passing teacher-supplied test inputs.

##### Materials Needed
- Thonny IDE
- Projector
- Printed Worksheet 8
- A printed image (or projected slide) of a Scratch `if-then-else` block, side-by-side with Python equivalent
- "Indent ruler" handout — a printed strip showing 0, 4, 8 spaces for visual reference (optional, helps younger learners)

##### Procedure

**0–5 min: Warm-Up — Decision Tree**
Project this real-world decision tree on the board:
- *Is it raining?*
  - YES → take an umbrella.
  - NO → *Is it sunny?*
    - YES → wear sunglasses.
    - NO → just go.

Ask: "Which branch do you take if the weather is cloudy and dry?" *(Just go.)* "If it's raining and also sunny?" *(Take an umbrella — first question wins.)*

This is the mental model for `if / elif / else`: ordered questions, first match wins, exactly one branch executes.

**5–15 min: Introduction — `if` Syntax & The Indentation Rule**

Type live in Thonny:

```python
age = 13
if age >= 13:
    print("You can watch a PG-13 movie.")
print("End of program.")
```

Walk through, line by line. Highlight:
- Line ends with **a colon `:`**.
- Body is **indented exactly 4 spaces** (Thonny inserts them automatically with Tab — show this).
- The line "End of program." is *not* indented, so it always runs.

**Indentation gotcha demo.** Modify to:

```python
age = 10
if age >= 13:
print("You can watch a PG-13 movie.")  # missing indent!
```

Run. Watch the `IndentationError: expected an indented block`. Explain: *Python uses whitespace where Scratch uses C-shaped blocks. The 4 spaces are how Python knows what's "inside" the if.*

**Scratch-to-Python bridge.** Project this side-by-side:

| Scratch | Python |
|---------|--------|
| `if (age > 12) then [say "teen"]` | `if age > 12:`<br>`    print("teen")` |
| `if … else` C-block with two slots | `if …:` block then `else:` block |

**Add `else`:**

```python
age = 10
if age >= 13:
    print("You can watch a PG-13 movie.")
else:
    print("Sorry, you must be 13 or older.")
```

**Add `elif` (the chain):**

```python
score = 75
if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")
```

Key rules to write on board:
- An `if` may stand alone.
- `else` is optional; if present it comes **last**.
- You can have **zero or many** `elif` between `if` and `else`.
- **Exactly one** branch will execute.

**15–35 min: Guided Practice — Build the Grade Calculator Together**

Save as `grade_calculator.py`. Build incrementally with the class:

```python
# Step 1: get input as a number
score_text = input("Enter your test score (0-100): ")
score = int(score_text)

# Step 2: decide the grade
if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

# Step 3: report it
print(f"Score: {score}  →  Grade: {grade}")
```

Run with these test inputs (write them on the board *before* running, so the class predicts):
- 95 → expected A
- 80 → expected B (boundary!)
- 79 → expected C
- 60 → expected D (boundary!)
- 0 → expected F
- 105 → still A (no upper bound check yet — we *will* fix this in Session 11)

Discuss the **boundary inputs** (80 and 60) — why these matter, and how a misplaced `>` instead of `>=` would break them. Foreshadow Session 11's test-data discipline.

**Common bug demo — order matters.** Reverse the conditions:

```python
# BUGGY: every score becomes F!
if score >= 60:
    grade = "D"  # wait, what?
elif score >= 70:
    grade = "C"
# ...
```

Run with score = 95. Watch it print "D". Why? *Because `if score >= 60` is True for 95, so the rest never runs.* Lesson: order `elif`s from **most specific** (highest threshold) to **least specific**.

**35–50 min: Independent Practice — Worksheet 8**
Students complete Parts 1–3 (trace table, fix-the-indentation, build the weather suggester). Teacher monitors for IndentationErrors and guides students who reverse the `elif` order.

**50–55 min: Sharing & Discussion**
One pair projects their weather-suggester solution. Class verifies with 3 test inputs. Teacher asks: "What input would *break* your program? What do you think we'd need to do about it?" *(Foreshadows Session 11 validation.)*

**55–60 min: Closure & Preview**
Exit ticket: *Write the smallest possible `if/else` that prints "even" or "odd" given a variable `n`. (Use `n % 2`.)*

Sample answer:
```python
if n % 2 == 0:
    print("even")
else:
    print("odd")
```

Preview: "Tomorrow, we combine *more than one* condition with `and`, `or`, `not`. Truth tables ahead!"

##### Differentiation
- **Support:** Provide a printed code skeleton with the colons and indentation already in place; students only fill in the conditions. Use the "indent ruler" strip. Pair students for paired-coding ("driver/navigator").
- **Extension:** Ask advanced students to refactor the grade calculator using a single `if` per grade with combined conditions (e.g., `if 80 <= score < 90:`). Compare readability. Introduce the *one-liner* `print("A" if score >= 90 else "B")` as a teaser (formal coverage in Unit 3 stretch).

##### Assessment Criteria

| Criterion | Not Yet | Developing | Proficient | Mastery |
|-----------|---------|------------|------------|---------|
| **Syntax (colon, indent)** | Frequent SyntaxError or IndentationError. | Occasional indent slips, but can debug them. | Clean syntax across all sessions tasks. | Writes nested `if`s with consistent style and explains Python's whitespace rule. |
| **`if`/`elif`/`else` logic** | Cannot order branches; uses only `if`. | Uses `if`/`else` correctly; struggles with `elif` order. | Uses full `if`/`elif`/`else` ladder, ordered correctly. | Refactors a flawed ladder into a correct one and justifies the order. |
| **Trace ability** | Cannot complete a trace table. | Traces simple two-branch examples. | Traces 3+ branch ladders for ≥3 inputs. | Predicts which branch runs *before* tracing, and explains why. |
| **Build from spec** | Cannot start without help. | Starts but produces a partial solution. | Produces a working program for all sample inputs. | Adds a 4th-grade-style "Distinction" tier or an "Out of range" branch on their own initiative. |

##### Teacher Notes
- Always type 4 spaces yourself, on screen — never tabs that look like spaces. Mixed tabs/spaces is the silent killer of Python programs and Thonny will show a warning.
- Reinforce that **only one branch runs**. Students often expect multiple `print`s from one trip through an `if/elif/else`.
- The grade calculator's "score 105 → A" issue is intentional — it's the hook for Session 11 (input validation).
- If a student's program prints two grades, you can almost guarantee they used `if … if …` instead of `if … elif …`. This is the #2 most common bug today.
- Encourage *plain English* before code: students should say aloud "if score is 90 or more, give an A; otherwise if it's 80 or more, give a B; …" before they type.

---

#### SESSION 8 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Trace Table — Grade Calculator
Use the grade calculator code below. For each input score, fill in **(a)** which branch is taken, and **(b)** the value of `grade` at the end.

```python
if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"
```

| Input `score` | Which condition is the FIRST to be True? | `grade` at the end |
|---------------|---------------------------------------------|---------------------|
| 100           |                                             |                     |
| 90            |                                             |                     |
| 89            |                                             |                     |
| 80            |                                             |                     |
| 70            |                                             |                     |
| 65            |                                             |                     |
| 60            |                                             |                     |
| 59            |                                             |                     |
| 0             |                                             |                     |

**Question:** What grade does a score of `90` produce, and what grade does a score of `89` produce? Why is this difference important?

________________________________________________________________________________

##### Part 2: Fix-the-Indentation
Each program below has at least one indentation or syntax bug. Rewrite it correctly.

**Bug A:**
```python
age = 14
if age >= 13:
print("Teen!")
else:
    print("Not a teen.")
```

**Your fix:**
```python



```

**Bug B:**
```python
score = 75
if score >= 80
    print("Great")
else
    print("Keep trying")
```

**Your fix:**
```python



```

**Bug C:**
```python
weather = "rainy"
if weather == "rainy":
    print("Bring umbrella")
   print("Wear boots")
print("Goodbye")
```

(The middle line uses 3 spaces instead of 4 — find and fix.)

**Your fix:**
```python



```

##### Part 3: Build a Weather Suggestion Program
Write a program that asks the user for the weather (`sunny`, `rainy`, `snowy`, `cloudy`, or anything else) and prints a suggestion. Use `if`/`elif`/`else`.

**Spec table:**

| Input weather | Output suggestion |
|---------------|--------------------|
| `sunny`  | "Wear sunglasses and sunscreen." |
| `rainy`  | "Bring an umbrella and a raincoat." |
| `snowy`  | "Wear gloves and a warm jacket." |
| `cloudy` | "A light jacket should be fine." |
| anything else | "Hmm, I don't know that weather. Just be careful!" |

**Your code:**
```python
weather = input("What's the weather like? ").lower()


```

**Test it with these inputs and write what your program prints:**

| Input            | Output |
|------------------|--------|
| `sunny`          |        |
| `RAINY`          |        |
| `Snowy`          |        |
| `tornado`        |        |
| (just press Enter) |     |

**Why did we use `.lower()` on the input?** ____________________________________

________________________________________________________________________________

##### Reflection
1. What is the difference between `else` and `elif`? When would you choose one over the other?

________________________________________________________________________________

________________________________________________________________________________

2. Why does Python use indentation instead of `{ }` like other languages? Do you find it easier or harder to read? Why?

________________________________________________________________________________

3. Describe a real-life decision (e.g., what to wear, what to eat) that you could write as `if / elif / else`. Sketch it in pseudocode (not code) using IF / ELSE IF / ELSE keywords.

________________________________________________________________________________

________________________________________________________________________________

##### Bonus / Stretch Challenge — Pizza Topping Recommender
Build a program that asks the user for a number 1 to 5 and prints a pizza topping:
- 1 → "Margherita"
- 2 → "Pepperoni"
- 3 → "Veggie Supreme"
- 4 → "Hawaiian"
- 5 → "BBQ Chicken"
- Any other number → "Sorry, that's not a valid choice."

```python
choice = int(input("Pick a topping (1-5): "))




```

**Stretch++ :** What happens if the user types `three` instead of `3`? Try it. **Don't fix the bug** — just describe what error appears. We'll fix it in Session 11.

________________________________________________________________________________

________________________________________________________________________________

---

### Session 9: Logical Operators & Nested Conditions

---

#### SESSION 9 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 9 of 48 |
| **Title** | Logical Operators & Nested Conditions |
| **Unit** | Unit 2: Decision Making & Iteration Foundations |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | IGCSE 0478 §7.2 (logic — AND/OR/NOT, truth tables); §10.2 (selection); Lower Secondary 0860 Stage 9 (logical operators) |
| **Singapore Alignment** | O-Level 7155 Module 1.4 (logic gates / truth tables); Module 2.2 (compound conditions) |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Construct** truth tables for `and`, `or`, and `not` from scratch, achieving 100% on the 12-row table in Worksheet 9.
2. **Combine** two or more conditions in an `if` statement using `and`/`or`/`not` correctly in at least 4 of 5 worksheet items.
3. **Refactor** a nested `if` into a flat `if … and …` (and vice versa) when appropriate, recognising that nesting is sometimes clearer.
4. **Build** a "movie ticket pricing" program with at least 3 conditional branches that reads age + day-of-week and outputs the correct price.

##### Materials Needed
- Thonny IDE
- Projector
- Printed Worksheet 9
- Truth-table poster (printed A3) for the wall

##### Procedure

**0–5 min: Warm-Up — "Both / Either / Not"**
Read scenarios; students hold up "1 finger" for *and* (both must be true), "2 fingers" for *or* (at least one), "fist" for *not*:
- "I'll go to the park if it's sunny **and** I've finished homework." → 1 finger
- "We'll have ice cream **or** cake." → 2 fingers
- "I'm **not** going if I'm tired." → fist
- "You can play if you've eaten dinner **and** done dishes **or** if Mum says it's okay." → mixed (and + or — preview!)

**5–15 min: Introduction — Truth Tables**
Build the AND truth table on the board with the class:

| `A` | `B` | `A and B` |
|-----|-----|-----------|
| True  | True  | **True**  |
| True  | False | False |
| False | True  | False |
| False | False | False |

*"AND is greedy — it needs BOTH to be True."*

OR truth table:

| `A` | `B` | `A or B` |
|-----|-----|----------|
| True  | True  | True  |
| True  | False | True  |
| False | True  | True  |
| False | False | **False** |

*"OR is generous — only one needs to be True. Both being True still works."*

NOT (single input):

| `A` | `not A` |
|-----|---------|
| True  | False |
| False | True  |

*"NOT flips the value."*

Confirm in Thonny:

```python
>>> True and True
True
>>> True and False
False
>>> True or False
True
>>> not True
False
>>> not (5 > 3)
False
```

**15–35 min: Guided Practice — Combining Conditions**

**Concrete example 1: teen check.**

```python
age = int(input("How old are you? "))
if age >= 13 and age <= 17:
    print("You are a teenager.")
else:
    print("You are NOT a teenager.")
```

Walk through with `age = 14` (True and True → True), `age = 12` (False and True → False), `age = 20` (True and False → False).

**Show the `<=`/`>=` chain shortcut** (Pythonic, but also acceptable on Cambridge papers):

```python
if 13 <= age <= 17:
    print("You are a teenager.")
```

Both forms are equivalent.

**Concrete example 2: weekend or holiday.**

```python
day = input("Day of the week? ").lower()
is_holiday = input("Is today a holiday? (yes/no) ").lower() == "yes"

if day == "saturday" or day == "sunday" or is_holiday:
    print("No school today!")
else:
    print("Get up — school day.")
```

Test cases (do live):
| `day` | `is_holiday` | Expected |
|-------|--------------|----------|
| `monday` | False | Get up |
| `monday` | True | No school |
| `saturday` | False | No school |
| `sunday` | True | No school |

**Concrete example 3: NOT.**

```python
password = input("Password: ")
if not password == "":
    print("Thanks!")
else:
    print("You must enter a password.")
```

Better Pythonic form: `if password != "":`. Both are equivalent. Discuss readability.

**Now build movie ticket pricing live:**

```python
age = int(input("Age? "))
day = input("Day? (mon/tue/wed/thu/fri/sat/sun) ").lower()

if age < 5:
    price = 0
    reason = "free for under 5s"
elif age >= 65:
    price = 6
    reason = "senior discount"
elif day == "wed":
    price = 7
    reason = "Wacky Wednesday"
elif age <= 12:
    price = 8
    reason = "child price"
else:
    price = 12
    reason = "standard adult"

print(f"Price: ${price} ({reason})")
```

**Discuss order!** A 4-year-old on Wednesday is still free (because `age < 5` is checked first). What if a 70-year-old comes on Wednesday? *Senior price wins ($6) because that branch is checked before Wednesday.* Could we change the rule so they always pay the cheaper of the two? *Yes — this is the perfect use case for `min()` or for explicit comparison.* Foreshadow.

**Nested vs flat refactor demo:**

```python
# NESTED — sometimes clearer:
if logged_in:
    if is_admin:
        print("Welcome, admin.")
    else:
        print("Welcome, user.")
else:
    print("Please log in.")

# FLAT with `and` — sometimes clearer:
if logged_in and is_admin:
    print("Welcome, admin.")
elif logged_in:
    print("Welcome, user.")
else:
    print("Please log in.")
```

Both work. Teach: **flat is usually preferred**, but nesting helps when the inner conditions only matter once you're inside the outer one (e.g., once logged in, *then* check admin).

**35–50 min: Independent Practice — Worksheet 9**
Students complete the truth tables, the simplification exercise, and the nested-vs-flat refactoring.

**50–55 min: Sharing & Discussion**
Volunteers share movie-ticket variants. Discuss tricky cases (a 3-year-old on Wednesday, a 65-year-old on Wednesday). Highlight: **the order of `elif` decides priority**.

**55–60 min: Closure & Preview**
Exit ticket: *Write a single `if` statement that prints "OK" only when `temp` is between 18 and 25 (inclusive) **and** `humidity` is below 70.*

Answer:
```python
if 18 <= temp <= 25 and humidity < 70:
    print("OK")
```

Preview: "Tomorrow we don't just decide *once* — we *repeat* using `while` loops!"

##### Differentiation
- **Support:** Provide truth-table fill-in with three rows already filled. Use physical blocks (red/green tokens) to "evaluate" expressions left to right. Pair-code the movie-ticket exercise.
- **Extension:** Ask advanced students to write the De Morgan's transformation: `not (A and B) == (not A) or (not B)`. Verify by code with all 4 (A, B) combinations. Bonus: write the movie-ticket program *without `elif`*, using nested `if`s only — and explain why it's harder to read.

##### Assessment Criteria

| Criterion | Not Yet | Developing | Proficient | Mastery |
|-----------|---------|------------|------------|---------|
| **Truth tables** | Less than half correct. | Most rows correct, slips on AND vs OR. | All rows correct. | Constructs truth table for compound expression like `(A and B) or (not C)`. |
| **Combine conditions** | Cannot use `and`/`or`/`not`. | Uses one operator correctly. | Uses all three correctly in independent items. | Uses chained comparison `13 <= age <= 17` and explains its meaning. |
| **Refactor nested ↔ flat** | Cannot identify equivalence. | Refactors with hints. | Refactors correctly when prompted. | Decides which form is more readable for a given context and justifies. |
| **Build (movie ticket)** | Incomplete. | Works for 1–2 cases. | Works for all teacher-supplied test cases. | Adds an additional rule (e.g., 3D surcharge, family bundle) and tests it. |

##### Teacher Notes
- Students often write `if age >= 13 or age <= 17:` (which is *always True* for any integer). Use this as a teachable moment — **`or` is generous, so this is satisfied by 1, 5, 12, 100, anything**. Test live to make the point land.
- Cambridge / Singapore exam papers love the phrase *"compound condition"* — use that vocabulary today.
- Avoid `&`/`|` (bitwise operators); they look right and sometimes work, but they are not the same as `and`/`or` and have surprising precedence. Reserve them for Unit 7+.
- For very young learners, the words "BOTH must be True" (and) and "AT LEAST ONE must be True" (or) work better than abstract truth tables. Use both representations.
- The "65-year-old on Wednesday" puzzle is a great springboard for Unit 4's `min()` introduction — note it but don't solve today.

---

#### SESSION 9 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Truth Table Fill-In
Complete the truth tables. Use `T` for True and `F` for False.

**AND**
| `A` | `B` | `A and B` |
|-----|-----|-----------|
| T   | T   |           |
| T   | F   |           |
| F   | T   |           |
| F   | F   |           |

**OR**
| `A` | `B` | `A or B` |
|-----|-----|----------|
| T   | T   |          |
| T   | F   |          |
| F   | T   |          |
| F   | F   |          |

**NOT**
| `A` | `not A` |
|-----|---------|
| T   |         |
| F   |         |

**Compound — `(A and B) or C`**

| `A` | `B` | `C` | `A and B` | `(A and B) or C` |
|-----|-----|-----|-----------|------------------|
| T   | T   | F   |           |                  |
| T   | F   | F   |           |                  |
| F   | T   | T   |           |                  |
| F   | F   | F   |           |                  |

##### Part 2: Predict-the-Bool — Compound Edition
Predict, then verify in Thonny.

| # | Expression | Prediction | Actual |
|---|------------|-----------|--------|
| 1 | `True and False` |   |   |
| 2 | `True or False` |   |   |
| 3 | `not True` |   |   |
| 4 | `(5 > 3) and (10 < 20)` |   |   |
| 5 | `(5 > 3) and (10 > 20)` |   |   |
| 6 | `(5 < 3) or (10 < 20)` |   |   |
| 7 | `not (5 == 5)` |   |   |
| 8 | `(7 > 5) and not (3 == 3)` |   |   |
| 9 | `"a" < "b" and "b" < "c"` |   |   |
| 10 | `not (False or False)` |   |   |

##### Part 3: Simplify-this-Condition
Each expression below can be **simplified** to a shorter form that means the same thing. Rewrite it.

| # | Original | Simpler form |
|---|----------|---------------|
| 1 | `if x == True:` | `if x:` |
| 2 | `if x == False:` |   |
| 3 | `if not (a == b):` |   |
| 4 | `if age >= 13 and age <= 17:` |   |
| 5 | `if not (score < 50):` |   |

##### Part 4: Nested vs Flat Refactor
Below is a nested `if`. Refactor it into a **flat** version using `and`. Both should produce identical output.

```python
# Nested:
if has_ticket:
    if age >= 18:
        print("Welcome to the concert!")
    else:
        print("You need a guardian.")
else:
    print("No ticket — no entry.")
```

**Flat version:**
```python




```

Now, the **opposite direction**. Below is flat code with `and`. Rewrite it as a *nested* version. Why might the nested version be clearer here?

```python
# Flat:
if logged_in and (role == "admin"):
    print("Admin dashboard")
elif logged_in and (role == "user"):
    print("User dashboard")
else:
    print("Please log in")
```

**Nested version:**
```python




```

**Why might the nested version be clearer?** _____________________________________

________________________________________________________________________________

##### Part 5: Build — Movie Ticket Pricing
Spec:
- Under 5 → free
- 5 to 12 → $8
- 13 to 64 → $12
- 65 and over → $6
- **Override:** if it is Wednesday, anyone aged 13–64 pays only $7.

```python
age = int(input("Age? "))
day = input("Day (mon/tue/wed/thu/fri/sat/sun)? ").lower()




```

**Test table — fill in:**

| Age | Day | Expected Price | Your Output |
|-----|-----|----------------|--------------|
| 3   | mon |                |              |
| 8   | wed |                |              |
| 30  | wed |                |              |
| 30  | tue |                |              |
| 70  | wed |                |              |
| 13  | wed |                |              |
| 64  | sun |                |              |

##### Reflection
1. Which is "stricter": `and` or `or`? Explain.

________________________________________________________________________________

2. Give a real-life situation where you'd use `not`.

________________________________________________________________________________

3. When does **nesting** read more clearly than **flat `and`**?

________________________________________________________________________________

##### Bonus / Stretch Challenge — De Morgan's Law
The mathematician Augustus De Morgan discovered that:

`not (A and B)` is the same as `(not A) or (not B)`

Verify this with a truth table for **all four** combinations of A and B:

| A | B | `A and B` | `not (A and B)` | `not A` | `not B` | `(not A) or (not B)` |
|---|---|-----------|------------------|---------|---------|------------------------|
| T | T |           |                  |         |         |                        |
| T | F |           |                  |         |         |                        |
| F | T |           |                  |         |         |                        |
| F | F |           |                  |         |         |                        |

**Are the two columns (`not (A and B)`) and (`(not A) or (not B)`) identical?** ___________

Now write a tiny Python program that *proves* it for any boolean values:

```python
for a in [True, False]:
    for b in [True, False]:
        left = not (a and b)
        right = (not a) or (not b)
        print(a, b, left, right, left == right)
```

What do you notice about the last column of every row?

________________________________________________________________________________

---

### Session 10: While Loops & Trace Tables

---

#### SESSION 10 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 10 of 48 |
| **Title** | While Loops & Trace Tables |
| **Unit** | Unit 2: Decision Making & Iteration Foundations |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | IGCSE 0478 §10.2 (iteration — pre-condition loop); §7.3 (trace tables); Lower Secondary 0860 Stage 8 (count-controlled and condition-controlled loops) |
| **Singapore Alignment** | O-Level 7155 Module 2.2 (iteration); Module 1.3 (dry running with trace tables) |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Write** a `while` loop with a counter that runs a specified number of times, debugging any off-by-one errors with help.
2. **Write** a sentinel-controlled `while` loop that terminates on a specific input (e.g., `"quit"`).
3. **Complete** a trace table for a multi-iteration loop, recording every variable's value per iteration with 100% accuracy on a 4-row example.
4. **Recognise** an infinite loop in code, halt it in Thonny using the red Stop button, and identify the missing/incorrect update statement.

##### Materials Needed
- Thonny IDE
- Projector — visible Thonny toolbar (so the red Stop button is on screen)
- Printed Worksheet 10
- Printed blank trace-table template (4 columns × 8 rows)

##### Procedure

**0–5 min: Warm-Up — "Pat your head until I say stop"**
Teacher: "Pat your head. Keep patting until I say *stop*." Pat for ~10 seconds. "STOP." All stop.

Now: "Pat your head 5 times exactly." Students pat 5 times.

These are the **two flavours** of `while`:
- **Sentinel-controlled** — keep going until some condition triggers stop ("until I say stop").
- **Count-controlled** — repeat exactly N times.

**5–15 min: Introduction — `while` Syntax**

Type live:

```python
count = 0
while count < 5:
    print("Hello", count)
    count = count + 1
print("Done!")
```

Walk through:
- **Initialise** the counter (`count = 0`) **before** the loop.
- **Test condition** at the top each iteration (`while count < 5:`). If True, body runs; if False, loop exits.
- **Update** the counter inside the body (`count = count + 1`). Without this, the loop runs forever.

Run it. Output:
```
Hello 0
Hello 1
Hello 2
Hello 3
Hello 4
Done!
```

Ask: *Why does it print 0 to 4 — five lines — but stop before 5?* Because `count < 5` becomes False when `count` becomes 5, **before** the body runs again.

**Trace table demo on the board:**

| Iteration | `count` (start) | `count < 5`? | Action | `count` (end) |
|-----------|------------------|---------------|--------|----------------|
| 1         | 0                | True          | print "Hello 0", count += 1 | 1 |
| 2         | 1                | True          | print "Hello 1", count += 1 | 2 |
| 3         | 2                | True          | print "Hello 2", count += 1 | 3 |
| 4         | 3                | True          | print "Hello 3", count += 1 | 4 |
| 5         | 4                | True          | print "Hello 4", count += 1 | 5 |
| 6         | 5                | **False**     | exit loop |   |

Trace tables are **a Cambridge IGCSE staple** — students who skip them tend to write buggy loops.

Introduce the shorthand:

```python
count = count + 1
# is the same as
count += 1
```

Show both work. Use `+=` from now on.

**15–35 min: Guided Practice**

**Pattern 1 — Counter, count up:**

```python
n = 1
while n <= 10:
    print(n)
    n += 1
```

**Pattern 2 — Counter, count down:**

```python
seconds = 5
while seconds > 0:
    print(seconds)
    seconds -= 1
print("Blast off!")
```

**Pattern 3 — Sentinel-controlled (most useful in real programs):**

```python
answer = ""
while answer != "quit":
    answer = input("Type something (or 'quit' to stop): ")
    print("You typed:", answer)
print("Bye!")
```

Run it. Notice the *bug* — the program echoes "quit" before stopping. Why? Because we update `answer` inside the loop, then loop back to test, but the body's `print` already ran. Discuss: how would we fix? Refactor:

```python
while True:
    answer = input("Type something (or 'quit' to stop): ")
    if answer == "quit":
        break
    print("You typed:", answer)
print("Bye!")
```

Briefly introduce `break` as "leave the loop now" — full coverage in Unit 3.

**Pattern 4 — sum of inputs:**

```python
total = 0
count = 0
while count < 5:
    n = int(input(f"Number {count + 1}: "))
    total += n
    count += 1
print("Total:", total)
print("Average:", total / count)
```

**The Infinite Loop Demo. (Crucial.)**

```python
n = 1
while n <= 10:
    print(n)
    # forgot n += 1 !!!
```

Run. Watch the output flood the Shell. **Press the red Stop button in Thonny** (point to it on screen). Discuss: what was missing? *The update.* Three things every `while` needs:
1. **Initialise** the loop variable.
2. **Test** the condition.
3. **Update** the loop variable so the test eventually becomes False.

If any of those is missing or wrong, you have an infinite loop.

**35–50 min: Independent Practice — Worksheet 10**
Students fill trace tables, predict iteration counts, and fix infinite-loop bugs.

**50–55 min: Sharing & Discussion**
Project a student's trace table. Class verifies. Discuss: "What changes if we use `<=` instead of `<`?" *The loop runs one more time — classic off-by-one.*

**55–60 min: Closure & Preview**
Exit ticket: *In one sentence, what are the THREE parts every counter-controlled `while` loop needs?*

Answer: Initialise, Test (condition), Update.

Preview: "Tomorrow we use loops to *protect* our programs from bad input — input validation!"

##### Differentiation
- **Support:** Use a printed loop "shape" with three boxes (initialise, test, update). Students fill them in for given problems before writing code. For the infinite loop demo, walk students through the Stop button in pairs.
- **Extension:** Introduce the `else` clause on a `while` loop (runs only if the loop exited *normally*, not via `break`). Ask them to write a "find the secret password" program that prints "Welcome" only after a successful guess and uses a counter to limit attempts to 3.

##### Assessment Criteria

| Criterion | Not Yet | Developing | Proficient | Mastery |
|-----------|---------|------------|------------|---------|
| **`while` syntax** | Frequent SyntaxError; missing colon. | Compiles but logic flawed. | Clean syntax, runs as intended. | Uses `+=`, `-=` consistently and writes both up- and down-counter loops. |
| **Trace table** | Blank or random values. | Half-correct. | All rows correct for a 5-iteration example. | Creates own trace table for a fresh loop, including the exit row. |
| **Off-by-one awareness** | Doesn't notice. | Notices after running. | Predicts off-by-one before running. | Explains the `<` vs `<=` distinction in own words. |
| **Infinite-loop diagnosis** | Cannot stop the loop. | Stops it; can't explain. | Stops, identifies the missing update, fixes it. | Predicts before running which loops will be infinite and corrects on paper. |

##### Teacher Notes
- Show the red Stop button on Thonny early — students will produce real infinite loops in the worksheet, and they need to know how to recover without panicking.
- Insist on hand-tracing *before* running, especially for off-by-one cases. The discipline pays off through the rest of the course.
- Some students will discover `time.sleep(1)` and want to add it. Allow it for fun, but don't make it required — it's covered in Unit 5.
- Avoid `for` loops today — they appear in Unit 3. The pedagogical sequence (while first, then for) makes iteration's mechanics explicit before the Pythonic shorthand.
- Sentinel + `break` is the bread-and-butter pattern for the next session and the project. Make sure every student leaves today comfortable with it.

---

#### SESSION 10 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Trace This Loop
Given this code:

```python
n = 1
total = 0
while n <= 4:
    total = total + n
    print("n =", n, " total =", total)
    n += 1
print("Final total:", total)
```

Fill in the trace table. Add as many rows as needed.

| Iteration | `n` (start) | `n <= 4`? | `total` (end) | `n` (end) | What gets printed |
|-----------|--------------|-----------|----------------|-----------|---------------------|
| 1         |              |           |                |           |                     |
| 2         |              |           |                |           |                     |
| 3         |              |           |                |           |                     |
| 4         |              |           |                |           |                     |
| 5         |              |           |                |           |                     |

**What is the final total printed?** ____________

**How many lines does this program print to the Shell in total?** ____________

##### Part 2: Predict the Iteration Count
For each loop, predict **how many times the body will run**, **without running the code**.

| # | Loop | Iteration count |
|---|------|------------------|
| 1 | `i = 0`<br>`while i < 5:`<br>`    print(i)`<br>`    i += 1` |  |
| 2 | `i = 1`<br>`while i <= 5:`<br>`    print(i)`<br>`    i += 1` |  |
| 3 | `i = 0`<br>`while i < 10:`<br>`    print(i)`<br>`    i += 2` |  |
| 4 | `i = 10`<br>`while i > 0:`<br>`    print(i)`<br>`    i -= 1` |  |
| 5 | `i = 0`<br>`while i <= 0:`<br>`    print(i)`<br>`    i += 1` |  |
| 6 | `i = 5`<br>`while i < 5:`<br>`    print(i)`<br>`    i += 1` |  |

Now run each in Thonny and verify your predictions. Circle any you got wrong.

##### Part 3: Fix the Infinite Loop
Each loop below runs forever. **Identify the bug** and **fix it**.

**Bug A:**
```python
n = 1
while n <= 10:
    print(n)
```

**What's missing?** _____________________________________________________________

**Your fix:**
```python


```

**Bug B:**
```python
n = 10
while n > 0:
    print(n)
    n += 1   # <-- ?
```

**What's wrong?** _______________________________________________________________

**Your fix:**
```python


```

**Bug C:**
```python
answer = ""
while answer != "quit":
    print("Hello!")
    # never asks for answer
```

**What's missing?** _____________________________________________________________

**Your fix:**
```python


```

##### Part 4: Build — Sentinel Loop
Write a program that keeps asking the user for a number and prints its square, until the user types `done`. Use a sentinel-controlled `while` loop.

Example session:
```
Number (or 'done'): 4
4 squared is 16
Number (or 'done'): 7
7 squared is 49
Number (or 'done'): done
Goodbye!
```

```python




```

**Trace table:** suppose the user enters `3`, then `5`, then `done`. Fill in:

| Iteration | `entry` value | `entry == "done"`? | Action |
|-----------|----------------|--------------------|--------|
| 1         |                |                    |        |
| 2         |                |                    |        |
| 3         |                |                    |        |

##### Reflection
1. What are the **three things** every counter-controlled `while` loop needs?

________________________________________________________________________________

2. Describe (in your own words) what an **infinite loop** is and how to stop one in Thonny.

________________________________________________________________________________

3. Why is a trace table useful even *before* you run your code?

________________________________________________________________________________

##### Bonus / Stretch Challenge — Multiplication Table
Use a `while` loop to print the multiplication table of a number the user picks. For example, if they pick 7:
```
7 x 1 = 7
7 x 2 = 14
...
7 x 12 = 84
```

```python
num = int(input("Which times-table would you like? "))




```

**Stretch++ :** Add an outer loop that prints **all** times-tables from 1 to 5 (one block each, separated by a blank line). You'll have a `while` loop *inside* a `while` loop — that's called a *nested loop*.

```python




```

---

### Session 11: Input Validation & Test Data

---

#### SESSION 11 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 11 of 48 |
| **Title** | Input Validation & Test Data |
| **Unit** | Unit 2: Decision Making & Iteration Foundations |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | IGCSE 0478 §11 (testing — normal, boundary, erroneous data); §10.2 (validation routines); Lower Secondary 0860 Stage 9 (validation & verification) |
| **Singapore Alignment** | O-Level 7155 Module 1.5 (test data); Module 2.3 (validation routines, error handling) |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Define** the three categories of test data — normal, boundary, invalid — and produce at least 2 examples of each for a given problem.
2. **Write** a `while` loop that re-prompts the user until valid input is received, for a number-in-range problem.
3. **Test** their own program against a 6-input test plan covering all three data categories, recording actual vs expected outputs.
4. **Recognise** the role of `try`/`except` (preview only) for catching non-numeric input.

##### Materials Needed
- Thonny IDE
- Projector
- Printed Worksheet 11
- Printed test-data planning template
- Printed reference card listing the 3 test-data categories with examples

##### Procedure

**0–5 min: Warm-Up — "Mean Tester"**
Teacher: "I just wrote a program that asks for your age and prints how old you'll be in 10 years. What weird inputs could break it?"
Crowd-source on the board: negative numbers, words ("ten"), 999, blank, emoji, decimals, very large numbers, "abc"…

The lesson framing: **The user is not your friend. Your program must defend itself.**

**5–15 min: Introduction — Three Categories of Test Data**

Project on the board:

| Category | Definition | Example for "age 1–120" |
|----------|------------|--------------------------|
| **Normal** | Typical, expected input. | 14, 25, 50 |
| **Boundary** | The edges of the valid range. | 1 (lower), 120 (upper) |
| **Invalid** | Outside the valid range, or wrong type entirely. | 0, 121, -5, "abc", "" (blank) |

This three-way split is **directly assessed on Cambridge IGCSE 0478 paper 2 and Singapore 7155 papers** — students will see this categorisation again on exam day.

**Why all three?**
- *Normal* tests the happy path.
- *Boundary* catches off-by-one bugs (`<` vs `<=`).
- *Invalid* checks that your validation actually works.

**The validation pattern (re-prompt with `while`):**

```python
# Step 1: ask once
age_text = input("Age (1-120)? ")
age = int(age_text)

# Step 2: keep asking until valid
while age < 1 or age > 120:
    print("That's not in range. Try again.")
    age_text = input("Age (1-120)? ")
    age = int(age_text)

print(f"Got it — you are {age}.")
```

Live-test with: 14 (passes immediately), 0 (re-prompts), 121 (re-prompts), 50 (passes). Discuss the **sentinel** logic — same pattern as Session 10.

**The "ask once, then loop" cleanup with a flag:**

```python
valid = False
while not valid:
    age_text = input("Age (1-120)? ")
    age = int(age_text)
    if 1 <= age <= 120:
        valid = True
    else:
        print("Out of range. Try again.")

print(f"Got it — you are {age}.")
```

Both patterns work. The flag pattern is more readable when validation has multiple sub-checks.

**The "non-number" gotcha and a `try`/`except` preview.**

Run with input `"twenty"`. Watch `ValueError: invalid literal for int()`.

```python
# PREVIEW — full coverage in Unit 6
while True:
    age_text = input("Age (1-120)? ")
    try:
        age = int(age_text)
        if 1 <= age <= 120:
            break
        else:
            print("Out of range.")
    except ValueError:
        print("Please type a whole number.")
print(f"Got it — you are {age}.")
```

Don't dwell — this is a teaser. Today's main focus is range validation with `while`.

**15–35 min: Guided Practice — "Guess a number 1–10" with Validation**

Build live:

```python
secret = 7  # we'll randomise next session
guess = -1   # any out-of-range starting value

while guess < 1 or guess > 10:
    guess_text = input("Guess a number 1-10: ")
    guess = int(guess_text)
    if guess < 1 or guess > 10:
        print("Out of range. 1 to 10 only.")

if guess == secret:
    print("Correct!")
else:
    print(f"Wrong — the answer was {secret}.")
```

**Now build the test plan together** before testing:

| Test # | Input | Category | Expected Output |
|--------|-------|----------|------------------|
| 1 | 7  | Normal (correct) | "Correct!" |
| 2 | 5  | Normal (wrong) | "Wrong — the answer was 7." |
| 3 | 1  | Boundary (low) | "Wrong — the answer was 7." |
| 4 | 10 | Boundary (high) | "Wrong — the answer was 7." |
| 5 | 0  | Invalid (below) | "Out of range." then re-prompt |
| 6 | 11 | Invalid (above) | "Out of range." then re-prompt |
| 7 | -3 | Invalid (negative) | "Out of range." then re-prompt |
| 8 | "abc" | Invalid (type) | ValueError (we haven't fixed this — it's expected for now) |

Run each test, fill in actual results. Mark any that don't match expected as **bugs to fix**.

This is the discipline of testing: **plan inputs and expected outputs *before* running**.

**35–50 min: Independent Practice — Worksheet 11**
Students design test plans for given problems and write a validated PIN-entry program.

**50–55 min: Sharing & Discussion**
A pair shares their test plan for one of the worksheet problems. Class checks: "Did they cover all 3 categories? Any boundary they missed?"

**55–60 min: Closure & Preview**
Exit ticket: *Give 1 normal, 1 boundary, and 1 invalid input for a program that asks for a month number (1–12).*
Sample answer: Normal 6, Boundary 1 (or 12), Invalid 0 (or 13, or "Jan").

Preview: "Tomorrow we put **everything** from Unit 2 together: random numbers, loops, conditions, validation, and a real game. Project Day!"

##### Differentiation
- **Support:** Provide a half-written validation skeleton; students fill in the condition and the print. Use a partner system for test-data brainstorming. Don't require `try`/`except` in independent work.
- **Extension:** Add an **attempt limit** (max 3 wrong guesses), then add **try/except** for non-numeric input. Compare the program's robustness before and after. Stretch: refactor validation into a function (preview Unit 4) using `def get_int_in_range(low, high)`.

##### Assessment Criteria

| Criterion | Not Yet | Developing | Proficient | Mastery |
|-----------|---------|------------|------------|---------|
| **Test data categories** | Cannot distinguish. | Names categories but examples sometimes wrong. | 2+ correct examples per category. | Designs an exhaustive plan with edge cases (empty input, very large numbers). |
| **Validation loop** | Cannot write. | Loop works but accepts some invalid. | Loop correctly rejects invalid inputs and re-prompts. | Combines range + type validation cleanly. |
| **Test plan execution** | Doesn't test. | Tests a few inputs informally. | Executes a written test plan and records results. | Identifies a real bug from the test plan and fixes it. |
| **`try`/`except` awareness** | Unaware. | Mentions it. | Reads sample code and explains what it does. | Uses it correctly in stretch work. |

##### Teacher Notes
- Today's vocabulary (normal / boundary / invalid) is **exam vocabulary**. Print and post the reference card.
- Resist the urge to teach `try`/`except` fully. It's a Unit 6 topic. Today, mention it as the tool they'll use *next month* to handle "abc"-style errors.
- Some students will write `while age != 14 and age != 25 and age != 50:` to "validate" — i.e., listing every valid value. Use this as a teachable moment about **range conditions** vs **enumeration**.
- For the worksheet's PIN problem, ensure students don't print the PIN on screen during validation (privacy hygiene — security teaser).
- This session is the *single most important* hand-off into the project session. Don't shortchange it for time.

---

#### SESSION 11 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Test-Data Categories Design
For each problem below, write **2 normal**, **2 boundary**, and **2 invalid** test inputs.

**Problem A:** A program asks for the user's age and only accepts ages **5 to 17**.

| Category | Test Input | Why this category? |
|----------|------------|---------------------|
| Normal   |            |                     |
| Normal   |            |                     |
| Boundary |            |                     |
| Boundary |            |                     |
| Invalid  |            |                     |
| Invalid  |            |                     |

**Problem B:** A program asks for a percentage score, accepting **0 to 100** (whole numbers).

| Category | Test Input | Why this category? |
|----------|------------|---------------------|
| Normal   |            |                     |
| Normal   |            |                     |
| Boundary |            |                     |
| Boundary |            |                     |
| Invalid  |            |                     |
| Invalid  |            |                     |

**Problem C:** A program asks for a day of the week (`mon` through `sun`).

| Category | Test Input | Why this category? |
|----------|------------|---------------------|
| Normal   |            |                     |
| Normal   |            |                     |
| Boundary |            |                     |
| Boundary |            |                     |
| Invalid  |            |                     |
| Invalid  |            |                     |

##### Part 2: Validate-This-Input
Each program below has **incomplete or buggy validation**. Identify the issue and fix it.

**Code A — accepts 0, which is wrong:**
```python
age = int(input("Age (1-120)? "))
while age > 120:
    age = int(input("Try again: "))
```

**What's wrong?** _____________________________________________________________

**Your fix:**
```python


```

**Code B — only checks once:**
```python
score = int(input("Score (0-100)? "))
if score < 0 or score > 100:
    print("Out of range")
    score = int(input("Score (0-100)? "))
```

**What's wrong?** _____________________________________________________________

**Your fix (use a `while` loop):**
```python


```

**Code C — message is misleading:**
```python
day = input("Day (mon-sun)? ").lower()
while day != "mon":
    print("Try again")
    day = input("Day? ").lower()
```

**What's wrong?** _____________________________________________________________

**Your fix:**
```python


```

##### Part 3: Build — PIN-Entry Validator
Write a program that:
1. Stores a secret 4-digit PIN (you choose, e.g., `1234`).
2. Asks the user to enter their PIN.
3. Re-prompts up to **3 times** if wrong.
4. Prints "Access granted" if correct, "Account locked" if 3 wrong attempts.

```python
secret_pin = "1234"
attempts = 0




```

**Test plan — fill in expected vs actual:**

| Test # | Inputs (in order)         | Category | Expected Output | Actual Output |
|--------|---------------------------|----------|------------------|----------------|
| 1      | `1234`                    | Normal   |                  |                |
| 2      | `0000`, `1234`            | Normal   |                  |                |
| 3      | `0000`, `1111`, `1234`    | Boundary |                  |                |
| 4      | `0000`, `1111`, `2222`    | Boundary |                  |                |
| 5      | `0000`, `1111`, `2222`, `3333` | Invalid (4th attempt) |    |        |
| 6      | `12`                      | Invalid (too short) |          |                |

##### Reflection
1. Why are **boundary** test inputs especially important?

________________________________________________________________________________

2. What's the difference between a **normal** test and an **invalid** test?

________________________________________________________________________________

3. Did your PIN program pass all 6 tests? If not, which one failed and what would you change?

________________________________________________________________________________

##### Bonus / Stretch Challenge — Try/Except Preview
Currently, if the user types `abc` for the score, your program crashes with `ValueError`. Below is a preview of how Python catches this. Type it, run it, and try inputs `50`, `200`, `-5`, `abc`, `(empty)`.

```python
while True:
    text = input("Score (0-100)? ")
    try:
        score = int(text)
    except ValueError:
        print("Please type a whole number.")
        continue
    if 0 <= score <= 100:
        break
    print("Out of range — try again.")

print("Final score:", score)
```

(a) What does `try` do?
________________________________________________________________________________

(b) What does `except ValueError` do?
________________________________________________________________________________

(c) Try input `3.5`. What happens? Why does `int("3.5")` fail?
________________________________________________________________________________

(d) Make a test plan with **at least one input from each category** including a non-numeric.

| Input | Category | Expected |
|-------|----------|----------|
|       |          |          |
|       |          |          |
|       |          |          |
|       |          |          |
|       |          |          |

---

### Session 12: Project 2 — Number Guessing Game

---

#### SESSION 12 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 12 of 48 |
| **Title** | Project 2 — Number Guessing Game |
| **Unit** | Unit 2: Decision Making & Iteration Foundations |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | IGCSE 0478 §7 (algorithm design — pseudocode, flowcharts); §10.2 (selection + iteration); §11 (testing); Lower Secondary 0860 Stage 8 — "design, write, test and debug a program" |
| **Singapore Alignment** | O-Level 7155 Module 1 (algorithm design + dry run); Module 2 (full programming task with validation) |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Design** the Number Guessing Game algorithm using **pseudocode** and a **flowchart** before writing any code, completing both on the worksheet planner.
2. **Implement** a working Number Guessing Game in Python that uses `random.randint`, a `while` loop, `if`/`elif`/`else` for higher/lower hints, and an attempt counter.
3. **Validate** input so only integers 1–100 are accepted, re-prompting on invalid input.
4. **Peer-test** another student's project using a structured rubric, providing one praise and one suggestion in writing.

##### Materials Needed
- Thonny IDE
- Projector
- Printed Worksheet 12 (project planner + checklist + debug log + peer-test rubric)
- Printed flowchart symbol reference card (start/end oval, process rectangle, decision diamond, I/O parallelogram, arrows)
- Sticky notes for peer testing

##### Procedure

**0–5 min: Warm-Up — "Pick a number…"**
Teacher: "I'm thinking of a number between 1 and 100. You have to guess it, and I'll only tell you 'higher' or 'lower'. How many guesses do you think you'll need at most?"

Take a few class guesses. The mathematical answer is **7** (binary search: 100 → 50 → 25 → 12 → 6 → 3 → 1, 7 halvings). Today's project is the *computer's* version of this game.

**5–15 min: Mini Design Phase — Pseudocode & Flowchart Together**

**Pseudocode (whiteboard):**

```
START
    secret ← random integer between 1 and 100
    attempts ← 0

    REPEAT
        guess ← input from user (must be integer 1–100)
        attempts ← attempts + 1
        IF guess < secret THEN
            print "Higher!"
        ELSE IF guess > secret THEN
            print "Lower!"
        ELSE
            print "Correct! You took N attempts."
        END IF
    UNTIL guess = secret

END
```

**Flowchart (sketch on the board):**
- Oval: START
- Parallelogram: input guess
- Rectangle: attempts += 1
- Diamond: guess < secret? → Yes → print Higher → loop back
- Diamond: guess > secret? → Yes → print Lower → loop back
- Otherwise → print Correct → END

Discuss: pseudocode and flowcharts are **languaged-agnostic**. Cambridge / Singapore exams ask you to write pseudocode for a problem *before* coding. Today, we practise that discipline.

**15–35 min: Build the Game (live, with class translating from pseudocode)**

```python
import random

# 1. set up
secret = random.randint(1, 100)
attempts = 0
guess = 0  # any value not equal to secret to enter loop

# 2. main loop
while guess != secret:
    # 2a. validated input
    text = input("Guess a number 1-100: ")
    if not text.isdigit():
        print("That's not a whole number. Try again.")
        continue
    guess = int(text)
    if guess < 1 or guess > 100:
        print("Out of range. 1-100 only.")
        continue

    # 2b. count this attempt
    attempts += 1

    # 2c. give a hint
    if guess < secret:
        print("Higher!")
    elif guess > secret:
        print("Lower!")
    else:
        print(f"Correct! You took {attempts} attempts.")

print("Thanks for playing.")
```

**Walk through the new piece — `random.randint`:**

```python
>>> import random
>>> random.randint(1, 10)
7
>>> random.randint(1, 10)
3
```

`random.randint(a, b)` returns a random integer **including both endpoints**. (Unlike many other languages where the upper bound is exclusive!)

**Walk through `text.isdigit()`:**

```python
>>> "42".isdigit()
True
>>> "abc".isdigit()
False
>>> "".isdigit()
False
>>> "3.5".isdigit()
False
>>> "-5".isdigit()
False  # the minus sign isn't a digit
```

This is a clean way to *check before converting* — no `try`/`except` needed yet.

**Walk through `continue`:**
- `continue` jumps back to the top of the loop, skipping the rest of the body.
- It's the "try again" command inside a loop.
- Full coverage in Unit 3, but used here to keep code readable.

**Run with these test cases:**
- A normal play (a few guesses, eventual correct).
- Type `abc` — should re-prompt.
- Type `200` — should re-prompt.
- Type `-5` — should re-prompt (`isdigit()` returns False for the minus).
- Type `0` — should re-prompt.

**35–50 min: Independent Practice / Build Phase**
Students work in pairs or solo:
- Complete the worksheet's planning section (pseudocode + flowchart) **first** if they haven't.
- Build the game.
- Add **at least one stretch feature** of their choice:
  - **Difficulty levels** (Easy: 1–10; Medium: 1–100; Hard: 1–1000).
  - **Best-score tracking** using a global variable, e.g., `best = None` and update if `attempts < best`.
  - **Limit on attempts** (lose if you exceed it).
  - **Themed messages** ("Burning hot!" if within 5 of the secret).

Sample stretch — difficulty levels:

```python
import random

print("Difficulty: 1=Easy(1-10) 2=Medium(1-100) 3=Hard(1-1000)")
level = input("Choose 1, 2, or 3: ")
while level not in ("1", "2", "3"):
    level = input("Pick 1, 2, or 3: ")

if level == "1":
    upper = 10
elif level == "2":
    upper = 100
else:
    upper = 1000

secret = random.randint(1, upper)
attempts = 0
guess = 0

while guess != secret:
    text = input(f"Guess a number 1-{upper}: ")
    if not text.isdigit():
        print("Not a whole number.")
        continue
    guess = int(text)
    if guess < 1 or guess > upper:
        print(f"Out of range — 1 to {upper}.")
        continue
    attempts += 1
    if guess < secret:
        print("Higher!")
    elif guess > secret:
        print("Lower!")
    else:
        print(f"Correct! You took {attempts} attempts.")
```

**50–55 min: Peer Playtest**
Each student swaps seats with a partner, plays *their* program for 2 minutes, and fills the **peer-test rubric** on the worksheet (1 praise + 1 suggestion + checklist).

**55–60 min: Sharing & Closure**
2–3 students project their game and demo. Class gives applause + one star + one wish. Teacher recaps Unit 2: *We learned booleans, comparison, if/elif/else, and/or/not, while loops, trace tables, and validation. Unit 3 next week — strings, lists, and `for` loops!*

##### Differentiation
- **Support:** Provide a near-complete code skeleton with the loop, hint logic, and `random.randint` already filled in; students complete the validation. Allow pair-coding for the entire build. Skip stretch features.
- **Extension:** Implement **all** stretch features (difficulty + best-score + attempt limit + hot/cold messages). Refactor input validation into a helper function `def get_guess(upper):` (preview Unit 4). Add a "play again?" outer loop.

##### Assessment Criteria — Project Rubric

| Criterion | Not Yet | Developing | Proficient | Mastery |
|-----------|---------|------------|------------|---------|
| **Design (pseudocode + flowchart)** | Missing or unrelated to code. | One present, the other partial. | Both complete and match the code. | Pseudocode + flowchart catch a design issue *before* coding (revisions visible). |
| **Core gameplay** | Doesn't run / can't guess. | Runs but no hints, or no end condition. | Higher/lower hints, ends on correct guess, counts attempts. | All of Proficient + clean output formatting + final summary. |
| **Validation** | None. | Catches one of (out-of-range, non-numeric). | Catches both, re-prompts cleanly. | Catches all + handles empty input + uses `.isdigit()` or try/except idiomatically. |
| **Stretch feature** | None attempted. | Started, incomplete. | One stretch feature working. | 2+ stretch features working and tested. |
| **Peer test feedback** | Doesn't complete. | Vague comments. | Specific praise + specific suggestion. | Identifies a real bug from playtesting and the author fixes it during the session. |

##### Teacher Notes
- Insist on the **plan-before-code** discipline. Walk around in the first 10 minutes of independent work; don't let anyone open a `.py` file until pseudocode is on paper.
- The single most common bug today: forgetting to update `guess` inside the loop, leading to infinite loop. Reinforce the Session 10 "init / test / update" rule.
- Watch for students who hard-code a secret (e.g., `secret = 42`). The rubric requires `random.randint` for proficient — make this explicit when handing out the worksheet.
- Encourage students to **save their stretch version separately** (`numguess_v1.py`, `numguess_v2.py`) so they don't break a working program while experimenting.
- Peer-testing produces some of the richest feedback of the unit. Insist on **written** comments — kids will ask "what should I write?" and the rubric in Worksheet 12 gives them the structure.
- Save 2 minutes at the end for an actual Unit 2 wrap-up. Students should leave celebrating.

---

#### SESSION 12 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Project Planning

**Step 1A — Pseudocode.** Write the steps of the Number Guessing Game in pseudocode. Use `START`, `END`, `INPUT`, `OUTPUT`, `IF / ELSE IF / ELSE`, `REPEAT … UNTIL`. Don't use Python syntax — use natural language.

```
START
    secret ← __________________________________________
    attempts ← __________________________________________

    REPEAT
        ____________________________________________________
        ____________________________________________________
        IF __________________________________________ THEN
            OUTPUT ___________________________________
        ELSE IF __________________________________________ THEN
            OUTPUT ___________________________________
        ELSE
            OUTPUT ___________________________________
        END IF
    UNTIL ____________________________________________
END
```

**Step 1B — Flowchart.** Draw a flowchart of your game. Use the standard symbols:
- **Oval** — start / end
- **Parallelogram** — input / output
- **Rectangle** — process (e.g., assignment)
- **Diamond** — decision (yes/no question)
- **Arrows** — flow direction

(Use the box below — pencil first!)

```
+--------------------------------------------------------------+
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
|                                                              |
+--------------------------------------------------------------+
```

##### Part 2: Build Checklist
Tick each box when complete.

- [ ] Imported `random` at the top of the file
- [ ] Generated `secret = random.randint(1, 100)`
- [ ] Initialised `attempts = 0` (or similar)
- [ ] Initialised `guess` so the loop can start
- [ ] `while` loop continues until `guess == secret`
- [ ] Read input from user
- [ ] **Validation:** rejects non-numeric input
- [ ] **Validation:** rejects numbers outside 1–100
- [ ] Counted the attempt only after validation passes
- [ ] Printed "Higher!" when guess is too low
- [ ] Printed "Lower!" when guess is too high
- [ ] Printed "Correct! You took N attempts." on success
- [ ] Tested with at least one normal, one boundary (1 or 100), one invalid input

##### Part 3: Stretch Choice
Pick **at least one** stretch feature to implement. Tick which one(s) you did:

- [ ] Difficulty levels (Easy 1–10, Medium 1–100, Hard 1–1000)
- [ ] Best-score tracker across plays
- [ ] Attempt limit (e.g., max 7 guesses; lose if exceeded)
- [ ] Hot/cold themed messages ("Burning!" within 5; "Cold!" if more than 25 away)
- [ ] "Play again?" outer loop
- [ ] Other (describe): ________________________________________________

**Briefly describe what you built:**
________________________________________________________________________________

________________________________________________________________________________

##### Part 4: Debug Log
Every coder hits bugs. Log at least 3 bugs you encountered and how you fixed them.

| # | What went wrong (symptom) | What caused it (cause) | How you fixed it |
|---|----------------------------|-------------------------|-------------------|
| 1 |                            |                         |                   |
| 2 |                            |                         |                   |
| 3 |                            |                         |                   |
| 4 |                            |                         |                   |

##### Part 5: My Test Plan
Before you say "done", run these tests on your final program. Record the actual output.

| Test # | Input(s) | Category | Expected Output | Actual Output | Pass / Fail |
|--------|----------|----------|------------------|----------------|--------------|
| 1 | (a number you already know is the secret) | Normal | "Correct! …" |   |   |
| 2 | A guess that is too low | Normal | "Higher!" |   |   |
| 3 | A guess that is too high | Normal | "Lower!" |   |   |
| 4 | `1` | Boundary low | depends |   |   |
| 5 | `100` | Boundary high | depends |   |   |
| 6 | `0` | Invalid (too low) | re-prompt |   |   |
| 7 | `101` | Invalid (too high) | re-prompt |   |   |
| 8 | `abc` | Invalid (non-numeric) | re-prompt |   |   |
| 9 | (just press Enter) | Invalid (empty) | re-prompt |   |   |

**How many tests passed?** ____ of 9.

**For any failures, what will you fix?**
________________________________________________________________________________

##### Part 6: Peer Playtest

**Tester's name:** ________________________________________

Tick each box if the program does this when you play it:

- [ ] Asks for a guess clearly
- [ ] Generates a different secret each time you run it
- [ ] Gives "Higher!"/"Lower!" hints
- [ ] Recovers gracefully when I type something silly (`abc`, `0`, `999`)
- [ ] Tells me how many attempts I took
- [ ] Ends nicely with a goodbye message

**One thing I really liked (a star):** _______________________________________

________________________________________________________________________________

**One thing that could improve (a wish):** _________________________________

________________________________________________________________________________

**Did you find a bug? If yes, describe it:** _______________________________

________________________________________________________________________________

##### Reflection
1. Which part of building this project was **hardest**? Why?

________________________________________________________________________________

________________________________________________________________________________

2. Which part are you **most proud** of?

________________________________________________________________________________

3. Looking at all of Unit 2 (booleans, if/elif/else, and/or/not, while loops, trace tables, validation), which idea feels the most **powerful** to you, and what would you build with it next?

________________________________________________________________________________

________________________________________________________________________________

##### Bonus / Stretch Challenge — "AI Reverse Mode"
In this version, **the user thinks of a secret**, and the **computer guesses**. The user replies `higher`, `lower`, or `correct`. Use binary search (always guess the midpoint of the remaining range).

Pseudocode hint:
```
low ← 1, high ← 100
WHILE not solved:
    guess ← (low + high) // 2
    OUTPUT "Is it " + guess + "?"
    reply ← INPUT
    IF reply = "higher" THEN low ← guess + 1
    ELSE IF reply = "lower" THEN high ← guess - 1
    ELSE solved ← True
```

Build it:

```python
low = 1
high = 100




```

**How many guesses does the computer need at most?** ____________

(Try with secrets 1, 50, 100. Do you ever exceed 7 guesses? Why does that match the warm-up answer?)

________________________________________________________________________________

---
