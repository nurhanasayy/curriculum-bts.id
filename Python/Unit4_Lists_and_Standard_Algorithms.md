# Python Programming for Kids: Lesson Plans & Worksheets
## Unit 4: Lists & Standard Algorithms (Sessions 19–24)

### Unit Overview
Unit 4 is the pivotal middle of the course, introducing **lists** — Python's equivalent of the "1D array" required by Cambridge IGCSE 0478 §10 and Singapore O-Level 7155 Module 4 — together with the two **standard algorithms** mandated by both syllabi: **linear search** and **bubble sort**. Learners progress from creating, indexing, and mutating lists, through using built-in list methods and the accumulator pattern, into reading and writing IGCSE-style pseudocode for searching and sorting, and finally to working with **tuples and dictionaries** (the natural next step toward records and tables). The unit closes with **Project 4: Quiz & Leaderboard App**, where students apply linear search and bubble sort in a real, playable program. By the end of these six sessions, learners can store collections of related data, choose appropriate operations on them, hand-trace standard algorithms, and explain when to write their own algorithm versus reaching for `sorted()`.

---

### Session 19: Lists Basics

---

#### SESSION 19 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 19 of 48 |
| **Title** | Lists Basics — Storing a Collection of Values |
| **Unit** | Unit 4: Lists & Standard Algorithms |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — 1D arrays, indexing, length; Lower Secondary Computing 0860 — sequences of data |
| **Singapore Alignment** | O-Level 7155 Module 4 — list creation, indexing, traversal |

##### Learning Objectives (SMART)
By the end of this session, learners will be able to:
1. **Create** a Python list using the literal syntax `[ ... ]` and store **at least 5 related items** in a single variable.
2. **Access** any element of a list using **positive and negative indices**, and **extract sub-lists** using **slicing** with `[start:stop]` notation, with **3/3 correctness** on the worksheet's indexing puzzles.
3. **Iterate** over a list using **two distinct patterns** — `for x in nums:` and `for i in range(len(nums)):` — and explain when each is preferred.
4. **Distinguish** mutable lists from immutable strings by **modifying a list element by index** and predicting the outcome of the same attempt on a string.

##### Materials Needed
- Thonny IDE (Python 3.11+) installed on each student's machine.
- Printed worksheet (one per student) — Session 19.
- Whiteboard / shared screen for live coding.
- "Index Card" props: 6 numbered index cards labelled `0` through `5` to physically demonstrate list positions.
- Reference handout: Cambridge IGCSE 0478 pseudocode for arrays (one-page summary).

##### Procedure

**0–5 min: Warm-Up — "How many variables would we need?"**
Pose a question on the board: *"You want to store the names of all 30 students in your class. How many variables do you need with what we know so far?"* Take answers, then say: *"Today we learn one variable that holds them all — a **list**."* Show the contrast:
```python
# The OLD way — painful!
student1 = "Aisha"
student2 = "Bilal"
student3 = "Chen"
# ... 27 more lines! 

# The NEW way — one line, one name
students = ["Aisha", "Bilal", "Chen"]
```

**5–15 min: Introduction — Anatomy of a List**
Walk through these four core ideas with live code in Thonny.

(1) **List literal** — square brackets, comma-separated:
```python
nums = [3, 1, 4, 1, 5, 9]
print(nums)          # [3, 1, 4, 1, 5, 9]
print(type(nums))    # <class 'list'>
```

(2) **Indexing** — positions start at **0** (this is universal in computing):
```python
nums = [3, 1, 4, 1, 5, 9]
print(nums[0])    # 3   <- first item
print(nums[1])    # 1
print(nums[5])    # 9   <- last item
print(nums[-1])   # 9   <- "from the end"
print(nums[-2])   # 5
```
Use the index-card props: hand 6 cards (labelled 0–5) to 6 students standing in a line. Ask: *"What's at index 2? At index -1?"* Make the abstract physical.

(3) **Length** — `len()` works on lists just like strings:
```python
nums = [3, 1, 4, 1, 5, 9]
print(len(nums))           # 6
print(nums[len(nums) - 1]) # 9  <- last item, the "long way"
```

(4) **Slicing** — same `[start:stop]` rule as strings, **stop is exclusive**:
```python
letters = ["P", "y", "t", "h", "o", "n"]
print(letters[0:3])   # ['P', 'y', 't']
print(letters[2:])    # ['t', 'h', 'o', 'n']
print(letters[:4])    # ['P', 'y', 't', 'h']
print(letters[-2:])   # ['o', 'n']
```

**Predict-the-output (on whiteboard, students vote):**
```python
data = [10, 20, 30, 40, 50]
print(data[1])
print(data[-1])
print(data[1:4])
```
*Expected: `20`, `50`, `[20, 30, 40]`.*

**15–35 min: Guided Practice — Iteration & Mutability**

(1) **Two ways to iterate.** Type both, side by side, and discuss:
```python
fruits = ["apple", "banana", "cherry"]

# Pattern A: directly over items (cleaner when you only need the value)
for fruit in fruits:
    print("I like", fruit)

# Pattern B: over indices (use when you need the position too)
for i in range(len(fruits)):
    print(i, "->", fruits[i])
```
Ask: *"In Pattern A, can you tell which one is fruit number 2? In Pattern B, can you?"* Pattern B is essential when the **index matters** (renumbering, comparing neighbours) — it returns repeatedly in the search/sort sessions.

(2) **Mutability — lists can change, strings cannot.** This is a core IGCSE distinction.
```python
# Lists are MUTABLE
colours = ["red", "green", "blue"]
colours[1] = "lime"
print(colours)   # ['red', 'lime', 'blue']  

# Strings are IMMUTABLE
word = "hello"
word[0] = "H"     # TypeError!
```
Run the broken `word[0] = "H"` deliberately so students see the error. Ask: *"How can we still get `Hello` from `hello`?"* Lead them to `word = "H" + word[1:]` — reinforcing that strings produce **new** strings.

(3) **Heterogeneous lists work, but…** Show that Python *allows* mixed types but the convention is homogeneous:
```python
weird = [42, "hello", True, 3.14]   # legal but rarely a good idea
scores = [85, 92, 78, 90]            # GOOD — all the same kind
```
*Rule of thumb: a list usually represents "many of the same thing".*

**Mini-trace table** for `nums = [4, 2, 8, 6]`:

| Step | i | nums[i] | total |
|------|---|---------|-------|
| start | — | — | 0 |
| 1 | 0 | 4 | 4 |
| 2 | 1 | 2 | 6 |
| 3 | 2 | 8 | 14 |
| 4 | 3 | 6 | 20 |

```python
nums = [4, 2, 8, 6]
total = 0
for i in range(len(nums)):
    total = total + nums[i]
print(total)   # 20
```

**35–50 min: Independent Practice — Worksheet (Session 19)**
Students work through Parts 1–3 of the worksheet at their own pace. Teacher circulates, checking especially that students:
- Type the brackets correctly (square `[ ]`, not curly `{ }`).
- Understand that `nums[6]` on a 6-element list is an **IndexError**.
- Use `len()` rather than hard-coding the size.

**50–55 min: Sharing & Discussion**
Two volunteers share their "favourites" list and read aloud one negative-index access. Class predicts the output before it is run. Briefly discuss: *"What kinds of real data are 'a list of the same kind of thing'?"* (Class register, high scores, shopping cart, song queue, sensor readings.)

**55–60 min: Closure & Preview**
Recap the **3 things you can always do to a list**: index it, slice it, loop over it. Preview Session 20: *"Tomorrow we'll learn how to **grow, shrink, and reorder** a list using its built-in methods — and meet the `in` operator that powers `if 'apple' in fruits:`."*

##### Differentiation
**Support:**
- Provide a printed "List Cheat Sheet" with `nums[0]`, `nums[-1]`, `nums[1:3]`, `len(nums)` annotated with diagrams.
- Pair with a stronger peer for the slicing puzzles.
- For Pattern B iteration, allow them to first write Pattern A, then convert.

**Extension:**
- Challenge: write a single line that prints the **middle** element of any odd-length list (`nums[len(nums)//2]`).
- Explore the `step` argument in slicing: `nums[::2]` (every second item), `nums[::-1]` (reversed) — preview of Session 20.
- Research and explain: *"Why does Python start counting at 0?"*

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **List creation** | Cannot create a list literal without help | Creates a list but with syntax errors (e.g. `()` or missing commas) | Creates a correct homogeneous list of 5+ items | Creates lists confidently and chooses appropriate item type/order |
| **Indexing & slicing** | Confuses index 1 with "first item" | Positive indexing OK; negative or slicing causes errors | Both positive/negative indices and basic slices correct | Uses slicing fluently incl. open-ended `[2:]`, `[:3]`, `[-2:]` |
| **Iteration patterns** | Cannot loop over a list | Uses `for x in list` only; cannot access index | Uses both patterns; chooses correctly when prompted | Justifies independently which pattern fits the task |
| **Mutability concept** | Believes strings can be modified by index | Knows lists change but is unsure about strings | Articulates "lists mutable, strings immutable" with examples | Connects mutability to memory/identity and predicts errors before running |

##### Teacher Notes
- The `[]` vs `()` vs `{}` confusion is the **single most common bug** at this stage. Make it a class chant: "**S**quare brackets for lists, **R**ound for tuples, **C**urly for dictionaries" — they will meet all three this unit.
- Some learners arriving from Scratch expect indexing to start at **1**. Address it head-on: "Computers count from zero. Get used to it — it shows up in every language you'll ever use."
- Avoid showing list comprehensions today. They are powerful but distracting; brief mention belongs in Session 20.
- Watch for off-by-one when using `range(len(nums))` — students sometimes write `range(len(nums)+1)`.
- If a student finishes very fast, push them to write a function `def average(nums): ...` — this previews unit 5 and locks in iteration.

---

#### SESSION 19 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Indexing & Slicing Puzzles

Given the list:
```python
animals = ["cat", "dog", "fox", "owl", "bee", "ant"]
```
Write the **value** that each expression produces. If it would cause an error, write **ERROR**.

| # | Expression | Predicted output |
|---|------------|------------------|
| 1 | `animals[0]` | __________________ |
| 2 | `animals[3]` | __________________ |
| 3 | `animals[-1]` | __________________ |
| 4 | `animals[-3]` | __________________ |
| 5 | `animals[6]` | __________________ |
| 6 | `len(animals)` | __________________ |
| 7 | `animals[1:4]` | __________________ |
| 8 | `animals[:2]` | __________________ |
| 9 | `animals[3:]` | __________________ |
| 10 | `animals[-2:]` | __________________ |

**Now check** in Thonny by typing the list and each expression into the shell. Circle any answer you got wrong and write the correct answer beside it.

---

##### Part 2: List Tracing — Complete the Trace Table

Trace this program step by step. Fill in the table.
```python
scores = [50, 70, 60, 90, 80]
total = 0
for i in range(len(scores)):
    total = total + scores[i]
average = total / len(scores)
print(average)
```

| Iteration | i | scores[i] | total (after this line) |
|-----------|---|-----------|-------------------------|
| start | — | — | 0 |
| 1 | 0 | _____ | _____ |
| 2 | 1 | _____ | _____ |
| 3 | 2 | _____ | _____ |
| 4 | 3 | _____ | _____ |
| 5 | 4 | _____ | _____ |

After the loop:
- `total` = ________
- `len(scores)` = ________
- **Final printed value of `average`** = ________

---

##### Part 3: Build Your "Favourites" List

Open Thonny, create a new file called `favourites.py`, and write a program that:

1. Stores **at least 5** of your favourite foods in a list called `favs`.
2. Prints the **first** and **last** item using both **positive** and **negative** indexing.
3. Prints the **total number** of favourites using `len()`.
4. Uses a **`for x in favs:`** loop to print each favourite on its own line, prefixed with `"I love"`.
5. Uses a **`for i in range(len(favs)):`** loop to print each favourite as `1. apple`, `2. banana`, …  
   *(Hint: `print(i + 1, favs[i])` — why `i + 1` and not `i`?)*
6. Changes your **second favourite** (index 1) to something else, then prints the updated list.

Paste your finished code below or attach a printout:
```
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
```

**Mutability mini-experiment.** Try these two snippets in the Thonny shell. Write what happens:

```python
nums = [1, 2, 3]
nums[0] = 99
print(nums)
```
Output: ___________________________________________

```python
word = "cat"
word[0] = "b"
print(word)
```
Output: ___________________________________________

Why are these different? ___________________________________________________________________
______________________________________________________________________________________

---

##### Reflection
1. Before today, if you wanted to store 10 names, how would you have done it? What is the **biggest advantage** of using a list?
   ______________________________________________________________________________________
2. Explain in your own words the difference between `nums[2]` and `nums[-2]`.
   ______________________________________________________________________________________
3. Which iteration pattern do you prefer right now — `for x in nums` or `for i in range(len(nums))`? Why?
   ______________________________________________________________________________________

##### Bonus / Stretch Challenge
Write a single program that:
- Asks the user for **5 numbers** (one at a time) and stores them in a list.
- Prints them back in the **reverse order they were entered**, using slicing.
- Prints the **largest** and **smallest** without using `max()` or `min()` (loop and compare!).

```python
# Your code here
__________________________________________________________
__________________________________________________________
__________________________________________________________
```

---

### Session 20: List Methods & Iteration

---

#### SESSION 20 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 20 of 48 |
| **Title** | List Methods, the `in` Operator & the Accumulator Pattern |
| **Unit** | Unit 4: Lists & Standard Algorithms |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — array operations (insert, delete, find); 0860 — manipulating sequences |
| **Singapore Alignment** | O-Level 7155 Module 4 — list manipulation; membership testing; building lists |

##### Learning Objectives (SMART)
By the end of this session, learners will be able to:
1. **Use** the seven core list methods — `.append()`, `.insert()`, `.remove()`, `.pop()`, `.sort()`, `.reverse()`, `.index()` (and `.count()`) — and **predict** the result of each on a given list with **6/7 correctness**.
2. **Test membership** with the `in` operator and use it inside an `if`-statement to make a real decision.
3. **Build a list dynamically** inside a loop using the **accumulator pattern** (start with `[]`, then `.append()` each iteration).
4. **Distinguish** methods that **modify in place** (return `None`) from methods that **return a value**, avoiding the classic `nums = nums.sort()` bug.

##### Materials Needed
- Thonny IDE.
- Printed worksheet (Session 20).
- "List of Methods" reference card (one per student) — see Teacher Notes for layout.
- Whiteboard for the live "build the list" exercise.

##### Procedure

**0–5 min: Warm-Up — Recall Quiz**
Whiteboard the list `nums = [3, 1, 4]`. Three quickfire questions: *(a) What is `nums[0]`? (b) What is `nums[-1]`? (c) What is `len(nums)`?* Then ask the kicker: *"How would I add the number 5 to this list?"* Some will say `nums[3] = 5` — try it live (it errors, IndexError) — and pivot: *"That's because the list only has slots 0, 1, 2. Today we learn how to grow it."*

**5–15 min: Introduction — The Big Seven**
Show each method on the projector with a fresh `nums = [3, 1, 4]` each time so outputs are predictable.

```python
# 1. .append(x) — add to the END
nums = [3, 1, 4]
nums.append(5)
print(nums)        # [3, 1, 4, 5]

# 2. .insert(i, x) — add at position i, shifting others right
nums = [3, 1, 4]
nums.insert(1, 99)
print(nums)        # [3, 99, 1, 4]

# 3. .remove(x) — remove the FIRST occurrence of value x
nums = [3, 1, 4, 1]
nums.remove(1)
print(nums)        # [3, 4, 1]   <- only the first 1 left!

# 4. .pop() — remove & RETURN the last item; .pop(i) for position i
nums = [3, 1, 4]
last = nums.pop()
print(last, nums)  # 4 [3, 1]

# 5. .sort() — sort in PLACE, ascending
nums = [3, 1, 4, 1, 5, 9, 2]
nums.sort()
print(nums)        # [1, 1, 2, 3, 4, 5, 9]

# 6. .reverse() — reverse in PLACE
nums = [1, 2, 3]
nums.reverse()
print(nums)        # [3, 2, 1]

# 7. .index(x) — find the position of the first x
fruits = ["apple", "banana", "cherry"]
print(fruits.index("banana"))   # 1
```

**Critical pitfall — write this on the board in red:**
```python
nums = [3, 1, 4]
nums = nums.sort()    # WRONG! .sort() returns None
print(nums)           # None  -- you just deleted your list!
```
*"Methods that change a list in place return `None`. Don't assign their result back."*

**15–35 min: Guided Practice — `in`, `count`, and the Accumulator Pattern**

(1) **The `in` operator.** Reads exactly like English:
```python
fruits = ["apple", "banana", "cherry"]
if "apple" in fruits:
    print("We have apples!")
if "mango" not in fruits:
    print("Sorry, no mangoes today.")
```
Pair this with `.count()`:
```python
votes = ["yes", "no", "yes", "yes", "no"]
print(votes.count("yes"))   # 3
print(votes.count("maybe")) # 0  <- never errors, just zero
```

(2) **Predict-the-output round** (whiteboard, students vote A/B/C):
```python
items = [10, 20, 30]
items.append(40)
items.insert(0, 5)
items.remove(20)
print(items)
```
*Expected: `[5, 10, 30, 40]`. Walk through each step on a drawn list-diagram.*

(3) **The Accumulator Pattern — start empty, grow inside the loop.** This is **the** technique for the rest of the course.
```python
# Goal: collect all even numbers from 1 to 20
evens = []                   # 1. Start empty
for n in range(1, 21):       # 2. Loop
    if n % 2 == 0:
        evens.append(n)      # 3. Add when condition is met
print(evens)                 # [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```
Read this aloud as a 3-step recipe: **start empty → loop → grow when needed**. Reinforce with a second example — collecting user input:
```python
names = []
for i in range(3):
    name = input(f"Enter name {i + 1}: ")
    names.append(name)
print("You entered:", names)
```

(4) **Brief mention** (do **not** dwell): list comprehensions are a one-liner shortcut for the accumulator pattern.
```python
evens = [n for n in range(1, 21) if n % 2 == 0]   # same result as above
```
*"You'll see this in older code — for now, write the long form. We want to **see** every step."*

**35–50 min: Independent Practice — Worksheet (Session 20)**
Students attempt all three Parts. The teacher's spot-check focus is the **accumulator pattern** (Part 3) — every student should produce a working `evens = []` / `for` / `.append()` solution before leaving.

**50–55 min: Sharing & Discussion**
Two students share their accumulator solutions to "collect every word longer than 4 letters". Class compares: did anyone use `len(word) > 4` vs `>= 5`? Both work — discuss. Then a quick poll: *"Which method did you forget the most today?"*

**55–60 min: Closure & Preview**
Recap the **two big ideas**: (a) lists have **methods** that change them, and (b) the **accumulator pattern** lets us *build* a list. Preview Session 21: *"Now that we can build and grow lists, the next question is — **how do we find a value inside one**? We meet our first **standard algorithm**: linear search."*

##### Differentiation
**Support:**
- Hand out the "Method Cheat Card" colour-coded by **return type** (red = returns `None`, green = returns a value).
- Provide skeleton code for Part 3 with `evens = []` and the loop header pre-written.
- Allow them to use `print(nums)` after every method call to "see" the change.

**Extension:**
- Use the accumulator pattern to build a list of all 3-digit numbers divisible by **both** 7 and 13.
- Implement your own `my_count(lst, target)` function without using `.count()` — preview of Session 21's linear search.
- Explore `list.copy()` and explain why `b = a` and `b = a.copy()` behave differently when `a` is then mutated.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Method usage** | Confuses methods; misuses syntax | Uses `.append()` only | Uses 5+ methods correctly with right arguments | Chooses the optimal method unprompted; explains return value |
| **`in` operator** | Does not use; writes manual loops | Uses `in` only in simple equality | Uses `in` and `not in` inside `if` to drive a decision | Combines `in` with `.count()` / loops for richer logic |
| **Accumulator pattern** | Cannot build a list inside a loop | Builds list but with one structural error (e.g. resets inside loop) | Correct three-step pattern: empty → loop → append | Adapts the pattern to filter, transform, and collect from input |
| **In-place vs return** | Confused by `None` results | Notices errors only when prompted | States the rule and avoids `nums = nums.sort()` | Predicts return type for any method before running |

##### Teacher Notes
- The "Method Cheat Card" should be one A5 sheet: left column **method name**, middle **example**, right **return value (None? new list? value?)**. Laminate if possible.
- The **`nums = nums.sort()` bug** is so common it deserves a name. We call it "the None trap." Mention it at least three times.
- Some students write `nums.append(1, 2, 3)` expecting it to add three things. `.append()` takes **one** argument; `.extend([1,2,3])` is the multi-add — only mention if asked.
- The accumulator pattern returns in **Sessions 21, 22, 24** and across the rest of the course. Lock it in today.
- For Part 1 of the worksheet, students sometimes execute methods in the *wrong order* and get confused. Stress: **rows are sequential — each row's "before" is the previous row's "after".**

---

#### SESSION 20 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Predict After Each Method

The list **starts** at `nums = [4, 2, 6]` for **row 1** only. Each subsequent row continues from the previous row's result.

| Row | Operation | List **after** the operation |
|-----|-----------|------------------------------|
| 1 | `nums.append(8)` | _____________________________ |
| 2 | `nums.insert(0, 1)` | _____________________________ |
| 3 | `nums.remove(2)` | _____________________________ |
| 4 | `last = nums.pop()` &nbsp;&nbsp;**(also write what `last` equals!)** | nums = ______ &nbsp;last = ______ |
| 5 | `nums.sort()` | _____________________________ |
| 6 | `nums.reverse()` | _____________________________ |
| 7 | `pos = nums.index(6)` &nbsp;**(write `pos`!)** | nums = ______ &nbsp;pos = ______ |

Now type the steps in Thonny one at a time and verify. Circle any prediction you missed.

---

##### Part 2: The `in` Operator and Counting

Given:
```python
words = ["sun", "moon", "star", "sun", "cloud", "sun"]
```
Predict the output of each:

| # | Code | Predicted output |
|---|------|------------------|
| 1 | `print("sun" in words)` | __________________ |
| 2 | `print("rain" in words)` | __________________ |
| 3 | `print("rain" not in words)` | __________________ |
| 4 | `print(words.count("sun"))` | __________________ |
| 5 | `print(words.count("rain"))` | __________________ |
| 6 | `print(words.index("star"))` | __________________ |

Now write a complete program that:
- Takes a word from the user with `input()`.
- Prints `"YES, found N times"` if the word is in `words`, where `N` is its count.
- Prints `"NO, not in the list"` otherwise.

```python
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
```

---

##### Part 3: Build the List — Accumulator Pattern

(a) Write a program that builds a list of all **multiples of 3** from 1 to 30 and prints it. Use the accumulator pattern.
```python
multiples = ___
for n in range(__, __):
    if ____________:
        ______________
print(multiples)
```
**Expected output:** `[3, 6, 9, 12, 15, 18, 21, 24, 27, 30]`

(b) Ask the user for **5 words** in a loop and store them in a list. Then print:
- The list itself.
- How many words start with the letter `'s'` (use `word.startswith("s")`).
- The longest word (loop and compare with `len()`).
```python
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
```

(c) **Filter into a new list.** Given:
```python
ages = [12, 7, 15, 9, 20, 11, 14]
```
Build a new list `teens` that contains only the ages **between 10 and 19 inclusive**. Print it.
```python
__________________________________________________________
__________________________________________________________
__________________________________________________________
```
**Expected:** `[12, 15, 11, 14]`

---

##### Reflection
1. What does `nums.sort()` *return*? Why is `nums = nums.sort()` a bug?
   ______________________________________________________________________________________
2. Describe the **3 steps** of the accumulator pattern in your own words.
   ______________________________________________________________________________________
3. Pick one method from today (`append`, `insert`, `remove`, `pop`, `sort`, `reverse`, `index`). Where in a real app (game, chat, school system) would you use it?
   ______________________________________________________________________________________

##### Bonus / Stretch Challenge
Write a function-free script that:
- Generates a list of 20 random integers between 1 and 50 using `random.randint` and the accumulator pattern.
- Prints the original list.
- Prints a **second** list containing only the **even** numbers from the first.
- Prints the **sorted** version of the even list, then the **reversed** version.
- Prints the **count** of how many even numbers there were.

```python
import random
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
```

---

### Session 21: Linear Search Algorithm

---

#### SESSION 21 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 21 of 48 |
| **Title** | Linear Search — The First Standard Algorithm |
| **Unit** | Unit 4: Lists & Standard Algorithms |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — **standard algorithm: linear search**; pseudocode style |
| **Singapore Alignment** | O-Level 7155 Module 4 — searching algorithm; algorithm efficiency for unsorted data |

##### Learning Objectives (SMART)
By the end of this session, learners will be able to:
1. **State** the linear-search problem in their own words and **read** Cambridge IGCSE-style pseudocode for the algorithm.
2. **Implement** linear search in Python in **two ways** — with a `found` flag and `while` loop, and with `for` + `break` — and explain when each style is preferable.
3. **Choose** between returning the **index** of a found item and returning a **True/False** result, depending on the caller's need.
4. **Trace** the execution of a linear search on a 6-element list and produce a complete trace table for both a successful and an unsuccessful search.

##### Materials Needed
- Thonny IDE.
- Printed worksheet (Session 21).
- Cambridge IGCSE pseudocode reference card (highlight `WHILE … ENDWHILE`, `FOR … NEXT`, `IF … THEN … ENDIF`, `OUTPUT`).
- 8 paper "library books" labelled with titles, plus a "request slip" — for the warm-up.
- Whiteboard for the trace table.

##### Procedure

**0–5 min: Warm-Up — "Find the Book" Game**
Lay 8 paper "books" face-down in a row on the table. Ask: *"I want **'Harry Potter'** — find it. But you can only flip books one at a time, **left to right**, and you must stop when you find it (or when you've checked them all)."* A volunteer plays. The class counts the flips. Run it twice — once with the target near the front, once near the back. Ask: *"Best case? Worst case?"* This **is** linear search.

**5–15 min: Introduction — The Problem and the Pseudocode**

State the problem on the board:
> **Given a list and a target value, decide whether the target is in the list — and if so, where.**

Show the **Cambridge IGCSE-style pseudocode** (this style is examinable):

```
// Linear Search — IGCSE 0478 pseudocode
DECLARE Found : BOOLEAN
DECLARE Position : INTEGER
DECLARE i : INTEGER

Found  Position  -1
i  0

WHILE (i < Length) AND (Found = FALSE)
    IF Items[i] = Target THEN
        Found  TRUE
        Position  i
    ELSE
        i  i + 1
    ENDIF
ENDWHILE

IF Found = TRUE THEN
    OUTPUT "Found at position ", Position
ELSE
    OUTPUT "Not in the list"
ENDIF
```

Walk through it line-by-line, decoding `←` as "becomes" and `=` as "equals" (comparison). Emphasise: **we exit the loop the moment we find it** — we don't keep searching.

**15–35 min: Guided Practice — Two Python Implementations**

(1) **Translation #1: `while` loop with a `found` flag** (closest to the pseudocode):
```python
def linear_search_while(items, target):
    found = False
    position = -1
    i = 0
    while i < len(items) and not found:
        if items[i] == target:
            found = True
            position = i
        else:
            i = i + 1
    return position    # -1 means "not found"

books = ["Matilda", "Holes", "Wonder", "Coraline", "Hatchet"]
print(linear_search_while(books, "Wonder"))    # 2
print(linear_search_while(books, "Dune"))      # -1
```

(2) **Translation #2: `for` loop with `break`** (more Pythonic, shorter):
```python
def linear_search_for(items, target):
    for i in range(len(items)):
        if items[i] == target:
            return i        # exit immediately on match
    return -1               # only reached if never found

print(linear_search_for(["red", "green", "blue"], "blue"))   # 2
print(linear_search_for(["red", "green", "blue"], "pink"))   # -1
```

Compare side by side. Both are **correct linear search**. The `for`+`break` version is shorter; the `while`+flag version more directly mirrors the IGCSE pseudocode (which is what students must **read** in exams).

(3) **Index vs True/False — choose what fits the caller.** Sometimes you need the *position* (to update or display); other times you only need *yes/no*:
```python
# Returns True/False
def contains(items, target):
    for x in items:
        if x == target:
            return True
    return False

print(contains([1, 2, 3], 2))   # True
print(contains([1, 2, 3], 5))   # False

# Note: Python already gives us this via the `in` operator!
print(2 in [1, 2, 3])           # True
```
**Big picture:** Python's `in` operator and `.index()` method *are* linear search under the hood — but the IGCSE syllabus expects you to be able to **write it yourself**, in pseudocode and in code.

(4) **Trace table — live on the whiteboard.** Search for `7` in `[3, 8, 7, 2, 5]`:

| Step | i | items[i] | items[i] = 7? | found | position |
|------|---|----------|---------------|-------|----------|
| start | 0 | — | — | False | -1 |
| 1 | 0 | 3 | No | False | -1 |
| 2 | 1 | 8 | No | False | -1 |
| 3 | 2 | 7 | **YES** | **True** | **2** |
| exit | — | — | — | True | 2 |

Now repeat for **target = 99** — students complete the table on their copies. Notice we visit **all 5** elements before declaring "not found" — this is the **worst case** for linear search (`O(n)` comparisons).

(5) **A buggy search** — students hunt the bug:
```python
# Bug! Why does this always say "not found" for the last element?
def buggy_search(items, target):
    for i in range(len(items) - 1):     # <-- BUG: -1 cuts off the last index
        if items[i] == target:
            return i
    return -1

print(buggy_search([10, 20, 30], 30))    # prints -1, but 30 IS there!
```
Discuss the **off-by-one** — the most famous bug in computing. Fix: `range(len(items))`.

**35–50 min: Independent Practice — Worksheet (Session 21)**

**50–55 min: Sharing & Discussion**
One pair shares their pseudocode-to-Python translation; another shares their trace table for the unsuccessful search. Discussion prompt: *"Imagine searching the school library catalogue (1 million books). Linear search would check up to 1 million entries. Is that OK? When is it OK, when is it not?"* (Foreshadow binary search, taught in IGCSE later.)

**55–60 min: Closure & Preview**
Recap the **two implementations** and the **two return styles**. Preview Session 22: *"If linear search **finds** an item in any list, **bubble sort** **arranges** the list. Tomorrow we write our second standard algorithm."*

##### Differentiation
**Support:**
- Provide the pseudocode side by side with a half-complete Python translation (blanks for `==`, `i + 1`, `return`).
- Hand-trace one search together at the desk before they tackle the worksheet trace.
- Allow the simpler `for` + `break` version only; defer the `while` version.

**Extension:**
- Implement linear search that returns **all** indices where the target appears (use the accumulator pattern from Session 20).
- Modify the search to be **case-insensitive** for strings.
- Research and explain in 2 sentences: *"What is binary search and why does it require sorted data?"*

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Algorithm understanding** | Cannot describe linear search | States "it looks through the list" but no halt condition | Articulates loop + early exit + not-found case | Explains worst/best case and where it fits in the bigger algorithm picture |
| **Pseudocode → Python** | Translation incorrect or incomplete | One-of-two implementations works | Both implementations work and produce correct output | Adapts implementation for new requirements (all matches, case-insensitive) |
| **Trace table** | Cannot complete trace | Trace partially correct (one variable wrong) | Both successful and unsuccessful trace complete and correct | Trace clean, explains every transition |
| **Return-value design** | Returns the wrong type or no value | Hard-codes one style | Chooses index vs True/False appropriately | Justifies the choice and uses `-1` as a sentinel correctly |

##### Teacher Notes
- The IGCSE pseudocode operator `←` is unfamiliar — write it as `<-` on the board if your projector font lacks the arrow.
- Students often write `return -1` **inside** the loop, which exits on the first non-match. Catch this early — `return -1` belongs **after** the loop.
- The `while … and not found` pattern requires comfort with **boolean operators** from Unit 2. Briefly recap if shaky.
- A common shortcut students try: `return items.index(target)`. Acknowledge it works, then say: *"That **is** linear search — but the syllabus wants **you** to write it. We'll use `.index()` happily after the exam."*
- The off-by-one bug in `buggy_search` is examinable in IGCSE Paper 2. Make it stick: chant "**range(len)** — no minus one!"

---

#### SESSION 21 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Pseudocode → Python Translation

Below is the IGCSE-style pseudocode for linear search. Fill in the blanks of the Python translation **exactly mirroring the pseudocode**.

**Pseudocode:**
```
Found  FALSE
Position  -1
i  0
WHILE (i < Length) AND (Found = FALSE)
    IF Items[i] = Target THEN
        Found  TRUE
        Position  i
    ELSE
        i  i + 1
    ENDIF
ENDWHILE
OUTPUT Position
```

**Python translation — fill the 8 blanks:**
```python
def linear_search(items, target):
    found = ________            # (1)
    position = ________         # (2)
    i = ________                # (3)
    while i < ________ and not found:    # (4)
        if items[i] ________ target:     # (5)
            found = ________             # (6)
            position = ________          # (7)
        else:
            i = ________                  # (8)
    return position
```

Test by running:
```python
print(linear_search([10, 30, 20, 40], 20))   # should print: 2
print(linear_search([10, 30, 20, 40], 99))   # should print: -1
```

---

##### Part 2: Trace Tables

**(a) Successful search** — `items = [5, 8, 2, 9, 1, 7]`, `target = 9`

| Step | i | items[i] | items[i] = target? | found | position |
|------|---|----------|---------------------|-------|----------|
| start | 0 | — | — | False | -1 |
| 1 | 0 | _____ | _____ | _____ | _____ |
| 2 | 1 | _____ | _____ | _____ | _____ |
| 3 | 2 | _____ | _____ | _____ | _____ |
| 4 | 3 | _____ | _____ | _____ | _____ |
| exit | — | — | — | _____ | _____ |

**Final returned value:** ________

**(b) Unsuccessful search** — same list, `target = 100`

| Step | i | items[i] | items[i] = target? | found | position |
|------|---|----------|---------------------|-------|----------|
| start | 0 | — | — | False | -1 |
| 1 | 0 | _____ | _____ | _____ | _____ |
| 2 | 1 | _____ | _____ | _____ | _____ |
| 3 | 2 | _____ | _____ | _____ | _____ |
| 4 | 3 | _____ | _____ | _____ | _____ |
| 5 | 4 | _____ | _____ | _____ | _____ |
| 6 | 5 | _____ | _____ | _____ | _____ |
| exit | — | — | — | _____ | _____ |

**Final returned value:** ________

**Comparison question:** How many comparisons did the **successful** search make? ___ The **unsuccessful** search? ___ Which is the **worst case**? ___________________________

---

##### Part 3: Find the Bug!

Each of the three functions below is supposed to be a linear search but has **one bug**. Identify the bug, describe it in words, and rewrite the corrected line.

**Bug 1:**
```python
def search1(items, target):
    for i in range(len(items) - 1):   # <-- problem here?
        if items[i] == target:
            return i
    return -1
```
What's wrong? __________________________________________________________________
Corrected line: __________________________________________________________________

**Bug 2:**
```python
def search2(items, target):
    for i in range(len(items)):
        if items[i] == target:
            return i
        return -1                      # <-- problem here?
```
What's wrong? __________________________________________________________________
Corrected line: __________________________________________________________________

**Bug 3:**
```python
def search3(items, target):
    for i in range(len(items)):
        if items[i] = target:           # <-- problem here?
            return i
    return -1
```
What's wrong? __________________________________________________________________
Corrected line: __________________________________________________________________

---

##### Reflection
1. In your own words, describe linear search **in one sentence**.
   ______________________________________________________________________________________
2. When would you prefer the `while` + `found` flag implementation over the `for` + `break` one?
   ______________________________________________________________________________________
3. The library has 1,000,000 books. With linear search, what is the **maximum** number of comparisons to find one book? Is that fast enough?
   ______________________________________________________________________________________

##### Bonus / Stretch Challenge
Write a function `find_all(items, target)` that returns a **list of every index** at which `target` appears in `items`. Use the accumulator pattern from Session 20.

```python
def find_all(items, target):
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________

# Tests
print(find_all([1, 2, 3, 2, 1, 2], 2))   # [1, 3, 5]
print(find_all([1, 2, 3], 9))            # []
```

---

### Session 22: Bubble Sort Algorithm

---

#### SESSION 22 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 22 of 48 |
| **Title** | Bubble Sort — The Second Standard Algorithm |
| **Unit** | Unit 4: Lists & Standard Algorithms |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — **standard algorithm: bubble sort**; nested loops; swap operation |
| **Singapore Alignment** | O-Level 7155 Module 4 — sorting algorithm; built-in sort vs hand-coded |

##### Learning Objectives (SMART)
By the end of this session, learners will be able to:
1. **Describe** the bubble-sort idea ("compare neighbours, swap if out of order, repeat") and **read** Cambridge IGCSE-style pseudocode.
2. **Implement** bubble sort in Python with **two nested loops** and a **tuple-swap**, then **optimise** it with a `swapped` flag for early exit.
3. **Trace** a complete bubble-sort run on a 5-element list across all passes, recording every comparison and swap in a trace table.
4. **Decide** when to **write your own** sort algorithm versus **use Python's built-in** `sorted()` / `list.sort()`, justifying the choice in one sentence.

##### Materials Needed
- Thonny IDE.
- Printed worksheet (Session 22).
- Six pieces of A5 card numbered with random integers — for the human bubble-sort demo.
- Whiteboard with a 5-column blank trace table pre-drawn.

##### Procedure

**0–5 min: Warm-Up — "Human Bubble Sort"**
Five volunteers stand at the front, each holding a number card (e.g. `5, 2, 8, 1, 4`). Rule: *"You may only swap with the person directly to your right, and only if your number is bigger than theirs."* The class calls "compare!" and "swap!" left-to-right, pass after pass, until no swaps happen. The numbers naturally **bubble** into order — and the largest "rises" to the right after each pass. *That's bubble sort.*

**5–15 min: Introduction — Pseudocode and the Idea**

The problem:
> **Given a list, rearrange its items into ascending order — using only neighbour-comparisons and swaps.**

**Cambridge IGCSE-style pseudocode** (study this carefully — it appears on exams):
```
// Bubble Sort — IGCSE 0478 pseudocode
DECLARE i, j, Temp : INTEGER
DECLARE Items : ARRAY[0:Length-1] OF INTEGER

FOR i  0 TO Length - 2
    FOR j  0 TO Length - 2 - i
        IF Items[j] > Items[j + 1] THEN
            Temp  Items[j]
            Items[j]  Items[j + 1]
            Items[j + 1]  Temp
        ENDIF
    NEXT j
NEXT i
```

Decode the **two loops**:
- **Outer (`i`)** — counts the *passes*. After pass `i`, the largest `i+1` items are in place at the end.
- **Inner (`j`)** — walks neighbour pairs from left, stopping a bit earlier each pass (the right side is already sorted).

The body's **3-line swap** uses a temporary variable `Temp` — Python will let us shorten this to one line.

**15–35 min: Guided Practice — Code, Optimise, Compare**

(1) **Direct translation to Python:**
```python
def bubble_sort(items):
    n = len(items)
    for i in range(n - 1):
        for j in range(n - 1 - i):
            if items[j] > items[j + 1]:
                # Python's tuple-swap — one line, no temp variable
                items[j], items[j + 1] = items[j + 1], items[j]
    return items

nums = [5, 2, 8, 1, 4]
print(bubble_sort(nums))    # [1, 2, 4, 5, 8]
```

Highlight the **tuple-swap**:
```python
a, b = b, a    # swaps the values of a and b in one line
```
Compare to the long-hand 3-line swap with `temp` — show students both work, but the tuple-swap is cleaner.

(2) **Live trace table — `nums = [5, 2, 8, 1, 4]`, first two passes**:

**Pass i = 0** (compare neighbours, j = 0..3):

| j | items[j] | items[j+1] | Swap? | List after |
|---|----------|------------|-------|------------|
| 0 | 5 | 2 | YES | [2, 5, 8, 1, 4] |
| 1 | 5 | 8 | no  | [2, 5, 8, 1, 4] |
| 2 | 8 | 1 | YES | [2, 5, 1, 8, 4] |
| 3 | 8 | 4 | YES | [2, 5, 1, 4, 8] |

**Largest item `8` is now in its final position.** Inner loop next time stops at `j = 2`.

**Pass i = 1** (j = 0..2):

| j | items[j] | items[j+1] | Swap? | List after |
|---|----------|------------|-------|------------|
| 0 | 2 | 5 | no  | [2, 5, 1, 4, 8] |
| 1 | 5 | 1 | YES | [2, 1, 5, 4, 8] |
| 2 | 5 | 4 | YES | [2, 1, 4, 5, 8] |

After pass 2, the **two** largest are placed. Students continue passes 3 and 4 in the worksheet.

(3) **The optimisation — a `swapped` flag:** if a whole pass makes no swaps, the list is sorted; we can stop early.
```python
def bubble_sort_optimised(items):
    n = len(items)
    for i in range(n - 1):
        swapped = False
        for j in range(n - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
                swapped = True
        if not swapped:
            break        # already sorted — stop early
    return items

print(bubble_sort_optimised([1, 2, 3, 4, 5]))    # already sorted -> 1 pass!
```
Best case (already sorted) is now `O(n)` instead of `O(n²)`. *"Why is this a good idea? Imagine sorting the class register that's already alphabetical."*

(4) **Built-in vs hand-written:** Python's built-ins use **Timsort** (very fast). Compare:
```python
nums = [5, 2, 8, 1, 4]

# Sort in place — modifies nums, returns None
nums.sort()
print(nums)               # [1, 2, 4, 5, 8]

# Returns a NEW sorted list, leaves original alone
nums = [5, 2, 8, 1, 4]
result = sorted(nums)
print(result)             # [1, 2, 4, 5, 8]
print(nums)               # [5, 2, 8, 1, 4]   <- unchanged

# Descending
print(sorted(nums, reverse=True))   # [8, 5, 4, 2, 1]
```
**Rule of thumb:** in **real code**, use `sorted()` / `.sort()`. In **exams** and to **understand the algorithm**, write bubble sort. Both matter.

**35–50 min: Independent Practice — Worksheet (Session 22)**
Students complete the trace table, the from-pseudocode implementation, and the swap/no-swap quiz. Teacher prioritises checking the trace table — common errors are forgetting the inner loop's shrinking upper bound and miscounting `j`.

**50–55 min: Sharing & Discussion**
Volunteer reads pass-3 of the trace; another reads pass-4. Quick poll: *"Whose list was sorted **before** the last pass?"* Discuss why the `swapped` flag would have helped.

**55–60 min: Closure & Preview**
Recap: *"You now know **two standard algorithms** — linear search (find) and bubble sort (arrange). They appear in every exam paper this course is aligned to."* Preview Session 23: *"We've stored values in lists. What if we want to store **a name with an age**, **a question with an answer**? Tomorrow we meet **tuples and dictionaries** — the building blocks of records and tables."*

##### Differentiation
**Support:**
- Provide a printed pre-drawn 5-column trace table for every pass.
- Use the human-sort cards on a desk in pairs to physically run the algorithm.
- Allow them to skip the `swapped` flag optimisation.

**Extension:**
- Modify bubble sort to sort **descending** without using `reverse`.
- Sort a list of **strings** (`>` works alphabetically) and confirm.
- Count the **number of swaps** the algorithm performs and compare best/worst cases.
- Look up insertion sort, write a 2-sentence summary of how it differs.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Algorithm idea** | Cannot explain bubble sort | States "it sorts" but no mechanism | Articulates compare-neighbours-and-swap; knows passes | Explains why largest "bubbles up" and why inner loop shrinks |
| **Implementation** | Code does not run | Sorts but with extra/missing iteration | Two nested loops + correct swap, sorts correctly | Adds `swapped` optimisation and ascending/descending option |
| **Trace table** | Trace blank or wildly wrong | Pass 1 correct, later passes wrong | All passes correct, swap column accurate | Trace clean, accompanied by short explanation of bounds |
| **When to use built-in** | Always reaches for hand-coded | Uses one or the other arbitrarily | Justifies built-in for real use, hand-coded for learning/exam | Compares time complexity informally and links to Timsort |

##### Teacher Notes
- The **inner loop bound** `n - 1 - i` is the most common bug. Students often write `n - 1`, which still works but is wasteful (re-checks already-sorted tails). Either is **functionally** correct; the `n - 1 - i` form is what IGCSE pseudocode shows and what the mark scheme rewards.
- The **tuple swap** is one of Python's loveliest features. Demo it standalone (`a, b = 1, 2; a, b = b, a`) before embedding in the sort.
- Some students will still write `temp = items[j]; items[j] = items[j+1]; items[j+1] = temp` from pseudocode. Both are accepted — celebrate that they read the pseudocode literally.
- After Session 22 students may say "bubble sort is slow." It **is** — `O(n²)` — but acknowledge they are not yet expected to know other sorts. The IGCSE syllabus only requires bubble sort; the O-Level 7155 mentions it as one example.
- Reserve 2 min at the end for a **whole-class clap** when they finish their first sort algorithm — it's a milestone.

---

#### SESSION 22 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Complete the Trace Table

You will fully trace `bubble_sort` on `items = [4, 1, 7, 3, 2]`. The list has length 5, so there are at most **4 passes** (`i = 0, 1, 2, 3`).

**Pass i = 0**  (j runs 0 → 3)

| j | items[j] | items[j+1] | Swap? | List after this comparison |
|---|----------|------------|-------|----------------------------|
| 0 | _____ | _____ | _____ | __________________________ |
| 1 | _____ | _____ | _____ | __________________________ |
| 2 | _____ | _____ | _____ | __________________________ |
| 3 | _____ | _____ | _____ | __________________________ |

**Pass i = 1**  (j runs 0 → 2)

| j | items[j] | items[j+1] | Swap? | List after this comparison |
|---|----------|------------|-------|----------------------------|
| 0 | _____ | _____ | _____ | __________________________ |
| 1 | _____ | _____ | _____ | __________________________ |
| 2 | _____ | _____ | _____ | __________________________ |

**Pass i = 2**  (j runs 0 → 1)

| j | items[j] | items[j+1] | Swap? | List after this comparison |
|---|----------|------------|-------|----------------------------|
| 0 | _____ | _____ | _____ | __________________________ |
| 1 | _____ | _____ | _____ | __________________________ |

**Pass i = 3**  (j runs 0 → 0)

| j | items[j] | items[j+1] | Swap? | List after this comparison |
|---|----------|------------|-------|----------------------------|
| 0 | _____ | _____ | _____ | __________________________ |

**Final sorted list:** ___________________________

**Question:** After **which pass** did the list first become fully sorted? ____  
If we had used the `swapped` flag, on which pass would the algorithm have stopped early? ____

---

##### Part 2: Implement-from-Pseudocode

Translate this pseudocode to Python. Fill the 7 blanks.

```
FOR i  0 TO Length - 2
    FOR j  0 TO Length - 2 - i
        IF Items[j] > Items[j + 1] THEN
            SWAP Items[j] AND Items[j + 1]
        ENDIF
    NEXT j
NEXT i
```

```python
def bubble_sort(items):
    n = ________                          # (1)
    for i in range(________):             # (2)
        for j in range(________):         # (3)
            if items[j] ________ items[j + 1]:    # (4)
                items[j], ________ = items[j + 1], ________   # (5) (6)
    return ________                       # (7)

# Test
print(bubble_sort([6, 3, 8, 1, 9, 2]))   # expected: [1, 2, 3, 6, 8, 9]
print(bubble_sort([1]))                  # expected: [1]
print(bubble_sort([]))                   # expected: []
```

Now **add** the optimisation — a `swapped` flag and `break`. Rewrite the function below:
```python
def bubble_sort_optimised(items):
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
```

---

##### Part 3: Swap-or-No-Swap Prediction Quiz

For each pair, write **SWAP** or **NO** assuming we are sorting **ascending**.

| # | Comparison | Swap? |
|---|------------|-------|
| 1 | `items[j] = 5`, `items[j+1] = 8` | _____ |
| 2 | `items[j] = 8`, `items[j+1] = 5` | _____ |
| 3 | `items[j] = 3`, `items[j+1] = 3` | _____ |
| 4 | `items[j] = "apple"`, `items[j+1] = "banana"` | _____ |
| 5 | `items[j] = "banana"`, `items[j+1] = "apple"` | _____ |
| 6 | `items[j] = 0`, `items[j+1] = -1` | _____ |
| 7 | `items[j] = 100`, `items[j+1] = 99` | _____ |

---

##### Part 4: Built-in vs Hand-Written

For each scenario, circle the better choice and write a one-line reason.

(a) You are writing **production code** for a banking app that sorts millions of transactions.  
**Built-in `sorted()` / hand-written bubble sort?** Reason: ____________________________________

(b) You are answering an **IGCSE Paper 2** question that asks you to write the algorithm.  
**Built-in `sorted()` / hand-written bubble sort?** Reason: ____________________________________

(c) You are sorting a list of **5 student names** in a classroom demo to **show how sorting works**.  
**Built-in `sorted()` / hand-written bubble sort?** Reason: ____________________________________

---

##### Reflection
1. After each pass of bubble sort, **which item is guaranteed to be in its final position**, and **where**?
   ______________________________________________________________________________________
2. Why does the inner loop stop at `n - 1 - i` instead of `n - 1`?
   ______________________________________________________________________________________
3. The `swapped` flag makes one specific case much faster. Which case, and why?
   ______________________________________________________________________________________

##### Bonus / Stretch Challenge
Modify `bubble_sort` to **count the total number of swaps** it performs. Sort each of these lists and report the swap count:

```python
def bubble_sort_count(items):
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    return items, swap_count

print(bubble_sort_count([1, 2, 3, 4, 5]))         # already sorted: ___ swaps
print(bubble_sort_count([5, 4, 3, 2, 1]))         # reversed: ___ swaps
print(bubble_sort_count([3, 1, 4, 1, 5, 9, 2, 6])) # random: ___ swaps
```
Which case caused the **most** swaps? Which the **fewest**? Does that match the worst/best-case theory?
______________________________________________________________________________________

---

### Session 23: Tuples & Dictionaries

---

#### SESSION 23 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 23 of 48 |
| **Title** | Tuples & Dictionaries — Records and Lookup Tables |
| **Unit** | Unit 4: Lists & Standard Algorithms |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — records and lookup data structures (extension); 0860 — structuring related data |
| **Singapore Alignment** | O-Level 7155 Module 4 — record-style and key-value data structures |

##### Learning Objectives (SMART)
By the end of this session, learners will be able to:
1. **Distinguish** tuples from lists in terms of **mutability** and **typical use** (records, multiple-return), and create both correctly.
2. **Create, access, modify, and iterate** a Python dictionary using `[]`, `.get()`, `.keys()`, `.values()`, and `.items()`.
3. **Predict** when a missing-key access raises **`KeyError`** and choose the **defensive** alternative `.get()`.
4. **Build a "list of dictionaries"** as the natural representation of a small table (rows = dicts, columns = keys) — preparing for Project 4.

##### Materials Needed
- Thonny IDE.
- Printed worksheet (Session 23).
- Sample "phonebook" reference table on the board with rows = people, columns = name/phone/age.
- A real-world dictionary (book) prop — for the warm-up analogy.

##### Procedure

**0–5 min: Warm-Up — "Look it Up"**
Hold up a real dictionary book. Ask: *"To find the meaning of 'algorithm', do you start at page 1 and turn pages until you reach 'A'? No — you jump straight to the **A** section. The book is **organised by key** — the word — and gives you a **value** — the meaning."* Then write on the board:
```
"name"  -> "Aisha"
"age"   -> 12
"grade" -> "8A"
```
*"That's a Python dictionary. We meet it in 30 seconds."*

**5–15 min: Introduction — Tuples First, Then Dictionaries**

(1) **Tuples** — round brackets, comma-separated. Like lists, but **immutable**.
```python
# Tuples — for records / fixed groupings
person = ("Aisha", 12)             # name, age
print(person[0])                   # Aisha
print(person[1])                   # 12

# Mutability test
person[0] = "Bilal"                # TypeError — tuples are IMMUTABLE
```
**Use tuples for:** records (a row), coordinate pairs `(x, y)`, "multiple return" from a function.

```python
def stats(nums):
    return min(nums), max(nums)    # returns a TUPLE of two values

low, high = stats([3, 1, 4, 1, 5, 9])    # tuple-unpacking
print(low, high)    # 1 9
```

(2) **Dictionaries** — curly braces, **key: value** pairs.
```python
student = {"name": "Aisha", "age": 12, "grade": "8A"}

# Access by key — like a list, but the index is a string
print(student["name"])     # Aisha
print(student["age"])      # 12

# Modify or add by key
student["age"] = 13         # change existing
student["club"] = "chess"   # add NEW key
print(student)
# {'name': 'Aisha', 'age': 13, 'grade': '8A', 'club': 'chess'}
```

(3) **The KeyError** — and how `.get()` saves you:
```python
print(student["height"])         # KeyError: 'height'

print(student.get("height"))     # None  — no error!
print(student.get("height", 0))  # 0     — your chosen default
```
*"`.get(key, default)` is your friend. It says: 'try this key; if not there, give me the default'."*

**15–35 min: Guided Practice — Iterating + List of Dicts**

(1) **Three ways to iterate a dict.** Type all three side by side.
```python
student = {"name": "Aisha", "age": 12, "grade": "8A"}

# (a) over keys (default)
for key in student:
    print(key, "->", student[key])

# (b) over values
for value in student.values():
    print(value)

# (c) over (key, value) pairs — the most useful
for key, value in student.items():
    print(f"{key}: {value}")
```
Walkthrough output for each — students predict before you press Run.

(2) **Predict-the-output** (whiteboard):
```python
d = {"a": 1, "b": 2, "c": 3}
print(len(d))
print("a" in d)
print(2 in d)             # tricky — `in` on a dict checks KEYS!
print(d.get("z", -1))
```
*Expected:* `3`, `True`, `False` (because `2` is a value, not a key), `-1`.

(3) **The big idea — list of dictionaries = a table.** This pattern powers Project 4.
```python
students = [
    {"name": "Aisha", "score": 85},
    {"name": "Bilal", "score": 72},
    {"name": "Chen",  "score": 90},
    {"name": "Dewi",  "score": 78},
]

# How would you print the average score?
total = 0
for s in students:
    total = total + s["score"]
average = total / len(students)
print(f"Average: {average}")
```
Read aloud: *"`students` is a list of rows; each row is a dictionary; each dictionary's keys are the columns."*

(4) **Mini trace table — accumulate names of high scorers:**
```python
high_scorers = []
for s in students:
    if s["score"] >= 80:
        high_scorers.append(s["name"])
print(high_scorers)    # ['Aisha', 'Chen']
```
| Iter | s | s["score"] | s["score"] >= 80? | high_scorers |
|------|---|------------|---------------------|--------------|
| 1 | {Aisha, 85} | 85 | True  | ['Aisha'] |
| 2 | {Bilal, 72} | 72 | False | ['Aisha'] |
| 3 | {Chen,  90} | 90 | True  | ['Aisha', 'Chen'] |
| 4 | {Dewi,  78} | 78 | False | ['Aisha', 'Chen'] |

(5) **Convert a list of pairs to a dictionary** (worksheet preview):
```python
pairs = [("apple", 3), ("banana", 5), ("cherry", 7)]
inventory = {}
for fruit, count in pairs:    # tuple-unpack inside the loop
    inventory[fruit] = count
print(inventory)              # {'apple': 3, 'banana': 5, 'cherry': 7}
```

**35–50 min: Independent Practice — Worksheet (Session 23)**
Students complete all four parts. Teacher's spot-check focuses on Part 3 (KeyError handling) and Part 4 (list-of-dicts iteration).

**50–55 min: Sharing & Discussion**
Two volunteers read aloud their **contact-book entry** dictionary. Class checks: are all keys strings? Did they use `.get()` for missing fields? Whole-class question: *"What real-world data is best as a list of dicts? What is best as just a list? Just a dict?"*

**55–60 min: Closure & Preview**
Recap the **three structures** of Unit 4: list (ordered, mutable), tuple (ordered, immutable, record-like), dictionary (key→value lookup). Preview Session 24: *"Tomorrow we apply **everything** — lists, dicts, linear search, bubble sort — to build a **Quiz & Leaderboard App**. Bring your wittiest trivia questions!"*

##### Differentiation
**Support:**
- Provide a printed cheat-card with one example of each: a 3-element list, a 2-element tuple, a 3-key dictionary.
- Pre-fill the `students` list of dicts on the worksheet so they only need to write the loop.
- Allow `student[key]` access only; defer `.get()` to the bonus.

**Extension:**
- Build a function `count_words(text)` that returns a dict mapping each word to its count (the classic "word frequency" exercise).
- Sort a list of dicts by a chosen key using `sorted(students, key=lambda s: s["score"], reverse=True)` — preview of Project 4.
- Research and explain in 2 sentences: *"Why is dictionary lookup so fast — even for a million entries?"*

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Tuple vs list** | Cannot distinguish | States one difference but mis-applies | Knows immutability + typical uses | Chooses correct structure unprompted in new contexts |
| **Dictionary basics** | Cannot create or access | Creates dict; can access existing keys only | Creates, accesses, modifies, adds keys | Uses `.get(default)` defensively; reasons about KeyError |
| **Iteration** | Cannot loop a dict | Loops keys only | Uses `.items()` correctly with unpacking | Combines iteration with accumulator and conditional filtering |
| **List of dicts** | Cannot construct | Constructs but cannot iterate | Builds and reads a 4-row table-like structure | Performs aggregate operations (sum, average, filter) on it |

##### Teacher Notes
- **Single biggest confusion:** that `in` on a dict checks **keys**, not values. Reinforce with the predict-the-output line `print(2 in d)`.
- Some students try `student.name` (Java/JavaScript style). Gently correct — Python dictionaries use `student["name"]`.
- Tuples with **one** element need a trailing comma: `(5,)` not `(5)`. Worth a 30-second mention; otherwise some bonus attempts will silently use the wrong type.
- The `for key, value in d.items():` line is many learners' first **tuple-unpack inside a loop**. Demonstrate it standalone: `for a, b in [(1,2), (3,4)]: print(a, b)`.
- Throughout the lesson, link forward: *"Tomorrow's project quiz uses exactly this — `[{'q': '...', 'a': '...'}, …]`."* The list-of-dicts pattern is the **bridge** to Session 24.

---

#### SESSION 23 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Tuples vs Lists

(a) For each statement, write **TUPLE**, **LIST**, or **BOTH**.

| # | Statement | TUPLE / LIST / BOTH |
|---|-----------|---------------------|
| 1 | Created with square brackets `[ ]` | _____ |
| 2 | Created with round brackets `( )` | _____ |
| 3 | Items are accessed by integer index | _____ |
| 4 | You can change an item by index | _____ |
| 5 | Best for storing a record like (name, age) | _____ |
| 6 | Has a `.append()` method | _____ |
| 7 | Can be looped over with `for x in ...` | _____ |
| 8 | A `(5)` is a tuple of one item | _____ &nbsp;**(careful!)** |

(b) Run this code mentally and write the output:
```python
def min_max(nums):
    return min(nums), max(nums)

low, high = min_max([7, 3, 9, 1, 4])
print(low, high)
```
Output: ____________________________________

What is the **type** of `min_max([7, 3, 9, 1, 4])`? ________

---

##### Part 2: Build a Contact-Book Entry

In Thonny, create a file `contact.py`:

1. Build a dictionary `contact` with **at least 4 keys**: `name`, `phone`, `email`, `birthday`.
2. Print each value using `contact["key"]`.
3. **Add** a new key `city` after creation.
4. **Modify** the `phone` value.
5. Print the dictionary at the end.

```python
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
```

---

##### Part 3: Predict the KeyError (and Fix It)

Given:
```python
person = {"name": "Bilal", "age": 11}
```

| # | Code | Output (or **KeyError**) |
|---|------|--------------------------|
| 1 | `print(person["name"])` | __________________________________ |
| 2 | `print(person["age"])` | __________________________________ |
| 3 | `print(person["height"])` | __________________________________ |
| 4 | `print(person.get("height"))` | __________________________________ |
| 5 | `print(person.get("height", "unknown"))` | __________________________________ |
| 6 | `print("name" in person)` | __________________________________ |
| 7 | `print("Bilal" in person)` | __________________________________ &nbsp;**(careful!)** |
| 8 | `print(len(person))` | __________________________________ |

**Rewrite line 3** so it does not crash, and instead prints `"unknown"`:
```python
__________________________________________________________
```

---

##### Part 4: List of Dictionaries

You are given:
```python
books = [
    {"title": "Holes",      "author": "Sachar",   "pages": 233},
    {"title": "Wonder",     "author": "Palacio",  "pages": 315},
    {"title": "Coraline",   "author": "Gaiman",   "pages": 162},
    {"title": "Matilda",    "author": "Dahl",     "pages": 240},
    {"title": "Hatchet",    "author": "Paulsen",  "pages": 195},
]
```

Write Python (in Thonny) to answer each:

(a) Print **just the titles**, one per line.
```python
__________________________________________________________
__________________________________________________________
```

(b) Print the **total number of pages** across all books.
```python
__________________________________________________________
__________________________________________________________
__________________________________________________________
```
Total: ________

(c) Print the **titles of books with more than 200 pages** (use the accumulator pattern).
```python
__________________________________________________________
__________________________________________________________
__________________________________________________________
__________________________________________________________
```
Result: ________________________________

(d) Convert the following list-of-tuples into a single dictionary `inventory`:
```python
pairs = [("apple", 3), ("banana", 5), ("cherry", 7), ("date", 2)]
```
```python
inventory = ___
for fruit, count in pairs:
    ______________________
print(inventory)
```
Expected: `{'apple': 3, 'banana': 5, 'cherry': 7, 'date': 2}`

---

##### Reflection
1. Give one **real-world** example where a **tuple** is the right choice and explain why.
   ______________________________________________________________________________________
2. Why does `student["height"]` raise `KeyError` but `student.get("height")` does not?
   ______________________________________________________________________________________
3. When would you choose a **list of dictionaries** over a **dictionary of lists**?
   ______________________________________________________________________________________

##### Bonus / Stretch Challenge
Write a function `word_count(text)` that takes a string and returns a dictionary mapping each lowercase word to the number of times it appears.

```python
def word_count(text):
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________

print(word_count("the cat sat on the mat the cat slept"))
# Expected: {'the': 3, 'cat': 2, 'sat': 1, 'on': 1, 'mat': 1, 'slept': 1}
```

---

### Session 24: Project 4 — Quiz & Leaderboard App

---

#### SESSION 24 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 24 of 48 |
| **Title** | Project 4: Quiz & Leaderboard App — Apply Lists, Dicts, Search & Sort |
| **Unit** | Unit 4: Lists & Standard Algorithms |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate |
| **Cambridge Alignment** | 0478 §10 — applied use of arrays, search, sort; §7 — algorithm design (pseudocode + flowchart) |
| **Singapore Alignment** | O-Level 7155 Module 4 — integrated project applying list operations + standard algorithms |

##### Learning Objectives (SMART)
By the end of this session, learners will have:
1. **Designed** the program with **pseudocode + a flowchart** before coding (Cambridge problem-solving cycle).
2. **Built** a working quiz that stores questions as a **list of dictionaries**, tracks score, and shows an end-of-quiz summary.
3. **Applied** **linear search** (find a player's score on the leaderboard) and **bubble sort** (sort the leaderboard descending) — the two unit standard algorithms — inside their own program.
4. **Tested** their app against a peer-test rubric and made at least one improvement based on the feedback.

##### Materials Needed
- Thonny IDE.
- Printed worksheet (Session 24) — project planner + checklist + peer-test rubric.
- Whiteboard for the design walkthrough.
- A starter scaffold file `project4_starter.py` provided on the shared drive (containing only the question bank and TODOs).
- Optional: small prizes / stickers for "best UX" and "best stretch goal".

##### Procedure

**0–5 min: Warm-Up — Project Tour**
Show a 30-second demo of the **finished** app on the projector (the teacher's reference build). Players are asked 5 questions, get a score, and see a **sorted leaderboard** of the past players. *"By the end of today, **you** will have built this — using **everything** from the last 5 sessions."* Reveal the goal cards on the board:
- ✅ Question bank as **list of dicts**
- ✅ Score tracking with a counter
- ✅ End-of-quiz summary
- ✅ **Linear search** to look up a player's score
- ✅ **Bubble sort** to rank the leaderboard

**5–15 min: Design Phase — Pseudocode + Flowchart**

Walk through the **design** on the board **before** any typing. Cambridge IGCSE rewards this in problem-solving questions.

**Pseudocode** (collaborative — students copy as you write):
```
PROCEDURE main()
    DECLARE questions  list of {q, a} dictionaries
    DECLARE leaderboard  empty list of {name, score} dictionaries

    REPEAT
        OUTPUT "Enter your name:"
        INPUT player_name
        score  0
        FOR each q in questions
            OUTPUT q["q"]
            INPUT user_answer
            IF user_answer = q["a"] THEN
                score  score + 1
                OUTPUT "Correct!"
            ELSE
                OUTPUT "Wrong. Answer was ", q["a"]
            ENDIF
        NEXT q
        OUTPUT "Your score: ", score, " / ", LENGTH(questions)
        APPEND {player_name, score} TO leaderboard
        BUBBLE_SORT leaderboard BY score DESCENDING
        OUTPUT leaderboard
        OUTPUT "Play again? (y/n)"
        INPUT again
    UNTIL again = "n"
ENDPROCEDURE
```

**Flowchart** — draw a vertical flowchart with:
- **Terminal**: Start
- **Process**: Set up questions
- **Process**: Get player_name; score = 0
- **Decision**: More questions?
- **Process**: Ask question, read answer
- **Decision**: Correct?
- **Process**: score += 1 (or show correct answer)
- **Process** (after loop): append to leaderboard, **bubble sort**, show
- **Decision**: Play again?
- **Terminal**: End

Students copy the flowchart on the worksheet's planner.

**15–35 min: Guided Build — Live Code the Backbone**

Type the core file together. Pace: ~20 minutes. Students follow along.

```python
# project4_quiz.py — Quiz & Leaderboard App

# 1) The question bank: a list of dictionaries
questions = [
    {"q": "What is 7 * 8?",                   "a": "56"},
    {"q": "Capital of Japan?",                "a": "tokyo"},
    {"q": "How many continents are there?",   "a": "7"},
    {"q": "What does CPU stand for?",         "a": "central processing unit"},
    {"q": "Largest planet in our system?",    "a": "jupiter"},
]

# 2) The leaderboard — list of {name, score} dictionaries
leaderboard = []

# 3) Bubble sort — descending by 'score' key
def sort_leaderboard_desc(board):
    n = len(board)
    for i in range(n - 1):
        for j in range(n - 1 - i):
            if board[j]["score"] < board[j + 1]["score"]:    # < for DESCENDING
                board[j], board[j + 1] = board[j + 1], board[j]
    return board

# 4) Linear search — find a player's row by name
def find_player(board, name):
    for i in range(len(board)):
        if board[i]["name"].lower() == name.lower():
            return i
    return -1

# 5) Run one round of the quiz for a single player
def play_quiz(player_name):
    score = 0
    for item in questions:
        user_answer = input(item["q"] + " ")
        if user_answer.strip().lower() == item["a"].lower():
            score = score + 1
            print("Correct!")
        else:
            print(f"Wrong. The answer was: {item['a']}")
    print(f"\n{player_name}, you scored {score} / {len(questions)}.\n")
    return score

# 6) Main loop
print("=== QUIZ & LEADERBOARD ===\n")
while True:
    name = input("Enter your name (or 'quit' to stop): ").strip()
    if name.lower() == "quit":
        break

    score = play_quiz(name)
    leaderboard.append({"name": name, "score": score})
    sort_leaderboard_desc(leaderboard)

    print("\n--- LEADERBOARD ---")
    for i in range(len(leaderboard)):
        row = leaderboard[i]
        print(f"{i + 1}. {row['name']:<15} {row['score']}")
    print()

    # Use linear search to show the current player's rank
    rank = find_player(leaderboard, name)
    print(f"{name}, you are at rank {rank + 1}.\n")

print("Thanks for playing!")
```

**Key teaching beats while typing:**
- Point at `[{"q": ..., "a": ...}, …]` — *"this is the **list of dicts** from yesterday."*
- Point at `if board[j]["score"] < board[j+1]["score"]` — *"This is **bubble sort** from Session 22, but with `<` for descending and `["score"]` to compare a dict field."*
- Point at `find_player` — *"This is **linear search** from Session 21 — exactly the same shape, different data."*
- Use `input(...).strip().lower()` to make answers forgiving — discuss *robustness*.

**Stretch ideas (write on the board):**
- `import random; random.shuffle(questions)` at start of each round — order-randomised.
- Persistent leaderboard saved to a `.txt` file (preview Unit 6).
- Show the **top 3** only after sorting (`leaderboard[:3]`).
- Hint system — e.g. show the first letter of the answer.

**35–50 min: Independent Practice — Build & Customise**
Students start from the scaffold or rebuild from scratch. Teacher rotates and uses the **Build Checklist** (worksheet Part 3) for spot-check. Insist that **every** student wires up `find_player` and `sort_leaderboard_desc`, even if they skip stretch goals.

**50–55 min: Sharing & Discussion — Peer Test**
Pairs swap seats and play each other's quiz using the **Peer-Test Rubric** (worksheet Part 4). Each tester gives one ⭐ ("works great") and one 🔧 ("could improve") note.

**55–60 min: Closure & Preview**
Whole-class round of applause for shipping a real, multi-feature app. Recap unit: *"You can now store collections (lists, tuples, dicts), search them (linear search), sort them (bubble sort), and combine all of these into a working program."* Preview Unit 5 (Sessions 25–30): *"Functions — how to package up our linear-search, bubble-sort, and quiz logic into reusable, testable building blocks. The professional way to write code."*

##### Differentiation
**Support:**
- Provide the scaffold file with `questions` already typed and `find_player` / `sort_leaderboard_desc` already implemented — student writes only `play_quiz` and the main loop.
- Reduce the question bank to 3 questions to shrink the testing time.
- Allow exact-string answer matching (no `.lower()` / `.strip()`).

**Extension:**
- Implement `random.shuffle(questions)` and save/load the leaderboard from a file.
- Add **categories**: extend each question dict with `"category"` and let the player pick.
- Track **time per question** with `import time` and break ties on the leaderboard by speed.
- Replace bubble sort with `sorted(board, key=lambda r: r["score"], reverse=True)` and discuss the trade-off.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Mastery (4) |
|-----------|---------------|----------------|----------------|-------------|
| **Design before code** | No pseudocode/flowchart | Pseudocode only, partial | Pseudocode + flowchart, both match the build | Design includes edge cases (empty board, repeat name) |
| **Core build** | App does not run | Runs but score or summary missing | All 5 goal cards ticked: bank, score, summary, search, sort | App also has at least one stretch feature |
| **Correct algorithm use** | Uses `sorted()` instead of bubble sort | Bubble sort present but buggy or ascending only | Bubble sort descending + linear search both correct | Algorithms generalised (e.g. sort by any key) |
| **Robustness & UX** | Crashes on blank input | Some forgiving comparison, minimal prompts | Strips/lowers answers, clear prompts, clean leaderboard print | Handles "quit", duplicate names, prints rank gracefully |

##### Teacher Notes
- The biggest time-sink is the **answer normalisation** (`.strip().lower()`). If you skip it, half the class will type `Tokyo` and be marked wrong by `tokyo`. Address it explicitly.
- Bubble sort on a list of **dicts** is a small leap from sorting a list of **numbers**. The key is `board[j]["score"]` — circle this on the board.
- Don't let the stretch goals derail the core build. The **5 goal cards** are non-negotiable; everything else is bonus.
- For peer testing, encourage **kindness with specifics**: "I liked that you accepted lower-case answers" beats "It was good".
- End the unit with a clear bridge to functions (Unit 5): *"Notice how `play_quiz`, `find_player`, and `sort_leaderboard_desc` are already **functions**? That's the secret of good code, and it's the whole next unit."*

---

#### SESSION 24 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Project Planning

(a) **Pseudocode skeleton** — fill in the blanks for the main loop:
```
DECLARE leaderboard  empty list
REPEAT
    OUTPUT "Enter your name:"
    INPUT name
    IF name = "quit" THEN
        ____________________
    ENDIF
    score  ____________________
    FOR each item in questions
        OUTPUT item["q"]
        INPUT user_answer
        IF ____________________ THEN
            score  ____________________
        ENDIF
    NEXT item
    APPEND ____________________ TO leaderboard
    CALL ____________________  // bubble sort, descending
    OUTPUT leaderboard
UNTIL ____________________
```

(b) **Flowchart** — draw your flowchart in the box. Use these standard shapes:
- **Oval** = Start / End
- **Parallelogram** = Input / Output
- **Rectangle** = Process
- **Diamond** = Decision

```
+-------------------------------------------------------------+
|                                                             |
|                                                             |
|                                                             |
|                                                             |
|                                                             |
|                                                             |
|                                                             |
|                                                             |
|                                                             |
|                                                             |
|                                                             |
|                                                             |
+-------------------------------------------------------------+
```

---

##### Part 2: Sample Question Bank

Create your **own** question bank of **at least 5** questions. Aim for variety (maths, geography, computing, pop culture). Write them in this table first, **then** transfer to code as a list of dictionaries.

| # | Question | Answer (lowercase) |
|---|----------|---------------------|
| 1 | _______________________________________ | _________________ |
| 2 | _______________________________________ | _________________ |
| 3 | _______________________________________ | _________________ |
| 4 | _______________________________________ | _________________ |
| 5 | _______________________________________ | _________________ |
| 6 | _______________________________________ | _________________ |

Now write it as Python:
```python
questions = [
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
    __________________________________________________________
]
```

---

##### Part 3: Build Checklist (tick as you go)

| ✓ | Goal | How I know it works |
|---|------|---------------------|
| ☐ | Question bank stored as a list of dictionaries | I can `print(questions[0]["q"])` |
| ☐ | Score variable starts at 0 and increments only on correct | I can deliberately get one wrong and watch the score not change |
| ☐ | End-of-quiz summary shows score and total | "You scored 3 / 5" appears |
| ☐ | New player added to leaderboard as `{"name": ..., "score": ...}` | `print(leaderboard)` after the round shows them |
| ☐ | **Bubble sort** sorts leaderboard **descending** by score | The highest score is index 0 |
| ☐ | **Linear search** `find_player(board, name)` returns the rank | Re-playing as the same name shows the correct rank |
| ☐ | Answers are case-insensitive and ignore extra spaces | `Tokyo`, `tokyo`, ` tokyo  ` all count as correct |
| ☐ | Player can quit cleanly with `"quit"` | Program ends without crashing |
| ☐ | **Stretch:** questions are shuffled with `random.shuffle` | The order changes every round |
| ☐ | **Stretch:** only top 3 are shown on the leaderboard | Slice `[:3]` |

---

##### Part 4: Peer-Test Rubric

Swap seats with a partner and play **their** app. Score 1–4 in each row.

| Criterion | 1 (poor) | 2 (some) | 3 (good) | 4 (excellent) | My score |
|-----------|----------|----------|----------|---------------|----------|
| **Runs without crashing** | crashes on first input | crashes occasionally | runs to end | survives bad input gracefully | _____ |
| **Score tracking is correct** | score stays 0 always | score sometimes wrong | counts correctly | also handles ties / re-plays | _____ |
| **Leaderboard sorted descending** | not sorted | sorted ascending | sorted descending | also formatted nicely with rank numbers | _____ |
| **Linear search shows player rank** | not implemented | implemented but wrong | correct rank shown | also says "personal best!" if they improved | _____ |
| **Question quality / fun** | bland / repeated | OK | varied & interesting | clever, challenging, age-appropriate | _____ |

**One ⭐ ("works great")**: ____________________________________________________________

**One 🔧 ("could improve")**: __________________________________________________________

After the peer test, write **one improvement** you will make to **your own** app:
______________________________________________________________________________________

---

##### Reflection
1. Where in your code did you use the **list of dictionaries** pattern from Session 23? What would you have done **without** dictionaries?
   ______________________________________________________________________________________
2. Where did **linear search** appear in your project? Where did **bubble sort** appear?
   ______________________________________________________________________________________
3. If you re-built this app tomorrow, what is the **first thing** you would design differently and why?
   ______________________________________________________________________________________

##### Bonus / Stretch Challenge
Pick **one** of these to attempt and demo at the end of class. Record what you did:

(a) **Shuffled questions** with `random.shuffle(questions)` so each round is different.

(b) **Top-3 leaderboard** — only print the top 3 entries; if there are fewer, print all.

(c) **Hint system** — if the player presses Enter on a blank answer, reveal the first letter and re-ask.

(d) **Persistent leaderboard** — save the leaderboard to `leaderboard.txt` after each round and load it at startup.

What I tried: ________________________________________________________________________
What worked: ________________________________________________________________________
What didn't (yet!): __________________________________________________________________

---
