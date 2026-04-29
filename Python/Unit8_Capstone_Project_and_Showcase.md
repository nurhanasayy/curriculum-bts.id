# Python Programming for Kids: Lesson Plans & Worksheets
## Unit 8: Capstone Project & Showcase (Sessions 43–48)

### Unit Overview

Unit 8 is the synthesis arc of the 48-session course: across six 60-minute sessions students plan, build, test, debug, polish, and present a capstone project of their own choosing. Three project tracks are offered — a **Console Application** (interactive, data-driven), a **Turtle Art / Visualization** piece (generative art or data visualizer), or a **Pygame Zero Game** (an extension of the Unit 7 game with multiple levels, persistent scores, and polished UI) — and students may also propose an original idea with instructor approval. The unit deliberately models the **iterative development cycle** (CSTA 2-AP-16) and **systematic testing with normal, boundary, and invalid data** (CSTA 2-AP-17, Cambridge 0478 §10.1, O-Level 7155 Module 4), so the worksheets in this unit are themselves the project artefacts: a design document, build log, polish checklist, test plan + trace table, code review, refactor log, peer feedback form, and a course reflection. Assessment is based on a five-criterion **Capstone Rubric** (Functionality, Code Quality, Algorithm Design, Creativity & Originality, Presentation) applied at three checkpoints — Session 43 (design), Session 46 (testing), and Session 48 (final showcase). The unit closes with a public **Showcase**, where each student delivers a 3-minute demo plus 2-minute Q&A, receives written peer feedback, and reflects on next steps (Cambridge IGCSE 0478, Singapore O-Level 7155, or a chosen library/framework). Replit is introduced alongside Thonny as the sharing platform for showcase day so families and remote audiences can run the projects in a browser. Successful completion of Unit 8 earns students a **Certificate of Completion** for the 48-session Intermediate Python course.

---

### Session 43: Capstone Planning & Design Document

---

#### SESSION 43 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 43 of 48 |
| **Title** | Capstone Planning & Design Document |
| **Unit** | Unit 8: Capstone Project & Showcase |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced (synthesis) |
| **Cambridge Alignment** | Lower Secondary Computing 0860 strand "Programming" (decomposition, abstraction); IGCSE 0478 §7 Algorithm design and problem-solving (decomposition, top-down design, structure diagrams), §8 Programming (programming concepts), §10.1 Programming as it leads to designed solutions |
| **Singapore Alignment** | O-Level Computing 7155 Module 1 (Abstraction & Algorithms), Module 2 (Programming) — design before code; 21CC creative thinking, self-directed learning |

##### Learning Objectives (SMART)

By the end of this session, students will be able to:

1. **Choose** one of three capstone tracks (Console App, Turtle Art, Pygame Zero Game) — or propose an approved original idea — and justify the choice with a one-paragraph problem statement that names a target user.
2. **Decompose** their chosen idea into an MVP feature list (3–5 must-haves) and a stretch list (3+ nice-to-haves), using vocabulary from Unit 5 (functions) and Unit 7 (classes) where relevant.
3. **Produce** at least three design artefacts — a flowchart sketch of the main flow, a function decomposition listing 5+ functions with one-line descriptions, and a testing plan with at least three sample test cases (normal / boundary / invalid).
4. **Critique** a peer's design document using the Design Review checklist, giving one specific strength and one specific suggestion.

##### Materials Needed

- Thonny (Python 3.11+) installed
- One sheet of plain A4 / printer paper per student for the flowchart sketch
- Pens, pencils, coloured pens
- Printed Capstone Design Document worksheet (this session)
- Printed Capstone Rubric (one per student, kept in folder for the rest of the unit)
- Whiteboard / projector for the three project track gallery
- Optional: example design documents from prior cohorts (anonymised)

##### Procedure

**0–5 min: Warm-Up — "What problem do you want to solve?"**
Pose the question on the board. Each student writes one sentence on a sticky note: "Something I wish a computer would do for me, my friends, or my class." Stick notes on the wall and read 4–5 aloud. This primes problem-statement thinking before they pick a track.

**5–15 min: Introduction / Mini-Lesson — Three Tracks and the MVP Mindset**
Walk through the three project tracks on the projector with one tiny example of each:

- **Console App (data-driven)** — quiz bank, study planner, library catalogue, recipe finder, mini banking app. Likely uses: input/print, lists, dicts, functions, file I/O (Unit 6), maybe one class.
- **Turtle Art / Visualization** — fractal explorer, generative tree, spirograph, simple bar-chart from a CSV. Likely uses: functions, loops, recursion (light), turtle module.
- **Pygame Zero Game** — a polished extension of the Unit 7 platformer/shooter/maze with multiple levels, a high-score file, and a title screen.

Then introduce the **MVP Mindset**: "Build the skeleton first, polish never." Show the diagram:

```
IDEA  ->  MVP (must-haves)  ->  Stretch (nice-to-haves)  ->  Polish
                 |
                 +--- this is what you must finish in Session 44.
```

State the scope rule clearly: **MVP must be achievable in one session of focused work (≈40 min in Session 44).** If a feature can't be built in 10 minutes, it's probably not MVP.

Briefly review the Capstone Rubric (the same one used at Sessions 43, 46, 48). Tell students it will be applied today to their *design*, in Session 46 to *testing*, and in Session 48 to the *finished project*.

**15–50 min: Independent / Studio Work — Fill the Design Document**
Students complete the worksheet in this order:

1. Title + chosen track (2 min)
2. Problem statement + target user (5 min)
3. MVP feature list (5 min)
4. Stretch features (3 min)
5. Data model — what variables, lists, dicts, files, classes (5 min)
6. Pseudocode of the main flow (7 min)
7. Flowchart sketch on plain paper (5 min)
8. Function decomposition table (5 min)
9. Testing plan — three sample test cases (3 min)

Instructor circulates and "scope-trims" — the most common intervention is to push a stretch feature *out* of the MVP list. Sample line: "I love that idea. Put it in *Stretch* — I want you to finish core gameplay first."

**50–55 min: Sharing & Discussion — Pair Design Review**
Pair students up. Each gets 2 minutes to walk their partner through the document. The partner uses the Design Review checklist (on the worksheet) and writes one **strength** and one **suggestion**. Switch.

**55–60 min: Closure & Preview**
Whole-class share-out: 3–4 students name their project in one sentence. Preview Session 44: "Bring this design document. We build the MVP — every must-have feature gets shipped."
Homework: students may sketch additional flowchart panels or research one library/function they'll need.

##### Differentiation

**Support:**
- Provide a "design document fill-in" version with the data model and function decomposition partially scaffolded for one of the three tracks (e.g., a quiz-bank console app skeleton).
- Pair with a peer for the flowchart step.
- Allow the student to pick a *smaller* version of an existing example (e.g., extend the Unit 7 game rather than start fresh).

**Extension:**
- Require an **original** project (not from the example list) approved by instructor.
- Add a non-functional requirement: the project must read from a CSV or JSON file, OR must use a class hierarchy, OR must include recursion.
- Ask the student to draft a **structure diagram** in addition to the flowchart, showing top-down decomposition into modules.

##### Assessment Criteria (Full Capstone Rubric — applied to the design document only)

| Criterion | Excellent (4) | Good (3) | Satisfactory (2) | Needs Improvement (1) |
|-----------|---------------|----------|------------------|----------------------|
| Functionality | All features work; handles edge cases | All core features work; minor edge-case gaps | Core features work with bugs | Major features missing |
| Code Quality | Modular, well-named, commented; uses functions and OOP appropriately | Mostly modular and clear | Some structure, some duplication | Monolithic, unclear, no comments |
| Algorithm Design | Pseudocode/flowchart matches code; trace table verifies behaviour | Design artefacts present and mostly accurate | Design artefacts present but partial | No design artefacts |
| Creativity & Originality | Original concept with personal flair | Personalised standard concept | Standard concept | Direct copy of example |
| Presentation | Clear demo, articulates design choices, handles questions | Clear demo with minor gaps | Demo runs but explanation thin | Cannot demo or explain |

> Session 43 emphasises **Algorithm Design** (the design artefacts) and **Creativity & Originality** (the chosen concept). Functionality, Code Quality, and Presentation are placeholder columns at this stage and will be revisited in Sessions 46 and 48.

##### Teacher Notes

- The single biggest pitfall is *scope creep*. Be ruthless: enforce that MVP = "I could finish this in one focused 40-minute session." If a student lists 10 must-haves, mark seven as Stretch.
- Watch for students who pick a track because their friend did. Encourage one minute of "Why this project, why this user?"
- Don't allow a student to skip the flowchart because "I'll just code it." The flowchart is the artefact that makes Session 46's trace table possible.
- If a student wants to do an original project (game-engine port, AI chatbot, web scraper), say yes only if the MVP fits in 40 minutes of build time.
- Save photos of the flowcharts. They're useful evidence for showcase day.

---

#### SESSION 43 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

---

### Part A — Project Identification

**Project Title (be specific, not "My Game"):**

____________________________________________________________________

**Track (circle one):**

&nbsp; &nbsp; CONSOLE APP &nbsp; / &nbsp; TURTLE ART &nbsp; / &nbsp; PYGAME ZERO GAME &nbsp; / &nbsp; ORIGINAL (instructor-approved)

**Original-track approval signature (instructor):** ____________________

---

### Part B — Problem Statement & Target User

**1. In 2–4 sentences, what problem does your project solve, or what experience does it create?**

____________________________________________________________________

____________________________________________________________________

____________________________________________________________________

____________________________________________________________________

**2. Who is the target user? Be specific. ("My 8-year-old brother who is learning multiplication" beats "kids".)**

____________________________________________________________________

____________________________________________________________________

**3. What will the user *do* with your project? Describe their first 30 seconds.**

____________________________________________________________________

____________________________________________________________________

---

### Part C — MVP Feature List (3–5 must-haves)

These are the features that, if missing, the project is broken. Aim for 3–5.

| # | MVP Feature | Why is this a must-have? |
|---|-------------|--------------------------|
| 1 | ____________________________________ | ____________________________________ |
| 2 | ____________________________________ | ____________________________________ |
| 3 | ____________________________________ | ____________________________________ |
| 4 | ____________________________________ | ____________________________________ |
| 5 | ____________________________________ | ____________________________________ |

---

### Part D — Stretch Features (3+ nice-to-haves)

These are features you'd *love* to add if time allows after Session 44.

| # | Stretch Feature | What unit/skill does this draw on? |
|---|-----------------|------------------------------------|
| 1 | ____________________________________ | ____________________________________ |
| 2 | ____________________________________ | ____________________________________ |
| 3 | ____________________________________ | ____________________________________ |
| 4 | ____________________________________ | ____________________________________ |
| 5 | ____________________________________ | ____________________________________ |

---

### Part E — Data Model

What data does your program hold? List every variable, list, dict, file, or class you expect.

| Name | Type (variable / list / dict / set / file / class) | What it stores | Example value |
|------|----------------------------------------------------|----------------|---------------|
| ______________ | ______________ | ______________ | ______________ |
| ______________ | ______________ | ______________ | ______________ |
| ______________ | ______________ | ______________ | ______________ |
| ______________ | ______________ | ______________ | ______________ |
| ______________ | ______________ | ______________ | ______________ |
| ______________ | ______________ | ______________ | ______________ |
| ______________ | ______________ | ______________ | ______________ |
| ______________ | ______________ | ______________ | ______________ |

---

### Part F — Pseudocode of the Main Flow

Write the **main loop / main flow** in pseudocode. No Python syntax — just steps. 8–15 lines.

```
START
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
  ____________________________________________________
END
```

---

### Part G — Flowchart Sketch

Sketch the flowchart for the main flow on a separate sheet of plain paper. Use the standard symbols:

- **Oval** for START / END
- **Rectangle** for a process step
- **Parallelogram** for input/output
- **Diamond** for a decision

> Staple the sketch to this worksheet. Tick the box once attached: ☐

---

### Part H — Function Decomposition (5+ functions)

Plan the functions you will write. Name them in `snake_case`. One-sentence descriptions.

| # | Function name (snake_case) | Inputs (parameters) | Returns | What it does (one sentence) |
|---|----------------------------|--------------------|---------| --------------------------- |
| 1 | ______________________ | ______________ | ______________ | ______________________________________ |
| 2 | ______________________ | ______________ | ______________ | ______________________________________ |
| 3 | ______________________ | ______________ | ______________ | ______________________________________ |
| 4 | ______________________ | ______________ | ______________ | ______________________________________ |
| 5 | ______________________ | ______________ | ______________ | ______________________________________ |
| 6 | ______________________ | ______________ | ______________ | ______________________________________ |
| 7 | ______________________ | ______________ | ______________ | ______________________________________ |

---

### Part I — Initial Testing Plan (3 cases minimum)

For each test, predict what should happen *before* you build anything.

| # | Test type (normal / boundary / invalid) | Input | Expected output / behaviour |
|---|-----------------------------------------|-------|----------------------------|
| 1 | ______________ | __________________ | __________________________ |
| 2 | ______________ | __________________ | __________________________ |
| 3 | ______________ | __________________ | __________________________ |

---

### Part J — Success Criteria

Write 3 sentences that begin "**My project is successful when…**"

1. ___________________________________________________________________________

2. ___________________________________________________________________________

3. ___________________________________________________________________________

---

### Part K — Pair Design Review (filled in by your partner)

Partner's name: ____________________________________

**Strength I noticed in this design:**

____________________________________________________________________

____________________________________________________________________

**Suggestion for improvement:**

____________________________________________________________________

____________________________________________________________________

**One question I still have about this project:**

____________________________________________________________________

____________________________________________________________________

---

### Part L — Self-Check Before Submitting (tick all)

- ☐ I picked exactly one track (or got original approval)
- ☐ My problem statement names a real user
- ☐ I have 3–5 MVP features and at least 3 stretch features
- ☐ My data model lists everything my program needs to remember
- ☐ My pseudocode reflects the main flow from start to end
- ☐ My flowchart is sketched and stapled
- ☐ I have at least 5 functions named in snake_case
- ☐ I have at least one normal, one boundary, and one invalid test
- ☐ I had a peer review my design

**Instructor sign-off (Session 43 design checkpoint):** ____________________

---

### Session 44: Capstone Build — Core Mechanics

---

#### SESSION 44 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 44 of 48 |
| **Title** | Capstone Build — Core Mechanics (MVP) |
| **Unit** | Unit 8: Capstone Project & Showcase |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced (synthesis) |
| **Cambridge Alignment** | IGCSE 0478 §8 (programming concepts: sequence, selection, iteration, totalling, counting), §10.1 (programming) — full integration; Lower Secondary 0860 "Programming" |
| **Singapore Alignment** | O-Level 7155 Module 2 (Programming — control structures, modular design), Module 4 (Data) where applicable; 21CC self-management |

##### Learning Objectives (SMART)

By the end of this session, students will be able to:

1. **Implement** every MVP feature listed in their Session 43 Design Document, producing a working end-to-end skeleton (no polish required).
2. **Translate** their pseudocode and function decomposition table into Python functions whose names and parameters match the design.
3. **Track** their own progress by completing a Build Log table that records each MVP feature's status (not-started / in-progress / done) and any blockers encountered.
4. **Identify** at least one moment in the build where they encountered a bug, and describe in one sentence what the symptom was and how they (tried to) fix it.

##### Materials Needed

- Thonny (Python 3.11+)
- Their Session 43 Design Document (must be present — no design, no build)
- Printed Build Log worksheet (this session)
- Code-quality checklist printout (in worksheet)
- Optional: starter file template for each track in a shared folder
- For Pygame Zero track: ensure `pgzrun` is installed and a `images/` & `sounds/` folder ready
- For Turtle track: confirm `turtle` works in Thonny on the lab machines

##### Procedure

**0–5 min: Warm-Up — "Tell me your MVP in one sentence."**
Each student says aloud: "My MVP is a [program type] where the user can [verb] and the program will [verb]." Anyone who can't say it in one sentence pulls out their design doc and rewrites the problem statement before opening Thonny.

**5–15 min: Mini-Lesson — Build the Skeleton First, Polish Never**
Project an empty Thonny window. Demonstrate the **skeleton-first pattern** with a tiny console quiz example:

```python
# 1. Define empty functions matching the design.
def load_questions():
    return []

def ask_question(q):
    return False

def show_score(score, total):
    print(f"You scored {score}/{total}")

# 2. Wire main flow. Each function returns a placeholder.
def main():
    questions = load_questions()
    score = 0
    for q in questions:
        if ask_question(q):
            score += 1
    show_score(score, len(questions))

if __name__ == "__main__":
    main()
```

Run it. It does nothing. That's *correct*. The point: **the wiring works before any feature does**.

Walk through the three biggest pitfalls:

1. **The Big-Bang Build** — student writes 200 lines, runs, gets 14 errors. Cure: run after every 5–10 lines.
2. **The Polish Trap** — student spends 25 minutes picking a colour scheme. Cure: polish goes in Session 45.
3. **The Forgotten Design** — student abandons the design doc and improvises. Cure: design doc stays open in another window.

End with the **two-rule constitution** for today:
1. *Run your code at least every 5 minutes.*
2. *Cross a feature off the Build Log the moment it works.*

**15–55 min: Studio Work — Build the MVP**
40 minutes of focused build time. Instructor moves between students with these triage prompts:

- "Show me your design doc — which feature are you on?"
- "What's the smallest version of this that runs?"
- "Have you run it in the last 5 minutes?"
- "Stuck? Paste the error and read it out loud."

Mid-session checkpoint at the 35-minute mark: every student updates the Build Log on screen for the instructor.

**55–60 min: Sharing, Closure & Preview**
Each student says: "I finished features ___, ___, ___ today. I'm stuck on ___ ." Preview Session 45: features and polish. Remind them to bring the Build Log.

##### Differentiation

**Support:**
- Provide a starter `.py` file with empty function stubs already named per the standard track examples.
- Pair-program with a peer at the same scope.
- Reduce MVP from 5 features to 3.
- Allow voice-typing of comments for students who type slowly.

**Extension:**
- Require all functions to have a docstring describing parameters and return value.
- Require at least one class with `__init__` and one method (Unit 7 link).
- Require file I/O (read or write) somewhere in the MVP.

##### Assessment Criteria

| Criterion | Excellent (4) | Good (3) | Satisfactory (2) | Needs Improvement (1) |
|-----------|---------------|----------|------------------|----------------------|
| Skeleton wiring | Every MVP function exists and is called from `main`; runs without error | All functions exist; one wiring gap | Some functions missing | No clear `main` flow |
| Feature progress | All 3–5 MVP features working end-to-end | 3+ features working, 1 partial | 2 features working | 0–1 features working |
| Build Log discipline | Log updated, every feature has status + notes; blockers named | Log mostly complete | Log started but sparse | Log blank or missing |
| Code-design fidelity | Function names + parameters match Session 43 design | Mostly matches design | Some divergence, justified | Code unrelated to design |

##### Teacher Notes

- Walk the room every 5 minutes for the first 20 minutes. Most fires are small if caught early.
- The hardest students are the ones already polishing. Redirect: "Write the function first. Make it pretty in Session 45."
- Encourage students to commit to a **save naming pattern** like `capstone_v1.py`, `capstone_v2.py`. It saves disasters.
- For Pygame Zero, remind them about the `images/` and `sounds/` folder location — it's a common blocker.
- A blocker in the Build Log is a *gift* — it tells you what to support next session.

---

#### SESSION 44 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Project Title:** ________________________________________ **Track:** ____________________

---

### Part A — Build Log

Update this **as you work**. Status options: NOT-STARTED / IN-PROGRESS / DONE / BLOCKED.

| # | MVP Feature (from Session 43) | Status | Time stamp when finished | Blocker (if any) | Notes / hack used |
|---|-------------------------------|--------|-------------------------|------------------|-------------------|
| 1 | ________________________ | ____________ | __________ | ____________________ | ____________________ |
| 2 | ________________________ | ____________ | __________ | ____________________ | ____________________ |
| 3 | ________________________ | ____________ | __________ | ____________________ | ____________________ |
| 4 | ________________________ | ____________ | __________ | ____________________ | ____________________ |
| 5 | ________________________ | ____________ | __________ | ____________________ | ____________________ |

---

### Part B — Function Implementation Tracker

Tick each function once it returns the right value for at least one test input.

| # | Function name | Implemented? | Tested with | Returned what was expected? |
|---|---------------|--------------|-------------|------------------------------|
| 1 | ____________________ | ☐ | __________ | ☐ Yes &nbsp; ☐ No |
| 2 | ____________________ | ☐ | __________ | ☐ Yes &nbsp; ☐ No |
| 3 | ____________________ | ☐ | __________ | ☐ Yes &nbsp; ☐ No |
| 4 | ____________________ | ☐ | __________ | ☐ Yes &nbsp; ☐ No |
| 5 | ____________________ | ☐ | __________ | ☐ Yes &nbsp; ☐ No |
| 6 | ____________________ | ☐ | __________ | ☐ Yes &nbsp; ☐ No |
| 7 | ____________________ | ☐ | __________ | ☐ Yes &nbsp; ☐ No |

---

### Part C — Code-Quality Checklist (self-evaluated mid-session)

- ☐ Every function has a name in `snake_case`
- ☐ Every function name describes what the function *does*, not where it sits
- ☐ I have at least one comment explaining the *why* (not just the *what*) of a tricky line
- ☐ My main flow is wrapped in a `main()` function (or equivalent for Pygame Zero)
- ☐ I do not have any duplicated blocks of more than 4 lines
- ☐ I run the program at least every 5 minutes
- ☐ My filename is meaningful (not `untitled.py`)
- ☐ I have saved at least one backup version

---

### Part D — Pseudocode-to-Code Trace

Pick **one** function from your build today. Show your pseudocode line and the code line side by side.

| Pseudocode (from Session 43) | Python code I wrote |
|-------------------------------|---------------------|
| __________________________ | __________________________ |
| __________________________ | __________________________ |
| __________________________ | __________________________ |
| __________________________ | __________________________ |
| __________________________ | __________________________ |
| __________________________ | __________________________ |

---

### Part E — Bug Encounter Log (today)

| # | Symptom (what went wrong) | What I tried | Did it fix it? |
|---|---------------------------|--------------|----------------|
| 1 | __________________________ | __________________________ | ☐ Yes &nbsp; ☐ No |
| 2 | __________________________ | __________________________ | ☐ Yes &nbsp; ☐ No |
| 3 | __________________________ | __________________________ | ☐ Yes &nbsp; ☐ No |

---

### Part F — End-of-Session Reflection

**1. Which MVP feature am I most proud of finishing today?**

____________________________________________________________________

____________________________________________________________________

**2. Which feature am I worried about and why?**

____________________________________________________________________

____________________________________________________________________

**3. What is the *one* thing I want help with next session?**

____________________________________________________________________

____________________________________________________________________

**Instructor sign-off (Session 44 build checkpoint):** ____________________

---

### Session 45: Capstone Build — Features & Polish

---

#### SESSION 45 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 45 of 48 |
| **Title** | Capstone Build — Features & Polish |
| **Unit** | Unit 8: Capstone Project & Showcase |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced (synthesis) |
| **Cambridge Alignment** | IGCSE 0478 §8 (programming concepts), §10.1 (validation, verification, error handling), §10.2 (presentation/UI considerations as part of effective solutions) |
| **Singapore Alignment** | O-Level 7155 Module 2 (Programming — robustness, validation), Module 4 (Data — file I/O if used); 21CC critical thinking, communication |

##### Learning Objectives (SMART)

By the end of this session, students will be able to:

1. **Add** at least one stretch feature from their Session 43 list, OR fully harden one MVP feature with input validation and friendly error messages.
2. **Apply** at least three UX-polish improvements (e.g., a banner / title screen, coloured / formatted output, an instructions screen, sound/animation if game/turtle, replay-or-quit prompt).
3. **Evaluate** their own project against the Polish Checklist, scoring each item Yes / Partial / No with one-line justification.
4. **Update** their Stretch Features Tracker, marking which stretch items are now in-progress, done, or deferred.

##### Materials Needed

- Thonny (Python 3.11+)
- Pygame Zero with `images/` and `sounds/` folders for game-track students
- Optional: a simple sound library (free CC0 sounds) for game-track polish
- ANSI / `colorama` reference for console-track students who want coloured output (optional)
- Printed Polish Checklist + Stretch Features Tracker (this session's worksheet)

##### Procedure

**0–5 min: Warm-Up — "What does *good* feel like?"**
Show two screenshots side by side: a bare console output ("Score: 8") versus a polished one (banner, divider, congratulatory message, replay prompt). Ask: "Same code, same logic — what changed?" Students should land on phrases like *friendly*, *clear*, *finished*, *cared-about*.

**5–15 min: Mini-Lesson — UX Polish for Kids**
Walk through the **five polish levers** kids can pull in 40 minutes:

1. **Welcome / instructions screen** — a banner, the rules, a "press Enter to start" prompt.
2. **Friendly error messages** — never crash on bad input; replace `ValueError` traceback with `"Hmm, that's not a number — try again."`
3. **Pretty output** — separators (`"-" * 40`), section headings, aligned columns, optional colour via `colorama` or Pygame Zero text rendering.
4. **Replayability** — "Play again? (y/n)" loops; high-score persistence; multi-level support.
5. **Sound / animation** (game + turtle tracks only) — a victory sound, an enemy hit, a fade-in title.

Show a quick "before/after" of input validation:

```python
# Before
age = int(input("How old? "))   # crashes on "ten"

# After
while True:
    raw = input("How old? ").strip()
    if raw.isdigit() and 1 <= int(raw) <= 120:
        age = int(raw)
        break
    print("Hmm, please type a whole number between 1 and 120.")
```

End with the **Polish Rule of Three**: *Pick three polish levers today. Don't try all five. Three done beats five half-done.*

**15–55 min: Studio Work — Stretch + Polish**
Students self-direct. Two parallel tasks happen at most desks:

- **Pick one stretch feature** from the Session 43 list and implement it (or formally defer it).
- **Apply at least three polish levers** to the existing MVP.

Instructor circulates. Standard interventions:
- "Show me what your program looks like when the user types nonsense. What happens?"
- "Read the welcome screen aloud. Would your target user understand it?"
- "Update your Polish Checklist now, not at the end."

**Mini check-in at 35 min mark:** ask the class to demo *one polish change* to a neighbour for 60 seconds.

**55–60 min: Sharing & Preview**
Three volunteers demo a polish moment. Preview Session 46: testing, trace tables, bug logs. Reminder: bring the project file, the design doc, and *do not change any code* between now and the start of Session 46 — we want to test the version we have today.

##### Differentiation

**Support:**
- Limit polish to two levers (welcome screen + friendly error message).
- Offer a `print_banner()` helper as a snippet to drop in.
- Pair with a peer for input-validation refactors.

**Extension:**
- Require *all five* polish levers.
- Require sound (game) or animation (turtle) implemented from a CC0 asset.
- Add a settings screen (difficulty level, colour scheme) saved to a JSON file (Unit 6 link).

##### Assessment Criteria

| Criterion | Excellent (4) | Good (3) | Satisfactory (2) | Needs Improvement (1) |
|-----------|---------------|----------|------------------|----------------------|
| Stretch progress | 1+ stretch feature shipped or 1 MVP fully hardened | Stretch attempted, mostly working | Stretch started, not landed | No stretch progress |
| UX polish | 3+ levers applied with clear effect | 2 levers applied | 1 lever applied | None applied |
| Error handling | Invalid inputs handled with friendly messages everywhere it matters | Most invalid inputs handled | Some invalid inputs handled | Crashes on bad input |
| Polish Checklist | Honest, every item ticked with reason | Mostly complete | Sparse | Missing |

##### Teacher Notes

- The biggest temptation is to add *new* features rather than polish *existing* ones. Redirect students who keep starting and never finishing.
- Friendly error messages are the highest-leverage polish item — push every student to do this at least once.
- For Pygame Zero, emphasise that polish that *doesn't* work (e.g., a sound file in the wrong folder) is worse than no polish. Keep a fallback.
- Encourage students to read their own welcome screen out loud to themselves. They'll find typos and tone problems instantly.
- This is the last "free build" session. Tomorrow we test, and what we have is what we test.

---

#### SESSION 45 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Project Title:** ________________________________________

---

### Part A — Polish Checklist

Score each item: **Y** (done well), **P** (partial), **N** (not yet) — and give a one-line reason.

| # | Polish item | Y / P / N | Reason / what I did |
|---|-------------|-----------|----------------------|
| 1 | Welcome / title screen with the project name | _____ | ________________________________ |
| 2 | Instructions for the user before play / use | _____ | ________________________________ |
| 3 | Output is formatted (banners, separators, aligned columns) | _____ | ________________________________ |
| 4 | Friendly error message for invalid number input | _____ | ________________________________ |
| 5 | Friendly error message for invalid string / choice input | _____ | ________________________________ |
| 6 | "Play again?" or "continue?" loop (where it makes sense) | _____ | ________________________________ |
| 7 | High score / progress saved to a file (if applicable) | _____ | ________________________________ |
| 8 | Sound / animation / colour added thoughtfully | _____ | ________________________________ |
| 9 | Code is organised into functions (no giant `main`) | _____ | ________________________________ |
| 10 | Comments explain *why*, not just *what* | _____ | ________________________________ |
| 11 | Filename, variables, and functions are named meaningfully | _____ | ________________________________ |
| 12 | A short README note exists (paste below) | _____ | ________________________________ |

---

### Part B — Stretch Features Tracker

Refer to the Session 43 Stretch list. Update statuses honestly.

| # | Stretch feature | Status today (NOT-STARTED / IN-PROGRESS / DONE / DEFERRED) | Note |
|---|-----------------|------------------------------------------------------------|------|
| 1 | __________________ | __________________ | __________________ |
| 2 | __________________ | __________________ | __________________ |
| 3 | __________________ | __________________ | __________________ |
| 4 | __________________ | __________________ | __________________ |
| 5 | __________________ | __________________ | __________________ |

---

### Part C — README Note (3–6 sentences)

This goes at the top of your code file as a comment block, OR in a `README.md` next to it.

```
"""
Project: ____________________________________________________
Author:  ____________________________________________________
What it does: _______________________________________________
              _______________________________________________
How to run:   _______________________________________________
              _______________________________________________
Controls / inputs: __________________________________________
                   __________________________________________
"""
```

---

### Part D — Three Polish Levers I Pulled Today

| Lever | Before (one line describing the rough version) | After (one line describing the polished version) |
|-------|------------------------------------------------|---------------------------------------------------|
| 1. ________________ | ____________________________ | ____________________________ |
| 2. ________________ | ____________________________ | ____________________________ |
| 3. ________________ | ____________________________ | ____________________________ |

---

### Part E — User Walk-through (1 min thought experiment)

Pretend a brand-new user (not you, not your partner) sits in front of your project.

**1. What is the first thing they see?**

____________________________________________________________________

**2. What is the first thing they have to do?**

____________________________________________________________________

**3. What happens if they type the *wrong* thing?**

____________________________________________________________________

**4. What happens at the end? (Does the program tell them it's over?)**

____________________________________________________________________

---

### Part F — End-of-Session Reflection

**1. Which polish change made the biggest difference?**

____________________________________________________________________

**2. What stretch feature did I have to defer? Why?**

____________________________________________________________________

**3. What is the most fragile part of my project — the one I'd worry about during testing?**

____________________________________________________________________

**Instructor sign-off (Session 45 polish checkpoint):** ____________________

---

### Session 46: Capstone Testing & Trace Tables

---

#### SESSION 46 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 46 of 48 |
| **Title** | Capstone Testing & Trace Tables |
| **Unit** | Unit 8: Capstone Project & Showcase |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced (synthesis) |
| **Cambridge Alignment** | IGCSE 0478 §7.3 (testing — normal, boundary, erroneous data; trace tables; identifying errors), §10.1 (validation, verification); Lower Secondary 0860 "evaluating algorithms" |
| **Singapore Alignment** | O-Level 7155 Module 1 (algorithms — trace tables, dry-running), Module 2 (testing strategies, types of test data); 21CC critical thinking |

##### Learning Objectives (SMART)

By the end of this session, students will be able to:

1. **Construct** a Test Plan with at least 8 test cases that include normal, boundary, and invalid (erroneous) inputs, recording expected output before running each test.
2. **Execute** every test case against their capstone project and record actual output, marking pass/fail and noting the failure cause when applicable.
3. **Trace** the most complex function in their project line-by-line in a trace table, listing each variable's value at every step and the final return.
4. **File** at least one bug ticket per failed test (or write "no failures" with evidence) using the Bug Log format, including reproduction steps and a proposed fix.

##### Materials Needed

- Thonny (Python 3.11+)
- Their capstone project file (frozen at end of Session 45)
- Printed Test Plan / Trace Table / Bug Log worksheet (this session)
- Whiteboard for the live trace-table demo
- Optional: a partner laptop for "fresh-eyes" testing

##### Procedure

**0–5 min: Warm-Up — "Three kinds of input"**
On the board, write three columns: NORMAL / BOUNDARY / INVALID. Hold up a simple example function: `divide(a, b)` returns `a / b`. As a class, list 6 inputs and place each in a column:

| Input | Column |
|-------|--------|
| `divide(10, 2)` | NORMAL |
| `divide(0, 5)` | BOUNDARY |
| `divide(5, 0)` | INVALID |
| `divide(-3, -3)` | NORMAL |
| `divide("hi", 2)` | INVALID |
| `divide(1, 0.0001)` | BOUNDARY |

This grounds the testing vocabulary that drives the worksheet.

**5–20 min: Mini-Lesson — Systematic Testing + Trace Tables**

Part 1: **Test Plan structure** — show the table they'll fill in, with one fully worked row. Stress: *expected* is written **before** *actual*.

Part 2: **Trace Tables** (10 min) — pick one function, e.g.:

```python
def total_with_discount(prices, discount_pct):
    total = 0
    for price in prices:
        total = total + price
    discount = total * discount_pct / 100
    final = total - discount
    return final
```

Trace it on the board for `prices = [10, 20, 30]`, `discount_pct = 10`:

| Step | price | total | discount | final | Output |
|------|-------|-------|----------|-------|--------|
| init | — | 0 | — | — | — |
| loop 1 | 10 | 10 | — | — | — |
| loop 2 | 20 | 30 | — | — | — |
| loop 3 | 30 | 60 | — | — | — |
| after loop | — | 60 | 6.0 | 54.0 | — |
| return | — | 60 | 6.0 | 54.0 | 54.0 |

Tell students: in the worksheet, you do this for the *trickiest* function in **your** project — usually a scoring, sorting, or game-loop function.

**20–55 min: Studio Work — Run the Test Plan + Build the Trace Table + File Bug Tickets**

Workflow on the board:

```
1. Write all 8 test cases first (5 min).
2. Run them one by one. Record actual output. Mark pass/fail. (15 min)
3. For every fail, file a bug ticket. (5 min)
4. Pick one function. Build a full trace table. (10 min)
```

Students who finish early should attempt to **fix** one bug, then re-run the failed test and update the table.

**55–60 min: Sharing & Closure**
2 students share one bug they found. Whole-class question: "Was the bug in the *code* or in the *expected output*?" — a great teaching moment that good tests sometimes reveal misunderstandings, not just defects.

Preview Session 47: peer code review, refactor, debug.

##### Differentiation

**Support:**
- Reduce test-plan target from 8 to 5 cases.
- Pre-fill 3 normal-data tests for the student to start from.
- Pair with a peer for the trace table.
- Allow trace table on a smaller helper function rather than the main loop.

**Extension:**
- Require 12+ test cases including 3+ boundary and 3+ invalid.
- Trace two functions: one with a loop and one with a conditional.
- Add a *test runner* function in code that prints pass/fail automatically (intro to assertions).

##### Assessment Criteria (Full Capstone Rubric — testing checkpoint)

| Criterion | Excellent (4) | Good (3) | Satisfactory (2) | Needs Improvement (1) |
|-----------|---------------|----------|------------------|----------------------|
| Functionality | All features work; handles edge cases | All core features work; minor edge-case gaps | Core features work with bugs | Major features missing |
| Code Quality | Modular, well-named, commented; uses functions and OOP appropriately | Mostly modular and clear | Some structure, some duplication | Monolithic, unclear, no comments |
| Algorithm Design | Pseudocode/flowchart matches code; trace table verifies behaviour | Design artefacts present and mostly accurate | Design artefacts present but partial | No design artefacts |
| Creativity & Originality | Original concept with personal flair | Personalised standard concept | Standard concept | Direct copy of example |
| Presentation | Clear demo, articulates design choices, handles questions | Clear demo with minor gaps | Demo runs but explanation thin | Cannot demo or explain |

> Session 46 emphasises **Functionality** (do the tests pass?) and **Algorithm Design** (does the trace table match the code?).

##### Teacher Notes

- Force the order: *write expected before running actual*. Otherwise students will write expected = actual after the fact and learn nothing.
- The trickiest part of the trace table for kids is remembering that variables retain values between rows. Demo this twice if needed.
- A test that *passes unexpectedly* is also worth a bug ticket — sometimes the code is right by accident.
- If a student "has no bugs", challenge them with one new invalid input you devise on the spot. Almost always finds one.
- Encourage screen recording or a photo of the bug — useful evidence for showcase Q&A.

---

#### SESSION 46 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Project Title:** ________________________________________

---

### Part A — Test Plan (8+ test cases)

Tick the type for each row. Write expected **before** running. Record actual after.

| # | Type (N/B/I) | Test description (what user does) | Input | Expected output / behaviour | Actual output / behaviour | Pass / Fail | Notes |
|---|--------------|-----------------------------------|-------|------------------------------|---------------------------|------------|-------|
| 1 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |
| 2 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |
| 3 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |
| 4 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |
| 5 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |
| 6 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |
| 7 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |
| 8 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |
| 9 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |
| 10 | _____ | ____________________ | __________ | __________________ | __________________ | ______ | __________ |

**Test type key: N = Normal | B = Boundary | I = Invalid**

**Coverage check:**
- Normal data tests: _____ (need ≥ 3)
- Boundary data tests: _____ (need ≥ 2)
- Invalid data tests: _____ (need ≥ 2)

---

### Part B — Trace Table for the Trickiest Function

**Function name I am tracing:** ________________________________________

**Inputs / parameter values used for this trace:** ________________________________________

**Paste (or rewrite) the function code here for reference:**

```
___________________________________________________________________________

___________________________________________________________________________

___________________________________________________________________________

___________________________________________________________________________

___________________________________________________________________________

___________________________________________________________________________

___________________________________________________________________________

___________________________________________________________________________
```

**Trace table — add as many rows as needed:**

| Step | Line | Variable 1: ______ | Variable 2: ______ | Variable 3: ______ | Variable 4: ______ | Output / Return |
|------|------|---------------------|---------------------|---------------------|---------------------|------------------|
| init | ___ | __________ | __________ | __________ | __________ | __________ |
| 1    | ___ | __________ | __________ | __________ | __________ | __________ |
| 2    | ___ | __________ | __________ | __________ | __________ | __________ |
| 3    | ___ | __________ | __________ | __________ | __________ | __________ |
| 4    | ___ | __________ | __________ | __________ | __________ | __________ |
| 5    | ___ | __________ | __________ | __________ | __________ | __________ |
| 6    | ___ | __________ | __________ | __________ | __________ | __________ |
| 7    | ___ | __________ | __________ | __________ | __________ | __________ |
| 8    | ___ | __________ | __________ | __________ | __________ | __________ |
| return | ___ | __________ | __________ | __________ | __________ | __________ |

**Did the trace match the actual program output for the same inputs?** ☐ Yes &nbsp; ☐ No

If no, where do they differ? ________________________________________

---

### Part C — Bug Log

File **one ticket per failed test** (and feel free to log more if you find them).

| Bug # | Description (one sentence) | Steps to reproduce (1, 2, 3...) | Suspected cause | Fix attempted | Status (OPEN / FIXED / DEFERRED) |
|-------|---------------------------|--------------------------------|------------------|---------------|----------------------------------|
| 1 | ________________________ | ________________________ | __________ | __________ | __________ |
| 2 | ________________________ | ________________________ | __________ | __________ | __________ |
| 3 | ________________________ | ________________________ | __________ | __________ | __________ |
| 4 | ________________________ | ________________________ | __________ | __________ | __________ |

---

### Part D — Testing Reflection

**1. How many tests passed on the first run? ____ / ____**

**2. What was the most surprising failure?**

____________________________________________________________________

**3. Did any test reveal that *the expected output was wrong* (your model of the code was off)?**

____________________________________________________________________

**4. Which bug do I most want to fix before Session 48?**

____________________________________________________________________

**Instructor sign-off (Session 46 testing checkpoint):** ____________________

---

### Session 47: Code Review, Refactor & Debug

---

#### SESSION 47 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 47 of 48 |
| **Title** | Code Review, Refactor & Debug |
| **Unit** | Unit 8: Capstone Project & Showcase |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced (synthesis) |
| **Cambridge Alignment** | IGCSE 0478 §10.1 (maintainability, readable code), §7.3 (debugging strategies); Lower Secondary 0860 "improving algorithms" |
| **Singapore Alignment** | O-Level 7155 Module 2 (modular design, refactoring, code readability); 21CC communication, collaboration |

##### Learning Objectives (SMART)

By the end of this session, students will be able to:

1. **Conduct** a structured peer code review on a partner's capstone using a 12-item Code Review Checklist, recording at least one strength and two specific suggestions per item that scores below "Good".
2. **Refactor** their own code based on peer and self-review feedback, making at least three improvements such as renaming variables for clarity, extracting a function, removing dead code, or replacing a magic number with a named constant.
3. **Debug** at least one outstanding issue from the Session 46 Bug Log, recording the fix in the Refactor Log.
4. **Reflect** on the difference between *cosmetic* refactoring (renaming) and *structural* refactoring (extraction), and explain when each is appropriate.

##### Materials Needed

- Thonny (Python 3.11+)
- Each student's full capstone (code, design doc, test plan, bug log)
- Printed Code Review Checklist + Refactor Log worksheet
- Optional: a "review etiquette" reference card on the wall ("Ask, don't tell." / "Suggest one, not seven." / "Praise specifically.")
- Pairing list (instructor pre-pairs by skill mix where possible)

##### Procedure

**0–5 min: Warm-Up — "Read this code aloud"**
Project a 12-line snippet with poor naming (`def f(x, y): a = x + y; return a`) and one with good naming (`def total_score(quiz_score, bonus): final = quiz_score + bonus; return final`). Ask students which they'd want to maintain. The point: *names are documentation*.

**5–15 min: Mini-Lesson — Review Etiquette + Refactoring Mindset**

Two halves:

**(a) Peer review etiquette — "Ask, don't tell."**
Show the difference:

- ❌ "This is wrong. Use a list."
- ✅ "I noticed you have five `score1, score2, score3, score4, score5`. Have you considered storing them in a list? What would change?"

Three rules on the board:
1. **Ask, don't tell.** Frame suggestions as questions.
2. **Praise specifically.** "Your function names are great because they're verbs" beats "Nice work."
3. **Suggest one, not seven.** Pick the highest-impact change.

**(b) The refactoring mindset.**
Refactoring = *changing the shape of code without changing what it does*. Show three classic refactors:

- **Rename for clarity:** `x → cart_total`
- **Extract a function:** turn 8 lines used twice into one helper called twice.
- **Remove dead code:** that commented-out block from Session 44? Delete it.

Plus a fourth mini-refactor:

- **Magic number → named constant:** `if score >= 80` → `WIN_THRESHOLD = 80`.

State the **rule of refactor**: *the tests must still pass after every refactor*.

**15–55 min: Studio — Review (15 min) + Refactor / Debug (25 min)**

Phase 1 — **Peer Code Review (15 min):**
- Pair students. Swap projects.
- Each student opens partner's code in Thonny **read-only mind**: no edits, just reading and ticking the Code Review Checklist.
- Fill the checklist on the worksheet for the partner.
- Hand the worksheet back at the end of 15 minutes.

Phase 2 — **Refactor / Debug (25 min):**
- Students return to their own code with the partner's review and their Session 46 Bug Log open.
- **Required:** at least 3 refactors.
- **Required:** at least 1 bug fix from the Session 46 log.
- After every change, run all 8+ tests from Session 46 to confirm nothing broke.
- Log every change in the Refactor Log table.

**55–60 min: Sharing & Closure**
Two volunteers share one refactor that *felt* small but made the code much clearer. Preview Session 48: showcase day.
**Homework:** prepare a 3-minute demo script. Bring final project file. Bring all worksheets to date.

##### Differentiation

**Support:**
- Reduce checklist from 12 items to 8.
- Allow voice-feedback for peer review instead of written.
- Lower required refactors from 3 to 2.
- Pair Support student with an instructor or a confident peer.

**Extension:**
- Require a *structural* refactor: extract a function, or convert a duplicated block to a loop.
- Require addition of one assertion (`assert`) to validate an internal invariant.
- Run all Session 46 tests automatically with a small test-runner function and produce a pass/fail count.

##### Assessment Criteria

| Criterion | Excellent (4) | Good (3) | Satisfactory (2) | Needs Improvement (1) |
|-----------|---------------|----------|------------------|----------------------|
| Review quality | 12 checklist items + specific praise + ≥2 suggestions on weak items | Most items, mostly specific feedback | Items ticked but vague | Checklist barely filled |
| Refactor depth | 3+ refactors including at least one structural | 3 refactors, mostly cosmetic | 1–2 refactors | 0 refactors |
| Debug follow-through | At least one Session 46 bug closed and re-tested | Bug attempted, partially fixed | Bug attempted, no resolution | Bug log untouched |
| Test integrity | All Session 46 tests still pass after refactor | One test broke and was fixed | Tests not re-run | Refactor broke logic |

##### Teacher Notes

- The biggest danger is *uncivil* peer review. Coach the language. Pre-print the etiquette rules on a card if needed.
- Watch for students who refactor *and* break their tests — make re-running the tests after every change a hard rule.
- Praise refactors that *delete* code. Reducing line count while keeping function is the gold standard.
- Keep the partner's review as evidence for the showcase day — it tells a story of growth.
- Some students will want to keep adding features. Hold the line: today is *quality*, not *features*.

---

#### SESSION 47 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**My Project Title:** ________________________________________

**Partner I am reviewing:** ________________________________________

**Partner's Project Title:** ________________________________________

---

### Part A — Code Review Checklist (fill in for your partner)

For each item, score **Y / P / N** and write a one-line, *specific* note. Use "ask, don't tell."

| # | Item | Y / P / N | Specific note (a question or a praise) |
|---|------|-----------|----------------------------------------|
| 1 | The project runs without crashing on a typical input | _____ | ____________________________________ |
| 2 | Function names are verbs and describe what the function does | _____ | ____________________________________ |
| 3 | Variable names are meaningful (no `x`, `tmp`, `data2` unless justified) | _____ | ____________________________________ |
| 4 | Code is broken into functions; no giant `main` block | _____ | ____________________________________ |
| 5 | I can match each pseudocode step from the design doc to a code line | _____ | ____________________________________ |
| 6 | Invalid input is handled with a friendly message, not a crash | _____ | ____________________________________ |
| 7 | There is at least one comment explaining a tricky decision | _____ | ____________________________________ |
| 8 | There are no obviously duplicated 4+ line blocks | _____ | ____________________________________ |
| 9 | Magic numbers are named (`WIN_THRESHOLD`, not `80` scattered around) | _____ | ____________________________________ |
| 10 | The welcome / instructions screen is clear to a new user | _____ | ____________________________________ |
| 11 | If files are used, the program handles a missing file gracefully | _____ | ____________________________________ |
| 12 | The code uses Unit 1–7 ideas appropriately (lists/dicts/functions/files/OOP) | _____ | ____________________________________ |

**One thing I really liked about my partner's code (be specific):**

____________________________________________________________________

____________________________________________________________________

**The single highest-impact suggestion I'd offer:**

____________________________________________________________________

____________________________________________________________________

---

### Part B — Feedback Received From My Partner (paste/transcribe)

**My partner's standout praise:**

____________________________________________________________________

**My partner's top suggestion:**

____________________________________________________________________

**Their second suggestion (if given):**

____________________________________________________________________

---

### Part C — Refactor Log (changes I made today)

| # | Change type (rename / extract / delete / constant / fix bug / other) | Before (one line) | After (one line) | Tests still pass? |
|---|---------------------------------------------------------------------|-------------------|------------------|-------------------|
| 1 | __________________ | ____________________ | ____________________ | ☐ Yes &nbsp; ☐ No |
| 2 | __________________ | ____________________ | ____________________ | ☐ Yes &nbsp; ☐ No |
| 3 | __________________ | ____________________ | ____________________ | ☐ Yes &nbsp; ☐ No |
| 4 | __________________ | ____________________ | ____________________ | ☐ Yes &nbsp; ☐ No |
| 5 | __________________ | ____________________ | ____________________ | ☐ Yes &nbsp; ☐ No |

---

### Part D — Bug Closed Today

**Bug # from Session 46 log:** _____

**Symptom:** ________________________________________

**Root cause (in 1–2 sentences):** ________________________________________

**Fix (what I changed):** ________________________________________

**Re-tested? Result:** ☐ Pass &nbsp; ☐ Fail

---

### Part E — Reflection

**1. What is the difference between a *cosmetic* refactor (e.g., renaming) and a *structural* refactor (e.g., extracting a function)?**

____________________________________________________________________

____________________________________________________________________

**2. Which refactor today made the biggest improvement to readability?**

____________________________________________________________________

**3. Was anything in my partner's feedback hard to hear at first? How did I respond?**

____________________________________________________________________

____________________________________________________________________

**Instructor sign-off (Session 47 review + refactor checkpoint):** ____________________

---

### Session 48: Final Showcase & Reflection

---

#### SESSION 48 — LESSON PLAN

---

| Attribute | Details |
|-----------|---------|
| **Session Number** | 48 of 48 |
| **Title** | Final Showcase & Reflection |
| **Unit** | Unit 8: Capstone Project & Showcase |
| **Duration** | 60 minutes |
| **Age Group** | 10–14 years |
| **Difficulty** | Intermediate–Advanced (synthesis + presentation) |
| **Cambridge Alignment** | IGCSE 0478 full integration (algorithm design, programming, testing, presentation of solutions); Lower Secondary 0860 evaluation strand |
| **Singapore Alignment** | O-Level 7155 Modules 1, 2, 4 — full integration; 21CC communication, civic literacy / global awareness, self-management |

##### Learning Objectives (SMART)

By the end of this session, students will be able to:

1. **Demonstrate** their capstone project to an audience in a 3-minute structured demo, articulating the problem, approach, and one design decision they're proud of.
2. **Field** at least two audience questions on their design or implementation, drawing on their Session 43 design document and Session 46 trace table.
3. **Provide** structured peer feedback on at least four classmates using the Peer Feedback Form, including one specific praise and one constructive question per peer.
4. **Reflect** on the 48-session journey by completing the Course Reflection, identifying personal growth, hardest moments, and a concrete next-step pathway (Cambridge IGCSE 0478, Singapore O-Level 7155, or a chosen library/track).

##### Materials Needed

- Thonny + Replit (for sharing) on the demo machine
- Projector / screen for live demos
- Printed Showcase Self-Evaluation, Peer Feedback Form (×4–6 copies per student), Course Reflection
- **Certificate of Completion** templates printed on heavier card (one per student)
- Optional: families / parents / instructors invited as audience
- A simple stopwatch or timer visible to all
- Snacks (it's the last day!)

##### Procedure

**0–5 min: Mini-Lesson — Showcase Format and Tone**
On the board, the demo formula:

```
3 minutes:
  0:00–0:30  Hook + problem statement
  0:30–1:30  Live demo (run the project, walk through happy path)
  1:30–2:30  One design decision I'm proud of (show the code or the trace table)
  2:30–3:00  What I'd add next + thanks

2 minutes:
  Audience Q&A
```

Ground rules for the audience: ask one specific question; offer one specific praise; tone is celebratory.

Hand out blank Peer Feedback Forms (4–6 per student) and the Showcase order list.

**5–45 min: Showcases (≈40 min for ~8 students at 5 min each — adjust for class size)**
Each student presents in turn, following the formula. The instructor times. The audience fills the Peer Feedback Form for at least 4 classmates (more if class is small enough that everyone reviews everyone).

For larger classes (>10), run two showcase rounds in parallel groups, each with an instructor or older student facilitator.

**45–55 min: Course Reflection (silent, individual)**
Students work through the Course Reflection prompts in the worksheet — 10 minutes of focused, individual writing.

**55–60 min: Closure — Certificate of Completion**
Award each student their printed Certificate of Completion. A short sentence per student from the instructor: "What I saw you grow in across these 48 sessions." Group photo if desired.

End on the **next-steps card**: each student leaves with a personal next-step pathway written on the back of the certificate or on the Course Reflection.

##### Differentiation

**Support:**
- Allow students who are nervous to demo from a written script (the Self-Evaluation script section).
- Reduce the demo time to 2 minutes.
- Pre-record a screen capture and play it during the live slot, with the student narrating live.
- Pair-demo: two students co-present complementary projects.

**Extension:**
- Demo for 4 minutes including a *deliberate failure* and a *recovery*, showing error handling live.
- Field 4+ audience questions, including one "What would you do differently?".
- Submit a one-page written reflection in addition to the worksheet.
- Publish the project on Replit and share the link with the cohort.

##### Assessment Criteria (Full Capstone Rubric — final checkpoint, scored across the *whole project*)

| Criterion | Excellent (4) | Good (3) | Satisfactory (2) | Needs Improvement (1) |
|-----------|---------------|----------|------------------|----------------------|
| Functionality | All features work; handles edge cases | All core features work; minor edge-case gaps | Core features work with bugs | Major features missing |
| Code Quality | Modular, well-named, commented; uses functions and OOP appropriately | Mostly modular and clear | Some structure, some duplication | Monolithic, unclear, no comments |
| Algorithm Design | Pseudocode/flowchart matches code; trace table verifies behaviour | Design artefacts present and mostly accurate | Design artefacts present but partial | No design artefacts |
| Creativity & Originality | Original concept with personal flair | Personalised standard concept | Standard concept | Direct copy of example |
| Presentation | Clear demo, articulates design choices, handles questions | Clear demo with minor gaps | Demo runs but explanation thin | Cannot demo or explain |

> Session 48 applies all five criteria. Final grade = average across criteria. Evidence draws from: design doc (S43), build/polish (S44–45), test plan + trace table (S46), peer review + refactor log (S47), and the demo + Q&A today.

##### Teacher Notes

- Time-keeping is the single biggest factor. Use a visible timer. Cut at 3 minutes — kindly but firmly.
- Have a back-up: if a project crashes during demo, applaud the student for showing they can debug live. Real software fails; presentation grace matters.
- Audience feedback forms are evidence too — collect them, photograph them, share copies with families.
- The Certificate moment matters. Read each student's name aloud. Say one specific thing you saw them grow in.
- Save photos / video clips with parental permission for the next cohort's "what to expect" gallery.

---

#### SESSION 48 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Project Title:** ________________________________________

---

### Part A — Showcase Self-Evaluation (fill before demoing)

**1. My demo plan in 4 lines (the formula):**

| Slot | What I will say or show |
|------|--------------------------|
| 0:00–0:30 Hook + problem | ____________________________________________________________ |
| 0:30–1:30 Live demo path | ____________________________________________________________ |
| 1:30–2:30 Design pride | ____________________________________________________________ |
| 2:30–3:00 Next steps + thanks | ____________________________________________________________ |

**2. The one sentence I want every audience member to remember:**

____________________________________________________________________

____________________________________________________________________

**3. Two questions I am ready for:**

a. ________________________________________

b. ________________________________________

**4. The risky moment in my live demo (the part most likely to crash) and my back-up plan:**

____________________________________________________________________

____________________________________________________________________

---

### Part B — Showcase Self-Evaluation (fill after demoing)

**1. What went well in my demo?**

____________________________________________________________________

____________________________________________________________________

**2. What would I do differently if I demoed again tomorrow?**

____________________________________________________________________

____________________________________________________________________

**3. Hardest question I was asked, and how I answered:**

____________________________________________________________________

____________________________________________________________________

**4. Final self-rating against the rubric (circle one per row):**

| Criterion | 4 | 3 | 2 | 1 |
|-----------|---|---|---|---|
| Functionality | 4 | 3 | 2 | 1 |
| Code Quality | 4 | 3 | 2 | 1 |
| Algorithm Design | 4 | 3 | 2 | 1 |
| Creativity & Originality | 4 | 3 | 2 | 1 |
| Presentation | 4 | 3 | 2 | 1 |

**Total / 20:** _____

---

### Part C — Peer Feedback Forms (fill one per classmate, at least 4)

#### Peer #1

**Classmate's name:** ________________________________________

**Their project title:** ________________________________________

**1. One thing I really liked (be specific):**

____________________________________________________________________

**2. One specific question I have about how it works:**

____________________________________________________________________

**3. One feature I'd add if it were my project:**

____________________________________________________________________

**4. Star rating for the demo overall (circle):** ★ &nbsp; ★★ &nbsp; ★★★ &nbsp; ★★★★ &nbsp; ★★★★★

---

#### Peer #2

**Classmate's name:** ________________________________________

**Their project title:** ________________________________________

**1. One thing I really liked (be specific):**

____________________________________________________________________

**2. One specific question I have about how it works:**

____________________________________________________________________

**3. One feature I'd add if it were my project:**

____________________________________________________________________

**4. Star rating for the demo overall (circle):** ★ &nbsp; ★★ &nbsp; ★★★ &nbsp; ★★★★ &nbsp; ★★★★★

---

#### Peer #3

**Classmate's name:** ________________________________________

**Their project title:** ________________________________________

**1. One thing I really liked (be specific):**

____________________________________________________________________

**2. One specific question I have about how it works:**

____________________________________________________________________

**3. One feature I'd add if it were my project:**

____________________________________________________________________

**4. Star rating for the demo overall (circle):** ★ &nbsp; ★★ &nbsp; ★★★ &nbsp; ★★★★ &nbsp; ★★★★★

---

#### Peer #4

**Classmate's name:** ________________________________________

**Their project title:** ________________________________________

**1. One thing I really liked (be specific):**

____________________________________________________________________

**2. One specific question I have about how it works:**

____________________________________________________________________

**3. One feature I'd add if it were my project:**

____________________________________________________________________

**4. Star rating for the demo overall (circle):** ★ &nbsp; ★★ &nbsp; ★★★ &nbsp; ★★★★ &nbsp; ★★★★★

---

#### Peer #5 (optional)

**Classmate's name:** ________________________________________

**Their project title:** ________________________________________

**1. One thing I really liked (be specific):**

____________________________________________________________________

**2. One specific question I have about how it works:**

____________________________________________________________________

**3. One feature I'd add if it were my project:**

____________________________________________________________________

**4. Star rating for the demo overall (circle):** ★ &nbsp; ★★ &nbsp; ★★★ &nbsp; ★★★★ &nbsp; ★★★★★

---

#### Peer #6 (optional)

**Classmate's name:** ________________________________________

**Their project title:** ________________________________________

**1. One thing I really liked (be specific):**

____________________________________________________________________

**2. One specific question I have about how it works:**

____________________________________________________________________

**3. One feature I'd add if it were my project:**

____________________________________________________________________

**4. Star rating for the demo overall (circle):** ★ &nbsp; ★★ &nbsp; ★★★ &nbsp; ★★★★ &nbsp; ★★★★★

---

### Part D — Course Reflection (the 48-session journey)

**1. Looking back at all 48 sessions, the moment I'm most proud of is…**

____________________________________________________________________

____________________________________________________________________

____________________________________________________________________

**2. The hardest part of the course for me was…**

____________________________________________________________________

____________________________________________________________________

____________________________________________________________________

**3. The most useful thing I learned (and where I think I'll use it again):**

____________________________________________________________________

____________________________________________________________________

____________________________________________________________________

**4. A skill I now want to develop further (be specific — e.g., "OOP", "game physics", "data analysis with `pandas`", "web with Flask"):**

____________________________________________________________________

____________________________________________________________________

**5. My next-step pathway — circle one or more, then write a one-line plan:**

- ☐ Continue toward **Cambridge IGCSE Computer Science (0478)**
- ☐ Continue toward **Singapore O-Level Computing (7155)**
- ☐ Pursue **competitive programming** (e.g., Bebras, NOI Junior, USACO Bronze)
- ☐ Build a **portfolio** of personal Python projects on GitHub / Replit
- ☐ Explore a specific area: ☐ Game dev (Pygame Zero / Pygame) &nbsp; ☐ Data (pandas / matplotlib) &nbsp; ☐ Web (Flask / Django) &nbsp; ☐ AI/ML (intro level) &nbsp; ☐ Microcontrollers (micro:bit / Raspberry Pi)
- ☐ Other: ____________________________________

**One-line plan for the next 4 weeks:**

____________________________________________________________________

____________________________________________________________________

**6. A message to a future student starting this course:**

____________________________________________________________________

____________________________________________________________________

____________________________________________________________________

**7. (Optional) Who would I like to thank from this course, and why?**

____________________________________________________________________

____________________________________________________________________

---

### Part E — Final Submission Checklist

I am submitting today, with all artefacts kept together:

- ☐ Final capstone code file (Thonny + Replit link if applicable)
- ☐ Session 43 Capstone Design Document + flowchart sketch
- ☐ Session 44 Build Log
- ☐ Session 45 Polish Checklist + Stretch Tracker
- ☐ Session 46 Test Plan + Trace Table + Bug Log
- ☐ Session 47 Code Review (received from partner) + Refactor Log
- ☐ Session 48 Self-Evaluation + 4+ Peer Feedback Forms + Course Reflection
- ☐ Replit share link (if used): ____________________________________

**Instructor sign-off (Session 48 final showcase checkpoint):** ____________________

---

### Part F — Certificate of Completion

> Print this page on heavier card. Cut along the dashed border. Sign and present.

```
+----------------------------------------------------------------------------+
|                                                                            |
|                       CERTIFICATE OF COMPLETION                            |
|                                                                            |
|                  Python Programming for Kids — Intermediate                |
|                              48-Session Course                             |
|                                                                            |
|                          This certificate is awarded to                    |
|                                                                            |
|              ____________________________________________________          |
|                              (Student Name)                                |
|                                                                            |
|       for successfully completing all 48 sessions across 8 units —         |
|       Foundations, Control Flow, Data Structures, Algorithms,              |
|       Functions & Modular Code, File I/O, Object-Oriented Programming,     |
|       and the Capstone Project & Showcase — with alignment to              |
|       Cambridge Lower Secondary Computing (0860), IGCSE 0478,              |
|       and Singapore O-Level Computing (7155).                              |
|                                                                            |
|       Capstone project: ____________________________________________       |
|                                                                            |
|       Final rubric score: _____ / 20                                        |
|                                                                            |
|       Date: ___________________                                            |
|                                                                            |
|       Instructor signature: ____________________________________            |
|                                                                            |
|       Next-step pathway: ____________________________________________       |
|                                                                            |
+----------------------------------------------------------------------------+
```

**Congratulations, programmer. You shipped a project. The next one is easier.**

---
