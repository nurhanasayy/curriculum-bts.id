# Python Programming Curriculum for Kids
## 48 Sessions × 60 Minutes — Cambridge × Singapore MOE Aligned

---

## Table of Contents

- [Curriculum Design Analysis](#curriculum-design-analysis)
- [Curriculum Framework & References](#curriculum-framework--references)
- [Course Overview](#course-overview)
- [Alignment with Cambridge Computing](#alignment-with-cambridge-computing)
- [Alignment with Singapore MOE Frameworks](#alignment-with-singapore-moe-frameworks)
- [CSTA K-12 Cross-Walk](#csta-k-12-cross-walk)
- [Course-Level Learning Objectives](#course-level-learning-objectives)
- [Tools & Materials](#tools--materials)

### Unit 1: Python Foundations & Computational Thinking (Sessions 1-6)
- [Session 1: Course Introduction & Thonny Setup](#session-1)
- [Session 2: Variables, Constants & Data Types](#session-2)
- [Session 3: Input, Numbers & Arithmetic](#session-3)
- [Session 4: Strings, Indexing & Slicing](#session-4)
- [Session 5: Pseudocode & Flowcharts](#session-5)
- [Session 6: Project 1 — Personal Profile App](#session-6)

### Unit 2: Decision Making & Iteration Foundations (Sessions 7-12)
- [Session 7: Booleans & Comparison Operators](#session-7)
- [Session 8: If / Elif / Else Statements](#session-8)
- [Session 9: Logical Operators & Nested Conditions](#session-9)
- [Session 10: While Loops & Trace Tables](#session-10)
- [Session 11: Input Validation & Test Data](#session-11)
- [Session 12: Project 2 — Number Guessing Game](#session-12)

### Unit 3: Loops, Repetition & Turtle Graphics (Sessions 13-18)
- [Session 13: For Loops & range()](#session-13)
- [Session 14: Loop Patterns — Totalling, Counting, Min/Max/Average](#session-14)
- [Session 15: Nested Loops](#session-15)
- [Session 16: Loop Control — break & continue](#session-16)
- [Session 17: Turtle Graphics with Loops](#session-17)
- [Session 18: Project 3 — Geometric Art Generator](#session-18)

### Unit 4: Lists & Standard Algorithms (Sessions 19-24)
- [Session 19: Lists Basics](#session-19)
- [Session 20: List Methods & Iteration](#session-20)
- [Session 21: Linear Search Algorithm](#session-21)
- [Session 22: Bubble Sort Algorithm](#session-22)
- [Session 23: Tuples & Dictionaries](#session-23)
- [Session 24: Project 4 — Quiz & Leaderboard App](#session-24)

### Unit 5: Functions & Modular Design (Sessions 25-30)
- [Session 25: Defining & Calling Functions](#session-25)
- [Session 26: Parameters & Arguments](#session-26)
- [Session 27: Return Values & Scope](#session-27)
- [Session 28: Default Parameters](#session-28)
- [Session 29: Top-Down Design with Functions](#session-29)
- [Session 30: Project 5 — Modular Math Helper](#session-30)

### Unit 6: File I/O, Errors & Built-in Modules (Sessions 31-36)
- [Session 31: Reading from Text Files](#session-31)
- [Session 32: Writing to Text Files](#session-32)
- [Session 33: Errors & Try / Except](#session-33)
- [Session 34: random & math Modules](#session-34)
- [Session 35: datetime & Simple Data Persistence](#session-35)
- [Session 36: Project 6 — Journal Application](#session-36)

### Unit 7: Object-Oriented Programming & Game Mini-Project (Sessions 37-42)
- [Session 37: Classes & Objects](#session-37)
- [Session 38: Methods & Attributes](#session-38)
- [Session 39: Designing with Multiple Objects](#session-39)
- [Session 40: Pygame Zero — Sprites, Draw, Update](#session-40)
- [Session 41: Pygame Zero — Input & Collisions](#session-41)
- [Session 42: Project 7 — Mini Arcade Game](#session-42)

### Unit 8: Capstone Project & Showcase (Sessions 43-48)
- [Session 43: Capstone Planning & Design Document](#session-43)
- [Session 44: Capstone Build — Core Mechanics](#session-44)
- [Session 45: Capstone Build — Features & Polish](#session-45)
- [Session 46: Capstone Testing & Trace Tables](#session-46)
- [Session 47: Code Review, Refactor & Debug](#session-47)
- [Session 48: Final Showcase & Reflection](#session-48)

### Assessment & Resources
- [Assessment Framework](#assessment-framework)
- [Resources and Materials](#resources-and-materials)
- [Differentiation Strategies](#differentiation-strategies)
- [Teacher Notes](#teacher-notes)
- [Appendices](#appendices)
- [Sources and References](#sources-and-references)

---

## Curriculum Design Analysis

### Why 48 Sessions?

The 48-session structure doubles the standard 24-session block to give text-based programming the time it genuinely needs at this age band. Cambridge Lower Secondary Computing (0860) and Singapore O-Level Computing (7155) both treat Python as a multi-year skill — squeezing it into 24 sessions forces shallow coverage of foundational topics like data types, control flow, and functions, which then become bottlenecks at IGCSE / O-Level. Forty-eight 60-minute sessions (48 hours total) gives roughly **6 sessions per major concept area**, allowing one session to introduce, several to practise, and one to apply through a project.

### Learning Weight Distribution

| Topic Strand | Sessions | Weight | Rationale |
|--------------|----------|--------|-----------|
| Python Foundations & CT | 6 | 12.5% | Setup, syntax, data types, strings, design tools — must be solid |
| Control Flow | 6 | 12.5% | Selection, validation, trace tables — IGCSE/O-Level core |
| Loops & Iteration | 6 | 12.5% | For/while, nested, turtle — repetition mastery |
| Lists & Standard Algorithms | 6 | 12.5% | Linear search, bubble sort — required by 0478 & 7155 |
| Functions & Modular Design | 6 | 12.5% | Top-down design, parameters, scope |
| Files, Errors & Modules | 6 | 12.5% | File I/O, exception handling, library use |
| OOP & Game Mini-Project | 6 | 12.5% | Classes/objects + Pygame Zero application |
| Capstone Project | 6 | 12.5% | Plan → build → test → polish → present |
| **Total** | **48** | **100%** | |

### Pedagogical Approach

The course follows a **PRIMM** sequence (Predict, Run, Investigate, Modify, Make) within each session, paired with **explicit unplugged design steps** (pseudocode, flowcharts, trace tables) before any code is written. This dual approach is recommended by both the Cambridge teaching guidance and the Singapore MOE Computing syllabus.

Every session ends with a **reflection-and-debug** segment so students articulate what they learned and what went wrong — building the metacognitive habits IGCSE/O-Level practical exams reward.

---

## Curriculum Framework & References

| Framework / Source | Organisation | Reference |
|--------------------|--------------|-----------|
| Lower Secondary Computing (0860) | Cambridge International | https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-lower-secondary/curriculum/computing/ |
| IGCSE Computer Science (0478) 2026–2028 | Cambridge International | https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-igcse-computer-science-0478/ |
| Primary Computing (0072 / 0059) | Cambridge International | https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-primary/curriculum/computing/ |
| O-Level Computing (7155) | SEAB / MOE Singapore | https://www.seab.gov.sg/files/O%20Lvl%20Syllabus%20Sch%20Cddts/2026/7155_y26_sy.pdf |
| Code for Fun Programme | IMDA & MOE Singapore | https://www.imda.gov.sg/how-we-can-help/code-for-fun |
| EdTech Masterplan 2030 / DLTS | MOE Singapore | https://www.moe.gov.sg/education-in-sg/educational-technology-journey/edtech-masterplan/digital-literacy-and-technological-skills |
| 21st Century Competencies | MOE Singapore | https://www.moe.gov.sg/education-in-sg/21st-century-competencies |
| CSTA K-12 Computer Science Standards | Computer Science Teachers Association | https://csteachers.org/k12standards/interactive/ |
| Creative Computing Curriculum | Harvard GSE | https://creativecomputing.gse.harvard.edu/guide/ |
| PRIMM Pedagogy | Sue Sentance, King's College London | https://blogs.kcl.ac.uk/cser/primm/ |

---

## Course Overview

| Field | Details |
|-------|---------|
| **Course Title** | Python Programming for Kids: Intermediate Programme |
| **Target Age Group** | 10–14 years (Primary 5–6 advanced, Secondary 1–2) |
| **Duration** | 48 sessions (48 hours total) |
| **Session Length** | 60 minutes |
| **Recommended Schedule** | 2 sessions / week × 24 weeks, OR 1 session / week × 48 weeks |
| **Class Size** | 8–14 students (1 instructor); 14–20 with a teaching assistant |
| **Prerequisites** | Block-based programming experience (Scratch / equivalent) recommended; basic computer literacy required |
| **Primary IDE** | Thonny (https://thonny.org/) — bundled Python, beginner-friendly debugger |
| **Secondary IDE** | Replit (capstone, sharing) and VS Code (optional, advanced students) |
| **Graphics Library** | `turtle` (built-in) for Units 1–6; `pgzero` (Pygame Zero) for Unit 7 |
| **Python Version** | Python 3.11 or later |

---

## Alignment with Cambridge Computing

### Cambridge Lower Secondary Computing (0860) — Stages 7–9 — Primary Anchor

| Strand | How This Course Addresses It | Sessions |
|--------|------------------------------|----------|
| **Computational Thinking — Decomposition, Pattern Recognition, Abstraction, Algorithms** | Pseudocode, flowcharts, trace tables, top-down function design | 5, 10, 15, 22, 29, 43, 46 |
| **Programming — Sequence, Selection, Iteration, Variables, Sub-routines** | Whole course; selection in U2, iteration in U2–U3, sub-routines in U5 | 1–48 |
| **Data Types & Structures** | Int, float, string, bool, list, tuple, dict | 2, 4, 19–23 |
| **Data Representation** | Discussed in U1 (binary as enrichment) and U6 (file encoding) | 2, 31–32 |
| **Digital Literacy & Safe Computing** | File handling boundaries, error messages, attribution of code | 31–35, 47 |

### Cambridge IGCSE Computer Science (0478) 2026–2028 — Forward Anchor

| Section | Topic | Sessions |
|---------|-------|----------|
| **§7 Algorithm Design** | Pseudocode, flowcharts, trace tables, test data | 5, 10, 11, 22, 29, 43, 46 |
| **§10 Programming — Core** | Sequence, selection, iteration | 1–18 |
| **§10 Programming — Data Types** | Integer, real, char, string, Boolean | 2, 4 |
| **§10 Programming — String Manipulation** | Length, indexing, slicing, upper/lower | 4 |
| **§10 Programming — Arrays** | 1D arrays (Python lists), 2D arrays as lists of lists | 19–24, 39 |
| **§10 Programming — Procedures & Functions** | Parameters, return values, scope | 25–30 |
| **§10 Programming — File Handling** | Read and write text files | 31–32 |
| **§10 Programming — Library Routines** | `random`, `math`, `datetime`, MOD/DIV/ROUND equivalents | 34–35 |
| **§10 Standard Algorithms** | Linear search, bubble sort, totalling, counting, max/min/average | 14, 21, 22 |

### Cambridge Primary Computing (0072 / 0059) — Bridge

This course is positioned as the **text-based bridge** from Primary block-based programming (Scratch, micro:bit) into Lower Secondary Python. Students arriving with Scratch fluency will recognise the underlying concepts (events, loops, conditionals) but learn to express them in text.

---

## Alignment with Singapore MOE Frameworks

### Code for Fun (CFF) — Bridge from Primary to Secondary

Primary CFF uses Scratch / PictoBlox. Secondary CFF and the optional CFF Plus modules introduce Python. **This 48-session course mirrors the CFF Secondary Python pathway** while adding the depth needed for O-Level Computing 7155.

### O-Level Computing (Syllabus 7155) — Module Mapping

| 7155 Module | Course Coverage | Sessions |
|-------------|-----------------|----------|
| **Module 1: Algorithms** | Pseudocode, flowcharts, trace tables, test data | 5, 10, 11, 22, 29, 43, 46 |
| **Module 2: Programming** | Sequence, selection, iteration, variables, lists | 1–24 |
| **Module 4 — Programming sub-strands** | Built-in functions, string manipulation, list operations (min, max, average, search), check digits | 4, 14, 21, 22 |
| **Module 3: Data & Information** | Lists, dictionaries, file I/O, simple data persistence | 19–23, 31–35 |
| **Module 5: Internet & Communication** | Touched in capstone if students publish via Replit | 48 |

### 21st Century Competencies (21CC) Mapping

| 21CC Domain | Competencies Developed | Sessions |
|-------------|------------------------|----------|
| **Critical & Inventive Thinking** | Problem decomposition, debugging, algorithmic thinking | All; especially 5, 10, 22, 29, 43–47 |
| **Communication, Collaboration & Information Skills** | Pair programming, code review, project showcase | 6, 12, 18, 24, 30, 36, 42, 47–48 |
| **Civic Literacy & Cross-cultural Skills** | Attribution of code, ethical use of libraries, responsible publishing | 34, 47–48 |

### EdTech Masterplan 2030 — Digital Literacy & Technological Skills (DLTS)

| DLTS Competency | Course Coverage | Sessions |
|-----------------|-----------------|----------|
| **Computational Thinking** | Decomposition, abstraction, algorithms, debugging | All sessions |
| **Coding & Programming** | Python text-based programming | All sessions |
| **Digital Information Management** | Files, lists, dictionaries, simple persistence | 19–23, 31–36 |
| **Digital Knowledge Currency** | Using documentation, libraries, online help | 34–35, 47 |
| **Digital Safety & Responsibility** | Attribution, error messages, validating user input | 11, 33, 34 |

---

## CSTA K-12 Cross-Walk

CSTA Level 2 (Grades 6–8, ages 11–14) is the closest international standard. Coverage:

| CSTA Standard | Description | Sessions |
|---------------|-------------|----------|
| **2-AP-10** | Use flowcharts/pseudocode to design algorithms | 5, 10, 22, 29, 43 |
| **2-AP-11** | Create clearly named variables of different data types | 2, 3, 4 |
| **2-AP-12** | Design programs combining control structures | 8–18 |
| **2-AP-13** | Decompose problems using procedures with parameters | 25–30 |
| **2-AP-14** | Use libraries with attribution | 34–35, 40–41 |
| **2-AP-16** | Iteratively develop programs through incremental work | 6, 12, 18, 24, 30, 36, 42, 43–48 |
| **2-AP-17** | Systematically test and refine programs | 11, 33, 46–47 |
| **2-AP-19** | Document programs with comments | All from S6 onward |
| **2-DA-07/08/09** | Collect, transform, and refine data using lists/dicts | 19–24, 31–36 |

---

## Course-Level Learning Objectives

By the end of this 48-session course, students will be able to:

1. Set up a Python development environment, write, save, run, and debug Python programs using Thonny.
2. Use variables and constants of all standard data types (`int`, `float`, `str`, `bool`, `list`, `tuple`, `dict`) and convert between them with type-casting.
3. Manipulate strings using indexing, slicing, length, case conversion, and concatenation.
4. Design algorithms using pseudocode and flowcharts before coding, and verify correctness using trace tables.
5. Apply selection (`if`/`elif`/`else`), iteration (`for`, `while`), and loop control (`break`, `continue`) to solve problems.
6. Implement and explain standard algorithms: linear search, bubble sort, totalling, counting, finding max/min/average.
7. Decompose problems into reusable functions with parameters, return values, and appropriate scope.
8. Read from and write to text files, handle errors with `try`/`except`, and use built-in modules (`random`, `math`, `datetime`).
9. Define classes with attributes and methods, and create multiple objects to model real-world entities.
10. Build a small interactive game using Pygame Zero, applying OOP and event-driven programming.
11. Plan, build, test, debug, polish, and present an original capstone project demonstrating accumulated skills.
12. Communicate technical work clearly through code comments, design documents, and a final showcase.

---

## Tools & Materials

### Software / Platform

- [ ] **Thonny IDE** (https://thonny.org/) — primary IDE Sessions 1–42
- [ ] **Replit** (https://replit.com/) — for sharing/capstone, Sessions 43–48
- [ ] **Python 3.11+** — bundled with Thonny
- [ ] **Pygame Zero** (`pip install pgzero`) — installed before Session 40
- [ ] Web browser with internet — for documentation lookup
- [ ] (Optional) **VS Code** with Python extension — for advanced students

### Hardware Requirements

- [ ] One laptop / desktop per student (Windows, macOS, or Linux)
- [ ] Minimum 4 GB RAM, 2 GB free disk space
- [ ] Headphones (Unit 7 — game audio)
- [ ] Projector / screen-sharing for instructor demonstrations

### Print Materials

- [ ] Per-session worksheet (provided in `LessonPlans/`)
- [ ] Pseudocode reference sheet (Appendix A)
- [ ] Flowchart symbols reference sheet (Appendix B)
- [ ] Python syntax cheat sheet (Appendix C)
- [ ] Common error messages glossary (Appendix D)

---

## Unit Summaries

> **Detailed lesson plans and worksheets for each unit are in the `LessonPlans/` folder.**
> Each unit file contains all 6 sessions with: lesson plan (objectives, materials, procedure, differentiation, assessment, teacher notes) and student worksheet.

### Unit 1 — Python Foundations & Computational Thinking (Sessions 1–6)
File: `LessonPlans/Unit1_Python_Foundations_and_Computational_Thinking.md`
Students set up Thonny, write their first Python programs, master variables and the four primary data types, type-casting, arithmetic, and string indexing/slicing. They learn to design programs using pseudocode and flowcharts before coding. The unit ends with a Personal Profile App project that consolidates input, variables, strings, and arithmetic.

### Unit 2 — Decision Making & Iteration Foundations (Sessions 7–12)
File: `LessonPlans/Unit2_Decision_Making_and_Iteration_Foundations.md`
Students learn Boolean logic, comparison operators, and the full `if`/`elif`/`else` family. Logical operators (`and`, `or`, `not`) and nested conditions follow. The unit introduces `while` loops, trace tables (a Cambridge IGCSE staple), and structured input validation using normal/boundary/invalid test data. Capped with a Number Guessing Game project.

### Unit 3 — Loops, Repetition & Turtle Graphics (Sessions 13–18)
File: `LessonPlans/Unit3_Loops_Repetition_and_Turtle_Graphics.md`
Students master `for` loops with `range()`, the standard loop patterns (totalling, counting, finding max/min/average), nested loops, and loop control (`break`, `continue`). The Turtle module makes loops visual and intuitive. The Geometric Art Generator project ties everything together creatively.

### Unit 4 — Lists & Standard Algorithms (Sessions 19–24)
File: `LessonPlans/Unit4_Lists_and_Standard_Algorithms.md`
Students learn lists, list methods, and iteration patterns. They implement two standard algorithms required by IGCSE 0478 and O-Level 7155: **linear search** and **bubble sort**. Tuples and dictionaries are introduced as complementary data structures. The Quiz & Leaderboard App project applies search and sort to real data.

### Unit 5 — Functions & Modular Design (Sessions 25–30)
File: `LessonPlans/Unit5_Functions_and_Modular_Design.md`
Students learn to define and call functions, pass parameters, return values, and reason about scope. Default parameters and top-down design with pseudocode follow. The Modular Math Helper project demands at least five custom functions, enforcing modular thinking.

### Unit 6 — File I/O, Errors & Built-in Modules (Sessions 31–36)
File: `LessonPlans/Unit6_File_IO_Errors_and_Modules.md`
Students read and write text files, handle errors gracefully with `try`/`except`, and explore the `random`, `math`, and `datetime` modules. They learn the discipline of testing with normal/boundary/invalid data. The Journal Application project persists user data across runs.

### Unit 7 — Object-Oriented Programming & Game Mini-Project (Sessions 37–42)
File: `LessonPlans/Unit7_OOP_and_Game_Mini_Project.md`
Students learn classes, objects, methods, and attributes. With this OOP foundation, they move to Pygame Zero — a beginner-friendly game library — to build a Mini Arcade Game. Inheritance is touched as a stretch concept for advanced students.

### Unit 8 — Capstone Project & Showcase (Sessions 43–48)
File: `LessonPlans/Unit8_Capstone_Project_and_Showcase.md`
Students design, build, test, polish, debug, and present an original Python project of their choosing. The unit walks them through professional development habits: design documents, version control basics, code review, and final showcase. Assessment is portfolio-based.

---

## Assessment Framework

### Formative Assessment (Continuous)

- **Per-session worksheets** — completed and reviewed during/after each session
- **Code observation** — instructor circulates and notes who needs intervention
- **Peer code review** — Sessions 12, 24, 36, 47 — students read each other's code
- **Trace-table exercises** — Sessions 10, 22, 46 — checks dry-running ability
- **Debug challenges** — embedded in worksheets; students must fix broken code

### Summative Assessment (Project-Based)

| Project | Session | Weight | Assessed Skills |
|---------|---------|--------|-----------------|
| Project 1 — Personal Profile App | 6 | 5% | Variables, strings, arithmetic, input |
| Project 2 — Number Guessing Game | 12 | 5% | Selection, iteration, validation |
| Project 3 — Geometric Art Generator | 18 | 10% | Loops, functions, turtle |
| Project 4 — Quiz & Leaderboard | 24 | 10% | Lists, search, sort |
| Project 5 — Modular Math Helper | 30 | 10% | Functions, modular design |
| Project 6 — Journal Application | 36 | 10% | File I/O, errors, modules |
| Project 7 — Mini Arcade Game | 42 | 15% | OOP, Pygame Zero |
| **Capstone Project** | 48 | 35% | Plan, build, test, polish, present |

### Capstone Rubric (4-Point)

| Criterion | Excellent (4) | Good (3) | Satisfactory (2) | Needs Improvement (1) |
|-----------|---------------|----------|------------------|----------------------|
| **Functionality** | All features work; handles edge cases | All core features work; minor edge-case gaps | Core features work with bugs | Major features missing or broken |
| **Code Quality** | Modular, well-named, commented; uses functions and OOP appropriately | Mostly modular and clear | Some structure, some duplication | Monolithic, unclear, no comments |
| **Algorithm Design** | Pseudocode/flowchart matches code; trace table verifies behaviour | Design artefacts present and mostly accurate | Design artefacts present but partial | No design artefacts |
| **Creativity & Originality** | Original concept with personal flair | Personalised version of standard concept | Standard concept | Direct copy of example |
| **Presentation** | Clear demo, articulates design choices, handles questions | Clear demo with minor gaps | Demo runs but explanation thin | Cannot demo or explain |

---

## Differentiation Strategies

### For Advanced Learners
- **Stretch challenges** in every worksheet — typically introduce a more elegant or efficient approach
- **Algorithm efficiency** discussions — compare bubble sort to "insertion sort" (Unit 4)
- **Inheritance** stretch sidebar in Unit 7
- **Recursion** as enrichment in Unit 5
- **VS Code + Git** introduction for capstone

### For Learners Needing Support
- **Starter code skeletons** with TODO comments
- **Pair programming** — pair with a confident peer, with rotating "driver / navigator" roles
- **Step-debugger demos** — use Thonny's variable inspector to make state visible
- **Annotated worked examples** — each new concept introduced with a fully-explained solved example
- **Pseudocode-only versions** of harder problems — they design, instructor codes

---

## Teacher Notes

- **Install Thonny ahead of time** on every machine. The Session 1 setup will fail if students are downloading on a slow network.
- **The instructor must run every worksheet themselves** before teaching. This is the single biggest factor in session quality.
- **Use the step-debugger early** (Session 2). Students who learn to use Thonny's debugger from Day 1 reach Unit 5 much faster.
- **Pseudocode is non-negotiable** from Session 5 onward — Cambridge IGCSE 0478 requires students to read and write pseudocode for the 15-mark scenario question.
- **Trace tables become muscle memory** by Session 22. Don't skip them just because students protest.
- **The capstone is a portfolio piece** — encourage students to add it to a Replit profile and (with parental consent) share to family.

---

## Sources and References

- [Cambridge Lower Secondary Computing (0860)](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-lower-secondary/curriculum/computing/)
- [Cambridge IGCSE Computer Science 0478 — 2026–2028 syllabus](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-igcse-computer-science-0478/)
- [Cambridge Primary Computing (0072 / 0059)](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-primary/curriculum/computing/)
- [SEAB O-Level Computing 7155 — 2026 syllabus](https://www.seab.gov.sg/files/O%20Lvl%20Syllabus%20Sch%20Cddts/2026/7155_y26_sy.pdf)
- [MOE O-Level Computing — Teaching & Learning Syllabus](https://www.moe.gov.sg/-/media/files/secondary/syllabuses/science/o-level-computing-teaching-and-learning-syllabus.pdf)
- [IMDA Code for Fun Programme](https://www.imda.gov.sg/how-we-can-help/code-for-fun)
- [IMDA Code for Fun — Primary](https://www.imda.gov.sg/how-we-can-help/code-for-fun/code-for-fun-primary)
- [Code@SG — Code for Fun Secondary](https://codesg.imda.gov.sg/in-schools/code-for-fun/secondary)
- [MOE Digital Literacy & Technological Skills](https://www.moe.gov.sg/education-in-sg/educational-technology-journey/edtech-masterplan/digital-literacy-and-technological-skills)
- [MOE EdTech Masterplan 2030](https://www.moe.gov.sg/education-in-sg/educational-technology-journey/edtech-masterplan)
- [MOE 21st Century Competencies](https://www.moe.gov.sg/education-in-sg/21st-century-competencies)
- [CSTA K-12 Computer Science Standards](https://csteachers.org/k12standards/interactive/)
- [Thonny — Python IDE for Beginners](https://thonny.org/)
- [Pygame Zero documentation](https://pygame-zero.readthedocs.io/)
- [Harvard Creative Computing Curriculum](https://creativecomputing.gse.harvard.edu/guide/)
- [PRIMM Pedagogy — King's College London](https://blogs.kcl.ac.uk/cser/primm/)

---

*Curriculum designed for kids' coding programmes blending Cambridge International computing standards with Singapore MOE digital literacy frameworks.*
