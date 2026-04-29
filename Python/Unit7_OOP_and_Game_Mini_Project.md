# Python Programming for Kids: Lesson Plans & Worksheets
## Unit 7: Object-Oriented Programming & Game Mini-Project (Sessions 37–42)

### Unit Overview
Unit 7 introduces learners to **object-oriented programming (OOP)** at an awareness level appropriate for ages 10–14, then channels those ideas into a friendly, visual **Pygame Zero** mini-project. Students learn to model real-world things as **classes** with **attributes** and **methods**, build small simulations using **lists of objects**, and finally translate the abstract idea of "an object that has state and behaviour" into a tangible game sprite. The unit closes with a self-designed arcade game that uses score, lives, collisions, sound, and a clear "game over" state. Although formal OOP is a Cambridge AS/A Level 9618 topic, an early, gentle introduction here gives students who continue to IGCSE 0478 or Singapore O-Level Computing 7155 a powerful conceptual head-start. The unit deliberately keeps inheritance as a *stretch sidebar* only — the core takeaway is "code that bundles data + behaviour together."

---

### Session 37: Classes & Objects

---

#### SESSION 37 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 37 of 48 |
| **Title** | Classes & Objects — Modelling the World in Code |
| **Unit** | Unit 7: OOP & Game Mini-Project |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced |
| **Cambridge Alignment** | 9618 introductory paradigms — OOP awareness; 0478 §10 programming concepts (data structures and program design); Lower Secondary Computing 0860 — abstraction and decomposition |
| **Singapore Alignment** | O-Level Computing 7155 §1 problem analysis & design (abstraction); 21CC critical & creative thinking; EdTech Masterplan creation pillar |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Define** the terms *class*, *object (instance)*, and *attribute* and give one real-world example for each within 60 seconds when asked orally.
2. **Write** a Python class with at least three attributes initialised through `__init__(self, ...)` that runs without `NameError` or `TypeError`.
3. **Create** at least two distinct instances of their class and print each instance's attribute values using dot-notation (`obj.attribute`).
4. **Distinguish** between a class definition (the *blueprint*) and an instance (the *built thing*) by correctly labelling 4 out of 5 examples on the worksheet.

##### Materials Needed
- Thonny IDE with Python 3.11+ on every workstation
- Projector / shared screen for live coding
- Printed worksheets (one per student)
- A physical "blueprint vs building" prop — e.g. a paper house plan and a small Lego house — to anchor the metaphor
- Whiteboard for drawing object diagrams
- Note: **install Pygame Zero (`pip install pgzero`) on all machines before Session 40** — flag this to lab tech today

##### Procedure

**0–5 min: Warm-Up — "Cookie Cutter and Cookies"**
Hold up a cookie cutter and (if possible) two cookies cut from it. Ask: *"How many cookie cutters? How many cookies? Are the cookies all identical?"* Lead the conclusion: one *cutter* (the **class**), many *cookies* (the **objects/instances**), each cookie can have its own decoration (its own **attribute values**). Tell students: today they will write a "cookie cutter" in Python.

**5–15 min: Introduction — From Variables to Classes**
Recap on the board: so far, to describe a dog we used many separate variables:

```python
dog1_name = "Rex"
dog1_breed = "Labrador"
dog1_age = 4

dog2_name = "Bella"
dog2_breed = "Poodle"
dog2_age = 2
```

Ask: *"What's annoying about this?"* Elicit: it doesn't scale, you can mix up `dog1_name` with `dog2_age`, the data isn't bundled. Introduce the solution:

```python
class Dog:
    def __init__(self, name, breed, age):
        self.name = name
        self.breed = breed
        self.age = age

rex = Dog("Rex", "Labrador", 4)
bella = Dog("Bella", "Poodle", 2)

print(rex.name, "is a", rex.breed)
print(bella.name, "is", bella.age, "years old")
```

Walk through, line by line:
- `class Dog:` — the **blueprint**. **PascalCase** name (capital first letter of each word).
- `def __init__(self, ...):` — the **constructor**. Runs automatically when you say `Dog(...)`.
- `self` — "the object I'm currently building." Every time you write `self.name = name`, you're saying *"on this particular dog, store its name."*
- `rex = Dog("Rex", "Labrador", 4)` — Python builds a fresh dog and hands it back.
- `rex.name` — dot-notation: "go inside `rex` and read its `name`."

Spend extra time on **`self`**. Use the analogy: when a teacher says "open *your* book," each student opens *their own* book. `self` is "your" inside the class.

**15–35 min: Guided Practice — Build a `Student` Class Together**
Live code, pausing every few lines for student predictions (PRIMM: Predict → Run → Investigate → Modify → Make):

```python
class Student:
    def __init__(self, name, grade, score):
        self.name = name
        self.grade = grade
        self.score = score

# Predict: what will print?
amir = Student("Amir", 7, 88)
priya = Student("Priya", 7, 92)

print(amir.name, "scored", amir.score)
print(priya.name, "is in grade", priya.grade)
```

Then run **Modify**:
1. Change `amir`'s score to 95 *after* creation: `amir.score = 95`.
2. Add a 4th attribute `school` and rebuild.
3. Try the common bug: forget `self.` on one line and watch the error.

Demonstrate the bug deliberately:

```python
class BadStudent:
    def __init__(self, name, grade):
        self.name = name
        grade = grade   # <-- BUG: missing self.

s = BadStudent("Ravi", 8)
print(s.grade)   # AttributeError!
```

Read the error together: *"AttributeError: 'BadStudent' object has no attribute 'grade'"* — and explain the fix. This sets students up to debug their own missing-`self.` errors later.

Object diagram on the whiteboard:

```
    +---------------+
    |   Student     |
    +---------------+
    | name = "Amir" |
    | grade = 7     |
    | score = 88    |
    +---------------+
```

Show two boxes side-by-side: one for `amir`, one for `priya`. Same blueprint, different filled-in values.

**35–50 min: Independent Practice — Worksheet**
Distribute the worksheet. Students:
- Identify class vs object in 6 examples (Part 1).
- Build a `Book` class with `title`, `author`, `pages` (Part 2).
- Draw object diagrams for two book instances (Part 3).

Circulate. Common error to watch for: students writing `def __init__(name, age):` without `self`. Ask them to read the error aloud — it's a teaching moment.

**50–55 min: Sharing & Discussion**
Two volunteers project their `Book` classes. Class spots whether `__init__` uses `self` correctly. Discuss: *"Why do we say 'an object has state'?"* Land on: state = attribute values; behaviour comes next session.

**55–60 min: Closure & Preview**
Exit ticket (one sentence on a sticky note): *"In your own words, what is the difference between a class and an object?"* Preview Session 38: *"Right now our objects only **have** stuff. Next session we'll teach them to **do** stuff — methods!"*

##### Differentiation
**Support:** Provide a fill-in-the-blank `Book` class skeleton. Pair with a confident peer for the diagram drawing. Allow them to copy the `Dog` example and rename to `Book` step by step.
**Extension:** Ask them to add a 5th attribute that is itself a list (e.g. `genres = ["fantasy", "adventure"]`) and access individual genres with `book.genres[0]`. Introduce the idea of a default argument: `def __init__(self, title, author, pages=100):`.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Advanced (4) |
|-----------|---------------|----------------|----------------|--------------|
| Class syntax | Misses `class` keyword or colon | Class compiles but `__init__` malformed | Correct `class` + `__init__` with `self` | Correct + uses PascalCase + sensible defaults |
| Attribute assignment | Forgets `self.` on most lines | One missing `self.` | All attributes assigned with `self.` | All assigned + types match parameter names |
| Instance creation | Cannot create an instance | Creates one instance only | Creates ≥ 2 distinct instances | Creates ≥ 2 instances + accesses all attributes |
| Class vs object understanding | Confuses the two terms | Identifies most examples correctly | Identifies all 6 worksheet examples | Identifies all + explains in own words |

##### Teacher Notes
- The single biggest stumble is **`self`**. Don't promise a deep explanation today — promise that "if you write `self.x = x` on every line, it will work, and we'll see *why* in Session 38."
- PascalCase vs snake_case is genuinely useful here — `class Student` for the blueprint, `student1` for the variable. Reinforce.
- Don't introduce methods yet. Resist! Today is purely *state*.
- Some students will ask "is this like a dictionary?" — yes, attributes feel dictionary-like, but say *"it's even more powerful — wait until tomorrow."*
- If `__init__` is mistyped as `__int__` or `_init_`, the class will silently *not* run the constructor and `obj.name` will fail. Watch for this.

---

#### SESSION 37 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Class or Object?
For each item, circle whether it describes a **CLASS** (a blueprint) or an **OBJECT** (a specific thing). Then explain in one sentence why.

1. The recipe for chocolate-chip cookies. ........... CLASS / OBJECT — Why? _______________________
2. The cookie I am eating right now. ................ CLASS / OBJECT — Why? _______________________
3. The plan for a Honda Civic in the factory. ....... CLASS / OBJECT — Why? _______________________
4. My uncle's red Honda Civic with licence plate SGB-5587. CLASS / OBJECT — Why? _______________________
5. `class Dog:` ..................................... CLASS / OBJECT — Why? _______________________
6. `rex = Dog("Rex", "Labrador", 4)` ................ CLASS / OBJECT — Why? _______________________

##### Part 2: Build a `Book` Class
Complete the missing lines so that the program runs without errors and prints the correct output.

```python
class _________ :
    def __init__(self, title, author, pages):
        self.title = _________
        self._________ = author
        self.pages = _________

book1 = Book("Charlotte's Web", "E. B. White", 192)
book2 = Book("The Hobbit", "_________", _________)

print(book1.title, "has", book1.pages, "pages.")
print(book2.title, "is by", book2.author)
```

Expected output:
```
Charlotte's Web has 192 pages.
The Hobbit is by J. R. R. Tolkien
```

Now extend the class on the same machine (Thonny):
1. Add a 4th attribute `is_borrowed` that defaults to `False`.
2. Create a 3rd instance `book3` with values of your own choice.
3. Print: `<title> is borrowed: <True/False>`.

Paste your final code below (or attach a printout):

```python
# Your extended Book class:




```

##### Part 3: Object Diagram Drawing
For each instance you created (`book1`, `book2`, `book3`), draw a labelled box that lists every attribute and its value. Example shape:

```
+----------------------------+
|         book1              |
+----------------------------+
| title = "Charlotte's Web"  |
| author = "E. B. White"     |
| pages = 192                |
| is_borrowed = False        |
+----------------------------+
```

Draw `book2` and `book3` here:

(Space provided.)

##### Reflection
1. What does the keyword `self` mean *inside* a class? Try to answer in your own words, not the teacher's.

   _____________________________________________________________________

2. What happens if you forget the `self.` in front of an attribute inside `__init__`? Describe the error message you saw (or that you predict).

   _____________________________________________________________________

3. Give one real-world example (different from Dog/Book/Student) of something you could model as a class. What 3 attributes would it have?

   Class name: ________________  Attributes: ________________________________

##### Bonus / Stretch Challenge
Design a `Pizza` class with attributes `size` (small/medium/large), `toppings` (a *list* of strings), and `price` (a number). Create three pizzas and print a tidy "menu" using a `for` loop:

```
Pizza 1: medium with ['cheese', 'mushroom'] — $12
Pizza 2: ...
```

---

### Session 38: Methods & Attributes

---

#### SESSION 38 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 38 of 48 |
| **Title** | Methods & Attributes — Giving Objects Behaviour |
| **Unit** | Unit 7: OOP & Game Mini-Project |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced |
| **Cambridge Alignment** | 9618 OOP awareness — methods and encapsulation; 0478 §10 program construction; Lower Secondary Computing 0860 — modular design |
| **Singapore Alignment** | O-Level Computing 7155 §2 program design (procedures and modularity); 21CC self-directed learning |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Add** a method to an existing class such that the method takes `self` as its first parameter and runs without a `TypeError` about missing positional arguments.
2. **Differentiate** between methods that *read* attributes and methods that *change* attributes by correctly classifying 4 out of 5 examples.
3. **Implement** a `__str__` method that returns a string and verify it is invoked when the object is printed.
4. **Trace** by hand the value of an attribute (e.g. `account.balance`) across at least 3 method calls, achieving 80% accuracy on the worksheet trace table.

##### Materials Needed
- Thonny + Python 3.11+
- Printed worksheets
- Whiteboard for trace tables
- Optional: a stress-ball "Player" prop you pretend to "damage" and "heal" while live coding

##### Procedure

**0–5 min: Warm-Up — "What can a Dog DO?"**
Recall yesterday's `Dog` class. Ask: *"It has name, breed, age — but a real dog can also do things. What?"* Collect: bark, eat, sleep, fetch. Tell students: those are **methods**.

**5–15 min: Introduction — Methods Are Functions That Live Inside a Class**

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print(self.name + " says Woof!")

    def have_birthday(self):
        self.age = self.age + 1
        print(self.name + " is now", self.age)

rex = Dog("Rex", 4)
rex.bark()              # Rex says Woof!
rex.have_birthday()     # Rex is now 5
rex.have_birthday()     # Rex is now 6
print(rex.age)          # 6
```

Key teaching points:
- A **method** is just a `def` *indented inside the class*.
- Every method's first parameter is **`self`**. Always. (We don't pass it ourselves — Python fills it in.)
- `bark` only **reads** an attribute (`self.name`). It's a *getter-style* method.
- `have_birthday` **changes** an attribute (`self.age = self.age + 1`). It's a *setter / mutator*.

Now show why `self` matters:

```python
rex = Dog("Rex", 4)
bella = Dog("Bella", 2)

rex.have_birthday()
print(rex.age, bella.age)   # 5  2  — only Rex changed!
```

`self` is the way a method knows *which dog* to operate on.

**15–35 min: Guided Practice — `BankAccount` Then `Player`**

Build live, with predictions:

```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        self.balance = self.balance + amount
        print(self.owner, "deposited", amount, "— new balance:", self.balance)

    def withdraw(self, amount):
        if amount > self.balance:
            print("Sorry,", self.owner + ", insufficient funds.")
        else:
            self.balance = self.balance - amount
            print(self.owner, "withdrew", amount, "— new balance:", self.balance)

    def __str__(self):
        return f"Account[{self.owner}: ${self.balance}]"

acc = BankAccount("Mei Ling", 100)
acc.deposit(50)        # 150
acc.withdraw(30)       # 120
acc.withdraw(500)      # refused
print(acc)             # Account[Mei Ling: $120]
```

Highlight `__str__`:
- It must `return` (not `print`) a string.
- Python calls it automatically when you `print(obj)` or use `str(obj)`.
- Without it, you'd see something like `<__main__.BankAccount object at 0x10a5d8>` — useless to humans.

Trace table on the whiteboard for the call sequence:

| Step | Call | self.balance before | self.balance after |
|------|------|---------------------|--------------------|
| 1 | `__init__("Mei Ling", 100)` | — | 100 |
| 2 | `deposit(50)` | 100 | 150 |
| 3 | `withdraw(30)` | 150 | 120 |
| 4 | `withdraw(500)` | 120 | 120 (refused) |

Now `Player` for game vibes:

```python
class Player:
    def __init__(self, name, health=100):
        self.name = name
        self.health = health

    def take_damage(self, amount):
        self.health -= amount
        if self.health < 0:
            self.health = 0
        print(self.name, "took", amount, "damage. Health:", self.health)

    def heal(self, amount):
        self.health += amount
        if self.health > 100:
            self.health = 100
        print(self.name, "healed. Health:", self.health)

    def is_alive(self):
        return self.health > 0

    def __str__(self):
        status = "alive" if self.is_alive() else "DEFEATED"
        return f"{self.name} [{self.health} HP — {status}]"

hero = Player("Aria")
hero.take_damage(30)
hero.take_damage(40)
hero.heal(20)
print(hero)
print("Still alive?", hero.is_alive())

hero.take_damage(200)
print(hero)
print("Still alive?", hero.is_alive())
```

Notice `is_alive()` *returns* a boolean — it's a **predicate** method. Methods that return values are useful inside `if` and `while`.

Show one common bug — forgetting `self`:

```python
class Counter:
    def __init__(self):
        self.count = 0

    def increment():       # BUG: missing self
        self.count += 1

c = Counter()
c.increment()
# TypeError: increment() takes 0 positional arguments but 1 was given
```

Read the error together: *"takes 0 but 1 was given"*. The "1" Python is complaining about is the implicit `self`. The fix is `def increment(self):`.

**35–50 min: Independent Practice — Worksheet**
Students:
- Predict outputs of method calls on a given class (Part 1).
- Find and fix three `self` bugs (Part 2).
- Add two new methods to an existing `Robot` class (Part 3).

**50–55 min: Sharing & Discussion**
Volunteers share a method they added to `Robot`. Discuss: *"Which of your methods read attributes and which change them?"*

**55–60 min: Closure & Preview**
Exit ticket: *"Why is `self` the first parameter of every method?"* Preview Session 39: *"Tomorrow: many objects working together — a whole classroom, a whole shop, a whole team."*

##### Differentiation
**Support:** Hand out a partially completed `BankAccount` class with method signatures already typed; students only fill in the bodies. Use a sticker labelled "self" they can physically place on whichever object is "talking" right now.
**Extension:** Add a class-level counter `BankAccount.total_accounts` that increments inside `__init__` and a `transfer(self, other, amount)` method that moves money between two accounts.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Advanced (4) |
|-----------|---------------|----------------|----------------|--------------|
| Method definition | Methods missing `self` | One method missing `self` | All methods correctly take `self` | All correct + sensible parameter names |
| Read vs change | Cannot tell them apart | Identifies one type | Classifies 4/5 correctly | All correct + explains why |
| `__str__` use | Not implemented | Implemented but uses `print` | Returns a clear string | Returns string + uses f-string + uses helper method |
| Trace table | <50% correct | 50–79% correct | 80–95% correct | 100% + annotates each step |

##### Teacher Notes
- Many students will write `print` instead of `return` in `__str__`. The result still prints something, but `str(obj)` returns `None`. Catch this early.
- Discourage using `BankAccount.balance` (class-level access) — it's an instance attribute. Always `acc.balance`.
- The `if amount > self.balance` guard in `withdraw` is a teaching moment for **defensive programming** — methods should protect their own data.
- Avoid showing `@property` or `@staticmethod` today. Awareness, not depth.
- Some learners want to know "how does Python know to fill in `self`?" — short answer: `acc.deposit(50)` is secretly translated to `BankAccount.deposit(acc, 50)`. Mention only if asked.

---

#### SESSION 38 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Predict the Output
Read the code carefully. Write what each `print` statement will display.

```python
class Lamp:
    def __init__(self):
        self.is_on = False
        self.brightness = 0

    def switch_on(self):
        self.is_on = True
        self.brightness = 50

    def dim(self, amount):
        self.brightness -= amount
        if self.brightness < 0:
            self.brightness = 0

    def __str__(self):
        return f"Lamp(on={self.is_on}, brightness={self.brightness})"

lamp = Lamp()
print(lamp)                # (a) ________________________
lamp.switch_on()
print(lamp)                # (b) ________________________
lamp.dim(20)
print(lamp.brightness)     # (c) ________________________
lamp.dim(40)
print(lamp.brightness)     # (d) ________________________
print(lamp.is_on)          # (e) ________________________
```

##### Part 2: Fix the `self` Bugs
Each snippet below contains exactly ONE bug related to `self`. Circle the bug and write the corrected line beside it.

**Bug 1**
```python
class Cat:
    def __init__(self, name):
        name = name              # <-- bug?
    def meow(self):
        print(self.name + ": meow")
```
Fix: __________________________________________

**Bug 2**
```python
class Counter:
    def __init__(self):
        self.value = 0
    def increment():             # <-- bug?
        self.value += 1
```
Fix: __________________________________________

**Bug 3**
```python
class Box:
    def __init__(self, w, h):
        self.w = w
        self.h = h
    def area(self):
        return w * h             # <-- bug?
```
Fix: __________________________________________

##### Part 3: Extend the `Robot` Class
You are given:

```python
class Robot:
    def __init__(self, name, energy=100):
        self.name = name
        self.energy = energy

    def move(self, steps):
        cost = steps * 2
        self.energy -= cost
        if self.energy < 0:
            self.energy = 0
        print(self.name, "moved", steps, "steps. Energy left:", self.energy)
```

**Task A:** Add a `recharge(self, amount)` method that increases `energy` but never above 100.

**Task B:** Add a method `report(self)` that returns (not prints!) a string in the form `"R2D2 has 80 energy"`.

**Task C:** Add a `__str__` method that uses `report` so `print(robot)` works nicely.

**Task D:** Trace the calls below. Fill in the trace table.

```python
r = Robot("R2D2")
r.move(10)
r.recharge(15)
r.move(50)
r.recharge(200)
print(r)
```

| Step | Call | energy before | energy after |
|------|------|---------------|--------------|
| 1 | `__init__("R2D2")` | — | ____ |
| 2 | `move(10)` | ____ | ____ |
| 3 | `recharge(15)` | ____ | ____ |
| 4 | `move(50)` | ____ | ____ |
| 5 | `recharge(200)` | ____ | ____ |
| 6 | `print(r)` outputs: ____________________________________ | | |

##### Reflection
1. In your own words, explain why every method needs `self` as its first parameter.

   _____________________________________________________________________

2. What is the difference between a method that *reads* an attribute and one that *changes* it? Give an example of each from this worksheet.

   _____________________________________________________________________

3. Why does `__str__` use `return` and not `print`?

   _____________________________________________________________________

##### Bonus / Stretch Challenge
Add a `battle(self, other)` method to `Player` (from class) where two players take turns hitting each other for 10 damage until one is no longer `is_alive()`. Print every round. Whose `take_damage` does each call need to invoke?

---

### Session 39: Designing with Multiple Objects

---

#### SESSION 39 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 39 of 48 |
| **Title** | Designing with Multiple Objects — Lists of Things |
| **Unit** | Unit 7: OOP & Game Mini-Project |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced |
| **Cambridge Alignment** | 9618 OOP awareness — composition; 0478 §10 program design + §8 algorithms (iteration over collections); Lower Secondary Computing 0860 — abstraction |
| **Singapore Alignment** | O-Level Computing 7155 §1 problem analysis (decomposition); 21CC critical thinking, communication |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Construct** a list of at least 4 instances of a class and iterate over them with a `for` loop calling at least one method per iteration.
2. **Design** a 3-class simulation by listing classes, attributes, and methods on a planning template.
3. **Refactor** a procedural (no-class) program into one that uses a class, preserving the original output.
4. **Justify** in writing one situation where OOP helps and one where plain functions are enough.

##### Materials Needed
- Thonny + Python 3.11+
- Printed worksheets + design planning template
- Whiteboard
- Optional: index cards for the "card-sort" activity (one card per attribute/method to assign to a class)

##### Procedure

**0–5 min: Warm-Up — "Class Roll Call"**
Ask: *"If I made a `Student` object for every person in this room, how many would I have?"* Then: *"How would I store them all?"* Lead toward: *a list*.

**5–15 min: Introduction — A List of Objects**
Live code, building on yesterday:

```python
class Student:
    def __init__(self, name, score):
        self.name = name
        self.score = score

    def is_passing(self):
        return self.score >= 50

    def __str__(self):
        return f"{self.name} ({self.score})"

# A whole class:
students = [
    Student("Amir", 88),
    Student("Bella", 42),
    Student("Chen", 71),
    Student("Diya", 95),
]

for s in students:
    status = "PASS" if s.is_passing() else "FAIL"
    print(s, "—", status)
```

Output:
```
Amir (88) — PASS
Bella (42) — FAIL
Chen (71) — PASS
Diya (95) — PASS
```

Then aggregate:

```python
total = 0
for s in students:
    total += s.score
average = total / len(students)
print("Class average:", average)

passing = [s for s in students if s.is_passing()]
print("Number passing:", len(passing))
```

Highlight: lists of objects feel exactly like lists of dictionaries, but **you call methods, not look up keys**.

**15–35 min: Guided Practice — A Tiny Shop Simulation**

```python
class Item:
    def __init__(self, name, price, stock):
        self.name = name
        self.price = price
        self.stock = stock

    def sell(self, qty):
        if qty > self.stock:
            print(f"Not enough {self.name} (have {self.stock})")
            return 0
        self.stock -= qty
        print(f"Sold {qty} x {self.name} for ${qty * self.price}")
        return qty * self.price

    def restock(self, qty):
        self.stock += qty

    def __str__(self):
        return f"{self.name}: ${self.price} (stock {self.stock})"


inventory = [
    Item("Apple",  1.0, 20),
    Item("Bread",  3.5,  8),
    Item("Cheese", 7.0,  5),
]

# Show current stock
print("--- Inventory ---")
for it in inventory:
    print(it)

# Run a few transactions
total_revenue = 0
total_revenue += inventory[0].sell(5)    # 5 apples
total_revenue += inventory[1].sell(3)    # 3 bread
total_revenue += inventory[2].sell(10)   # too much cheese!
inventory[2].restock(20)
total_revenue += inventory[2].sell(4)

print("--- After ---")
for it in inventory:
    print(it)
print("Total revenue:", total_revenue)
```

Have students predict each line's output before running. Observe how the **list** holds the inventory and **methods** carry the behaviour. The main program is short and reads almost like English.

Now demonstrate **finding** a particular object:

```python
def find_item(inventory, name):
    for it in inventory:
        if it.name == name:
            return it
    return None

bread = find_item(inventory, "Bread")
if bread is not None:
    bread.sell(2)
```

This is a great place to talk about **decomposition**: `find_item` is a free-standing function because it operates on the *whole list*, not a single item. Not everything has to be a method.

**Stretch Sidebar — Inheritance (advanced students only)**
Mark visibly on the board: ★ STRETCH — not required.

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print(self.name, "makes a sound")

class Dog(Animal):           # Dog INHERITS from Animal
    def speak(self):         # Dog OVERRIDES speak
        print(self.name, "says Woof!")

class Cat(Animal):
    def speak(self):
        print(self.name, "says Meow!")

zoo = [Dog("Rex"), Cat("Whiskers"), Animal("Generic")]
for a in zoo:
    a.speak()
```

Briefly: `class Dog(Animal):` means "a Dog **is-a** Animal." It inherits attributes/methods. Mention only — no worksheet question on inheritance.

**Discussion: When does OOP help?**
Two columns on the whiteboard:

| OOP shines | Functions are enough |
|------------|----------------------|
| Many similar things with state (players, items, accounts) | One-off calculation |
| Behaviour bundled with data | Pure transformation of data in/out |
| Things change over time (deposit, take_damage) | Stateless utilities (e.g. `square_root`) |
| Want to grow the program later | Tiny script |

**35–50 min: Independent Practice — Worksheet**
Students:
- Plan a 3-class simulation (Part 1 — design, no code).
- Build a list-of-objects loop (Part 2).
- Refactor a procedural snippet into a class (Part 3).

**50–55 min: Sharing & Discussion**
Two volunteers share their refactored programs. Ask the class: *"Is the new version easier or harder to read? Why?"*

**55–60 min: Closure & Preview**
Exit ticket: *"Name one thing you'd model as a class in a video game."* Preview Session 40: *"Tomorrow we leave the text terminal — Pygame Zero, sprites, and a moving square on the screen!"*

##### Differentiation
**Support:** Provide a half-built shop simulation; learner only writes the `for` loop and the `find_item` body. Use index cards: write attributes and methods on cards, sort onto labelled "class" sheets.
**Extension:** Add a `Customer` class to the shop, give each customer a `cart`, and let them check out. Or implement inheritance: `class Snack(Item)` with an extra `expiry_date` attribute.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Advanced (4) |
|-----------|---------------|----------------|----------------|--------------|
| List of objects | Cannot build a list | Builds a list, no iteration | List + for-loop calling methods | List + filter/aggregate |
| Design plan | <2 classes named | 3 classes but vague | 3 classes with attributes & methods | 3 classes + clear interactions |
| Refactor | Refactor doesn't run | Runs but output differs | Same output, uses class | Same output + improved naming + `__str__` |
| Justification (OOP vs functions) | No example | One example | One of each, correct | Both + a borderline case discussed |

##### Teacher Notes
- The biggest "aha" today is that the **main program shrinks**. Point this out: "Look how short the bottom of the file is now."
- Many students will try to make *everything* a class. Resist gently — give the "shopping cart total" counter-example, where a function is fine.
- Inheritance is genuinely advanced. Don't quiz on it. The goal is awareness so a confident student doesn't feel boxed in.
- Refactoring is a high-leverage skill; encourage students to keep their pre-refactor file open in a second tab so they can compare outputs.
- If a student writes a class that has only attributes (no methods) — that's fine, it's basically a record. Praise it but ask "what behaviour might it need later?"

---

#### SESSION 39 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Design a Mini-Simulation
Choose ONE scenario and plan it. **Do not code yet.** Fill in the planner.

Scenarios (pick one):
- **Library** — `Book`, `Member`, `Library`
- **Pet Shop** — `Pet`, `Customer`, `Shop`
- **Football Team** — `Player`, `Coach`, `Team`

**My choice:** ________________________________________

**Class A — name:** _______________________
- Attributes: ___________________________________________________
- Methods: ____________________________________________________

**Class B — name:** _______________________
- Attributes: ___________________________________________________
- Methods: ____________________________________________________

**Class C — name:** _______________________ (this one likely *contains a list* of A or B)
- Attributes: ___________________________________________________
- Methods: ____________________________________________________

**Sample interaction (1–2 sentences):**
_____________________________________________________________________
_____________________________________________________________________

##### Part 2: Build a List-of-Objects Loop
Use the following class — type it into Thonny, then complete the tasks below:

```python
class Song:
    def __init__(self, title, artist, length_sec):
        self.title = title
        self.artist = artist
        self.length_sec = length_sec

    def minutes(self):
        return self.length_sec / 60

    def __str__(self):
        return f"{self.title} by {self.artist} ({self.minutes():.1f} min)"
```

**Task 2a:** Create a list `playlist` of at least 4 `Song` objects.

**Task 2b:** Print every song using a `for` loop.

**Task 2c:** Compute and print the **total playlist length in minutes**.

**Task 2d:** Print only songs longer than 3 minutes.

Paste your code:
```python
# Your playlist code:




```

##### Part 3: Refactor — Functions → Class
Below is a working program with no classes. Rewrite it so that it uses a `Car` class. The output must stay identical.

**Original (no class):**
```python
def drive(fuel, distance):
    used = distance * 0.1
    fuel -= used
    if fuel < 0:
        fuel = 0
    return fuel

def refuel(fuel, amount):
    fuel += amount
    if fuel > 50:
        fuel = 50
    return fuel

car_a_fuel = 30
car_a_fuel = drive(car_a_fuel, 100)
car_a_fuel = refuel(car_a_fuel, 25)
car_a_fuel = drive(car_a_fuel, 80)
print("Car A fuel:", car_a_fuel)
```

**Your refactor (use `class Car:`):**
```python
# Your refactored code:




```

##### Reflection
1. Give one example where OOP would help. Why?

   _____________________________________________________________________

2. Give one example where plain functions are enough. Why?

   _____________________________________________________________________

3. After your refactor, did the program get longer or shorter overall? Was it easier or harder to read?

   _____________________________________________________________________

##### Bonus / Stretch Challenge
Take your **Part 1** plan and turn ONE of the three classes into actual Python code with at least 2 methods and a `__str__`. Then create 3 instances and put them in a list. Print the list with a `for` loop.

---

### Session 40: Pygame Zero — Sprites, Draw, Update

---

#### SESSION 40 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 40 of 48 |
| **Title** | Pygame Zero — Sprites, Draw & Update |
| **Unit** | Unit 7: OOP & Game Mini-Project |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced |
| **Cambridge Alignment** | 0478 §10 program development with libraries; 9618 awareness — event-driven & frame-loop programming; Lower Secondary Computing 0860 — creating digital artefacts |
| **Singapore Alignment** | O-Level Computing 7155 §3 software development (use of libraries); EdTech Masterplan creation pillar; 21CC creative thinking |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Run** a Pygame Zero program from the command line using `pgzrun program.py` and observe a window with `WIDTH`/`HEIGHT` set correctly.
2. **Place** at least one `Actor` sprite on a coloured background using a PNG inside an `images/` folder.
3. **Animate** an Actor by modifying `actor.x` or `actor.y` inside `update()` so it visibly moves each frame.
4. **Distinguish** the responsibilities of `draw()` (drawing only) and `update()` (state changes only) by correctly classifying 5 example statements.

##### Materials Needed
- Thonny + Python 3.11+
- **Pygame Zero** installed (`pip install pgzero`) — confirm before class
- Starter sprites in an `images/` folder per workstation. Free-to-use options: **Kenney.nl** (`https://kenney.nl/assets`), OpenGameArt.org. Provide a zip of pre-cleared sprites: `alien.png`, `coin.png`, `apple.png`, `rocket.png`.
- Projector
- Printed worksheets

##### Procedure

**0–5 min: Warm-Up — "What's a Frame?"**
Show a flipbook (or wave fingers like a movie clapper). *"A game is just many still pictures shown very fast. Pygame Zero shows about 60 per second. Today we tell it what to draw."*

**5–15 min: Introduction — The Pygame Zero Magic**

Open Thonny side-by-side with a terminal. Walk through:

```python
# File: hello_pgz.py
WIDTH = 600
HEIGHT = 400

def draw():
    screen.fill((30, 30, 60))
    screen.draw.text("Hello Pygame Zero!", (180, 180), color="white", fontsize=40)
```

To run it, in the **terminal**, not Python:
```
pgzrun hello_pgz.py
```

Key things to flag:
- No `import pygame`. No `while True:` loop. No `pygame.init()`. Pygame Zero hides all that.
- `WIDTH`, `HEIGHT` are **special** module-level variables Pygame Zero reads.
- `draw()` is a **special** function Pygame Zero calls automatically every frame.
- `screen` is a **special** object Pygame Zero gives you — you don't create it.

Stress: *"You don't call `draw` yourself. Pygame Zero calls it for you."*

Now add an Actor:

```python
# File: rocket.py
WIDTH = 600
HEIGHT = 400

rocket = Actor("rocket")           # looks for images/rocket.png
rocket.pos = (300, 200)

def draw():
    screen.fill((10, 10, 30))
    rocket.draw()
```

The `images/` folder must exist next to `rocket.py`. The filename must be lowercase (`rocket.png`). Run with `pgzrun rocket.py`.

**15–35 min: Guided Practice — Move That Rocket**

Add `update()`:

```python
WIDTH = 600
HEIGHT = 400

rocket = Actor("rocket")
rocket.pos = (50, 200)

def draw():
    screen.fill((10, 10, 30))
    rocket.draw()

def update():
    rocket.x += 2          # move right 2 pixels per frame
    if rocket.x > WIDTH + 50:
        rocket.x = -50     # wrap around
```

Now the rocket flies across. Discuss the loop conceptually:

```
Pygame Zero, 60 times per second:
    1. call update()        <-- you change positions / state
    2. call draw()          <-- you redraw the screen
```

Drawing primitives, not just sprites:

```python
WIDTH = 600
HEIGHT = 400

box_x = 100

def draw():
    screen.fill("skyblue")
    # Filled rectangle
    screen.draw.filled_rect(Rect((box_x, 300), (80, 80)), "red")
    # Outlined rectangle
    screen.draw.rect(Rect((400, 200), (120, 60)), "yellow")
    # Circle
    screen.draw.filled_circle((300, 100), 30, "orange")
    # Line
    screen.draw.line((0, 380), (WIDTH, 380), "white")
    # Text
    screen.draw.text("Score: 0", (10, 10), color="white", fontsize=30)

def update():
    global box_x
    box_x += 1
    if box_x > WIDTH:
        box_x = -80
```

Note `global box_x` — because `box_x` is a plain module variable, not an attribute on an object. **Foreshadow**: this is exactly why next session and the project will use Actors / classes — much cleaner.

A two-actor scene:

```python
WIDTH = 800
HEIGHT = 500

alien = Actor("alien")
alien.pos = (100, 250)

coin = Actor("coin")
coin.pos = (700, 250)

def draw():
    screen.fill((20, 30, 50))
    screen.draw.text("Catch the coin!", (260, 20), color="white", fontsize=36)
    alien.draw()
    coin.draw()

def update():
    alien.x += 1
    coin.x -= 1
    if coin.x < 0:
        coin.x = WIDTH
```

**Modify** prompts (PRIMM):
- Change the background colour using a hex tuple `(r, g, b)`.
- Make the alien also bob up and down (`alien.y += something_oscillating`).
- Add a 3rd actor of your choice.

**`draw()` vs `update()` — golden rule:**

| Goes in `draw()` | Goes in `update()` |
|------------------|--------------------|
| `screen.fill(...)` | `actor.x += 1` |
| `actor.draw()` | `score += 1` |
| `screen.draw.text(...)` | `if actor.x > WIDTH: ...` |
| `screen.draw.rect(...)` | `if game_over: ...` |

**35–50 min: Independent Practice — Worksheet**
Students:
- Predict-the-screen for 3 small programs (Part 1).
- Modify a given demo (colour, position, speed) (Part 2).
- Design and draw their own scene with at least 2 Actors and 1 shape (Part 3).

**50–55 min: Sharing & Discussion**
Walk-around gallery: every student turns their screen toward the room while the teacher counts down 30 seconds for each. Ask: *"Whose scene used `update()` to move something?"*

**55–60 min: Closure & Preview**
Exit ticket: *"Name one thing that goes in `draw` and one that goes in `update`."* Preview Session 41: *"Tomorrow: keyboard controls and collisions — your sprite will finally listen to you."*

##### Differentiation
**Support:** Provide a fully working scene (`scene_starter.py`) with a TODO comment at exactly one line; students only change that one line. Pre-make the `images/` folder.
**Extension:** Use the `clock.schedule_interval(callback, seconds)` API to spawn an extra Actor every 2 seconds, or rotate an Actor with `actor.angle += 1`.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Advanced (4) |
|-----------|---------------|----------------|----------------|--------------|
| Window setup | `pgzrun` fails | Window opens but blank | `WIDTH`/`HEIGHT` + filled background | + custom title and dimensions |
| Sprite loading | Image not found | One Actor draws | ≥1 Actor + correct positioning | ≥2 Actors composed nicely |
| Animation | Nothing moves | Movement glitches (no `update`) | Smooth motion in `update()` | Motion + wrap/bounce logic |
| draw vs update split | Mixes them | Some confusion | All 5 examples sorted correctly | Sorted + can articulate *why* |

##### Teacher Notes
- **`pgzrun` runs from the terminal**, not Thonny's green ▶ button. Some Thonny configurations run it fine through F5; if not, open Thonny's "Tools → Open system shell" and call `pgzrun file.py`. Demonstrate both.
- The `images/` folder is **case-sensitive on macOS/Linux**. `Rocket.png` ≠ `rocket.png`. Always lowercase.
- Students will forget to put the script in the *same* directory as `images/`. Show how `cd` and `ls` confirm placement.
- Resist the urge to introduce keyboard input today — Session 41 is dedicated to that.
- For students with Wi-Fi issues: have a USB stick or shared LAN folder with the Kenney sprites pre-loaded.
- Mention the licence note: Kenney.nl assets are CC0 (public domain). Students can use them freely, even in projects they share.

---

#### SESSION 40 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Predict the Screen
For each program, sketch what the window looks like (or describe in words) and say whether anything moves.

**Program A**
```python
WIDTH = 400
HEIGHT = 200

def draw():
    screen.fill("black")
    screen.draw.filled_circle((200, 100), 50, "yellow")
```
Sketch / describe: __________________________________________
Moves? YES / NO

**Program B**
```python
WIDTH = 500
HEIGHT = 300

x = 0

def draw():
    screen.fill("white")
    screen.draw.filled_rect(Rect((x, 120), (60, 60)), "green")

def update():
    global x
    x += 3
```
Sketch / describe: __________________________________________
Moves? YES / NO    What happens when `x` becomes very large? __________________

**Program C**
```python
WIDTH = 400
HEIGHT = 400

ball = Actor("coin")
ball.pos = (200, 50)

def draw():
    screen.fill("navy")
    ball.draw()

def update():
    ball.y += 2
    if ball.y > HEIGHT:
        ball.y = 0
```
Sketch / describe: __________________________________________
Moves? YES / NO    Direction? __________________________

##### Part 2: Modify the Demo
Save the following as `space_demo.py` in a folder that has `images/alien.png` and `images/rocket.png`. Run it with `pgzrun space_demo.py`. Then make the listed modifications.

```python
WIDTH = 700
HEIGHT = 400

alien = Actor("alien")
alien.pos = (100, 200)

rocket = Actor("rocket")
rocket.pos = (600, 200)

def draw():
    screen.fill((10, 10, 40))
    screen.draw.text("Space scene", (10, 10), color="white", fontsize=24)
    alien.draw()
    rocket.draw()

def update():
    alien.x += 1
    if alien.x > WIDTH:
        alien.x = 0
```

**Mod 1:** Change the background to a different RGB colour. Write the new tuple here: `(_____, _____, _____)`

**Mod 2:** Make the rocket move *upwards*. Which line did you add or change?
```python
# answer:

```

**Mod 3:** Make the alien move *twice as fast*. New line?
```python
# answer:

```

**Mod 4:** Make the rocket wrap to the bottom when it leaves the top. Pseudocode this first:
```
IF rocket.y < 0 THEN
    ____________________
ENDIF
```
Now write the Python: ________________________________________

##### Part 3: Design Your Own Scene
On the grid below, sketch a scene with:
- At least **2 Actors** (any sprite from `images/`)
- At least **1 drawn shape** (`filled_rect`, `filled_circle`, or `line`)
- At least **1 piece of text** (e.g., a title)
- At least **1 thing that moves** (in `update()`)

```
+-------------------------------------------------+
|                                                 |
|                                                 |
|                                                 |
|                                                 |
|                                                 |
|                                                 |
|                                                 |
+-------------------------------------------------+
```

Now turn the sketch into code:
```python
# my_scene.py — run with:  pgzrun my_scene.py
WIDTH = ____
HEIGHT = ____

# actors

# draw

# update

```

##### Reflection
1. Pygame Zero calls `draw()` and `update()` for you about 60 times every second. What goes in each?

   draw → ____________________________________________________
   update → __________________________________________________

2. Why do we need an `images/` folder, and why must filenames be lowercase?

   _____________________________________________________________________

3. What was the trickiest thing about getting `pgzrun` to work? How did you fix it?

   _____________________________________________________________________

##### Bonus / Stretch Challenge
Make an Actor **bounce** off all four edges of the window. (Hint: store `vx` and `vy` as module variables; flip their sign when the Actor hits an edge.)

```python
# starter:
ball = Actor("coin")
ball.pos = (200, 200)
vx = 3
vy = 2
# fill in update() ...
```

---

### Session 41: Pygame Zero — Input & Collisions

---

#### SESSION 41 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 41 of 48 |
| **Title** | Pygame Zero — Input & Collisions |
| **Unit** | Unit 7: OOP & Game Mini-Project |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced |
| **Cambridge Alignment** | 0478 §10 program development; 9618 awareness — event-driven programming; Lower Secondary Computing 0860 — interactive artefacts |
| **Singapore Alignment** | O-Level Computing 7155 §3 software development (input handling, debugging); 21CC creative thinking |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Move** an Actor with all four arrow keys by reading from the `keyboard` object inside `update()`.
2. **Implement** the `on_mouse_down(pos)` event handler so a mouse click produces a visible response on screen.
3. **Detect** collision between two Actors using `actor.colliderect(other)` and trigger a state change (e.g., score increase, sprite reposition).
4. **Classify** at least 5 statements as belonging to *input*, *update*, or *draw* with 80% accuracy on the worksheet sorting task.

##### Materials Needed
- Thonny + Python 3.11+
- Pygame Zero installed
- `images/` folder (carry over from Session 40) plus a new `coin.png` and `player.png` if not present
- Printed worksheets
- Projector

##### Procedure

**0–5 min: Warm-Up — "Three Things"**
On the board:
```
INPUT  →  UPDATE  →  DRAW
```
*"Every game does these three things, in this order, 60 times a second. Yesterday we did UPDATE and DRAW. Today: INPUT."*

**5–15 min: Introduction — The `keyboard` Object**

```python
WIDTH = 600
HEIGHT = 400

player = Actor("player")
player.pos = (300, 200)
SPEED = 4

def draw():
    screen.fill("forestgreen")
    player.draw()

def update():
    if keyboard.left:
        player.x -= SPEED
    if keyboard.right:
        player.x += SPEED
    if keyboard.up:
        player.y -= SPEED
    if keyboard.down:
        player.y += SPEED
```

Run with `pgzrun player_move.py`. Hold arrow keys; the player moves. Release; it stops.

Notes to flag:
- `keyboard.left`, `keyboard.right`, `keyboard.up`, `keyboard.down` are **booleans**. They tell you "is this key currently held down?"
- Other useful ones: `keyboard.space`, `keyboard.a`, `keyboard.escape`.
- We use `if` (not `elif`) for each direction, so diagonal movement works (left + up).
- In Pygame Zero, **screen Y increases downward.** `up` decreases `y`.

Add **edge clamping** so the player can't fly off:

```python
def update():
    if keyboard.left:  player.x -= SPEED
    if keyboard.right: player.x += SPEED
    if keyboard.up:    player.y -= SPEED
    if keyboard.down:  player.y += SPEED

    # Keep on screen
    if player.left < 0: player.left = 0
    if player.right > WIDTH: player.right = WIDTH
    if player.top < 0: player.top = 0
    if player.bottom > HEIGHT: player.bottom = HEIGHT
```

`actor.left`, `.right`, `.top`, `.bottom` are convenient: they reference the edges of the sprite's bounding box.

**Mouse input:**

```python
clicks = []

def draw():
    screen.fill("midnightblue")
    for c in clicks:
        screen.draw.filled_circle(c, 10, "yellow")
    screen.draw.text(f"Clicks: {len(clicks)}", (10, 10), color="white", fontsize=24)

def on_mouse_down(pos):
    clicks.append(pos)
```

`on_mouse_down(pos)` is another **special function** Pygame Zero calls whenever the mouse is pressed. `pos` is an `(x, y)` tuple.

**15–35 min: Guided Practice — "Catch the Coin"**

Build the prototype together:

```python
import random

WIDTH = 600
HEIGHT = 400
SPEED = 4

player = Actor("player")
player.pos = (300, 350)

coin = Actor("coin")
coin.pos = (random.randint(40, WIDTH - 40), random.randint(40, 200))

score = 0

def draw():
    screen.fill((20, 60, 20))
    player.draw()
    coin.draw()
    screen.draw.text(f"Score: {score}", (10, 10), color="white", fontsize=28)

def update():
    global score

    # ---- INPUT ----
    if keyboard.left:  player.x -= SPEED
    if keyboard.right: player.x += SPEED
    if keyboard.up:    player.y -= SPEED
    if keyboard.down:  player.y += SPEED

    # Clamp
    if player.left < 0: player.left = 0
    if player.right > WIDTH: player.right = WIDTH
    if player.top < 0: player.top = 0
    if player.bottom > HEIGHT: player.bottom = HEIGHT

    # ---- COLLISION ----
    if player.colliderect(coin):
        score += 1
        coin.x = random.randint(40, WIDTH - 40)
        coin.y = random.randint(40, HEIGHT - 40)
```

Notice the comments **INPUT** / **COLLISION**. They are not required, but they teach the model: input → update → draw.

`actor.colliderect(other)` is a **method** — call back to OOP. It returns a boolean. That's it.

Add a tiny on-screen prompt:

```python
def draw():
    screen.fill((20, 60, 20))
    player.draw()
    coin.draw()
    screen.draw.text(f"Score: {score}", (10, 10), color="white", fontsize=28)
    screen.draw.text("Arrow keys to move", (10, HEIGHT - 30), color="white", fontsize=18)
```

**Multi-coin variant** (foreshadows the project):

```python
import random

WIDTH = 600
HEIGHT = 400
SPEED = 4

player = Actor("player", (300, 350))

coins = []
for _ in range(5):
    c = Actor("coin", (random.randint(40, WIDTH - 40),
                       random.randint(40, HEIGHT - 100)))
    coins.append(c)

score = 0

def draw():
    screen.fill((10, 30, 10))
    player.draw()
    for c in coins:
        c.draw()
    screen.draw.text(f"Score: {score}/5", (10, 10), color="white", fontsize=28)
    if not coins:
        screen.draw.text("YOU WIN!", (220, 180), color="yellow", fontsize=48)

def update():
    global score
    if keyboard.left:  player.x -= SPEED
    if keyboard.right: player.x += SPEED
    if keyboard.up:    player.y -= SPEED
    if keyboard.down:  player.y += SPEED

    for c in coins[:]:               # iterate over a COPY because we mutate
        if player.colliderect(c):
            coins.remove(c)
            score += 1
```

The slice copy `coins[:]` is a teachable moment: *"Don't modify a list while you're iterating over it."*

**Sorting activity (whole class):**
Write five lines on the board and ask: input, update, or draw?
1. `if keyboard.space: player.y -= 5` → **input/update** (it reads keyboard inside update — input feels nested inside update in Pygame Zero, that's fine)
2. `screen.fill("black")` → **draw**
3. `if player.colliderect(coin): score += 1` → **update**
4. `screen.draw.text("Score:", (10, 10), color="white")` → **draw**
5. `coin.x = random.randint(0, WIDTH)` → **update**

**35–50 min: Independent Practice — Worksheet**
Students:
- Implement keyboard controls on a starter file (Part 1).
- Design a 3-object collision scene on paper (Part 2).
- Sort a list of statements into draw/update buckets (Part 3).

**50–55 min: Sharing & Discussion**
Two volunteers demo their working "catch" prototype. Ask: *"Whose game has the trickiest control feel? What did you change?"* Possible answers: speed, edge clamping, multiple coins.

**55–60 min: Closure & Preview**
Exit ticket: *"What method tells two Actors they have collided?"* (`colliderect`). Preview Session 42: *"Tomorrow: design and build your own arcade game. Bring an idea!"*

##### Differentiation
**Support:** Provide a `controls_starter.py` with the player Actor pre-positioned and the coin Actor pre-spawned; learner only fills in the four `if keyboard.<dir>:` lines. Tape arrow-key reminders to the keyboard.
**Extension:** Add a second player controlled by `WASD`. Or use `keyboard.space` to fire a "bullet" Actor that moves up the screen and despawns at the top.

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Advanced (4) |
|-----------|---------------|----------------|----------------|--------------|
| Keyboard controls | One direction works | Two directions | All four directions + clamping | All four + diagonal smooth + speed constant |
| Mouse / event handler | Not implemented | Implemented but no visible result | `on_mouse_down` produces visible feedback | + maintains state across clicks |
| Collisions | `colliderect` not used | Detected but no response | Detection + state change (e.g., score) | Detection + multi-object iteration |
| Loop sorting (input/update/draw) | <50% correct | 50–79% | 80–95% | 100% + justifies each |

##### Teacher Notes
- The **"copy the list"** pattern (`for c in coins[:]:`) is a real-world bug that bites professional developers. Make a small fuss about it.
- Y-axis confusion is common — *"up" decreases y* — repeat at least twice.
- Some keyboards have sticky modifier keys; if a student claims `keyboard.left` doesn't work, swap keyboards before debugging code.
- Pygame Zero has more events: `on_key_down`, `on_key_up`, `on_mouse_move`. Mention only — keep today on `keyboard.<key>` and `on_mouse_down`.
- If a student wants to play sound on collision, you may preview `sounds.coin.play()` — but the full demo is reserved for Session 42.
- Encourage students to save their "catch the coin" file — it's a perfect base for tomorrow's project.

---

#### SESSION 41 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Implement Keyboard Controls
You are given the starter below. Save it as `move_me.py` next to your `images/` folder and run with `pgzrun move_me.py`. Right now, the player does not move. Make it move.

```python
WIDTH = 600
HEIGHT = 400
SPEED = 5

player = Actor("player")
player.pos = (WIDTH / 2, HEIGHT / 2)

def draw():
    screen.fill("teal")
    player.draw()

def update():
    # TODO: read keyboard.left, .right, .up, .down and move the player
    pass
```

**Task 1a:** Add the four `if keyboard.<dir>:` lines.

**Task 1b:** Stop the player from going off-screen. Which 4 lines did you add?
```python
# answer:




```

**Task 1c:** Add an `on_mouse_down(pos)` handler that **teleports** the player to the mouse position. (Hint: `player.pos = pos`.)
```python
# answer:

```

##### Part 2: Design a 3-Object Collision Scene
On paper, design a Pygame Zero scene with **three** Actors that interact through collisions. Examples:
- Player + coin + bomb (coin = +score, bomb = game over)
- Hero + treasure + dragon
- Cat + mouse + cheese

**My three objects:**
1. ____________________ (controlled by? ___________________)
2. ____________________
3. ____________________

**Collision table** — what happens when each pair collides?

| Pair | What happens? |
|------|---------------|
| 1 ↔ 2 | _______________________________________ |
| 1 ↔ 3 | _______________________________________ |
| 2 ↔ 3 | _______________________________________ |

**Pseudocode** for the `update()` function (no Python yet):

```
IF keyboard.left THEN move object 1 left
...
IF object 1 collides with object 2 THEN ...
IF object 1 collides with object 3 THEN ...
```

##### Part 3: Sort — `update()` or `draw()`?
Place each statement in the correct column by writing **U** (update) or **D** (draw) beside it.

| # | Statement | U / D |
|---|-----------|-------|
| 1 | `screen.fill("black")` | ____ |
| 2 | `player.x += 4` | ____ |
| 3 | `screen.draw.text("Hi", (10, 10), color="white")` | ____ |
| 4 | `if keyboard.space: bullet.y -= 6` | ____ |
| 5 | `coin.draw()` | ____ |
| 6 | `if player.colliderect(coin): score += 1` | ____ |
| 7 | `screen.draw.filled_rect(Rect((0,0),(50,50)), "red")` | ____ |
| 8 | `if player.x > WIDTH: player.x = 0` | ____ |

**Score: ____ / 8**

##### Reflection
1. Why do we use `if` (not `elif`) for the four arrow-key checks?

   _____________________________________________________________________

2. What does `actor.colliderect(other)` return? How is it used inside `if`?

   _____________________________________________________________________

3. In Pygame Zero's coordinate system, "up" makes `y` *decrease*. Why might that surprise someone learning maths in school?

   _____________________________________________________________________

##### Bonus / Stretch Challenge
Add a second player controlled by `WASD` to your `move_me.py`. When the two players collide with each other, swap their positions! (Hint: use a temporary tuple.)

```python
# tip:
if player1.colliderect(player2):
    p1_pos = player1.pos
    player1.pos = player2.pos
    player2.pos = p1_pos
```

---

### Session 42: Project 7 — Mini Arcade Game

---

#### SESSION 42 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 42 of 48 |
| **Title** | Project 7 — Mini Arcade Game (OOP + Pygame Zero) |
| **Unit** | Unit 7: OOP & Game Mini-Project |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced |
| **Cambridge Alignment** | 0478 §10 programming concepts (problem-solving project); 9618 awareness — software development life-cycle; Lower Secondary Computing 0860 — designing & evaluating digital artefacts |
| **Singapore Alignment** | O-Level Computing 7155 §3 software development (full SDLC mini-project); 21CC creative & critical thinking, communication; EdTech Masterplan creation pillar |

##### Learning Objectives (SMART)
By the end of this session, students will be able to:
1. **Plan** their game by producing pseudocode, a flowchart, and a list of classes/Actors before any code is written.
2. **Build** a working arcade game with at least one player Actor, one or more enemy/target Actors, a score, lives, and a "game over" state.
3. **Apply** OOP by defining at least one `class` (e.g., `Player` or `Enemy`) used inside the game.
4. **Playtest** a peer's game using the rubric and provide one strength + one improvement in writing.

##### Materials Needed
- Thonny + Python 3.11+
- Pygame Zero installed
- `images/` folder with project sprites (player, coin, asteroid, fruit, etc.)
- `sounds/` folder with at least one short `.wav` or `.ogg` (e.g., `coin.wav`)
- Printed project planning template + asset checklist + build checklist + peer-playtest rubric (worksheet)
- Projector for the closing showcase

##### Procedure

**0–5 min: Warm-Up — "Pitch Your Game in 30 Seconds"**
Round-robin: each student gives a one-sentence pitch ("It's a frog dodging trucks on a highway"). No silence allowed — if stuck, pick a template.

**5–15 min: The Three Templates (pick one)**

**Template A — Catch the Falling Fruit**
- Player at the bottom moves left/right.
- Fruit Actors fall from the top.
- Catch a fruit → +1 score. Miss it (it hits the floor) → -1 life. 3 lives → game over.

**Template B — Dodge the Asteroids**
- Spaceship moves anywhere.
- Asteroid Actors spawn at the top and fall.
- Survive as long as you can. Score = seconds survived. Hit by asteroid → game over.

**Template C — Maze Chase**
- Player navigates a static maze (drawn with `filled_rect` walls).
- A coin spawns at a random non-wall spot. Reach it → +1 score, respawn elsewhere.
- Optional enemy Actor patrols and ends the game on collision.

Project a **scaffold** (Template A example) for students to fork:

```python
# fruit_catcher.py — run with: pgzrun fruit_catcher.py
import random

WIDTH = 600
HEIGHT = 480

# ---- Classes ----
class Player:
    def __init__(self):
        self.actor = Actor("player", (WIDTH / 2, HEIGHT - 40))
        self.speed = 5

    def update(self):
        if keyboard.left:  self.actor.x -= self.speed
        if keyboard.right: self.actor.x += self.speed
        if self.actor.left < 0: self.actor.left = 0
        if self.actor.right > WIDTH: self.actor.right = WIDTH

    def draw(self):
        self.actor.draw()


class Fruit:
    def __init__(self):
        self.actor = Actor("apple", (random.randint(20, WIDTH - 20), -20))
        self.speed = random.randint(2, 5)

    def update(self):
        self.actor.y += self.speed

    def draw(self):
        self.actor.draw()

    def off_screen(self):
        return self.actor.top > HEIGHT

# ---- Game state ----
player = Player()
fruits = []
score = 0
lives = 3
game_over = False
spawn_timer = 0

def draw():
    screen.fill((20, 30, 50))
    player.draw()
    for f in fruits:
        f.draw()
    screen.draw.text(f"Score: {score}", (10, 10), color="white", fontsize=28)
    screen.draw.text(f"Lives: {lives}", (WIDTH - 120, 10), color="white", fontsize=28)
    if game_over:
        screen.draw.text("GAME OVER", (WIDTH / 2 - 130, HEIGHT / 2 - 40),
                         color="yellow", fontsize=64)
        screen.draw.text(f"Final score: {score}", (WIDTH / 2 - 100, HEIGHT / 2 + 20),
                         color="white", fontsize=32)

def update():
    global score, lives, game_over, spawn_timer
    if game_over:
        return

    player.update()

    # spawn a fruit roughly every 40 frames
    spawn_timer += 1
    if spawn_timer >= 40:
        fruits.append(Fruit())
        spawn_timer = 0

    for f in fruits[:]:
        f.update()

        # caught?
        if f.actor.colliderect(player.actor):
            score += 1
            sounds.coin.play()       # needs sounds/coin.wav (or .ogg)
            fruits.remove(f)
            continue

        # missed?
        if f.off_screen():
            lives -= 1
            fruits.remove(f)
            if lives <= 0:
                game_over = True

def on_key_down(key):
    global score, lives, game_over, fruits, spawn_timer
    if game_over and key == keys.R:
        score = 0
        lives = 3
        fruits = []
        spawn_timer = 0
        game_over = False
```

Highlights to discuss:
- The `Player` and `Fruit` classes wrap an `Actor` — that's **composition**.
- Each class has its own `update()` and `draw()` — the global `update()`/`draw()` just delegates.
- `sounds.coin.play()` — Pygame Zero looks for `sounds/coin.wav` (or `.ogg`).
- `on_key_down(key)` + `keys.R` — restart on R press.
- `for f in fruits[:]:` — copy-the-list trick from Session 41.

**Stretch features (board them at the front):**
- **Difficulty scaling:** decrease `spawn_timer` threshold every 10 score points.
- **High-score persistence:** read/write `highscore.txt` (Unit 6 callback).

```python
# at startup
try:
    with open("highscore.txt", "r") as f:
        highscore = int(f.read())
except (FileNotFoundError, ValueError):
    highscore = 0

# on game over (only once):
if score > highscore:
    highscore = score
    with open("highscore.txt", "w") as f:
        f.write(str(highscore))
```

**15–25 min: Plan First (no code yet!)**
Students fill in **Part 1** of the worksheet: pseudocode, flowchart, class list, asset checklist. Teacher circulates approving plans. *No coding without an approved plan.*

**25–50 min: Build**
Students code. Teacher coaches one-on-one. Common rescues:
- "Image not found" → check `images/` and lowercase filename.
- "Sound silent" → check `sounds/coin.wav` exists; some systems prefer `.ogg`.
- Sprites tunnel through walls → simplistic clamping, fine for today.

Encourage MVP first, polish second:
1. Player moves.
2. Enemy/target spawns.
3. Collision works.
4. Score on screen.
5. Game over screen.
6. *Then* add sound, scaling, persistence.

**50–55 min: Peer Playtest**
Pair up. Each student plays the partner's game for ~2 minutes and fills the rubric in **Part 4** of the worksheet. Required output: one strength + one improvement.

**55–60 min: Showcase & Closure**
Two or three volunteers project their game on the big screen. Teacher names what was good — *"Notice the lives counter, the smooth controls, the restart on R."* Closure question: *"Which OOP idea did your game actually use? How did it help?"*

Preview Unit 8: *"Final unit next session — capstone project where you choose your own adventure across everything we've learnt."*

##### Differentiation
**Support:** Provide the Template A scaffold pre-coded (above). Student modifies sprites, colours, speeds, and adds the score-display text. Counts as full credit.
**Extension:** Implement *all* stretch features (scaling difficulty, high-score file, multiple enemy types). Add a power-up Actor that briefly increases player size. Or implement a `class Game` that owns the entire state (so almost no globals).

##### Assessment Criteria

| Criterion | Beginning (1) | Developing (2) | Proficient (3) | Advanced (4) |
|-----------|---------------|----------------|----------------|--------------|
| Planning artefact | No plan | Pseudocode only | Pseudocode + flowchart + class list | + asset checklist + risk notes |
| Game runs & is playable | Crashes | Runs but unplayable | Runs, has score, ends cleanly | Runs + difficulty + restart |
| OOP usage | No class | Class defined but unused | ≥1 class with attributes + methods used in main loop | ≥2 classes, clear responsibilities, `__str__` or similar |
| Polish & feedback | Skipped peer review | Filled rubric vaguely | Strength + improvement noted | Improvement implemented in build |

##### Teacher Notes
- **Time pressure is real** — 25 minutes of build is tight. Insist on MVP first; stretch later.
- The **scaffold** above is intentionally complete enough for support students to ship. Don't withhold it; learning OOP from a worked example is fine.
- Students will want to use sprites from the internet — only allow CC0 / Kenney / pre-cleared. A 60-second licence chat is healthy.
- Watch for `global` overuse. If a student adds 10 globals, point at the scaffold's `Player` class and ask "could a class own this?"
- Sounds can crash some systems if missing. Wrap `sounds.coin.play()` in a `try`/`except` if your lab is flaky:
  ```python
  try: sounds.coin.play()
  except Exception: pass
  ```
- For peer review, set a hard 2-minute play timer. Otherwise students drift.
- Save a `solutions/` folder with all three templates fully completed for students who want to study after class.

---

#### SESSION 42 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

##### Part 1: Project Planning

**1a. My template (circle one):**   A — Catch Fruit   /   B — Dodge Asteroids   /   C — Maze Chase   /   D — Other: ______________

**1b. One-sentence game pitch:**
_____________________________________________________________________

**1c. Pseudocode for the main loop:**
```
LOOP every frame:
    READ keyboard
    UPDATE player position
    UPDATE _________________________________________
    IF player collides with _______________ THEN _______________
    IF ______________________________________ THEN game_over = True
    DRAW background
    DRAW _________________________________________
    DRAW score, lives
    IF game_over THEN DRAW "GAME OVER"
ENDLOOP
```

**1d. Flowchart** — sketch the flow from "frame start" through input → update → collisions → draw → next frame, with at least ONE decision diamond:

```
( frame start )
      │
      ▼
[ read input ]
      │
      ▼
[ update positions ]
      │
      ▼
   ◇ collision?
   │     │
  YES    NO
   │     │
   ▼     ▼
 [...] [...]
      │
      ▼
   [ draw ]
      │
      ▼
( next frame )
```

(Re-draw / annotate to fit your game.)

**1e. Class list:**

| Class name | Attributes | Methods |
|------------|------------|---------|
| ____________ | _________________________ | _________________________ |
| ____________ | _________________________ | _________________________ |

##### Part 2: Asset Checklist
Tick each as you obtain it. All assets must be CC0 or pre-cleared (Kenney.nl recommended).

| # | Asset | File path | Got it? |
|---|-------|-----------|---------|
| 1 | Player sprite | `images/_____________.png` | ☐ |
| 2 | Target / enemy sprite | `images/_____________.png` | ☐ |
| 3 | (Optional) extra sprite | `images/_____________.png` | ☐ |
| 4 | Pickup / hit sound | `sounds/_____________.wav` (or `.ogg`) | ☐ |
| 5 | (Optional) game-over sound | `sounds/_____________.wav` | ☐ |

##### Part 3: Build Checklist
Tick when each milestone is on screen and working.

- [ ] Window opens at correct `WIDTH` × `HEIGHT`
- [ ] Background is filled (not black-by-accident)
- [ ] Player sprite appears
- [ ] Player moves with arrow keys
- [ ] Player cannot leave the screen
- [ ] Target / enemy spawns (random position)
- [ ] At least one **class** is defined
- [ ] At least one **method** is called in `update()` or `draw()`
- [ ] Collision detected with `colliderect`
- [ ] Score visible on screen, increments on collision
- [ ] Lives visible on screen, decrements appropriately
- [ ] Game-over state stops gameplay and shows "GAME OVER"
- [ ] At least one sound plays on a key event (e.g., score)
- [ ] (Stretch) Difficulty scales with score
- [ ] (Stretch) High-score saved to `highscore.txt`
- [ ] (Stretch) Restart key (e.g., R) works

##### Part 4: Peer Playtest Rubric
Swap with a partner. Play their game for **2 minutes**. Fill in honestly and kindly.

**Game I tested:** ____________________________ **By:** ____________________________

| Criterion | 1 | 2 | 3 | 4 | Notes |
|-----------|---|---|---|---|-------|
| Controls feel responsive | ☐ | ☐ | ☐ | ☐ | |
| Goal of the game is clear | ☐ | ☐ | ☐ | ☐ | |
| Score / lives display works | ☐ | ☐ | ☐ | ☐ | |
| Game-over state is satisfying | ☐ | ☐ | ☐ | ☐ | |
| Visual / audio polish | ☐ | ☐ | ☐ | ☐ | |

**One thing that works really well:**
_____________________________________________________________________

**One concrete improvement (not "make it better" — be specific):**
_____________________________________________________________________

##### Reflection
1. Which OOP idea did you actually use today (class, attribute, method)? How did it make your game easier to build?

   _____________________________________________________________________

2. What was the most frustrating bug, and how did you eventually fix it?

   _____________________________________________________________________

3. If you had another 60 minutes on this game, what is the **single most important** thing you'd add — and why?

   _____________________________________________________________________

##### Bonus / Stretch Challenge
Implement **two** of the stretch features end-to-end:
- Difficulty scaling that visibly changes the game after every 10 points.
- High-score persistence using `highscore.txt` (Unit 6 file I/O).
- A `class Enemy` distinct from your target/fruit class, with at least one method.
- A two-player mode (`WASD` for player 2).

Write a one-paragraph explanation of how your chosen feature(s) work, naming at least one specific Pygame Zero or OOP concept used.

_____________________________________________________________________
_____________________________________________________________________
_____________________________________________________________________

---
