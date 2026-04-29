# Python Programming for Kids: Lesson Plans & Worksheets
## Unit 5: Functions & Modular Design (Sessions 25–30)

### Unit Overview
Unit 5 transforms students from line-by-line scripters into **modular thinkers**. Across six sessions they learn to define and call functions, pass parameters and arguments, return values, manage local versus global scope, supply default parameters, and finally **decompose** a substantial problem into a coordinated set of sub-routines. The unit is anchored in Cambridge IGCSE 0478 §10 (procedures and functions, with and without parameters) and Singapore O-Level 7155 Module 4 (sub-routines, scope, parameter passing). It also embeds the Cambridge problem-solving habit of writing pseudocode **before** typing Python, and it culminates in a Modular Math Helper project where students must list at least five function stubs on paper before any code is written. By the end of Session 30, every learner can read and write a Python program that is split into named, testable, reusable building blocks — the foundation for every later unit.

---

### Session 25: Defining & Calling Functions

---

#### SESSION 25 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 25 of 48 |
| **Title** | Defining & Calling Functions |
| **Unit** | Unit 5: Functions & Modular Design |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — procedures and functions (without parameters); Lower Secondary Computing 0860 — abstraction and decomposition |
| **Singapore Alignment** | O-Level 7155 Module 4 — defining and calling sub-routines; EdTech Masterplan CT pillar: decomposition |

##### Learning Objectives (SMART)
By the end of this 60-minute session, students will be able to:
1. **Define** a no-argument function in Python using the `def name():` syntax with a correctly indented body, in at least 3 different examples.
2. **Call** a previously defined function from a main program, distinguishing between *defining* and *calling* on a trace table.
3. **Refactor** a short repetitive program (with at least two duplicated blocks) into a version that uses one function called multiple times, reducing line count by ≥30%.
4. **Explain**, in their own words, the Cambridge distinction between a *procedure* (does something) and a *function* (returns a value), and why Python collapses both into `def`.

##### Materials Needed
- Thonny IDE (Python 3.11+) on each student computer.
- Projector / shared screen for live coding.
- Printed Session 25 worksheet (one per student).
- Whiteboard for "definition vs call" diagram.
- Optional: turtle graphics enabled (built-in to Python).
- Stickers or stamps for the *Refactor Hero* award at the end.

##### Procedure

**0–5 min: Warm-Up — "The Repeat Trap"**
Display this code on the board and ask students to count the lines:

```python
print("*" * 30)
print("   WELCOME TO PY-CLUB   ")
print("*" * 30)
print("Lesson begins now!")

print("*" * 30)
print("   WELCOME TO PY-CLUB   ")
print("*" * 30)
print("Reminder: bring your laptop tomorrow.")

print("*" * 30)
print("   WELCOME TO PY-CLUB   ")
print("*" * 30)
print("Goodbye!")
```

Ask: *"If we wanted to change the banner text from PY-CLUB to PY-HEROES, how many lines would we need to edit?"* (Answer: 3.) Lead them to: *"Wouldn't it be nice if we could write the banner once, give it a name, and just say its name three times?"* That is exactly what a **function** is.

**5–15 min: Introduction — What is a function?**
Write on the board:

> A **function** is a named, reusable chunk of code. You **define** it once and **call** it many times.

Live-type and run:

```python
def print_banner():
    print("*" * 30)
    print("   WELCOME TO PY-CLUB   ")
    print("*" * 30)

# Call it three times:
print_banner()
print("Lesson begins now!")
print_banner()
print("Reminder: bring your laptop tomorrow.")
print_banner()
print("Goodbye!")
```

Annotate live:
- `def` is a Python keyword meaning *define*.
- `print_banner` is the **name** we chose (snake_case, like a variable).
- The empty `()` means "no parameters yet — we'll add those next session".
- The `:` opens a block; the body is **indented** (4 spaces).
- `print_banner()` *with* the parentheses is the **call** — that's what actually runs the body.

Cambridge sidebar (write on board):
| Cambridge term | Meaning | Python equivalent |
|----------------|---------|-------------------|
| **Procedure** | Does an action, returns nothing | `def` with no `return` |
| **Function** | Computes and **returns** a value | `def` with `return` |

Tell students: *"In Python both use `def`. We will say function for both, but if your IGCSE exam asks, remember the distinction."*

**15–35 min: Guided Practice — Build three functions together**

**(a) `greet_class()` — a procedure**

```python
def greet_class():
    print("Good morning, coders!")
    print("Today we are learning about functions.")
    print("Get ready to have fun.")

greet_class()
greet_class()   # call it again — works instantly
```

Ask predict-the-output: how many lines print? (6.)

**(b) `draw_square()` — using turtle**

```python
import turtle

pen = turtle.Turtle()
pen.speed(5)

def draw_square():
    for _ in range(4):
        pen.forward(80)
        pen.right(90)

draw_square()
pen.penup()
pen.forward(120)
pen.pendown()
draw_square()        # second square, no copy-paste!

turtle.done()
```

Discuss: imagine drawing a row of 5 houses — how many lines saved?

**(c) Refactor demo — the warm-up code**
Together, transform the warm-up into:

```python
def print_banner():
    print("*" * 30)
    print("   WELCOME TO PY-CLUB   ")
    print("*" * 30)

print_banner(); print("Lesson begins now!")
print_banner(); print("Reminder: bring your laptop tomorrow.")
print_banner(); print("Goodbye!")
```

Count lines: 12 → 7. Discuss DRY (*Don't Repeat Yourself*).

**Common-bug demo (do this on purpose):**

```python
def say_hi()
    print("Hi!")
say_hi()
```

Run it — `SyntaxError: expected ':'`. Fix it. Then forget the parentheses on call:

```python
def say_hi():
    print("Hi!")
say_hi   # no () — nothing prints!
```

Lead them to: *"`say_hi` without parentheses is just the name of the function, not a call."*

**35–50 min: Independent Practice — Worksheet**
Hand out the Session 25 worksheet. Students work individually; teacher circulates. Encourage typing into Thonny and *running each function at least twice* to feel the reuse.

**50–55 min: Sharing & Discussion**
Two volunteers project their refactor of Part 3 (Question 7). Class compares line counts. Ask: *"Which name is clearer — `func1` or `print_invoice_header`?"* Reinforce **descriptive names**.

**55–60 min: Closure & Preview**
Exit ticket on a sticky note: *"Write the one-line difference between defining and calling a function."* Preview: *"Today our functions all said the same thing every time. Next session we'll teach them to listen to us using **parameters** so we can say `greet('Aisha')` and `greet('Ben')` with the same function!"*

##### Differentiation
- **Support:** Provide a fill-in-the-blank skeleton for Q5 (`def ____():` with body already written). Pair-program with a stronger peer for Q7.
- **Extension:** Bonus task — define `draw_house()` that calls `draw_square()` *inside* it, then add a triangle roof. This previews **function composition**.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| Function definition syntax | Forgets `def`, `:`, or indentation | Defines but with one syntax error | Defines correctly | Defines correctly with descriptive name + comment |
| Calling functions | Confuses define with call | Calls but only once | Calls multiple times | Calls in varied contexts including inside another function |
| Refactoring | Cannot identify duplication | Spots duplication, struggles to extract | Successfully extracts function | Extracts and re-uses function ≥3 times, line count cut ≥30% |
| Vocabulary | Uses "thing" / "block" | Uses "function" inconsistently | Uses *define*, *call*, *body* correctly | Adds *procedure* vs *function* (Cambridge) and *DRY* |

##### Teacher Notes
- The single biggest beginner error is **forgetting the parentheses on the call** — it produces no error and no output, only a confused student. Drill this.
- Do not introduce parameters today even if a bright student asks; promise it for Session 26.
- The turtle demo is optional — skip if your lab does not allow GUI windows; substitute a text-art square using nested loops.
- Encourage `snake_case` names and verbs (`print_banner`, not `banner`).
- If time runs short, drop the second turtle square and keep the refactor demo — that is the load-bearing concept.

---

#### SESSION 25 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Spot the Function

Look at the code listing below and answer the questions.

```python
def show_menu():
    print("1) Play")
    print("2) Settings")
    print("3) Quit")

def play_intro():
    print(">>> Loading game...")
    print(">>> Ready!")

show_menu()
play_intro()
show_menu()
```

1. How many functions are **defined**? ________
2. List their names: ____________________________________________
3. How many times is `show_menu` **called**? ________
4. **Predict the output** — write it in the box, then run it in Thonny to check.

| Predicted output | Actual output |
|------------------|---------------|
|                  |               |
|                  |               |
|                  |               |
|                  |               |
|                  |               |
|                  |               |
|                  |               |
|                  |               |

5. **Spot the bug.** What is wrong with this code? Circle the line and write a fix below.

```python
def cheer():
    print("Go team!")

cheer
cheer()
```

Bug explanation: ___________________________________________________________________
Fix: _______________________________________________________________________________

##### Part 2: Write Three Functions

In Thonny, write **all three** of the following functions in one file. Then call each one at least twice.

6a) A function `print_line()` that prints a line of 40 dashes (`-`).

6b) A function `greet_morning()` that prints three sentences welcoming students to the morning lesson (your choice of words).

6c) A function `draw_text_square()` that prints a 5×5 square made from `#` characters using a `for` loop (no manual `print("#####")` five times!). Bonus: make it use *one* `for` loop, not nested.

Paste your finished code into the box (or staple a printout):

```
[your code here]




```

##### Part 3: Refactor Challenge

7) Below is a repetitive program. Refactor it so the duplicated block becomes ONE function called multiple times. Write the **before line count**, the **after line count**, and the **percentage reduction**.

**BEFORE:**

```python
print("=== INVOICE ===")
print("Pyclub Robotics Co.")
print("---------------")
print("Item: Robot kit  $50")

print("=== INVOICE ===")
print("Pyclub Robotics Co.")
print("---------------")
print("Item: Sensor pack  $20")

print("=== INVOICE ===")
print("Pyclub Robotics Co.")
print("---------------")
print("Item: Battery  $10")
```

**AFTER (write your refactor in the box):**

```
[your refactored code here]





```

Before line count: ______ After line count: ______ Reduction %: ______

##### Reflection (3 prompts)
R1. In your own words, what is the difference between **defining** a function and **calling** a function?
________________________________________________________________________________
R2. Which of your three functions in Part 2 would be most useful to keep and reuse in future programs? Why?
________________________________________________________________________________
R3. The Cambridge syllabus distinguishes a *procedure* from a *function*. Write one sentence explaining how they differ.
________________________________________________________________________________

##### Bonus / Stretch Challenge

Write a function `draw_staircase()` that prints a 5-step staircase using `#` characters, like this:

```
#
##
###
####
#####
```

Then call it twice. Can you make a *second* function `draw_double_staircase()` that calls `draw_staircase()` **twice** internally, with a blank line between? (This previews function composition!)

---

### Session 26: Parameters & Arguments

---

#### SESSION 26 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 26 of 48 |
| **Title** | Parameters & Arguments |
| **Unit** | Unit 5: Functions & Modular Design |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — procedures and functions with parameters; pseudocode `PROCEDURE name(p1, p2)` / `FUNCTION name(p1) RETURNS type` |
| **Singapore Alignment** | O-Level 7155 Module 4 — parameter passing; argument vs parameter terminology |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Distinguish** between a *parameter* (in the `def` line) and an *argument* (at the call site), labelling each correctly in 5 of 6 examples.
2. **Define and call** functions with one and multiple positional parameters, including at least one numeric and one string parameter.
3. **Trace** a 3-call sequence through a parameterised function using a parameter trace table.
4. **Refactor** a no-arg function into a parameterised version that handles 3 different inputs without rewriting the body.

##### Materials Needed
- Thonny / Python 3.11+
- Worksheet S26
- Slide or whiteboard with the *parameter vs argument* diagram
- Cambridge pseudocode reference card (one per pair)
- Coloured pens for parameter tracing

##### Procedure

**0–5 min: Warm-Up — "The Boring Greeter"**
Show:

```python
def greet():
    print("Hello, Aisha!")

greet()
greet()
greet()
```

Ask: *"What is annoying about this function?"* (It always says Aisha.) *"How could we make it greet anyone?"* Take guesses. Reveal: **parameters**.

**5–15 min: Introduction — Parameters and Arguments**

Write a giant diagram on the board:

```
def greet(name):     <-- 'name' is a PARAMETER (in the definition)
    print("Hello,", name)

greet("Aisha")       <-- "Aisha" is an ARGUMENT (passed at the call)
greet("Ben")
greet("Chloe")
```

Sentence to chant together: *"Parameters are in the def. Arguments are at the call."*

Live-run it. Show that the same function, called three times, produces three different outputs. Tell students: *"The parameter is like a labelled box. When the call happens, Python puts the argument value into the box `name` and runs the body."*

Then add **two parameters**:

```python
def area_rectangle(width, height):
    area = width * height
    print("Area =", area)

area_rectangle(5, 3)     # 15
area_rectangle(10, 4)    # 40
area_rectangle(7, 7)     # 49
```

Position matters: the first argument fills the first parameter. Show what happens if you swap:

```python
def divide(a, b):
    print(a / b)

divide(10, 2)   # 5.0
divide(2, 10)   # 0.2  -- different!
```

Briefly mention **keyword arguments** (don't drill):

```python
divide(b=10, a=2)   # = 0.2
```

> Tell students: *"You'll mostly use positional. Keyword args are an option for clarity."*

Cambridge pseudocode parallel — write on board:

```
PROCEDURE Greet(Name : STRING)
    OUTPUT "Hello, ", Name
ENDPROCEDURE

CALL Greet("Aisha")
```

**15–35 min: Guided Practice**

**(a) Parameter trace table.** Project this code:

```python
def describe_pet(name, animal, age):
    print(name, "is a", age, "year old", animal)

describe_pet("Mochi", "cat", 3)
describe_pet("Rex", "dog", 7)
describe_pet("Kiki", "parrot", 1)
```

Build a trace table together:

| Call # | name   | animal | age | Output                          |
|--------|--------|--------|-----|----------------------------------|
| 1      | Mochi  | cat    | 3   | Mochi is a 3 year old cat       |
| 2      | Rex    | dog    | 7   | Rex is a 7 year old dog         |
| 3      | Kiki   | parrot | 1   | Kiki is a 1 year old parrot     |

Stress: each call gives the parameters **fresh** values. The old values are gone.

**(b) `draw_polygon` with turtle.**

```python
import turtle
pen = turtle.Turtle(); pen.speed(0)

def draw_polygon(sides, length):
    angle = 360 / sides
    for _ in range(sides):
        pen.forward(length)
        pen.right(angle)

draw_polygon(3, 80)
pen.penup(); pen.forward(120); pen.pendown()
draw_polygon(5, 60)
pen.penup(); pen.forward(120); pen.pendown()
draw_polygon(8, 40)
turtle.done()
```

Three shapes, one function!

**(c) Common bug demos.**

> **Bug 1: too few arguments.**
> ```python
> def add(a, b):
>     print(a + b)
> add(5)        # TypeError: missing 1 required positional argument: 'b'
> ```

> **Bug 2: argument-order mistake.**
> ```python
> def greet(greeting, name):
>     print(greeting, name)
> greet("Aisha", "Hello")   # prints: Aisha Hello -- wrong!
> ```
> Fix by swapping arguments OR using keywords: `greet(name="Aisha", greeting="Hello")`.

**35–50 min: Independent Practice — Worksheet**
Students complete Sessions 26 worksheet. Teacher circulates to catch *parameter vs argument* confusion.

**50–55 min: Sharing & Discussion**
One pair shares their `draw_polygon` extension. Class debates: *"Would using `keyword=` arguments make this clearer?"*

**55–60 min: Closure & Preview**
Exit ticket: write the chant *"Parameters are in the def. Arguments are at the call."* on a sticky note and stick it to the board. Preview: *"Our functions print results, but what if I want to use the result in another calculation? Next session: `return`."*

##### Differentiation
- **Support:** Provide a parameter table template pre-printed for Q5. Allow function bodies to be written first, then parameters identified.
- **Extension:** Q-bonus: write `pythagoras(a, b)` that prints the hypotenuse using `(a*a + b*b) ** 0.5`. Then make it accept a third optional parameter `units="cm"` (foreshadows Session 28).

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| Parameter syntax | Confuses position of params | Defines 1 param OK, multi struggles | Multi-param defs correct | Mixed positional/keyword used correctly |
| Vocabulary | Says "input" generically | Uses parameter only | Uses parameter and argument | Uses both correctly + can correct a peer |
| Tracing | Fills 1 row | Fills most rows w/ errors | All rows correct | Predicts output before running |
| Refactor | Adds param but breaks body | Adds param, body works for 1 case | Works for all 3 cases | Adds 2 params, all cases, descriptive names |

##### Teacher Notes
- Do not yet introduce `return` — that is Session 27. If a student writes `return`, accept it but do not teach it formally.
- The biggest sticking point is **order of arguments**. Hammer the rectangle/divide examples.
- The `_` underscore in `for _ in range(sides):` deserves a one-line comment ("we don't need the loop variable").
- Cambridge IGCSE pseudocode uses `PROCEDURE` and `FUNCTION` — show but do not require students to write pseudocode today; that's Session 29.
- Use `print(name, animal, age)` (commas) rather than f-strings for now to reduce syntax noise; f-strings appear only as bonus.

---

#### SESSION 26 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Parameter or Argument?

For each underlined item in the code below, write **P** for parameter or **A** for argument.

```python
def total_price(price, quantity):     # (1) ____  (2) ____
    print(price * quantity)

total_price(12, 3)                    # (3) ____  (4) ____
total_price(price=5, quantity=10)     # (5) ____  (6) ____
```

##### Part 2: Predict-the-Output

For each snippet, write your prediction in the box, then run it in Thonny.

**Snippet A:**

```python
def shout(word, times):
    for _ in range(times):
        print(word.upper(), "!")

shout("hello", 2)
shout("python", 3)
```

| Predicted output | Actual output |
|------------------|---------------|
|                  |               |
|                  |               |
|                  |               |
|                  |               |
|                  |               |
|                  |               |

**Snippet B (spot the swap):**

```python
def order(first, second):
    print(first, "before", second)

order("breakfast", "lunch")
order("lunch", "breakfast")
```

What is the **second** line of output? ____________________________________

**Snippet C (bug):**

```python
def add(a, b):
    print(a + b)

add(5)
```

Will this run? ________ If not, what error appears? __________________________

##### Part 3: Build & Refactor

Q5. Write a function `greet(name)` that prints `Hello, <name>! Welcome to Py-Club.` Call it three times with different names.

```
[your code here]




```

Q6. Write `area_rectangle(width, height)` that prints `Area of <w> x <h> rectangle = <area>`. Call it for (5,3), (10,4), (7,7).

```
[your code here]




```

Q7. **Refactor.** Below is a no-parameter function. Add **one** parameter so it can handle any country's flag colours. Then call it for at least 3 countries.

**BEFORE:**

```python
def announce_flag():
    print("The flag of France has 3 colours.")
```

**AFTER:**

```
[your refactored code here]



```

Q8. **Trace table.** Fill in the table for the calls below.

```python
def label(item, price, tax):
    total = price + tax
    print(item, "costs", total)

label("pen", 2, 1)
label("book", 10, 2)
label("bag", 25, 5)
```

| Call # | item | price | tax | total | Output |
|--------|------|-------|-----|-------|--------|
| 1      |      |       |     |       |        |
| 2      |      |       |     |       |        |
| 3      |      |       |     |       |        |

##### Reflection (3 prompts)
R1. In one sentence, what is the difference between a parameter and an argument?
________________________________________________________________________________
R2. Why does the order of arguments matter? Give a real example from your code today.
________________________________________________________________________________
R3. Look at Cambridge pseudocode `PROCEDURE Greet(Name : STRING)`. Translate it to Python.
________________________________________________________________________________

##### Bonus / Stretch Challenge

Write `pythagoras(a, b)` that prints the hypotenuse of a right-angled triangle (use `(a*a + b*b) ** 0.5`). Then write `triangle_report(name, a, b)` that prints the triangle's name and the hypotenuse, using `pythagoras` internally is fine but only after Session 27. Today, just print it inside `triangle_report`.

---

### Session 27: Return Values & Scope

---

#### SESSION 27 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 27 of 48 |
| **Title** | Return Values & Scope |
| **Unit** | Unit 5: Functions & Modular Design |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — `RETURN` in functions; local vs global identifiers; §7 algorithm trace tables |
| **Singapore Alignment** | O-Level 7155 Module 4 — return values, scope, side effects |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Use** the `return` statement correctly so a function gives back a value to its caller, in at least 3 examples.
2. **Distinguish** between *print-only* functions (procedures) and *return* functions (true functions), and choose the appropriate one for a given task.
3. **Identify** local vs global scope in a 10-line program with 100% accuracy on a labelling exercise.
4. **Debug** a scope error in a given buggy program by either adding `global` or (preferred) restructuring with parameters/return.

##### Materials Needed
- Thonny
- Worksheet S27
- "Scope ladder" diagram printout (one per pair)
- Two-column poster: PRINT vs RETURN

##### Procedure

**0–5 min: Warm-Up — "The Useless Calculator"**
Show:

```python
def add(a, b):
    print(a + b)

result = add(5, 3)
print("The result was:", result)
```

Ask predict-the-output. Most will say `8` then `The result was: 8`. Run it. The actual second line is `The result was: None`!

Ask: *"What is `None`? Why isn't it 8?"* Tease: *"Because `print` shows a value but does NOT give it back to the caller. We need a new word: `return`."*

**5–15 min: Introduction — `return`**

Side-by-side board:

| PRINT version (procedure) | RETURN version (true function) |
|---------------------------|---------------------------------|
| ```python\ndef add(a, b):\n    print(a + b)\n``` | ```python\ndef add(a, b):\n    return a + b\n``` |
| Use only when you want to **show** something to the user | Use when you want to **use** the value later |
| Calling: `add(5,3)` prints 8 | Calling: `total = add(5,3)` stores 8 in `total` |

Live demo:

```python
def add(a, b):
    return a + b

total = add(5, 3)
print("The result was:", total)         # 8

big = add(add(2, 3), add(4, 1))         # functions inside functions!
print("Big total:", big)                 # 10
```

Tell students:
> *"`return` ends the function immediately and hands a value back. Anything after `return` (in the same path) doesn't run."*

Demo:

```python
def first_positive(a, b):
    if a > 0:
        return a
    if b > 0:
        return b
    return 0

print(first_positive(-3, 7))   # 7
print(first_positive(5, 9))    # 5 (stops at first return)
print(first_positive(-1, -1))  # 0
```

**15–35 min: Guided Practice — Scope**

Now the harder concept. Draw the **scope ladder** on the board:

```
+--------------------------------------+
|  GLOBAL SCOPE (the main program)     |
|                                      |
|   +------------------------------+   |
|   |  LOCAL SCOPE (inside func)   |   |
|   |  parameters live here        |   |
|   |  variables made here die     |   |
|   |  when the function ends      |   |
|   +------------------------------+   |
+--------------------------------------+
```

Live demo 1 — local stays local:

```python
def double_it(x):
    answer = x * 2          # 'answer' is LOCAL
    return answer

result = double_it(5)
print(result)               # 10
print(answer)               # NameError: name 'answer' is not defined
```

Read it aloud: *"Local variables don't exist outside the function."*

Live demo 2 — read global is fine, but writing creates a new local:

```python
score = 0

def add_point():
    score = score + 1       # UnboundLocalError!
    print(score)

add_point()
```

Run it. Get the error. Discuss.

Show the two fixes:

**Fix A — `global` keyword (show but discourage):**

```python
score = 0

def add_point():
    global score
    score = score + 1
    print(score)

add_point()
add_point()
print(score)    # 2
```

> Teacher script: *"This works, but it makes functions depend on outside variables. It is a code smell. Cambridge will accept it; professionals avoid it."*

**Fix B — preferred: parameter + return:**

```python
def add_point(score):
    return score + 1

score = 0
score = add_point(score)
score = add_point(score)
print(score)    # 2
```

Stress: this version is **pure** — given the same input it always gives the same output, and it changes nothing outside.

**Common-bug demo: shadowing.**

```python
total = 100
def discount():
    total = 5            # creates a NEW local 'total'
    print("In func:", total)

discount()              # 5
print("Outside:", total) # 100 — the global is untouched!
```

Lead them through it on a trace table.

**35–50 min: Independent Practice — Worksheet**
Students complete S27 worksheet, especially the *fix-the-scope-bug* section.

**50–55 min: Sharing & Discussion**
Project two students' fixes for Q9. Compare `global` solution vs parameter/return solution. Vote: which is easier to read?

**55–60 min: Closure & Preview**
Exit ticket: *"Why is `local variables don't exist outside the function` a feature, not a bug?"* (Hint: it stops accidental name clashes.)

Preview: *"Tomorrow: making parameters **optional** with default values, like `greet(name, greeting='Hello')`."*

##### Differentiation
- **Support:** Provide a printed scope-ladder diagram to colour for each example.
- **Extension:** Introduce `def stats(numbers): return min(numbers), max(numbers)` — multiple return values via tuple unpacking. Foreshadows Unit 6.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| Use of `return` | Forgets `return`, uses `print` | Returns simple expr | Returns + caller stores | Returns + chains/composes calls |
| Print vs return | Confused | Knows definition | Picks right one for task | Refactors others' code |
| Scope identification | Cannot tell local from global | Identifies most | All correct on 10-line example | Predicts UnboundLocalError before running |
| Debug scope bug | Cannot fix | Fixes with `global` | Fixes with param/return | Explains *why* param/return is preferred |

##### Teacher Notes
- The `score = score + 1` UnboundLocalError baffles even adults. Take time on it.
- Resist teaching `nonlocal` today — it is out of scope (no pun) and confuses the global picture.
- Functional purity (no side effects) is a powerful idea — sneak it in but don't quiz on it.
- If a student returns multiple values via `return a, b` and unpacks with `x, y = func()`, celebrate but defer the formal lesson.
- Tie back to Cambridge pseudocode: `FUNCTION Add(a, b : INTEGER) RETURNS INTEGER ... RETURN a + b ... ENDFUNCTION`.

---

#### SESSION 27 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Print or Return?

For each function, decide if it should use **print**, **return**, or **both**, and write the keyword in the blank.

1. `area_rectangle(w, h)` — used inside other calculations: ________
2. `welcome_player(name)` — first thing the game shows: ________
3. `is_even(n)` — used in `if is_even(score):` ________
4. `format_money(amount)` — gives `"$12.50"` to be printed by another function: ________
5. `goodbye()` — final farewell screen: ________

##### Part 2: Predict-the-Output (Scope Puzzles)

**Puzzle A:**

```python
def make_double(x):
    doubled = x * 2
    return doubled

result = make_double(7)
print(result)
print(doubled)
```

What happens on the LAST line? ____________________________________________

**Puzzle B:**

```python
name = "Global Aisha"

def greet():
    name = "Local Aisha"
    print("Inside:", name)

greet()
print("Outside:", name)
```

| Predicted output | Actual output |
|------------------|---------------|
|                  |               |
|                  |               |

**Puzzle C:**

```python
def add(a, b):
    return a + b
    print("This line never runs")

x = add(2, 3)
print(x)
```

What prints? ________ Why does the `print` line not run? ____________________

**Puzzle D — UnboundLocal:**

```python
counter = 0

def tick():
    counter = counter + 1
    print(counter)

tick()
```

What error appears? ________________________________________________________

##### Part 3: Refactor "print" → "return"

Q6. Refactor each function so it **returns** the value instead of printing it. Then update the call site to print the returned value.

**Original:**

```python
def square(n):
    print(n * n)

square(4)
```

**Refactored:**

```
[your code here]



```

**Original:**

```python
def full_name(first, last):
    print(first + " " + last)

full_name("Ada", "Lovelace")
```

**Refactored:**

```
[your code here]



```

##### Part 4: Fix the Scope Bug

Q7. The program below is supposed to add up coins. Fix the bug **with `global`** first, then write a **second version** that uses parameters and return instead.

**Buggy:**

```python
total = 0

def add_coin(value):
    total = total + value

add_coin(5)
add_coin(10)
print(total)         # expected 15
```

**Version 1 — `global` fix:**

```
[your code here]




```

**Version 2 — preferred (parameter + return):**

```
[your code here]




```

Q8. **Spot the scope bug.** Circle the offending line and explain in one sentence.

```python
price = 100

def apply_discount():
    price = price - 10
    print(price)

apply_discount()
```

Explanation: ______________________________________________________________

##### Reflection (3 prompts)
R1. Why is `return` more flexible than `print` for most calculations?
________________________________________________________________________________
R2. The phrase *"local variables don't exist outside the function"* — why is this actually GOOD?
________________________________________________________________________________
R3. The `global` keyword is allowed but discouraged. Why?
________________________________________________________________________________

##### Bonus / Stretch Challenge

Write a function `min_max(numbers)` that takes a list and **returns two values** — the smallest and largest — using `return small, large`. At the call site, unpack with `lo, hi = min_max([3,1,4,1,5,9,2,6])`. Print both.

```
[your code here]




```

---

### Session 28: Default Parameters

---

#### SESSION 28 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 28 of 48 |
| **Title** | Default Parameters |
| **Unit** | Unit 5: Functions & Modular Design |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — flexibility in sub-routine interfaces; algorithm efficiency through configurable behaviour |
| **Singapore Alignment** | O-Level 7155 Module 4 — sub-routine design with optional inputs; Module 5 — code maintainability |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Define** functions with default parameter values using the `def f(x, y=value):` syntax in at least 3 worked examples.
2. **Call** a default-parameter function with both *some* and *all* arguments supplied, predicting the output correctly each time.
3. **Order** parameters correctly so that all required parameters appear before any optional ones (avoiding `SyntaxError`).
4. **Recognise** the mutable-default trap and apply the recommended `None` pattern in 1 example.

##### Materials Needed
- Thonny
- Worksheet S28
- Slide showing the rule: *required before optional*
- "Default = fallback" poster

##### Procedure

**0–5 min: Warm-Up — "Almost the Same"**
Show two functions:

```python
def greet_hello(name):
    print("Hello,", name)

def greet_hi(name):
    print("Hi,", name)
```

Ask: *"This is silly — they're 95% identical. How could one function do both?"* Take guesses. Some will say "add another parameter". Yes — and the next idea is: *what if we make that parameter optional with a default?*

**5–15 min: Introduction — Default Parameter Values**

Live-type:

```python
def greet(name, greeting="Hello"):
    print(greeting, name)

greet("Aisha")                    # uses default → Hello Aisha
greet("Ben", "Hi")                # overrides   → Hi Ben
greet("Chloe", "Welcome,")        # overrides   → Welcome, Chloe
```

Annotate:
- `greeting="Hello"` is the default.
- Calling with one argument fills only `name`; `greeting` falls back to `"Hello"`.
- Calling with two arguments overrides the default.

Sentence to chant: *"Defaults are fallbacks — used only when the caller doesn't supply that argument."*

**The order rule.** Try (and let it fail):

```python
def bad(greeting="Hello", name):     # SyntaxError!
    print(greeting, name)
```

Run it. `SyntaxError: non-default argument follows default argument`. Discuss why this rule exists: Python fills positional arguments left-to-right, so if `greeting` defaulted but `name` didn't, calling `bad("Aisha")` would be ambiguous.

**Rule on board:**

> **REQUIRED parameters before OPTIONAL parameters.**

**15–35 min: Guided Practice — Three demos**

**(a) Banner builder.**

```python
def banner(text, char="*", width=30):
    line = char * width
    print(line)
    print(text.center(width))
    print(line)

banner("Hello!")
banner("Game Over", char="-")
banner("VICTORY", char="=", width=40)
```

Three calls, three different banners, one function. Beautiful.

**(b) Power calculator.**

```python
def power(base, exp=2):
    return base ** exp

print(power(5))      # 25  (default exp=2 = squared)
print(power(5, 3))   # 125
print(power(2, 10))  # 1024
```

**(c) Mutable default trap (briefly!).**

```python
def add_item(item, basket=[]):     # BAD!
    basket.append(item)
    return basket

print(add_item("apple"))     # ['apple']
print(add_item("banana"))    # ['apple', 'banana']  -- surprise!
```

Why? Python builds the default `[]` **once** when `def` runs, and reuses the same list every call.

**Recommended fix — the `None` pattern:**

```python
def add_item(item, basket=None):
    if basket is None:
        basket = []
    basket.append(item)
    return basket

print(add_item("apple"))     # ['apple']
print(add_item("banana"))    # ['banana']  -- correct!
```

> Teacher script: *"You don't need to memorise this today, but if your default ever needs to be a list or dict, write `=None` and check inside."*

**(d) Spot-the-bug warm-up:**

```python
def label(text, font="Arial", size):     # error!
    print(text, font, size)
```

Why does this fail? (Required `size` after default `font`.) Fix: move `size` before `font` *or* give `size` a default too.

**35–50 min: Independent Practice — Worksheet S28**
Students complete the worksheet. Watch for parameter-order errors and the mutable-default trap.

**50–55 min: Sharing & Discussion**
Two volunteers project their `make_invoice` (Q6) calls. Discuss: *"When is a default helpful?"* (Anything that has a sensible *most-of-the-time* value: `currency='$'`, `tax=0.07`, `language='en'`.)

**55–60 min: Closure & Preview**
Exit ticket: *"Write the rule about parameter order in 8 words or fewer."* Preview: *"Tomorrow we use everything we know — parameters, return, defaults — to **decompose** a real problem from scratch using top-down design."*

##### Differentiation
- **Support:** Provide pre-written function signatures; students fill bodies and call sites.
- **Extension:** Add a fourth optional parameter `prefix=">>"` to the banner. Use `**kwargs` only if a curious student asks (out-of-scope; mention it exists in Unit 7).

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| Default syntax | Forgets `=` value, syntax errors | One default works | Multiple defaults work | Mixed positional + keyword + default |
| Call variety | Only calls with all args | Calls with default once | Calls 3 times: default, override, mix | Designs API: chooses smart defaults |
| Order rule | Violates rule | Spots violation w/ help | Spots and fixes | Explains *why* rule exists |
| Mutable trap | Unaware | Aware after demo | Aware + uses `None` pattern when prompted | Predicts the trap and applies pattern unprompted |

##### Teacher Notes
- Do not over-emphasise the mutable trap — students will rarely meet it. One demo + the `None` pattern is enough.
- The `text.center(width)` method is a freebie — celebrate it; previews Unit 6 string methods.
- If using turtle, defaults are great for `pen_color="black"`, `pen_size=2`.
- Reinforce: defaults make functions *configurable but easy to start with*.
- Encourage students to refactor previous-session functions and add at least one default.

---

#### SESSION 28 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Predict-the-Output

```python
def greet(name, greeting="Hello", punctuation="!"):
    print(greeting, name, punctuation)

greet("Aisha")
greet("Ben", "Hi")
greet("Chloe", "Yo", "?!")
greet("Dan", punctuation=".")
```

| Call | Predicted output | Actual output |
|------|------------------|---------------|
| 1    |                  |               |
| 2    |                  |               |
| 3    |                  |               |
| 4    |                  |               |

##### Part 2: Spot the Default Bug

For each snippet, identify the bug and write a fix.

**Bug 1:**

```python
def label(size, color="red"):
    print(color, size)

label("blue", 12)
```

What gets printed? __________________ Why is it wrong? ________________________
Fix: ____________________________________________________________________

**Bug 2:**

```python
def order(item, quantity=1, price):
    total = quantity * price
    print(item, total)
```

What error appears at definition time? _______________________________________
Fix (re-order parameters): __________________________________________________

**Bug 3 — the classic:**

```python
def add_to_cart(item, cart=[]):
    cart.append(item)
    return cart

print(add_to_cart("apple"))
print(add_to_cart("banana"))
```

What is the second printed line? ______________________
Why does this happen? ___________________________________________________
Rewrite using the `None` pattern:

```
[your code here]




```

##### Part 3: Design-the-Default

Q4. For each function, suggest a sensible default value for the underlined parameter.

| Function | Underlined param | Sensible default |
|----------|------------------|------------------|
| `make_user(name, age, country)` | country | __________ |
| `pay(amount, currency)` | currency | __________ |
| `print_quiz(name, attempts)` | attempts | __________ |
| `greet(name, language)` | language | __________ |
| `draw_circle(radius, color)` | color | __________ |

Q5. Write a function `make_invoice(item, price, tax=0.07, currency="$")` that prints something like:

```
Item: Robot kit
Price: $50.00
Tax: $3.50
Total: $53.50
```

Then call it three ways:
- `make_invoice("Robot kit", 50)`
- `make_invoice("Sensor", 20, tax=0.10)`
- `make_invoice("Battery", 10, currency="€")`

```
[your code here]




```

Q6. **Build a parameterised banner-printer.** Write `banner(text, char="*", width=30, repeat=1)`. The `repeat` controls how many full banners print stacked. Test with at least 4 different calls.

```
[your code here]





```

##### Reflection (3 prompts)
R1. Why must required parameters come before optional ones?
________________________________________________________________________________
R2. Give one real-world example where a default value would save you typing.
________________________________________________________________________________
R3. Why is `def f(x, items=[]):` dangerous? What is the safer pattern?
________________________________________________________________________________

##### Bonus / Stretch Challenge

Write `make_id(name, length=4, prefix="USR")` that returns a string like `USR-AISHA-0001`. The `length` controls how many digits the numeric tail has (use `str(n).zfill(length)`). Test by generating IDs for 5 students stored in a list.

```
[your code here]





```

---

### Session 29: Top-Down Design with Functions

---

#### SESSION 29 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 29 of 48 |
| **Title** | Top-Down Design with Functions |
| **Unit** | Unit 5: Functions & Modular Design |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §7 — algorithm design, decomposition; §10 — sub-routine structure; pseudocode `PROCEDURE`/`FUNCTION` |
| **Singapore Alignment** | O-Level 7155 Module 1 — problem analysis & decomposition; Module 4 — sub-routine modular design; EdTech Masterplan CT pillar: decomposition |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Decompose** a multi-step problem into 4 or more named sub-tasks before writing any Python code.
2. **Write pseudocode** for each sub-task using Cambridge IGCSE conventions (`PROCEDURE`, `FUNCTION RETURNS`, `INPUT`, `OUTPUT`).
3. **Translate** pseudocode into Python function stubs (signature + `pass`) and then fill them in one at a time.
4. **Compose** the sub-functions inside a `main()` driver to solve the whole problem end-to-end.

##### Materials Needed
- Thonny
- Worksheet S29
- Whiteboard / large sticky notes for the decomposition tree
- Cambridge pseudocode reference card
- Printed *function-stub table* template

##### Procedure

**0–5 min: Warm-Up — "Eat the Elephant"**
Ask: *"How do you eat an elephant?"* (One bite at a time.) That is **decomposition** — the most important skill in the Singapore EdTech Masterplan and the Cambridge IGCSE problem-solving paper.

**5–15 min: Introduction — Top-Down Design**

State the goal:

> **Problem:** *Write a program that prints a student report card given a name and 4 test scores. Output should show the name, the average, and a letter grade (A/B/C/D/F).*

Resist the urge to type. Instead, decompose on the board:

```
                  Print Report Card
                          |
   +-------+-------------+-------------+----------+
   |       |             |             |          |
get_grades  compute_average  assign_letter   print_report
```

Now write **pseudocode for each function** in Cambridge style:

```
FUNCTION get_grades() RETURNS ARRAY OF INTEGER
    DECLARE grades : ARRAY[1:4] OF INTEGER
    FOR i ← 1 TO 4
        OUTPUT "Enter score ", i
        INPUT grades[i]
    NEXT i
    RETURN grades
ENDFUNCTION

FUNCTION compute_average(grades : ARRAY) RETURNS REAL
    total ← 0
    FOR each score IN grades
        total ← total + score
    RETURN total / LENGTH(grades)
ENDFUNCTION

FUNCTION assign_letter(average : REAL) RETURNS CHAR
    IF average >= 80 THEN RETURN 'A'
    ELSE IF average >= 70 THEN RETURN 'B'
    ELSE IF average >= 60 THEN RETURN 'C'
    ELSE IF average >= 50 THEN RETURN 'D'
    ELSE RETURN 'F'
ENDFUNCTION

PROCEDURE print_report(name, average, letter)
    OUTPUT "===== REPORT CARD ====="
    OUTPUT "Name: ", name
    OUTPUT "Average: ", average
    OUTPUT "Grade: ", letter
ENDPROCEDURE
```

**15–35 min: Guided Practice — Stub then fill**

**Stage 1: Skeleton with `pass`** — type all four function signatures, leave bodies as `pass`:

```python
def get_grades():
    pass

def compute_average(grades):
    pass

def assign_letter(average):
    pass

def print_report(name, average, letter):
    pass

def main():
    name = input("Student name: ")
    grades = get_grades()
    avg = compute_average(grades)
    letter = assign_letter(avg)
    print_report(name, avg, letter)

main()
```

Discuss: even though it does nothing yet, the **architecture** is complete. You can read the `main()` and instantly see the whole algorithm.

**Stage 2: Fill in one function at a time, test each.**

```python
def get_grades():
    grades = []
    for i in range(1, 5):
        score = int(input(f"Enter score {i}: "))
        grades.append(score)
    return grades
```

Run a quick test inside Thonny shell: `get_grades()` then enter four numbers — confirm a list comes back.

```python
def compute_average(grades):
    total = 0
    for score in grades:
        total += score
    return total / len(grades)

# Test
print(compute_average([80, 70, 60, 50]))    # 65.0
```

```python
def assign_letter(average):
    if average >= 80: return "A"
    if average >= 70: return "B"
    if average >= 60: return "C"
    if average >= 50: return "D"
    return "F"

# Test
print(assign_letter(85))   # A
print(assign_letter(45))   # F
```

```python
def print_report(name, average, letter):
    print("===== REPORT CARD =====")
    print("Name:   ", name)
    print("Average:", round(average, 1))
    print("Grade:  ", letter)
```

Now run `main()` end-to-end. It works.

**Why is this powerful?** Discuss:
- Each function is **testable in isolation**.
- If the letter rule changes, you only edit `assign_letter`.
- A teammate could write `compute_average` while you write `print_report`.
- The pseudocode plan is the same in any language — Python, Java, C++.

**35–50 min: Independent Practice — Worksheet S29**
Students decompose a *new* problem (a "movie ticket calculator") on paper, write pseudocode, then build the stubs.

**50–55 min: Sharing & Discussion**
A volunteer projects their decomposition tree. Class critiques: *"Are the function names clear? Is anything missing? Should two functions become one — or one become two?"*

**55–60 min: Closure & Preview**
Exit ticket: *"Write the 3 steps of top-down design."* (1. Decompose into named sub-tasks. 2. Pseudocode each. 3. Stub then fill.) Preview Project 5: *"Tomorrow you put it all together — design first, code second, build a Modular Math Helper with 5+ functions."*

##### Differentiation
- **Support:** Provide a half-completed decomposition tree; students fill in the missing leaves and pseudocode.
- **Extension:** Add a fifth function `save_report(filename, name, avg, letter)` that writes to a text file (preview Unit 7 file I/O).

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| Decomposition | 1 mega-function | 2 functions, uneven | ≥4 single-purpose functions | ≥4, named clearly, single responsibility each |
| Pseudocode | Skips it | Pseudocode written but not Cambridge style | Cambridge-style for all functions | Pseudocode + reasoning for return types |
| Stub-then-fill | Writes whole program at once | Stubs but fills randomly | Stubs first, fills one-at-a-time, tests each | Tests each stub in isolation before composing |
| Composition in `main` | No `main`, top-level mess | `main` exists but messy | `main` reads like the algorithm | `main` is 5–8 lines of clear orchestration |

##### Teacher Notes
- The temptation to start typing immediately is strong. **Confiscate keyboards** for the first 10 minutes if needed.
- Cambridge pseudocode uses arrow assignment `←` — accept `=` from kids; teach the arrow as bonus.
- Praise *clear function names* loudly. `get_grades` > `gg` > `function1`.
- The `main()` pattern foreshadows `if __name__ == "__main__":` — mention but defer.
- Watch for students who hide all logic in `print_report`; remind them to keep each function single-purpose.

---

#### SESSION 29 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Decompose This Mess

Q1. Below is a monolithic program. Decompose it into 3+ functions on paper. Draw a tree.

```python
print("=== TICKET PRICE ===")
age = int(input("Age: "))
day = input("Day (mon/tue/.../sun): ")
member = input("Member? (y/n): ")

if age < 12:
    base = 5
elif age >= 60:
    base = 6
else:
    base = 10

if day in ("sat", "sun"):
    base = base + 2

if member == "y":
    base = base * 0.9

print("Total: $", base)
```

**Decomposition tree:**

```
                Calculate Ticket Price
                          |
    +---------------+-----+-----+--------------+
    |               |           |              |
    ?               ?           ?              ?

(write your function names in the boxes)
```

Q2. List your function names with one-line purposes:

| # | Function name | Purpose |
|---|---------------|---------|
| 1 | _______________ | _______________________________________ |
| 2 | _______________ | _______________________________________ |
| 3 | _______________ | _______________________________________ |
| 4 | _______________ | _______________________________________ |

##### Part 2: Pseudocode First

Q3. Write Cambridge-style pseudocode for **two** of your functions from Q2. Use `FUNCTION ... RETURNS ...` or `PROCEDURE ...`.

```
Function 1:




Function 2:




```

##### Part 3: Stub Then Fill

Q4. Type the **stubs** in Thonny first (each function has just `pass`). Run the empty program — it should do nothing without errors.

```
[stub-only code]




```

Q5. Now fill in **one function at a time**, testing each in the Thonny shell before moving on. Paste the final program here:

```
[final code]








```

Q6. **Build a 4-function `student_report` clone** for a different scenario: instead of student grades, build a `fitness_report` that takes a name and 4 daily step counts, computes the average, assigns a fitness rating (`Active >= 10000`, `Moderate >= 7000`, `Light >= 4000`, `Sedentary` otherwise), and prints a report. Plan your 4 functions in this table BEFORE coding:

| Function | Parameters | Returns / does | Single-line purpose |
|----------|-----------|----------------|---------------------|
| `get_steps`     |  |  |  |
| `compute_average` |  |  |  |
| `assign_rating` |  |  |  |
| `print_report`  |  |  |  |

Now code it:

```
[your code here]








```

##### Reflection (3 prompts)
R1. Why is decomposition called "the highest-level computational thinking skill"?
________________________________________________________________________________
R2. What is the advantage of writing pseudocode BEFORE Python?
________________________________________________________________________________
R3. Imagine the grade boundaries change next year. Which function would you edit, and which functions would stay the same? What does this teach you about modular design?
________________________________________________________________________________

##### Bonus / Stretch Challenge

Add a fifth function `save_report(filename, name, average, rating)` that writes the report to a `.txt` file using:

```python
with open(filename, "w") as f:
    f.write(...)
```

Test that the file appears in your folder and contains the right content. (This previews Unit 7 — File I/O.)

---

### Session 30: Project 5 — Modular Math Helper

---

#### SESSION 30 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 30 of 48 |
| **Title** | Project 5 — Modular Math Helper |
| **Unit** | Unit 5: Functions & Modular Design |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §7 algorithm design, §10 sub-routines with parameters and return; project-style assessment objective AO2 |
| **Singapore Alignment** | O-Level 7155 Module 4 sub-routines + Module 1 problem-solving; integrated project task |

##### Learning Objectives (SMART)
By the end of this session, students will have:
1. **Designed** (on paper) a Modular Math Helper application with at least 5 named function stubs and a function-stub table BEFORE coding.
2. **Implemented** at least 5 distinct, single-purpose math functions, each with parameters and a `return` value.
3. **Composed** the functions in a `main()` menu loop that takes user choice, calls the right function, displays the result, and loops until "Quit".
4. **Peer-tested** another student's program against a 5-criterion rubric and provided one written improvement suggestion.

##### Materials Needed
- Thonny
- Worksheet S30 (project planning template)
- Printed peer-test rubric
- Printed "function menu" cards (optional — students draw the menu on paper first)
- Stickers / certificates for *Modular Math Master*

##### Procedure

**0–5 min: Warm-Up — Project Briefing**

Show the brief:

> **Project: Modular Math Helper.** Build a menu-driven program. The user picks a calculation, supplies inputs, and gets a result. The program must:
> - have **at least 5 distinct functions**, each with parameters and a `return` value;
> - include a `main()` loop that runs until the user picks "Quit";
> - import `sqrt` and `pi` from `math` (preview of Unit 6);
> - be designed on paper FIRST.

The 5 functions must be chosen from (or similar to):
- `area_rectangle(w, h)`
- `area_circle(r)`
- `area_triangle(b, h)`
- `solve_quadratic(a, b, c)` — returns the two roots or `None` if discriminant < 0
- `fibonacci(n)` — returns the *n*-th Fibonacci number
- `is_prime(n)` — returns `True`/`False`
- `factorial(n)`
- `bmi(weight, height)`

**5–15 min: Design Phase (NO TYPING)**

Students fill in the planning template on the worksheet:
- list the 5 chosen functions
- write each signature with parameter names + return type
- write 1-line pseudocode purpose for each

Teacher inspects each plan and **signs it off** before the student opens Thonny.

Display this driver-loop template on the board:

```
PROCEDURE main()
    OUTPUT "===== MODULAR MATH HELPER ====="
    REPEAT
        OUTPUT menu
        choice ← INPUT
        IF choice = '1' THEN
            ... call function 1 ...
        ELSE IF choice = '2' THEN
            ... call function 2 ...
        ...
        ELSE IF choice = 'q' THEN
            BREAK
        ENDIF
    UNTIL FALSE
ENDPROCEDURE
```

**15–35 min: Build Phase (Guided)**

Live-type a *minimal skeleton* together so no one is stuck:

```python
from math import sqrt, pi

def area_rectangle(w, h):
    return w * h

def area_circle(r):
    return pi * r * r

def solve_quadratic(a, b, c):
    d = b * b - 4 * a * c
    if d < 0:
        return None
    root1 = (-b + sqrt(d)) / (2 * a)
    root2 = (-b - sqrt(d)) / (2 * a)
    return root1, root2

def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a

def is_prime(n):
    if n < 2:
        return False
    for k in range(2, int(sqrt(n)) + 1):
        if n % k == 0:
            return False
    return True

def show_menu():
    print()
    print("--- Choose ---")
    print("1) Area of rectangle")
    print("2) Area of circle")
    print("3) Solve quadratic")
    print("4) Fibonacci(n)")
    print("5) Is prime?")
    print("q) Quit")

def main():
    print("===== MODULAR MATH HELPER =====")
    while True:
        show_menu()
        choice = input("Pick: ").strip().lower()
        if choice == "1":
            w = float(input("width: "))
            h = float(input("height: "))
            print("Area =", area_rectangle(w, h))
        elif choice == "2":
            r = float(input("radius: "))
            print("Area =", round(area_circle(r), 2))
        elif choice == "3":
            a = float(input("a: ")); b = float(input("b: ")); c = float(input("c: "))
            roots = solve_quadratic(a, b, c)
            if roots is None:
                print("No real roots.")
            else:
                print("Roots:", roots)
        elif choice == "4":
            n = int(input("n: "))
            print("Fib =", fibonacci(n))
        elif choice == "5":
            n = int(input("n: "))
            print("Prime?" , is_prime(n))
        elif choice == "q":
            print("Bye!")
            break
        else:
            print("Unknown choice.")

main()
```

After the skeleton runs, students **swap one function for a different choice from the brief** (e.g., replace `fibonacci` with `factorial`) so the project becomes their own.

**Stretch (if quick):** Add a `history` list at the top of `main()`. After every successful calculation, append a string like `"area_rectangle(5,3)=15"` to it. Add a menu option `h` to print history.

```python
history = []

# inside choice == "1":
result = area_rectangle(w, h)
history.append(f"area_rectangle({w},{h}) = {result}")
print("Area =", result)

# new option
elif choice == "h":
    for line in history:
        print(line)
```

**35–50 min: Independent Practice — Build, Test, Polish**

Students customise their helper. Teacher circulates with the rubric clipboard, ticking criteria as they appear.

**50–55 min: Sharing & Peer Test**

Students pair up and run each other's programs. Each tester completes the peer-test rubric on the worksheet and writes ONE concrete improvement.

**55–60 min: Closure**

Whole-class round-robin: each student says ONE function they wrote and ONE thing their peer tester praised.

Award: **Modular Math Master** sticker for any student whose program scored ≥17/20 on the rubric. Preview Unit 6: *"Next: lists, dictionaries, and the `math` module — your helper will get even more powerful."*

##### Differentiation
- **Support:** Allow exact reuse of the live-typed skeleton, but require the student to add a 6th function of their choosing (with stub-then-fill).
- **Extension:** Wrap each function with a *try/except* so bad input doesn't crash the program. Add input validation. Persist `history` to a file (preview Unit 7).

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| Design first | No plan | Plan written but skipped | Plan signed off, followed | Plan + 6th function + signature documented |
| Function count & quality | <5, or some missing return | 5 functions, some print-only | 5 functions, all return, single-purpose | 5+ pure functions with sensible defaults |
| Menu loop | No loop | Loop but no quit | Clean menu, quit works, invalid input handled | Loop + history + try/except |
| Peer test feedback | Not done | Ticks only | Ticks + 1 improvement suggestion | Ticks + actionable suggestion + offers fix |
| Code clarity | No comments, bad names | Some good names | Descriptive names, minimal comments | Names + docstring + tested edge cases |

##### Teacher Notes
- The 10-minute design phase is non-negotiable. Walk around with a marker pen to sign off plans.
- Encourage students to *test each function alone* in the Thonny shell before wiring it into the menu.
- Watch for "wall of `if`" — if a student has 8+ branches, suggest a dictionary `{ "1": area_rectangle, ... }` (preview Unit 6) but only if they're flying.
- The `solve_quadratic` returning `None` or a tuple is a fantastic teaching moment for "functions can return different types".
- Celebrate students who refactored without prompting (e.g., extracted `read_float()` helper). That is mastery thinking.

---

#### SESSION 30 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Project Planning Template (Complete BEFORE coding — get teacher signature)

P1. **Pick at least 5 functions** for your Math Helper. Tick from the list or invent your own:

- [ ] `area_rectangle(w, h)`
- [ ] `area_circle(r)`
- [ ] `area_triangle(base, height)`
- [ ] `solve_quadratic(a, b, c)`
- [ ] `fibonacci(n)`
- [ ] `is_prime(n)`
- [ ] `factorial(n)`
- [ ] `bmi(weight_kg, height_m)`
- [ ] My own: ______________________________________

P2. **Function-stub table.** Fill in BEFORE coding.

| # | Function name | Parameters | Returns | One-line purpose |
|---|---------------|-----------|---------|------------------|
| 1 |               |           |         |                  |
| 2 |               |           |         |                  |
| 3 |               |           |         |                  |
| 4 |               |           |         |                  |
| 5 |               |           |         |                  |

P3. **Menu sketch.** Draw what your menu will look like on screen:

```
[menu sketch]






```

**Teacher signature (plan approved): _______________________**

##### Part 2: Build Checklist

Tick each item as you complete it. Do NOT skip.

- [ ] Created file `math_helper.py` in Thonny.
- [ ] `from math import sqrt, pi` at top.
- [ ] Wrote all 5 function stubs with `pass` first.
- [ ] Filled in function 1, tested in shell.
- [ ] Filled in function 2, tested in shell.
- [ ] Filled in function 3, tested in shell.
- [ ] Filled in function 4, tested in shell.
- [ ] Filled in function 5, tested in shell.
- [ ] Wrote `show_menu()` function.
- [ ] Wrote `main()` with `while True:` loop and `q` to quit.
- [ ] All 5 functions reachable from menu.
- [ ] Invalid choice prints "Unknown choice." and loops.
- [ ] Saved file and ran end-to-end successfully.

##### Part 3: Final Code

Paste your final code (or staple a printout):

```
[your final code here]
















```

##### Part 4: Peer-Test Rubric

**Tester name: __________________________** **Author name: __________________________**

| # | Criterion | Pass / Fail | Note |
|---|-----------|-------------|------|
| 1 | Menu appears clearly with all options | / | |
| 2 | At least 5 functions are reachable | / | |
| 3 | Each function returns (not just prints) | / | |
| 4 | Quit option works cleanly | / | |
| 5 | Invalid input handled gracefully | / | |
| 6 | Function names are descriptive | / | |
| 7 | One stretch feature present (history, validation, etc.) | / | |

**One concrete improvement I would suggest:**
________________________________________________________________________________
________________________________________________________________________________

##### Reflection (3 prompts)
R1. Which of your 5 functions are *pure* (always same output for same input, no side effects)? Which are not, and why?
________________________________________________________________________________
R2. If a teacher asked you to add a sixth function next week, how easy would that be? What does this say about modular design?
________________________________________________________________________________
R3. Compare today's program to the very first program you wrote in Session 1 of this course. What is the biggest *structural* difference?
________________________________________________________________________________

##### Bonus / Stretch Challenge

Add a `history` feature:
1. At the top of `main()`, create `history = []`.
2. After every successful calculation, append a string like `"area_rectangle(5, 3) = 15"` to `history`.
3. Add a new menu option `h` that prints all history lines.
4. **Super-stretch:** when the user quits, save history to a `history.txt` file using:

```python
with open("history.txt", "w") as f:
    for line in history:
        f.write(line + "\n")
```

This previews Unit 7 (File I/O). Show your teacher the saved file in the folder.

---
