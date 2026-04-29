# Roblox Studio Intermediate: Lesson Plans & Worksheets
## Unit 1: Roblox Studio Fundamentals & Luau Scripting Foundations (Sessions 1-4)

### Unit Overview

Unit 1 opens the Roblox Studio Intermediate course by establishing a professional working environment and the programming fundamentals that students will rely on throughout the entire curriculum. Students begin by touring the Roblox Studio interface in depth — learning not just where each panel is, but why it is designed the way it is and how professional Roblox developers use it. They then build fluency with parts, models, materials, and the Workspace hierarchy, learning to construct clean, organised game worlds. The unit continues into Luau scripting, introducing variables, data types, the Output window, and the critical distinction between Scripts and LocalScripts. By Session 4, students are writing structured functions, implementing control flow with `if/elseif/else`, `for` loops, and `while` loops, and building a complete traffic light system from scratch. Every session pairs a detailed teacher-facing lesson plan with a hands-on student worksheet, ensuring that theory and practice remain inseparable.

---

### Session 1: Course Introduction & Roblox Studio Environment

---

#### SESSION 1 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 1 of 24 |
| **Title** | Course Introduction & Roblox Studio Environment |
| **Unit** | Unit 1: Roblox Studio Fundamentals & Luau Scripting Foundations |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Identify and describe the purpose of at least six distinct panels in Roblox Studio (Explorer, Properties, Toolbox, Output, Command Bar, Script Editor) and explain when a developer would use each one.
2. Create a new Roblox Studio project with a professional workspace structure containing organised folders in ServerScriptService, ReplicatedStorage, StarterPlayer, and Workspace.
3. Navigate the 3D viewport using camera controls (right-click drag, WASD, scroll wheel, Focus) and use the Move, Scale, and Rotate tools with precision.
4. Summarise the course structure and articulate one personal learning goal related to Roblox game development.

##### Materials Needed

- Computer with Roblox Studio installed and logged into a Roblox account (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 1 Worksheet (printed or displayed digitally)
- Whiteboard or interactive whiteboard for brainstorm responses
- Sticky notes (optional) for goal-setting activity
- Timer or stopwatch for timed activities
- Teacher reference: Roblox Creator Hub documentation bookmarked at `https://create.roblox.com/docs`

##### Procedure

**0–5 min: Warm-Up — "What Makes a Roblox Game Stand Out?"**

- As students settle, display the following prompt on the board: *"Think of a Roblox game you really enjoy playing — one that feels well-made. What is one specific thing that makes it better than most other Roblox games?"*
- Allow 90 seconds of quiet thinking. Then invite five or six students to share. Write each response on the board.
- Typical responses: "the obby feels smooth," "the combat system is satisfying," "the UI looks clean," "you can collect things and see your score," "the map is detailed and beautiful."
- Group the responses into four columns: **Gameplay Feel**, **Visuals & Building**, **UI & Feedback**, **Systems & Scoring**. Leave the columns on the board.
- Say: *"Every single thing on this board is something you will be able to build by the end of this course. The goal of this Intermediate course is not just to make Roblox games — it is to make Roblox games that feel professional and that other players actually want to play."*

**5–15 min: Introduction — Course Overview & Professional Habits**

- Display the six-unit structure and walk through it at a high level:
  - **Unit 1** — Roblox Studio environment mastery and Luau scripting foundations.
  - **Unit 2** — Game mechanics: player interaction, tools, collectibles, and leaderboards.
  - **Unit 3** — Advanced scripting: data stores, remote events, and client-server architecture.
  - **Unit 4** — World building: terrain, lighting, atmosphere, and environmental design.
  - **Unit 5** — UI design, sound, animations, and game polish.
  - **Unit 6** — Capstone project: design, build, test, publish, and showcase.
- Emphasise the capstone project: *"In the final sessions, you will build YOUR game from scratch — one that you designed, coded, and can publish on Roblox for the whole world to play. Everything we do before that is preparing you for that moment."*
- Introduce three professional habits students will practise every session:
  1. **Save constantly** — use Ctrl+S after every meaningful change. Roblox Studio can crash.
  2. **Name things clearly** — parts, models, scripts, and folders use descriptive names in PascalCase.
  3. **Organise first** — create the folder structure before adding any content.
- Tell students: *"When professional Roblox developers start a new project, the first thing they do is set up the Explorer hierarchy. That is exactly what we will do today."*

**15–35 min: Guided Practice — Roblox Studio Interface Deep Dive**

- Open Roblox Studio on the projector. Click **New > Baseplate** to create a fresh project. Walk through each panel slowly, keeping students hands-on at their own machines:

  1. **Explorer Panel (right side)** — *"This is your game's family tree. Every single object in your game lives here — parts, scripts, cameras, lighting, everything. Think of it as the blueprint of your entire game."* Expand the default hierarchy: show `Workspace`, `Players`, `Lighting`, `ReplicatedStorage`, `ServerScriptService`, `ServerStorage`, `StarterGui`, `StarterPack`, `StarterPlayer`. Say: *"Each of these services has a specific job. We will learn what each one does over the coming weeks."*

  2. **Properties Panel (right side, below Explorer)** — *"When you select any object in the Explorer or in the viewport, this panel shows you every setting for that object — its position, colour, size, material, whether it is anchored, whether players can walk through it."* Select the Baseplate part. Show Name, Position, Size, BrickColor, Material, Anchored, CanCollide. Change the BrickColor to demonstrate live updating.

  3. **Toolbox (left side or View menu)** — *"The Toolbox is Roblox's library of community-created models, meshes, images, audio, and plugins. Think of it as an asset store."* Open the Toolbox, search for "tree" to demonstrate. Say: *"We will mostly build our own objects in this course, but knowing the Toolbox exists is important. Always check the creator and ratings before using community assets."*

  4. **Output Panel (View > Output)** — *"This is your debugging window — your window into what the game is doing while it runs. Every time a script prints something or an error occurs, it appears here."* If not visible, go to View > Output. Say: *"If your game does something unexpected, the Output panel will almost always tell you what went wrong. Always have this open."*

  5. **Command Bar (View > Command Bar)** — *"The Command Bar lets you run single lines of Luau code instantly, without writing a full script. It is perfect for quick tests."* Type `print("Hello, Roblox!")` in the Command Bar and press Enter. Show the output. Say: *"We will use this a lot for quick experiments."*

  6. **Script Editor** — *"This is where you write Luau code. Double-click any script in the Explorer to open it here."* Insert a Script into Workspace (right-click Workspace > Insert Object > Script). Double-click it. Show the default `print("Hello world!")` code. Show syntax highlighting. Say: *"This editor has auto-complete, colour coding, and error highlighting. It is a real code editor built right into Roblox Studio."*

- After the tour, demonstrate the **3D navigation controls**:
  - **Right-click + WASD** — fly through the scene like a first-person camera.
  - **Scroll wheel** — zoom in and out.
  - **Middle mouse button drag** — pan the view.
  - **F key** — focus on the selected object (centres the camera on it).
  - **Move tool (Ctrl+1)**, **Scale tool (Ctrl+2)**, **Rotate tool (Ctrl+3)** — show each one on the Baseplate or a new Part.

- Say: *"Now you have seen every tool you will use this course. On your worksheet, you are going to go find them all yourself."*

**35–60 min: Independent Practice — Project Setup & Interface Scavenger Hunt**

- Direct students to Part 1 of the worksheet (Interface Scavenger Hunt). Set a timer for 10 minutes.
- Students locate each panel and feature listed, writing down where it is and what it does.
- After the scavenger hunt, direct students to Part 2 (Project Setup Checklist). They create their personal course project. They follow the checklist to:
  - Create a new Baseplate project and save it with a descriptive name.
  - Create organised folders in the Explorer: a `Models` folder in Workspace, a `GameScripts` folder in ServerScriptService, a `SharedAssets` folder in ReplicatedStorage.
  - Add a Part to Workspace and name it descriptively.
  - Delete the default Script from Workspace (to keep things clean).
- Circulate the room. Check that:
  - Folder names use PascalCase (e.g., `GameScripts`, not `game_scripts` or `gamescripts`).
  - The Output window is visible.
  - Students can navigate the 3D viewport using right-click + WASD.
  - Students have located and can name all six panels.
- If a student finishes early, direct them to the Bonus Challenge on the worksheet.

**60–75 min: Extension — Camera Controls Obstacle Course & Goal Setting**

- **Camera Controls Obstacle Course (8 minutes):**
  - Place four Parts at different locations in the Workspace (teacher can describe positions or pre-place them). Students must navigate to each Part using only the camera controls and press F to focus on it. They write down the Name of each Part they find on their worksheet.
  - Say: *"Being fast with camera controls saves you hours over a long project. The best Roblox developers can fly around their game world as easily as walking down a hallway."*

- **Goal Setting (7 minutes):**
  - Direct students to Part 3 of the worksheet. Read the prompts aloud:
    - *"Write the name of a Roblox game you would love to build by the end of this course."*
    - *"Write three specific skills you want to master."*
    - *"Write one thing about Roblox Studio or scripting that confused you before or that you want to understand better."*
  - Students write independently.

**75–85 min: Sharing & Discussion**

- Invite 3–4 volunteers to share one goal from their worksheet. Affirm each response: *"That is a great, specific goal — we will get to exactly that in Unit [X]."*
- Ask: *"What was the hardest panel to find during the scavenger hunt?"* Discuss briefly.
- Ask: *"Can anyone explain why the Explorer panel is so important?"* Guide to the answer: *"Because every object in your game is managed through the Explorer. If something is not in the Explorer, it does not exist in your game."*

**85–90 min: Closure & Preview**

- Quick check: *"Raise your hand if you can name at least five Roblox Studio panels right now."* Scan the room.
- Preview Session 2: *"Next session, we go deep into Parts, Models, and building. You will construct a small scene — a room or a playground — using everything Roblox Studio offers for 3D building."*
- Remind students: *"Save your project right now. Use Ctrl+S. You will need it again next session."*

##### Differentiation

**Support:**
- Provide a printed annotated screenshot of the Roblox Studio interface with each panel labelled and numbered, so students can use it as a reference map during the scavenger hunt.
- Pair students who struggle with navigation with a confident partner during the independent project setup phase; the stronger student acts as a guide, not a doer.
- Pre-create the folder structure in a starter project file that struggling students can open, then explore the structure rather than build it from scratch.

**Extension:**
- Challenge advanced students to explore the **Game Settings** (File > Game Settings) and write down three settings they think would be useful for a professional game (e.g., permissions, genre, playable devices).
- Ask them to investigate the difference between `ServerScriptService`, `ReplicatedStorage`, and `StarterPlayerScripts` in the Explorer, and write a one-paragraph explanation of when you would use each.
- Have them open the Command Bar and experiment with at least three different `print()` statements, including one that uses string concatenation.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Identifies Studio panels | Cannot locate or name panels | Names 2–3 panels with guidance | Names and describes 5–6 panels independently | Names all 6+ panels, explains purpose and workflow connection |
| Project folder structure | Project not created or has no folders | Created project but folders are missing or misnamed | All required folders created with correct PascalCase names | All folders correct; explains why the structure matters for large games |
| 3D navigation | Cannot move the camera or use tools | Uses one navigation method only | Uses right-click+WASD, scroll, and focus confidently | Navigates fluently, uses all tools (Move, Scale, Rotate) with snapping |
| Professional habits | No saving or naming conventions used | Inconsistent saving or naming | Saves consistently; uses correct naming conventions | Saves, names correctly, and explains the habit to a peer |

##### Teacher Notes

- Roblox Studio requires an active internet connection and a Roblox account. Ensure all students are logged in before the session begins. If any student does not have an account, create one with parental consent beforehand.
- The Output panel is not visible by default. You will need to explicitly tell students to go to View > Output. This is a critical step — students who do not have the Output panel open will struggle to debug scripts in later sessions.
- Some students may be tempted to explore the Toolbox and insert community models. This is fine for exploration, but remind them that for this course, they will primarily build their own objects to develop their skills.
- The Command Bar is also not visible by default. Go to View > Command Bar. It is an excellent tool for quick experiments.
- Windows users may experience slow performance if their computer does not meet Roblox Studio's minimum requirements. If a student's machine is lagging, advise them to reduce the graphics quality in File > Studio Settings > Rendering.
- Collect worksheets (or check them digitally) at the end of the session. The goal-setting section gives you valuable insight into each student's confidence level and specific interests.

---

#### SESSION 1 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 1: Course Introduction & Roblox Studio Environment**

---

##### Part 1: Interface Scavenger Hunt

**Instructions:** Open Roblox Studio on your computer and create a new Baseplate project. Your mission is to locate each feature listed below. Check the box when you find it, then write a short description of what it does in the "Purpose" column. You have **10 minutes** — go!

| # | Feature to Find | Found? | Purpose (what does it do?) |
|---|----------------|--------|---------------------------|
| 1 | **Explorer Panel** (right side) | [ ] | ____________________________________________ |
| 2 | **Properties Panel** (below Explorer) | [ ] | ____________________________________________ |
| 3 | **Toolbox** (left side or View menu) | [ ] | ____________________________________________ |
| 4 | **Output Panel** (View > Output) | [ ] | ____________________________________________ |
| 5 | **Command Bar** (View > Command Bar) | [ ] | ____________________________________________ |
| 6 | **Script Editor** (double-click a script) | [ ] | ____________________________________________ |
| 7 | **3D Viewport** (centre of screen) | [ ] | ____________________________________________ |
| 8 | **Home Tab** (top ribbon) | [ ] | ____________________________________________ |
| 9 | **Model Tab** (top ribbon) | [ ] | ____________________________________________ |
| 10 | **Move / Scale / Rotate tools** (top toolbar) | [ ] | ____________________________________________ |

**My score: _________ / 10 features found**

**Bonus:** What keyboard shortcut zooms the camera to focus on a selected object?

Answer: _______________________________________________

---

##### Part 2: Project Setup Checklist

**Instructions:** Create your personal course project by following each step in order. Tick each box as you complete the step.

1. [ ] Open Roblox Studio and click **New > Baseplate**.
2. [ ] Go to **File > Save to Roblox As...** or **File > Save to File**. Name your project `IntermediateCourse_YourName` (replace `YourName` with your own name, no spaces).
3. [ ] In the **Explorer Panel**, find `Workspace`. Right-click it and select **Insert Object > Folder**. Name the folder `Models`.
4. [ ] Find `ServerScriptService` in the Explorer. Right-click it and insert a **Folder**. Name it `GameScripts`.
5. [ ] Find `ReplicatedStorage` in the Explorer. Right-click it and insert a **Folder**. Name it `SharedAssets`.

   Your Explorer should now contain these folders:
   ```
   Workspace
   └── Models (Folder)

   ServerScriptService
   └── GameScripts (Folder)

   ReplicatedStorage
   └── SharedAssets (Folder)
   ```

6. [ ] In the **Home** tab, click **Part** to insert a new Part into Workspace.
7. [ ] In the **Explorer**, find the new Part. Click its name and rename it to `TestBlock`.
8. [ ] With `TestBlock` selected, look at the **Properties Panel**. Change its **BrickColor** to any colour you like.
9. [ ] Change the **Material** property to `SmoothPlastic`.
10. [ ] Press **Ctrl+S** to save your project.

**Total steps completed: _________ / 10**

**Question:** Why do you think it is important to organise scripts into folders like `GameScripts` rather than leaving them loose in the Explorer?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 3: My Roblox Development Goals

**Instructions:** Answer each question thoughtfully. There are no wrong answers — this is about YOUR learning journey.

**1. My dream game:**

Describe a Roblox game you would love to have built and published by the end of this course. What genre is it? What is the most exciting feature?

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

**2. Three skills I want to master this course:**

| # | Skill I Want to Master | Which Unit Do You Think Covers This? |
|---|----------------------|-------------------------------------|
| 1 | __________________________________ | Unit _____ |
| 2 | __________________________________ | Unit _____ |
| 3 | __________________________________ | Unit _____ |

**3. One thing I found confusing before that I want to understand this course:**

> _______________________________________________________________________________
>
> _______________________________________________________________________________

**4. Rate your current confidence with Roblox Studio (circle one):**

`Never Used It` — `Used It a Little` — `Comfortable` — `Confident` — `I Could Teach It`

---

##### Part 4: Navigation Challenge

**Instructions:** Use the camera controls you learned to navigate to different parts of your Baseplate world. Complete each challenge:

1. **Fly-through:** Hold right-click and use WASD to fly around the Baseplate. Move to all four corners. Done? [ ] Yes

2. **Zoom mastery:** Use the scroll wheel to zoom in until you can see the texture of the Baseplate up close. Then zoom out until you can see the entire plate from far away. Done? [ ] Yes

3. **Focus snap:** Select your `TestBlock` in the Explorer, then press **F** to focus the camera on it. Did the camera snap to the block? [ ] Yes

4. **Tool practice:** Use the **Move tool (Ctrl+1)** to move your TestBlock to a new position. Use the **Rotate tool (Ctrl+3)** to rotate it 45 degrees. Use the **Scale tool (Ctrl+2)** to make it twice as wide.

   Final position of TestBlock (check Properties): X: _______ Y: _______ Z: _______

---

##### Part 5: Explorer Hierarchy Diagram

**Instructions:** Fill in the blanks to complete the default Roblox Studio Explorer hierarchy. Write the correct service name in each blank.

```
Game
├── Workspace            ← Where all 3D objects live
├── Players              ← Tracks connected players
├── [A] ________________ ← Controls lighting, atmosphere, time of day
├── [B] ________________ ← Assets shared between server and client
├── [C] ________________ ← Scripts that only run on the server
├── ServerStorage        ← Server-only storage (clients cannot see)
├── StarterGui           ← UI screens given to each player
├── [D] ________________ ← Tools given to each player
├── StarterPlayer        ← Player character settings and scripts
└── SoundService         ← Controls game audio
```

**A:** ______________________________
**B:** ______________________________
**C:** ______________________________
**D:** ______________________________

---

##### Reflection

1. What is the most surprising or interesting thing you discovered about Roblox Studio today?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Why do you think professional Roblox developers care so much about naming and organising objects in the Explorer? Can you think of a situation where a messy project would cause a real problem?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge

Open the **Command Bar** (View > Command Bar). Try typing each of these Luau commands one at a time and pressing Enter. Write down what happens in the Output window.

1. `print("My name is " .. "YOUR_NAME_HERE")`

   Output: _______________________________________________

2. `print(10 + 25)`

   Output: _______________________________________________

3. `print(#workspace:GetChildren())`

   Output: _______________________________________________ What do you think this number represents?

   Your guess: _______________________________________________

*Save your project! You will use it again in Session 2.*

---

### Session 2: Parts, Models, and the Workspace Hierarchy

---

#### SESSION 2 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 2 of 24 |
| **Title** | Parts, Models, and the Workspace Hierarchy |
| **Unit** | Unit 1: Roblox Studio Fundamentals & Luau Scripting Foundations |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Create and configure all five Part types (Block, Sphere, Cylinder, Wedge, MeshPart) and explain when to use each shape for different game elements.
2. Modify at least six key Part properties (Color, Material, Transparency, Anchored, CanCollide, Size) and explain how each property affects gameplay.
3. Group Parts into Models using the Explorer hierarchy and demonstrate how moving a Model's PrimaryPart moves the entire group.
4. Construct a small scene (a room or playground) using at least eight Parts with varied shapes, materials, and colours, organised into named Models.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project from Session 1 (`IntermediateCourse_YourName`)
- Projector or screen-share for teacher demonstrations
- Session 2 Worksheet (printed or digital)
- Whiteboard for drawing hierarchy diagrams
- Reference images of simple game environments (obbies, tycoons, showcases) — display on a slide or printed handout

##### Procedure

**0–5 min: Warm-Up — "Building Blocks of the Real World"**

- As students settle, ask: *"Look around this room. If you had to rebuild this room in Roblox Studio using only basic shapes — blocks, spheres, cylinders, and wedges — how would you do it? What shapes would you use for the desk? The chair? The door?"*
- Take three or four responses. Students will say things like "blocks for the desk," "cylinders for chair legs," "a wedge for a ramp."
- Say: *"Every Roblox game you have ever played is built from these same basic shapes — or from meshes that started as basic shapes. Today you will learn to build like a professional: choosing the right shape, setting the right properties, and organising everything into clean Models."*

**5–15 min: Introduction — Part Types and Properties**

- Open Roblox Studio on the projector. Open the project from Session 1 or a fresh Baseplate.
- In the **Home** tab, click the dropdown arrow next to the **Part** button. Show each Part type:

  1. **Block** — *"The most common Part. A rectangular box. Used for floors, walls, platforms, buildings — anything boxy."* Insert one and name it `Floor`.
  2. **Sphere** — *"A perfectly round ball. Used for decorations, collectibles, projectiles, planets."* Insert one and name it `Decoration`.
  3. **Cylinder** — *"A tube shape. Used for columns, pipes, wheels, tree trunks, coins."* Insert one and name it `Pillar`.
  4. **Wedge** — *"A triangle-shaped block. Used for ramps, roofs, slopes, stairs."* Insert one and name it `Ramp`.
  5. **MeshPart** — *"A custom 3D shape imported from external software or the Toolbox. We will explore this more in later units. For now, know it exists."*

- For each Part, select it and walk through Properties in the Properties panel:
  - **Color / BrickColor** — *"The visual colour of the Part. Click the colour box to open the picker."*
  - **Material** — *"Changes the surface texture. Try SmoothPlastic, Wood, Grass, Neon, Metal, Glass."* Demonstrate changing material — show how Neon makes Parts glow.
  - **Transparency** — *"A value from 0 (fully visible) to 1 (invisible). Set it to 0.5 to make the Part semi-transparent — like glass."*
  - **Anchored** — *"If true, the Part stays in place even if other things hit it. If false, it falls and bounces with gravity. ALWAYS anchor parts that should not move — floors, walls, platforms."*
  - **CanCollide** — *"If true, players and other Parts cannot pass through it. If false, things go straight through it — like a ghost wall."*
  - **Size** — *"The dimensions of the Part in studs (Roblox units). A character is about 5 studs tall. Use this to judge scale."*

**15–35 min: Guided Practice — Building a Room Together**

- Say: *"We are going to build a simple room together — four walls, a floor, and a ceiling. Then we will add furniture."*
- Guide students step by step. Students follow along at their machines:

  **Step 1: Floor**
  - Insert a Block Part. Rename it `Floor`.
  - Set Size to `(40, 1, 40)` — a wide, thin platform.
  - Set Position to `(0, 0, 0)`.
  - Set Material to `SmoothPlastic`. Set Color to a light grey.
  - Check **Anchored** = true.

  **Step 2: Walls**
  - Insert a Block Part. Rename it `WallNorth`.
  - Set Size to `(40, 12, 1)`. Position to `(0, 6, -20)`.
  - Set **Anchored** = true. Set Material to `Brick`. Set Color to warm red.
  - Say: *"The wall is 12 studs tall — about twice as tall as a player character. The Y position is 6 because the wall's centre needs to be 6 studs above the floor."*
  - Duplicate (Ctrl+D) and create `WallSouth` at Position `(0, 6, 20)`.
  - Create `WallEast`: Size `(1, 12, 40)`, Position `(20, 6, 0)`.
  - Create `WallWest`: Size `(1, 12, 40)`, Position `(-20, 6, 0)`.

  **Step 3: Grouping into a Model**
  - Select all five Parts (Floor + 4 walls) by holding Ctrl and clicking each one in the Explorer.
  - Press **Ctrl+G** to group them into a **Model**.
  - Rename the Model to `Room`.
  - Say: *"Now these five Parts are children of the Room Model. If we move the Model, all the Parts move together. This is how you organise complex builds."*
  - Show setting the Model's **PrimaryPart** property: select the Model in Explorer, go to Properties, click the PrimaryPart field, then click the Floor in the viewport. Say: *"PrimaryPart tells Roblox which Part is the 'anchor' of the Model. When you use code to move a Model, it moves relative to the PrimaryPart."*

  **Step 4: Adding Furniture**
  - Add a table: Block Part, Size `(8, 1, 4)`, Position above the floor, Material = `Wood`. Name it `Table`.
  - Add a chair: Block Part (seat) + Block Part (back) grouped into a Model called `Chair`.
  - Add a lamp: Cylinder Part (base) + Sphere Part (bulb, Material = `Neon`, Color = yellow). Group into `Lamp`.
  - Drag the furniture Models into the `Room` Model in the Explorer.

- Say: *"Look at your Explorer now. You should see a clean hierarchy: Room contains Floor, four Walls, Table, Chair, and Lamp. This is how professional developers organise their games."*

**35–60 min: Independent Practice — Build Your Own Scene**

- Direct students to Part 2 of the worksheet. They will build their own scene independently. They can choose one of three options:
  - **Option A: Playground** — slide (wedge ramp), swings (cylinders), sandbox (transparent walls), seesaw.
  - **Option B: Bedroom** — bed, desk, wardrobe, window (transparent Part), lamp.
  - **Option C: Free choice** — any scene with at least 8 Parts, 3 different shapes, 3 different materials, and 2 Models.
- Requirements:
  - At least 8 Parts total.
  - At least 3 different Part shapes used.
  - At least 3 different Materials used.
  - At least 2 named Models in the Explorer.
  - All Parts must be Anchored.
  - All Parts must have descriptive names (not `Part`, `Part2`, `Part3`).
- Circulate the room. Common issues:
  - Parts falling through the floor — Anchored is not checked.
  - Parts named `Part` — remind students to rename everything.
  - Parts not aligned properly — show the **Snap to Grid** feature (Model tab > toggle snap, set increment).
- If a student finishes early, direct them to the Bonus Challenge on the worksheet.

**60–75 min: Extension — Advanced Properties & Special Effects**

- Demonstrate advanced Part properties for students who are ready:
  - **Reflectance** — makes metal Parts reflect the environment.
  - **CastShadow** — turn off shadows for small decorative Parts to improve performance.
  - **CollisionGroup** — preview concept: Parts can belong to groups that ignore collisions between each other.
- Challenge: *"Add a secret room to your scene. Use a Part with Transparency = 1 and CanCollide = false as a hidden entrance. A player who walks into the invisible wall will discover the secret room behind it."*
- Students who complete this write about it in their worksheet's Extension section.

**75–85 min: Sharing & Discussion — Scene Gallery Walk**

- Ask 3–4 students to share their screen and give a 60-second tour of their scene.
- For each presentation, ask the class: *"What is one thing they did really well? What is one suggestion for improvement?"*
- Discuss: *"How did naming and organising your Parts into Models help you while building? Would it have been harder without Models?"*
- Guide to the conclusion: *"When you have 50 or 100 Parts, Models are essential. Without them, your Explorer becomes an unreadable mess and you cannot find anything."*

**85–90 min: Closure & Preview**

- Quick check: *"Raise your hand if you can name all five Part types."* Call on one student to list them.
- Preview Session 3: *"Next session, we give our game a brain — we start writing Luau code. You will learn variables, data types, and how to make your game talk to you through the Output window."*
- Remind students: *"Save your project right now. Ctrl+S. Your scene will be used again in future sessions."*

##### Differentiation

**Support:**
- Provide a printed "Part Properties Cheat Sheet" listing each property name, what it does, and its valid values — students can refer to this while building.
- Pre-build the Room (floor and walls) and let struggling students focus on adding furniture and organising Models, reducing the build-from-scratch burden.
- Use the Move tool's grid snapping (Model tab > set Move increment to 1 stud) so Parts align neatly without requiring manual precision.

**Extension:**
- Challenge advanced students to use **Unions** (Model tab > Negate + Union) to create custom shapes by combining or subtracting Parts — for example, cutting a door-shaped hole in a wall.
- Ask them to add **SurfaceGui** to a Part and display text (like a sign or poster) — a preview of UI concepts from Unit 5.
- Have them experiment with the **Lighting** service: change TimeOfDay in the Properties panel and observe how it affects the scene. Write a short paragraph about how lighting changes the mood.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Part types | Cannot create or name Part types | Creates 1–2 types, cannot explain differences | Creates 4+ Part types and explains when to use each | Creates all 5 types, chooses optimal shapes for purpose |
| Properties mastery | Cannot change properties | Changes 1–2 properties with guidance | Confidently modifies 5+ properties (Color, Material, Transparency, Anchored, CanCollide, Size) | Uses properties creatively (Neon glow, transparency for glass, etc.) |
| Model organisation | No Models used; Parts are loose | 1 Model created but naming is poor | 2+ well-named Models with correct hierarchy | Clean hierarchy; uses PrimaryPart; explains benefits of Models |
| Scene construction | Fewer than 4 Parts; scene incomplete | 4–7 Parts; limited variety in shapes/materials | 8+ Parts; 3+ shapes; 3+ materials; all Anchored and named | Detailed scene with creative use of properties and excellent organisation |

##### Teacher Notes

- The most common beginner mistake: forgetting to set **Anchored = true**. When students press Play (F5) and their entire room falls apart and flies away, it is almost always because Parts are not anchored. Emphasise this repeatedly.
- Grid snapping is extremely helpful at this stage. Show students how to enable it in the Model tab and set the increment to 1 or 2 studs for precise alignment.
- Students will discover that rotating Parts changes their orientation but the Size property stays the same — a Part with Size `(10, 1, 4)` will still report those dimensions regardless of rotation. If students get confused, explain that Size describes the Part's local dimensions, not its world-space footprint.
- MeshParts require an external 3D model file (.fbx or .obj) to be useful. Do not spend significant time on MeshParts today — mention them as a preview for later units.
- Some students may want to use the Toolbox to insert pre-made models. Allow this for decoration, but require that at least 8 Parts in their scene are built by hand.

---

#### SESSION 2 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 2: Parts, Models, and the Workspace Hierarchy**

---

##### Part 1: Part Types Knowledge Check

**Instructions:** Fill in the table below. For each Part type, describe what it looks like, give one example of how you would use it in a game, and sketch the shape.

| Part Type | Description | Game Use Example | Sketch |
|-----------|-------------|-----------------|--------|
| **Block** | _________________________ | _________________________ | [draw here] |
| **Sphere** | _________________________ | _________________________ | [draw here] |
| **Cylinder** | _________________________ | _________________________ | [draw here] |
| **Wedge** | _________________________ | _________________________ | [draw here] |
| **MeshPart** | _________________________ | _________________________ | [draw here] |

**Properties Matching:** Match each property (left) to its correct description (right). Write the correct letter in the blank.

| Property | | Description |
|----------|---|-------------|
| 1. Anchored | ____ | A. Makes the Part partially or fully see-through (0 to 1). |
| 2. CanCollide | ____ | B. Changes the surface texture (Wood, Metal, Neon, etc.). |
| 3. Transparency | ____ | C. Prevents the Part from falling or being pushed by physics. |
| 4. Material | ____ | D. The visual colour of the Part. |
| 5. Color | ____ | E. Determines whether players and objects can pass through the Part. |
| 6. Size | ____ | F. The dimensions of the Part in studs (X, Y, Z). |

**Answers:** 1.____ 2.____ 3.____ 4.____ 5.____ 6.____

---

##### Part 2: Build Your Own Scene

**Instructions:** Choose one of the three scene options below (or create your own with teacher approval). Build the scene in Roblox Studio, following the requirements checklist.

**Choose one:**
- [ ] **Option A: Playground** — slide, swings, sandbox, seesaw, bench
- [ ] **Option B: Bedroom** — bed, desk, wardrobe, window, lamp
- [ ] **Option C: Free choice** — describe your scene: ____________________________________

**Requirements Checklist:**

| # | Requirement | Done? |
|---|------------|-------|
| 1 | At least **8 Parts** in total | [ ] |
| 2 | At least **3 different Part shapes** used (Block, Sphere, Cylinder, Wedge) | [ ] |
| 3 | At least **3 different Materials** used | [ ] |
| 4 | At least **2 named Models** grouping related Parts | [ ] |
| 5 | **All Parts are Anchored** | [ ] |
| 6 | **All Parts have descriptive names** (no "Part", "Part2") | [ ] |
| 7 | Scene is **saved** (Ctrl+S) | [ ] |

**List the Models you created and what Parts are inside each one:**

Model 1 name: `____________________`
- Parts inside: ________________________________________________________________

Model 2 name: `____________________`
- Parts inside: ________________________________________________________________

Model 3 name (if applicable): `____________________`
- Parts inside: ________________________________________________________________

---

##### Part 3: Explorer Hierarchy Diagram

**Instructions:** Draw the Explorer hierarchy for your scene. Show every Model and Part, using indentation to show parent-child relationships.

```
Workspace
├── Models (Folder)
│   ├── _____________________________ (Model)
│   │   ├── _________________________
│   │   ├── _________________________
│   │   └── _________________________
│   ├── _____________________________ (Model)
│   │   ├── _________________________
│   │   └── _________________________
│   └── (add more if needed)
├── Baseplate
└── Camera
```

**Question:** Why is it better to group related Parts into a Model instead of leaving them as individual Parts in Workspace?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 4: Properties Experiment

**Instructions:** Create a new Block Part for each experiment below. Observe what happens and write the result.

**Experiment 1: Transparency**
- Create a Part. Set Transparency to `0.5`. Set Material to `Glass`.
- What does it look like? _______________________________________________
- Now set Transparency to `1`. Can you still see it in the viewport? _______________
- Can you select it in the Explorer? _______________

**Experiment 2: CanCollide**
- Create a Part. Set CanCollide to `false`. Set Anchored to `true`.
- Press Play (F5) and walk your character into the Part.
- What happens? _______________________________________________

**Experiment 3: Anchored**
- Create a Part. Set Anchored to `false`. Position it 20 studs above the floor.
- Press Play (F5).
- What happens to the Part? _______________________________________________

**Experiment 4: Neon Material**
- Create a Part. Set Material to `Neon`. Set Color to bright yellow.
- What visual effect does Neon produce? _______________________________________________

---

##### Part 5: Properties Challenge — Design a Special Part

**Instructions:** Using what you know about properties, design a Part with each of these characteristics. Write the property values you would use.

1. **A glass window** — you can see through it, but players cannot walk through it.
   - Transparency: _______ CanCollide: _______ Material: _______

2. **A hidden trap** — completely invisible, players walk through it and fall.
   - Transparency: _______ CanCollide: _______ Anchored: _______

3. **A glowing lamp** — emits a warm glow, players can walk through it.
   - Material: _______ Color: _______ CanCollide: _______

4. **An immovable steel wall** — solid, heavy-looking, nothing can push it.
   - Material: _______ Anchored: _______ CanCollide: _______

---

##### Reflection

1. What was the most challenging part of building your scene today? How did you solve it?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. If you had to explain the Anchored property to a friend who has never used Roblox Studio, what would you say?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge

Create a **secret room** in your scene:

1. Build a small enclosed room behind one of your walls.
2. Add a special Part that acts as a hidden entrance: set its **Transparency to 1** (invisible) and **CanCollide to false** (walk-through).
3. Place this invisible Part where a wall would normally be — players who walk into that spot will discover they can pass through and enter the secret room.
4. Put something interesting inside the secret room (a glowing Neon Part, a special coloured object, etc.).

Did you complete the secret room? [ ] Yes [ ] No

How would a player discover the hidden entrance? _______________________________________________

*Save your project! You will build on this scene in future sessions.*

---

### Session 3: Luau Fundamentals — Variables, Data Types, and Output

---

#### SESSION 3 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 3 of 24 |
| **Title** | Luau Fundamentals — Variables, Data Types, and Output |
| **Unit** | Unit 1: Roblox Studio Fundamentals & Luau Scripting Foundations |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Explain the difference between Scripts and LocalScripts in Roblox, including where each type runs (server vs client) and where each should be placed in the Explorer hierarchy.
2. Declare and use variables of four core Luau data types (`string`, `number`, `boolean`, `nil`) using the `local` keyword with descriptive naming conventions.
3. Use `print()` to output variable values, string concatenation (`..`), and basic arithmetic expressions to the Output window for debugging.
4. Write well-organised code with single-line comments (`--`) and multi-line comments (`--[[ ]]`), explaining why comments matter in collaborative projects.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project from Session 2
- Projector or screen-share for teacher demonstrations
- Session 3 Worksheet (printed or digital)
- Whiteboard for illustrating variable concepts
- Output panel must be open (View > Output) on all machines

##### Procedure

**0–5 min: Warm-Up — "Variables in Real Life"**

- Ask: *"Before we write any code, tell me — if you were building an obby game, what information would the game need to remember about each player?"*
- Accept answers. Write them on the board: name, score, health, what level they are on, if they are alive, how fast they move.
- Say: *"Every single one of these is a variable — a named container that stores a value. Today we learn how to create variables in Luau, the programming language that powers every Roblox game."*

**5–15 min: Introduction — Scripts vs LocalScripts**

- Open Roblox Studio on the projector. Explain the client-server model with a simple diagram on the whiteboard:

  ```
  [Roblox Server] ←————→ [Player 1's Client]
                  ←————→ [Player 2's Client]
                  ←————→ [Player 3's Client]
  ```

- Say: *"When a Roblox game runs, there is ONE server that controls the game world, and every player has their own client (their screen, their keyboard, their camera). Scripts run on the server. LocalScripts run on the client."*

- **Script (Server Script):**
  - Runs on the server.
  - Can change the game world for ALL players.
  - Place in: `ServerScriptService`, `Workspace`, or inside server-side objects.
  - Example uses: managing scores, spawning enemies, handling game logic.
  - Say: *"If you want something to happen for EVERYONE — like a door opening or a score updating — use a Script."*

- **LocalScript (Client Script):**
  - Runs on ONE player's computer.
  - Can only affect that player's experience (camera, UI, input).
  - Place in: `StarterPlayerScripts`, `StarterCharacterScripts`, `StarterGui`, or inside a Tool.
  - Example uses: handling keyboard input, updating the player's GUI, camera effects.
  - Say: *"If you want something to happen for just ONE player — like detecting when they press a key or showing them a menu — use a LocalScript."*

- Demonstrate: insert a Script into ServerScriptService. Insert a LocalScript into StarterPlayerScripts. Open each one and show that the code looks the same — the only difference is where it runs.

**15–35 min: Guided Practice — Variables, Data Types, and print()**

- In the Script inside ServerScriptService, delete the default code. Type each line live, with students following along:

```lua
-- ============================================
-- Session 3: Variables and Data Types in Luau
-- ============================================

-- STRINGS: text inside double quotes or single quotes
local playerName = "Alex"
local greeting = 'Welcome to the game!'

-- NUMBERS: integers and decimals (Luau uses one type for both)
local health = 100
local speed = 16.5
local score = 0

-- BOOLEANS: true or false only
local isAlive = true
local hasKey = false

-- NIL: represents "nothing" or "no value"
local mysteryItem = nil

-- Printing variables to the Output window
print("=== Player Info ===")
print("Name: " .. playerName)
print("Health: " .. health)
print("Speed: " .. speed)
print("Is Alive: " .. tostring(isAlive))
print("Has Key: " .. tostring(hasKey))

-- String concatenation with ..
local fullGreeting = greeting .. " " .. playerName .. "!"
print(fullGreeting)

-- Basic arithmetic
local damage = 25
local remainingHealth = health - damage
print(playerName .. " took " .. damage .. " damage!")
print("Remaining health: " .. remainingHealth)

-- More arithmetic operations
local doubleScore = score * 2
local halfHealth = health / 2
local healthSquared = health ^ 2
local remainder = health % 7

print("Double score: " .. doubleScore)
print("Half health: " .. halfHealth)
print("Health squared: " .. healthSquared)
print("100 divided by 7, remainder: " .. remainder)
```

- After each section, press **F5** (Play) to run the game and show the Output. Then press **F5** again to stop. Point to each line in the Output and trace it back to the print statement that produced it.

- Key teaching points:
  - *"The `local` keyword means this variable only exists inside this script. Always use `local` — it is a best practice."*
  - *"The `..` operator joins strings together. It is called concatenation. In Python you use `+`, in Luau you use `..` — two dots."*
  - *"When you concatenate a number or boolean with a string, Luau automatically converts numbers for you, but you need `tostring()` for booleans."*
  - *"The `print()` function is your best friend for debugging. When something goes wrong, add print statements to figure out what your variables actually contain."*

**35–60 min: Independent Practice — Students Write Their Own Variables Script**

- Direct students to Part 2 of the worksheet. They write a complete script that:
  - Declares at least 2 string variables.
  - Declares at least 3 number variables.
  - Declares at least 2 boolean variables.
  - Uses `print()` to display all variable values.
  - Uses string concatenation to create at least one combined message.
  - Uses at least 3 different arithmetic operations.
  - Includes at least 5 comments explaining the code.

- Students type their script into a new Script in ServerScriptService, run it with F5, and verify the output matches what they expected.

- Circulate the room. Common issues:
  - Using `+` instead of `..` for string concatenation — Luau uses `..`.
  - Forgetting `local` keyword — remind students to always use it.
  - Quotation mark mismatches — opening with `"` and closing with `'`.
  - Not pressing F5 to test — remind students to run frequently.

**60–75 min: Extension — Comments and Code Organisation**

- Introduce comments with a live demonstration:

```lua
-- This is a single-line comment. Luau ignores everything after --

--[[
    This is a multi-line comment.
    It starts with --[[ and ends with ]].
    Use it for longer explanations or to temporarily
    disable blocks of code during testing.
]]

-- GOOD comment: explains WHY, not WHAT
local maxHealth = 100  -- Cap health at 100 to prevent overpowered healing

-- BAD comment: states the obvious
local score = 0  -- Set score to 0
```

- Say: *"A good comment explains WHY you made a decision, not WHAT the code does. If someone reads `local score = 0`, they already know the score is being set to zero. But they do not know WHY the maximum health is 100 — that is worth a comment."*

- **Code organisation challenge:** Students reorganise their script from the Independent Practice into clearly labelled sections using comment headers:

```lua
-- ============================================
-- Game: [Your Game Name]
-- Author: [Your Name]
-- Date: [Today's Date]
-- Description: Character stats and game info
-- ============================================

-- === PLAYER INFORMATION ===
local playerName = "Alex"
-- (more variables here)

-- === COMBAT STATS ===
local health = 100
-- (more variables here)

-- === GAME STATE ===
local isGameOver = false
-- (more variables here)

-- === OUTPUT ===
print("=== Game Stats ===")
-- (print statements here)
```

- Students complete Part 4 of the worksheet (Debug Challenge) if time allows.

**75–85 min: Sharing & Discussion**

- Ask 2–3 students to share their Output window results with the class. For each, ask: *"Can anyone spot a line that uses concatenation? Can anyone spot a comment that explains WHY?"*
- Discussion question: *"Why do you think Roblox separates Scripts and LocalScripts? Why not just have one type that works everywhere?"*
- Guide to the answer: *"Security. If a player could run server-side code, they could cheat — give themselves infinite health, delete other players, break the game. By separating client and server, Roblox keeps the game safe."*

**85–90 min: Closure & Preview**

- Quick check: *"Name the four data types we learned today."* (string, number, boolean, nil)
- Ask: *"What does the `..` operator do?"* (String concatenation)
- Preview Session 4: *"Next session, we learn how to make decisions in code — if statements, loops, and functions. Your game will start thinking for itself."*
- Remind: *"Save your project! Ctrl+S."*

##### Differentiation

**Support:**
- Provide a printed "Luau Variables Cheat Sheet" with syntax for each data type, example declarations, and common errors to avoid.
- Allow struggling students to copy the teacher's demo code first, then modify it with their own variable names and values — scaffolding from copying to creating.
- Pair students so one types while the other watches the Output for errors — this builds debugging skills while reducing typing pressure.

**Extension:**
- Challenge advanced students to use the `type()` function to print the data type of each variable: `print(type(health))` outputs `number`. Have them verify all their variables.
- Ask them to research and use `string.upper()`, `string.lower()`, and `string.len()` on their string variables, printing the results.
- Have them experiment with `string.format()`: `print(string.format("Health: %d / %d", remainingHealth, maxHealth))` for formatted output.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Scripts vs LocalScripts | Cannot explain the difference | Knows they are different but cannot explain where each runs | Correctly explains server vs client and where to place each | Explains the security reasoning and gives game-dev examples |
| Variable declaration | Cannot declare a variable | Declares variables but forgets `local` or types | Uses `local`, correct naming, all 4 data types | Uses all types with descriptive names and explains type choices |
| print() and concatenation | Cannot use print() | Uses print() for simple values only | Uses print() with concatenation and arithmetic expressions | Uses print() strategically for debugging with formatted output |
| Comments and organisation | No comments in code | 1–2 comments, mostly obvious ("set x to 5") | 5+ comments explaining reasoning; code in labelled sections | Professional header, clear sections, WHY comments throughout |

##### Teacher Notes

- The Scripts vs LocalScripts distinction is conceptually challenging for younger students. Use the analogy: *"A Script is like a teacher making an announcement to the whole class (everyone hears it). A LocalScript is like whispering a note to one student (only they see it)."*
- Luau does not have separate `int` and `float` types — there is only `number`. If students have Python experience and ask about integers vs floats, explain that Luau handles both under `number`.
- The `..` concatenation operator is a common source of errors. Students will forget the space: `"Hello"..name` works but `"Hello " .. name` is more readable. Encourage spaces around `..`.
- `tostring()` is required when concatenating booleans with strings. Without it, students will get an error: `attempt to concatenate a boolean value`. Show this error on purpose so students learn to recognise it.
- If a student's script has an error, the Output panel will show the error in red with a line number. Teach students to read the error message and click on it to jump to the problematic line.

---

#### SESSION 3 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 3: Luau Fundamentals — Variables, Data Types, and Output**

---

##### Part 1: Scripts vs LocalScripts

**Instructions:** Read each scenario and decide whether you would use a **Script** or a **LocalScript**. Write your answer and explain why.

| # | Scenario | Script or LocalScript? | Why? |
|---|---------|----------------------|------|
| 1 | A player presses the "E" key to open a door. You need to detect the key press. | ________________ | _________________________________ |
| 2 | When a player collects a coin, add 10 points to the game's scoreboard for everyone to see. | ________________ | _________________________________ |
| 3 | Show a "Welcome!" message on a player's screen when they join the game. | ________________ | _________________________________ |
| 4 | Spawn a new enemy every 30 seconds in the game world. | ________________ | _________________________________ |
| 5 | Move the camera to a cinematic angle during a cutscene for one player. | ________________ | _________________________________ |

**Fill in the blanks:**

- Scripts run on the ________________ and can affect ________________ players.
- LocalScripts run on the ________________ and can only affect ________________ player.
- Scripts should be placed in ________________ or ________________.
- LocalScripts should be placed in ________________ or ________________.

---

##### Part 2: Write Your Own Variables Script

**Instructions:** In Roblox Studio, insert a new **Script** into **ServerScriptService**. Rename it `VariablesPractice`. Write a script that meets ALL the requirements below. Then press F5 to test it and paste your Output results.

**Requirements:**
- [ ] At least 2 `string` variables
- [ ] At least 3 `number` variables
- [ ] At least 2 `boolean` variables
- [ ] At least 1 variable set to `nil`
- [ ] Use `print()` to display all variable values
- [ ] Use string concatenation (`..`) in at least 2 print statements
- [ ] Use at least 3 different arithmetic operations (+, -, *, /, ^, %)
- [ ] Include at least 5 comments explaining your code

**Write your script here (or attach a screenshot):**

```lua
-- ============================================
-- Script: Variables Practice
-- Author: ____________________
-- Date: ____________________
-- ============================================

-- === STRING VARIABLES ===



-- === NUMBER VARIABLES ===



-- === BOOLEAN VARIABLES ===



-- === NIL VARIABLE ===



-- === OUTPUT ===



-- === ARITHMETIC ===



```

**Paste your Output results here:**

```
Line 1: _______________________________________________
Line 2: _______________________________________________
Line 3: _______________________________________________
Line 4: _______________________________________________
Line 5: _______________________________________________
Line 6: _______________________________________________
Line 7: _______________________________________________
Line 8: _______________________________________________
(add more lines as needed)
```

**Did your Output match what you expected?** [ ] Yes [ ] No — What was different? _______________

---

##### Part 3: Data Types Knowledge Check

**Instructions:** For each value below, write its Luau data type (`string`, `number`, `boolean`, or `nil`).

| Value | Data Type |
|-------|-----------|
| `"Hello World"` | ________________ |
| `42` | ________________ |
| `true` | ________________ |
| `3.14159` | ________________ |
| `nil` | ________________ |
| `false` | ________________ |
| `"100"` | ________________ |
| `0` | ________________ |

**Tricky question:** What is the difference between `100` and `"100"` in Luau?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 4: Debug Challenge

**Instructions:** Each code block below has ONE error. Find the error, explain what is wrong, and write the corrected line.

**Bug 1:**
```lua
local playerName = "Alex"
local greeting = "Hello, " + playerName
print(greeting)
```
Error: _______________________________________________
Corrected line: _______________________________________________

**Bug 2:**
```lua
local health = 100
local isAlive = true
print("Alive: " .. isAlive)
```
Error: _______________________________________________
Corrected line: _______________________________________________

**Bug 3:**
```lua
local score = 50
local message = "Your score is: " .. Score
print(message)
```
Error: _______________________________________________
Corrected line: _______________________________________________

**Bug 4:**
```lua
playerSpeed = 16
print("Speed: " .. playerSpeed)
```
Error: _______________________________________________
Corrected line: _______________________________________________

**Bug 5:**
```lua
local weapon = "Sword
print("Weapon: " .. weapon)
```
Error: _______________________________________________
Corrected line: _______________________________________________

---

##### Part 5: Arithmetic Practice

**Instructions:** Predict the output of each print statement. Write your prediction, then check it in Roblox Studio.

```lua
local a = 10
local b = 3

print(a + b)        -- Prediction: _______  Actual: _______
print(a - b)        -- Prediction: _______  Actual: _______
print(a * b)        -- Prediction: _______  Actual: _______
print(a / b)        -- Prediction: _______  Actual: _______
print(a % b)        -- Prediction: _______  Actual: _______
print(a ^ 2)        -- Prediction: _______  Actual: _______
print(a + b * 2)    -- Prediction: _______  Actual: _______
print((a + b) * 2)  -- Prediction: _______  Actual: _______
```

**Question:** Why do `a + b * 2` and `(a + b) * 2` give different results?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Reflection

1. What is the most important thing you learned about Luau scripting today?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Why is `print()` considered a developer's "best friend" for debugging? Give a specific example of when you would use it.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. In your own words, explain why you should always use the `local` keyword when declaring variables.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge

Use the `type()` function to check the data type of each variable below. Write the output.

```lua
local name = "Roblox"
local age = 18
local isOnline = true
local nothing = nil

print(type(name))       -- Output: _______________
print(type(age))        -- Output: _______________
print(type(isOnline))   -- Output: _______________
print(type(nothing))    -- Output: _______________
print(type(print))      -- Output: _______________  (Surprise! What type is a function?)
```

**Extra:** Try `string.len("Hello")` and `string.upper("hello")` in the Command Bar. What do they return?

- `string.len("Hello")` returns: _______________
- `string.upper("hello")` returns: _______________
- `string.lower("WORLD")` returns: _______________

*Save your project! You will build on this in Session 4.*

---

### Session 4: Luau Control Flow — Conditions, Loops, and Functions

---

#### SESSION 4 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 4 of 24 |
| **Title** | Luau Control Flow — Conditions, Loops, and Functions |
| **Unit** | Unit 1: Roblox Studio Fundamentals & Luau Scripting Foundations |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Write `if/elseif/else` conditional statements in Luau to make decisions based on variable values, using comparison operators (`==`, `~=`, `<`, `>`, `<=`, `>=`) and logical operators (`and`, `or`, `not`).
2. Implement `for` loops (numeric and generic) and `while` loops to repeat actions, including using `task.wait()` to control timing.
3. Define and call custom functions with parameters and return values, explaining how functions reduce code duplication.
4. Build a functional traffic light system in Roblox Studio that uses conditions, loops, and functions together to cycle through red, yellow, and green states.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project from Session 3
- Projector or screen-share for teacher demonstrations
- Session 4 Worksheet (printed or digital)
- Three coloured Parts pre-built (or built live) representing traffic light bulbs — red, yellow, green
- Whiteboard for drawing flowcharts

##### Procedure

**0–5 min: Warm-Up — "If This, Then That"**

- Display the prompt: *"Think about a traffic light. What rules does it follow?"*
- Take responses: *"If it is red, cars stop. If it is green, cars go. If it is yellow, cars slow down. It repeats forever."*
- Say: *"You just described three programming concepts without knowing it. The 'if red, then stop' part is a CONDITION. The 'it repeats forever' part is a LOOP. And if we wanted a single command called 'changeLight' that handles the whole process, that is a FUNCTION. Today we learn all three."*
- Draw a simple flowchart on the board: Start → Is it red? → Yes → Stop / No → Is it green? → Yes → Go / No → Slow down → Loop back to Start.

**5–15 min: Introduction — Conditional Statements**

- Open Roblox Studio. Create a new Script in ServerScriptService called `ControlFlowLesson`. Type live:

```lua
-- ============================================
-- Conditional Statements in Luau
-- ============================================

local health = 75
local playerName = "Alex"

-- Basic if/else
if health > 0 then
    print(playerName .. " is alive!")
else
    print(playerName .. " has been defeated!")
end

-- if/elseif/else for multiple conditions
if health >= 80 then
    print("Status: Healthy")
elseif health >= 50 then
    print("Status: Injured")
elseif health >= 20 then
    print("Status: Critical")
else
    print("Status: Defeated")
end

-- Comparison operators
print("--- Comparison Operators ---")
print("health == 75: " .. tostring(health == 75))   -- equal to
print("health ~= 100: " .. tostring(health ~= 100)) -- not equal to
print("health > 50: " .. tostring(health > 50))      -- greater than
print("health < 100: " .. tostring(health < 100))    -- less than
print("health >= 75: " .. tostring(health >= 75))     -- greater or equal
print("health <= 80: " .. tostring(health <= 80))     -- less or equal

-- Logical operators: and, or, not
local hasArmor = true
local hasShield = false

if health > 50 and hasArmor then
    print("Player is in good shape with armor!")
end

if hasArmor or hasShield then
    print("Player has some protection!")
end

if not hasShield then
    print("Player has no shield! Be careful!")
end
```

- Run with F5 and walk through each output line. Key points:
  - *"In Luau, `~=` means 'not equal to.' In Python it is `!=`, in Luau it is `~=`. This is the one that trips up everyone."*
  - *"Every `if` block MUST end with `end`. No colons, no indentation rules like Python — just `then` at the start and `end` at the finish."*
  - *"`and` means BOTH conditions must be true. `or` means AT LEAST ONE must be true. `not` flips true to false and vice versa."*

**15–35 min: Guided Practice — Loops**

- Continue in the same script or create a new section:

```lua
-- ============================================
-- Loops in Luau
-- ============================================

-- FOR LOOP: counting from start to finish
print("--- Counting 1 to 5 ---")
for i = 1, 5 do
    print("Count: " .. i)
end

-- FOR LOOP with step: counting by 2s
print("--- Counting by 2s ---")
for i = 0, 10, 2 do
    print("Even number: " .. i)
end

-- FOR LOOP counting down
print("--- Countdown ---")
for i = 5, 1, -1 do
    print(i .. "...")
end
print("Blast off!")

-- FOR LOOP through a table (array)
local fruits = {"Apple", "Banana", "Cherry", "Dragonfruit"}

print("--- Fruit List ---")
for index, fruit in ipairs(fruits) do
    print(index .. ": " .. fruit)
end

-- WHILE LOOP: runs as long as condition is true
local energy = 5

print("--- While Loop: Using Energy ---")
while energy > 0 do
    print("Energy remaining: " .. energy)
    energy = energy - 1
end
print("Out of energy!")

-- WHILE TRUE with task.wait() for timed loops
-- (We will use this pattern in the traffic light!)
-- while true do
--     print("This would run forever!")
--     task.wait(1) -- Wait 1 second before repeating
-- end
```

- Run with F5. Walk through outputs. Key points:
  - *"The `for` loop has three values: start, stop, and step. If you leave out the step, it defaults to 1."*
  - *"`ipairs()` is used to loop through a table (Luau's version of an array) in order. The `i` stands for index."*
  - *"A `while` loop keeps running as long as its condition is true. Be careful — if the condition never becomes false, the loop runs forever and freezes your game!"*
  - *"`task.wait(1)` pauses the script for 1 second. We use this in `while true do` loops to prevent the game from freezing. NEVER write a `while true do` loop without a `task.wait()` inside!"*

**35–60 min: Guided Practice — Functions + Traffic Light Build**

- **Part A: Functions Introduction (10 minutes)**

```lua
-- ============================================
-- Functions in Luau
-- ============================================

-- A simple function with no parameters
local function sayHello()
    print("Hello, welcome to the game!")
end

-- Call the function
sayHello()
sayHello()  -- We can call it as many times as we want!

-- A function with parameters
local function greetPlayer(name, score)
    print("Welcome, " .. name .. "! Your score is " .. score .. ".")
end

greetPlayer("Alex", 100)
greetPlayer("Jordan", 250)
greetPlayer("Sam", 0)

-- A function with a return value
local function calculateDamage(baseDamage, multiplier)
    local totalDamage = baseDamage * multiplier
    return totalDamage
end

local hit1 = calculateDamage(10, 1.5)
local hit2 = calculateDamage(25, 2.0)
print("Hit 1 damage: " .. hit1)
print("Hit 2 damage: " .. hit2)

-- A function that uses conditions
local function getHealthStatus(health)
    if health >= 80 then
        return "Healthy"
    elseif health >= 50 then
        return "Injured"
    elseif health >= 20 then
        return "Critical"
    else
        return "Defeated"
    end
end

print("Status at 90 HP: " .. getHealthStatus(90))
print("Status at 55 HP: " .. getHealthStatus(55))
print("Status at 10 HP: " .. getHealthStatus(10))
print("Status at 0 HP: " .. getHealthStatus(0))
```

- Key points:
  - *"Functions are reusable blocks of code. You write them once, call them many times. This is called DRY — Don't Repeat Yourself."*
  - *"Parameters are the inputs a function receives. Return values are the outputs it sends back."*
  - *"In Luau, we write `local function name()` — using `local` keeps the function scoped to this script."*

- **Part B: Traffic Light System (15 minutes)**

- First, build the traffic light in the 3D viewport:
  - Insert a Block Part (Size 4, 12, 4), name it `TrafficLightPole`, Material = Metal, Color = Dark Grey, Anchored = true.
  - Insert three Sphere Parts stacked vertically on top of the pole:
    - `RedLight` — Color = Red, Material = SmoothPlastic, Anchored = true.
    - `YellowLight` — Color = Yellow, Material = SmoothPlastic, Anchored = true.
    - `GreenLight` — Color = Green, Material = SmoothPlastic, Anchored = true.
  - Group all four Parts into a Model called `TrafficLight`.

- Insert a Script into the `TrafficLight` Model. Name it `TrafficController`. Write the complete script:

```lua
-- ============================================
-- Traffic Light Controller
-- Cycles through Red, Yellow, Green using
-- conditions, loops, and functions
-- ============================================

-- Get references to the light Parts
local redLight = script.Parent:FindFirstChild("RedLight")
local yellowLight = script.Parent:FindFirstChild("YellowLight")
local greenLight = script.Parent:FindFirstChild("GreenLight")

-- Function to turn off all lights (set them dim)
local function turnOffAllLights()
    redLight.Material = Enum.Material.SmoothPlastic
    yellowLight.Material = Enum.Material.SmoothPlastic
    greenLight.Material = Enum.Material.SmoothPlastic
    redLight.Color = Color3.fromRGB(100, 0, 0)       -- dim red
    yellowLight.Color = Color3.fromRGB(100, 100, 0)   -- dim yellow
    greenLight.Color = Color3.fromRGB(0, 100, 0)      -- dim green
end

-- Function to activate a specific light
local function activateLight(lightPart, brightColor)
    turnOffAllLights()  -- First turn off all lights
    lightPart.Material = Enum.Material.Neon  -- Make it glow
    lightPart.Color = brightColor             -- Set bright color
    print("Traffic light changed to: " .. lightPart.Name)
end

-- Function to determine what message to display
local function getTrafficMessage(lightName)
    if lightName == "RedLight" then
        return "STOP! Red light is active."
    elseif lightName == "YellowLight" then
        return "CAUTION! Yellow light - prepare to stop."
    elseif lightName == "GreenLight" then
        return "GO! Green light is active."
    else
        return "Unknown light state."
    end
end

-- Main loop: cycle through the lights forever
local cycleCount = 0

while true do
    cycleCount = cycleCount + 1
    print("=== Cycle " .. cycleCount .. " ===")

    -- Green light: 5 seconds
    activateLight(greenLight, Color3.fromRGB(0, 255, 0))
    print(getTrafficMessage("GreenLight"))
    task.wait(5)

    -- Yellow light: 2 seconds
    activateLight(yellowLight, Color3.fromRGB(255, 255, 0))
    print(getTrafficMessage("YellowLight"))
    task.wait(2)

    -- Red light: 5 seconds
    activateLight(redLight, Color3.fromRGB(255, 0, 0))
    print(getTrafficMessage("RedLight"))
    task.wait(5)
end
```

- Run with F5 and watch the traffic light cycle. Point out:
  - *"The `while true do` loop makes it run forever — just like a real traffic light."*
  - *"`task.wait(5)` pauses for 5 seconds between changes."*
  - *"The `activateLight` function takes care of turning off old lights and turning on the new one. Without this function, we would have to write the same 5 lines of code three times."*
  - *"The `getTrafficMessage` function uses `if/elseif/else` to return a different message for each state."*

**60–75 min: Independent Practice — Students Build Their Own Traffic Light**

- Students complete Part 3 of the worksheet: they build their own traffic light and write the controller script.
- **Extension challenge:** Add a pedestrian walk signal — a Part that turns Neon green when the traffic light is red (safe to walk) and Neon red otherwise.

**75–85 min: Sharing & Discussion**

- Ask 2–3 students to demonstrate their traffic lights. Run each one and watch the Output together.
- Discussion questions:
  - *"What would happen if we removed `task.wait()` from the while loop?"* (The game would freeze — the loop runs infinitely without yielding.)
  - *"Why did we create functions instead of writing all the code directly in the while loop?"* (Reusability, readability, easier to change.)
  - *"How would you add a blinking yellow mode that blinks 3 times before switching to red?"* (Use a for loop inside the while loop.)
- If time allows, demonstrate the blinking modification live:

```lua
-- Blinking yellow (add this before the red light section)
for blink = 1, 3 do
    activateLight(yellowLight, Color3.fromRGB(255, 255, 0))
    task.wait(0.5)
    turnOffAllLights()
    task.wait(0.5)
end
```

**85–90 min: Closure & Preview**

- Quick recap: *"Today we covered three huge concepts: conditions make decisions, loops repeat actions, and functions package code for reuse. These three tools are the foundation of ALL programming."*
- Preview Unit 2: *"Next session, we enter Unit 2 — Game Mechanics and Player Interaction. You will learn how to detect when a player touches a Part, make kill bricks, speed boosts, and jump pads. The real game-building starts now."*
- Remind: *"Save your traffic light project! You have earned it."*

##### Differentiation

**Support:**
- Provide the traffic light script pre-written with blanks for students to fill in (e.g., the timing values, the colour values, the function names) — reducing the typing burden while still requiring understanding.
- Create a printed flowchart template that students fill in before writing code — translating visual logic to code is easier than writing code from scratch.
- Allow struggling students to build a simpler two-state system (on/off) instead of the three-state traffic light.

**Extension:**
- Challenge advanced students to add a **countdown display** using a SurfaceGui and TextLabel on the traffic light pole that shows the seconds remaining for each state.
- Ask them to add a **pedestrian crossing signal** — a separate Part that turns green when the traffic light is red and vice versa, with a print message for pedestrians.
- Have them create a **configurable traffic light** where the timing for each state is stored in variables at the top of the script, making it easy to change without modifying the loop logic.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Conditional statements | Cannot write an if statement | Writes basic if/else but misses syntax (then, end) | Correctly uses if/elseif/else with comparison operators | Uses logical operators (and, or, not) in complex conditions |
| Loops | Cannot write a loop | Writes a for loop but cannot explain the parameters | Uses for and while loops correctly with task.wait() | Combines loops with conditions; explains infinite loop dangers |
| Functions | Cannot define a function | Defines a function but cannot use parameters or returns | Defines functions with parameters and return values | Creates multiple functions that call each other; explains DRY |
| Traffic light project | Not attempted or non-functional | Partially working (1–2 states cycle) | All 3 states cycle correctly with proper timing | Adds extensions (blinking, pedestrian signal, countdown) |

##### Teacher Notes

- The traffic light project is the capstone of Unit 1. It integrates variables, conditions, loops, and functions into one tangible, visual project. Students who complete this successfully have a strong foundation for Unit 2.
- `task.wait()` is the modern Roblox replacement for the older `wait()` function. Both work, but `task.wait()` is more precise and is the recommended approach. If students see `wait()` in online tutorials, tell them it still works but `task.wait()` is better practice.
- The `Enum.Material.Neon` syntax may be new to students. Explain briefly: *"Enums are predefined lists of valid values. `Enum.Material.Neon` is Roblox's way of saying 'the Neon material.' You will see Enums throughout Roblox scripting."*
- `Color3.fromRGB(r, g, b)` takes values from 0–255. Some students may confuse this with the 0–1 scale used by `Color3.new()`. Stick with `fromRGB` as it is more intuitive.
- Common mistake: students put the traffic light script in ServerScriptService instead of inside the TrafficLight Model. The script uses `script.Parent` to find the lights, so it MUST be a child of the Model. If a student's lights are not changing, check the script's location first.
- If time is very tight, the traffic light can be simplified to just change colours without the Neon/dim distinction — changing `Color` alone is sufficient to demonstrate the concept.

---

#### SESSION 4 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 4: Luau Control Flow — Conditions, Loops, and Functions**

---

##### Part 1: Conditional Statements Practice

**Instructions:** Write the Luau code to solve each challenge. Use `if/elseif/else` statements.

**Challenge 1: Grade Calculator**

Write a script that checks a student's `score` variable and prints their grade:
- 90 or above: "Grade: A"
- 80–89: "Grade: B"
- 70–79: "Grade: C"
- 60–69: "Grade: D"
- Below 60: "Grade: F"

```lua
local score = 85  -- Change this value to test different grades

-- Write your if/elseif/else statement below:








```

**Challenge 2: Game Access Check**

Write a script that checks TWO conditions: a player's `age` and whether they have a `ticket` (boolean). Print whether they can play:
- Age 13 or older AND has a ticket: "Welcome to the game!"
- Age 13 or older but no ticket: "You need a ticket to play."
- Under 13: "Sorry, you must be 13 or older."

```lua
local age = 14
local hasTicket = true

-- Write your conditional logic below:








```

**Challenge 3: Predict the Output**

What will each code block print? Write your prediction, then check in Roblox Studio.

```lua
local x = 10
local y = 20

if x > y then
    print("A")
elseif x == y then
    print("B")
else
    print("C")
end
```
Prediction: _______ Actual: _______

```lua
local isRaining = true
local hasUmbrella = false

if isRaining and hasUmbrella then
    print("Stay dry!")
elseif isRaining and not hasUmbrella then
    print("Getting wet!")
else
    print("Nice day!")
end
```
Prediction: _______ Actual: _______

---

##### Part 2: Loops Practice

**Instructions:** Write the code for each loop challenge.

**Challenge 1: Multiplication Table**

Write a `for` loop that prints the 7 times table from 7x1 to 7x10.

Expected output:
```
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
... (up to 7 x 10 = 70)
```

```lua
-- Write your for loop below:




```

**Challenge 2: Countdown Timer**

Write a `for` loop that counts down from 10 to 1, with a `task.wait(1)` between each number, then prints "Go!".

```lua
-- Write your countdown loop below:




```

**Challenge 3: Password Checker**

Write a `while` loop that keeps asking for a password (simulated with a variable). The loop should run a maximum of 3 times. If the password matches "roblox123", print "Access granted!" and stop. Otherwise, print "Wrong password, try again."

```lua
local correctPassword = "roblox123"
local attempts = 0
local maxAttempts = 3
local enteredPassword = "wrong"  -- Simulate wrong input

-- Write your while loop below:




-- After the loop, check if access was granted or attempts ran out:


```

**Challenge 4: Table Iteration**

Given the following table, write a `for` loop using `ipairs()` that prints each item with its index.

```lua
local inventory = {"Sword", "Shield", "Health Potion", "Map", "Key"}

-- Write your loop below:




```

Expected output:
```
1: Sword
2: Shield
3: Health Potion
4: Map
5: Key
```

---

##### Part 3: Build a Traffic Light

**Instructions:** Follow these steps to build and program a working traffic light in Roblox Studio.

**Step A: Build the Traffic Light (in the 3D viewport)**

1. [ ] Insert a **Block Part**. Name it `Pole`. Size: `(2, 14, 2)`. Material: Metal. Color: Dark grey. Anchored: true.
2. [ ] Insert a **Sphere Part**. Name it `RedLight`. Position it at the top of the pole. Color: `(100, 0, 0)` (dim red). Anchored: true.
3. [ ] Insert a **Sphere Part**. Name it `YellowLight`. Position it below RedLight. Color: `(100, 100, 0)` (dim yellow). Anchored: true.
4. [ ] Insert a **Sphere Part**. Name it `GreenLight`. Position it below YellowLight. Color: `(0, 100, 0)` (dim green). Anchored: true.
5. [ ] Select all four Parts and press **Ctrl+G** to group them into a Model.
6. [ ] Rename the Model to `TrafficLight`.

**Step B: Write the Controller Script**

7. [ ] Right-click the `TrafficLight` Model in Explorer > Insert Object > Script. Rename it `TrafficController`.
8. [ ] Delete the default code and write the traffic light controller script.

**Write your complete traffic light script below:**

```lua
-- ============================================
-- Traffic Light Controller
-- Author: ____________________
-- Date: ____________________
-- ============================================

-- Get references to the light Parts
local redLight = script.Parent:FindFirstChild("RedLight")
local yellowLight = script.Parent:FindFirstChild("YellowLight")
local greenLight = script.Parent:FindFirstChild("GreenLight")

-- Function to turn off all lights


-- Function to activate a specific light


-- Main loop: cycle through lights forever


```

9. [ ] Press **F5** to test. Does the traffic light cycle through all three colors? [ ] Yes [ ] No
10. [ ] Check the **Output window**. Do you see messages for each state change? [ ] Yes [ ] No

**If something is not working, check these common issues:**
- Is the script inside the TrafficLight Model (not in ServerScriptService)?
- Are the Part names exactly `RedLight`, `YellowLight`, `GreenLight` (case-sensitive)?
- Does your `while true do` loop have a `task.wait()` inside?

---

##### Part 4: Functions Practice

**Instructions:** Write the Luau functions described below.

**Challenge 1: Area Calculator**

Write a function called `calculateArea` that takes `width` and `height` as parameters and returns the area. Then call it three times with different values and print the results.

```lua
-- Write your function and test calls below:








```

**Challenge 2: Max Value Finder**

Write a function called `findMax` that takes two numbers and returns the larger one. Use an `if` statement inside the function.

```lua
-- Write your function below:






-- Test it:
print(findMax(10, 25))    -- Should print: 25
print(findMax(100, 50))   -- Should print: 100
print(findMax(7, 7))      -- Should print: 7
```

**Challenge 3: Greeting Generator**

Write a function called `generateGreeting` that takes a `name` and `timeOfDay` (string: "morning", "afternoon", "evening") and returns an appropriate greeting.

```lua
-- Write your function below:








-- Test it:
print(generateGreeting("Alex", "morning"))    -- Should print: Good morning, Alex!
print(generateGreeting("Sam", "evening"))     -- Should print: Good evening, Sam!
```

---

##### Part 5: Putting It All Together — Code Reading

**Instructions:** Read the following complete script carefully. Answer the questions below without running the code.

```lua
local function checkTemperature(temp)
    if temp >= 35 then
        return "Hot"
    elseif temp >= 20 then
        return "Warm"
    elseif temp >= 10 then
        return "Cool"
    else
        return "Cold"
    end
end

local temperatures = {32, 18, 25, 8, 40, 15}

for index, temp in ipairs(temperatures) do
    local status = checkTemperature(temp)
    print("Day " .. index .. ": " .. temp .. "C - " .. status)
end
```

**Question 1:** How many lines will this script print? _______

**Question 2:** What will the FIRST line of output be?

> _______________________________________________

**Question 3:** What will the FOURTH line of output be?

> _______________________________________________

**Question 4:** If we added the value `22` to the end of the `temperatures` table, what would the new last line of output be?

> _______________________________________________

**Question 5:** What does the `checkTemperature` function return when given the value `10`?

> _______________________________________________

---

##### Reflection

1. Which of the three concepts (conditions, loops, functions) was the most challenging for you today? Why?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Explain in your own words why `task.wait()` is essential inside a `while true do` loop.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. Give a real-world example (from a Roblox game you have played) where you think the game uses a loop.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge: Pedestrian Signal Extension

Add a **pedestrian walk signal** to your traffic light:

1. Insert a new Block Part next to the traffic light pole. Name it `WalkSignal`.
2. In your script, get a reference to it: `local walkSignal = script.Parent:FindFirstChild("WalkSignal")`
3. Modify your `while true do` loop so that:
   - When the traffic light is **RED**, the WalkSignal turns **Neon Green** (safe to cross).
   - When the traffic light is **GREEN** or **YELLOW**, the WalkSignal turns **Neon Red** (do not cross).
   - Before the WalkSignal changes from green to red, it **blinks 3 times** to warn pedestrians.

Write your modified loop code below:

```lua
-- Modified while true do loop with pedestrian signal:








```

Did you get the pedestrian signal working? [ ] Yes [ ] No

*Congratulations on completing Unit 1! Save your project — you will build on these skills in Unit 2.*
# Roblox Studio Intermediate: Lesson Plans & Worksheets
## Unit 2: Game Mechanics & Player Interaction (Sessions 5-8)

### Unit Overview

Unit 2 transitions students from foundational scripting into building real, playable game mechanics. Students begin by exploring the Player-Character-Humanoid hierarchy — the backbone of every Roblox experience — and learn to detect collisions using the Touched event, building kill bricks, speed boosts, and jump pads with proper debouncing techniques. They then move into the Tool system, creating custom weapons with Activated, Equipped, and Unequipped events and learning how StarterPack distributes tools to players. The unit deepens with the leaderstats system, where students build collectible coin systems with real-time scoreboard tracking. By Session 8, students integrate everything into a complete Obstacle Course (Obby) project with checkpoints, hazards, collectibles, and a leaderboard — their first fully playable Roblox game. Every session pairs a detailed teacher-facing lesson plan with a hands-on student worksheet, ensuring that theory and practice remain inseparable.

---

### Session 5: Player Character & Touched Events

---

#### SESSION 5 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 5 of 24 |
| **Title** | Player Character & Touched Events |
| **Unit** | Unit 2: Game Mechanics & Player Interaction |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Explain the Player → Character → Humanoid hierarchy in Roblox, including how to access the Humanoid from a Touched event and what properties the Humanoid controls (Health, WalkSpeed, JumpHeight).
2. Implement the `.Touched` event on Parts to detect when a player's character makes contact, and correctly identify the touching part's parent as the character model.
3. Build three functional game mechanics using Touched events: a kill brick, a speed boost pad, and a jump pad.
4. Apply the debouncing technique to prevent Touched events from firing multiple times and explain why debouncing is necessary.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project from Unit 1 (or a fresh Baseplate)
- Projector or screen-share for teacher demonstrations
- Session 5 Worksheet (printed or digital)
- Whiteboard for drawing the Player/Character/Humanoid hierarchy diagram
- Three pre-coloured Parts for demonstration (red kill brick, blue speed pad, green jump pad) — or build live

##### Procedure

**0–5 min: Warm-Up — "What Happens When You Touch Something in a Game?"**

- Display the prompt: *"In Roblox games, what happens when your character touches different things? Think of three examples."*
- Take responses. Typical answers: "lava kills you," "a coin disappears and gives points," "a speed pad makes you run faster," "a spring launches you into the air."
- Say: *"All of those are powered by one single event in Roblox: the Touched event. Today we learn how to use it — and by the end of the session, you will have built a kill brick, a speed boost, and a jump pad."*

**5–15 min: Introduction — The Player/Character/Humanoid Hierarchy**

- Open Roblox Studio. Press F5 to run the game. Open the Explorer and expand the `Players` service. Show the hierarchy:

  ```
  Players
  └── YourPlayerName (Player object)
      └── (Backpack, PlayerGui, etc.)

  Workspace
  └── YourPlayerName (Character Model)
      ├── Head (MeshPart)
      ├── Torso / UpperTorso (MeshPart)
      ├── Left Arm / LeftUpperArm (MeshPart)
      ├── Right Arm / RightUpperArm (MeshPart)
      ├── Left Leg / LeftUpperLeg (MeshPart)
      ├── Right Leg / RightUpperLeg (MeshPart)
      ├── HumanoidRootPart (Part)
      ├── Humanoid (Humanoid object)
      └── Animate (LocalScript)
  ```

- Draw the simplified version on the whiteboard:

  ```
  Player (in Players service)
      ↓ has a
  Character (Model in Workspace)
      ↓ contains a
  Humanoid (controls health, speed, jumping)
  ```

- Explain each level:
  - **Player** — *"The Player object represents the connected person. It lives in the Players service. It stores things like the player's name, their backpack (inventory), and their GUI."*
  - **Character** — *"The Character is the 3D model in the game world — the avatar you see running around. It is a Model in Workspace with body parts (Head, Torso, Arms, Legs) and a HumanoidRootPart."*
  - **Humanoid** — *"The Humanoid is the brain inside the Character. It controls Health, WalkSpeed, JumpHeight, and whether the character is alive. When we want to kill a player, change their speed, or make them jump higher, we change the Humanoid's properties."*

- Show key Humanoid properties in the Properties panel during Play mode:
  - `Health` — default 100. Set to 0 and the character dies.
  - `MaxHealth` — default 100.
  - `WalkSpeed` — default 16. Increase to make the player run faster.
  - `JumpHeight` — default 7.2. Increase for higher jumps.

- Stop the game (F5 again). Say: *"Now let's learn how to detect when a player TOUCHES a Part — and then change these Humanoid properties with code."*

**15–35 min: Guided Practice — Touched Event and Kill Brick**

- Create a red Part in the Workspace. Name it `KillBrick`. Set Color to bright red, Material to Neon, Size to `(10, 1, 10)`, Anchored = true.
- Insert a Script into the KillBrick. Name it `KillScript`. Type live:

```lua
-- ============================================
-- Kill Brick Script
-- Any player who touches this Part dies instantly
-- ============================================

local killBrick = script.Parent

-- This function runs every time something touches the kill brick
local function onTouched(otherPart)
    -- otherPart is the Part that touched us (e.g., a player's leg or arm)
    -- We need to find the Character model (the parent of the body part)
    local character = otherPart.Parent

    -- Check if the parent has a Humanoid (this confirms it is a player character)
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        -- Set health to 0 to kill the player
        humanoid.Health = 0
        print(character.Name .. " was killed by the KillBrick!")
    end
end

-- Connect the function to the Touched event
killBrick.Touched:Connect(onTouched)
```

- Run with F5. Walk the character onto the red brick. Show the character dying. Check the Output.

- Key teaching points:
  - *"When a player walks on the KillBrick, Roblox fires the `.Touched` event. The event passes `otherPart` — which is the specific body part that touched the brick (like the player's LeftFoot or RightLeg)."*
  - *"To find the Character model, we go UP one level: `otherPart.Parent`. The parent of LeftFoot is the Character model."*
  - *"We use `FindFirstChild('Humanoid')` to check if the thing that touched us is actually a player character. If a random Part falls on the kill brick, it does not have a Humanoid, so we skip it."*
  - *"`:Connect(onTouched)` links our function to the event. Every time the event fires, our function runs automatically."*

- Now introduce **debouncing**. Say: *"Watch the Output window carefully."* Walk on the kill brick again. Show that the print message fires MANY times — because many body parts touch the brick simultaneously.

- Say: *"This is a problem. If we were giving points instead of killing, the player would get 10 points for one coin instead of 1. We fix this with a technique called DEBOUNCING."*

```lua
-- ============================================
-- Kill Brick Script WITH DEBOUNCE
-- ============================================

local killBrick = script.Parent
local debounce = false  -- Flag to prevent multiple triggers

local function onTouched(otherPart)
    -- If we are already processing a touch, skip this one
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        debounce = true  -- Lock: prevent further triggers
        humanoid.Health = 0
        print(character.Name .. " was killed by the KillBrick!")
        task.wait(1)     -- Wait 1 second before allowing another trigger
        debounce = false -- Unlock: allow triggers again
    end
end

killBrick.Touched:Connect(onTouched)
```

- Run again. Show that the message now prints only once. Explain:
  - *"The `debounce` variable acts like a lock. When the first touch happens, we set it to `true` — locking the door. While the door is locked, any other touches are ignored. After 1 second, we unlock the door by setting it back to `false`."*

**35–60 min: Independent Practice — Speed Boost and Jump Pad**

- Guide students through building two more mechanics, then let them work independently:

- **Speed Boost Pad** (teacher demonstrates, students follow):

```lua
-- ============================================
-- Speed Boost Pad Script
-- Doubles the player's speed for 3 seconds
-- ============================================

local speedPad = script.Parent
local debounce = false

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        debounce = true

        -- Store original speed and apply boost
        local originalSpeed = humanoid.WalkSpeed
        humanoid.WalkSpeed = originalSpeed * 2
        print(character.Name .. " got a speed boost!")

        -- Change pad appearance to show it has been used
        speedPad.Color = Color3.fromRGB(100, 100, 100)  -- grey (used)
        speedPad.Material = Enum.Material.SmoothPlastic

        -- Wait for boost duration
        task.wait(3)

        -- Restore original speed
        humanoid.WalkSpeed = originalSpeed
        print(character.Name .. "'s speed boost ended.")

        -- Restore pad appearance
        speedPad.Color = Color3.fromRGB(0, 100, 255)  -- blue (ready)
        speedPad.Material = Enum.Material.Neon

        task.wait(1)  -- Cooldown before pad can be used again
        debounce = false
    end
end

speedPad.Touched:Connect(onTouched)
```

- **Jump Pad** (students build independently with worksheet guidance):

```lua
-- ============================================
-- Jump Pad Script
-- Launches the player into the air
-- ============================================

local jumpPad = script.Parent
local debounce = false
local LAUNCH_FORCE = 100  -- How high the player launches

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        debounce = true

        -- Find the HumanoidRootPart (the main physics part of the character)
        local rootPart = character:FindFirstChild("HumanoidRootPart")

        if rootPart then
            -- Apply an upward velocity to launch the player
            rootPart.AssemblyLinearVelocity = Vector3.new(0, LAUNCH_FORCE, 0)
            print(character.Name .. " was launched by the Jump Pad!")

            -- Visual feedback: pad flashes
            jumpPad.Color = Color3.fromRGB(255, 255, 255)
            task.wait(0.2)
            jumpPad.Color = Color3.fromRGB(0, 255, 0)
        end

        task.wait(0.5)
        debounce = false
    end
end

jumpPad.Touched:Connect(onTouched)
```

- Students build their own speed boost and jump pad, writing the scripts themselves using the worksheet as a guide. Circulate and assist.

**60–75 min: Extension — Custom Mechanics Challenge**

- Challenge students to create ONE additional Touched mechanic of their own design:
  - **Heal Pad** — restores health to maximum when touched.
  - **Shrink Zone** — reduces the character's scale temporarily.
  - **Teleporter** — moves the player to a different position.
  - **Gravity Flipper** — changes workspace gravity temporarily.
- Students who finish write about their custom mechanic in the Extension section of the worksheet.

- Example Heal Pad for reference:

```lua
-- ============================================
-- Heal Pad Script
-- Restores player health to maximum
-- ============================================

local healPad = script.Parent
local debounce = false

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        if humanoid.Health < humanoid.MaxHealth then
            debounce = true
            humanoid.Health = humanoid.MaxHealth
            print(character.Name .. " was healed to full health!")

            -- Visual feedback
            healPad.Color = Color3.fromRGB(255, 255, 255)
            task.wait(0.3)
            healPad.Color = Color3.fromRGB(0, 255, 100)

            task.wait(2)
            debounce = false
        end
    end
end

healPad.Touched:Connect(onTouched)
```

**75–85 min: Sharing & Discussion**

- Ask 2–3 students to demonstrate their mechanics. Run each game and test it live.
- Discussion questions:
  - *"Why do we check for `FindFirstChild('Humanoid')` instead of just assuming the touching Part belongs to a player?"* (Other Parts can touch it too — like falling debris or tools.)
  - *"What would happen if we removed the debounce from the speed boost?"* (The speed would multiply every time a body part touches — the player would move at 1000+ speed.)
  - *"Can you think of a game mechanic that should NOT use debouncing?"* (A moving platform that needs continuous contact detection.)

**85–90 min: Closure & Preview**

- Quick recap: *"Today we learned three things: the Player/Character/Humanoid hierarchy, the Touched event, and debouncing. These are the building blocks of almost every Roblox game mechanic."*
- Preview Session 6: *"Next session, we build custom tools — swords, gadgets, and weapons that players can equip and use. You will learn how tools work in Roblox."*
- Remind: *"Save your project! Ctrl+S."*

##### Differentiation

**Support:**
- Provide the kill brick script pre-written and let struggling students focus on understanding each line rather than typing it from scratch. Use colour-coded comments to highlight the key patterns.
- Create a "Touched Event Template" that students can copy and modify — changing only the mechanic inside the `if humanoid then` block.
- Pair weaker students with confident partners for the jump pad exercise, with clear roles: one types, one debugs.

**Extension:**
- Challenge advanced students to create a **teleporter pair** — two Parts that teleport the player between them using `HumanoidRootPart.CFrame = CFrame.new(x, y, z)`.
- Ask them to add **visual particle effects** using a ParticleEmitter inside the speed boost pad that activates during the boost.
- Have them create a **damage zone** that reduces health by 10 every second the player stands on it, using a `while` loop and `Humanoid.Health`.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Player/Character/Humanoid | Cannot describe the hierarchy | Knows the hierarchy exists but confuses levels | Correctly explains all three levels and how to access Humanoid | Explains hierarchy and demonstrates accessing properties in code |
| Touched event | Cannot write a Touched event | Writes event but cannot identify the character from otherPart | Correctly identifies character via otherPart.Parent and checks for Humanoid | Handles edge cases and explains why FindFirstChild is necessary |
| Game mechanics | No mechanics working | 1 mechanic partially working | All 3 mechanics (kill, speed, jump) working correctly | All 3 plus a custom mechanic with clean code |
| Debouncing | Does not understand or implement debounce | Understands concept but implementation has bugs | Implements debounce correctly with proper timing | Explains debounce clearly and adjusts cooldown for different mechanics |

##### Teacher Notes

- The Touched event fires for EVERY Part that makes contact — if a player walks on a kill brick, the event may fire for LeftFoot, RightFoot, LeftLowerLeg, RightLowerLeg, etc. This is why debouncing is essential. Show students the un-debounced Output to make the problem visceral.
- `otherPart.Parent` is the standard pattern for finding the Character from a Touched event. However, this breaks if the Part that touches is a child of something else (like a Tool). For now, the `FindFirstChild("Humanoid")` check is sufficient; in later units, students can use `Players:GetPlayerFromCharacter()` for a more robust approach.
- `AssemblyLinearVelocity` is the modern Roblox property for setting velocity on Parts. The older `Velocity` property is deprecated. Always use `AssemblyLinearVelocity`.
- Some students may set WalkSpeed to extremely high values (1000+). This can cause the character to clip through walls. Suggest a maximum of 50-60 for speed boosts.
- The HumanoidRootPart is the invisible Part that drives character physics. It is always present in the Character model and is the best Part to apply forces or set positions on.

---

#### SESSION 5 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 5: Player Character & Touched Events**

---

##### Part 1: Player/Character/Humanoid Hierarchy

**Instructions:** Fill in the diagram below and answer the questions.

```
[A] _________________ service
└── Player (e.g., "Alex")
        ↓ has a Character in...

[B] _________________ service
└── "Alex" (Character Model)
    ├── Head
    ├── Torso / UpperTorso
    ├── HumanoidRootPart
    ├── [C] _________________ ← Controls health, speed, jumping
    └── Body part meshes...
```

**A:** ______________________________
**B:** ______________________________
**C:** ______________________________

**Questions:**

1. What is the default `Health` value of a Humanoid? _______

2. What is the default `WalkSpeed` value? _______

3. What property would you change to make a player jump higher? ______________________________

4. What happens when you set `Humanoid.Health` to `0`? ______________________________

5. Where does the Character model exist — in the Players service or in Workspace? ______________________________

---

##### Part 2: Touched Event — Kill Brick

**Instructions:** Build a Kill Brick in Roblox Studio and write the script. Follow each step.

1. [ ] Insert a **Block Part** into Workspace. Name it `KillBrick`.
2. [ ] Set Color to bright red. Set Material to `Neon`. Size: `(10, 1, 10)`. Anchored: true.
3. [ ] Insert a **Script** into the KillBrick. Name it `KillScript`.
4. [ ] Write the kill brick script with debouncing:

```lua
-- Kill Brick Script with Debounce
-- Author: ____________________

local killBrick = script.Parent
local debounce = ________  -- What should the initial value be?

local function onTouched(otherPart)
    if ________ then return end  -- Skip if already processing

    local character = otherPart.________  -- How do we get the Character?
    local humanoid = character:FindFirstChild("________")  -- What are we looking for?

    if humanoid then
        debounce = ________  -- Lock the debounce
        humanoid.________ = 0  -- What property kills the player?
        print(character.Name .. " was killed!")
        task.wait(1)
        debounce = ________  -- Unlock the debounce
    end
end

killBrick.________:Connect(onTouched)  -- What event are we connecting?
```

5. [ ] Press **F5** to test. Walk onto the kill brick. Did your character die? [ ] Yes [ ] No
6. [ ] Check the **Output**. Did the print message appear? [ ] Yes [ ] No

**Fill in the blanks above, then check your answers:**
- Initial debounce value: _______________
- Skip condition: _______________
- Get character: _______________
- Looking for: _______________
- Lock value: _______________
- Kill property: _______________
- Unlock value: _______________
- Event name: _______________

---

##### Part 3: Speed Boost Pad

**Instructions:** Build a Speed Boost Pad that doubles the player's speed for 3 seconds.

1. [ ] Insert a **Block Part**. Name it `SpeedPad`. Color: bright blue. Material: Neon. Anchored: true.
2. [ ] Insert a **Script** into SpeedPad.
3. [ ] Write the complete speed boost script below:

```lua
-- Speed Boost Pad Script
-- Author: ____________________

local speedPad = script.Parent
local debounce = false

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        debounce = true

        -- Write code to:
        -- 1. Store the original WalkSpeed
        -- 2. Double the WalkSpeed
        -- 3. Print a message
        -- 4. Wait 3 seconds
        -- 5. Restore the original WalkSpeed
        -- 6. Print that the boost ended
        -- 7. Wait 1 second cooldown
        -- 8. Set debounce to false




    end
end

speedPad.Touched:Connect(onTouched)
```

4. [ ] Test it. Does the speed increase for 3 seconds? [ ] Yes [ ] No
5. [ ] Does the speed return to normal afterwards? [ ] Yes [ ] No

---

##### Part 4: Jump Pad

**Instructions:** Build a Jump Pad that launches the player into the air.

1. [ ] Insert a **Block Part**. Name it `JumpPad`. Color: bright green. Material: Neon. Anchored: true. Size: `(6, 1, 6)`.
2. [ ] Insert a **Script** into JumpPad.
3. [ ] Write the complete jump pad script:

```lua
-- Jump Pad Script
-- Author: ____________________

local jumpPad = script.Parent
local debounce = false
local LAUNCH_FORCE = 100

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        debounce = true

        -- Find the HumanoidRootPart
        local rootPart = character:FindFirstChild("HumanoidRootPart")

        if rootPart then
            -- Apply upward velocity
            rootPart.AssemblyLinearVelocity = Vector3.new(0, LAUNCH_FORCE, 0)
            print(character.Name .. " was launched!")
        end

        task.wait(0.5)
        debounce = false
    end
end

jumpPad.Touched:Connect(onTouched)
```

4. [ ] Test it. Does the player launch into the air? [ ] Yes [ ] No
5. [ ] Try changing `LAUNCH_FORCE` to different values. What value feels best?

   LAUNCH_FORCE = 50: feels _______________
   LAUNCH_FORCE = 100: feels _______________
   LAUNCH_FORCE = 200: feels _______________

   My preferred value: _______

---

##### Part 5: Debounce Understanding Check

**Instructions:** Answer these questions about debouncing.

1. In your own words, what is debouncing?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. What would happen to the Speed Boost Pad without debouncing?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. Look at the debounce pattern below. Number the steps in order (1-5):

| Step | Order |
|------|-------|
| Set `debounce = false` to unlock | ____ |
| Check `if debounce then return end` | ____ |
| Set `debounce = true` to lock | ____ |
| Execute the main game mechanic | ____ |
| `task.wait()` for cooldown | ____ |

---

##### Reflection

1. Which of the three mechanics (kill brick, speed boost, jump pad) was the most satisfying to build? Why?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Can you think of a mechanic from a Roblox game you play that uses the Touched event?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge: Custom Mechanic

Design and build your OWN Touched mechanic. Choose one or invent your own:
- [ ] **Heal Pad** — restores health to 100
- [ ] **Teleporter** — moves player to a different location
- [ ] **Slow Zone** — reduces speed by half for 5 seconds
- [ ] **Other:** ____________________

Write your script below:

```lua
-- Custom Mechanic: ____________________
-- Author: ____________________




```

Does it work? [ ] Yes [ ] No

*Save your project! You will need these mechanics for the Obby in Session 8.*

---

### Session 6: Tools, Weapons, and StarterPack

---

#### SESSION 6 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 6 of 24 |
| **Title** | Tools, Weapons, and StarterPack |
| **Unit** | Unit 2: Game Mechanics & Player Interaction |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Explain how the Roblox Tool object works, including the relationship between Tools, Handles, the Backpack, and StarterPack, and describe the Tool equip/unequip lifecycle.
2. Create a custom Tool with a Handle Part and configure its properties (Name, ToolTip, CanBeDropped, RequiresHandle).
3. Implement Tool events (`Activated`, `Equipped`, `Unequipped`) to create interactive gameplay mechanics such as a simple sword that deals damage on click.
4. Use StarterPack to distribute Tools to all players automatically when they join or respawn.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project from Session 5
- Projector or screen-share for teacher demonstrations
- Session 6 Worksheet (printed or digital)
- Whiteboard for drawing the Tool lifecycle diagram

##### Procedure

**0–5 min: Warm-Up — "Your Favourite Roblox Tool"**

- Ask: *"Think of a Roblox game where you get a cool tool or weapon. Maybe a sword in a fighting game, a pickaxe in a mining game, or a paintbrush in an art game. What made that tool fun to use?"*
- Take 4-5 responses. Write key qualities on the board: "it did something when I clicked," "I could see it in my hand," "it had a cool animation," "it showed up in my backpack."
- Say: *"Today you are going to build your own tools. By the end of this session, you will have a working sword that deals damage when you click — and every player who joins your game will get one automatically."*

**5–15 min: Introduction — How Tools Work in Roblox**

- Draw the Tool lifecycle on the whiteboard:

  ```
  StarterPack (where Tools live before the game starts)
      ↓ Player joins or respawns
  Backpack (player's inventory — press 1, 2, 3 to select)
      ↓ Player selects the Tool
  Character (Tool appears in the player's hand)
      ↓ Player clicks
  Activated event fires → your code runs
  ```

- Explain each component:
  - **Tool** — *"A Tool is a special Roblox object that players can pick up, equip, and use. When equipped, it attaches to the character's hand."*
  - **Handle** — *"Every Tool needs a Part named exactly `Handle` (capital H). This is the physical Part that the player holds. Without a Handle, the Tool will not attach to the character's hand."*
  - **StarterPack** — *"Any Tool placed in StarterPack is automatically given to every player when they join the game and every time they respawn. It is the distribution system."*
  - **Backpack** — *"The player's personal inventory. Tools from StarterPack are copied into each player's Backpack. Players press 1, 2, 3 (or click) to equip Tools from the backpack toolbar at the bottom of the screen."*

- Show Tool properties:
  - `Name` — the display name shown in the toolbar.
  - `ToolTip` — hover text that describes the tool.
  - `CanBeDropped` — if true, player can press Backspace to drop the tool.
  - `RequiresHandle` — if true, the Tool must have a Part named Handle.

- Show Tool events:
  - `Activated` — fires when the player left-clicks while the Tool is equipped.
  - `Equipped` — fires when the player selects the Tool from their backpack.
  - `Unequipped` — fires when the player switches away from the Tool.

**15–35 min: Guided Practice — Building a Simple Sword**

- Build the sword step by step. Students follow along:

  **Step 1: Create the Tool structure**
  - In the Explorer, right-click `StarterPack` > Insert Object > **Tool**.
  - Rename the Tool to `Sword`.
  - Set ToolTip to `"Click to swing!"`.
  - Set CanBeDropped to `false`.

  **Step 2: Create the Handle**
  - Right-click the `Sword` Tool > Insert Object > **Part**.
  - CRITICAL: Rename the Part to exactly `Handle` (capital H, no typos).
  - Set the Handle's Size to `(1, 1, 5)` — long and thin like a blade.
  - Set Material to `Metal`. Set Color to silver/grey.
  - Set Anchored to `false` (Tools must NOT be anchored — they attach to the character's hand).
  - Set CanCollide to `false`.

  **Step 3: Write the Sword Script**
  - Right-click the `Sword` Tool > Insert Object > **Script**. Name it `SwordScript`.

```lua
-- ============================================
-- Sword Tool Script
-- Deals damage to other players on click
-- ============================================

local tool = script.Parent
local handle = tool:FindFirstChild("Handle")
local DAMAGE = 25
local SWING_COOLDOWN = 0.5
local debounce = false

-- Runs when the player clicks while holding the sword
local function onActivated()
    if debounce then return end
    debounce = true

    print(tool.Parent.Name .. " swung the sword!")

    -- Connect a temporary Touched event on the Handle
    -- This detects what the sword blade hits during the swing
    local connection
    connection = handle.Touched:Connect(function(otherPart)
        local targetCharacter = otherPart.Parent
        local targetHumanoid = targetCharacter:FindFirstChild("Humanoid")

        -- Make sure we are not hitting ourselves
        local myCharacter = tool.Parent
        if targetHumanoid and targetCharacter ~= myCharacter then
            targetHumanoid:TakeDamage(DAMAGE)
            print("Hit " .. targetCharacter.Name .. " for " .. DAMAGE .. " damage!")
        end
    end)

    -- Keep the Touched listener active for a short swing window
    task.wait(0.3)
    connection:Disconnect()  -- Stop listening for touches

    task.wait(SWING_COOLDOWN)
    debounce = false
end

-- Runs when the player equips the sword
local function onEquipped()
    print("Sword equipped by " .. tool.Parent.Name)
end

-- Runs when the player unequips the sword
local function onUnequipped()
    print("Sword unequipped")
end

-- Connect events
tool.Activated:Connect(onActivated)
tool.Equipped:Connect(onEquipped)
tool.Unequipped:Connect(onUnequipped)
```

- Run with F5. Show:
  - The sword appears in the backpack toolbar at the bottom.
  - Press `1` to equip it — the Handle appears in the character's hand.
  - Click to swing — check the Output for the print message.
  - If there are test dummies or a second player (test with two Studio windows), demonstrate damage.

- Key teaching points:
  - *"The `tool.Parent` changes depending on whether the tool is equipped or not. When equipped, `tool.Parent` is the Character. When in the backpack, `tool.Parent` is the Backpack."*
  - *"We use `connection:Disconnect()` to stop listening for touches after the swing window. Without this, the sword would deal damage forever, even when not swinging."*
  - *"`Humanoid:TakeDamage(amount)` is the proper way to deal damage. It respects ForceField protection and other built-in Roblox systems."*
  - *"We check `targetCharacter ~= myCharacter` to prevent the player from hitting themselves."*

**35–60 min: Independent Practice — Custom Tool Creation**

- Students build their own custom tool. Options:
  - **Option A: Super Punch** — a tool that deals damage in a radius around the player when clicked (no Handle needed, set RequiresHandle to false).
  - **Option B: Flashlight** — a tool with a SpotLight inside the Handle that toggles on/off when clicked.
  - **Option C: Healing Staff** — a tool that heals the user by 20 HP when clicked, with a cooldown.

- Students complete Part 3 of the worksheet, writing their scripts and testing.

- Example Flashlight script for reference:

```lua
-- ============================================
-- Flashlight Tool Script
-- Toggles a SpotLight on and off
-- ============================================

local tool = script.Parent
local handle = tool:FindFirstChild("Handle")

-- Create a SpotLight inside the Handle
local spotlight = Instance.new("SpotLight")
spotlight.Parent = handle
spotlight.Brightness = 5
spotlight.Range = 60
spotlight.Angle = 45
spotlight.Enabled = false  -- Start with light off

local isOn = false

local function onActivated()
    isOn = not isOn  -- Toggle the state
    spotlight.Enabled = isOn

    if isOn then
        print("Flashlight ON")
        handle.Color = Color3.fromRGB(255, 255, 200)  -- warm glow
        handle.Material = Enum.Material.Neon
    else
        print("Flashlight OFF")
        handle.Color = Color3.fromRGB(50, 50, 50)  -- dark
        handle.Material = Enum.Material.SmoothPlastic
    end
end

local function onEquipped()
    print("Flashlight ready")
end

tool.Activated:Connect(onActivated)
tool.Equipped:Connect(onEquipped)
```

**60–75 min: Extension — Tool Polish and Multiple Tools**

- Challenge advanced students to:
  - Add a **swing animation** or visual effect to their sword (a trail effect using a Trail object).
  - Create a **second tool** and place both in StarterPack — demonstrate switching between tools with the number keys.
  - Add **sound effects** to tool actions using a Sound object inside the Handle.

- Example: Adding a Trail to the sword:

```lua
-- Add this to the SwordScript after getting the handle
local attachment0 = Instance.new("Attachment")
attachment0.Parent = handle
attachment0.Position = Vector3.new(0, 0, -2.5)  -- tip of blade

local attachment1 = Instance.new("Attachment")
attachment1.Parent = handle
attachment1.Position = Vector3.new(0, 0, 2.5)  -- base of blade

local trail = Instance.new("Trail")
trail.Parent = handle
trail.Attachment0 = attachment0
trail.Attachment1 = attachment1
trail.Lifetime = 0.3
trail.MinLength = 0.1
trail.Color = ColorSequence.new(Color3.fromRGB(200, 200, 255))
trail.Transparency = NumberSequence.new({
    NumberSequenceKeypoint.new(0, 0),
    NumberSequenceKeypoint.new(1, 1)
})
```

**75–85 min: Sharing & Discussion**

- Ask 3-4 students to demonstrate their tools. For each, ask: *"What events did you use? How did you handle the cooldown?"*
- Discussion questions:
  - *"What is the difference between StarterPack and Backpack?"* (StarterPack is the template — Tools are copied from StarterPack to each player's Backpack.)
  - *"Why must the Handle Part not be Anchored?"* (Because it needs to move with the character's hand.)
  - *"Why did we disconnect the Touched event after the swing window?"* (To prevent the sword from dealing damage when the player is not swinging.)

**85–90 min: Closure & Preview**

- Quick recap: *"Today we learned how to create Tools, handle Activated/Equipped/Unequipped events, and distribute tools via StarterPack."*
- Preview Session 7: *"Next session, we build a scoring system — leaderstats. You will create collectible coins that give players points and display their score on a leaderboard visible to everyone."*
- Remind: *"Save your project! Ctrl+S."*

##### Differentiation

**Support:**
- Provide the Sword Tool pre-built (Handle already created and positioned) so struggling students can focus on writing the script rather than setting up the Tool structure.
- Create a step-by-step visual guide showing where each object should be in the Explorer hierarchy (Tool > Handle, Tool > Script).
- Simplify the sword script to just print messages on Activated/Equipped/Unequipped, without the damage system, then add damage as a stretch goal.

**Extension:**
- Challenge advanced students to create a **ranged weapon** that fires a projectile (a small Part that moves forward) when Activated, using `Instance.new("Part")` and velocity.
- Ask them to implement a **durability system** — the tool breaks after 10 uses, removing itself from the Backpack.
- Have them create a **tool shop** where players walk up to a Part and receive a tool (inserting it into their Backpack via script).

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Tool structure | Cannot create a Tool | Creates a Tool but Handle is missing or wrong | Tool with correct Handle, placed in StarterPack | Tool with Handle, tooltip, and correct properties |
| Tool events | Cannot connect events | Connects one event (Activated) only | Uses Activated, Equipped, and Unequipped correctly | Uses events with parameters and explains lifecycle |
| Sword mechanic | Not working | Sword equips but Activated does not work | Sword deals damage on click with debounce | Sword with damage, self-hit prevention, swing window, effects |
| StarterPack | Does not use StarterPack | Puts Tool in wrong location | Correctly uses StarterPack for distribution | Explains StarterPack vs Backpack and tests with respawn |

##### Teacher Notes

- The Handle Part MUST be named exactly `Handle` with a capital H. This is the most common mistake — students will name it `handle`, `Handle1`, or forget to rename it entirely. If a tool is not appearing in the character's hand, check the Handle name first.
- Tools in StarterPack are automatically cloned to each player's Backpack when they join or respawn. If students modify the Tool in StarterPack during Play mode, changes will not apply until the next respawn or rejoin.
- The `tool.Parent` trick is important: when a Tool is equipped, its Parent is the Character model. When unequipped, its Parent is the Backpack. This is how you find the player using the tool.
- `Humanoid:TakeDamage()` is preferred over directly setting `Humanoid.Health` because TakeDamage respects ForceField objects (which provide temporary invincibility after respawning).
- For testing sword damage, students need a target. Options: (1) Insert a test dummy from the Toolbox (search "test dummy"), (2) Use File > Test > Start (2 Players) to test with two characters, or (3) Create a simple NPC with a Humanoid.

---

#### SESSION 6 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 6: Tools, Weapons, and StarterPack**

---

##### Part 1: Tool System Knowledge Check

**Instructions:** Answer the following questions about how Tools work in Roblox.

1. What is the special Part inside a Tool that the player holds? What must it be named?

> _______________________________________________________________________________

2. Where should you place a Tool so that every player gets it automatically when they join?

> _______________________________________________________________________________

3. Fill in the Tool lifecycle diagram:

```
[A] _________________ (where Tools are stored)
    ↓ Player joins or respawns
[B] _________________ (player's personal inventory)
    ↓ Player presses 1, 2, or 3
[C] _________________ (Tool appears in player's hand)
    ↓ Player clicks
[D] _________________ event fires
```

**A:** ______________________________
**B:** ______________________________
**C:** ______________________________
**D:** ______________________________

4. Match each Tool event to its description:

| Event | | Description |
|-------|---|-------------|
| 1. `Activated` | ____ | A. Fires when the player switches away from the Tool |
| 2. `Equipped` | ____ | B. Fires when the player left-clicks while holding the Tool |
| 3. `Unequipped` | ____ | C. Fires when the player selects the Tool from the backpack |

5. Why must the Handle Part NOT be Anchored?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 2: Build a Sword — Step by Step

**Instructions:** Follow each step to build a working Sword tool.

1. [ ] In the Explorer, right-click **StarterPack** > Insert Object > **Tool**.
2. [ ] Rename the Tool to `Sword`.
3. [ ] Set ToolTip to `"Click to swing!"` in the Properties panel.
4. [ ] Right-click the Sword Tool > Insert Object > **Part**.
5. [ ] IMPORTANT: Rename the Part to exactly `Handle` (capital H).
6. [ ] Set the Handle's Size to `(1, 1, 5)`. Material: `Metal`. Color: Silver.
7. [ ] Set Handle's **Anchored** to `false`. Set **CanCollide** to `false`.
8. [ ] Right-click the Sword Tool > Insert Object > **Script**. Name it `SwordScript`.
9. [ ] Write the sword script (copy from the lesson or write your own):

**Your Explorer should look like this:**
```
StarterPack
└── Sword (Tool)
    ├── Handle (Part)
    └── SwordScript (Script)
```

Does your Explorer match? [ ] Yes [ ] No

10. [ ] Press **F5** to test. The Sword should appear in the toolbar at the bottom of the screen.
11. [ ] Press **1** to equip the Sword. Does the Handle appear in your character's hand? [ ] Yes [ ] No
12. [ ] Click to swing. Does the Output show a message? [ ] Yes [ ] No

**Troubleshooting:**
- Tool not appearing in toolbar? → Make sure it is inside **StarterPack**.
- Handle not in character's hand? → Make sure the Part is named exactly `Handle`.
- Nothing happens on click? → Check that the Script is inside the Tool, not in ServerScriptService.

---

##### Part 3: Create Your Own Custom Tool

**Instructions:** Design and build a custom tool of your choice. Fill in the design document, then build it.

**Tool Design Document:**

| Property | Your Tool |
|----------|-----------|
| Tool Name | _________________________ |
| ToolTip | _________________________ |
| Handle Shape | Block / Sphere / Cylinder |
| Handle Size | (______, ______, ______) |
| Handle Material | _________________________ |
| Handle Color | _________________________ |
| What happens on Activated? | _________________________ |
| What happens on Equipped? | _________________________ |
| Cooldown time (seconds) | _________________________ |

**Write your complete tool script below:**

```lua
-- ============================================
-- Tool: ____________________
-- Author: ____________________
-- Description: ____________________
-- ============================================

local tool = script.Parent
local handle = tool:FindFirstChild("Handle")

-- Variables



-- Activated: what happens when the player clicks?
local function onActivated()



end

-- Equipped: what happens when the player selects this tool?
local function onEquipped()


end

-- Unequipped: what happens when the player switches away?
local function onUnequipped()


end

-- Connect events
tool.Activated:Connect(onActivated)
tool.Equipped:Connect(onEquipped)
tool.Unequipped:Connect(onUnequipped)
```

**Testing:**
- [ ] Tool appears in toolbar
- [ ] Tool equips when pressed
- [ ] Activated event works correctly
- [ ] Debounce/cooldown prevents spam clicking

---

##### Part 4: Tool Events Code Reading

**Instructions:** Read the script below and answer the questions WITHOUT running the code.

```lua
local tool = script.Parent
local handle = tool:FindFirstChild("Handle")
local uses = 0
local maxUses = 5

local function onActivated()
    if uses >= maxUses then
        print("Tool is broken!")
        tool:Destroy()
        return
    end

    uses = uses + 1
    print("Use " .. uses .. " of " .. maxUses)

    handle.Color = Color3.fromRGB(255, 255, 255)
    task.wait(0.2)
    handle.Color = Color3.fromRGB(100, 100, 100)
end

local function onEquipped()
    print("Uses remaining: " .. (maxUses - uses))
end

tool.Activated:Connect(onActivated)
tool.Equipped:Connect(onEquipped)
```

**Question 1:** What happens when the player clicks the tool for the 3rd time?

> _______________________________________________

**Question 2:** What happens when the player clicks the tool for the 6th time?

> _______________________________________________

**Question 3:** What does `tool:Destroy()` do?

> _______________________________________________

**Question 4:** If the player unequips and re-equips the tool after 2 uses, what will the Equipped message say?

> _______________________________________________

**Question 5:** Why does the Handle flash white and then go grey? What visual effect does this create?

> _______________________________________________

---

##### Reflection

1. What was the hardest part of building a Tool today? How did you solve it?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Why does Roblox require a Part named exactly "Handle" inside a Tool? What do you think would happen if you named it something else?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge

Create a **Flashlight Tool** that toggles a SpotLight on and off when clicked:

1. Create a Tool called `Flashlight` in StarterPack.
2. Add a Handle (Cylinder shape, dark colour).
3. Add a SpotLight inside the Handle (Insert Object > SpotLight).
4. Write a script that toggles `spotlight.Enabled` between `true` and `false` each time the player clicks.
5. Change the Handle colour to yellow (Neon) when the light is on, and dark grey when off.

Did you complete the flashlight? [ ] Yes [ ] No

Does the light toggle on and off? [ ] Yes [ ] No

*Save your project! Ctrl+S.*

---

### Session 7: Collectibles, Scoring, and Leaderboards

---

#### SESSION 7 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 7 of 24 |
| **Title** | Collectibles, Scoring, and Leaderboards |
| **Unit** | Unit 2: Game Mechanics & Player Interaction |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Implement the `leaderstats` system in Roblox using a Script that creates a Folder named `leaderstats` inside each Player object, containing IntValue children for tracking scores.
2. Create collectible objects (coins/gems) that detect player contact with a Touched event, add points to the player's leaderboard score, and then disappear.
3. Access and modify a player's leaderstats values from any server Script, demonstrating the path `player.leaderstats.StatName.Value`.
4. Explain why leaderstats must be set up from a server Script in ServerScriptService and why the folder must be named exactly `leaderstats`.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project from Session 6
- Projector or screen-share for teacher demonstrations
- Session 7 Worksheet (printed or digital)
- Several coin/gem Parts pre-placed (or built live) in the Workspace
- Whiteboard for diagramming the leaderstats structure

##### Procedure

**0–5 min: Warm-Up — "High Scores and Leaderboards"**

- Ask: *"In your favourite Roblox games, how do you know what your score is? How do you compare your score with other players?"*
- Take responses: "there is a leaderboard on the side," "I can see my coins in the corner," "the tab menu shows everyone's stats."
- Say: *"That leaderboard you see when you press Tab — that is the `leaderstats` system. Roblox has a built-in feature where, if you set it up correctly, it automatically displays player stats on the leaderboard. Today we build that system from scratch."*

**5–15 min: Introduction — The leaderstats System**

- Draw the structure on the whiteboard:

  ```
  Players
  └── Alex (Player)
      ├── Backpack
      ├── PlayerGui
      └── leaderstats (Folder) ← MUST be named exactly "leaderstats"
          ├── Coins (IntValue) → .Value = 0
          └── Stage (IntValue) → .Value = 1
  ```

- Key rules:
  - *"The folder MUST be named exactly `leaderstats` — lowercase L, no spaces, no capitals. If you misspell it, Roblox will NOT display the leaderboard."*
  - *"Inside the folder, you create Value objects: `IntValue` for whole numbers (score, coins, level), `StringValue` for text (team name, rank)."*
  - *"This setup MUST happen in a server Script in ServerScriptService, using the `PlayerAdded` event."*
  - *"Once set up, Roblox automatically shows the stats on the Tab leaderboard for ALL players."*

- Explain `PlayerAdded`: *"This event fires every time a new player joins the game. We use it to set up their leaderstats as soon as they arrive."*

**15–35 min: Guided Practice — Setting Up leaderstats**

- Create a new Script in ServerScriptService. Name it `LeaderboardSetup`. Type live:

```lua
-- ============================================
-- Leaderboard Setup Script
-- Creates leaderstats for every player who joins
-- Place this in ServerScriptService
-- ============================================

local Players = game:GetService("Players")

local function onPlayerAdded(player)
    -- Create the leaderstats folder
    local leaderstats = Instance.new("Folder")
    leaderstats.Name = "leaderstats"  -- MUST be exactly "leaderstats"
    leaderstats.Parent = player

    -- Create a Coins stat
    local coins = Instance.new("IntValue")
    coins.Name = "Coins"
    coins.Value = 0
    coins.Parent = leaderstats

    -- Create a Stage stat
    local stage = Instance.new("IntValue")
    stage.Name = "Stage"
    stage.Value = 1
    stage.Parent = leaderstats

    print(player.Name .. " joined! Leaderstats created.")
    print("Starting coins: " .. coins.Value)
    print("Starting stage: " .. stage.Value)
end

-- Connect the function to the PlayerAdded event
Players.PlayerAdded:Connect(onPlayerAdded)
```

- Run with F5. Show:
  - Press **Tab** — the leaderboard appears showing the player name, Coins (0), and Stage (1).
  - In the Explorer, expand Players > YourName > leaderstats — show the Folder with IntValue children.
  - In the Command Bar, type: `game.Players.YourName.leaderstats.Coins.Value = 100` — watch the leaderboard update instantly.

- Key teaching points:
  - *"`Instance.new('Folder')` creates a new Folder object in code. `Instance.new('IntValue')` creates a new integer value object."*
  - *"We set the Name BEFORE setting the Parent. This is a best practice — if you set Parent first, the object appears in the Explorer briefly with a default name, which can cause confusion."*
  - *"`game:GetService('Players')` is the professional way to access the Players service. It always works, even if someone renamed the Players service."*

**35–60 min: Guided + Independent Practice — Collectible Coins**

- **Guided: Build and script the first coin (15 minutes)**

- Create a collectible coin: Cylinder Part, Size `(1, 0.2, 1)` (flat disc), Material = Neon, Color = bright yellow. Name it `Coin`. Anchored = true. Rotate it 90 degrees so it stands upright.

- Insert a Script into the Coin. Name it `CoinScript`:

```lua
-- ============================================
-- Coin Collectible Script
-- Awards points and disappears when touched
-- ============================================

local coin = script.Parent
local COIN_VALUE = 10
local debounce = false

local function onTouched(otherPart)
    if debounce then return end

    -- Find the character and humanoid
    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        debounce = true

        -- Find the Player from the Character
        local Players = game:GetService("Players")
        local player = Players:GetPlayerFromCharacter(character)

        if player then
            -- Find the player's leaderstats
            local leaderstats = player:FindFirstChild("leaderstats")

            if leaderstats then
                local coins = leaderstats:FindFirstChild("Coins")

                if coins then
                    -- Add points
                    coins.Value = coins.Value + COIN_VALUE
                    print(player.Name .. " collected a coin! Total: " .. coins.Value)
                end
            end
        end

        -- Destroy the coin (make it disappear)
        coin:Destroy()
    end
end

coin.Touched:Connect(onTouched)
```

- Run with F5. Walk into the coin. Show:
  - The coin disappears.
  - The Output shows the collection message.
  - Press Tab — the leaderboard shows 10 Coins.

- Key teaching points:
  - *"`Players:GetPlayerFromCharacter(character)` is the safest way to get the Player object from a Character model. It returns the Player if found, or nil if the character does not belong to a player."*
  - *"We chain `FindFirstChild` calls to safely navigate the hierarchy. If any step returns nil, we do not crash — we just skip the rest."*
  - *"`coin:Destroy()` permanently removes the coin from the game. It will not come back unless we re-create it with code."*

- **Independent: Students create a coin course (10 minutes)**
  - Students place at least 5 coins around their scene from Session 2.
  - Each coin needs the CoinScript inside it.
  - Challenge: vary the `COIN_VALUE` — some coins are worth 10, some worth 25, some worth 50.
  - TIP: Duplicate a scripted coin (Ctrl+D) to save time — the script is copied too.

**60–75 min: Extension — Gem Collectibles and Respawning Coins**

- Challenge 1: Create **Gem** collectibles worth 50 points each, with a different colour (purple/blue) and shape (Sphere).

- Challenge 2: Make coins **respawn** after being collected instead of being destroyed permanently:

```lua
-- ============================================
-- Respawning Coin Script
-- Coin reappears after a delay
-- ============================================

local coin = script.Parent
local COIN_VALUE = 10
local RESPAWN_TIME = 10  -- seconds until coin reappears
local debounce = false

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        debounce = true

        local Players = game:GetService("Players")
        local player = Players:GetPlayerFromCharacter(character)

        if player then
            local leaderstats = player:FindFirstChild("leaderstats")
            if leaderstats then
                local coins = leaderstats:FindFirstChild("Coins")
                if coins then
                    coins.Value = coins.Value + COIN_VALUE
                    print(player.Name .. " collected a coin! Total: " .. coins.Value)
                end
            end
        end

        -- Hide the coin instead of destroying it
        coin.Transparency = 1
        coin.CanCollide = false

        -- Wait for respawn timer
        task.wait(RESPAWN_TIME)

        -- Show the coin again
        coin.Transparency = 0
        coin.CanCollide = true
        debounce = false
    end
end

coin.Touched:Connect(onTouched)
```

- Challenge 3: Add a **sound effect** when collecting a coin:

```lua
-- Add this at the top of the coin script, after getting the coin variable:
local collectSound = Instance.new("Sound")
collectSound.SoundId = "rbxassetid://6042053626"  -- coin collect sound
collectSound.Volume = 0.5
collectSound.Parent = coin

-- Add this inside the if humanoid block, before hiding/destroying:
collectSound:Play()
task.wait(0.2)  -- Let the sound play briefly before hiding
```

**75–85 min: Sharing & Discussion**

- Ask students to press Tab and compare their leaderboard scores. Who collected the most coins?
- Ask 2-3 students to show their coin layouts and any custom mechanics they added (respawning, sounds, gems).
- Discussion questions:
  - *"Why does the leaderstats folder have to be named exactly `leaderstats`?"* (Roblox's leaderboard system specifically looks for a Folder with that exact name.)
  - *"Why do we use `Players:GetPlayerFromCharacter()` instead of just using `otherPart.Parent`?"* (Because `otherPart.Parent` gives us the Character, but we need the Player to access leaderstats. They are different objects in different locations.)
  - *"If we wanted to track multiple stats like Coins, Gems, and Level, how would we do it?"* (Add more IntValue objects inside the leaderstats folder.)

**85–90 min: Closure & Preview**

- Quick recap: *"Today we built the leaderstats system, created collectible coins, and learned how to track scores on the leaderboard. These are the building blocks of any Roblox game with progression."*
- Preview Session 8: *"Next session, we put EVERYTHING together — kill bricks, speed boosts, jump pads, collectibles, and leaderboards — into a complete Obstacle Course. You will build a full obby from start to finish."*
- Remind: *"Save your project! This is important — you will use everything from today in Session 8."*

##### Differentiation

**Support:**
- Provide the `LeaderboardSetup` script pre-written and tested, so struggling students can focus on the coin collection mechanic.
- Create a template coin with the script already inside — students only need to duplicate (Ctrl+D) and position the coins.
- Simplify the coin script by removing the nested `FindFirstChild` checks and using direct path access: `player.leaderstats.Coins.Value` — less safe but easier to read.

**Extension:**
- Challenge advanced students to create a **coin magnet tool** — a Tool that, when equipped, automatically collects any coin within 20 studs of the player (using `(coin.Position - rootPart.Position).Magnitude` to check distance).
- Ask them to add a **"Double Coins" power-up** — a special glowing Part that, when touched, doubles all coin collection values for 15 seconds.
- Have them create a **shop system** — a Part with a ClickDetector that lets players spend coins to buy a tool or item.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| leaderstats setup | Cannot create leaderstats | Creates folder but wrong name or missing values | Correct leaderstats with IntValues and PlayerAdded | Explains why naming matters and adds multiple stats |
| Coin collection | No collectible mechanic | Coin touched but no score update | Coin updates score and disappears with debounce | Adds respawning, sound, and varied coin values |
| Player ↔ Character | Cannot navigate the hierarchy | Accesses Character but not Player | Uses GetPlayerFromCharacter correctly | Explains full hierarchy and uses FindFirstChild safely |
| Leaderboard display | Leaderboard not visible | Leaderboard shows but values incorrect | Leaderboard shows correct values that update on collection | Multiple stats, all updating correctly in real time |

##### Teacher Notes

- The most common mistake: misspelling `leaderstats`. Students will write `leaderStats`, `LeaderStats`, `leader_stats`, or `Leaderstats`. Only lowercase `leaderstats` works. Check this FIRST when a student's leaderboard does not appear.
- `Instance.new()` creates objects in code. The pattern is: create it, set its Name, configure its properties, THEN set its Parent. Setting Parent last ensures the object does not briefly appear in an incomplete state.
- `Players:GetPlayerFromCharacter(character)` is essential for connecting a Character model back to its Player object. This function returns `nil` if the Character does not belong to any player, which prevents errors with NPCs or test dummies.
- When students duplicate coins (Ctrl+D), the script inside is also duplicated. This is efficient but means each coin has its own script instance. For games with hundreds of coins, a more efficient approach uses a single script — but that is an advanced topic for later.
- `coin:Destroy()` is permanent within a single game session. When the server restarts, the coin exists again (because it is in the saved place file). For respawning coins, use the hide/show approach instead of Destroy.

---

#### SESSION 7 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 7: Collectibles, Scoring, and Leaderboards**

---

##### Part 1: leaderstats Knowledge Check

**Instructions:** Answer the following questions about the leaderstats system.

1. What must the leaderstats Folder be named EXACTLY? ______________________________

2. Where should the leaderstats setup Script be placed? ______________________________

3. What event do we use to run code when a new player joins? ______________________________

4. What type of Value object do we use for whole numbers like score? ______________________________

5. Draw the leaderstats hierarchy for a game that tracks Coins, Gems, and Level:

```
Players
└── Alex (Player)
    └── ______________ (Folder)
        ├── ______________ (____________) → Value = ____
        ├── ______________ (____________) → Value = ____
        └── ______________ (____________) → Value = ____
```

6. How do you access a player's Coins value in code? Write the full path:

> `player.________________.________________.________________`

---

##### Part 2: Build the Leaderboard System

**Instructions:** Set up the leaderstats system in your project.

1. [ ] Insert a new **Script** into **ServerScriptService**. Name it `LeaderboardSetup`.
2. [ ] Write the leaderstats setup script:

```lua
local Players = game:GetService("Players")

local function onPlayerAdded(player)
    -- Create the leaderstats folder
    local leaderstats = Instance.new("Folder")
    leaderstats.Name = "leaderstats"
    leaderstats.Parent = player

    -- Create Coins stat
    local coins = Instance.new("IntValue")
    coins.Name = "Coins"
    coins.Value = 0
    coins.Parent = leaderstats

    -- Create Stage stat (for the Obby in Session 8)
    local stage = Instance.new("IntValue")
    stage.Name = "Stage"
    stage.Value = 1
    stage.Parent = leaderstats

    print(player.Name .. " joined! Leaderstats ready.")
end

Players.PlayerAdded:Connect(onPlayerAdded)
```

3. [ ] Press **F5** to test. Press **Tab**. Does the leaderboard appear? [ ] Yes [ ] No
4. [ ] Does it show "Coins: 0" and "Stage: 1"? [ ] Yes [ ] No

**If the leaderboard does NOT appear, check:**
- [ ] Is the folder named exactly `leaderstats` (lowercase)?
- [ ] Is the Script in `ServerScriptService`?
- [ ] Are the IntValues parented to the leaderstats folder?

---

##### Part 3: Create Collectible Coins

**Instructions:** Build coins that give players points when collected.

1. [ ] Insert a **Cylinder Part** into Workspace. Name it `Coin`.
2. [ ] Set Size to `(1, 0.2, 1)`. Rotate it so it stands upright.
3. [ ] Set Color to bright yellow. Material: `Neon`. Anchored: true.
4. [ ] Insert a **Script** into the Coin. Write the coin collection script:

```lua
local coin = script.Parent
local COIN_VALUE = 10
local debounce = false

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        debounce = true

        -- Get the Player from the Character
        local Players = game:GetService("Players")
        local player = Players:GetPlayerFromCharacter(character)

        if player then
            local leaderstats = player:FindFirstChild("leaderstats")
            if leaderstats then
                local coins = leaderstats:FindFirstChild("Coins")
                if coins then
                    coins.Value = coins.Value + COIN_VALUE
                    print(player.Name .. " collected a coin! Total: " .. coins.Value)
                end
            end
        end

        coin:Destroy()
    end
end

coin.Touched:Connect(onTouched)
```

5. [ ] Test: Walk into the coin. Does it disappear? [ ] Yes [ ] No
6. [ ] Press Tab. Did your Coins stat increase? [ ] Yes [ ] No
7. [ ] Duplicate the coin (Ctrl+D) and place at least 4 more around your scene.
8. [ ] Test again: collect all coins. What is your final score? _______

---

##### Part 4: Coin Variety Challenge

**Instructions:** Create THREE different types of collectibles with different values and appearances.

| Collectible | Shape | Color | Material | Value |
|------------|-------|-------|----------|-------|
| Bronze Coin | Cylinder | _________ | _________ | 10 |
| Silver Coin | Cylinder | _________ | _________ | 25 |
| Gold Gem | Sphere | _________ | _________ | 50 |

For the Gold Gem, change the `COIN_VALUE` in the script to 50. How many of each did you place in your scene?

- Bronze Coins: _______
- Silver Coins: _______
- Gold Gems: _______
- Maximum possible score: _______

---

##### Part 5: Respawning Coins

**Instructions:** Modify one of your coins so it respawns after being collected instead of being destroyed permanently.

Instead of `coin:Destroy()`, use this approach:

```lua
-- Replace coin:Destroy() with:
coin.Transparency = 1      -- Make invisible
coin.CanCollide = false     -- Walk through

task.wait(10)               -- Wait 10 seconds

coin.Transparency = 0       -- Make visible again
coin.CanCollide = true      -- Solid again
debounce = false            -- Allow collection again
```

Test it:
- [ ] Does the coin disappear when you collect it? [ ] Yes [ ] No
- [ ] Does the coin reappear after 10 seconds? [ ] Yes [ ] No
- [ ] Can you collect it again after it respawns? [ ] Yes [ ] No

---

##### Part 6: Code Reading — Find the Bugs

**Instructions:** The following leaderstats script has THREE bugs. Find and fix them.

```lua
local Players = game:GetService("Players")

local function onPlayerAdded(player)
    local leaderstats = Instance.new("Folder")
    leaderstats.Name = "Leaderstats"  -- BUG 1: ___________________________
    leaderstats.Parent = player

    local coins = Instance.new("StringValue")  -- BUG 2: ___________________________
    coins.Name = "Coins"
    coins.Value = 0
    coins.Parent = player  -- BUG 3: ___________________________

    print(player.Name .. " is ready!")
end

Players.PlayerAdded:Connect(onPlayerAdded)
```

**Bug 1 — What is wrong?** _______________________________________________
**Fix:** _______________________________________________

**Bug 2 — What is wrong?** _______________________________________________
**Fix:** _______________________________________________

**Bug 3 — What is wrong?** _______________________________________________
**Fix:** _______________________________________________

---

##### Reflection

1. Why is the leaderstats system useful for game developers? How does it help players?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Explain the difference between `coin:Destroy()` and hiding the coin with `Transparency = 1`. When would you use each approach?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. What other stats (besides Coins) might you want to track in a game? List three ideas.

> 1. _______________________________________________
> 2. _______________________________________________
> 3. _______________________________________________

---

##### Bonus Challenge

Add a **sound effect** to your coins. When collected, the coin should play a short sound before disappearing.

```lua
-- Add this BEFORE the coin:Destroy() or hide logic:
local collectSound = Instance.new("Sound")
collectSound.SoundId = "rbxassetid://6042053626"
collectSound.Volume = 0.5
collectSound.Parent = coin
collectSound:Play()
task.wait(0.3)
```

Did the sound play when you collected a coin? [ ] Yes [ ] No

*Save your project! You will need everything for the Obby project in Session 8.*

---

### Session 8: Project 1 — Obstacle Course (Obby) with Scoring

---

#### SESSION 8 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 8 of 24 |
| **Title** | Project 1 — Obstacle Course (Obby) with Scoring |
| **Unit** | Unit 2: Game Mechanics & Player Interaction |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Design and build a complete multi-stage Obstacle Course (Obby) in Roblox Studio with at least 5 stages, each featuring different platform arrangements and increasing difficulty.
2. Integrate at least three different game mechanics from Sessions 5–7 (kill bricks, speed boosts, jump pads, checkpoints, collectibles) into a cohesive gameplay experience.
3. Implement a checkpoint system that updates the player's Stage stat on the leaderboard and respawns the player at the last reached checkpoint after dying.
4. Playtest their own Obby, identify and fix at least two gameplay issues (difficulty spikes, unfair hazards, missing collisions), and explain their design decisions.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project with leaderstats and mechanics from Sessions 5–7
- Projector or screen-share for teacher demonstrations
- Session 8 Worksheet (printed or digital)
- Whiteboard for sketching Obby layouts
- Timer for structured work phases
- Reference images of popular Roblox obbies (optional, for inspiration)

##### Procedure

**0–5 min: Warm-Up — "What Makes a Great Obby?"**

- Ask: *"You have all played obbies on Roblox. What makes a GOOD obby versus a BAD obby?"*
- Take responses and write them in two columns on the board:

  **Good Obby:** "gets harder gradually," "has checkpoints," "has variety," "rewards you for collecting things," "feels fair."

  **Bad Obby:** "too hard too fast," "no checkpoints (you restart from the beginning)," "same jumps over and over," "laggy," "unfair obstacles."

- Say: *"Today you are building your OWN obby — and you are going to make a GOOD one. You have all the tools: kill bricks, speed boosts, jump pads, collectibles, and leaderboards. Now it is time to put them all together."*

**5–15 min: Introduction — Obby Architecture & Checkpoint System**

- On the whiteboard, sketch a simple 5-stage Obby layout:

  ```
  [Spawn] → [Stage 1: Easy Jumps] → [Checkpoint 1]
           → [Stage 2: Kill Brick Path] → [Checkpoint 2]
           → [Stage 3: Speed Section] → [Checkpoint 3]
           → [Stage 4: Jump Pad Gauntlet] → [Checkpoint 4]
           → [Stage 5: Final Challenge] → [Finish!]
  ```

- Explain the checkpoint system:
  - *"When a player reaches a checkpoint, their Stage stat on the leaderboard updates."*
  - *"When a player dies, they respawn at their most recent checkpoint — NOT at the beginning."*
  - *"The checkpoint uses a SpawnLocation Part, which is a special Part type that players can respawn at."*

- Demonstrate the checkpoint script:

```lua
-- ============================================
-- Checkpoint Script
-- Updates player's stage and sets spawn point
-- Place inside each checkpoint SpawnLocation
-- ============================================

local checkpoint = script.Parent  -- This is a SpawnLocation
local STAGE_NUMBER = 1  -- Change this for each checkpoint (1, 2, 3, etc.)

-- Make this SpawnLocation non-default (players do not spawn here unless assigned)
checkpoint.AllowTeamChangeOnTouch = false

local debounce = false

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        local Players = game:GetService("Players")
        local player = Players:GetPlayerFromCharacter(character)

        if player then
            local leaderstats = player:FindFirstChild("leaderstats")
            if leaderstats then
                local stage = leaderstats:FindFirstChild("Stage")

                -- Only update if this is a NEW checkpoint (not one already passed)
                if stage and stage.Value < STAGE_NUMBER then
                    debounce = true
                    stage.Value = STAGE_NUMBER

                    -- Set this SpawnLocation as the player's respawn point
                    player.RespawnLocation = checkpoint

                    print(player.Name .. " reached Stage " .. STAGE_NUMBER .. "!")

                    -- Visual feedback: checkpoint glows
                    checkpoint.Color = Color3.fromRGB(0, 255, 0)
                    checkpoint.Material = Enum.Material.Neon
                    task.wait(1)
                    checkpoint.Color = Color3.fromRGB(100, 100, 100)
                    checkpoint.Material = Enum.Material.SmoothPlastic

                    debounce = false
                end
            end
        end
    end
end

checkpoint.Touched:Connect(onTouched)
```

- Key teaching points:
  - *"`SpawnLocation` is a special Part type that acts as a respawn point. Insert it from the Model tab or right-click > Insert Object > SpawnLocation."*
  - *"`player.RespawnLocation = checkpoint` tells Roblox to spawn the player HERE after they die, instead of the default spawn point."*
  - *"We check `stage.Value < STAGE_NUMBER` to prevent the checkpoint from triggering if the player has already passed it. This way, going backwards does not reset your progress."*

**15–35 min: Guided Practice — Building the First Two Stages Together**

- Build the first two stages of an Obby together as a class:

  **Spawn Area:**
  - Delete the default SpawnLocation from the Baseplate (if it exists).
  - Insert a SpawnLocation. Name it `Spawn`. Position it at the start of the Obby. Size: `(8, 1, 8)`. Anchored = true.
  - Set `Spawn.Neutral = true` so all players can spawn here.

  **Stage 1: Easy Jumps**
  - Create 4-5 Block Parts as platforms with gaps between them. Space them so the jumps are easy.
  - Name them `Platform1_1`, `Platform1_2`, etc. Anchored = true.
  - Add ONE collectible coin on the 3rd platform (copy from Session 7).

  **Checkpoint 1:**
  - Insert a SpawnLocation after the last platform of Stage 1. Name it `Checkpoint1`.
  - Insert the checkpoint script (from above). Set `STAGE_NUMBER = 2`.
  - Set the SpawnLocation's `Neutral = false` and `AllowTeamChangeOnTouch = false`.

  **Stage 2: Kill Brick Path**
  - Create a path of Block Parts. Insert 2–3 red kill bricks (from Session 5) between safe platforms.
  - Players must jump over the kill bricks to proceed.
  - Add 2 coins along this path.

  **Checkpoint 2:**
  - Insert another SpawnLocation. Name it `Checkpoint2`. Insert checkpoint script with `STAGE_NUMBER = 3`.

- Run with F5 and playtest together. Show that:
  - Collecting coins updates the leaderboard.
  - Reaching Checkpoint 1 updates Stage to 2.
  - Dying on a kill brick respawns the player at their last checkpoint.

**35–60 min: Independent Practice — Students Build Stages 3-5**

- Students build the remaining stages of their Obby independently. Requirements:

  **Stage 3** must include:
  - At least one **speed boost pad** (from Session 5).
  - At least 3 platforms.
  - At least 2 coins.
  - A checkpoint at the end.

  **Stage 4** must include:
  - At least one **jump pad** (from Session 5).
  - A challenging section that requires the jump pad to cross.
  - At least 2 coins.
  - A checkpoint at the end.

  **Stage 5** (Final Challenge) must include:
  - A combination of at least 2 different mechanics (kill bricks + jump pads, speed boosts + narrow paths, etc.).
  - At least 3 coins.
  - A **finish line** Part that prints a congratulations message.

- Minimum Obby requirements (displayed on the board):
  - [ ] At least 5 stages with increasing difficulty
  - [ ] At least 5 checkpoints (including spawn)
  - [ ] At least 3 different mechanics used (kill bricks, speed, jump, coins)
  - [ ] At least 10 collectible coins total
  - [ ] Leaderboard showing Coins and Stage
  - [ ] All platforms Anchored
  - [ ] All Parts named descriptively

- Example finish line script:

```lua
-- ============================================
-- Finish Line Script
-- Congratulates the player for completing the Obby
-- ============================================

local finishLine = script.Parent
local debounce = false

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        local Players = game:GetService("Players")
        local player = Players:GetPlayerFromCharacter(character)

        if player then
            debounce = true

            local leaderstats = player:FindFirstChild("leaderstats")
            if leaderstats then
                local stage = leaderstats:FindFirstChild("Stage")
                if stage then
                    stage.Value = 6  -- Final stage
                end

                -- Bonus coins for finishing
                local coins = leaderstats:FindFirstChild("Coins")
                if coins then
                    coins.Value = coins.Value + 100
                    print(player.Name .. " completed the Obby! +100 bonus coins!")
                end
            end

            -- Visual celebration
            finishLine.Color = Color3.fromRGB(255, 215, 0)  -- Gold
            finishLine.Material = Enum.Material.Neon

            task.wait(3)
            debounce = false
        end
    end
end

finishLine.Touched:Connect(onTouched)
```

- Circulate the room. Common issues:
  - Checkpoints not working: script not inside the SpawnLocation, or STAGE_NUMBER not updated.
  - Player not respawning at checkpoint: `player.RespawnLocation` not being set.
  - Kill bricks too close together: difficulty spike. Suggest spacing them out.
  - Platforms too far apart: impossible jumps. Remind students that the default jump covers about 8-10 studs horizontally.

**60–75 min: Extension — Polish and Advanced Features**

- Students who finish early can add advanced features:

  - **Moving platforms** using TweenService:

```lua
-- ============================================
-- Moving Platform Script
-- Platform moves back and forth
-- ============================================

local TweenService = game:GetService("TweenService")
local platform = script.Parent

local startPosition = platform.Position
local endPosition = startPosition + Vector3.new(20, 0, 0)  -- Move 20 studs right

local tweenInfo = TweenInfo.new(
    3,                           -- Duration: 3 seconds
    Enum.EasingStyle.Linear,     -- Constant speed
    Enum.EasingDirection.InOut,  -- Smooth start and stop
    -1,                          -- Repeat forever
    true,                        -- Reverse (go back to start)
    0                            -- No delay between repeats
)

local tween = TweenService:Create(platform, tweenInfo, {Position = endPosition})
tween:Play()
```

  - **Disappearing platforms** that vanish briefly:

```lua
-- ============================================
-- Disappearing Platform Script
-- Platform disappears for 2 seconds, then returns
-- ============================================

local platform = script.Parent
local VISIBLE_TIME = 3
local HIDDEN_TIME = 2

while true do
    -- Platform is visible and solid
    platform.Transparency = 0
    platform.CanCollide = true
    task.wait(VISIBLE_TIME)

    -- Warning: platform flashes before disappearing
    for i = 1, 3 do
        platform.Transparency = 0.5
        task.wait(0.2)
        platform.Transparency = 0
        task.wait(0.2)
    end

    -- Platform disappears
    platform.Transparency = 1
    platform.CanCollide = false
    task.wait(HIDDEN_TIME)
end
```

  - **Timer system** that tracks completion time.

**75–85 min: Sharing & Discussion — Playtest Party**

- Pair students up. Each student playtests their partner's Obby.
- Playtesters answer three questions on the worksheet:
  1. What was the most fun part of the Obby?
  2. Was there any part that felt unfair or too difficult?
  3. What is one suggestion to make it even better?
- After testing, students share feedback with their partner.
- Ask 2-3 students to share their Obby with the whole class. Run the game and let the class watch.
- Discuss: *"What did you learn from watching someone else play your game that you did not notice yourself?"*

**85–90 min: Closure & Preview**

- Celebrate: *"You have just built your first complete Roblox game — an Obby with checkpoints, hazards, collectibles, and a leaderboard. This is a REAL game that players could play."*
- Quick reflection: *"Raise your hand if you found a bug during playtesting that you did not notice while building."* (Most hands should go up.) *"This is why playtesting is essential. The developer NEVER sees their own game the way a player does."*
- Preview Unit 3: *"In Unit 3, we go deeper into scripting — data stores to save player progress, remote events for client-server communication, and more. Your games are about to get much more sophisticated."*
- Final reminder: *"Save your project! This Obby is your first portfolio piece."*

##### Differentiation

**Support:**
- Provide a pre-built 3-stage Obby framework with checkpoints already scripted. Struggling students add their own platforms, hazards, and collectibles to the existing framework.
- Allow students to work in pairs for the entire session — one builds while the other scripts.
- Reduce the minimum requirement to 3 stages instead of 5, with at least 2 mechanics and 5 coins.

**Extension:**
- Challenge advanced students to add a **timer system** that tracks how long it takes to complete the Obby, displaying the time on a SurfaceGui at the finish line.
- Ask them to implement **difficulty settings** — a starting area where players choose Easy (wider platforms), Medium, or Hard (narrow platforms) using ClickDetectors.
- Have them add a **"Reset Progress" button** — a Part with a ClickDetector that resets the player's Stage to 1 and teleports them back to the start.
- Challenge them to publish their Obby to Roblox (File > Publish to Roblox) and share the link with classmates to play outside of Studio.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Obby design | Fewer than 3 stages; no variety | 3–4 stages; limited variety | 5+ stages with increasing difficulty and variety | Creative layout with multiple paths, themes, or unique challenges |
| Mechanics integration | Fewer than 2 mechanics | 2 mechanics working but not integrated well | 3+ mechanics integrated smoothly (kill, speed, jump, coins) | Advanced mechanics (moving platforms, timers) added creatively |
| Checkpoint system | No checkpoints | 1–2 checkpoints but respawn not working | All checkpoints working with Stage tracking and respawn | Checkpoints with visual feedback, stage-gate logic |
| Playtesting & iteration | No testing done | Tested but did not fix issues | Tested and fixed 2+ issues based on feedback | Tested with peer, incorporated feedback, explains design reasoning |

##### Teacher Notes

- This is the most open-ended session so far. Set clear time boundaries: 5 minutes for planning (on paper), 25 minutes for building, 10 minutes for polish. Without structure, students will spend the entire time building and never test.
- The SpawnLocation's `Neutral` property determines whether all players can spawn there or only specific teams. For the starting spawn, set `Neutral = true`. For checkpoints, it does not matter as long as `player.RespawnLocation` is set.
- Jump distance in Roblox: a standard character can jump approximately 7-8 studs horizontally with a running start. Remind students to test their gaps — if THEY cannot make the jump, players will not be able to either.
- If a student's checkpoint system is not working, check these in order: (1) Is the checkpoint a SpawnLocation (not a regular Part)? (2) Is the script inside the SpawnLocation? (3) Is `STAGE_NUMBER` correct? (4) Is `player.RespawnLocation` being set?
- Playtesting is a real skill. Encourage students to watch their partner play without giving hints — the temptation to say "jump here!" is strong, but the value of watching someone struggle (or succeed) independently is enormous for game design.
- If time allows and computers have internet access, students can publish their Obby to Roblox (File > Publish to Roblox) and share links. This is extremely motivating.

---

#### SESSION 8 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 8: Project 1 — Obstacle Course (Obby) with Scoring**

---

##### Part 1: Obby Design Plan

**Instructions:** Before building, plan your Obby on paper. Sketch a simple layout and describe each stage.

**My Obby Name:** ______________________________________

| Stage | Theme / Description | Mechanics Used | Number of Coins | Difficulty (1-5) |
|-------|-------------------|----------------|-----------------|-------------------|
| Spawn | Starting area | None | 0 | 1 |
| Stage 1 | _______________________ | _______________________ | _______ | _______ |
| Stage 2 | _______________________ | _______________________ | _______ | _______ |
| Stage 3 | _______________________ | _______________________ | _______ | _______ |
| Stage 4 | _______________________ | _______________________ | _______ | _______ |
| Stage 5 | _______________________ | _______________________ | _______ | _______ |
| Finish | Celebration / End | Bonus coins | _______ | - |

**Total coins in my Obby:** _______

**Sketch your Obby layout here (bird's-eye view):**

```
[Draw your layout — show platforms, hazards, checkpoints, and coins]










```

---

##### Part 2: Requirements Checklist

**Instructions:** As you build, check off each requirement. ALL items must be completed.

| # | Requirement | Done? |
|---|------------|-------|
| 1 | At least **5 stages** with increasing difficulty | [ ] |
| 2 | At least **5 checkpoints** (SpawnLocations with checkpoint scripts) | [ ] |
| 3 | Checkpoints **update Stage** on leaderboard | [ ] |
| 4 | Player **respawns at last checkpoint** after dying | [ ] |
| 5 | At least **3 different mechanics** used (kill bricks, speed pads, jump pads, etc.) | [ ] |
| 6 | At least **10 collectible coins** placed throughout | [ ] |
| 7 | Coins **update score** on leaderboard when collected | [ ] |
| 8 | **Leaderboard** visible with Coins and Stage stats | [ ] |
| 9 | **All platforms Anchored** | [ ] |
| 10 | **All Parts named descriptively** (no "Part", "Part2") | [ ] |
| 11 | **Finish line** with congratulations message and bonus coins | [ ] |
| 12 | **Playtested** and at least 2 issues fixed | [ ] |

**Total requirements completed: _______ / 12**

---

##### Part 3: Checkpoint Script Template

**Instructions:** Use this template for each checkpoint. Change the STAGE_NUMBER for each one.

```lua
-- Checkpoint Script for Stage ___
-- Place this inside a SpawnLocation Part

local checkpoint = script.Parent
local STAGE_NUMBER = ___  -- CHANGE THIS for each checkpoint

local debounce = false

local function onTouched(otherPart)
    if debounce then return end

    local character = otherPart.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        local Players = game:GetService("Players")
        local player = Players:GetPlayerFromCharacter(character)

        if player then
            local leaderstats = player:FindFirstChild("leaderstats")
            if leaderstats then
                local stage = leaderstats:FindFirstChild("Stage")
                if stage and stage.Value < STAGE_NUMBER then
                    debounce = true
                    stage.Value = STAGE_NUMBER
                    player.RespawnLocation = checkpoint
                    print(player.Name .. " reached Stage " .. STAGE_NUMBER)

                    -- Visual feedback
                    checkpoint.Color = Color3.fromRGB(0, 255, 0)
                    checkpoint.Material = Enum.Material.Neon
                    task.wait(1)
                    checkpoint.Color = Color3.fromRGB(100, 100, 100)
                    checkpoint.Material = Enum.Material.SmoothPlastic

                    debounce = false
                end
            end
        end
    end
end

checkpoint.Touched:Connect(onTouched)
```

**Checkpoint Log:**

| Checkpoint | Stage Number | Position (X, Y, Z) | Script Working? |
|-----------|-------------|--------------------|-----------------|
| Spawn | 1 | (______, ______, ______) | [ ] Yes |
| Checkpoint 1 | 2 | (______, ______, ______) | [ ] Yes |
| Checkpoint 2 | 3 | (______, ______, ______) | [ ] Yes |
| Checkpoint 3 | 4 | (______, ______, ______) | [ ] Yes |
| Checkpoint 4 | 5 | (______, ______, ______) | [ ] Yes |

---

##### Part 4: Mechanics Inventory

**Instructions:** List every mechanic you used in your Obby and which stage it appears in.

| Mechanic | Stage(s) Used In | How It Works |
|----------|-----------------|-------------|
| Kill Brick | _________________ | _________________________________ |
| Speed Boost | _________________ | _________________________________ |
| Jump Pad | _________________ | _________________________________ |
| Collectible Coins | _________________ | _________________________________ |
| (Other) _____________ | _________________ | _________________________________ |
| (Other) _____________ | _________________ | _________________________________ |

---

##### Part 5: Playtesting Record

**Instructions:** Playtest your Obby at least twice. Record any issues you find and how you fixed them.

**Playtest 1 (self-test):**

| Issue Found | How I Fixed It |
|------------|---------------|
| _________________________________ | _________________________________ |
| _________________________________ | _________________________________ |
| _________________________________ | _________________________________ |

**Playtest 2 (partner test):**

Partner's name: ______________________________

| Partner's Feedback | Action I Took |
|-------------------|--------------|
| _________________________________ | _________________________________ |
| _________________________________ | _________________________________ |
| _________________________________ | _________________________________ |

---

##### Part 6: Partner Obby Review

**Instructions:** Play your partner's Obby and provide constructive feedback.

**Partner's name:** ______________________________
**Obby name:** ______________________________

1. What was the most fun part of their Obby?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Was there any part that felt unfair or too difficult? Which stage?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. What is one specific suggestion to make their Obby even better?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

4. Rate the Obby (circle one):

`Needs Work` — `Good Start` — `Fun to Play` — `Really Polished` — `I Would Play This Again`

---

##### Reflection

1. What are you most proud of in your Obby? Why?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. What was the most challenging part of the project? How did you overcome it?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. If you had one more hour to work on your Obby, what would you add or change?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

4. How did playtesting change your perspective on your own game?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge: Advanced Features

Complete one or more of these advanced features and describe what you did:

- [ ] **Moving Platform** — A platform that moves back and forth using TweenService.
- [ ] **Disappearing Platform** — A platform that fades away and reappears on a timer.
- [ ] **Secret Bonus Room** — A hidden area with extra coins, accessible through an invisible wall.
- [ ] **Finish Line Timer** — Displays how long it took the player to complete the Obby.
- [ ] **Custom Tool** — A tool from Session 6 integrated into the Obby (e.g., a speed boost tool).

**Which feature(s) did you add?** ______________________________

**Describe how it works:**

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

*Congratulations on completing your first Roblox game! Save your project — this is your first portfolio piece.*
# Roblox Studio Intermediate: Lesson Plans & Worksheets
## Unit 3: Advanced Scripting & Data Systems (Sessions 9-12)

### Unit Overview

Unit 3 elevates students from basic scripting to professional-level Luau programming patterns used in real Roblox games. Students begin by mastering tables — the single most versatile data structure in Luau — learning to build arrays, dictionaries, and nested tables that power everything from inventory systems to game configurations. They then discover ModuleScripts, the backbone of organised Roblox codebases, and learn to split their game logic into reusable, require()-able modules. The unit's most conceptually demanding session introduces the client-server model: students learn why Roblox separates client and server execution, how RemoteEvents and RemoteFunctions bridge that gap, and why server-side validation is non-negotiable for any published game. The unit culminates in Project 2 — a functional tycoon game that ties together tables, ModuleScripts, RemoteEvents, and DataStoreService, giving students a tangible, publishable creation that demonstrates every concept from the unit.

---

### Session 9: Tables, Arrays, and Dictionaries in Luau

---

#### SESSION 9 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 9 of 24 |
| **Title** | Tables, Arrays, and Dictionaries in Luau |
| **Unit** | Unit 3: Advanced Scripting & Data Systems |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Create and manipulate Luau tables used as arrays, including inserting, removing, and accessing elements by numeric index.
2. Create and manipulate Luau tables used as dictionaries, storing and retrieving values by string keys.
3. Iterate over arrays using `ipairs()` and over dictionaries using `pairs()`, explaining the difference between the two functions.
4. Build a functional inventory system that uses a table of dictionaries to store item names, quantities, and properties, and display the inventory contents using a loop.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 9 Worksheet (printed or displayed digitally)
- Whiteboard or interactive whiteboard for diagramming table structures
- Timer or stopwatch for timed activities
- Teacher reference: Roblox Creator Documentation bookmarked at `https://create.roblox.com/docs`
- Students' existing Roblox Studio project from Sessions 1-8

##### Procedure

**0-5 min: Warm-Up — "What Would You Store?"**

- As students settle, display the following prompt on the board: *"Imagine you are building an RPG game. List five pieces of information you would need to store about the player's inventory."*
- Allow 90 seconds of quiet thinking. Then invite five or six students to share. Write each response on the board.
- Typical responses: "item names," "how many of each item," "item rarity," "item damage," "whether the item is equipped."
- Say: *"Every single one of these needs to be stored somewhere in your code. But imagine you have 50 different items. Would you create 50 separate variables? That would be insane. Today we learn about TABLES — the single most powerful data structure in Luau. Tables let you store entire collections of data in one variable."*

**5-15 min: Introduction — Tables as Arrays**

- Open Roblox Studio on the projector. Create a new Script inside ServerScriptService for demonstration purposes.
- Write the following code on the projector, explaining each line:

  ```lua
  -- An array is a table with numbered positions (indices)
  local fruits = {"Apple", "Banana", "Cherry", "Dragonfruit"}

  -- Accessing elements (Luau arrays start at index 1, not 0!)
  print(fruits[1])  -- Output: Apple
  print(fruits[3])  -- Output: Cherry

  -- Getting the length of an array
  print(#fruits)  -- Output: 4

  -- Adding an element to the end
  table.insert(fruits, "Elderberry")
  print(#fruits)  -- Output: 5

  -- Inserting at a specific position
  table.insert(fruits, 2, "Blueberry")
  -- Now: {"Apple", "Blueberry", "Banana", "Cherry", "Dragonfruit", "Elderberry"}

  -- Removing an element by position
  table.remove(fruits, 1)
  -- Now: {"Blueberry", "Banana", "Cherry", "Dragonfruit", "Elderberry"}

  -- Replacing an element
  fruits[3] = "Coconut"
  -- Now: {"Blueberry", "Banana", "Coconut", "Dragonfruit", "Elderberry"}
  ```

- Emphasise: *"In Luau, arrays start at index 1, not 0. This is different from many other programming languages. If you have used Python or JavaScript before, be careful — Luau counts from 1."*
- Run the script and show the output. Ask: *"What happens if I try to access `fruits[10]` when the array only has 5 elements?"* Run it and show: it returns `nil`. Explain: *"Nil means 'nothing' in Luau. Accessing an index that does not exist gives you nil — it does not crash. But you need to be careful, because nil can cause unexpected behaviour downstream."*

**15-35 min: Guided Practice — Dictionaries and Iteration**

- Continue on the projector, building on the previous script:

  ```lua
  -- A dictionary uses string keys instead of number indices
  local playerStats = {
      Name = "HeroPlayer",
      Health = 100,
      MaxHealth = 100,
      Level = 5,
      Experience = 2350,
      IsAlive = true
  }

  -- Accessing values with dot notation
  print(playerStats.Name)       -- Output: HeroPlayer
  print(playerStats.Health)     -- Output: 100

  -- Accessing values with bracket notation
  print(playerStats["Level"])   -- Output: 5

  -- Modifying values
  playerStats.Health = 75
  playerStats.Experience = playerStats.Experience + 100
  print(playerStats.Health)      -- Output: 75
  print(playerStats.Experience)  -- Output: 2450

  -- Adding new keys
  playerStats.Gold = 500
  print(playerStats.Gold)  -- Output: 500
  ```

- Say: *"Dot notation and bracket notation do the same thing. Use dot notation when the key is a simple word. Use bracket notation when the key is stored in a variable or contains spaces."*
- Demonstrate bracket notation with a variable:

  ```lua
  local keyName = "Health"
  print(playerStats[keyName])  -- Output: 75
  ```

- Now introduce iteration:

  ```lua
  -- ipairs() iterates over arrays in order (index 1, 2, 3, ...)
  local weapons = {"Sword", "Bow", "Staff", "Dagger"}

  print("=== Weapons (ipairs) ===")
  for index, weapon in ipairs(weapons) do
      print("Slot " .. index .. ": " .. weapon)
  end
  -- Output:
  -- Slot 1: Sword
  -- Slot 2: Bow
  -- Slot 3: Staff
  -- Slot 4: Dagger

  -- pairs() iterates over ALL keys in a dictionary (order is NOT guaranteed)
  print("=== Player Stats (pairs) ===")
  for key, value in pairs(playerStats) do
      print(key .. " = " .. tostring(value))
  end
  ```

- Run the code. Point out that `pairs()` output order may vary each time: *"Dictionaries do not have a guaranteed order. If you need order, use an array. If you need named access, use a dictionary. Sometimes you need both — and that is where nested tables come in."*

- Demonstrate nested tables — an array of dictionaries:

  ```lua
  -- Nested tables: an array of dictionaries
  local inventory = {
      {Name = "Health Potion", Quantity = 5, Rarity = "Common"},
      {Name = "Iron Sword", Quantity = 1, Rarity = "Uncommon"},
      {Name = "Dragon Shield", Quantity = 1, Rarity = "Rare"},
      {Name = "Magic Scroll", Quantity = 3, Rarity = "Common"},
  }

  -- Print the full inventory
  print("=== Player Inventory ===")
  for i, item in ipairs(inventory) do
      print(i .. ". " .. item.Name .. " (x" .. item.Quantity .. ") [" .. item.Rarity .. "]")
  end

  -- Find a specific item
  local function findItem(inv, itemName)
      for _, item in ipairs(inv) do
          if item.Name == itemName then
              return item
          end
      end
      return nil  -- Item not found
  end

  local potion = findItem(inventory, "Health Potion")
  if potion then
      print("Found: " .. potion.Name .. " x" .. potion.Quantity)
  else
      print("Item not found!")
  end
  ```

- Walk through the `findItem` function line by line. Ask: *"Why do we use `_` as the first variable in the loop?"* Answer: *"The underscore is a convention that means 'I do not need this value.' We do not need the index inside the loop — we only need the item dictionary."*

- Students follow along at their machines, typing each code block into their own Script. Pause after each block to ensure everyone has caught up.

**35-60 min: Independent Practice — Building an Inventory System**

- Direct students to Part 2 of the worksheet. They will build a complete inventory system from scratch. The requirements are:
  1. Create an `inventory` table (array of dictionaries) with at least 6 items, each having `Name`, `Quantity`, `Type`, and `Value` fields.
  2. Write a `displayInventory()` function that prints all items in a formatted way.
  3. Write an `addItem()` function that either adds a new item or increases quantity if it already exists.
  4. Write a `removeItem()` function that decreases quantity or removes the item entirely if quantity hits 0.
  5. Write a `getTotalValue()` function that calculates the total gold value of all items.

- Circulate the room. Common issues to watch for:
  - Students forgetting to use `table.insert` and instead writing `inventory[#inventory + 1] = newItem` — both work, but `table.insert` is clearer.
  - Students forgetting that `table.remove` requires the index, not the value — they need to find the index first.
  - Off-by-one errors when accessing arrays.

- If a student finishes early, direct them to the Bonus Challenge on the worksheet.

**60-75 min: Extension/Advanced Activity — Sorting and Filtering Tables**

- Introduce `table.sort()` on the projector:

  ```lua
  -- Sorting an array of dictionaries by a specific field
  local items = {
      {Name = "Copper Coin", Value = 1},
      {Name = "Gold Bar", Value = 100},
      {Name = "Silver Ring", Value = 25},
      {Name = "Diamond", Value = 500},
      {Name = "Iron Ore", Value = 10},
  }

  -- Sort by value (ascending)
  table.sort(items, function(a, b)
      return a.Value < b.Value
  end)

  print("=== Items Sorted by Value (Low to High) ===")
  for i, item in ipairs(items) do
      print(i .. ". " .. item.Name .. " - " .. item.Value .. " gold")
  end

  -- Sort by value (descending)
  table.sort(items, function(a, b)
      return a.Value > b.Value
  end)

  print("=== Items Sorted by Value (High to Low) ===")
  for i, item in ipairs(items) do
      print(i .. ". " .. item.Name .. " - " .. item.Value .. " gold")
  end

  -- Filtering: create a new table with only items above a certain value
  local function filterByMinValue(itemList, minValue)
      local result = {}
      for _, item in ipairs(itemList) do
          if item.Value >= minValue then
              table.insert(result, item)
          end
      end
      return result
  end

  local expensiveItems = filterByMinValue(items, 25)
  print("=== Items Worth 25+ Gold ===")
  for _, item in ipairs(expensiveItems) do
      print(item.Name .. " - " .. item.Value .. " gold")
  end
  ```

- Students add sorting and filtering functions to their own inventory system.
- Challenge advanced students: *"Can you sort your inventory alphabetically by item name? Can you filter by item type?"*

**75-85 min: Sharing/Discussion**

- Ask 2-3 students to share their inventory systems on the projector. Discuss:
  - *"How did you handle the case where a player tries to remove an item they do not have?"*
  - *"What happens if two items have the same name but different types?"*
  - *"How would you modify your system to support a maximum inventory size?"*
- Ask the class: *"When would you use an array versus a dictionary? Give me a game example for each."*
- Guide to answers: arrays for ordered lists (inventory slots, leaderboards, wave spawn orders), dictionaries for named lookups (player stats, game settings, item definitions).

**85-90 min: Closure & Preview**

- Ask: *"What is the ONE most important thing you learned about tables today?"* Take three responses.
- Preview Session 10: *"Today you put all your code in one script. But real Roblox games have dozens of scripts. Next session, we learn ModuleScripts — the way professional developers organise their code so that every script can share functions and data without repeating itself."*
- Remind students: *"Save your project. You will use your inventory system again in Session 12."*

##### Differentiation

**Support:**
- Provide a printed "Tables Cheat Sheet" with syntax examples for creating arrays, dictionaries, using `table.insert`, `table.remove`, `ipairs()`, and `pairs()` — students can refer to this throughout the session.
- Pre-write the skeleton of the inventory system (function signatures with comments describing what each should do) so struggling students only need to fill in the function bodies.
- Pair struggling students with a confident partner during independent practice; the stronger student explains concepts while the other types the code.

**Extension:**
- Challenge advanced students to build a "shop system" where a separate `shopInventory` table exists and the player can buy items (transferring from shop to player inventory, deducting gold).
- Ask them to implement a `stackLimit` property on each item so that no single inventory entry can have a Quantity above a defined maximum — excess items should create a new stack.
- Have them research and implement Luau's `table.find()` function and rewrite their `findItem` function using it.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Array creation and manipulation | Cannot create or access arrays | Creates arrays but struggles with insert/remove | Creates, accesses, inserts, and removes elements correctly | Fluently manipulates arrays including edge cases (empty arrays, nil checks) |
| Dictionary creation and access | Cannot create dictionaries | Creates dictionaries but confuses dot and bracket notation | Uses both dot and bracket notation correctly; adds and modifies keys | Creates nested dictionaries, uses variable keys, and explains when to use each notation |
| Iteration with ipairs/pairs | Cannot write a for loop over a table | Writes a loop but confuses ipairs and pairs | Uses ipairs for arrays and pairs for dictionaries correctly | Explains ordering behaviour, uses underscore convention, and applies loops to nested structures |
| Inventory system completeness | No inventory system attempted | Partial system with 1-2 functions working | All four required functions work correctly | Complete system with sorting, filtering, and robust error handling |

##### Teacher Notes

- The most common conceptual hurdle is that Luau tables serve as BOTH arrays and dictionaries — there is no separate data type. Reinforce that a table with consecutive integer keys (1, 2, 3) behaves like an array, while a table with string keys behaves like a dictionary. A single table can even have both, though this is rare in practice.
- Students coming from Python may try to use `len()` instead of `#` for array length. Gently correct and explain the `#` operator.
- When using `pairs()`, the iteration order is non-deterministic. If students ask why their output is in a different order from the projector, explain that this is by design — dictionaries are unordered.
- The `table.remove()` function shifts elements down to fill the gap. If students remove elements while iterating forward, they may skip elements. Teach them to iterate backwards when removing: `for i = #array, 1, -1 do`.
- Some students may want to use `table.clear()` — this function empties the entire table and is available in Luau. Mention it briefly but ensure students understand it is destructive.
- Save 2-3 minutes at the end to ensure every student has saved their project — the inventory code will be reused in Session 12's tycoon project.

---

#### SESSION 9 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 9: Tables, Arrays, and Dictionaries in Luau**

---

##### Part 1: Table Basics — Arrays

**Instructions:** Open your Roblox Studio project. Create a new **Script** inside **ServerScriptService** and name it `TablePractice`. Type each code block below, predict the output, then run the script to check your prediction.

**Exercise 1: Creating and Accessing Arrays**

```lua
local colours = {"Red", "Green", "Blue", "Yellow", "Purple"}

print(colours[1])
print(colours[4])
print(#colours)
print(colours[6])
```

**Your prediction:**
- `colours[1]` will print: _______________
- `colours[4]` will print: _______________
- `#colours` will print: _______________
- `colours[6]` will print: _______________

**Actual output (after running):**
- `colours[1]` printed: _______________
- `colours[4]` printed: _______________
- `#colours` printed: _______________
- `colours[6]` printed: _______________

**Were your predictions correct?** [ ] Yes [ ] Partially [ ] No

---

**Exercise 2: Modifying Arrays**

```lua
local animals = {"Cat", "Dog", "Fish"}

-- Add "Hamster" to the end
table.insert(animals, "Hamster")

-- Add "Bird" at position 2
table.insert(animals, 2, "Bird")

-- Remove the element at position 3
table.remove(animals, 3)

-- Print all elements
for i, animal in ipairs(animals) do
    print(i .. ": " .. animal)
end
```

**Before running, write what you think the final array contains (in order):**

1. _______________
2. _______________
3. _______________
4. _______________

**After running, write the actual output:**

1. _______________
2. _______________
3. _______________
4. _______________

**Question:** Why did removing position 3 remove "Dog" and not "Fish"? (Hint: think about what happened after the insert at position 2.)

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 2: Dictionaries

**Instructions:** Continue in the same script. Add the following code below your previous work.

**Exercise 3: Create a Player Stats Dictionary**

Write a dictionary called `playerStats` that stores the following information:

| Key | Value |
|-----|-------|
| Name | Your character's name (a string) |
| Health | 100 |
| MaxHealth | 100 |
| Attack | 25 |
| Defense | 15 |
| Speed | 10.5 |
| IsAlive | true |

Write your code here:

```lua
local playerStats = {
    ____________________________________________
    ____________________________________________
    ____________________________________________
    ____________________________________________
    ____________________________________________
    ____________________________________________
    ____________________________________________
}
```

Now print the player's Name, Health, and Attack using dot notation:

```lua
print("Name: " .. __________________)
print("Health: " .. __________________)
print("Attack: " .. __________________)
```

**Exercise 4: Modifying and Iterating Over a Dictionary**

```lua
-- Reduce health by 30
playerStats.Health = playerStats.Health - 30

-- Check if player should be alive
if playerStats.Health <= 0 then
    playerStats.IsAlive = false
    print(playerStats.Name .. " has been defeated!")
else
    print(playerStats.Name .. " has " .. playerStats.Health .. " HP remaining.")
end

-- Print ALL stats using pairs()
print("=== Full Stats ===")
for key, value in pairs(playerStats) do
    print(key .. ": " .. tostring(value))
end
```

**Question:** Why do we need `tostring(value)` when printing with `pairs()`?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 3: Build an Inventory System

**Instructions:** Create a new Script inside ServerScriptService called `InventorySystem`. Build a complete inventory system following the steps below.

**Step 1:** Create your inventory table — an array of dictionaries. Each item must have `Name`, `Quantity`, `Type`, and `Value` fields. Include at least 6 items.

```lua
local inventory = {
    {Name = "Health Potion", Quantity = 5, Type = "Consumable", Value = 10},
    {Name = "Iron Sword", Quantity = 1, Type = "Weapon", Value = 50},
    -- Add at least 4 more items below:
    ________________________________________________________________
    ________________________________________________________________
    ________________________________________________________________
    ________________________________________________________________
}
```

**Step 2:** Write a `displayInventory()` function that prints all items in a neat format.

```lua
local function displayInventory()
    print("========== INVENTORY ==========")
    for i, item in ipairs(inventory) do
        -- Print each item in this format: "1. Health Potion (x5) [Consumable] - 10 gold"
        ________________________________________________________________
    end
    print("===============================")
end

displayInventory()
```

**Step 3:** Write an `addItem()` function. If the item already exists, increase its quantity. If not, add a new entry.

```lua
local function addItem(name, quantity, itemType, value)
    -- First, check if the item already exists
    for _, item in ipairs(inventory) do
        if item.Name == name then
            ________________________________________
            print("Updated: " .. name .. " now x" .. item.Quantity)
            return
        end
    end

    -- If we get here, the item was not found — add it as new
    ________________________________________________________________
    print("Added new item: " .. name)
end

-- Test it:
addItem("Health Potion", 3, "Consumable", 10)  -- Should increase existing quantity
addItem("Magic Ring", 1, "Accessory", 200)      -- Should add new item
displayInventory()
```

**Step 4:** Write a `removeItem()` function. Decrease quantity, or remove entirely if quantity reaches 0.

```lua
local function removeItem(name, quantity)
    for i, item in ipairs(inventory) do
        if item.Name == name then
            item.Quantity = item.Quantity - quantity
            if item.Quantity <= 0 then
                ________________________________________
                print("Removed: " .. name .. " from inventory")
            else
                print("Updated: " .. name .. " now x" .. item.Quantity)
            end
            return
        end
    end
    print("Item not found: " .. name)
end

-- Test it:
removeItem("Health Potion", 2)
removeItem("Iron Sword", 1)  -- Should remove entirely (quantity becomes 0)
displayInventory()
```

**Step 5:** Write a `getTotalValue()` function that returns the total gold value of the inventory.

```lua
local function getTotalValue()
    local total = 0
    for _, item in ipairs(inventory) do
        ________________________________________
    end
    return total
end

print("Total inventory value: " .. getTotalValue() .. " gold")
```

**Checkpoint:** Run your script. Does the inventory display correctly? Do add and remove work? [ ] Yes [ ] No

---

##### Part 4: Challenge — Filtering and Sorting

**Challenge 1:** Write a function that returns only items of a specific type.

```lua
local function getItemsByType(itemType)
    local result = {}
    ________________________________________________________________
    ________________________________________________________________
    ________________________________________________________________
    ________________________________________________________________
    return result
end

-- Test: print all "Consumable" items
local consumables = getItemsByType("Consumable")
print("=== Consumable Items ===")
for _, item in ipairs(consumables) do
    print(item.Name .. " x" .. item.Quantity)
end
```

**Challenge 2:** Sort the inventory by value (highest first) and display it.

```lua
-- Hint: use table.sort() with a custom comparison function
table.sort(inventory, function(a, b)
    ________________________________________
end)

print("=== Inventory Sorted by Value ===")
displayInventory()
```

---

##### Bonus Challenge

Build a complete "Loot Drop" system:

1. Create a `lootTable` with items and their drop chances (as percentages that add up to 100).
2. Write a function `rollLoot()` that randomly selects an item based on the drop chances using `math.random()`.
3. Call `rollLoot()` ten times, adding each dropped item to the player's inventory using your `addItem()` function.
4. Display the final inventory.

```lua
local lootTable = {
    {Name = "Gold Coin", DropChance = 40},
    {Name = "Health Potion", DropChance = 30},
    {Name = "Iron Ore", DropChance = 20},
    {Name = "Rare Gem", DropChance = 10},
}

local function rollLoot()
    local roll = math.random(1, 100)
    local cumulative = 0
    for _, loot in ipairs(lootTable) do
        cumulative = cumulative + loot.DropChance
        if roll <= cumulative then
            return loot.Name
        end
    end
    return lootTable[#lootTable].Name  -- Fallback
end

-- Roll 10 times and add to inventory
for i = 1, 10 do
    local droppedItem = rollLoot()
    print("Loot drop #" .. i .. ": " .. droppedItem)
    addItem(droppedItem, 1, "Loot", 25)
end

displayInventory()
```

---

##### Reflection

1. What is the difference between `ipairs()` and `pairs()`? When would you use each one?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Why are nested tables (an array of dictionaries) so useful for game development? Give a specific example from a game you would like to build.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. What was the hardest part of building the inventory system? How did you solve it?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

### Session 10: ModuleScripts and Code Organization

---

#### SESSION 10 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 10 of 24 |
| **Title** | ModuleScripts and Code Organization |
| **Unit** | Unit 3: Advanced Scripting & Data Systems |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Explain what a ModuleScript is, how it differs from a regular Script and LocalScript, and why ModuleScripts are essential for code organisation in larger Roblox projects.
2. Create a ModuleScript that returns a table of shared utility functions and use `require()` to load and call those functions from other scripts.
3. Build a GameConfig ModuleScript that centralises game settings (such as starting health, walk speed, currency name) so that changes propagate to all scripts that reference it.
4. Organise a multi-script project with a clear folder structure inside ReplicatedStorage and ServerScriptService, demonstrating the single-responsibility principle.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 10 Worksheet (printed or displayed digitally)
- Whiteboard for drawing module dependency diagrams
- Timer or stopwatch for timed activities
- Students' project from previous sessions
- Teacher reference: Roblox Creator Documentation — ModuleScript page

##### Procedure

**0-5 min: Warm-Up — "The Copy-Paste Problem"**

- Display two code blocks on the board, each in a different script, both containing the exact same function — a `formatNumber()` that adds commas to large numbers.
- Ask: *"What is wrong with this situation?"*
- Take responses. Guide to the key problem: *"If you need to fix a bug in this function, you have to find and fix it in EVERY script that has a copy. Miss one, and your game breaks in one place but not another. This is the copy-paste problem — and it is one of the most common reasons real game projects become unmaintainable."*
- Say: *"Today we learn the solution: ModuleScripts. Write the function once, share it everywhere."*

**5-15 min: Introduction — What Are ModuleScripts?**

- Open Roblox Studio on the projector. Explain the three script types in Roblox:
  - **Script** — runs on the server. Used for game logic, data handling, security.
  - **LocalScript** — runs on the client (the player's computer). Used for UI, camera, input.
  - **ModuleScript** — does NOT run on its own. It is a library of code that other scripts can load using `require()`. It can be used by both Scripts and LocalScripts.
- Say: *"A ModuleScript is like a toolbox. On its own, it just sits there. But any script that needs a tool can open the toolbox and grab what it needs."*
- Draw a diagram on the whiteboard:

  ```
  [ModuleScript: MathUtils]
       |           |
       v           v
  [Script A]  [Script B]
  (both use the same functions)
  ```

- Create a ModuleScript in ReplicatedStorage on the projector. Name it `MathUtils`. Show the default code:

  ```lua
  local MathUtils = {}

  return MathUtils
  ```

- Explain: *"Every ModuleScript MUST return something — usually a table. This table is what other scripts receive when they call `require()`. Think of it as: the ModuleScript packs up a care package, and `require()` delivers it."*

**15-35 min: Guided Practice — Building and Using ModuleScripts**

- Build the `MathUtils` module step by step on the projector:

  ```lua
  -- ModuleScript: MathUtils (in ReplicatedStorage)
  local MathUtils = {}

  -- Clamp a number between a minimum and maximum value
  function MathUtils.clamp(value, min, max)
      if value < min then
          return min
      elseif value > max then
          return max
      else
          return value
      end
  end

  -- Round a number to a specified number of decimal places
  function MathUtils.round(value, decimals)
      local multiplier = 10 ^ (decimals or 0)
      return math.floor(value * multiplier + 0.5) / multiplier
  end

  -- Format a number with commas (e.g., 1234567 becomes "1,234,567")
  function MathUtils.formatWithCommas(number)
      local formatted = tostring(math.floor(number))
      local result = ""
      local count = 0
      for i = #formatted, 1, -1 do
          count = count + 1
          result = string.sub(formatted, i, i) .. result
          if count % 3 == 0 and i > 1 then
              result = "," .. result
          end
      end
      return result
  end

  -- Calculate the percentage of a value relative to a maximum
  function MathUtils.percentage(current, maximum)
      if maximum == 0 then
          return 0
      end
      return MathUtils.round((current / maximum) * 100, 1)
  end

  return MathUtils
  ```

- Now create a Script in ServerScriptService called `TestMathUtils`:

  ```lua
  -- Script: TestMathUtils (in ServerScriptService)
  local ReplicatedStorage = game:GetService("ReplicatedStorage")
  local MathUtils = require(ReplicatedStorage:WaitForChild("MathUtils"))

  -- Test clamp
  print(MathUtils.clamp(150, 0, 100))   -- Output: 100
  print(MathUtils.clamp(-20, 0, 100))   -- Output: 0
  print(MathUtils.clamp(50, 0, 100))    -- Output: 50

  -- Test round
  print(MathUtils.round(3.14159, 2))    -- Output: 3.14
  print(MathUtils.round(3.14159, 0))    -- Output: 3

  -- Test formatWithCommas
  print(MathUtils.formatWithCommas(1234567))   -- Output: 1,234,567
  print(MathUtils.formatWithCommas(42))        -- Output: 42

  -- Test percentage
  print(MathUtils.percentage(75, 100))   -- Output: 75
  print(MathUtils.percentage(33, 200))   -- Output: 16.5
  ```

- Run the game and show the output. Emphasise: *"`require()` only runs the ModuleScript once. The first time any script calls `require()`, Luau executes the ModuleScript and caches the returned table. Every subsequent `require()` call gets the SAME cached table. This means if one script modifies a value in the module's table, every other script that required the same module will see the change."*

- Next, build a `GameConfig` module — a centralised settings file:

  ```lua
  -- ModuleScript: GameConfig (in ReplicatedStorage)
  local GameConfig = {}

  -- Player settings
  GameConfig.StartingHealth = 100
  GameConfig.MaxHealth = 100
  GameConfig.StartingWalkSpeed = 16
  GameConfig.SprintSpeed = 24
  GameConfig.JumpPower = 50

  -- Currency settings
  GameConfig.CurrencyName = "Coins"
  GameConfig.StartingCurrency = 100

  -- Game rules
  GameConfig.MaxPlayers = 12
  GameConfig.RoundDuration = 180  -- seconds
  GameConfig.RespawnTime = 5      -- seconds

  -- Difficulty scaling
  GameConfig.EnemyHealthMultiplier = 1.0
  GameConfig.LootDropRate = 0.25  -- 25% chance

  return GameConfig
  ```

- Show how to use it from another script:

  ```lua
  -- Script: PlayerSetup (in ServerScriptService)
  local ReplicatedStorage = game:GetService("ReplicatedStorage")
  local Players = game:GetService("Players")
  local GameConfig = require(ReplicatedStorage:WaitForChild("GameConfig"))

  Players.PlayerAdded:Connect(function(player)
      player.CharacterAdded:Connect(function(character)
          local humanoid = character:WaitForChild("Humanoid")
          humanoid.MaxHealth = GameConfig.MaxHealth
          humanoid.Health = GameConfig.StartingHealth
          humanoid.WalkSpeed = GameConfig.StartingWalkSpeed
          humanoid.JumpPower = GameConfig.JumpPower
          print(player.Name .. " spawned with " .. GameConfig.StartingHealth .. " HP")
      end)
  end)
  ```

- Say: *"Now, if I want to change the starting health for all players, I change ONE number in GameConfig. Every script that uses GameConfig automatically gets the new value. This is the power of centralised configuration."*

- Students follow along, creating both ModuleScripts and the test scripts at their machines.

**35-60 min: Independent Practice — Create Your Own Modules**

- Direct students to Part 2 of the worksheet. They will create:
  1. A `StringUtils` ModuleScript with at least 3 string utility functions.
  2. A `GameConfig` ModuleScript customised for their own game idea.
  3. A test script that demonstrates both modules working together.

- Circulate the room. Watch for:
  - Students placing ModuleScripts in the wrong location (they should be in ReplicatedStorage if both client and server need them, or ServerScriptService if only the server needs them).
  - Forgetting to `return` the table at the end of the ModuleScript.
  - Typos in `require()` paths — `WaitForChild` must match the exact name of the ModuleScript.

**60-75 min: Extension/Advanced Activity — Module Dependencies and Folder Structure**

- Show a more complex project structure on the projector:

  ```
  ReplicatedStorage/
  ├── Modules/
  │   ├── MathUtils (ModuleScript)
  │   ├── StringUtils (ModuleScript)
  │   ├── GameConfig (ModuleScript)
  │   └── ItemDatabase (ModuleScript)
  ServerScriptService/
  ├── GameManager (Script)
  ├── PlayerSetup (Script)
  └── LootSystem (Script)
  StarterPlayerScripts/
  └── UIController (LocalScript)
  ```

- Create an `ItemDatabase` module that depends on `GameConfig`:

  ```lua
  -- ModuleScript: ItemDatabase (in ReplicatedStorage/Modules)
  local ReplicatedStorage = game:GetService("ReplicatedStorage")
  local GameConfig = require(ReplicatedStorage:WaitForChild("Modules"):WaitForChild("GameConfig"))

  local ItemDatabase = {}

  ItemDatabase.Items = {
      ["Health Potion"] = {
          Type = "Consumable",
          BaseValue = 10,
          Effect = "Heal",
          Amount = math.floor(GameConfig.MaxHealth * 0.3),  -- Heals 30% of max HP
          Rarity = "Common",
          DropWeight = 40,
      },
      ["Speed Boost"] = {
          Type = "Consumable",
          BaseValue = 25,
          Effect = "Speed",
          Amount = GameConfig.SprintSpeed - GameConfig.StartingWalkSpeed,
          Duration = 10,
          Rarity = "Uncommon",
          DropWeight = 20,
      },
      ["Iron Sword"] = {
          Type = "Weapon",
          BaseValue = 100,
          Damage = 15,
          AttackSpeed = 1.2,
          Rarity = "Common",
          DropWeight = 30,
      },
      ["Diamond Shield"] = {
          Type = "Armor",
          BaseValue = 250,
          Defense = 20,
          Rarity = "Rare",
          DropWeight = 10,
      },
  }

  function ItemDatabase.getItem(name)
      return ItemDatabase.Items[name]
  end

  function ItemDatabase.getItemsByRarity(rarity)
      local result = {}
      for name, data in pairs(ItemDatabase.Items) do
          if data.Rarity == rarity then
              result[name] = data
          end
      end
      return result
  end

  function ItemDatabase.getItemsByType(itemType)
      local result = {}
      for name, data in pairs(ItemDatabase.Items) do
          if data.Type == itemType then
              result[name] = data
          end
      end
      return result
  end

  return ItemDatabase
  ```

- Say: *"Notice how ItemDatabase uses values from GameConfig — the Health Potion heals 30% of MaxHealth, and the Speed Boost amount is calculated from the sprint and walk speeds. If you change MaxHealth in GameConfig, the potion automatically adjusts. This is the power of modules depending on other modules."*

- Advanced students organise their project into folders and create module dependencies.

**75-85 min: Sharing/Discussion**

- Ask 2-3 students to share their `GameConfig` on the projector. Discuss:
  - *"What settings did you include? Why those?"*
  - *"If you wanted to add a 'Hard Mode' to your game, how would you change GameConfig to support it?"*
- Discuss the single-responsibility principle: *"Each module should do ONE thing well. MathUtils handles math. StringUtils handles strings. GameConfig holds settings. ItemDatabase holds item data. You would never put string functions inside your GameConfig module. Why?"*
- Take responses. Reinforce: *"Because when something breaks, you want to know exactly which module to look at. And when another developer reads your code, the module name tells them what is inside."*

**85-90 min: Closure & Preview**

- Ask: *"Name one benefit of using ModuleScripts over copy-pasting code."* Take three responses.
- Preview Session 11: *"We now know how to organise code. But there is a bigger question: WHERE does code run? In Roblox, some code runs on your computer and some runs on the server. Next session, we learn about the client-server model and how to send messages between them using RemoteEvents."*
- Remind students to save their project.

##### Differentiation

**Support:**
- Provide a "ModuleScript Template" handout showing the exact structure of a basic ModuleScript with blanks for students to fill in their own function names and logic.
- Walk struggling students through the `require()` process step by step: (1) identify where the ModuleScript is, (2) build the path using `game:GetService()` and `WaitForChild()`, (3) store the result in a local variable.
- Allow struggling students to create a simpler ModuleScript with just 2 functions (e.g., `add` and `subtract`) before tackling the more complex utility modules.

**Extension:**
- Challenge advanced students to create a `WeaponDatabase` ModuleScript that stores weapon stats and a `CombatUtils` module that imports both `WeaponDatabase` and `MathUtils` to calculate damage with clamping and rounding.
- Ask them to implement a "module loader" pattern where a single master module requires all sub-modules and exposes them through a single table.
- Have them investigate `shared` (a global table accessible to all server scripts) and explain why ModuleScripts are preferred over using `shared` for code organisation.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Understands ModuleScript purpose | Cannot explain what a ModuleScript is | Describes ModuleScripts vaguely as "shared code" | Explains how ModuleScripts return tables and are loaded with require() | Explains caching behaviour, placement rules, and single-responsibility benefits |
| Creates functional ModuleScripts | Cannot create a working ModuleScript | Creates a module but forgets return statement or has syntax errors | Creates a module with 3+ functions that return correct results | Creates multiple interdependent modules with clean, well-documented code |
| Uses require() correctly | Cannot load a ModuleScript | Uses require() but with incorrect paths | Uses require() with proper GetService and WaitForChild paths | Requires modules from different locations and explains server vs shared placement |
| Code organisation | All code in one script | Separates code into modules but with unclear naming | Clear folder structure with well-named, focused modules | Professional structure with folders, dependencies, and a centralised config |

##### Teacher Notes

- The most common error is forgetting the `return` statement at the end of a ModuleScript. If a student's `require()` returns `nil` or `true`, check the module's last line — it should be `return ModuleName`.
- ModuleScripts in ReplicatedStorage are accessible to both server Scripts and client LocalScripts. ModuleScripts in ServerScriptService are ONLY accessible to server Scripts. This distinction becomes critical in Session 11. For today, place all modules in ReplicatedStorage for simplicity.
- `require()` caches the returned value. If students modify the module table at runtime from one script, those changes are visible to other scripts that required the same module. This can be a feature (shared state) or a bug (unintended side effects). Mention this briefly but do not dwell on it — Session 11's client-server discussion will clarify when shared state is appropriate.
- Some students may ask about `_G` (the global table). Acknowledge it exists but discourage its use — ModuleScripts are the modern, maintainable alternative.
- If time runs short, the Extension/Advanced Activity can be simplified to just the folder organisation (without the ItemDatabase dependency chain). The core concepts — creating modules, requiring them, and GameConfig — must be covered.

---

#### SESSION 10 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 10: ModuleScripts and Code Organization**

---

##### Part 1: Understanding ModuleScripts

**Instructions:** Answer the following questions based on the lesson introduction.

**Question 1:** What are the three types of scripts in Roblox Studio? Write the name and purpose of each.

| Script Type | Where It Runs | Purpose |
|-------------|---------------|---------|
| _________________ | _________________ | _________________ |
| _________________ | _________________ | _________________ |
| _________________ | _________________ | _________________ |

**Question 2:** What happens when you call `require()` on a ModuleScript for the second time? (Choose one)

- [ ] A. It runs the entire ModuleScript again from scratch.
- [ ] B. It returns the cached (saved) result from the first time it was required.
- [ ] C. It throws an error because you can only require a module once.
- [ ] D. It creates a new copy of the module table.

**Question 3:** Where should you place a ModuleScript if you want BOTH server scripts AND client scripts to access it?

> _______________________________________________________________________________

**Question 4:** What happens if you forget the `return` statement at the end of a ModuleScript?

> _______________________________________________________________________________

---

##### Part 2: Create a StringUtils Module

**Instructions:** Create a **ModuleScript** inside **ReplicatedStorage** named `StringUtils`. Build the following utility functions.

**Step 1:** Set up the module structure.

```lua
-- ModuleScript: StringUtils (in ReplicatedStorage)
local StringUtils = {}

-- Function 1: Capitalise the first letter of a string
function StringUtils.capitalise(text)
    if #text == 0 then
        return text
    end
    return string.upper(string.sub(text, 1, 1)) .. string.sub(text, 2)
end

-- Function 2: Repeat a string a given number of times with a separator
function StringUtils.repeatText(text, times, separator)
    separator = separator or " "
    local result = ""
    for i = 1, times do
        result = result .. text
        if i < times then
            result = result .. separator
        end
    end
    return result
end

-- Function 3: Check if a string contains a substring (case-insensitive)
function StringUtils.containsIgnoreCase(text, search)
    ________________________________________________________________
    ________________________________________________________________
    ________________________________________________________________
end

-- Function 4 (YOUR CHOICE): Write your own string utility function
-- Ideas: truncate text to a max length, reverse a string, count words, etc.
function StringUtils.___________________(________________________)
    ________________________________________________________________
    ________________________________________________________________
    ________________________________________________________________
    ________________________________________________________________
end

return StringUtils
```

**Step 2:** Create a test script in ServerScriptService named `TestStringUtils`:

```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local StringUtils = require(ReplicatedStorage:WaitForChild("StringUtils"))

-- Test capitalise
print(StringUtils.capitalise("hello"))          -- Expected: "Hello"
print(StringUtils.capitalise("roblox studio"))  -- Expected: "Roblox studio"

-- Test repeatText
print(StringUtils.repeatText("Ha", 3, "-"))     -- Expected: "Ha-Ha-Ha"
print(StringUtils.repeatText("Go", 4, " "))     -- Expected: "Go Go Go Go"

-- Test containsIgnoreCase
print(StringUtils.containsIgnoreCase("Hello World", "hello"))  -- Expected: true
print(StringUtils.containsIgnoreCase("Hello World", "xyz"))    -- Expected: false

-- Test your custom function
print(StringUtils.___________________(________________________))
```

**Does your module work correctly?** [ ] Yes [ ] No — if No, what error did you get?

> _______________________________________________________________________________

---

##### Part 3: Build a GameConfig Module

**Instructions:** Create a ModuleScript in ReplicatedStorage called `GameConfig`. Design it for a game YOU would want to build.

**Step 1:** Decide on your game type (circle one or write your own):

`Obby` -- `Tycoon` -- `Fighting Game` -- `RPG` -- `Simulator` -- `Other: _______________`

**Step 2:** Write your GameConfig module with at least 10 settings:

```lua
-- ModuleScript: GameConfig (in ReplicatedStorage)
local GameConfig = {}

-- Game info
GameConfig.GameName = "______________________________"
GameConfig.GameVersion = "1.0"

-- Player settings
GameConfig.__________ = __________
GameConfig.__________ = __________
GameConfig.__________ = __________
GameConfig.__________ = __________

-- Game rules
GameConfig.__________ = __________
GameConfig.__________ = __________
GameConfig.__________ = __________

-- Economy / Scoring
GameConfig.__________ = __________
GameConfig.__________ = __________

return GameConfig
```

**Step 3:** Create a Script in ServerScriptService that uses your GameConfig:

```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local GameConfig = require(ReplicatedStorage:WaitForChild("GameConfig"))

print("Welcome to " .. GameConfig.GameName .. " v" .. GameConfig.GameVersion)
-- Use at least 3 other settings from your GameConfig in meaningful ways below:
________________________________________________________________
________________________________________________________________
________________________________________________________________
________________________________________________________________
```

---

##### Part 4: Module Dependency Challenge

**Instructions:** Study the code below and answer the questions.

```lua
-- ModuleScript: GameConfig (in ReplicatedStorage/Modules)
local GameConfig = {}
GameConfig.MaxHealth = 100
GameConfig.CurrencyName = "Gems"
GameConfig.StartingGems = 50
return GameConfig

-- ModuleScript: PlayerUtils (in ReplicatedStorage/Modules)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local GameConfig = require(ReplicatedStorage.Modules.GameConfig)

local PlayerUtils = {}

function PlayerUtils.getHealthPercentage(currentHealth)
    return math.floor((currentHealth / GameConfig.MaxHealth) * 100)
end

function PlayerUtils.formatCurrency(amount)
    return amount .. " " .. GameConfig.CurrencyName
end

return PlayerUtils
```

**Question 1:** If you change `GameConfig.MaxHealth` to `200`, what will `PlayerUtils.getHealthPercentage(100)` return?

> Answer: _______________  Explain: _____________________________________________

**Question 2:** If you change `GameConfig.CurrencyName` to `"Stars"`, what will `PlayerUtils.formatCurrency(50)` return?

> Answer: _______________

**Question 3:** The `PlayerUtils` module depends on `GameConfig`. Draw an arrow showing the dependency:

```
[ GameConfig ]          [ PlayerUtils ]
```

**Question 4:** What would happen if `GameConfig` required `PlayerUtils`, AND `PlayerUtils` required `GameConfig`?

> _______________________________________________________________________________
>
> _______________________________________________________________________________ (Hint: this is called a "circular dependency")

---

##### Reflection

1. In your own words, explain why ModuleScripts are better than copying and pasting the same code into multiple scripts.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Imagine your game has 20 different scripts. Without ModuleScripts, how would you change the player's starting health across the entire game? With a GameConfig module, how would you do it?

> Without modules: _____________________________________________________________
>
> With GameConfig: _____________________________________________________________

3. What was the most useful utility function you created today? Why?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

### Session 11: Client-Server Model & RemoteEvents

---

#### SESSION 11 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 11 of 24 |
| **Title** | Client-Server Model & RemoteEvents |
| **Unit** | Unit 3: Advanced Scripting & Data Systems |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Explain the Roblox client-server architecture, identifying which services run on the server (ServerScriptService, ServerStorage) and which run on the client (StarterPlayerScripts, StarterGui), and why this separation exists.
2. Create and use RemoteEvents to send data from a LocalScript (client) to a Script (server) using `FireServer()` and `OnServerEvent`, and from server to client using `FireClient()` and `OnClientEvent`.
3. Create and use RemoteFunctions to request data from the server using `InvokeServer()` and `OnServerInvoke`, and explain the difference between events (fire-and-forget) and functions (request-and-wait).
4. Identify at least three security vulnerabilities that arise from trusting client data and implement basic server-side validation to prevent exploitation.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 11 Worksheet (printed or displayed digitally)
- Whiteboard for drawing client-server communication diagrams
- Timer or stopwatch for timed activities
- Students' project with ModuleScripts from Session 10
- Printed or digital "Client-Server Quick Reference" handout (optional)

##### Procedure

**0-5 min: Warm-Up — "The Restaurant Analogy"**

- Say: *"Imagine a restaurant. You, the customer, sit at a table. You can see the menu. You can tell the waiter what you want. But can you walk into the kitchen and cook the food yourself?"*
- Students respond: No.
- Say: *"Why not? Because the kitchen is the restaurant's secure area. Only the chef and kitchen staff are allowed in. The customer (you) can REQUEST food through the waiter, but the kitchen decides what to actually cook and serve."*
- Draw on the board:

  ```
  [Customer/Client]  --order-->  [Waiter/RemoteEvent]  --deliver-->  [Kitchen/Server]
  [Customer/Client]  <--food--   [Waiter/RemoteEvent]  <--cook----  [Kitchen/Server]
  ```

- Say: *"This is EXACTLY how Roblox works. Your computer (the client) can request things from the Roblox server. But the server decides what actually happens in the game. Today we learn how to build the waiter — the communication system between client and server."*

**5-15 min: Introduction — Client vs Server in Roblox**

- Open Roblox Studio on the projector. Show the Explorer panel and walk through the service hierarchy:

  **Server-side (only the server can access):**
  - `ServerScriptService` — *"Scripts here run ONLY on the server. Players cannot see or modify this code. This is where you put sensitive game logic — health calculations, currency changes, anti-cheat checks."*
  - `ServerStorage` — *"Assets and data stored here are invisible to clients. Use it for items, maps, or templates the server spawns when needed."*

  **Client-side (each player's computer runs these):**
  - `StarterPlayerScripts` — *"LocalScripts here run on EACH player's computer. Every player gets their own copy. Use it for input handling, camera control, and local UI logic."*
  - `StarterGui` — *"UI elements (ScreenGuis, frames, buttons) and their LocalScripts live here."*

  **Shared (both can see):**
  - `ReplicatedStorage` — *"Both the server and client can access this. ModuleScripts, RemoteEvents, and RemoteFunctions go here because both sides need to reference them."*
  - `Workspace` — *"The 3D world. Both client and server can read it; the server has authority over changes."*

- Say: *"The golden rule of Roblox security: NEVER trust the client. The client can be hacked, modified, exploited. The server is the source of truth. The server makes all important decisions."*

- Show a concrete example: *"If a player's LocalScript says 'give me 1,000,000 gold,' should the server obey? Absolutely not. The server checks: did the player earn this gold legitimately? If not, it ignores the request."*

**15-35 min: Guided Practice — RemoteEvents**

- In the projector project, create a RemoteEvent:
  1. Right-click ReplicatedStorage > Insert Object > RemoteEvent.
  2. Name it `DamageEvent`.

- Create a LocalScript in StarterPlayerScripts called `ClientDamageTest`:

  ```lua
  -- LocalScript: ClientDamageTest (in StarterPlayerScripts)
  local ReplicatedStorage = game:GetService("ReplicatedStorage")
  local Players = game:GetService("Players")
  local UserInputService = game:GetService("UserInputService")

  local DamageEvent = ReplicatedStorage:WaitForChild("DamageEvent")
  local player = Players.LocalPlayer

  -- When the player presses "E", send a damage request to the server
  UserInputService.InputBegan:Connect(function(input, gameProcessed)
      if gameProcessed then return end

      if input.KeyCode == Enum.KeyCode.E then
          print("[CLIENT] Sending damage request to server...")
          DamageEvent:FireServer(25)  -- Request 25 damage
      end
  end)

  -- Listen for messages FROM the server
  DamageEvent.OnClientEvent:Connect(function(message, newHealth)
      print("[CLIENT] Server says: " .. message)
      print("[CLIENT] My new health: " .. newHealth)
  end)
  ```

- Create a Script in ServerScriptService called `ServerDamageHandler`:

  ```lua
  -- Script: ServerDamageHandler (in ServerScriptService)
  local ReplicatedStorage = game:GetService("ReplicatedStorage")

  local DamageEvent = ReplicatedStorage:WaitForChild("DamageEvent")

  DamageEvent.OnServerEvent:Connect(function(player, damageAmount)
      -- IMPORTANT: 'player' is automatically passed as the first argument
      -- It tells us WHICH player fired the event
      print("[SERVER] Received damage request from " .. player.Name)
      print("[SERVER] Requested damage: " .. damageAmount)

      -- SERVER-SIDE VALIDATION: Do not trust the client's damage value!
      -- Clamp the damage to a reasonable range
      if type(damageAmount) ~= "number" then
          warn("[SERVER] Invalid damage type from " .. player.Name .. "! Ignoring.")
          return
      end

      damageAmount = math.clamp(damageAmount, 0, 50)  -- Max 50 damage allowed

      -- Apply damage to the player's character
      local character = player.Character
      if character then
          local humanoid = character:FindFirstChild("Humanoid")
          if humanoid then
              humanoid.Health = humanoid.Health - damageAmount
              print("[SERVER] Applied " .. damageAmount .. " damage to " .. player.Name)
              print("[SERVER] " .. player.Name .. " health is now: " .. humanoid.Health)

              -- Send confirmation back to the client
              DamageEvent:FireClient(player, "Damage applied!", humanoid.Health)
          end
      end
  end)
  ```

- Run the game in Roblox Studio (Play mode). Press E. Show the output — both `[CLIENT]` and `[SERVER]` messages appear.

- Walk through the flow on the whiteboard:
  1. Player presses E on their keyboard (client-side input).
  2. LocalScript fires `DamageEvent:FireServer(25)`.
  3. Server receives the event in `OnServerEvent`. The `player` parameter is automatically injected by Roblox — you cannot fake it.
  4. Server validates the data, applies damage, and fires back to the client with `FireClient(player, ...)`.
  5. Client receives the response in `OnClientEvent`.

- Emphasise: *"Notice that the server does NOT blindly apply 25 damage. It CLAMPS the value to 0-50. It checks that the value is a number. It checks that the character and humanoid exist. This is server-side validation — the single most important security practice in Roblox development."*

**35-60 min: Independent Practice — RemoteFunctions and Building a Shop**

- Explain the difference between RemoteEvents and RemoteFunctions:
  - **RemoteEvent** — fire-and-forget. The sender does not wait for a response.
  - **RemoteFunction** — request-and-wait. The sender pauses until the server returns a value.

- Create a RemoteFunction in ReplicatedStorage named `BuyItemFunction`.

- Students build a basic shop system. Guide them through the worksheet:

  Server-side handler:

  ```lua
  -- Script: ShopHandler (in ServerScriptService)
  local ReplicatedStorage = game:GetService("ReplicatedStorage")

  local BuyItemFunction = ReplicatedStorage:WaitForChild("BuyItemFunction")

  -- Simple player gold storage (in a real game, use DataStoreService)
  local playerGold = {}

  game:GetService("Players").PlayerAdded:Connect(function(player)
      playerGold[player.UserId] = 500  -- Starting gold
  end)

  game:GetService("Players").PlayerRemoving:Connect(function(player)
      playerGold[player.UserId] = nil  -- Clean up
  end)

  -- Shop item prices
  local shopItems = {
      ["Speed Potion"] = 50,
      ["Health Potion"] = 30,
      ["Super Jump"] = 100,
      ["Shield"] = 75,
  }

  BuyItemFunction.OnServerInvoke = function(player, itemName)
      -- Validate the item exists
      local price = shopItems[itemName]
      if not price then
          return false, "Item does not exist: " .. tostring(itemName)
      end

      -- Validate the player has enough gold
      local gold = playerGold[player.UserId]
      if not gold then
          return false, "Player data not found"
      end

      if gold < price then
          return false, "Not enough gold. You have " .. gold .. " but need " .. price
      end

      -- Process the purchase
      playerGold[player.UserId] = gold - price
      print("[SERVER] " .. player.Name .. " bought " .. itemName .. " for " .. price .. " gold")
      print("[SERVER] " .. player.Name .. " gold remaining: " .. playerGold[player.UserId])

      -- Apply the item effect
      local character = player.Character
      if character then
          local humanoid = character:FindFirstChild("Humanoid")
          if humanoid then
              if itemName == "Speed Potion" then
                  humanoid.WalkSpeed = 32
                  task.delay(10, function()
                      if humanoid and humanoid.Parent then
                          humanoid.WalkSpeed = 16
                      end
                  end)
              elseif itemName == "Health Potion" then
                  humanoid.Health = math.min(humanoid.Health + 50, humanoid.MaxHealth)
              elseif itemName == "Super Jump" then
                  humanoid.JumpPower = 100
                  task.delay(10, function()
                      if humanoid and humanoid.Parent then
                          humanoid.JumpPower = 50
                      end
                  end)
              elseif itemName == "Shield" then
                  humanoid.MaxHealth = humanoid.MaxHealth + 50
                  humanoid.Health = humanoid.Health + 50
              end
          end
      end

      return true, "Successfully purchased " .. itemName .. "! Gold remaining: " .. playerGold[player.UserId]
  end
  ```

  Client-side:

  ```lua
  -- LocalScript: ShopClient (in StarterPlayerScripts)
  local ReplicatedStorage = game:GetService("ReplicatedStorage")
  local UserInputService = game:GetService("UserInputService")

  local BuyItemFunction = ReplicatedStorage:WaitForChild("BuyItemFunction")

  -- Key bindings for quick-buy
  local keyBindings = {
      [Enum.KeyCode.One] = "Health Potion",
      [Enum.KeyCode.Two] = "Speed Potion",
      [Enum.KeyCode.Three] = "Super Jump",
      [Enum.KeyCode.Four] = "Shield",
  }

  UserInputService.InputBegan:Connect(function(input, gameProcessed)
      if gameProcessed then return end

      local itemName = keyBindings[input.KeyCode]
      if itemName then
          print("[CLIENT] Attempting to buy: " .. itemName)
          local success, message = BuyItemFunction:InvokeServer(itemName)
          if success then
              print("[CLIENT] Purchase successful! " .. message)
          else
              print("[CLIENT] Purchase failed: " .. message)
          end
      end
  end)

  print("[CLIENT] Shop ready! Press 1-4 to buy items:")
  print("  1 = Health Potion (30g)")
  print("  2 = Speed Potion (50g)")
  print("  3 = Super Jump (100g)")
  print("  4 = Shield (75g)")
  ```

- Students type this code and test it. They should observe:
  - Pressing 1-4 triggers purchases.
  - The server validates gold and item existence.
  - The client receives success/failure messages.
  - Item effects are applied by the server.

**60-75 min: Extension/Advanced Activity — Security Exploration**

- Present three "hacker scenarios" on the board:

  **Scenario 1:** A hacker modifies their LocalScript to send `DamageEvent:FireServer(-500)` (negative damage = healing).
  - Ask: *"Would our server code catch this?"* Yes — `math.clamp(damageAmount, 0, 50)` prevents negative values.

  **Scenario 2:** A hacker sends `BuyItemFunction:InvokeServer("SUPER_WEAPON_OF_DOOM")`.
  - Ask: *"Would our server code catch this?"* Yes — the item lookup in `shopItems` would return `nil`, and the server returns "Item does not exist."

  **Scenario 3:** A hacker sends `DamageEvent:FireServer("not a number")`.
  - Ask: *"Would our server code catch this?"* Yes — the `type(damageAmount) ~= "number"` check catches it.

- Challenge students to think of ONE more hack attempt and write the server-side defence for it. Examples:
  - Spamming requests rapidly (defence: rate limiting with timestamps).
  - Sending damage to another player (defence: only allow self-damage in this system, or validate target identity).

- Advanced students implement a rate limiter:

  ```lua
  local lastRequestTime = {}

  DamageEvent.OnServerEvent:Connect(function(player, damageAmount)
      -- Rate limiting: max one request per second
      local now = tick()
      local lastTime = lastRequestTime[player.UserId] or 0
      if now - lastTime < 1 then
          warn("[SERVER] Rate limited: " .. player.Name)
          return
      end
      lastRequestTime[player.UserId] = now

      -- ... rest of validation and processing
  end)
  ```

**75-85 min: Sharing/Discussion**

- Ask: *"What is the most important rule of Roblox client-server security?"* Reinforce: **Never trust the client.**
- Discuss: *"Why does Roblox automatically pass the `player` parameter in `OnServerEvent`? Why can the client NOT fake this?"* Answer: because Roblox itself injects the player identity at the network level — the client has no way to impersonate another player.
- Ask 2 students to explain the difference between RemoteEvents and RemoteFunctions in their own words.
- Discuss when to use each: RemoteEvents for notifications where you do not need a response (damage effects, sound triggers, chat messages); RemoteFunctions for requests where you need a result back (shop purchases, data queries).

**85-90 min: Closure & Preview**

- Quick check: *"Raise your hand if you can name which service holds server-only scripts."* (ServerScriptService) *"Which service holds shared objects like RemoteEvents?"* (ReplicatedStorage)
- Preview Session 12: *"You now have tables, ModuleScripts, and RemoteEvents. Next session, we put it ALL together to build a tycoon game — earning currency, buying items, saving progress. It is project time."*
- Remind students to save.

##### Differentiation

**Support:**
- Provide a pre-built "Client-Server Communication Template" project with RemoteEvents already created and placed in ReplicatedStorage, LocalScript and Script stubs with comments indicating where code should go.
- Use colour-coded highlighting on the whiteboard: blue for client code, red for server code, green for shared objects (RemoteEvents in ReplicatedStorage). This visual coding helps students track which code runs where.
- Allow struggling students to focus on RemoteEvents only, skipping RemoteFunctions. The core concept (client sends data to server, server validates and acts) is the same for both.

**Extension:**
- Challenge advanced students to build a "Remote Event Logger" — a server script that records every RemoteEvent fired, by whom, with what data, and at what time, printing a formatted log.
- Ask them to research `FireAllClients()` and implement a server announcement system that broadcasts a message to every connected player simultaneously.
- Have them implement a "cooldown UI" on the client side that disables shop buttons for 2 seconds after a purchase, matching the server-side rate limiter.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Client-server understanding | Cannot explain the difference between client and server | Identifies client and server but confuses which services belong where | Correctly maps all services to client or server and explains why separation exists | Explains the security implications, the trust boundary, and gives real-world analogies |
| RemoteEvent usage | Cannot create or use a RemoteEvent | Creates a RemoteEvent but FireServer/OnServerEvent has errors | Successfully sends data client-to-server and server-to-client with correct syntax | Implements bidirectional communication with proper error handling and validation |
| RemoteFunction usage | Cannot explain or use RemoteFunctions | Understands the concept but cannot implement InvokeServer/OnServerInvoke | Implements a working RemoteFunction with return values | Uses RemoteFunctions for complex request-response patterns (shop, data queries) |
| Server-side validation | No validation on server-side code | Validates one aspect (e.g., type check) but misses others | Validates type, range, and existence of data before acting | Implements comprehensive validation including rate limiting and edge case handling |

##### Teacher Notes

- This session is conceptually the hardest in Unit 3. The client-server model is abstract, and many students have never thought about where code runs. The restaurant analogy helps, but be prepared to revisit it multiple times.
- When demonstrating, use `print("[CLIENT]")` and `print("[SERVER]")` prefixes consistently so students can see which side produced each output line. In Roblox Studio's Play mode, server output appears in the regular Output window, while client output may need the "Client/Server" toggle in the output panel.
- The `player` parameter in `OnServerEvent` is AUTOMATICALLY passed by Roblox. Students should NOT pass it manually from the client — `FireServer(25)` on the client becomes `function(player, 25)` on the server. This is a very common source of confusion.
- RemoteFunctions have a significant caveat: if the server's `OnServerInvoke` callback yields (takes too long), the client's `InvokeServer()` will hang. Warn students about this and encourage short, fast callbacks. For long-running operations, use RemoteEvents instead.
- Some students may ask about `BindableEvents` and `BindableFunctions`. These are for same-side communication (server-to-server or client-to-client). Acknowledge them but keep focus on RemoteEvents/RemoteFunctions today.
- If testing with multiple players is needed, use Roblox Studio's "Local Server" testing mode (Test tab > Clients and Servers). However, single-player testing is sufficient for this session.

---

#### SESSION 11 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 11: Client-Server Model & RemoteEvents**

---

##### Part 1: Client vs Server — Where Does Code Run?

**Instructions:** For each Roblox service listed below, write whether it runs on the **Client**, the **Server**, or is **Shared** (both). Then write one example of what you would put there.

| Service | Client / Server / Shared | Example of What Goes Here |
|---------|--------------------------|--------------------------|
| ServerScriptService | _________________ | _________________ |
| ServerStorage | _________________ | _________________ |
| StarterPlayerScripts | _________________ | _________________ |
| StarterGui | _________________ | _________________ |
| ReplicatedStorage | _________________ | _________________ |
| Workspace | _________________ | _________________ |

**Question:** Why is it important that the server makes all important gameplay decisions (like changing health or giving currency) instead of the client?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 2: Build a RemoteEvent Communication System

**Instructions:** Follow the steps below to create a client-server communication system.

**Step 1:** Create a RemoteEvent in ReplicatedStorage. Name it `ChatEvent`.

[ ] Done

**Step 2:** Create a LocalScript in StarterPlayerScripts called `ChatClient`:

```lua
-- LocalScript: ChatClient (in StarterPlayerScripts)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Players = game:GetService("Players")
local UserInputService = game:GetService("UserInputService")

local ChatEvent = ReplicatedStorage:WaitForChild("ChatEvent")
local player = Players.LocalPlayer

-- Pre-defined messages mapped to keys
local messages = {
    [Enum.KeyCode.One] = "Hello everyone!",
    [Enum.KeyCode.Two] = "Good game!",
    [Enum.KeyCode.Three] = "Need help!",
    [Enum.KeyCode.Four] = "Let's team up!",
}

UserInputService.InputBegan:Connect(function(input, gameProcessed)
    if gameProcessed then return end

    local message = messages[input.KeyCode]
    if message then
        print("[CLIENT] Sending message: " .. message)
        -- Fire the event to the server with the message text
        ________________________________________________
    end
end)

-- Listen for broadcast messages from the server
ChatEvent.OnClientEvent:Connect(function(senderName, message)
    print("[CHAT] " .. senderName .. ": " .. message)
end)

print("[CLIENT] Chat ready! Press 1-4 to send a message.")
```

**Fill in the blank:** What code fires the event to the server?

> _______________________________________________________________________________

**Step 3:** Create a Script in ServerScriptService called `ChatServer`:

```lua
-- Script: ChatServer (in ServerScriptService)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Players = game:GetService("Players")

local ChatEvent = ReplicatedStorage:WaitForChild("ChatEvent")

-- Allowed messages (for validation)
local allowedMessages = {
    "Hello everyone!",
    "Good game!",
    "Need help!",
    "Let's team up!",
}

local function isAllowed(message)
    for _, allowed in ipairs(allowedMessages) do
        if allowed == message then
            return true
        end
    end
    return false
end

ChatEvent.OnServerEvent:Connect(function(player, message)
    print("[SERVER] Received from " .. player.Name .. ": " .. tostring(message))

    -- VALIDATION: Only allow pre-approved messages
    if type(message) ~= "string" then
        warn("[SERVER] Invalid message type from " .. player.Name)
        return
    end

    if not isAllowed(message) then
        warn("[SERVER] Blocked unapproved message from " .. player.Name)
        return
    end

    -- Broadcast to ALL players
    for _, targetPlayer in ipairs(Players:GetPlayers()) do
        ChatEvent:FireClient(targetPlayer, player.Name, message)
    end
end)
```

**Question:** Why does the server check if the message is in the `allowedMessages` list instead of just broadcasting whatever the client sends?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 3: RemoteFunction — Data Request System

**Instructions:** Build a system where the client can request their stats from the server.

**Step 1:** Create a RemoteFunction in ReplicatedStorage. Name it `GetStatsFunction`.

**Step 2:** Server-side handler:

```lua
-- Script: StatsServer (in ServerScriptService)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Players = game:GetService("Players")

local GetStatsFunction = ReplicatedStorage:WaitForChild("GetStatsFunction")

-- Player stats storage
local playerStats = {}

Players.PlayerAdded:Connect(function(player)
    playerStats[player.UserId] = {
        Level = 1,
        Experience = 0,
        Gold = 100,
        EnemiesDefeated = 0,
        PlayTime = 0,
    }
end)

Players.PlayerRemoving:Connect(function(player)
    playerStats[player.UserId] = nil
end)

GetStatsFunction.OnServerInvoke = function(player)
    local stats = playerStats[player.UserId]
    if stats then
        -- Update play time before returning
        stats.PlayTime = math.floor(tick())
        return stats
    else
        return nil
    end
end
```

**Step 3:** Client-side requester — fill in the blanks:

```lua
-- LocalScript: StatsClient (in StarterPlayerScripts)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local UserInputService = game:GetService("UserInputService")

local GetStatsFunction = ReplicatedStorage:WaitForChild("GetStatsFunction")

UserInputService.InputBegan:Connect(function(input, gameProcessed)
    if gameProcessed then return end

    if input.KeyCode == Enum.KeyCode.P then
        print("[CLIENT] Requesting stats from server...")

        -- Use InvokeServer to get the stats table back
        local stats = ________________________________________________

        if stats then
            print("=== MY STATS ===")
            for key, value in pairs(stats) do
                print(key .. ": " .. tostring(value))
            end
        else
            print("[CLIENT] Could not retrieve stats.")
        end
    end
end)

print("[CLIENT] Press P to view your stats.")
```

**What did you write in the blank?**

> _______________________________________________________________________________

**Test your system:** Press P in play mode. Do your stats appear in the output? [ ] Yes [ ] No

---

##### Part 4: Security Challenge

**Instructions:** For each hacker scenario, write what could go wrong and how the server should defend against it.

**Scenario 1:** A hacker changes their LocalScript to send `ChatEvent:FireServer(12345)` (a number instead of a string).

- What goes wrong without validation? ________________________________________
- Server defence code already handles this because: ________________________________________

**Scenario 2:** A hacker sends `ChatEvent:FireServer("GIVE ME ADMIN POWERS")` — a message not in the allowed list.

- What goes wrong without validation? ________________________________________
- Server defence code already handles this because: ________________________________________

**Scenario 3:** A hacker sends 1000 RemoteEvent requests per second to overload the server.

- What goes wrong? ________________________________________
- Write a server-side defence (rate limiting). Fill in the blanks:

```lua
local lastMessageTime = {}

ChatEvent.OnServerEvent:Connect(function(player, message)
    local now = tick()
    local lastTime = lastMessageTime[player.UserId] or 0

    if now - lastTime < ________ then  -- Minimum seconds between messages
        warn("[SERVER] Rate limited: " .. player.Name)
        ________
    end

    lastMessageTime[player.UserId] = ________

    -- ... rest of the message handling
end)
```

---

##### Reflection

1. Explain the difference between a RemoteEvent and a RemoteFunction. When would you use each?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Why does Roblox automatically pass the `player` parameter in `OnServerEvent` instead of letting the client send it manually?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. Describe a feature in a game you would like to build that would require client-server communication. What data would the client send, and what would the server validate?

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

### Session 12: Project 2 — Tycoon Game

---

#### SESSION 12 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 12 of 24 |
| **Title** | Project 2 — Tycoon Game |
| **Unit** | Unit 3: Advanced Scripting & Data Systems |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Design and build a functional tycoon game that includes passive currency generation, a shop for purchasing game items, and visual feedback when items are bought.
2. Integrate ModuleScripts (GameConfig, ItemDatabase) with RemoteEvents to create a secure client-server tycoon architecture.
3. Implement basic data persistence using DataStoreService to save and load a player's currency and purchased items between game sessions.
4. Playtest, identify, and fix at least two bugs in their tycoon game, documenting the bug and the fix.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 12 Worksheet (printed or displayed digitally — serves as a project guide)
- Whiteboard for system architecture diagram
- Timer or stopwatch for managing project phases
- Students' projects with ModuleScripts and RemoteEvent experience from Sessions 9-11
- Teacher reference: Roblox Creator Documentation — DataStoreService page
- Note: DataStoreService requires publishing the game to Roblox (or enabling Studio API access in Game Settings > Security > Enable Studio Access to API Services)

##### Procedure

**0-5 min: Warm-Up — "What Makes a Tycoon Addictive?"**

- Ask: *"Has anyone played a tycoon game on Roblox? What keeps you playing? What makes you want to earn more and buy more?"*
- Take 4-5 responses. Write them on the board: progression, unlocking new things, numbers going up, competition with friends, visual change when you buy something.
- Say: *"Today you build your own tycoon. You will earn currency over time, buy items from a shop, see your tycoon grow, and even save your progress. This project brings together EVERYTHING from Unit 3: tables, ModuleScripts, and RemoteEvents."*

**5-15 min: Introduction — Tycoon Architecture Overview**

- Draw the system architecture on the whiteboard:

  ```
  ReplicatedStorage/
  ├── Modules/
  │   ├── TycoonConfig (ModuleScript)
  │   └── TycoonItems (ModuleScript)
  ├── BuyItemEvent (RemoteEvent)
  └── UpdateCurrencyEvent (RemoteEvent)

  ServerScriptService/
  ├── TycoonServer (Script)
  └── DataManager (Script)

  StarterPlayerScripts/
  └── TycoonClient (LocalScript)

  StarterGui/
  └── TycoonGui (ScreenGui)
      ├── CurrencyLabel (TextLabel)
      └── ShopFrame (Frame)
  ```

- Walk through each component:
  1. **TycoonConfig** — centralised settings (currency name, earn rate, item prices).
  2. **TycoonItems** — item definitions (name, price, model, position).
  3. **BuyItemEvent** — client requests a purchase; server validates and processes.
  4. **UpdateCurrencyEvent** — server sends updated currency to client for UI display.
  5. **TycoonServer** — handles currency generation, purchase logic, data saving.
  6. **TycoonClient** — handles UI updates and purchase button clicks.

- Say: *"We will build this in phases. Phase 1: Config and items. Phase 2: Server logic. Phase 3: Client and UI. Phase 4: Data saving. Let us go."*

**15-35 min: Guided Practice — Phase 1 & 2 (Config, Items, Server Logic)**

- Build TycoonConfig together on the projector:

  ```lua
  -- ModuleScript: TycoonConfig (in ReplicatedStorage/Modules)
  local TycoonConfig = {}

  TycoonConfig.CurrencyName = "Cash"
  TycoonConfig.StartingCurrency = 100
  TycoonConfig.EarnRate = 10          -- Currency earned per tick
  TycoonConfig.EarnInterval = 2       -- Seconds between each earn tick
  TycoonConfig.MaxCurrency = 1000000  -- Currency cap

  return TycoonConfig
  ```

- Build TycoonItems:

  ```lua
  -- ModuleScript: TycoonItems (in ReplicatedStorage/Modules)
  local TycoonItems = {}

  TycoonItems.Items = {
      {
          Id = "dropper1",
          Name = "Basic Dropper",
          Description = "Generates 5 Cash per cycle",
          Price = 100,
          EarnBonus = 5,
          Order = 1,
      },
      {
          Id = "dropper2",
          Name = "Advanced Dropper",
          Description = "Generates 15 Cash per cycle",
          Price = 500,
          EarnBonus = 15,
          Order = 2,
      },
      {
          Id = "upgrader1",
          Name = "Cash Multiplier",
          Description = "Doubles your earn rate",
          Price = 1000,
          EarnMultiplier = 2,
          Order = 3,
      },
      {
          Id = "decorator1",
          Name = "Gold Floor",
          Description = "A flashy gold floor for your tycoon",
          Price = 2500,
          EarnBonus = 0,
          Order = 4,
      },
      {
          Id = "dropper3",
          Name = "Elite Dropper",
          Description = "Generates 50 Cash per cycle",
          Price = 5000,
          EarnBonus = 50,
          Order = 5,
      },
  }

  function TycoonItems.getItemById(id)
      for _, item in ipairs(TycoonItems.Items) do
          if item.Id == id then
              return item
          end
      end
      return nil
  end

  function TycoonItems.getItemPrice(id)
      local item = TycoonItems.getItemById(id)
      return item and item.Price or nil
  end

  return TycoonItems
  ```

- Now build the TycoonServer script:

  ```lua
  -- Script: TycoonServer (in ServerScriptService)
  local Players = game:GetService("Players")
  local ReplicatedStorage = game:GetService("ReplicatedStorage")
  local DataStoreService = game:GetService("DataStoreService")

  local TycoonConfig = require(ReplicatedStorage:WaitForChild("Modules"):WaitForChild("TycoonConfig"))
  local TycoonItems = require(ReplicatedStorage:WaitForChild("Modules"):WaitForChild("TycoonItems"))

  local BuyItemEvent = ReplicatedStorage:WaitForChild("BuyItemEvent")
  local UpdateCurrencyEvent = ReplicatedStorage:WaitForChild("UpdateCurrencyEvent")

  -- DataStore for saving
  local TycoonDataStore = DataStoreService:GetDataStore("TycoonSaveData_v1")

  -- Player data stored in memory
  local playerData = {}

  -- Load player data
  local function loadData(player)
      local key = "Player_" .. player.UserId
      local success, data = pcall(function()
          return TycoonDataStore:GetAsync(key)
      end)

      if success and data then
          playerData[player.UserId] = data
          print("[SERVER] Loaded data for " .. player.Name)
      else
          playerData[player.UserId] = {
              Currency = TycoonConfig.StartingCurrency,
              OwnedItems = {},
              EarnMultiplier = 1,
          }
          print("[SERVER] Created new data for " .. player.Name)
      end
  end

  -- Save player data
  local function saveData(player)
      local key = "Player_" .. player.UserId
      local data = playerData[player.UserId]
      if data then
          local success, err = pcall(function()
              TycoonDataStore:SetAsync(key, data)
          end)
          if success then
              print("[SERVER] Saved data for " .. player.Name)
          else
              warn("[SERVER] Failed to save data for " .. player.Name .. ": " .. tostring(err))
          end
      end
  end

  -- Calculate total earn rate for a player
  local function getEarnRate(userId)
      local data = playerData[userId]
      if not data then return 0 end

      local baseRate = TycoonConfig.EarnRate
      local bonus = 0

      for _, itemId in ipairs(data.OwnedItems) do
          local item = TycoonItems.getItemById(itemId)
          if item and item.EarnBonus then
              bonus = bonus + item.EarnBonus
          end
      end

      return (baseRate + bonus) * (data.EarnMultiplier or 1)
  end

  -- Player joins
  Players.PlayerAdded:Connect(function(player)
      loadData(player)

      -- Send initial currency to client
      task.defer(function()
          local data = playerData[player.UserId]
          if data then
              UpdateCurrencyEvent:FireClient(player, data.Currency)
          end
      end)
  end)

  -- Player leaves
  Players.PlayerRemoving:Connect(function(player)
      saveData(player)
      playerData[player.UserId] = nil
  end)

  -- Handle buy requests
  BuyItemEvent.OnServerEvent:Connect(function(player, itemId)
      local data = playerData[player.UserId]
      if not data then return end

      -- Validate item exists
      local item = TycoonItems.getItemById(itemId)
      if not item then
          warn("[SERVER] Invalid item: " .. tostring(itemId))
          return
      end

      -- Check if already owned (for non-stackable items)
      for _, ownedId in ipairs(data.OwnedItems) do
          if ownedId == itemId then
              warn("[SERVER] " .. player.Name .. " already owns " .. item.Name)
              return
          end
      end

      -- Check currency
      if data.Currency < item.Price then
          warn("[SERVER] " .. player.Name .. " cannot afford " .. item.Name)
          return
      end

      -- Process purchase
      data.Currency = data.Currency - item.Price
      table.insert(data.OwnedItems, itemId)

      -- Apply multiplier if applicable
      if item.EarnMultiplier then
          data.EarnMultiplier = (data.EarnMultiplier or 1) * item.EarnMultiplier
      end

      print("[SERVER] " .. player.Name .. " bought " .. item.Name .. " for " .. item.Price)

      -- Send updated currency to client
      UpdateCurrencyEvent:FireClient(player, data.Currency)
  end)

  -- Currency generation loop
  task.spawn(function()
      while true do
          task.wait(TycoonConfig.EarnInterval)
          for _, player in ipairs(Players:GetPlayers()) do
              local data = playerData[player.UserId]
              if data then
                  local earned = getEarnRate(player.UserId)
                  data.Currency = math.min(data.Currency + earned, TycoonConfig.MaxCurrency)
                  UpdateCurrencyEvent:FireClient(player, data.Currency)
              end
          end
      end
  end)

  -- Auto-save every 60 seconds
  task.spawn(function()
      while true do
          task.wait(60)
          for _, player in ipairs(Players:GetPlayers()) do
              saveData(player)
          end
      end
  end)
  ```

- Students follow along, typing the code at their machines. Pause after TycoonConfig and TycoonItems to let students catch up before moving to TycoonServer.

**35-60 min: Independent Practice — Phase 3 & 4 (Client, UI, Testing)**

- Direct students to the worksheet, which guides them through building the client-side code and UI. Students work independently or in pairs.

- The client-side code students will build:

  ```lua
  -- LocalScript: TycoonClient (in StarterPlayerScripts)
  local Players = game:GetService("Players")
  local ReplicatedStorage = game:GetService("ReplicatedStorage")

  local TycoonItems = require(ReplicatedStorage:WaitForChild("Modules"):WaitForChild("TycoonItems"))
  local TycoonConfig = require(ReplicatedStorage:WaitForChild("Modules"):WaitForChild("TycoonConfig"))

  local BuyItemEvent = ReplicatedStorage:WaitForChild("BuyItemEvent")
  local UpdateCurrencyEvent = ReplicatedStorage:WaitForChild("UpdateCurrencyEvent")

  local player = Players.LocalPlayer
  local playerGui = player:WaitForChild("PlayerGui")

  -- Create the UI
  local screenGui = Instance.new("ScreenGui")
  screenGui.Name = "TycoonGui"
  screenGui.Parent = playerGui

  -- Currency display
  local currencyLabel = Instance.new("TextLabel")
  currencyLabel.Name = "CurrencyLabel"
  currencyLabel.Size = UDim2.new(0, 300, 0, 50)
  currencyLabel.Position = UDim2.new(0.5, -150, 0, 10)
  currencyLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
  currencyLabel.BackgroundTransparency = 0.5
  currencyLabel.TextColor3 = Color3.fromRGB(255, 255, 0)
  currencyLabel.TextSize = 28
  currencyLabel.Font = Enum.Font.GothamBold
  currencyLabel.Text = TycoonConfig.CurrencyName .. ": 0"
  currencyLabel.Parent = screenGui

  -- Add rounded corners
  local corner = Instance.new("UICorner")
  corner.CornerRadius = UDim.new(0, 10)
  corner.Parent = currencyLabel

  -- Shop frame
  local shopFrame = Instance.new("Frame")
  shopFrame.Name = "ShopFrame"
  shopFrame.Size = UDim2.new(0, 250, 0, 400)
  shopFrame.Position = UDim2.new(1, -260, 0.5, -200)
  shopFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
  shopFrame.BackgroundTransparency = 0.3
  shopFrame.Parent = screenGui

  local shopCorner = Instance.new("UICorner")
  shopCorner.CornerRadius = UDim.new(0, 10)
  shopCorner.Parent = shopFrame

  -- Shop title
  local shopTitle = Instance.new("TextLabel")
  shopTitle.Size = UDim2.new(1, 0, 0, 40)
  shopTitle.BackgroundTransparency = 1
  shopTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
  shopTitle.TextSize = 22
  shopTitle.Font = Enum.Font.GothamBold
  shopTitle.Text = "SHOP"
  shopTitle.Parent = shopFrame

  -- Create shop buttons
  local buttonHeight = 60
  for i, item in ipairs(TycoonItems.Items) do
      local button = Instance.new("TextButton")
      button.Name = item.Id
      button.Size = UDim2.new(0.9, 0, 0, buttonHeight - 5)
      button.Position = UDim2.new(0.05, 0, 0, 40 + (i - 1) * buttonHeight)
      button.BackgroundColor3 = Color3.fromRGB(50, 120, 50)
      button.TextColor3 = Color3.fromRGB(255, 255, 255)
      button.TextSize = 14
      button.Font = Enum.Font.Gotham
      button.Text = item.Name .. "\n" .. item.Price .. " " .. TycoonConfig.CurrencyName
      button.TextWrapped = true
      button.Parent = shopFrame

      local btnCorner = Instance.new("UICorner")
      btnCorner.CornerRadius = UDim.new(0, 8)
      btnCorner.Parent = button

      -- Buy on click
      button.MouseButton1Click:Connect(function()
          print("[CLIENT] Requesting purchase: " .. item.Name)
          BuyItemEvent:FireServer(item.Id)
      end)
  end

  -- Listen for currency updates from the server
  UpdateCurrencyEvent.OnClientEvent:Connect(function(newCurrency)
      currencyLabel.Text = TycoonConfig.CurrencyName .. ": " .. math.floor(newCurrency)
  end)

  print("[CLIENT] Tycoon UI loaded!")
  ```

- Students create the necessary RemoteEvents (`BuyItemEvent`, `UpdateCurrencyEvent`) in ReplicatedStorage and a `Modules` folder for the ModuleScripts.

- Circulate and help with:
  - Ensuring the folder structure matches the architecture diagram.
  - DataStoreService access — students must publish their game to Roblox OR enable "Enable Studio Access to API Services" in Game Settings > Security.
  - Common bugs: typos in `WaitForChild` names, forgetting to create RemoteEvents, UI elements not appearing because Parent was set before properties.

**60-75 min: Extension/Advanced Activity — Enhancements and Debugging**

- Challenge students to add at least ONE enhancement from the following list:
  1. **Visual feedback:** Change a shop button's colour to grey after purchase and update its text to "OWNED."
  2. **Sound effects:** Play a `ka-ching` sound when currency is earned and a different sound when an item is purchased.
  3. **Earn rate display:** Show the current earn rate per second in the UI.
  4. **Tycoon baseplate:** Create a physical Part in the workspace that changes colour or material when specific items are purchased.
  5. **Leaderboard:** Add `leaderstats` so currency appears on the Roblox leaderboard.

- Provide the leaderboard code as a bonus reference:

  ```lua
  -- Add to TycoonServer, inside PlayerAdded
  Players.PlayerAdded:Connect(function(player)
      loadData(player)

      -- Create leaderboard stats
      local leaderstats = Instance.new("Folder")
      leaderstats.Name = "leaderstats"
      leaderstats.Parent = player

      local cashStat = Instance.new("IntValue")
      cashStat.Name = TycoonConfig.CurrencyName
      cashStat.Value = playerData[player.UserId].Currency
      cashStat.Parent = leaderstats

      -- Update leaderboard whenever currency changes
      task.defer(function()
          local data = playerData[player.UserId]
          if data then
              UpdateCurrencyEvent:FireClient(player, data.Currency)
          end
      end)
  end)

  -- Then, wherever currency changes, also update:
  -- player:FindFirstChild("leaderstats")[TycoonConfig.CurrencyName].Value = data.Currency
  ```

**75-85 min: Sharing/Discussion — Playtesting and Presentations**

- Students playtest their tycoon games. If time allows, have 2-3 students share their screen and demonstrate their tycoon.
- Discussion questions:
  - *"What was the hardest part of building the tycoon?"*
  - *"How did you use ModuleScripts to keep your code organised?"*
  - *"What server-side validation did you include in the buy handler?"*
  - *"If you had another 90 minutes, what feature would you add?"*

**85-90 min: Closure & Preview**

- Say: *"You have just built a real, functional tycoon game with tables, modules, remote events, and data saving. That is a MASSIVE achievement. These are the same patterns used by the top games on Roblox."*
- Preview Unit 4: *"In the next four sessions, we shift focus to game WORLD design. We will learn terrain editing, TweenService for smooth animations, NPC creation with PathfindingService, and build an adventure RPG game. Get ready for things to get visual."*
- Remind students to save and optionally publish their game.

##### Differentiation

**Support:**
- Provide a "Tycoon Starter Project" template file with the folder structure, RemoteEvents, and ModuleScripts already created — struggling students only need to write the server logic and client UI.
- Break the project into smaller checkpoints: (1) Get currency to display and increase, (2) Get one shop button working, (3) Add remaining items, (4) Add data saving. Students aim for as many checkpoints as they can reach in the allotted time.
- Allow students to skip DataStoreService if it is too complex — the tycoon functions fully without persistence; data saving is an extension.

**Extension:**
- Challenge advanced students to add a "prestige" system — when the player reaches a currency threshold, they can reset and restart with a permanent earn rate multiplier.
- Ask them to implement item prerequisites (e.g., "Advanced Dropper" requires "Basic Dropper" to be owned first) with server-side validation.
- Have them create a physical tycoon base in the workspace using Parts and Models that visually appear when items are purchased, using `Clone()` from ServerStorage.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Tycoon functionality | No working tycoon | Currency displays but shop does not work | Currency earns passively; shop purchases work correctly | Full tycoon with progression, visual feedback, and multiple items |
| ModuleScript integration | No ModuleScripts used | One ModuleScript created but not fully utilised | TycoonConfig and TycoonItems both used correctly by server and client | Multiple well-structured modules with clear dependencies and no code duplication |
| Client-server architecture | All code on one side (client or server) | RemoteEvents created but validation is missing or incomplete | Proper client-server separation with server-side validation for purchases | Comprehensive validation, rate limiting, and secure data handling |
| Data persistence | No data saving attempted | DataStore code present but has errors or does not load correctly | Saves and loads currency correctly using DataStoreService | Saves currency, owned items, and multipliers; handles errors with pcall gracefully |

##### Teacher Notes

- DataStoreService is the most likely stumbling block. It requires either (a) the game to be published to Roblox, or (b) "Enable Studio Access to API Services" to be checked in Game Settings > Security. Walk students through this setup before they reach Phase 4.
- DataStoreService has rate limits: `GetAsync` and `SetAsync` are limited per key. For a classroom setting with few players, this is not an issue. But warn students that in a published game, they should use `UpdateAsync` instead of `SetAsync` and implement throttling.
- The `pcall()` wrapper around DataStore calls is essential. DataStore operations can fail (network issues, rate limits). Without `pcall()`, a failure crashes the script. With `pcall()`, you can handle the error gracefully.
- Some students may finish the core tycoon quickly. The Enhancement list in the Extension phase ensures fast workers stay engaged.
- If time is very tight, prioritise the core loop (earn currency, buy items) over DataStoreService. Data saving can be demonstrated conceptually and assigned as homework.
- Encourage students to test edge cases: What happens if you try to buy an item you already own? What if currency goes below zero? What if the player disconnects during a save?

---

#### SESSION 12 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 12: Project 2 — Tycoon Game**

---

##### Project Overview

Today you will build a complete tycoon game! Your tycoon will:
- Earn currency automatically over time
- Have a shop where players can buy items
- Save player progress between game sessions
- Use ModuleScripts for configuration and RemoteEvents for client-server communication

---

##### Phase 1: Setup (Complete the Checklist)

**Instructions:** Set up the project structure. Tick each box as you complete the step.

1. [ ] Create a **Folder** in ReplicatedStorage named `Modules`
2. [ ] Create a **ModuleScript** inside `Modules` named `TycoonConfig`
3. [ ] Create a **ModuleScript** inside `Modules` named `TycoonItems`
4. [ ] Create a **RemoteEvent** in ReplicatedStorage named `BuyItemEvent`
5. [ ] Create a **RemoteEvent** in ReplicatedStorage named `UpdateCurrencyEvent`
6. [ ] Create a **Script** in ServerScriptService named `TycoonServer`
7. [ ] Create a **LocalScript** in StarterPlayerScripts named `TycoonClient`

**Verify:** Does your Explorer panel match this structure?

```
ReplicatedStorage/
├── Modules/
│   ├── TycoonConfig
│   └── TycoonItems
├── BuyItemEvent
└── UpdateCurrencyEvent

ServerScriptService/
└── TycoonServer

StarterPlayerScripts/
└── TycoonClient
```

[ ] Yes -- proceed to Phase 2   [ ] No -- fix the structure before continuing

---

##### Phase 2: Configuration Modules

**TycoonConfig** — Customise the settings for YOUR tycoon:

```lua
local TycoonConfig = {}

TycoonConfig.CurrencyName = "_______________"   -- e.g., "Cash", "Gems", "Coins"
TycoonConfig.StartingCurrency = _______         -- How much currency players start with
TycoonConfig.EarnRate = _______                 -- Base currency earned per tick
TycoonConfig.EarnInterval = _______             -- Seconds between each earn tick
TycoonConfig.MaxCurrency = _______              -- Maximum currency cap

return TycoonConfig
```

**TycoonItems** — Design at least 5 items for your shop. Fill in the table first, then write the code:

| Item ID | Name | Description | Price | Earn Bonus |
|---------|------|-------------|-------|------------|
| _______ | _______ | _______ | _______ | _______ |
| _______ | _______ | _______ | _______ | _______ |
| _______ | _______ | _______ | _______ | _______ |
| _______ | _______ | _______ | _______ | _______ |
| _______ | _______ | _______ | _______ | _______ |

Now write the TycoonItems ModuleScript with your custom items (refer to the lesson code for the format).

[ ] TycoonConfig written and saved
[ ] TycoonItems written and saved with 5+ items and `getItemById` function

---

##### Phase 3: Server Logic

**Instructions:** Write the TycoonServer script. It must handle:

1. **Loading player data** when they join (from DataStore or create new data)
2. **Saving player data** when they leave
3. **Processing buy requests** from BuyItemEvent with validation:
   - Does the item exist?
   - Does the player already own it?
   - Does the player have enough currency?
4. **Currency generation loop** — earning currency every `EarnInterval` seconds
5. **Sending currency updates** to the client via UpdateCurrencyEvent

**Checkpoint questions (answer before coding):**

What should the server do if a player tries to buy an item that does not exist?

> _______________________________________________________________________________

What should the server do if a player tries to buy an item they already own?

> _______________________________________________________________________________

What should the server do if a player does not have enough currency?

> _______________________________________________________________________________

[ ] TycoonServer script written and saved

---

##### Phase 4: Client UI

**Instructions:** Write the TycoonClient LocalScript. It must create:

1. **Currency display** — a TextLabel showing current currency
2. **Shop panel** — buttons for each item in TycoonItems
3. **Buy functionality** — clicking a button fires `BuyItemEvent` with the item ID
4. **Currency updates** — listen for `UpdateCurrencyEvent` to update the display

[ ] TycoonClient script written and saved

---

##### Phase 5: Testing

**Instructions:** Playtest your tycoon game and complete the testing checklist.

| Test | Expected Result | Actual Result | Pass/Fail |
|------|----------------|---------------|-----------|
| Currency appears on screen | Shows starting currency amount | _____________ | [ ] P / [ ] F |
| Currency increases over time | Goes up by EarnRate every EarnInterval | _____________ | [ ] P / [ ] F |
| Click shop button | Sends buy request, currency decreases | _____________ | [ ] P / [ ] F |
| Buy item you cannot afford | Nothing happens, currency stays same | _____________ | [ ] P / [ ] F |
| Buy same item twice | Second purchase is blocked | _____________ | [ ] P / [ ] F |
| Items increase earn rate | Currency increases faster after buying | _____________ | [ ] P / [ ] F |

**Bug Log:** Document any bugs you found and how you fixed them.

| Bug Description | Cause | Fix Applied |
|----------------|-------|-------------|
| _________________________________ | _________________________________ | _________________________________ |
| _________________________________ | _________________________________ | _________________________________ |

---

##### Phase 6: Enhancements (Choose at Least One)

Pick one or more enhancements to add to your tycoon:

- [ ] **Owned indicator:** Grey out shop buttons after purchase and change text to "OWNED"
- [ ] **Earn rate display:** Show "Earning X per second" below the currency label
- [ ] **Leaderboard:** Add `leaderstats` so currency shows on the Roblox player list
- [ ] **Sound effects:** Play sounds on purchase and currency earn
- [ ] **Physical tycoon base:** Create Parts in workspace that appear when items are bought

**Which enhancement(s) did you choose?** _______________________________________________

**Describe what you added:**

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Reflection

1. Which concept from Unit 3 (tables, ModuleScripts, or RemoteEvents) was most important for building your tycoon? Why?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. What would happen if you put all the purchase logic in the LocalScript instead of the server Script? Why is that dangerous?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. If you had two more hours to work on this tycoon, what features would you add?

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

---
# Roblox Studio Intermediate: Lesson Plans & Worksheets
## Unit 4: Game World Design & Advanced Mechanics (Sessions 13-16)

### Unit Overview

Unit 4 transforms students from scripters into world-builders. Where Unit 3 focused on invisible systems — data structures, code organisation, and networking — Unit 4 makes everything visible, tangible, and immersive. Students begin by mastering Roblox's Terrain Editor, sculpting landscapes with mountains, rivers, and painted biomes, then learn to control Lighting and Atmosphere to set mood and time of day. They then discover TweenService, the engine behind every smooth animation in professional Roblox games — doors that slide open, platforms that float, UI elements that fade and pulse. The unit's third session introduces NPC creation using Humanoid characters, PathfindingService for intelligent movement, and ProximityPrompt for player-NPC dialogue. The unit culminates in Project 3: an adventure/RPG game that combines terrain, animated elements, interactive NPCs with a quest system, and DataStoreService persistence. By the end of Unit 4, students will have built a complete, polished game world that feels alive.

---

### Session 13: Terrain Editor & World Building

---

#### SESSION 13 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 13 of 24 |
| **Title** | Terrain Editor & World Building |
| **Unit** | Unit 4: Game World Design & Advanced Mechanics |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Use at least five Terrain Editor tools (Generate, Paint, Sculpt/Add, Sculpt/Subtract, Smooth, and Flatten) to create a varied game landscape with multiple biomes.
2. Apply at least four terrain materials (Grass, Sand, Rock, Water, Snow, Mud) to paint realistic environments and explain when each material is appropriate.
3. Configure Lighting properties (Ambient, Brightness, ClockTime, OutdoorAmbient) and Atmosphere effects (Density, Offset, Decay, Glare, Haze) to create a specific mood (e.g., sunrise, foggy forest, bright desert).
4. Build a complete, navigable game world with at least three distinct zones (e.g., forest, beach, mountain), appropriate lighting, and functional player spawn placement.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 13 Worksheet (printed or displayed digitally)
- Reference images of different game environments (forest, desert, snow, beach) — displayed on projector or printed
- Whiteboard for listing terrain materials and lighting properties
- Timer or stopwatch for timed activities
- Students' existing Roblox Studio project or a new baseplate place

##### Procedure

**0-5 min: Warm-Up — "Describe Your Dream Game World"**

- As students settle, display the prompt: *"Close your eyes for 10 seconds and imagine the perfect game world. When you open them, write down THREE things you see — the landscape, the sky, the colours, the mood."*
- Allow 90 seconds of writing. Invite 4-5 students to share. Write key words on the board: mountains, dark forest, bright beach, foggy swamp, sunset, snow.
- Say: *"Every one of these can be built in Roblox Studio using two tools: the Terrain Editor and the Lighting system. Today you become a world builder. By the end of this session, you will have a game world with mountains, valleys, water, painted biomes, and atmospheric effects that set the mood."*

**5-15 min: Introduction — The Terrain Editor Overview**

- Open Roblox Studio on the projector. Open a new Baseplate place. Navigate to the **Terrain** section in the Home tab (or View > Terrain Editor).
- Walk through each tool category, showing the panel:

  1. **Generate** — *"This creates an entire terrain automatically. You set the size, seed, and which biomes to include — mountains, canyons, water, plains. It is the fastest way to get a starting landscape."*
  2. **Add** — *"Paints terrain voxels into the world. Select a material, set your brush size, and click to add terrain. Like sculpting with digital clay."*
  3. **Subtract** — *"The eraser. Removes terrain to carve caves, valleys, or tunnels."*
  4. **Paint** — *"Changes the material of existing terrain WITHOUT changing its shape. Turn a grass hill into a sandy beach or a rocky cliff."*
  5. **Smooth** — *"Rounds off sharp edges and harsh transitions. Makes terrain look natural instead of blocky."*
  6. **Flatten** — *"Creates flat surfaces at a specific height. Perfect for building areas where you want a level floor."*
  7. **Sea Level** — *"Sets the water level. Any terrain below this level fills with water automatically."*
  8. **Region** — *"Select, copy, paste, move, and delete entire regions of terrain. Useful for duplicating a mountain or moving a section."*

- Demonstrate the materials palette. Show the full list: **Grass, Sand, Rock, Basalt, Snow, Ice, Mud, Ground, Sandstone, Limestone, Slate, Concrete, Brick, Cobblestone, Leafy Grass, Salt, Wood Planks, Glacier, Asphalt, Pavement, Cracked Lava**.
- Say: *"Each material has a unique texture and colour. Choosing the right materials for the right areas is what makes a game world feel believable."*

**15-35 min: Guided Practice — Building a Landscape**

- On the projector, build a landscape step by step. Students follow along:

  **Step 1: Generate a base terrain.**
  - Open the Terrain Editor > Generate tab.
  - Set Size to `256 x 128 x 256` (a medium-sized world).
  - Set Seed to any number (show that changing the seed changes the landscape).
  - Check: Mountains, Hills, Plains, Dunes. Uncheck others for now.
  - Click **Generate**. Wait for the terrain to appear.
  - Say: *"This gives us a starting point. We will now customise it."*

  **Step 2: Sculpt additions — add a mountain peak.**
  - Select the **Add** tool. Set material to **Rock**. Set brush size to about 15. Set strength to about 0.5.
  - Click and drag on an existing hill to raise it into a mountain peak.
  - Say: *"Notice how the Rock material creates a rough, stone-like texture. This looks natural for a mountain top."*

  **Step 3: Subtract — carve a valley.**
  - Select the **Subtract** tool. Set brush size to 10.
  - Click and drag through the terrain to carve a valley or path between two hills.
  - Say: *"Subtraction is how you create caves, gorges, and rivers. Carve a path and then fill it with water."*

  **Step 4: Paint — create biomes.**
  - Select the **Paint** tool. Set material to **Sand**.
  - Paint the flat areas near the edge of the map to create a beach zone.
  - Switch to **Snow**. Paint the top of the tallest mountain.
  - Switch to **Leafy Grass**. Paint a lush valley area.
  - Say: *"Painting does NOT change the shape — only the material. This is how you create distinct biomes: forest, desert, tundra, beach."*

  **Step 5: Smooth the transitions.**
  - Select the **Smooth** tool. Set brush size to 12.
  - Drag over the edges where different biomes meet — the grass-to-sand border, the rock-to-snow transition.
  - Say: *"Smoothing makes transitions look natural. Without it, your terrain has sharp, jagged edges that break the illusion."*

  **Step 6: Add water.**
  - Go to Terrain Editor > Sea Level. Set a level that fills the valley carved in Step 3.
  - Alternatively, use the **Add** tool with the **Water** material to hand-paint a lake or river.
  - Say: *"Water in Roblox is a terrain material. It fills any space below the sea level, or you can paint it manually for ponds and rivers."*

  **Step 7: Flatten — create a building area.**
  - Select the **Flatten** tool. Set the height to match the ground level of a flat area.
  - Drag to create a perfectly flat platform — suitable for placing buildings, spawn points, or NPCs later.
  - Say: *"Flat terrain is critical for gameplay areas. Players need flat ground to walk, build, and interact."*

- Students should now have a terrain with mountains, a valley, a beach, a snowy peak, and a body of water.

**35-60 min: Independent Practice — Lighting and Atmosphere**

- Now shift to Lighting. On the projector, select the **Lighting** service in the Explorer panel.

- Walk through key Lighting properties:

  ```
  Lighting Properties:
  - Ambient: Color3 — the colour of light in shadowed areas (darker = more contrast)
  - Brightness: number — overall scene brightness (default 2, range 0-10)
  - ClockTime: number — time of day (6 = sunrise, 12 = noon, 18 = sunset, 0 = midnight)
  - OutdoorAmbient: Color3 — the colour of outdoor ambient light
  - EnvironmentDiffuseScale: number — how much environment lighting affects surfaces
  - EnvironmentSpecularScale: number — shininess from environment reflections
  ```

- Demonstrate changing ClockTime:
  - Set to `6` — sunrise with warm orange light.
  - Set to `12` — bright midday.
  - Set to `18` — sunset with dramatic shadows.
  - Set to `0` — midnight, very dark.
  - Say: *"ClockTime alone transforms the entire mood of your game."*

- Now add an **Atmosphere** object. In the Explorer, right-click Lighting > Insert Object > Atmosphere.

  ```
  Atmosphere Properties:
  - Density: number — how thick the fog/atmosphere is (0 = clear, 1 = very foggy)
  - Offset: number — how far the fog starts from the camera (0 = right at camera, 1 = far away)
  - Decay: Color3 — the colour the atmosphere fades to at distance
  - Glare: number — how much the sun glares through the atmosphere
  - Haze: number — general haziness of the air
  - Color: Color3 — the tint colour of the atmosphere
  ```

- Create three mood presets on the projector:

  **Preset 1: Bright Summer Day**
  ```
  ClockTime = 14
  Brightness = 3
  Ambient = (150, 150, 150)
  Atmosphere.Density = 0.2
  Atmosphere.Offset = 0
  Atmosphere.Haze = 0
  Atmosphere.Glare = 0.5
  ```

  **Preset 2: Foggy Forest**
  ```
  ClockTime = 8
  Brightness = 1.5
  Ambient = (80, 100, 80)
  Atmosphere.Density = 0.6
  Atmosphere.Offset = 0.2
  Atmosphere.Color = (180, 200, 180)
  Atmosphere.Haze = 5
  Atmosphere.Glare = 0
  ```

  **Preset 3: Dramatic Sunset**
  ```
  ClockTime = 18.5
  Brightness = 2
  Ambient = (100, 60, 40)
  Atmosphere.Density = 0.35
  Atmosphere.Offset = 0.1
  Atmosphere.Decay = (200, 120, 80)
  Atmosphere.Glare = 1.5
  Atmosphere.Haze = 3
  ```

- Students apply these presets to their own worlds, then experiment with creating their own custom mood.

- Direct students to the worksheet. They will:
  1. Create at least three distinct terrain zones.
  2. Apply appropriate materials to each zone.
  3. Configure lighting for a specific mood.
  4. Place a SpawnLocation in a sensible starting area.
  5. Playtest to ensure the player can walk through the world.

**60-75 min: Extension/Advanced Activity — Scripted Lighting and Day/Night Cycle**

- Show students how to control Lighting with a script — creating a day/night cycle:

  ```lua
  -- Script: DayNightCycle (in ServerScriptService)
  local Lighting = game:GetService("Lighting")

  -- Configuration
  local MINUTES_PER_DAY = 4     -- One full day cycle takes 4 real minutes
  local UPDATE_INTERVAL = 0.1   -- How often to update (seconds)

  -- Calculate how much ClockTime should change per update
  -- 24 hours in a day, MINUTES_PER_DAY * 60 seconds in our cycle
  local hoursPerSecond = 24 / (MINUTES_PER_DAY * 60)
  local hoursPerUpdate = hoursPerSecond * UPDATE_INTERVAL

  -- Run the cycle
  while true do
      local currentTime = Lighting.ClockTime
      currentTime = currentTime + hoursPerUpdate

      -- Wrap around: if we pass 24, reset to 0
      if currentTime >= 24 then
          currentTime = currentTime - 24
      end

      Lighting.ClockTime = currentTime
      task.wait(UPDATE_INTERVAL)
  end
  ```

- Run the script and watch the sun move across the sky in real time.

- Challenge advanced students to add dynamic ambient changes:

  ```lua
  -- Enhanced Day/Night Cycle with ambient changes
  local Lighting = game:GetService("Lighting")

  local MINUTES_PER_DAY = 4
  local UPDATE_INTERVAL = 0.1
  local hoursPerSecond = 24 / (MINUTES_PER_DAY * 60)
  local hoursPerUpdate = hoursPerSecond * UPDATE_INTERVAL

  local function getAmbientForTime(clockTime)
      -- Night (0-5, 20-24): dark ambient
      if clockTime < 5 or clockTime > 20 then
          return Color3.fromRGB(30, 30, 50)
      -- Dawn/Dusk (5-7, 17-20): warm amber
      elseif clockTime < 7 or clockTime > 17 then
          return Color3.fromRGB(150, 100, 60)
      -- Day (7-17): bright
      else
          return Color3.fromRGB(180, 180, 180)
      end
  end

  local function getBrightnessForTime(clockTime)
      if clockTime < 5 or clockTime > 20 then
          return 0.5  -- Night
      elseif clockTime < 7 or clockTime > 17 then
          return 1.5  -- Dawn/Dusk
      else
          return 3    -- Day
      end
  end

  while true do
      local currentTime = Lighting.ClockTime
      currentTime = currentTime + hoursPerUpdate
      if currentTime >= 24 then
          currentTime = currentTime - 24
      end

      Lighting.ClockTime = currentTime
      Lighting.Ambient = getAmbientForTime(currentTime)
      Lighting.Brightness = getBrightnessForTime(currentTime)

      task.wait(UPDATE_INTERVAL)
  end
  ```

**75-85 min: Sharing/Discussion**

- Have 3-4 students share their worlds. For each, ask:
  - *"What mood were you going for?"*
  - *"Which terrain tools did you use the most?"*
  - *"What Lighting settings create the mood?"*
- Discuss: *"How does the environment affect gameplay? Think about a horror game versus a racing game — how would the terrain and lighting differ?"*
- Ask: *"If you were building a game with multiple levels (forest level, desert level, cave level), would you use one big terrain or separate places? What are the pros and cons?"*

**85-90 min: Closure & Preview**

- Ask: *"Name one Terrain tool and one Lighting property you used today."* Take three responses.
- Preview Session 14: *"Your world now looks great, but everything is static — nothing moves. Next session, we learn TweenService — the tool that makes doors slide open, platforms float, and UI elements animate smoothly. Your world is about to come alive."*
- Remind students to save.

##### Differentiation

**Support:**
- Provide a "Terrain Cheat Sheet" with screenshots of each tool's panel, the material palette with names labelled, and three lighting preset recipes.
- Pre-generate a terrain for struggling students so they can focus on painting materials and adjusting lighting rather than building from scratch.
- Pair students who struggle with spatial reasoning with a partner who can help them visualise where to add, subtract, and paint terrain.

**Extension:**
- Challenge advanced students to create a terrain entirely by hand (no Generate tool) that tells a visual story — a volcanic island, a frozen tundra, or a desert oasis.
- Ask them to add PointLights and SpotLights to specific areas (a campfire glow, a lighthouse beam) to create localised lighting effects beyond the global Lighting service.
- Have them research and add a **Bloom** post-processing effect (under Lighting) and a **SunRays** effect, tuning them for a cinematic look.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Terrain tool proficiency | Cannot use terrain tools | Uses 1-2 tools with limited results | Uses 5+ tools to create varied, natural-looking terrain | Creates professional terrain with smooth transitions, carved features, and water |
| Material application | No material painting applied | Applies 1-2 materials without considering context | Applies 4+ materials to create distinct, realistic biomes | Uses materials strategically with smooth blending and environmental storytelling |
| Lighting and atmosphere | Default lighting unchanged | Changes 1-2 properties with minimal effect | Configures ClockTime, Ambient, Brightness, and Atmosphere for a clear mood | Creates a cohesive atmosphere with multiple properties tuned, and can explain each choice |
| World design completeness | No playable world created | Basic terrain with no zones or spawn point | 3+ distinct zones with spawn point and navigable paths | Complete world with zones, paths, points of interest, lighting, and scripted day/night cycle |

##### Teacher Notes

- Terrain generation can be slow on older machines. If a student's computer struggles, reduce the generation size to `128 x 64 x 128` or skip generation entirely and use manual Add/Subtract tools.
- The Terrain Editor uses voxels (volumetric pixels), not polygons. This means terrain is resolution-limited — you cannot create very fine details. If students try to sculpt tiny features, they will get blocky results. Explain that terrain is for large-scale landscape; use Parts and Models for small-scale detail.
- Water material is special — it is semi-transparent, reflective, and has wave animations built in. If students paint Water above sea level, it may not behave as expected. Use the Sea Level tool for large bodies of water.
- Atmosphere effects can significantly impact performance on low-end hardware. If students report lag after adding Atmosphere, reduce Density and Haze values.
- Some students will spend excessive time on terrain and rush through Lighting. Set a timer: 25 minutes maximum for terrain building, then move to Lighting. The worksheet helps enforce this pacing.
- The Day/Night Cycle script in the Extension section is a great preview of how scripts can control non-character game elements — a concept that connects back to Unit 3's scripting foundations.

---

#### SESSION 13 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 13: Terrain Editor & World Building**

---

##### Part 1: Terrain Tool Identification

**Instructions:** Match each terrain tool to its correct description. Write the letter in the blank.

| Tool | | Description |
|------|---|-------------|
| 1. Generate | ____ | A. Creates a perfectly flat surface at a chosen height. |
| 2. Add | ____ | B. Automatically creates a landscape from settings and a seed number. |
| 3. Subtract | ____ | C. Rounds off sharp edges to make terrain look natural. |
| 4. Paint | ____ | D. Removes terrain to carve caves, valleys, or paths. |
| 5. Smooth | ____ | E. Paints new terrain material into the world, adding volume. |
| 6. Flatten | ____ | F. Changes the material of existing terrain without altering shape. |

**Answers:** 1.____ 2.____ 3.____ 4.____ 5.____ 6.____

---

##### Part 2: Build Your Game World

**Instructions:** Using the Terrain Editor, build a game world with at least three distinct zones. Follow the steps below and tick each box as you complete it.

**Step 1: Plan Your World**

Sketch a simple top-down map of your world in the box below. Label at least three zones.

```
+--------------------------------------------------+
|                                                  |
|                                                  |
|                                                  |
|                                                  |
|                                                  |
|               (Draw your map here)               |
|                                                  |
|                                                  |
|                                                  |
|                                                  |
|                                                  |
+--------------------------------------------------+
```

**My three zones:**
1. Zone name: ___________________ Material(s): ___________________
2. Zone name: ___________________ Material(s): ___________________
3. Zone name: ___________________ Material(s): ___________________

**Step 2: Generate or Build Base Terrain**

- [ ] Option A: Use Generate with size `256 x 128 x 256`, choose biomes that match your plan
- [ ] Option B: Build terrain manually using Add tool with Grass material as a base

**Step 3: Sculpt Your Landscape**

- [ ] Use **Add** to raise terrain for at least one hill or mountain
- [ ] Use **Subtract** to carve at least one valley, cave, or path
- [ ] Use **Smooth** on all sharp edges and transitions
- [ ] Use **Flatten** to create at least one flat building area

**Step 4: Paint Biomes**

- [ ] Paint Zone 1 with its materials: ___________________
- [ ] Paint Zone 2 with its materials: ___________________
- [ ] Paint Zone 3 with its materials: ___________________
- [ ] Smooth the material transitions between zones

**Step 5: Add Water**

- [ ] Add water using Sea Level or the Water material paint tool
- [ ] Water location: _____________________ (lake, river, ocean, pond)

**Step 6: Place a Spawn Point**

- [ ] Insert a **SpawnLocation** (Model tab > Spawn) in Zone 1
- [ ] Position it on flat ground where players will begin
- [ ] Set the SpawnLocation's **Duration** property to `0` (instant spawn)

**Checkpoint:** Press Play (F5). Can you walk through all three zones? [ ] Yes [ ] No

---

##### Part 3: Lighting and Atmosphere

**Instructions:** Configure the Lighting service to create a specific mood for your world.

**Step 1:** Choose a mood for your world (circle one or write your own):

`Bright Summer` -- `Foggy Mystery` -- `Dramatic Sunset` -- `Moonlit Night` -- `Other: ___________`

**Step 2:** Adjust Lighting properties. Write the values you used:

| Property | Your Value | Why You Chose It |
|----------|-----------|-----------------|
| ClockTime | _________ | _________________________________ |
| Brightness | _________ | _________________________________ |
| Ambient (R, G, B) | (_____, _____, _____) | _________________________________ |
| OutdoorAmbient (R, G, B) | (_____, _____, _____) | _________________________________ |

**Step 3:** Add an **Atmosphere** object (right-click Lighting > Insert Object > Atmosphere). Adjust:

| Property | Your Value | Effect |
|----------|-----------|--------|
| Density | _________ | _________________________________ |
| Offset | _________ | _________________________________ |
| Haze | _________ | _________________________________ |
| Glare | _________ | _________________________________ |
| Color (R, G, B) | (_____, _____, _____) | _________________________________ |

**Step 4:** Press Play and observe your world from the player's perspective.

Does the mood feel right? [ ] Yes [ ] Needs adjustment

If you adjusted, what did you change and why?

> _______________________________________________________________________________

---

##### Part 4: Challenge — Day/Night Cycle Script

**Instructions:** Create a Script in ServerScriptService called `DayNightCycle`. Make the sun move across the sky automatically.

```lua
-- Script: DayNightCycle (in ServerScriptService)
local Lighting = game:GetService("Lighting")

local MINUTES_PER_DAY = ________  -- How many real minutes = one full day
local UPDATE_INTERVAL = 0.1

local hoursPerSecond = 24 / (MINUTES_PER_DAY * 60)
local hoursPerUpdate = hoursPerSecond * UPDATE_INTERVAL

while true do
    local currentTime = Lighting.ClockTime
    currentTime = currentTime + hoursPerUpdate

    if currentTime >= 24 then
        currentTime = ________________________________________
    end

    Lighting.ClockTime = currentTime
    task.wait(UPDATE_INTERVAL)
end
```

**Fill in the blanks above, then test your script.**

Does the sun move across the sky? [ ] Yes [ ] No

How long does one full day take in real time? ___________ minutes

---

##### Bonus Challenge

Add dynamic ambient lighting to your Day/Night Cycle. Make the Ambient colour change based on the time of day:
- Night (0-5, 20-24): dark blue `Color3.fromRGB(30, 30, 50)`
- Dawn/Dusk (5-7, 17-20): warm amber `Color3.fromRGB(150, 100, 60)`
- Day (7-17): bright white `Color3.fromRGB(180, 180, 180)`

Write a function called `getAmbientForTime(clockTime)` that returns the correct colour and add it to your cycle script.

---

##### Reflection

1. Which terrain tool was the most useful for building your world? Why?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. How does Lighting and Atmosphere change the feeling of a game? Give a specific example (e.g., "Increasing fog density makes the forest feel mysterious because...").

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. If you were building a horror game, describe exactly what Lighting and Atmosphere settings you would use and why.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

### Session 14: TweenService & Animations

---

#### SESSION 14 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 14 of 24 |
| **Title** | TweenService & Animations |
| **Unit** | Unit 4: Game World Design & Advanced Mechanics |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Explain what TweenService is, how TweenInfo controls animation timing (Duration, EasingStyle, EasingDirection, RepeatCount, Reverses, DelayTime), and why tweens are preferred over manual frame-by-frame property changes.
2. Create tweens that animate Position, Size, Color, and Transparency of Parts and UI elements using `TweenService:Create()` and `:Play()`.
3. Apply at least three different EasingStyles (Linear, Quad, Bounce, Elastic, Sine) and explain how each creates a visually distinct motion curve.
4. Chain multiple tweens together to create complex animations such as a door opening sequence, a floating platform cycle, or a pulsing UI notification.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 14 Worksheet (printed or displayed digitally)
- Whiteboard for drawing easing curve diagrams
- Timer or stopwatch for timed activities
- Students' game world from Session 13 (or a new baseplate)
- Visual reference: Roblox easing style chart from documentation

##### Procedure

**0-5 min: Warm-Up — "Spot the Animation"**

- Play a short video clip (or screen-record) of a polished Roblox game that has visible animations: a door sliding open, a coin spinning and floating, a UI button pulsing, a platform moving up and down.
- Ask: *"How many different animations did you spot? List them."*
- Take responses. Write them on the board. Then ask: *"Do you think each of these is a separate animation file, like a video? Or is something else going on?"*
- Say: *"Almost every one of these is a TWEEN — a smooth transition from one value to another. The door goes from closed position to open position. The coin goes from full opacity to transparent. The platform goes from low to high. TweenService does the math to make the transition smooth. Today you master this tool."*

**5-15 min: Introduction — TweenService and TweenInfo**

- Open Roblox Studio on the projector. Create a Part in Workspace named `TweenDemo`. Set it to `Anchored = true`, colour it red, and position it at `(0, 5, -20)`.

- Create a Script in ServerScriptService:

  ```lua
  -- Script: TweenDemo (in ServerScriptService)
  local TweenService = game:GetService("TweenService")

  local part = workspace:WaitForChild("TweenDemo")

  -- TweenInfo defines HOW the animation behaves
  -- TweenInfo.new(Duration, EasingStyle, EasingDirection, RepeatCount, Reverses, DelayTime)
  local tweenInfo = TweenInfo.new(
      2,                              -- Duration: 2 seconds
      Enum.EasingStyle.Quad,          -- EasingStyle: starts slow, speeds up
      Enum.EasingDirection.Out,       -- EasingDirection: easing at the end
      0,                              -- RepeatCount: 0 = play once (use -1 for infinite)
      false,                          -- Reverses: false = does not reverse
      0                               -- DelayTime: 0 seconds delay before starting
  )

  -- The goal table defines WHAT changes
  local goal = {
      Position = Vector3.new(20, 5, -20)  -- Move to new position
  }

  -- Create the tween
  local tween = TweenService:Create(part, tweenInfo, goal)

  -- Play it
  tween:Play()
  ```

- Run the game. The red part slides smoothly from its original position to `(20, 5, -20)` over 2 seconds.

- Break down each TweenInfo parameter on the whiteboard:
  - **Duration** — how long the animation takes in seconds.
  - **EasingStyle** — the mathematical curve of the animation (Linear = constant speed; Quad = accelerates/decelerates; Bounce = bounces at the end; Elastic = springs past the target and back).
  - **EasingDirection** — In = easing at the start, Out = easing at the end, InOut = easing at both.
  - **RepeatCount** — how many times to repeat (0 = once, -1 = forever).
  - **Reverses** — if true, plays forward then backward (ping-pong).
  - **DelayTime** — seconds to wait before starting.

**15-35 min: Guided Practice — Tweening Multiple Properties**

- Expand the demo to show different tween targets:

  ```lua
  -- Tween 1: Move the part (Position)
  local moveTween = TweenService:Create(
      part,
      TweenInfo.new(2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut),
      {Position = Vector3.new(20, 5, -20)}
  )

  -- Tween 2: Change colour (Color)
  local colourTween = TweenService:Create(
      part,
      TweenInfo.new(1, Enum.EasingStyle.Linear),
      {Color = Color3.fromRGB(0, 100, 255)}  -- Red to blue
  )

  -- Tween 3: Change size (Size)
  local sizeTween = TweenService:Create(
      part,
      TweenInfo.new(1.5, Enum.EasingStyle.Bounce, Enum.EasingDirection.Out),
      {Size = Vector3.new(8, 8, 8)}  -- Grow larger with a bounce
  )

  -- Tween 4: Fade out (Transparency)
  local fadeTween = TweenService:Create(
      part,
      TweenInfo.new(2, Enum.EasingStyle.Quad, Enum.EasingDirection.In),
      {Transparency = 1}  -- 0 = fully visible, 1 = invisible
  )

  -- Play them one after another using the Completed event
  moveTween:Play()
  moveTween.Completed:Wait()
  print("Move complete!")

  colourTween:Play()
  colourTween.Completed:Wait()
  print("Colour change complete!")

  sizeTween:Play()
  sizeTween.Completed:Wait()
  print("Size change complete!")

  fadeTween:Play()
  fadeTween.Completed:Wait()
  print("Fade complete!")
  ```

- Run the script. Students watch the part move, change colour, grow with a bounce, and then fade out — each animation plays sequentially.

- Explain chaining: *"`Completed:Wait()` pauses the script until the tween finishes. This lets you chain tweens — play one, wait, play the next. Without this, all four tweens would play simultaneously."*

- Now demonstrate simultaneous tweens (without waiting):

  ```lua
  -- Multiple properties at once in a single tween
  local combinedTween = TweenService:Create(
      part,
      TweenInfo.new(3, Enum.EasingStyle.Elastic, Enum.EasingDirection.Out),
      {
          Position = Vector3.new(0, 15, -20),
          Size = Vector3.new(6, 6, 6),
          Color = Color3.fromRGB(255, 200, 0),
          Transparency = 0,  -- Make visible again
      }
  )

  combinedTween:Play()
  ```

- Say: *"You can tween MULTIPLE properties in one tween by adding them to the goal table. This makes them all change together, perfectly synchronised."*

- Show the EasingStyle comparison. Create multiple parts side by side, each with a different EasingStyle:

  ```lua
  local TweenService = game:GetService("TweenService")

  local styles = {
      {Name = "Linear", Style = Enum.EasingStyle.Linear},
      {Name = "Quad", Style = Enum.EasingStyle.Quad},
      {Name = "Sine", Style = Enum.EasingStyle.Sine},
      {Name = "Bounce", Style = Enum.EasingStyle.Bounce},
      {Name = "Elastic", Style = Enum.EasingStyle.Elastic},
      {Name = "Back", Style = Enum.EasingStyle.Back},
  }

  for i, data in ipairs(styles) do
      local part = Instance.new("Part")
      part.Anchored = true
      part.Size = Vector3.new(2, 2, 2)
      part.Position = Vector3.new(-15, 5, -10 - (i - 1) * 5)
      part.Color = Color3.fromRGB(math.random(100, 255), math.random(100, 255), math.random(100, 255))
      part.Name = data.Name
      part.Parent = workspace

      -- Add a label
      local billboard = Instance.new("BillboardGui")
      billboard.Size = UDim2.new(0, 100, 0, 30)
      billboard.StudsOffset = Vector3.new(0, 2, 0)
      billboard.Parent = part

      local label = Instance.new("TextLabel")
      label.Size = UDim2.new(1, 0, 1, 0)
      label.BackgroundTransparency = 1
      label.TextColor3 = Color3.new(1, 1, 1)
      label.TextStrokeTransparency = 0
      label.Text = data.Name
      label.Parent = billboard

      -- Tween each part to the right
      local tween = TweenService:Create(
          part,
          TweenInfo.new(3, data.Style, Enum.EasingDirection.Out),
          {Position = Vector3.new(15, 5, -10 - (i - 1) * 5)}
      )
      tween:Play()
  end
  ```

- Run the script. Students see six parts racing from left to right, each with a different easing curve. Linear moves at constant speed. Bounce bounces at the end. Elastic overshoots and springs back.

- Students follow along, creating their own easing comparison.

**35-60 min: Independent Practice — Building Animated Game Elements**

- Direct students to the worksheet. They build three animated elements:

  **Element 1: Animated Door**

  ```lua
  -- Script: AnimatedDoor (inside a Part named "Door" in Workspace)
  local TweenService = game:GetService("TweenService")
  local door = script.Parent

  -- Door should be Anchored = true
  local closedPosition = door.Position
  local openPosition = closedPosition + Vector3.new(0, door.Size.Y, 0)  -- Slides up

  local openInfo = TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
  local closeInfo = TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.In)

  local openTween = TweenService:Create(door, openInfo, {Position = openPosition})
  local closeTween = TweenService:Create(door, closeInfo, {Position = closedPosition})

  local isOpen = false

  -- Add a ProximityPrompt to the door
  local prompt = Instance.new("ProximityPrompt")
  prompt.ActionText = "Open Door"
  prompt.ObjectText = "Door"
  prompt.MaxActivationDistance = 10
  prompt.Parent = door

  prompt.Triggered:Connect(function(player)
      if isOpen then
          closeTween:Play()
          prompt.ActionText = "Open Door"
          isOpen = false
      else
          openTween:Play()
          prompt.ActionText = "Close Door"
          isOpen = true
      end
  end)
  ```

  **Element 2: Floating Platform**

  ```lua
  -- Script: FloatingPlatform (inside an Anchored Part named "Platform")
  local TweenService = game:GetService("TweenService")
  local platform = script.Parent

  local startPosition = platform.Position
  local endPosition = startPosition + Vector3.new(0, 10, 0)  -- Float up 10 studs

  local tweenInfo = TweenInfo.new(
      3,                              -- 3 seconds per direction
      Enum.EasingStyle.Sine,          -- Smooth sine wave motion
      Enum.EasingDirection.InOut,     -- Smooth start and end
      -1,                             -- Repeat forever
      true,                           -- Reverse (go up then come back down)
      0                               -- No delay
  )

  local tween = TweenService:Create(platform, tweenInfo, {Position = endPosition})
  tween:Play()
  ```

  **Element 3: Pulsing Collectible**

  ```lua
  -- Script: PulsingCollectible (inside an Anchored Part)
  local TweenService = game:GetService("TweenService")
  local collectible = script.Parent

  -- Pulse size
  local originalSize = collectible.Size
  local pulseSize = originalSize * 1.3

  local pulseInfo = TweenInfo.new(
      0.8,
      Enum.EasingStyle.Sine,
      Enum.EasingDirection.InOut,
      -1,    -- Infinite repeat
      true,  -- Reverse
      0
  )

  local pulseTween = TweenService:Create(collectible, pulseInfo, {Size = pulseSize})
  pulseTween:Play()

  -- Spin rotation
  local spinInfo = TweenInfo.new(
      4,
      Enum.EasingStyle.Linear,
      Enum.EasingDirection.In,
      -1,    -- Infinite repeat
      false, -- No reverse (continuous spin)
      0
  )

  local spinTween = TweenService:Create(
      collectible,
      spinInfo,
      {Orientation = collectible.Orientation + Vector3.new(0, 360, 0)}
  )
  spinTween:Play()

  -- Collect on touch
  collectible.Touched:Connect(function(hit)
      local humanoid = hit.Parent:FindFirstChild("Humanoid")
      if humanoid then
          pulseTween:Cancel()
          spinTween:Cancel()

          -- Fade and shrink on collect
          local collectTween = TweenService:Create(
              collectible,
              TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In),
              {Size = Vector3.new(0, 0, 0), Transparency = 1}
          )
          collectTween:Play()
          collectTween.Completed:Wait()
          collectible:Destroy()
      end
  end)
  ```

- Students add these elements to their game world from Session 13. Circulate and help with positioning, ensuring parts are Anchored, and debugging tween targets.

**60-75 min: Extension/Advanced Activity — UI Tweens**

- Show how TweenService works with GUI elements:

  ```lua
  -- LocalScript: UIAnimations (in StarterGui inside a ScreenGui)
  local TweenService = game:GetService("TweenService")
  local Players = game:GetService("Players")

  local player = Players.LocalPlayer
  local playerGui = player:WaitForChild("PlayerGui")

  -- Create a notification frame
  local screenGui = Instance.new("ScreenGui")
  screenGui.Name = "NotificationGui"
  screenGui.Parent = playerGui

  local notifFrame = Instance.new("Frame")
  notifFrame.Name = "Notification"
  notifFrame.Size = UDim2.new(0, 300, 0, 60)
  notifFrame.Position = UDim2.new(0.5, -150, 0, -70)  -- Start off-screen (above)
  notifFrame.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
  notifFrame.BackgroundTransparency = 0.2
  notifFrame.Parent = screenGui

  local corner = Instance.new("UICorner")
  corner.CornerRadius = UDim.new(0, 12)
  corner.Parent = notifFrame

  local notifLabel = Instance.new("TextLabel")
  notifLabel.Size = UDim2.new(1, 0, 1, 0)
  notifLabel.BackgroundTransparency = 1
  notifLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
  notifLabel.TextSize = 20
  notifLabel.Font = Enum.Font.GothamBold
  notifLabel.Text = "Achievement Unlocked!"
  notifLabel.Parent = notifFrame

  -- Function to show notification
  local function showNotification(text)
      notifLabel.Text = text
      notifFrame.Position = UDim2.new(0.5, -150, 0, -70)  -- Reset off-screen

      -- Slide in
      local slideIn = TweenService:Create(
          notifFrame,
          TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.Out),
          {Position = UDim2.new(0.5, -150, 0, 20)}
      )

      -- Slide out (after delay)
      local slideOut = TweenService:Create(
          notifFrame,
          TweenInfo.new(0.5, Enum.EasingStyle.Quad, Enum.EasingDirection.In),
          {Position = UDim2.new(0.5, -150, 0, -70)}
      )

      slideIn:Play()
      slideIn.Completed:Wait()
      task.wait(2)  -- Show for 2 seconds
      slideOut:Play()
  end

  -- Test notifications
  task.wait(2)
  showNotification("Welcome to the game!")
  task.wait(4)
  showNotification("Achievement: First Steps!")
  task.wait(4)
  showNotification("You found a secret area!")
  ```

- Advanced students create their own animated UI elements: health bar that smoothly decreases, score counter that bounces when updated, or a title screen with fade-in effects.

**75-85 min: Sharing/Discussion**

- Ask 3 students to demonstrate their animated elements. For each:
  - *"Which EasingStyle did you use and why?"*
  - *"Did you chain tweens or play them simultaneously?"*
- Discuss: *"When would you use `Reverses = true` versus creating two separate tweens? What are the pros and cons?"*
- Ask: *"Why are tweens better than manually changing position in a loop? Think about performance and code readability."* Guide to: tweens are optimised by the engine, run on a separate thread, handle interpolation math automatically, and the code is much cleaner.

**85-90 min: Closure & Preview**

- Ask: *"Name one thing you can tween and one EasingStyle you used."* Take three responses.
- Preview Session 15: *"Your world has terrain, lighting, and animated objects. But it is still empty of CHARACTERS. Next session, we build NPCs — non-player characters that walk around, patrol, chase the player, and talk. We will use PathfindingService to give them intelligence."*
- Remind students to save.

##### Differentiation

**Support:**
- Provide a "TweenService Reference Card" with the TweenInfo parameter order, common EasingStyles with visual descriptions (Linear = steady, Bounce = bouncy, Elastic = springy), and a template for creating a basic tween.
- Pre-create the Parts (Door, Platform, Collectible) in the workspace so struggling students only need to write the tween scripts, not build the objects.
- Start struggling students with a single-property tween (just Position) before adding colour, size, or multi-property goals.

**Extension:**
- Challenge advanced students to create a "tween playground" with buttons that trigger different animations — a showcase of every EasingStyle and Direction combination.
- Ask them to build a moving obstacle course with multiple floating platforms at different speeds and heights, requiring timing to navigate.
- Have them create a UI animation library ModuleScript with reusable functions like `slideIn()`, `fadeOut()`, `pulseButton()` that can be called from any LocalScript.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| TweenInfo understanding | Cannot explain TweenInfo parameters | Knows Duration but confused by EasingStyle and RepeatCount | Correctly configures all six TweenInfo parameters for desired effect | Chooses EasingStyles purposefully and explains why each fits the animation |
| Property tweening | Cannot create a working tween | Tweens one property (e.g., Position) with default settings | Tweens 3+ property types (Position, Color, Size, Transparency) correctly | Tweens multiple properties simultaneously and creates combined visual effects |
| Tween chaining | Cannot chain tweens | Attempts chaining but tweens overlap or timing is wrong | Chains 2+ tweens sequentially using Completed:Wait() | Creates complex multi-step animations with precise timing and smooth flow |
| Practical application | No animated game elements created | Creates one basic animated element | Creates 3+ animated elements integrated into the game world | Creates polished, purposeful animations that enhance gameplay (doors, platforms, UI) |

##### Teacher Notes

- The most common error: students forget to set `Anchored = true` on Parts they want to tween. Un-anchored parts are subject to physics and will fall. TweenService works on both anchored and un-anchored parts, but un-anchored results are unpredictable.
- TweenService cannot tween every property. It works on numeric values (Position, Size, Transparency, Rotation) and Color3 values. It does NOT work on boolean properties, string properties, or Instance references. If a student tries to tween `CanCollide` from true to false, it will not work — they need to set it directly.
- The `Orientation` property can be tricky. Tweening Orientation by adding 360 degrees does NOT create a full rotation if the engine finds a shorter path. For continuous spinning, use `CFrame` tweens instead of `Orientation`. The worksheet's spin example uses Orientation for simplicity; advanced students should be shown the CFrame approach.
- When tweening UI elements, the Position uses `UDim2` values, not `Vector3`. Students who have been tweening Parts may try to use `Vector3` for GUI positions — this will error.
- Performance note: each active tween consumes a small amount of CPU. Having 100+ simultaneous tweens can cause lag. For the classroom, this is unlikely to be an issue, but mention it for students building large worlds.
- ProximityPrompt (used in the door example) is a relatively new Roblox feature that creates an interactive prompt when a player is near an object. It replaces the older ClickDetector for many use cases. If students have not seen it before, take 2 minutes to explain its properties.

---

#### SESSION 14 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 14: TweenService & Animations**

---

##### Part 1: TweenInfo Parameters

**Instructions:** Fill in the table below with the correct description for each TweenInfo parameter.

| Parameter | Type | Description | Example Value |
|-----------|------|-------------|---------------|
| Duration | number | _________________________________ | 2 |
| EasingStyle | Enum | _________________________________ | Enum.EasingStyle.Bounce |
| EasingDirection | Enum | _________________________________ | Enum.EasingDirection.Out |
| RepeatCount | number | _________________________________ | -1 |
| Reverses | boolean | _________________________________ | true |
| DelayTime | number | _________________________________ | 0.5 |

**Question:** What does `RepeatCount = -1` do?

> _______________________________________________________________________________

**Question:** If `Reverses = true` and `Duration = 2`, how long does one complete forward-and-back cycle take?

> _______________________________________________________________________________

---

##### Part 2: EasingStyle Prediction

**Instructions:** For each EasingStyle, predict how the animation will look, then test it in Roblox Studio.

Create a Part named `StyleTest` (Anchored, Size 4x4x4). Write a script that moves it from `(0, 5, -20)` to `(30, 5, -20)` with each style. Change the EasingStyle and run each time.

| EasingStyle | Your Prediction (how will it move?) | Actual Result |
|-------------|-------------------------------------|---------------|
| Linear | _________________________________ | _________________________________ |
| Quad | _________________________________ | _________________________________ |
| Sine | _________________________________ | _________________________________ |
| Bounce | _________________________________ | _________________________________ |
| Elastic | _________________________________ | _________________________________ |
| Back | _________________________________ | _________________________________ |

**Which EasingStyle is your favourite? Why?**

> _______________________________________________________________________________

---

##### Part 3: Build Animated Game Elements

**Instructions:** Build each animated element below and add it to your game world.

**Element 1: Sliding Door**

1. [ ] Create a Part in Workspace named `Door` (Size: 6x10x1, Anchored: true, BrickColor: your choice)
2. [ ] Add a Script inside the Door
3. [ ] Write code that:
   - Stores the closed position
   - Calculates an open position (slide up by the door's height)
   - Creates open and close tweens
   - Adds a ProximityPrompt
   - Toggles open/close when the prompt is triggered

```lua
local TweenService = game:GetService("TweenService")
local door = script.Parent

local closedPos = door.Position
local openPos = closedPos + Vector3.new(0, __________, 0)  -- What value here?

local openTween = TweenService:Create(
    door,
    TweenInfo.new(1, Enum.EasingStyle.__________, Enum.EasingDirection.__________),
    {Position = openPos}
)

local closeTween = TweenService:Create(
    door,
    TweenInfo.new(1, Enum.EasingStyle.__________, Enum.EasingDirection.__________),
    {Position = closedPos}
)

local isOpen = false

local prompt = Instance.new("ProximityPrompt")
prompt.ActionText = "Open"
prompt.MaxActivationDistance = 10
prompt.Parent = door

prompt.Triggered:Connect(function(player)
    if isOpen then
        __________________________________________
        prompt.ActionText = "Open"
        isOpen = false
    else
        __________________________________________
        prompt.ActionText = "Close"
        isOpen = true
    end
end)
```

**Test:** Walk up to the door and press E. Does it open and close? [ ] Yes [ ] No

---

**Element 2: Floating Platform**

1. [ ] Create a Part named `FloatPlatform` (Size: 12x2x12, Anchored: true, Material: Neon or SmoothPlastic)
2. [ ] Add a Script inside it
3. [ ] Make it float up and down continuously using a single tween with `Reverses = true` and `RepeatCount = -1`

```lua
local TweenService = game:GetService("TweenService")
local platform = script.Parent

local startPos = platform.Position
local endPos = startPos + Vector3.new(0, ______, 0)  -- How many studs up?

local tweenInfo = TweenInfo.new(
    ______,                           -- Duration
    Enum.EasingStyle.__________,      -- Which style for smooth floating?
    Enum.EasingDirection.InOut,
    ______,                           -- RepeatCount (infinite)
    ______,                           -- Reverses?
    0
)

local tween = TweenService:Create(platform, tweenInfo, {Position = endPos})
tween:Play()
```

**Test:** Does the platform float up and down smoothly forever? [ ] Yes [ ] No

**Can you stand on it and ride it?** [ ] Yes [ ] No

---

**Element 3: Colour-Changing Part**

1. [ ] Create a Part named `ColourChanger` (Size: 4x4x4, Anchored: true)
2. [ ] Write a script that cycles through at least 4 colours using chained tweens

```lua
local TweenService = game:GetService("TweenService")
local part = script.Parent

local colours = {
    Color3.fromRGB(255, 0, 0),      -- Red
    Color3.fromRGB(0, 255, 0),      -- Green
    Color3.fromRGB(0, 100, 255),    -- Blue
    Color3.fromRGB(255, 255, 0),    -- Yellow
}

local tweenInfo = TweenInfo.new(1.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut)

while true do
    for _, colour in ipairs(colours) do
        local tween = TweenService:Create(part, tweenInfo, {Color = colour})
        tween:Play()
        ________________________________________________  -- Wait for it to finish
    end
end
```

**Fill in the blank to make each colour change wait before the next one starts.**

**Test:** Does the part smoothly cycle through all colours? [ ] Yes [ ] No

---

##### Part 4: Challenge — Multi-Step Animation Sequence

Create a "treasure chest" animation:

1. Create a Part for the chest (or use two Parts: base + lid)
2. When a player interacts via ProximityPrompt:
   - The lid rotates open (tween Orientation or CFrame)
   - A "sparkle" Part tweens upward from inside the chest
   - The sparkle fades out (Transparency tweens to 1)
   - A message prints: "You found treasure!"
3. After 3 seconds, the lid closes back

Write your code below or in Roblox Studio:

```lua
-- Your treasure chest code here:
________________________________________________________________
________________________________________________________________
________________________________________________________________
________________________________________________________________
________________________________________________________________
________________________________________________________________
________________________________________________________________
________________________________________________________________
________________________________________________________________
________________________________________________________________
```

---

##### Bonus Challenge

Create a UI notification system using TweenService:
1. A notification frame slides down from the top of the screen
2. It stays visible for 2 seconds
3. It slides back up off-screen
4. Wrap this in a reusable function `showNotification(text)` that can be called multiple times

---

##### Reflection

1. What is the advantage of using TweenService over changing a part's position manually in a loop (e.g., `while true do part.Position = part.Position + Vector3.new(0.1, 0, 0); task.wait() end`)?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Which animated element was hardest to build? What made it challenging?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. Describe an animation you have seen in a game you play that you could now recreate using TweenService. What properties would you tween, and which EasingStyle would you use?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

### Session 15: NPC Creation & Basic AI

---

#### SESSION 15 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 15 of 24 |
| **Title** | NPC Creation & Basic AI |
| **Unit** | Unit 4: Game World Design & Advanced Mechanics |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Create an NPC character using a Model with a Humanoid, HumanoidRootPart, and body parts, and explain the role of each component in making the NPC functional.
2. Use PathfindingService to calculate and execute a path between two points, enabling the NPC to navigate around obstacles intelligently.
3. Implement at least two NPC behaviour states (idle, patrol, chase) with logic to transition between states based on player proximity.
4. Create an interactive NPC dialogue system using ProximityPrompt that displays conversation text and responds to player input.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 15 Worksheet (printed or displayed digitally)
- Whiteboard for drawing state diagrams
- Timer or stopwatch for timed activities
- Students' game world from Sessions 13-14
- Pre-built NPC model (optional — teacher can provide a simple R6 or R15 rig, or students build from Parts)

##### Procedure

**0-5 min: Warm-Up — "What Makes an NPC Feel Alive?"**

- Ask: *"Think of the best NPC you have ever encountered in a game. What made them feel like a real character instead of a cardboard cutout?"*
- Take 4-5 responses. Write on the board: they move on their own, they react to you, they have dialogue, they patrol an area, they chase you, they have idle animations.
- Say: *"Today we build NPCs that do ALL of these things. We start by creating the character model, then give it a brain using PathfindingService and state machines. By the end, your NPCs will patrol, chase the player, and talk."*

**5-15 min: Introduction — Anatomy of an NPC**

- Open Roblox Studio on the projector. Explain the components of an NPC:

  - **Model** — the container that holds all NPC parts together.
  - **Humanoid** — the component that gives the model health, walk speed, and the ability to move using `:MoveTo()`. Without a Humanoid, the model is just static parts.
  - **HumanoidRootPart** — the invisible anchor part that the Humanoid uses for movement. Must be named exactly `HumanoidRootPart` and be the PrimaryPart of the Model.
  - **Body Parts** — Head, Torso, Left Arm, Right Arm, Left Leg, Right Leg (R6 format) or more detailed parts (R15 format).

- Show two approaches to creating an NPC:

  **Approach 1: Use a Rig (recommended)**
  - Go to the **Avatar** tab (or Plugins > Rig Builder in some versions).
  - Click **Rig Builder** > choose **R6** or **R15** > click **Generate**.
  - A complete character rig appears in the workspace with all parts, joints, and a Humanoid.
  - Rename the Model to `GuardNPC`.

  **Approach 2: Build from Parts (for understanding)**
  - Create a Model, add a Part named `HumanoidRootPart` (Anchored false, CanCollide false, Transparency 1).
  - Add body parts (Head, Torso, etc.) as children of the Model.
  - Add a `Humanoid` object inside the Model.
  - Set the Model's `PrimaryPart` to `HumanoidRootPart`.
  - Say: *"Approach 2 gives you full control but is tedious. In practice, always use a Rig and then customise it."*

- After generating the rig, show how to customise:
  - Change body part colours in the Inspector.
  - Add a shirt/pants (Insert Object > Shirt/Pants, set the asset ID).
  - Add an accessory (hat, weapon) by inserting it as a child.

**15-35 min: Guided Practice — PathfindingService and Movement**

- Create a Script inside the NPC Model:

  ```lua
  -- Script: NPCBrain (inside the GuardNPC Model)
  local PathfindingService = game:GetService("PathfindingService")
  local Players = game:GetService("Players")

  local npc = script.Parent
  local humanoid = npc:WaitForChild("Humanoid")
  local rootPart = npc:WaitForChild("HumanoidRootPart")

  -- Basic movement: MoveTo
  -- humanoid:MoveTo(Vector3.new(20, 0, 20))  -- Move to a world position

  -- PathfindingService: intelligent movement around obstacles
  local function walkTo(targetPosition)
      local path = PathfindingService:CreatePath({
          AgentRadius = 2,       -- NPC width (how much space it needs)
          AgentHeight = 5,       -- NPC height
          AgentCanJump = true,   -- Can the NPC jump over obstacles?
          AgentCanClimb = false, -- Can the NPC climb?
      })

      -- Compute the path from current position to target
      path:ComputeAsync(rootPart.Position, targetPosition)

      if path.Status == Enum.PathStatus.Success then
          -- Get the waypoints
          local waypoints = path:GetWaypoints()

          -- Walk through each waypoint
          for _, waypoint in ipairs(waypoints) do
              -- If this waypoint requires jumping, jump!
              if waypoint.Action == Enum.PathWaypointAction.Jump then
                  humanoid.Jump = true
              end

              -- Move to the waypoint
              humanoid:MoveTo(waypoint.Position)

              -- Wait until we reach the waypoint (or timeout)
              local reached = humanoid.MoveToFinished:Wait()
              if not reached then
                  -- We got stuck — break out
                  warn("[NPC] Failed to reach waypoint")
                  break
              end
          end
      else
          warn("[NPC] Could not compute path to target")
      end
  end

  -- Test: walk to a specific position
  task.wait(2)  -- Wait for the game to load
  walkTo(Vector3.new(30, 0, 30))
  print("[NPC] Arrived at destination!")
  ```

- Run the game. The NPC walks to `(30, 0, 30)`, navigating around any obstacles in the way.

- Explain PathfindingService: *"PathfindingService does the hard work of finding a path. You give it a start and end position. It returns a series of waypoints — points the NPC should walk through in order. If there is an obstacle, it routes around it. If it needs to jump, it tells you."*

- Now introduce patrol behaviour — the NPC walks between multiple waypoints:

  ```lua
  -- Patrol: walk between a list of positions in a loop
  local patrolPoints = {
      Vector3.new(20, 0, 20),
      Vector3.new(20, 0, -20),
      Vector3.new(-20, 0, -20),
      Vector3.new(-20, 0, 20),
  }

  local function patrol()
      while true do
          for _, point in ipairs(patrolPoints) do
              walkTo(point)
              task.wait(1)  -- Pause at each point for 1 second
          end
      end
  end

  patrol()
  ```

- Run the game. The NPC patrols in a square pattern, pausing at each corner.

**35-60 min: Independent Practice — NPC Behaviour States**

- Draw a state diagram on the whiteboard:

  ```
  [IDLE] --player near--> [CHASE] --player far--> [PATROL]
    ^                                                 |
    |                                                 |
    +-----------reached patrol point-------------------+
  ```

- Guide students through implementing a state machine:

  ```lua
  -- Script: NPCBrain (in GuardNPC Model) — Full State Machine
  local PathfindingService = game:GetService("PathfindingService")
  local Players = game:GetService("Players")

  local npc = script.Parent
  local humanoid = npc:WaitForChild("Humanoid")
  local rootPart = npc:WaitForChild("HumanoidRootPart")

  -- Configuration
  local CHASE_RANGE = 30       -- Start chasing if player is within 30 studs
  local LOSE_RANGE = 50        -- Stop chasing if player is beyond 50 studs
  local PATROL_WAIT = 2        -- Seconds to wait at each patrol point
  local NPC_WALK_SPEED = 14    -- Patrol speed
  local NPC_CHASE_SPEED = 22   -- Chase speed

  -- Patrol points (customise for your world)
  local patrolPoints = {
      Vector3.new(20, 0, 20),
      Vector3.new(20, 0, -20),
      Vector3.new(-20, 0, -20),
      Vector3.new(-20, 0, 20),
  }

  local currentState = "IDLE"
  local currentPatrolIndex = 1

  -- Utility: find the nearest player
  local function getNearestPlayer()
      local nearestPlayer = nil
      local nearestDistance = math.huge

      for _, player in ipairs(Players:GetPlayers()) do
          local character = player.Character
          if character then
              local playerRoot = character:FindFirstChild("HumanoidRootPart")
              if playerRoot then
                  local distance = (rootPart.Position - playerRoot.Position).Magnitude
                  if distance < nearestDistance then
                      nearestDistance = distance
                      nearestPlayer = player
                  end
              end
          end
      end

      return nearestPlayer, nearestDistance
  end

  -- Utility: walk to using pathfinding
  local function walkTo(targetPosition)
      local path = PathfindingService:CreatePath({
          AgentRadius = 2,
          AgentHeight = 5,
          AgentCanJump = true,
      })

      path:ComputeAsync(rootPart.Position, targetPosition)

      if path.Status == Enum.PathStatus.Success then
          local waypoints = path:GetWaypoints()
          for _, waypoint in ipairs(waypoints) do
              -- Check if we should switch states during movement
              local _, dist = getNearestPlayer()
              if currentState == "PATROL" and dist <= CHASE_RANGE then
                  currentState = "CHASE"
                  return  -- Break out to switch states
              end
              if currentState == "CHASE" and dist > LOSE_RANGE then
                  currentState = "PATROL"
                  return
              end

              if waypoint.Action == Enum.PathWaypointAction.Jump then
                  humanoid.Jump = true
              end
              humanoid:MoveTo(waypoint.Position)
              humanoid.MoveToFinished:Wait()
          end
      end
  end

  -- Main behaviour loop
  task.wait(2)  -- Wait for game to load

  while true do
      local nearestPlayer, distance = getNearestPlayer()

      if currentState == "IDLE" then
          -- Idle: wait, then start patrolling
          humanoid.WalkSpeed = 0
          task.wait(2)
          currentState = "PATROL"

      elseif currentState == "PATROL" then
          -- Patrol: walk between patrol points
          humanoid.WalkSpeed = NPC_WALK_SPEED
          local target = patrolPoints[currentPatrolIndex]
          walkTo(target)

          -- Only advance to next point if we are still in PATROL state
          if currentState == "PATROL" then
              task.wait(PATROL_WAIT)
              currentPatrolIndex = currentPatrolIndex + 1
              if currentPatrolIndex > #patrolPoints then
                  currentPatrolIndex = 1
              end
          end

      elseif currentState == "CHASE" then
          -- Chase: pursue the nearest player
          humanoid.WalkSpeed = NPC_CHASE_SPEED
          if nearestPlayer and nearestPlayer.Character then
              local playerRoot = nearestPlayer.Character:FindFirstChild("HumanoidRootPart")
              if playerRoot then
                  humanoid:MoveTo(playerRoot.Position)
                  task.wait(0.2)  -- Update chase direction frequently
              end
          end

          -- Check if player escaped
          if distance > LOSE_RANGE then
              print("[NPC] Lost the player, returning to patrol")
              currentState = "PATROL"
          end
      end

      task.wait(0.1)
  end
  ```

- Students implement this state machine in their NPC. They should test:
  - NPC patrols on its own when the player is far away.
  - NPC starts chasing when the player gets within 30 studs.
  - NPC returns to patrol when the player escapes beyond 50 studs.

**60-75 min: Extension/Advanced Activity — Dialogue System with ProximityPrompt**

- Create a friendly NPC (separate from the guard) with a dialogue system:

  ```lua
  -- Script: NPCDialogue (inside a friendly NPC Model)
  local npc = script.Parent
  local rootPart = npc:WaitForChild("HumanoidRootPart")

  -- Create a ProximityPrompt
  local prompt = Instance.new("ProximityPrompt")
  prompt.ActionText = "Talk"
  prompt.ObjectText = npc.Name
  prompt.MaxActivationDistance = 10
  prompt.HoldDuration = 0
  prompt.Parent = rootPart

  -- Create a BillboardGui for the dialogue text
  local billboardGui = Instance.new("BillboardGui")
  billboardGui.Name = "DialogueBubble"
  billboardGui.Size = UDim2.new(0, 250, 0, 80)
  billboardGui.StudsOffset = Vector3.new(0, 4, 0)
  billboardGui.Active = false
  billboardGui.Parent = rootPart

  local background = Instance.new("Frame")
  background.Size = UDim2.new(1, 0, 1, 0)
  background.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
  background.BackgroundTransparency = 0.2
  background.Parent = billboardGui

  local corner = Instance.new("UICorner")
  corner.CornerRadius = UDim.new(0, 8)
  corner.Parent = background

  local dialogueLabel = Instance.new("TextLabel")
  dialogueLabel.Size = UDim2.new(1, -10, 1, -10)
  dialogueLabel.Position = UDim2.new(0, 5, 0, 5)
  dialogueLabel.BackgroundTransparency = 1
  dialogueLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
  dialogueLabel.TextSize = 14
  dialogueLabel.Font = Enum.Font.Gotham
  dialogueLabel.TextWrapped = true
  dialogueLabel.Text = ""
  dialogueLabel.Parent = background

  -- Hide the bubble initially
  billboardGui.Enabled = false

  -- Dialogue lines
  local dialogues = {
      "Hello, adventurer! Welcome to our village.",
      "The forest to the north is dangerous. Be careful!",
      "If you find any gems, bring them back to me.",
      "I heard there is treasure hidden in the mountain cave.",
      "Good luck on your journey!",
  }

  local currentLine = 1
  local isTalking = false

  -- Typewriter effect: reveal text character by character
  local function typeText(text)
      dialogueLabel.Text = ""
      billboardGui.Enabled = true

      for i = 1, #text do
          dialogueLabel.Text = string.sub(text, 1, i)
          task.wait(0.03)  -- Speed of typing
      end
  end

  -- Handle interaction
  prompt.Triggered:Connect(function(player)
      if isTalking then return end
      isTalking = true

      -- Show the current dialogue line with typewriter effect
      typeText(dialogues[currentLine])

      -- Wait, then advance to next line
      task.wait(3)
      billboardGui.Enabled = false

      currentLine = currentLine + 1
      if currentLine > #dialogues then
          currentLine = 1  -- Loop back to the beginning
      end

      isTalking = false
  end)
  ```

- Students add dialogue NPCs to their worlds with custom conversation lines.

- Advanced students create a branching dialogue system with choices.

**75-85 min: Sharing/Discussion**

- Ask 2-3 students to demonstrate their NPCs. Discuss:
  - *"How does the NPC know when to switch from patrol to chase?"*
  - *"What happens if PathfindingService cannot find a path? How does your code handle that?"*
  - *"How could you make the NPC feel more realistic?"* (Answers: idle animations, varying patrol speeds, randomised pause durations, looking at the player during dialogue.)
- Discuss game design: *"When should an NPC chase the player versus flee from the player? How would you change the state machine for a scared NPC?"*

**85-90 min: Closure & Preview**

- Ask: *"Name the three NPC states we implemented today."* (Idle, Patrol, Chase)
- Preview Session 16: *"Next session is project time. You will build an Adventure/RPG game that combines EVERYTHING from Unit 4 — terrain, tweens, NPCs, dialogue, and quests. This is your biggest project yet."*
- Remind students to save.

##### Differentiation

**Support:**
- Provide a pre-built NPC model (generated from Rig Builder) that students can drop into their world, so they only need to write the AI script.
- Give struggling students the `walkTo()` function pre-written as a ModuleScript so they can focus on the state machine logic.
- Simplify to two states only (Patrol and Chase) instead of three, removing the Idle state to reduce complexity.

**Extension:**
- Challenge advanced students to add an "Attack" state where the NPC deals damage when within melee range and an "Investigate" state where the NPC walks to the player's last known position after losing sight.
- Ask them to create multiple NPC types (guard, merchant, villager) with different behaviours, patrol routes, and dialogue trees.
- Have them implement NPC health bars using BillboardGuis and TweenService — the health bar smoothly decreases when the NPC takes damage.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| NPC creation | Cannot create a functional NPC model | Creates a model but missing Humanoid or HumanoidRootPart | Creates a complete NPC with Humanoid, body parts, and PrimaryPart set | Customised NPC with accessories, proper naming, and clean hierarchy |
| PathfindingService usage | Cannot use PathfindingService | Computes a path but cannot execute waypoint walking | Computes paths and walks through waypoints with jump support | Handles path failures gracefully and re-computes paths dynamically |
| Behaviour states | No state system implemented | One behaviour (e.g., patrol only) without transitions | Two or more states with proximity-based transitions | Three or more states with smooth transitions, configurable ranges, and edge case handling |
| Dialogue system | No dialogue implemented | Basic print statements for dialogue | ProximityPrompt dialogue with multiple lines and typewriter effect | Branching dialogue with choices, visual speech bubbles, and proper NPC facing |

##### Teacher Notes

- NPC creation using Rig Builder is the fastest and most reliable approach. If Rig Builder is not available in the student's version of Studio, they can use the Toolbox to search for "R6 Rig" or "R15 Rig" and insert a pre-made model.
- The most critical property for NPC movement is `PrimaryPart`. If the Model's PrimaryPart is not set to `HumanoidRootPart`, `MoveTo()` and PathfindingService will not work correctly. Always check this first when debugging.
- PathfindingService requires a NavigationMesh (NavMesh) to be computed. Roblox does this automatically for most geometry, but very complex terrain or thin parts may not be pathfable. If an NPC gets stuck, check for terrain holes or parts that block the NavMesh.
- The state machine uses a `while true` loop with a short `task.wait(0.1)`. This is a polling approach — it checks the player's distance every 0.1 seconds. A more advanced approach would use events, but polling is simpler for students to understand and debug.
- ProximityPrompt has a default keybind of "E" on keyboard and a tap/hold on mobile. Students do not need to configure input — it is handled automatically.
- The typewriter effect in the dialogue system uses `string.sub()` to reveal one character at a time. If students are confused by this, walk through it: `string.sub("Hello", 1, 1)` = "H", `string.sub("Hello", 1, 2)` = "He", etc.
- Performance tip: having many NPCs with PathfindingService computing paths simultaneously can cause lag. For the classroom (1-3 NPCs), this is fine. Mention this for students planning large-scale games.

---

#### SESSION 15 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 15: NPC Creation & Basic AI**

---

##### Part 1: NPC Anatomy

**Instructions:** Label the key components of a Roblox NPC Model. Write the name and purpose of each.

```
NPC Model
├── _________________________  (Purpose: __________________________________)
├── _________________________  (Purpose: __________________________________)
├── Head                       (Purpose: visible head part)
├── Torso                      (Purpose: visible torso part)
├── Left Arm                   (Purpose: visible left arm part)
├── Right Arm                  (Purpose: visible right arm part)
├── Left Leg                   (Purpose: visible left leg part)
└── Right Leg                  (Purpose: visible right leg part)
```

**Question:** What happens if an NPC Model does not have a Humanoid component?

> _______________________________________________________________________________

**Question:** Why must the HumanoidRootPart be set as the Model's PrimaryPart?

> _______________________________________________________________________________

---

##### Part 2: Create Your NPC

**Instructions:** Build an NPC and add it to your game world.

**Step 1:** Generate an NPC

1. [ ] Go to the **Avatar** tab > **Rig Builder** > Choose **R6** > Click **Generate**
2. [ ] Rename the Model to a character name (e.g., `GuardNPC`, `Villager`, `Shopkeeper`)
3. [ ] Move the NPC to a sensible location in your game world
4. [ ] Optional: Change body part colours, add a Shirt/Pants, or add an accessory

**NPC Name:** ___________________________
**NPC Location:** ___________________________
**NPC Purpose in your game:** ___________________________

---

##### Part 3: PathfindingService — Walking to a Target

**Instructions:** Add a Script inside your NPC and write a `walkTo()` function using PathfindingService.

```lua
local PathfindingService = game:GetService("PathfindingService")

local npc = script.Parent
local humanoid = npc:WaitForChild("Humanoid")
local rootPart = npc:WaitForChild("HumanoidRootPart")

local function walkTo(targetPosition)
    local path = PathfindingService:CreatePath({
        AgentRadius = 2,
        AgentHeight = 5,
        AgentCanJump = true,
    })

    path:ComputeAsync(__________________, __________________)

    if path.Status == Enum.PathStatus.Success then
        local waypoints = path:GetWaypoints()
        for _, waypoint in ipairs(waypoints) do
            if waypoint.Action == Enum.PathWaypointAction.Jump then
                ____________________________________
            end
            humanoid:MoveTo(waypoint.Position)
            humanoid.MoveToFinished:Wait()
        end
    else
        warn("[NPC] Path failed!")
    end
end

-- Test: make the NPC walk somewhere
task.wait(2)
walkTo(Vector3.new(__________, __________, __________))
print("[NPC] Arrived!")
```

**Fill in the blanks and test. Does the NPC walk to the target?** [ ] Yes [ ] No

**Place an obstacle (a Part) between the NPC and the target. Does the NPC walk around it?** [ ] Yes [ ] No

---

##### Part 4: Patrol Behaviour

**Instructions:** Make your NPC patrol between at least 4 points in a loop.

```lua
local patrolPoints = {
    Vector3.new(__________, __________, __________),
    Vector3.new(__________, __________, __________),
    Vector3.new(__________, __________, __________),
    Vector3.new(__________, __________, __________),
}

local function patrol()
    while true do
        for _, point in ipairs(patrolPoints) do
            walkTo(point)
            task.wait(________)  -- How long to pause at each point?
        end
    end
end

patrol()
```

**Test:** Does the NPC patrol in a loop? [ ] Yes [ ] No

**Tip:** Choose patrol points that are within your game world and on walkable terrain!

---

##### Part 5: Chase Behaviour

**Instructions:** Add chase behaviour so the NPC pursues the nearest player when they get close.

Write a `getNearestPlayer()` function:

```lua
local Players = game:GetService("Players")

local CHASE_RANGE = 30
local LOSE_RANGE = 50

local function getNearestPlayer()
    local nearest = nil
    local nearestDist = math.huge

    for _, player in ipairs(Players:GetPlayers()) do
        local char = player.Character
        if char then
            local pRoot = char:FindFirstChild("HumanoidRootPart")
            if pRoot then
                local dist = (rootPart.Position - pRoot.Position).Magnitude
                if dist < nearestDist then
                    nearestDist = dist
                    nearest = player
                end
            end
        end
    end

    return nearest, nearestDist
end
```

Now modify your main loop to switch between PATROL and CHASE:

```lua
local currentState = "PATROL"
local currentPatrolIndex = 1

while true do
    local nearestPlayer, distance = getNearestPlayer()

    if currentState == "PATROL" then
        humanoid.WalkSpeed = 14

        -- Check if player is close enough to chase
        if distance <= CHASE_RANGE then
            currentState = "__________"
        else
            local target = patrolPoints[currentPatrolIndex]
            walkTo(target)
            task.wait(2)
            currentPatrolIndex = (currentPatrolIndex % #patrolPoints) + 1
        end

    elseif currentState == "CHASE" then
        humanoid.WalkSpeed = __________  -- Faster than patrol!

        if nearestPlayer and nearestPlayer.Character then
            local pRoot = nearestPlayer.Character:FindFirstChild("HumanoidRootPart")
            if pRoot then
                humanoid:MoveTo(pRoot.Position)
            end
        end

        -- Check if player escaped
        if distance > LOSE_RANGE then
            currentState = "__________"
        end

        task.wait(0.2)
    end

    task.wait(0.1)
end
```

**Fill in the blanks and test.**

Does the NPC chase you when you get close? [ ] Yes [ ] No

Does the NPC return to patrol when you move far away? [ ] Yes [ ] No

---

##### Part 6: Dialogue NPC (Challenge)

**Instructions:** Create a SECOND NPC (a friendly one) with a dialogue system.

1. [ ] Generate a new R6 rig, rename it (e.g., `Elder`, `Merchant`)
2. [ ] Add a Script inside the NPC
3. [ ] Create a ProximityPrompt with ActionText = "Talk"
4. [ ] Write at least 5 dialogue lines
5. [ ] Add a typewriter effect that reveals text character by character

Write your 5 dialogue lines:

1. "_______________________________________________________________"
2. "_______________________________________________________________"
3. "_______________________________________________________________"
4. "_______________________________________________________________"
5. "_______________________________________________________________"

**Test:** Can you walk up to the NPC and press E to talk? [ ] Yes [ ] No

Does the text appear one character at a time? [ ] Yes [ ] No

---

##### Bonus Challenge

Create an NPC that FLEES from the player instead of chasing. Invert the chase logic:
- When the player gets close, calculate a position AWAY from the player.
- Make the NPC run to that escape position.
- When the player is far enough away, return to idle.

**Hint:** To calculate a flee direction:
```lua
local direction = (rootPart.Position - playerRoot.Position).Unit
local fleeTarget = rootPart.Position + direction * 30  -- Run 30 studs away
```

---

##### Reflection

1. Explain the difference between `humanoid:MoveTo()` and using PathfindingService. When would you use each?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Draw a state diagram for your NPC showing all states and the conditions that cause transitions:

```
[State 1] --condition--> [State 2] --condition--> [State 3]
```

3. What was the most challenging part of creating NPC AI? How could you improve your NPC in the future?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

### Session 16: Project 3 — Adventure/RPG Game

---

#### SESSION 16 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 16 of 24 |
| **Title** | Project 3 — Adventure/RPG Game |
| **Unit** | Unit 4: Game World Design & Advanced Mechanics |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Design and build a functional adventure/RPG game that combines terrain, animated elements (tweens), interactive NPCs, and at least one quest with defined objectives.
2. Implement a quest system that tracks player progress through multiple objectives, provides NPC dialogue that updates based on quest state, and rewards the player upon completion.
3. Save and load player progress (quest state and inventory) using DataStoreService, ensuring data persists between game sessions.
4. Conduct a structured playtest, identify at least two gameplay issues, and present their game to peers with a clear explanation of design decisions.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 16 Worksheet (printed or displayed digitally — serves as project guide and design document)
- Whiteboard for system architecture and quest flowchart
- Timer or stopwatch for managing project phases
- Students' game worlds with terrain, tweens, and NPCs from Sessions 13-15
- Teacher reference: Roblox Creator Documentation — DataStoreService and PathfindingService pages

##### Procedure

**0-5 min: Warm-Up — "What Makes an Adventure Game?"**

- Ask: *"What is the difference between an adventure game and the tycoon you built in Session 12? What does an adventure game have that a tycoon does not?"*
- Take responses: story, quests, NPCs that give you tasks, exploration, a world to discover, enemies, dialogue, treasure.
- Say: *"Today you build YOUR adventure game. You have the terrain. You have the animated elements. You have NPCs. Now we add the glue that holds it all together — a QUEST SYSTEM. Quests give players a reason to explore, a goal to achieve, and a reward to earn."*

**5-15 min: Introduction — Quest System Architecture**

- Draw the quest system architecture on the whiteboard:

  ```
  ReplicatedStorage/
  ├── Modules/
  │   ├── QuestDatabase (ModuleScript)
  │   └── GameConfig (ModuleScript)
  ├── QuestUpdateEvent (RemoteEvent)
  └── QuestCompleteEvent (RemoteEvent)

  ServerScriptService/
  ├── QuestServer (Script)
  └── DataManager (Script)

  StarterPlayerScripts/
  └── QuestClient (LocalScript)
  ```

- Explain quest structure: each quest has an ID, a name, a description, objectives (things to do), NPC giver, NPC turn-in, and rewards.

- Build the QuestDatabase on the projector:

  ```lua
  -- ModuleScript: QuestDatabase (in ReplicatedStorage/Modules)
  local QuestDatabase = {}

  QuestDatabase.Quests = {
      {
          Id = "quest_welcome",
          Name = "Welcome to the Village",
          Description = "Talk to the Elder to learn about the village.",
          GiverNPC = "Elder",
          TurnInNPC = "Elder",
          Objectives = {
              {Id = "talk_elder", Description = "Talk to the Elder", Type = "Talk", Target = "Elder", Required = 1},
          },
          Rewards = {
              Gold = 50,
              Experience = 100,
          },
          NextQuest = "quest_gather",  -- Unlock next quest on completion
      },
      {
          Id = "quest_gather",
          Name = "Gather Supplies",
          Description = "Collect 3 crystals scattered across the forest.",
          GiverNPC = "Elder",
          TurnInNPC = "Elder",
          Objectives = {
              {Id = "collect_crystals", Description = "Collect Crystals", Type = "Collect", Target = "Crystal", Required = 3},
          },
          Rewards = {
              Gold = 150,
              Experience = 250,
          },
          NextQuest = "quest_defeat",
      },
      {
          Id = "quest_defeat",
          Name = "Defeat the Guardian",
          Description = "A powerful guardian blocks the mountain pass. Defeat it to proceed.",
          GiverNPC = "Elder",
          TurnInNPC = "Elder",
          Objectives = {
              {Id = "defeat_guardian", Description = "Defeat the Guardian", Type = "Defeat", Target = "Guardian", Required = 1},
          },
          Rewards = {
              Gold = 500,
              Experience = 1000,
              Item = "Golden Sword",
          },
          NextQuest = nil,  -- Final quest
      },
  }

  function QuestDatabase.getQuestById(id)
      for _, quest in ipairs(QuestDatabase.Quests) do
          if quest.Id == id then
              return quest
          end
      end
      return nil
  end

  return QuestDatabase
  ```

- Walk through the structure: *"Each quest has objectives. Each objective has a Type — Talk, Collect, or Defeat. The server tracks progress towards each objective. When all objectives are complete, the player can turn in the quest for rewards."*

**15-35 min: Guided Practice — Quest Server Logic**

- Build the QuestServer script:

  ```lua
  -- Script: QuestServer (in ServerScriptService)
  local Players = game:GetService("Players")
  local ReplicatedStorage = game:GetService("ReplicatedStorage")
  local DataStoreService = game:GetService("DataStoreService")

  local QuestDatabase = require(ReplicatedStorage:WaitForChild("Modules"):WaitForChild("QuestDatabase"))

  local QuestUpdateEvent = ReplicatedStorage:WaitForChild("QuestUpdateEvent")
  local QuestCompleteEvent = ReplicatedStorage:WaitForChild("QuestCompleteEvent")

  local QuestDataStore = DataStoreService:GetDataStore("QuestSaveData_v1")

  -- Player quest data stored in memory
  local playerQuestData = {}

  -- Initialise quest data for a player
  local function initQuestData(player)
      local key = "Quest_" .. player.UserId
      local success, data = pcall(function()
          return QuestDataStore:GetAsync(key)
      end)

      if success and data then
          playerQuestData[player.UserId] = data
          print("[QUEST SERVER] Loaded quest data for " .. player.Name)
      else
          playerQuestData[player.UserId] = {
              ActiveQuest = "quest_welcome",  -- First quest
              CompletedQuests = {},
              QuestProgress = {},            -- {objectiveId = currentCount}
              Gold = 0,
              Experience = 0,
          }
          print("[QUEST SERVER] New quest data for " .. player.Name)
      end

      -- Send initial quest info to client
      task.defer(function()
          local qData = playerQuestData[player.UserId]
          if qData and qData.ActiveQuest then
              local quest = QuestDatabase.getQuestById(qData.ActiveQuest)
              if quest then
                  QuestUpdateEvent:FireClient(player, "QuestActive", quest, qData.QuestProgress)
              end
          end
      end)
  end

  -- Save quest data
  local function saveQuestData(player)
      local key = "Quest_" .. player.UserId
      local data = playerQuestData[player.UserId]
      if data then
          local success, err = pcall(function()
              QuestDataStore:SetAsync(key, data)
          end)
          if not success then
              warn("[QUEST SERVER] Save failed for " .. player.Name .. ": " .. tostring(err))
          end
      end
  end

  -- Update quest progress
  local function updateProgress(player, objectiveType, targetName)
      local data = playerQuestData[player.UserId]
      if not data or not data.ActiveQuest then return end

      local quest = QuestDatabase.getQuestById(data.ActiveQuest)
      if not quest then return end

      -- Find matching objective
      for _, objective in ipairs(quest.Objectives) do
          if objective.Type == objectiveType and objective.Target == targetName then
              local progress = data.QuestProgress[objective.Id] or 0
              if progress < objective.Required then
                  progress = progress + 1
                  data.QuestProgress[objective.Id] = progress
                  print("[QUEST SERVER] " .. player.Name .. " progress: " .. objective.Description .. " " .. progress .. "/" .. objective.Required)

                  -- Notify client of progress update
                  QuestUpdateEvent:FireClient(player, "ProgressUpdate", quest, data.QuestProgress)

                  -- Check if all objectives are complete
                  local allComplete = true
                  for _, obj in ipairs(quest.Objectives) do
                      local p = data.QuestProgress[obj.Id] or 0
                      if p < obj.Required then
                          allComplete = false
                          break
                      end
                  end

                  if allComplete then
                      -- Apply rewards
                      data.Gold = data.Gold + (quest.Rewards.Gold or 0)
                      data.Experience = data.Experience + (quest.Rewards.Experience or 0)

                      -- Mark as completed
                      table.insert(data.CompletedQuests, quest.Id)
                      data.QuestProgress = {}  -- Reset progress for next quest

                      -- Activate next quest
                      if quest.NextQuest then
                          data.ActiveQuest = quest.NextQuest
                          local nextQuest = QuestDatabase.getQuestById(quest.NextQuest)
                          QuestUpdateEvent:FireClient(player, "QuestComplete", quest, data.QuestProgress)
                          task.wait(2)
                          QuestUpdateEvent:FireClient(player, "QuestActive", nextQuest, data.QuestProgress)
                      else
                          data.ActiveQuest = nil
                          QuestUpdateEvent:FireClient(player, "AllQuestsComplete", quest, data.QuestProgress)
                      end

                      print("[QUEST SERVER] " .. player.Name .. " completed: " .. quest.Name)
                  end
              end
          end
      end
  end

  -- Player connections
  Players.PlayerAdded:Connect(function(player)
      initQuestData(player)
  end)

  Players.PlayerRemoving:Connect(function(player)
      saveQuestData(player)
      playerQuestData[player.UserId] = nil
  end)

  -- Listen for quest-related interactions
  QuestCompleteEvent.OnServerEvent:Connect(function(player, action, targetName)
      if action == "Talk" then
          updateProgress(player, "Talk", targetName)
      elseif action == "Collect" then
          updateProgress(player, "Collect", targetName)
      elseif action == "Defeat" then
          updateProgress(player, "Defeat", targetName)
      end
  end)

  -- Auto-save every 60 seconds
  task.spawn(function()
      while true do
          task.wait(60)
          for _, player in ipairs(Players:GetPlayers()) do
              saveQuestData(player)
          end
      end
  end)
  ```

- Build a simple quest UI client:

  ```lua
  -- LocalScript: QuestClient (in StarterPlayerScripts)
  local Players = game:GetService("Players")
  local ReplicatedStorage = game:GetService("ReplicatedStorage")

  local QuestUpdateEvent = ReplicatedStorage:WaitForChild("QuestUpdateEvent")

  local player = Players.LocalPlayer
  local playerGui = player:WaitForChild("PlayerGui")

  -- Create Quest UI
  local screenGui = Instance.new("ScreenGui")
  screenGui.Name = "QuestGui"
  screenGui.Parent = playerGui

  local questFrame = Instance.new("Frame")
  questFrame.Name = "QuestTracker"
  questFrame.Size = UDim2.new(0, 280, 0, 120)
  questFrame.Position = UDim2.new(0, 10, 0, 10)
  questFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 40)
  questFrame.BackgroundTransparency = 0.3
  questFrame.Parent = screenGui

  local corner = Instance.new("UICorner")
  corner.CornerRadius = UDim.new(0, 10)
  corner.Parent = questFrame

  local questTitle = Instance.new("TextLabel")
  questTitle.Name = "QuestTitle"
  questTitle.Size = UDim2.new(1, -10, 0, 25)
  questTitle.Position = UDim2.new(0, 5, 0, 5)
  questTitle.BackgroundTransparency = 1
  questTitle.TextColor3 = Color3.fromRGB(255, 215, 0)
  questTitle.TextSize = 18
  questTitle.Font = Enum.Font.GothamBold
  questTitle.TextXAlignment = Enum.TextXAlignment.Left
  questTitle.Text = "No Active Quest"
  questTitle.Parent = questFrame

  local questDesc = Instance.new("TextLabel")
  questDesc.Name = "QuestDescription"
  questDesc.Size = UDim2.new(1, -10, 0, 30)
  questDesc.Position = UDim2.new(0, 5, 0, 30)
  questDesc.BackgroundTransparency = 1
  questDesc.TextColor3 = Color3.fromRGB(200, 200, 200)
  questDesc.TextSize = 13
  questDesc.Font = Enum.Font.Gotham
  questDesc.TextXAlignment = Enum.TextXAlignment.Left
  questDesc.TextWrapped = true
  questDesc.Text = ""
  questDesc.Parent = questFrame

  local questObjective = Instance.new("TextLabel")
  questObjective.Name = "QuestObjective"
  questObjective.Size = UDim2.new(1, -10, 0, 50)
  questObjective.Position = UDim2.new(0, 5, 0, 65)
  questObjective.BackgroundTransparency = 1
  questObjective.TextColor3 = Color3.fromRGB(150, 255, 150)
  questObjective.TextSize = 14
  questObjective.Font = Enum.Font.Gotham
  questObjective.TextXAlignment = Enum.TextXAlignment.Left
  questObjective.TextWrapped = true
  questObjective.Text = ""
  questObjective.Parent = questFrame

  -- Update UI when we receive quest data from the server
  QuestUpdateEvent.OnClientEvent:Connect(function(action, quest, progress)
      if action == "QuestActive" then
          questTitle.Text = quest.Name
          questDesc.Text = quest.Description

          -- Build objectives text
          local objText = ""
          for _, obj in ipairs(quest.Objectives) do
              local current = (progress and progress[obj.Id]) or 0
              local check = current >= obj.Required and "[DONE]" or "[" .. current .. "/" .. obj.Required .. "]"
              objText = objText .. check .. " " .. obj.Description .. "\n"
          end
          questObjective.Text = objText

      elseif action == "ProgressUpdate" then
          -- Update objectives display
          local objText = ""
          for _, obj in ipairs(quest.Objectives) do
              local current = (progress and progress[obj.Id]) or 0
              local check = current >= obj.Required and "[DONE]" or "[" .. current .. "/" .. obj.Required .. "]"
              objText = objText .. check .. " " .. obj.Description .. "\n"
          end
          questObjective.Text = objText

      elseif action == "QuestComplete" then
          questTitle.Text = "Quest Complete!"
          questDesc.Text = quest.Name .. " - Rewards collected!"
          questObjective.Text = "Gold: +" .. (quest.Rewards.Gold or 0) .. "\nXP: +" .. (quest.Rewards.Experience or 0)

      elseif action == "AllQuestsComplete" then
          questTitle.Text = "All Quests Complete!"
          questDesc.Text = "You have completed all available quests."
          questObjective.Text = "Congratulations, adventurer!"
      end
  end)

  print("[CLIENT] Quest UI loaded!")
  ```

- Students set up the RemoteEvents and ModuleScripts, then begin integrating the quest system with their existing NPCs and world.

**35-60 min: Independent Practice — Building the Adventure Game**

- Students work independently or in pairs to build their complete game. The worksheet serves as a project guide.

- Key integration tasks:
  1. **Connect NPC dialogue to quest system.** Modify the NPC dialogue script to fire `QuestCompleteEvent:FireServer("Talk", npcName)` when the player talks to a quest-relevant NPC.

  ```lua
  -- Add to NPC dialogue script (after displaying dialogue)
  local QuestCompleteEvent = ReplicatedStorage:WaitForChild("QuestCompleteEvent")

  prompt.Triggered:Connect(function(player)
      -- ... existing dialogue code ...

      -- Notify the quest server that the player talked to this NPC
      QuestCompleteEvent:FireServer("Talk", npc.Name)
  end)
  ```

  2. **Create collectible items.** Place Parts in the world that fire quest progress when collected:

  ```lua
  -- Script: Collectible (inside a Part named "Crystal" in Workspace)
  local ReplicatedStorage = game:GetService("ReplicatedStorage")
  local QuestCompleteEvent = ReplicatedStorage:WaitForChild("QuestCompleteEvent")
  local TweenService = game:GetService("TweenService")

  local collectible = script.Parent

  -- Add a pulsing animation (from Session 14!)
  local pulseInfo = TweenInfo.new(0.8, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut, -1, true)
  local pulseTween = TweenService:Create(collectible, pulseInfo, {Size = collectible.Size * 1.2})
  pulseTween:Play()

  local collected = false

  collectible.Touched:Connect(function(hit)
      if collected then return end
      local player = game:GetService("Players"):GetPlayerFromCharacter(hit.Parent)
      if player then
          collected = true
          pulseTween:Cancel()

          -- Notify quest server
          QuestCompleteEvent:FireServer("Collect", "Crystal")

          -- Animate collection
          local collectTween = TweenService:Create(
              collectible,
              TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In),
              {Size = Vector3.new(0, 0, 0), Transparency = 1}
          )
          collectTween:Play()
          collectTween.Completed:Wait()
          collectible:Destroy()
      end
  end)
  ```

  3. **Add quest-giving NPCs with conditional dialogue.** Modify NPC dialogue to change based on quest state (handled by the server sending updates to the client).

- Circulate the room. Help students with:
  - Connecting their existing NPCs from Session 15 to the quest system.
  - Placing collectibles in their terrain from Session 13.
  - Ensuring animated doors and platforms from Session 14 work alongside NPCs.

**60-75 min: Extension/Advanced Activity — Polish and Enhancements**

- Students choose at least ONE enhancement:
  1. **Quest notification animation:** Use TweenService to animate the quest tracker when a quest updates — flash the background colour, bounce the frame, or pulse the text.
  2. **Enemy NPC with health:** Create a guardian NPC that the player must defeat. When its Humanoid health reaches 0, fire `QuestCompleteEvent:FireServer("Defeat", "Guardian")`.
  3. **Reward items:** When a quest is completed, grant a visible item (a tool or accessory) to the player by cloning it from ServerStorage.
  4. **Sound design:** Add ambient sounds to terrain zones (bird chirps in the forest, wind on the mountain, waves at the beach) using Sound objects attached to Parts.
  5. **Map markers:** Add BillboardGuis above quest objectives (a glowing "!" above quest NPCs, a shimmering effect on collectibles).

- Provide enemy NPC code for students who want to implement the "Defeat" quest type:

  ```lua
  -- Script: EnemyNPC (inside a guardian Model with Humanoid)
  local ReplicatedStorage = game:GetService("ReplicatedStorage")
  local QuestCompleteEvent = ReplicatedStorage:WaitForChild("QuestCompleteEvent")

  local npc = script.Parent
  local humanoid = npc:WaitForChild("Humanoid")

  -- Track which players have contributed to the defeat
  local defeated = false

  humanoid.Died:Connect(function()
      if defeated then return end
      defeated = true

      -- Find the player who killed this NPC (simplified: credit nearest player)
      local Players = game:GetService("Players")
      local rootPart = npc:FindFirstChild("HumanoidRootPart")
      if rootPart then
          for _, player in ipairs(Players:GetPlayers()) do
              local char = player.Character
              if char then
                  local pRoot = char:FindFirstChild("HumanoidRootPart")
                  if pRoot and (rootPart.Position - pRoot.Position).Magnitude < 50 then
                      QuestCompleteEvent:FireServer("Defeat", npc.Name)
                  end
              end
          end
      end

      -- Remove the NPC after 3 seconds
      task.wait(3)
      npc:Destroy()
  end)
  ```

**75-85 min: Sharing/Discussion — Playtesting and Presentations**

- Students playtest each other's games. Have them switch seats and play a classmate's adventure game for 5 minutes, then provide feedback.

- Feedback protocol (written on the board):
  1. **One thing that works well:** _______________
  2. **One thing that could be improved:** _______________
  3. **One question about a design decision:** _______________

- After peer playtesting, ask 2-3 students to present their game to the class (3 minutes each):
  - *"What is the story of your adventure game?"*
  - *"How many quests does it have?"*
  - *"What was the hardest technical challenge and how did you solve it?"*
  - *"If you had more time, what would you add?"*

**85-90 min: Closure & Preview**

- Say: *"You have just completed Unit 4 — and with it, one of the most complex game projects in this course. You built a world, animated it, filled it with NPCs, and gave players a reason to explore with quests. That is game development."*
- Ask: *"What was the most satisfying moment of building your adventure game?"* Take 3-4 responses.
- Preview Unit 5: *"In the next unit, we go even deeper — UI design with professional-quality menus, audio systems with dynamic music and sound effects, save/load systems for complex game states, and visual polish that makes your games look like they belong on the Roblox front page."*
- Remind students to save and optionally publish their game.

##### Differentiation

**Support:**
- Provide a "Project Starter Template" with the folder structure, RemoteEvents, QuestDatabase, and quest UI already set up — struggling students focus on designing quests and placing NPCs/collectibles in their world.
- Simplify to a single quest with one "Talk" objective — the student only needs to connect one NPC to the quest system.
- Allow students who did not complete Sessions 13-15 features to use a pre-built world template with terrain, lighting, and one NPC already in place.

**Extension:**
- Challenge advanced students to implement branching quests — where the player's choice affects which quest comes next (e.g., "Help the village" vs "Explore the dungeon" branches).
- Ask them to create a minimap UI using a ViewportFrame that shows a top-down view of the game world with player and NPC positions.
- Have them implement a full combat system with attack animations (using TweenService), damage numbers floating above enemies (BillboardGui + TweenService), and a loot drop system that spawns items when enemies are defeated.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Game world quality | No terrain or world design | Basic terrain with minimal material or lighting | Multi-zone terrain with materials, lighting, atmosphere, and animated elements | Polished world with smooth transitions, thematic zones, dynamic lighting, and environmental detail |
| Quest system | No quest system implemented | Quest database exists but tracking/UI does not work | At least one quest works end-to-end: accept, progress, complete, reward | Multiple quests chain together with NPC dialogue, collectibles, and combat objectives |
| NPC integration | No NPCs in the game | NPCs exist but do not interact with the player | NPCs patrol and have dialogue connected to the quest system | NPCs have multiple behaviour states, contextual dialogue, and meaningful quest roles |
| Data persistence | No saving implemented | DataStore code present but not functional | Saves and loads quest progress correctly | Saves quest state, gold, experience, and completed quest history; handles errors gracefully |

##### Teacher Notes

- This session is the most ambitious in the course so far. Students are integrating four sessions worth of skills into one project. Expect a wide range of completion levels — some students will have a polished multi-quest game, others will have a single quest working. Both are acceptable outcomes.
- The quest system uses a linear quest chain (quest_welcome -> quest_gather -> quest_defeat). This is simpler than a branching system and appropriate for the intermediate level. Advanced students can modify the structure for branching.
- DataStoreService for quest saving works identically to the tycoon DataStore from Session 12. Students who completed Session 12 should find this familiar. For students who struggled with DataStore, allow them to skip persistence and focus on the quest logic.
- The collectible items should be placed manually in the workspace during build time. In a production game, they would be spawned dynamically by the server. For this project, manual placement is sufficient.
- Time management is critical. Recommend:
  - 0-15 min: Setup and quest system code (guided)
  - 15-35 min: Server logic (guided)
  - 35-60 min: Integration with existing world (independent)
  - 60-75 min: Enhancements (independent)
  - 75-90 min: Playtesting and presentation
- If students finish their adventure game early, encourage them to play-test a classmate's game and provide written feedback using the three-point protocol on the board.
- Peer playtesting is extremely valuable — students often find bugs and design issues that the creator missed. Encourage constructive, specific feedback rather than vague comments like "it's good."

---

#### SESSION 16 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 16: Project 3 — Adventure/RPG Game**

---

##### Game Design Document

Before coding, plan your adventure game.

**Game Title:** _______________________________________________

**Setting/Theme:** _______________________________________________

**Story Summary (2-3 sentences):**

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

**Zones in Your World:**

| Zone # | Name | Terrain Materials | Mood/Lighting | What Happens Here |
|--------|------|-------------------|---------------|-------------------|
| 1 | _____________ | _____________ | _____________ | _____________ |
| 2 | _____________ | _____________ | _____________ | _____________ |
| 3 | _____________ | _____________ | _____________ | _____________ |

**NPCs:**

| NPC Name | Location | Role | Behaviour (Patrol/Idle/Chase) |
|----------|----------|------|-------------------------------|
| _____________ | _____________ | _____________ | _____________ |
| _____________ | _____________ | _____________ | _____________ |
| _____________ | _____________ | _____________ | _____________ |

---

##### Quest Design

Design at least TWO quests. Fill in the details:

**Quest 1:**

| Field | Details |
|-------|---------|
| Quest Name | _________________________________ |
| Quest Giver (NPC) | _________________________________ |
| Description | _________________________________ |
| Objective Type | Talk / Collect / Defeat (circle one) |
| Objective Target | _________________________________ |
| Objective Count | _________ |
| Reward (Gold) | _________ |
| Reward (XP) | _________ |
| Next Quest | _________________________________ |

**Quest 2:**

| Field | Details |
|-------|---------|
| Quest Name | _________________________________ |
| Quest Giver (NPC) | _________________________________ |
| Description | _________________________________ |
| Objective Type | Talk / Collect / Defeat (circle one) |
| Objective Target | _________________________________ |
| Objective Count | _________ |
| Reward (Gold) | _________ |
| Reward (XP) | _________ |
| Next Quest | _________________________________ |

---

##### Project Setup Checklist

1. [ ] Create a **Folder** in ReplicatedStorage named `Modules`
2. [ ] Create a **ModuleScript** `QuestDatabase` in Modules (with your quest data)
3. [ ] Create a **RemoteEvent** `QuestUpdateEvent` in ReplicatedStorage
4. [ ] Create a **RemoteEvent** `QuestCompleteEvent` in ReplicatedStorage
5. [ ] Create a **Script** `QuestServer` in ServerScriptService
6. [ ] Create a **LocalScript** `QuestClient` in StarterPlayerScripts
7. [ ] Verify terrain world from Session 13 is present
8. [ ] Verify animated elements from Session 14 are present
9. [ ] Verify NPCs from Session 15 are present and functional

---

##### Integration Checklist

Connect all your systems together:

**NPC + Quests:**
- [ ] Quest-giver NPC has a ProximityPrompt
- [ ] Talking to the NPC fires `QuestCompleteEvent:FireServer("Talk", npcName)`
- [ ] NPC dialogue mentions the quest

**Collectibles + Quests:**
- [ ] Collectible items placed in the world (at least 3)
- [ ] Touching a collectible fires `QuestCompleteEvent:FireServer("Collect", itemName)`
- [ ] Collectibles have a pulse/spin animation (TweenService)
- [ ] Collectibles are destroyed after collection

**Quest UI:**
- [ ] Quest tracker shows in the top-left corner
- [ ] Quest name and description display correctly
- [ ] Objective progress updates (e.g., "1/3 Crystals Collected")
- [ ] "Quest Complete!" notification appears when finished

**Optional: Enemy + Quests:**
- [ ] Enemy NPC exists with Humanoid health
- [ ] Defeating the enemy fires `QuestCompleteEvent:FireServer("Defeat", enemyName)`

---

##### Testing Checklist

| Test | Expected Result | Actual Result | Pass/Fail |
|------|----------------|---------------|-----------|
| Quest tracker appears on screen | Shows first quest name and objective | _____________ | [ ] P / [ ] F |
| Talk to quest NPC | Progress updates, dialogue shows | _____________ | [ ] P / [ ] F |
| Collect quest items | Progress count increases, item disappears | _____________ | [ ] P / [ ] F |
| Complete quest | "Quest Complete!" shows, rewards granted | _____________ | [ ] P / [ ] F |
| Next quest activates | New quest appears after completing previous | _____________ | [ ] P / [ ] F |
| NPC patrols/chases | NPC moves as expected | _____________ | [ ] P / [ ] F |
| Animated elements work | Doors open, platforms float, items pulse | _____________ | [ ] P / [ ] F |
| Save and reload | Quest progress persists after rejoining | _____________ | [ ] P / [ ] F |

**Bug Log:**

| Bug Description | Cause | Fix Applied |
|----------------|-------|-------------|
| _________________________________ | _________________________________ | _________________________________ |
| _________________________________ | _________________________________ | _________________________________ |
| _________________________________ | _________________________________ | _________________________________ |

---

##### Peer Playtest Feedback

**Playtester Name:** _______________________________________________

Have a classmate play your game and write their feedback:

1. **One thing that works well:**

> _______________________________________________________________________________

2. **One thing that could be improved:**

> _______________________________________________________________________________

3. **One question about a design decision:**

> _______________________________________________________________________________

**Your response to their question:**

> _______________________________________________________________________________

---

##### Enhancements Added

Which enhancement(s) did you add to your game? (Check all that apply)

- [ ] Quest notification animations (TweenService)
- [ ] Enemy NPC with health and defeat objective
- [ ] Reward items granted on quest completion
- [ ] Ambient sounds in terrain zones
- [ ] Map markers above quest objectives (BillboardGui)
- [ ] Other: _______________________________________________

**Describe your best enhancement in detail:**

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Reflection

1. What was the most technically challenging part of building your adventure game? How did you solve it?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Which concept from Unit 4 (Terrain, TweenService, NPCs, or Quest Systems) was the most important for making your game feel complete? Why?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. Compare your tycoon game (Session 12) to your adventure game (today). What skills did you use in both? What new skills did you need for the adventure game?

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

4. If you could continue working on this adventure game for another two weeks, what three features would you add?

> 1. _________________________________________________________________________
>
> 2. _________________________________________________________________________
>
> 3. _________________________________________________________________________

---
# Roblox Studio Intermediate: Lesson Plans & Worksheets
## Unit 5: Multiplayer Systems & Game Polish (Sessions 17-20)

### Unit Overview

Unit 5 elevates students from functional game builders to polished game designers. The unit opens with GUI design, teaching students how to create professional heads-up displays using ScreenGui, Frames, TextLabels, and TextButtons — the visual layer that communicates game state to players. Session 18 introduces SoundService and audio implementation, transforming silent prototypes into immersive experiences with background music, sound effects, and volume control. Session 19 tackles multiplayer mechanics through the Teams service, team-based scoring, spawn configuration, and round-based game systems — the features that make Roblox games social and replayable. The unit concludes with a dedicated session on game balancing, systematic playtesting, bug tracking, and performance optimisation, ensuring students understand that great games are not just built but refined through iteration. Every session pairs a detailed teacher-facing lesson plan with a hands-on student worksheet, ensuring that theory and practice remain inseparable.

---

### Session 17: GUI Design — ScreenGui, Frames, and Labels

---

#### SESSION 17 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 17 of 24 |
| **Title** | GUI Design — ScreenGui, Frames, and Labels |
| **Unit** | Unit 5: Multiplayer Systems & Game Polish |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Explain the GUI hierarchy in Roblox (ScreenGui > Frame > TextLabel/TextButton/ImageLabel) and describe the role of each element in building a user interface.
2. Create a functional HUD displaying at least three game data elements (health bar, score counter, and timer) using ScreenGui, Frames, TextLabels, and TextButtons.
3. Style GUI elements using properties such as BackgroundColor3, TextColor3, Font, TextScaled, and layout objects (UIListLayout, UIPadding, UICorner) to achieve a professional appearance.
4. Write a Luau script that dynamically updates GUI elements based on game data, connecting interface to gameplay logic through events and value changes.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 17 Worksheet (printed or displayed digitally)
- Whiteboard or interactive whiteboard for diagramming GUI hierarchy
- Timer or stopwatch for timed activities
- Reference images of professional game HUDs (3-4 examples from popular Roblox games)
- Teacher reference: Roblox Creator Documentation bookmarked at `https://create.roblox.com/docs`

##### Procedure

**0-5 min: Warm-Up — "What Information Does a Game Show You?"**

- As students settle, display the following prompt on the board: *"Think of a game you play regularly. Without looking at it, list every piece of information the screen shows you while you are playing — not the game world, but the overlay."*
- Allow 90 seconds of quiet thinking and writing. Then invite five or six students to share. Write each response on the board.
- Typical responses: "health bar," "minimap," "score," "ammo count," "timer," "team names," "currency," "inventory slots," "chat window."
- Group the responses into categories: **Player Status** (health, shield, stamina), **Game Progress** (score, round, timer), **Navigation** (minimap, compass), **Social** (team, chat).
- Say: *"All of these elements together are called the GUI — the Graphical User Interface. It is the layer between the player and the game. Today, you are going to build your own GUI from scratch in Roblox Studio."*

**5-15 min: Introduction — GUI Hierarchy and Structure**

- Open Roblox Studio on the projector. Create a new Baseplate project or open an existing demo project.
- Navigate to StarterGui in the Explorer panel. Say: *"Every GUI element a player sees lives inside StarterGui. When a player joins the game, Roblox copies everything from StarterGui into that player's PlayerGui. This means every player gets their own copy of the interface."*
- Demonstrate the hierarchy by adding elements step by step:
  1. **ScreenGui** — Right-click StarterGui > Insert Object > ScreenGui. Say: *"ScreenGui is the container. Think of it as an invisible canvas that covers the entire screen. Everything we build goes inside this."*
  2. **Frame** — Right-click ScreenGui > Insert Object > Frame. Say: *"A Frame is a rectangle. It can hold other GUI elements inside it, or it can be a visual background. Frames are the building blocks of layout."* Resize the frame using the Properties panel: set Size to `{0, 300, 0, 60}`. Explain UDim2: *"The first number in each pair is Scale (percentage of parent), the second is Offset (pixels). So `{0, 300, 0, 60}` means 300 pixels wide, 60 pixels tall."*
  3. **TextLabel** — Right-click Frame > Insert Object > TextLabel. Say: *"TextLabel displays text but cannot be clicked. It is for information — health values, score numbers, player names."* Set the Text property to `"Score: 0"`.
  4. **TextButton** — Right-click Frame > Insert Object > TextButton. Say: *"TextButton looks like TextLabel but can be clicked. It fires an event when the player clicks it."*
  5. **ImageLabel** — Right-click Frame > Insert Object > ImageLabel. Say: *"ImageLabel displays an image. Use it for icons, health bar backgrounds, or decorative elements."*
- Draw the hierarchy on the board:
  ```
  StarterGui
  └── ScreenGui
      └── Frame (HUD Container)
          ├── TextLabel (Score Display)
          ├── TextButton (Menu Button)
          └── ImageLabel (Icon)
  ```
- Say: *"This tree structure is exactly like the Explorer panel. Parent-child relationships matter — a child is positioned relative to its parent. If you move a Frame, everything inside it moves too."*

**15-35 min: Guided Practice — Building a Complete HUD**

- Guide students through building a full HUD step by step. Students follow along at their own machines:

  **Step 1: Set Up the ScreenGui**
  - In StarterGui, add a ScreenGui. Rename it `GameHUD`. In Properties, set `ResetOnSpawn` to `false`. Say: *"ResetOnSpawn controls whether the GUI is destroyed and recreated when the player respawns. For a persistent HUD, we want false."*

  **Step 2: Create the Top Bar Frame**
  - Add a Frame inside GameHUD. Rename it `TopBar`.
  - Set the following properties in the Properties panel:
    - `AnchorPoint` = `0.5, 0`
    - `Position` = `{0.5, 0, 0, 10}` (centred horizontally, 10 pixels from top)
    - `Size` = `{0.6, 0, 0, 50}` (60% of screen width, 50 pixels tall)
    - `BackgroundColor3` = `0, 0, 0` (black)
    - `BackgroundTransparency` = `0.3` (slightly see-through)
    - `BorderSizePixel` = `0`
  - Add a **UICorner** inside TopBar (Insert Object > UICorner). Set `CornerRadius` to `{0, 12}`. Say: *"UICorner rounds the corners of any Frame or button. A radius of 12 pixels gives a clean, modern look."*
  - Add a **UIPadding** inside TopBar. Set all four paddings to `{0, 8}`. Say: *"UIPadding adds space between the Frame edge and its contents — like margins in a document."*
  - Add a **UIListLayout** inside TopBar. Set `FillDirection` to `Horizontal`, `HorizontalAlignment` to `Center`, `VerticalAlignment` to `Center`, `Padding` to `{0, 20}`. Say: *"UIListLayout automatically arranges child elements in a row or column. No more dragging elements pixel by pixel."*

  **Step 3: Create the Health Display**
  - Add a Frame inside TopBar. Rename it `HealthContainer`. Set Size to `{0, 150, 1, 0}` (150 pixels wide, full height of parent). Set `BackgroundTransparency` to `1` (invisible).
  - Add a TextLabel inside HealthContainer. Rename it `HealthLabel`. Set:
    - `Size` = `{1, 0, 1, 0}` (fill parent)
    - `BackgroundTransparency` = `1`
    - `Text` = `"Health: 100"`
    - `TextColor3` = `255, 85, 85` (red)
    - `Font` = `GothamBold`
    - `TextScaled` = `true`
  - Say: *"TextScaled makes the text automatically resize to fill the label. This means your GUI looks correct on any screen size."*

  **Step 4: Create the Score Display**
  - Add another Frame inside TopBar. Rename it `ScoreContainer`. Copy the same size and transparency settings as HealthContainer.
  - Add a TextLabel inside ScoreContainer. Rename it `ScoreLabel`. Set:
    - `Size` = `{1, 0, 1, 0}`
    - `BackgroundTransparency` = `1`
    - `Text` = `"Score: 0"`
    - `TextColor3` = `255, 255, 85` (yellow)
    - `Font` = `GothamBold`
    - `TextScaled` = `true`

  **Step 5: Create the Timer Display**
  - Add a third Frame inside TopBar. Rename it `TimerContainer`. Same settings.
  - Add a TextLabel inside. Rename it `TimerLabel`. Set:
    - `Size` = `{1, 0, 1, 0}`
    - `BackgroundTransparency` = `1`
    - `Text` = `"Time: 5:00"`
    - `TextColor3` = `255, 255, 255` (white)
    - `Font` = `GothamBold`
    - `TextScaled` = `true`

- Run the game (F5) and show the HUD in action. Say: *"The HUD is visible but static — it does not change. Now we connect it to actual game data."*

**35-60 min: Independent Practice — Scripting the GUI**

- Guide students through creating a script that updates the GUI. In ServerScriptService, add a Script. Rename it `GameManager`:

```lua
-- GameManager Script (ServerScriptService)
-- This script manages game data and updates the GUI for each player

local Players = game:GetService("Players")

local function setupPlayer(player)
    -- Wait for the character to load
    player.CharacterAdded:Connect(function(character)
        -- Create leaderstats (visible on the leaderboard)
        local leaderstats = Instance.new("Folder")
        leaderstats.Name = "leaderstats"
        leaderstats.Parent = player

        local score = Instance.new("IntValue")
        score.Name = "Score"
        score.Value = 0
        score.Parent = leaderstats

        -- Create a hidden stats folder for health tracking
        local stats = Instance.new("Folder")
        stats.Name = "PlayerStats"
        stats.Parent = player

        local maxHealth = Instance.new("IntValue")
        maxHealth.Name = "MaxHealth"
        maxHealth.Value = 100
        maxHealth.Parent = stats

        -- Give the player some score every 5 seconds (for testing)
        task.spawn(function()
            while player.Parent do
                task.wait(5)
                score.Value = score.Value + 10
            end
        end)
    end)
end

Players.PlayerAdded:Connect(setupPlayer)

-- Handle players already in the game (for Studio testing)
for _, player in ipairs(Players:GetPlayers()) do
    task.spawn(setupPlayer, player)
end
```

- Now create a LocalScript inside GameHUD (the ScreenGui). Rename it `HUDUpdater`:

```lua
-- HUDUpdater LocalScript (inside GameHUD ScreenGui)
-- This script reads game data and updates the GUI labels

local Players = game:GetService("Players")
local player = Players.LocalPlayer

-- Wait for GUI elements to be available
local topBar = script.Parent:WaitForChild("TopBar")
local healthLabel = topBar:WaitForChild("HealthContainer"):WaitForChild("HealthLabel")
local scoreLabel = topBar:WaitForChild("ScoreContainer"):WaitForChild("ScoreLabel")
local timerLabel = topBar:WaitForChild("TimerContainer"):WaitForChild("TimerLabel")

-- Function to update the health display
local function updateHealth()
    local character = player.Character
    if character then
        local humanoid = character:FindFirstChild("Humanoid")
        if humanoid then
            local currentHealth = math.floor(humanoid.Health)
            local maxHealth = humanoid.MaxHealth
            healthLabel.Text = "Health: " .. currentHealth .. "/" .. maxHealth

            -- Change colour based on health percentage
            local healthPercent = humanoid.Health / humanoid.MaxHealth
            if healthPercent > 0.6 then
                healthLabel.TextColor3 = Color3.fromRGB(85, 255, 85) -- Green
            elseif healthPercent > 0.3 then
                healthLabel.TextColor3 = Color3.fromRGB(255, 255, 85) -- Yellow
            else
                healthLabel.TextColor3 = Color3.fromRGB(255, 85, 85) -- Red
            end
        end
    end
end

-- Function to update the score display
local function updateScore()
    local leaderstats = player:FindFirstChild("leaderstats")
    if leaderstats then
        local score = leaderstats:FindFirstChild("Score")
        if score then
            scoreLabel.Text = "Score: " .. score.Value
        end
    end
end

-- Connect health updates when character loads
local function onCharacterAdded(character)
    local humanoid = character:WaitForChild("Humanoid")
    humanoid.HealthChanged:Connect(updateHealth)
    updateHealth() -- Update immediately
end

-- Connect character events
if player.Character then
    onCharacterAdded(player.Character)
end
player.CharacterAdded:Connect(onCharacterAdded)

-- Connect score updates
local function connectScore()
    local leaderstats = player:WaitForChild("leaderstats")
    local score = leaderstats:WaitForChild("Score")
    score.Changed:Connect(updateScore)
    updateScore() -- Update immediately
end

task.spawn(connectScore)

-- Timer countdown (runs locally for display)
local gameTime = 300 -- 5 minutes in seconds

task.spawn(function()
    while gameTime > 0 do
        local minutes = math.floor(gameTime / 60)
        local seconds = gameTime % 60
        timerLabel.Text = string.format("Time: %d:%02d", minutes, seconds)
        task.wait(1)
        gameTime = gameTime - 1
    end
    timerLabel.Text = "Time: 0:00"
    timerLabel.TextColor3 = Color3.fromRGB(255, 85, 85)
end)
```

- Walk through the code line by line. Emphasise:
  - `WaitForChild` ensures the element has loaded before we try to access it.
  - `HealthChanged` is an event on the Humanoid that fires whenever health changes.
  - `Changed` on an IntValue fires whenever the value is updated.
  - `string.format` with `%d:%02d` formats the timer with leading zeros.
- Students type the code into their own projects. Circulate and help with common errors (typos in element names, incorrect parent hierarchy).
- Have students playtest (F5) to see health, score, and timer updating live.

**60-75 min: Extension — Interactive Buttons and Health Bar**

- Challenge students to add a visual health bar (a coloured Frame that shrinks as health decreases):

```lua
-- Add this to the HUDUpdater LocalScript
-- Create a visual health bar below the TopBar

local healthBarBackground = Instance.new("Frame")
healthBarBackground.Name = "HealthBarBackground"
healthBarBackground.AnchorPoint = Vector2.new(0.5, 0)
healthBarBackground.Position = UDim2.new(0.5, 0, 0, 70)
healthBarBackground.Size = UDim2.new(0.3, 0, 0, 20)
healthBarBackground.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
healthBarBackground.BorderSizePixel = 0
healthBarBackground.Parent = script.Parent

local healthBarCorner = Instance.new("UICorner")
healthBarCorner.CornerRadius = UDim.new(0, 6)
healthBarCorner.Parent = healthBarBackground

local healthBarFill = Instance.new("Frame")
healthBarFill.Name = "HealthBarFill"
healthBarFill.Size = UDim2.new(1, 0, 1, 0)
healthBarFill.BackgroundColor3 = Color3.fromRGB(85, 255, 85)
healthBarFill.BorderSizePixel = 0
healthBarFill.Parent = healthBarBackground

local healthFillCorner = Instance.new("UICorner")
healthFillCorner.CornerRadius = UDim.new(0, 6)
healthFillCorner.Parent = healthBarFill

-- Function to update the visual health bar
local function updateHealthBar()
    local character = player.Character
    if character then
        local humanoid = character:FindFirstChild("Humanoid")
        if humanoid then
            local healthPercent = humanoid.Health / humanoid.MaxHealth
            healthBarFill.Size = UDim2.new(healthPercent, 0, 1, 0)

            -- Change bar colour based on health
            if healthPercent > 0.6 then
                healthBarFill.BackgroundColor3 = Color3.fromRGB(85, 255, 85)
            elseif healthPercent > 0.3 then
                healthBarFill.BackgroundColor3 = Color3.fromRGB(255, 255, 85)
            else
                healthBarFill.BackgroundColor3 = Color3.fromRGB(255, 85, 85)
            end
        end
    end
end

-- Connect the health bar to the Humanoid
local function connectHealthBar(character)
    local humanoid = character:WaitForChild("Humanoid")
    humanoid.HealthChanged:Connect(updateHealthBar)
    updateHealthBar()
end

if player.Character then
    connectHealthBar(player.Character)
end
player.CharacterAdded:Connect(connectHealthBar)
```

- Students who finish early can add a TextButton that, when clicked, toggles visibility of the HUD:

```lua
-- Add a menu toggle button
local menuButton = Instance.new("TextButton")
menuButton.Name = "MenuButton"
menuButton.AnchorPoint = Vector2.new(1, 0)
menuButton.Position = UDim2.new(1, -10, 0, 10)
menuButton.Size = UDim2.new(0, 80, 0, 35)
menuButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
menuButton.BackgroundTransparency = 0.3
menuButton.Text = "Menu"
menuButton.TextColor3 = Color3.fromRGB(255, 255, 255)
menuButton.Font = Enum.Font.GothamBold
menuButton.TextScaled = true
menuButton.Parent = script.Parent

local menuCorner = Instance.new("UICorner")
menuCorner.CornerRadius = UDim.new(0, 8)
menuCorner.Parent = menuButton

menuButton.MouseButton1Click:Connect(function()
    topBar.Visible = not topBar.Visible
end)
```

**75-85 min: Sharing and Discussion**

- Ask three students to share their HUD designs. Display on the projector.
- For each, ask the class: *"What works well about this GUI? What would you improve?"*
- Discuss common GUI design principles:
  - *"Keep it minimal — only show information the player needs right now."*
  - *"Use consistent colours — red for danger, green for positive, white for neutral."*
  - *"Position important information where the eye naturally goes — top corners, bottom centre."*
- Ask: *"What happens if we use too much of the screen for GUI?"* Guide to: *"The player cannot see the game world. The best GUI is nearly invisible until you need it."*

**85-90 min: Closure and Preview**

- Quick check: *"Raise your hand if your HUD updates health in real time. Keep it up if your score also updates. Keep it up if your timer counts down."*
- Preview Session 18: *"Your game now talks to the player through visuals. Next session, we add the second sense — sound. Background music, sound effects, and audio feedback that make your game feel alive."*
- Remind students to save their project.

##### Differentiation

**Support:**
- Provide a pre-built ScreenGui template with the Frame hierarchy already set up, so struggling students focus on scripting rather than manual GUI construction.
- Offer a properties cheat sheet listing the exact property names and values for each GUI element, reducing the chance of typos.
- Pair students who struggle with the scripting portion with a confident partner; the stronger student explains each line while the other types.

**Extension:**
- Challenge advanced students to create an animated GUI — for example, a health bar that smoothly tweens to its new size using `TweenService` instead of snapping instantly.
- Ask them to add an ImageLabel displaying a custom icon next to each stat (heart icon for health, star icon for score, clock icon for timer).
- Have them research `SizeConstraint` and `AspectRatioConstraint` to make their GUI fully responsive across different screen sizes.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| GUI hierarchy understanding | Cannot explain or create GUI structure | Creates ScreenGui but places elements without proper nesting | Correctly nests ScreenGui > Frame > Labels with proper hierarchy | Explains hierarchy, demonstrates parent-child positioning, and uses layout objects |
| HUD creation | No GUI elements created | Creates 1-2 GUI elements with incorrect sizing or positioning | Creates health, score, and timer displays with proper styling | Creates polished HUD with UICorner, UIPadding, UIListLayout, and responsive sizing |
| Script-GUI connection | No script or script does not reference GUI | Script references GUI elements but does not update them dynamically | Script updates GUI from game data using events | Script handles all edge cases (nil checks, CharacterAdded, colour changes) |
| Visual design quality | GUI is unstyled default appearance | Some styling applied inconsistently | Consistent colour scheme, readable fonts, proper transparency | Professional appearance with rounded corners, colour-coded feedback, responsive layout |

##### Teacher Notes

- The most common error is mismatched names between the Explorer hierarchy and the script's `WaitForChild` calls. If a student names a Frame "healthcontainer" but the script looks for "HealthContainer", it will hang forever on `WaitForChild`. Emphasise exact capitalisation.
- `ResetOnSpawn` on the ScreenGui is critical. If left as `true` (the default), the GUI will be destroyed and recreated every time the player dies and respawns, which can break script references. Set it to `false` for persistent HUDs.
- UDim2 notation can confuse students. Simplify it as: `UDim2.new(scaleX, offsetX, scaleY, offsetY)`. Scale is 0 to 1 (percentage), Offset is pixels. Most students find it easier to start with offset values and introduce scale later.
- When students playtest with F5, the GUI appears on the player's screen. If they use F6 (Run without player), the GUI will not appear because there is no local player. Always use F5 for GUI testing.
- Some students may try to modify GUI elements from a server Script. Clarify: GUI updates should happen in LocalScripts (client-side), while game data (scores, health) can be managed on the server and replicated to the client.

---

#### SESSION 17 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 17: GUI Design — ScreenGui, Frames, and Labels**

---

##### Part 1: GUI Hierarchy Matching

**Instructions:** The Roblox GUI system uses a specific hierarchy. Match each GUI element (left) to its correct description (right). Write the correct letter in the blank.

| GUI Element | | Description |
|-------------|---|-------------|
| 1. `ScreenGui` | ____ | A. Displays an image or icon on the screen. Cannot be clicked. |
| 2. `Frame` | ____ | B. The top-level container for all 2D GUI elements, covers the entire screen. |
| 3. `TextLabel` | ____ | C. A rectangle that groups other GUI elements and provides background styling. |
| 4. `TextButton` | ____ | D. Automatically arranges child elements in a row or column. |
| 5. `ImageLabel` | ____ | E. Displays text that the player can read but cannot interact with. |
| 6. `UIListLayout` | ____ | F. Adds rounded corners to a Frame or button. |
| 7. `UICorner` | ____ | G. Displays text and fires an event when the player clicks it. |
| 8. `UIPadding` | ____ | H. Adds space between a Frame's edge and its child elements. |

**Answers:** 1.____ 2.____ 3.____ 4.____ 5.____ 6.____ 7.____ 8.____

---

##### Part 2: Build Your HUD — Step-by-Step

**Instructions:** Follow each step to build a game HUD. Tick each box as you complete the step.

**Part A: Setting Up the Structure**

1. [ ] In StarterGui, insert a **ScreenGui**. Rename it `GameHUD`.
2. [ ] Set `ResetOnSpawn` to `false` in the Properties panel.
3. [ ] Inside GameHUD, insert a **Frame**. Rename it `TopBar`.
4. [ ] Set TopBar properties:
   - AnchorPoint = `0.5, 0`
   - Position = `{0.5, 0, 0, 10}`
   - Size = `{0.6, 0, 0, 50}`
   - BackgroundColor3 = `0, 0, 0`
   - BackgroundTransparency = `0.3`
   - BorderSizePixel = `0`
5. [ ] Inside TopBar, add a **UICorner**. Set CornerRadius to `{0, 12}`.
6. [ ] Inside TopBar, add a **UIPadding**. Set all paddings to `{0, 8}`.
7. [ ] Inside TopBar, add a **UIListLayout**. Set FillDirection to `Horizontal`, Padding to `{0, 20}`.

**Part B: Adding Display Elements**

8. [ ] Inside TopBar, add a **Frame**. Rename it `HealthContainer`. Size = `{0, 150, 1, 0}`. BackgroundTransparency = `1`.
9. [ ] Inside HealthContainer, add a **TextLabel**. Rename it `HealthLabel`. Set Text = `"Health: 100"`, TextColor3 = red, Font = GothamBold, TextScaled = true, BackgroundTransparency = 1.
10. [ ] Inside TopBar, add another **Frame**. Rename it `ScoreContainer`. Same settings as HealthContainer.
11. [ ] Inside ScoreContainer, add a **TextLabel**. Rename it `ScoreLabel`. Set Text = `"Score: 0"`, TextColor3 = yellow.
12. [ ] Inside TopBar, add a third **Frame**. Rename it `TimerContainer`. Same settings.
13. [ ] Inside TimerContainer, add a **TextLabel**. Rename it `TimerLabel`. Set Text = `"Time: 5:00"`, TextColor3 = white.

**Does your hierarchy look like this?**
```
StarterGui
└── GameHUD (ScreenGui)
    └── TopBar (Frame)
        ├── UICorner
        ├── UIPadding
        ├── UIListLayout
        ├── HealthContainer (Frame)
        │   └── HealthLabel (TextLabel)
        ├── ScoreContainer (Frame)
        │   └── ScoreLabel (TextLabel)
        └── TimerContainer (Frame)
            └── TimerLabel (TextLabel)
```

[ ] Yes — Excellent! [ ] No — Fix the hierarchy before continuing.

14. [ ] Press **F5** to playtest. Can you see the HUD at the top of the screen? [ ] Yes [ ] No

---

##### Part 3: Scripting the HUD

**Instructions:** Now connect your HUD to game data with scripts.

**Challenge A: Game Manager Script**

15. [ ] In **ServerScriptService**, insert a **Script**. Rename it `GameManager`.
16. [ ] Type the following code:

```lua
local Players = game:GetService("Players")

local function setupPlayer(player)
    player.CharacterAdded:Connect(function(character)
        local leaderstats = Instance.new("Folder")
        leaderstats.Name = "leaderstats"
        leaderstats.Parent = player

        local score = Instance.new("IntValue")
        score.Name = "Score"
        score.Value = 0
        score.Parent = leaderstats

        -- Give score every 5 seconds for testing
        task.spawn(function()
            while player.Parent do
                task.wait(5)
                score.Value = score.Value + 10
            end
        end)
    end)
end

Players.PlayerAdded:Connect(setupPlayer)
```

**Question:** What does `player.CharacterAdded:Connect(function(character)` do?

> _______________________________________________________________________________

**Challenge B: HUD Updater LocalScript**

17. [ ] Inside your `GameHUD` ScreenGui, insert a **LocalScript**. Rename it `HUDUpdater`.
18. [ ] Type the following code:

```lua
local Players = game:GetService("Players")
local player = Players.LocalPlayer

local topBar = script.Parent:WaitForChild("TopBar")
local healthLabel = topBar:WaitForChild("HealthContainer"):WaitForChild("HealthLabel")
local scoreLabel = topBar:WaitForChild("ScoreContainer"):WaitForChild("ScoreLabel")
local timerLabel = topBar:WaitForChild("TimerContainer"):WaitForChild("TimerLabel")

-- Update health display
local function updateHealth()
    local character = player.Character
    if character then
        local humanoid = character:FindFirstChild("Humanoid")
        if humanoid then
            local currentHealth = math.floor(humanoid.Health)
            healthLabel.Text = "Health: " .. currentHealth .. "/" .. humanoid.MaxHealth

            local healthPercent = humanoid.Health / humanoid.MaxHealth
            if healthPercent > 0.6 then
                healthLabel.TextColor3 = Color3.fromRGB(85, 255, 85)
            elseif healthPercent > 0.3 then
                healthLabel.TextColor3 = Color3.fromRGB(255, 255, 85)
            else
                healthLabel.TextColor3 = Color3.fromRGB(255, 85, 85)
            end
        end
    end
end

-- Update score display
local function updateScore()
    local leaderstats = player:FindFirstChild("leaderstats")
    if leaderstats then
        local score = leaderstats:FindFirstChild("Score")
        if score then
            scoreLabel.Text = "Score: " .. score.Value
        end
    end
end

-- Connect health updates
local function onCharacterAdded(character)
    local humanoid = character:WaitForChild("Humanoid")
    humanoid.HealthChanged:Connect(updateHealth)
    updateHealth()
end

if player.Character then
    onCharacterAdded(player.Character)
end
player.CharacterAdded:Connect(onCharacterAdded)

-- Connect score updates
task.spawn(function()
    local leaderstats = player:WaitForChild("leaderstats")
    local score = leaderstats:WaitForChild("Score")
    score.Changed:Connect(updateScore)
    updateScore()
end)

-- Timer countdown
local gameTime = 300
task.spawn(function()
    while gameTime > 0 do
        local minutes = math.floor(gameTime / 60)
        local seconds = gameTime % 60
        timerLabel.Text = string.format("Time: %d:%02d", minutes, seconds)
        task.wait(1)
        gameTime = gameTime - 1
    end
    timerLabel.Text = "Time: 0:00"
end)
```

19. [ ] Press **F5** to playtest. Verify:
   - [ ] Health display shows your current health
   - [ ] Score increases by 10 every 5 seconds
   - [ ] Timer counts down from 5:00

**Question:** Why do we use `WaitForChild` instead of `FindFirstChild` when getting GUI references at the start of the script?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 4: UDim2 Practice

**Instructions:** UDim2 values control position and size. Fill in the blanks.

`UDim2.new(scaleX, offsetX, scaleY, offsetY)`

| Description | UDim2 Value |
|-------------|-------------|
| 200 pixels wide, 50 pixels tall | `UDim2.new(0, ____, 0, ____)` |
| Full width of parent, 100 pixels tall | `UDim2.new(____, 0, 0, ____)` |
| Half the parent width, half the parent height | `UDim2.new(____, 0, ____, 0)` |
| Centred horizontally (with AnchorPoint 0.5, 0) | Position: `UDim2.new(____, 0, 0, 10)` |
| Bottom-right corner (with AnchorPoint 1, 1) | Position: `UDim2.new(____, 0, ____, 0)` |

---

##### Part 5: Bonus Challenge — Visual Health Bar

**Instructions:** Add a visual health bar that fills and empties based on your health. Add this code to your HUDUpdater LocalScript:

```lua
-- Create a health bar background
local healthBarBG = Instance.new("Frame")
healthBarBG.Name = "HealthBarBackground"
healthBarBG.AnchorPoint = Vector2.new(0.5, 0)
healthBarBG.Position = UDim2.new(0.5, 0, 0, 70)
healthBarBG.Size = UDim2.new(0.3, 0, 0, 20)
healthBarBG.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
healthBarBG.BorderSizePixel = 0
healthBarBG.Parent = script.Parent

local bgCorner = Instance.new("UICorner")
bgCorner.CornerRadius = UDim.new(0, 6)
bgCorner.Parent = healthBarBG

-- Create the fill bar
local healthBarFill = Instance.new("Frame")
healthBarFill.Name = "HealthBarFill"
healthBarFill.Size = UDim2.new(1, 0, 1, 0)
healthBarFill.BackgroundColor3 = Color3.fromRGB(85, 255, 85)
healthBarFill.BorderSizePixel = 0
healthBarFill.Parent = healthBarBG

local fillCorner = Instance.new("UICorner")
fillCorner.CornerRadius = UDim.new(0, 6)
fillCorner.Parent = healthBarFill

-- Update the bar when health changes
local function updateHealthBar()
    local character = player.Character
    if character then
        local humanoid = character:FindFirstChild("Humanoid")
        if humanoid then
            local percent = humanoid.Health / humanoid.MaxHealth
            healthBarFill.Size = UDim2.new(percent, 0, 1, 0)
        end
    end
end

local function connectBar(character)
    local humanoid = character:WaitForChild("Humanoid")
    humanoid.HealthChanged:Connect(updateHealthBar)
    updateHealthBar()
end

if player.Character then connectBar(player.Character) end
player.CharacterAdded:Connect(connectBar)
```

Did the health bar appear and respond to damage? [ ] Yes [ ] No

---

##### Reflection

1. Why is it important for GUI elements to update automatically (through events like `HealthChanged`) rather than checking values every frame?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. If you were designing a GUI for a mobile game (small screen, touch input), what would you change about your HUD design?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

### Session 18: SoundService & Audio Implementation

---

#### SESSION 18 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 18 of 24 |
| **Title** | SoundService & Audio Implementation |
| **Unit** | Unit 5: Multiplayer Systems & Game Polish |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Explain the role of SoundService in Roblox and describe the difference between 2D sounds (global) and 3D sounds (positional, attached to parts).
2. Add Sound objects to parts and GUI elements, configuring properties such as SoundId, Volume, PlaybackSpeed, Looped, and RollOffMaxDistance.
3. Write Luau scripts that play sounds in response to game events, including footsteps on movement, collection sounds on item pickup, UI click sounds, and background music on game start.
4. Organise audio using SoundGroups to control volume categories (music, SFX, UI) independently, creating a structured audio system.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project from Session 17 with working HUD
- Projector or screen-share software for teacher demonstrations
- Session 18 Worksheet (printed or displayed digitally)
- A list of free Roblox audio asset IDs (teacher prepares 8-10 sound IDs from the Roblox audio library)
- Headphones for each student (strongly recommended to avoid classroom noise chaos)
- Whiteboard for diagramming sound placement

##### Procedure

**0-5 min: Warm-Up — "Close Your Eyes and Listen"**

- Say: *"Everyone close your eyes for 30 seconds. I want you to listen to the sounds around you right now."*
- After 30 seconds: *"Open your eyes. What did you hear?"* Take responses: air conditioning, typing, footsteps, chairs moving, someone talking.
- Say: *"Now think about a game. Close your eyes again and imagine playing your favourite game. What sounds do you hear?"*
- After 30 seconds, take responses: music, footsteps, sword sounds, explosions, menu clicks, ambient wind, character voices.
- Say: *"Sound is half the experience of a game. Turn off the sound in any game and it immediately feels wrong — lifeless. Today we add life to your game."*

**5-15 min: Introduction — SoundService and Sound Objects**

- Open Roblox Studio. Navigate to SoundService in the Explorer panel (it is under the game icon at the top level).
- Say: *"SoundService is the manager of all audio in your game. It controls global settings like ambient reverb and distance attenuation. But the actual sounds live as Sound objects — and WHERE you put them determines HOW they behave."*
- Explain the two types of sounds:
  1. **2D Sound (Global)** — placed inside SoundService, Workspace, or a GUI element. Plays at the same volume regardless of the player's position. *"Use this for background music, UI clicks, and announcements."*
  2. **3D Sound (Positional)** — placed inside a Part or Attachment in the workspace. Volume depends on distance from the player's character. *"Use this for footsteps, waterfalls, machinery, and any sound that should feel like it comes from a specific location."*
- Demonstrate adding a Sound object:
  - Right-click SoundService > Insert Object > Sound. Rename it `BackgroundMusic`.
  - In Properties, set `SoundId` to a Roblox audio ID (e.g., `rbxassetid://1234567890` — use a valid free music ID).
  - Set `Looped` = true, `Volume` = 0.3, `Playing` = true.
  - Press F5 to hear the music playing.
- Show key Sound properties on the board:
  - `SoundId` — the asset ID of the audio file
  - `Volume` — 0 (silent) to 1 (full volume) and above for amplification
  - `PlaybackSpeed` — 1 is normal; 0.5 is half speed; 2 is double speed
  - `Looped` — whether the sound repeats when it ends
  - `Playing` — whether the sound is currently playing
  - `TimePosition` — current playback position in seconds
  - `RollOffMaxDistance` — for 3D sounds, the distance at which the sound becomes inaudible
  - `RollOffMinDistance` — the distance within which the sound plays at full volume

**15-35 min: Guided Practice — Adding Sounds to the Game**

- Guide students through adding multiple types of sounds:

  **Step 1: Background Music**
  - In SoundService, add a Sound. Rename it `BGMusic`. Set properties:
    - `SoundId` = a valid music asset ID
    - `Looped` = true
    - `Volume` = 0.3
  - Create a LocalScript in StarterPlayerScripts. Rename it `MusicPlayer`:

```lua
-- MusicPlayer LocalScript (StarterPlayerScripts)
-- Plays background music when the player joins

local SoundService = game:GetService("SoundService")

local bgMusic = SoundService:WaitForChild("BGMusic")

-- Start playing after a short delay (lets the game load first)
task.wait(2)
bgMusic:Play()

print("Background music started playing")
```

  - Playtest. Music should play after 2 seconds.

  **Step 2: Collectible Sound Effect**
  - In Workspace, create a Part. Rename it `Coin`. Change its shape to a Cylinder, colour it yellow, and make it small (Size = 1, 0.2, 1).
  - Inside the Coin part, add a Sound. Rename it `CollectSound`. Set:
    - `SoundId` = a coin/pickup sound asset ID
    - `Volume` = 0.8
    - `PlaybackSpeed` = 1
  - Add a Script inside the Coin part:

```lua
-- Coin Collection Script (inside the Coin part)
-- Plays a sound and destroys the coin when touched

local coin = script.Parent
local collectSound = coin:WaitForChild("CollectSound")
local debounce = false

coin.Touched:Connect(function(hit)
    if debounce then return end

    local character = hit.Parent
    local humanoid = character:FindFirstChild("Humanoid")

    if humanoid then
        debounce = true

        -- Award points
        local player = game:GetService("Players"):GetPlayerFromCharacter(character)
        if player then
            local leaderstats = player:FindFirstChild("leaderstats")
            if leaderstats then
                local score = leaderstats:FindFirstChild("Score")
                if score then
                    score.Value = score.Value + 25
                end
            end
        end

        -- Play the collection sound
        collectSound:Play()

        -- Hide the coin while the sound plays
        coin.Transparency = 1
        coin.CanCollide = false

        -- Wait for sound to finish, then destroy
        collectSound.Ended:Wait()
        coin:Destroy()
    end
end)
```

  - Playtest. Walk into the coin — hear the sound, see the coin vanish, score increases.

  **Step 3: UI Click Sound**
  - In the GameHUD ScreenGui, add a TextButton. Rename it `TestButton`. Style it with text "Click Me".
  - Inside the TextButton, add a Sound. Rename it `ClickSound`. Set SoundId to a UI click sound.
  - Add a LocalScript inside the TextButton:

```lua
-- UI Click Sound LocalScript (inside the TextButton)

local button = script.Parent
local clickSound = button:WaitForChild("ClickSound")

button.MouseButton1Click:Connect(function()
    clickSound:Play()
    print("Button clicked!")
end)
```

  - Playtest and click the button. The click sound should play.

**35-60 min: Independent Practice — Building an Audio System**

- Students work independently to build a complete audio system for their game. Direct them to Part 2 of the worksheet.

- Challenge students to create a footstep system. Provide the following starter code and have them type it into a LocalScript in StarterCharacterScripts:

```lua
-- Footstep Sound System (LocalScript in StarterCharacterScripts)
-- Plays footstep sounds when the character is walking

local character = script.Parent
local humanoid = character:WaitForChild("Humanoid")
local rootPart = character:WaitForChild("HumanoidRootPart")

-- Create footstep sounds
local footstepSound = Instance.new("Sound")
footstepSound.Name = "Footstep"
footstepSound.SoundId = "rbxassetid://YOUR_FOOTSTEP_SOUND_ID"
footstepSound.Volume = 0.5
footstepSound.PlaybackSpeed = 1
footstepSound.Parent = rootPart

-- Track walking state
local isWalking = false
local stepInterval = 0.4 -- seconds between footsteps

humanoid.Running:Connect(function(speed)
    if speed > 1 then
        if not isWalking then
            isWalking = true
            -- Play footsteps in a loop while walking
            task.spawn(function()
                while isWalking do
                    footstepSound:Play()
                    task.wait(stepInterval)
                end
            end)
        end
    else
        isWalking = false
    end
end)

-- Stop footsteps when jumping
humanoid.Jumping:Connect(function()
    isWalking = false
end)

-- Stop footsteps on death
humanoid.Died:Connect(function()
    isWalking = false
end)

print("Footstep system loaded")
```

- Circulate and assist. Common issues:
  - Students forgetting to replace `YOUR_FOOTSTEP_SOUND_ID` with an actual asset ID.
  - Sound not playing because the Sound object is not parented correctly.
  - Footsteps continuing after death (check the Died connection).

**60-75 min: Extension — SoundGroups and Volume Control**

- Introduce SoundGroups for organised volume control:

```lua
-- SoundGroup Setup Script (ServerScriptService)
-- Creates organised sound groups for volume control

local SoundService = game:GetService("SoundService")

-- Create SoundGroups if they don't exist
local function createSoundGroup(name, defaultVolume)
    local group = Instance.new("SoundGroup")
    group.Name = name
    group.Volume = defaultVolume
    group.Parent = SoundService
    return group
end

local musicGroup = createSoundGroup("MusicGroup", 0.5)
local sfxGroup = createSoundGroup("SFXGroup", 0.8)
local uiGroup = createSoundGroup("UIGroup", 1.0)

print("Sound groups created: Music, SFX, UI")
```

- Show students how to assign sounds to groups by setting the `SoundGroup` property of each Sound object.

- Challenge advanced students to build a volume settings GUI:

```lua
-- Volume Settings GUI (LocalScript inside a ScreenGui)
-- Creates buttons for adjusting Music, SFX, and UI volume

local SoundService = game:GetService("SoundService")
local player = game:GetService("Players").LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")

-- Create the settings frame
local settingsGui = Instance.new("ScreenGui")
settingsGui.Name = "VolumeSettings"
settingsGui.Parent = playerGui

local settingsFrame = Instance.new("Frame")
settingsFrame.Name = "SettingsFrame"
settingsFrame.AnchorPoint = Vector2.new(0.5, 0.5)
settingsFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
settingsFrame.Size = UDim2.new(0, 300, 0, 250)
settingsFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
settingsFrame.BackgroundTransparency = 0.1
settingsFrame.Visible = false
settingsFrame.Parent = settingsGui

local settingsCorner = Instance.new("UICorner")
settingsCorner.CornerRadius = UDim.new(0, 12)
settingsCorner.Parent = settingsFrame

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 40)
title.BackgroundTransparency = 1
title.Text = "Volume Settings"
title.TextColor3 = Color3.fromRGB(255, 255, 255)
title.Font = Enum.Font.GothamBold
title.TextScaled = true
title.Parent = settingsFrame

-- Create a volume control row
local function createVolumeControl(name, yPosition, soundGroupName)
    local label = Instance.new("TextLabel")
    label.Position = UDim2.new(0.05, 0, 0, yPosition)
    label.Size = UDim2.new(0.3, 0, 0, 30)
    label.BackgroundTransparency = 1
    label.Text = name
    label.TextColor3 = Color3.fromRGB(200, 200, 200)
    label.Font = Enum.Font.Gotham
    label.TextScaled = true
    label.TextXAlignment = Enum.TextXAlignment.Left
    label.Parent = settingsFrame

    local downButton = Instance.new("TextButton")
    downButton.Position = UDim2.new(0.4, 0, 0, yPosition)
    downButton.Size = UDim2.new(0, 30, 0, 30)
    downButton.Text = "-"
    downButton.TextColor3 = Color3.fromRGB(255, 255, 255)
    downButton.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
    downButton.Font = Enum.Font.GothamBold
    downButton.TextScaled = true
    downButton.Parent = settingsFrame

    local volumeDisplay = Instance.new("TextLabel")
    volumeDisplay.Position = UDim2.new(0.55, 0, 0, yPosition)
    volumeDisplay.Size = UDim2.new(0.2, 0, 0, 30)
    volumeDisplay.BackgroundTransparency = 1
    volumeDisplay.Text = "100%"
    volumeDisplay.TextColor3 = Color3.fromRGB(255, 255, 255)
    volumeDisplay.Font = Enum.Font.Gotham
    volumeDisplay.TextScaled = true
    volumeDisplay.Parent = settingsFrame

    local upButton = Instance.new("TextButton")
    upButton.Position = UDim2.new(0.8, 0, 0, yPosition)
    upButton.Size = UDim2.new(0, 30, 0, 30)
    upButton.Text = "+"
    upButton.TextColor3 = Color3.fromRGB(255, 255, 255)
    upButton.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
    upButton.Font = Enum.Font.GothamBold
    upButton.TextScaled = true
    upButton.Parent = settingsFrame

    local currentVolume = 1.0

    downButton.MouseButton1Click:Connect(function()
        currentVolume = math.max(0, currentVolume - 0.1)
        volumeDisplay.Text = math.floor(currentVolume * 100) .. "%"
        local soundGroup = SoundService:FindFirstChild(soundGroupName)
        if soundGroup then
            soundGroup.Volume = currentVolume
        end
    end)

    upButton.MouseButton1Click:Connect(function()
        currentVolume = math.min(1, currentVolume + 0.1)
        volumeDisplay.Text = math.floor(currentVolume * 100) .. "%"
        local soundGroup = SoundService:FindFirstChild(soundGroupName)
        if soundGroup then
            soundGroup.Volume = currentVolume
        end
    end)
end

createVolumeControl("Music", 60, "MusicGroup")
createVolumeControl("SFX", 110, "SFXGroup")
createVolumeControl("UI", 160, "UIGroup")
```

**75-85 min: Sharing and Discussion**

- Have three students playtest each other's games with headphones, focusing on the audio experience.
- Each reviewer answers: *"What sounds did you hear? What moment felt the most immersive? What sound is missing that would make the game better?"*
- Class discussion on audio best practices:
  - *"Background music should be quiet enough not to overpower sound effects."*
  - *"Every player action should have audio feedback — clicks, jumps, collections."*
  - *"Sudden loud sounds are jarring. Use volume levels carefully."*
  - *"3D sounds create a sense of space. A waterfall that gets louder as you approach is far more immersive than a flat sound."*

**85-90 min: Closure and Preview**

- Quick check: *"Thumbs up if you have background music playing. Keep it up if you have at least one sound effect. Keep it up if your sounds play at the right time based on game events."*
- Preview Session 19: *"Your game now looks good and sounds good. Next session, we make it social — Teams, multiplayer scoring, and round-based game modes."*
- Remind students to save.

##### Differentiation

**Support:**
- Provide a printed list of 10 valid Roblox audio asset IDs with descriptions (e.g., "coin collect," "footstep grass," "UI click," "epic background music") so students do not need to search the audio library.
- Pre-build the coin collectible with its Sound object and script, so struggling students can study the working example before creating their own sounds.
- Simplify the footstep system by removing the speed-based logic and using a basic `Humanoid.Running` check without the spawn loop.

**Extension:**
- Challenge advanced students to create material-based footsteps that change sound depending on the floor material (e.g., different sounds for grass, concrete, and wood) using `Humanoid.FloorMaterial`.
- Ask them to implement a music playlist system that plays multiple tracks in sequence, with crossfading between tracks using `TweenService` on the Volume property.
- Have them research `SoundEffect` objects (EqualizerSoundEffect, ReverbSoundEffect) and apply one to their background music.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Sound placement understanding | Cannot explain where to place sounds | Places sounds but in incorrect locations (e.g., 3D sound for music) | Correctly places 2D sounds for music/UI and 3D sounds for world objects | Explains the reasoning behind placement and configures RollOff distances |
| Background music | No music implemented | Music added but does not loop or has incorrect volume | Looping background music at appropriate volume | Music with SoundGroup, volume control, and smooth start |
| Sound effects | No sound effects | 1 sound effect that sometimes works | Multiple sound effects triggered by events (touch, click, movement) | Sound effects for all major interactions with debounce and cleanup |
| Audio organisation | Sounds scattered with no organisation | Some sounds named correctly | All sounds named descriptively and placed logically | Sounds organised into SoundGroups with independent volume control |

##### Teacher Notes

- Audio asset IDs from the Roblox library require that the audio be owned by the game creator or be a publicly available sound. Since March 2022, Roblox restricted audio access. Ensure students use audio they have uploaded or audio from the Roblox default library. Teacher should prepare a list of working asset IDs before the session.
- Headphones are strongly recommended. Without them, 25 students playing different sounds simultaneously creates chaos. If headphones are unavailable, have students work at low volume and mute when not actively testing.
- The footstep system uses `task.spawn` to run a loop concurrently. This is a good opportunity to briefly explain concurrent programming: *"task.spawn starts a new thread — the rest of the script keeps running while the footstep loop does its job."*
- Some students may experience audio delay when playtesting. Explain that sounds need to load from Roblox servers; using `ContentProvider:PreloadAsync()` can preload sounds before they are needed.
- The `Ended:Wait()` pattern in the coin script is important — it prevents the part from being destroyed before the sound finishes playing. Without it, the sound would cut off abruptly.

---

#### SESSION 18 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 18: SoundService & Audio Implementation**

---

##### Part 1: Sound Concepts

**Instructions:** Answer each question about Roblox audio.

**1.** What is the difference between a 2D sound and a 3D sound in Roblox?

> 2D sound: _______________________________________________________________________________
>
> 3D sound: _______________________________________________________________________________

**2.** Where should you place a Sound object for background music?

> _______________________________________________________________________________

**3.** Where should you place a Sound object for a waterfall in the game world?

> _______________________________________________________________________________

**4.** Match each Sound property to its purpose:

| Property | | Purpose |
|----------|---|---------|
| 1. `SoundId` | ____ | A. Controls whether the sound repeats after ending |
| 2. `Volume` | ____ | B. The Roblox asset ID of the audio file |
| 3. `PlaybackSpeed` | ____ | C. The distance at which a 3D sound becomes inaudible |
| 4. `Looped` | ____ | D. Controls loudness from 0 (silent) to 1+ (amplified) |
| 5. `RollOffMaxDistance` | ____ | E. Changes the speed and pitch of playback |

**Answers:** 1.____ 2.____ 3.____ 4.____ 5.____

---

##### Part 2: Build Your Audio System

**Instructions:** Add sounds to your game by following each step. Tick each box when complete.

**Challenge A: Background Music**

1. [ ] In **SoundService**, insert a **Sound**. Rename it `BGMusic`.
2. [ ] Set `SoundId` to a music asset ID: `rbxassetid://_______________`
3. [ ] Set `Looped` = true, `Volume` = 0.3.
4. [ ] In **StarterPlayerScripts**, insert a **LocalScript**. Rename it `MusicPlayer`.
5. [ ] Type this code:

```lua
local SoundService = game:GetService("SoundService")
local bgMusic = SoundService:WaitForChild("BGMusic")
task.wait(2)
bgMusic:Play()
```

6. [ ] Press **F5**. Does music play after 2 seconds? [ ] Yes [ ] No

**Challenge B: Collectible Sound**

7. [ ] In **Workspace**, create a Part. Rename it `Coin`. Make it small and yellow.
8. [ ] Inside the Coin, insert a **Sound**. Rename it `CollectSound`. Set a pickup sound ID.
9. [ ] Inside the Coin, insert a **Script**. Type the following:

```lua
local coin = script.Parent
local collectSound = coin:WaitForChild("CollectSound")
local debounce = false

coin.Touched:Connect(function(hit)
    if debounce then return end
    local humanoid = hit.Parent:FindFirstChild("Humanoid")
    if humanoid then
        debounce = true

        local player = game:GetService("Players"):GetPlayerFromCharacter(hit.Parent)
        if player then
            local leaderstats = player:FindFirstChild("leaderstats")
            if leaderstats then
                local score = leaderstats:FindFirstChild("Score")
                if score then
                    score.Value = score.Value + 25
                end
            end
        end

        collectSound:Play()
        coin.Transparency = 1
        coin.CanCollide = false
        collectSound.Ended:Wait()
        coin:Destroy()
    end
end)
```

10. [ ] Press **F5**. Walk into the coin. Does it play a sound, give points, and disappear? [ ] Yes [ ] No

**Question:** Why do we set `debounce = true` before playing the sound?

> _______________________________________________________________________________

**Challenge C: Footstep System**

11. [ ] In **StarterCharacterScripts**, insert a **LocalScript**. Rename it `FootstepSystem`.
12. [ ] Type the following code:

```lua
local character = script.Parent
local humanoid = character:WaitForChild("Humanoid")
local rootPart = character:WaitForChild("HumanoidRootPart")

local footstepSound = Instance.new("Sound")
footstepSound.Name = "Footstep"
footstepSound.SoundId = "rbxassetid://YOUR_FOOTSTEP_ID"
footstepSound.Volume = 0.5
footstepSound.Parent = rootPart

local isWalking = false

humanoid.Running:Connect(function(speed)
    if speed > 1 then
        if not isWalking then
            isWalking = true
            task.spawn(function()
                while isWalking do
                    footstepSound:Play()
                    task.wait(0.4)
                end
            end)
        end
    else
        isWalking = false
    end
end)

humanoid.Died:Connect(function()
    isWalking = false
end)
```

13. [ ] Replace `YOUR_FOOTSTEP_ID` with a real sound asset ID.
14. [ ] Press **F5**. Walk around. Do you hear footsteps? [ ] Yes [ ] No
15. [ ] Stop walking. Do the footsteps stop? [ ] Yes [ ] No

---

##### Part 3: Sound Design Plan

**Instructions:** Plan the complete audio for your game. List every sound your game needs.

| # | Sound Name | Type (2D/3D) | When Does It Play? | Where Is It Placed? |
|---|-----------|-------------|-------------------|-------------------|
| 1 | Background Music | 2D | When game starts | SoundService |
| 2 | Coin Collect | 3D | When player touches coin | Inside Coin part |
| 3 | ________________ | ______ | ________________________ | _________________ |
| 4 | ________________ | ______ | ________________________ | _________________ |
| 5 | ________________ | ______ | ________________________ | _________________ |
| 6 | ________________ | ______ | ________________________ | _________________ |
| 7 | ________________ | ______ | ________________________ | _________________ |
| 8 | ________________ | ______ | ________________________ | _________________ |

---

##### Part 4: Code Reading Challenge

**Instructions:** Read the following code and answer the questions without running it.

```lua
local part = script.Parent
local sound = part:WaitForChild("AlarmSound")
sound.Looped = true
sound.Volume = 0

sound:Play()

for i = 1, 10 do
    sound.Volume = i / 10
    task.wait(0.5)
end

task.wait(5)

for i = 10, 1, -1 do
    sound.Volume = i / 10
    task.wait(0.5)
end

sound:Stop()
```

**Question 1:** What does this script do with the volume over time? Describe the pattern.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

**Question 2:** How long does the sound play at full volume before fading out?

> _______________________________________________________________________________

**Question 3:** What is the total time from when the sound starts to when it stops?

> _______________________________________________________________________________

---

##### Reflection

1. Think about a game you have played that had excellent audio design. What specific sounds made it feel immersive?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Why is it important to use SoundGroups instead of setting volume on each sound individually?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge

Create a "jukebox" system. Place a Part in Workspace, add 3 different Sound objects inside it, and write a script that plays them in sequence — when one song ends, the next one starts automatically. When the last song finishes, loop back to the first.

```lua
-- Jukebox Script (inside a Part with Song1, Song2, Song3)

local part = script.Parent
local songs = {
    part:WaitForChild("Song1"),
    part:WaitForChild("Song2"),
    part:WaitForChild("Song3"),
}

local currentIndex = 1

local function playNext()
    local currentSong = songs[currentIndex]
    currentSong:Play()
    print("Now playing: " .. currentSong.Name)

    currentSong.Ended:Wait()

    currentIndex = currentIndex + 1
    if currentIndex > #songs then
        currentIndex = 1
    end

    playNext()
end

playNext()
```

Did your jukebox cycle through all three songs? [ ] Yes [ ] No

*Save your project! You will use it in Session 19.*

---

### Session 19: Teams, Multiplayer Mechanics & Game Modes

---

#### SESSION 19 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 19 of 24 |
| **Title** | Teams, Multiplayer Mechanics & Game Modes |
| **Unit** | Unit 5: Multiplayer Systems & Game Polish |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Configure the Teams service in Roblox Studio, creating multiple teams with distinct colours and assigning players to teams through scripting.
2. Set up team-specific SpawnLocations so players spawn at their team's designated area, configuring the TeamColor and AllowTeamChangeOnTouch properties correctly.
3. Implement a team-based scoring system with a leaderboard that tracks individual and team scores using leaderstats and server-side logic.
4. Build a round-based game system with countdown timer, round start/end logic, score tracking between rounds, and win condition evaluation.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project from Sessions 17-18 with HUD and audio
- Projector or screen-share software for teacher demonstrations
- Session 19 Worksheet (printed or displayed digitally)
- Whiteboard for diagramming round flow (start > play > end > restart)
- Timer or stopwatch for timed activities

##### Procedure

**0-5 min: Warm-Up — "What Makes a Multiplayer Game Fun?"**

- Ask: *"Think of a multiplayer game you enjoy. What makes playing WITH other people more exciting than playing alone?"*
- Take responses. Common answers: competition, teamwork, surprise (other humans are unpredictable), shared achievements, bragging rights.
- Say: *"All of those things come from systems — teams, scoring, rounds, win conditions. Today we build those systems. By the end of this session, your game will support multiplayer team battles."*

**5-15 min: Introduction — Teams Service and Team Configuration**

- Open Roblox Studio. In the Explorer, look for the Teams service. If it is not visible, click the **+** next to the game root or go to Model > Service > Teams.
- Say: *"The Teams service is built into Roblox. It handles team assignment, team colours, and team-based spawning. We just need to configure it."*
- Demonstrate creating teams:
  - Right-click Teams > Insert Object > Team. Rename it `RedTeam`. Set `TeamColor` to `Bright red`. Set `AutoAssignable` to `true`.
  - Right-click Teams again > Insert Object > Team. Rename it `BlueTeam`. Set `TeamColor` to `Bright blue`. Set `AutoAssignable` to `true`.
  - Say: *"AutoAssignable means Roblox will automatically distribute new players across teams to keep them balanced."*
- Demonstrate SpawnLocation configuration:
  - In Workspace, add two SpawnLocation parts (Insert > SpawnLocation). Rename them `RedSpawn` and `BlueSpawn`.
  - Position them apart (e.g., 100 studs away from each other).
  - Set `RedSpawn.TeamColor` to `Bright red`, `Neutral` to `false`, `AllowTeamChangeOnTouch` to `false`.
  - Set `BlueSpawn.TeamColor` to `Bright blue`, `Neutral` to `false`, `AllowTeamChangeOnTouch` to `false`.
  - Say: *"Now red team players spawn ONLY at the red spawn, and blue team players spawn ONLY at the blue spawn. The TeamColor on the SpawnLocation must match the TeamColor on the Team object exactly."*
- Playtest with two players using the Test tab > Start (2 Players). Show that players are automatically assigned to different teams and spawn at different locations.

**15-35 min: Guided Practice — Team-Based Scoring System**

- Guide students through building a team scoring system:

```lua
-- TeamScoreManager Script (ServerScriptService)
-- Manages team-based scoring and leaderboards

local Players = game:GetService("Players")
local Teams = game:GetService("Teams")

-- Team score tracking
local teamScores = {
    ["RedTeam"] = 0,
    ["BlueTeam"] = 0,
}

-- Create leaderstats for each player
local function setupPlayer(player)
    player.CharacterAdded:Connect(function(character)
        -- Create leaderstats folder
        local leaderstats = Instance.new("Folder")
        leaderstats.Name = "leaderstats"
        leaderstats.Parent = player

        -- Individual score
        local kills = Instance.new("IntValue")
        kills.Name = "Kills"
        kills.Value = 0
        kills.Parent = leaderstats

        local deaths = Instance.new("IntValue")
        deaths.Name = "Deaths"
        deaths.Value = 0
        deaths.Parent = leaderstats

        -- Track deaths
        local humanoid = character:WaitForChild("Humanoid")
        humanoid.Died:Connect(function()
            deaths.Value = deaths.Value + 1

            -- Find who killed this player (check for a tag)
            local creator = humanoid:FindFirstChild("creator")
            if creator and creator.Value then
                local killer = creator.Value
                local killerStats = killer:FindFirstChild("leaderstats")
                if killerStats then
                    local killerKills = killerStats:FindFirstChild("Kills")
                    if killerKills then
                        killerKills.Value = killerKills.Value + 1
                    end
                end

                -- Add to team score
                if killer.Team then
                    local teamName = killer.Team.Name
                    if teamScores[teamName] then
                        teamScores[teamName] = teamScores[teamName] + 1
                    end
                end
            end
        end)
    end)
end

Players.PlayerAdded:Connect(setupPlayer)

-- Function to get team scores (can be called from other scripts)
local function getTeamScores()
    return teamScores
end

-- Display team scores periodically
task.spawn(function()
    while true do
        task.wait(10)
        for teamName, score in pairs(teamScores) do
            print(teamName .. " score: " .. score)
        end
    end
end)
```

- Walk through the code. Explain:
  - `leaderstats` is a special folder name that Roblox automatically displays on the leaderboard (press Tab in-game).
  - The `creator` tag is a common pattern — when a weapon damages a player, it sets a `creator` ObjectValue inside the victim's Humanoid pointing to the attacker.
  - Team scores are stored in a simple table on the server.

- Create a simple damage tool to test the scoring system:

```lua
-- SimpleSword Script (inside a Tool in StarterPack)
-- A basic weapon that deals damage and tags the attacker

local tool = script.Parent
local damage = 25
local debounce = false

local function onTouch(hit)
    if debounce then return end

    local targetCharacter = hit.Parent
    local targetHumanoid = targetCharacter:FindFirstChild("Humanoid")

    if targetHumanoid and targetHumanoid.Health > 0 then
        local attacker = game:GetService("Players"):GetPlayerFromCharacter(tool.Parent)
        local target = game:GetService("Players"):GetPlayerFromCharacter(targetCharacter)

        -- Don't damage teammates
        if attacker and target and attacker.Team == target.Team then
            return
        end

        -- Don't damage yourself
        if attacker and target and attacker == target then
            return
        end

        debounce = true

        -- Tag the attacker as the creator
        local creatorTag = targetHumanoid:FindFirstChild("creator")
        if not creatorTag then
            creatorTag = Instance.new("ObjectValue")
            creatorTag.Name = "creator"
            creatorTag.Parent = targetHumanoid
        end
        creatorTag.Value = attacker

        -- Deal damage
        targetHumanoid:TakeDamage(damage)

        -- Clean up tag after a delay
        task.delay(1, function()
            if creatorTag then
                creatorTag:Destroy()
            end
        end)

        task.wait(0.5)
        debounce = false
    end
end

tool.Activated:Connect(function()
    local handle = tool:FindFirstChild("Handle")
    if handle then
        local connection
        connection = handle.Touched:Connect(function(hit)
            onTouch(hit)
            connection:Disconnect()
        end)

        task.delay(0.5, function()
            if connection then
                connection:Disconnect()
            end
        end)
    end
end)
```

**35-60 min: Independent Practice — Round-Based Game System**

- Students implement a round-based game mode. Guide them through the structure, then let them code independently:

```lua
-- RoundManager Script (ServerScriptService)
-- Manages rounds: intermission > countdown > gameplay > results

local Players = game:GetService("Players")
local Teams = game:GetService("Teams")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

-- Configuration
local INTERMISSION_TIME = 15  -- seconds between rounds
local ROUND_TIME = 120        -- seconds per round
local MIN_PLAYERS = 2         -- minimum players to start a round

-- Create a RemoteEvent for sending round updates to clients
local roundEvent = Instance.new("RemoteEvent")
roundEvent.Name = "RoundUpdate"
roundEvent.Parent = ReplicatedStorage

-- Create a StringValue to track game status (visible to all scripts)
local gameStatus = Instance.new("StringValue")
gameStatus.Name = "GameStatus"
gameStatus.Value = "Waiting"
gameStatus.Parent = ReplicatedStorage

-- Team scores for the current round
local roundScores = {
    ["RedTeam"] = 0,
    ["BlueTeam"] = 0,
}

-- Reset scores for a new round
local function resetRoundScores()
    for teamName, _ in pairs(roundScores) do
        roundScores[teamName] = 0
    end
end

-- Reset all players to full health and teleport to spawns
local function resetPlayers()
    for _, player in ipairs(Players:GetPlayers()) do
        if player.Character then
            local humanoid = player.Character:FindFirstChild("Humanoid")
            if humanoid then
                humanoid.Health = humanoid.MaxHealth
            end
        end

        -- Reset individual kills for the round
        local leaderstats = player:FindFirstChild("leaderstats")
        if leaderstats then
            local kills = leaderstats:FindFirstChild("Kills")
            if kills then
                kills.Value = 0
            end
        end
    end
end

-- Determine the winning team
local function getWinningTeam()
    local bestTeam = nil
    local bestScore = -1

    for teamName, score in pairs(roundScores) do
        if score > bestScore then
            bestScore = score
            bestTeam = teamName
        end
    end

    return bestTeam, bestScore
end

-- Main game loop
local function gameLoop()
    while true do
        -- Phase 1: Waiting for players
        gameStatus.Value = "Waiting for players..."
        roundEvent:FireAllClients("Status", "Waiting for " .. MIN_PLAYERS .. " players...")

        while #Players:GetPlayers() < MIN_PLAYERS do
            task.wait(1)
        end

        -- Phase 2: Intermission
        gameStatus.Value = "Intermission"
        for i = INTERMISSION_TIME, 1, -1 do
            roundEvent:FireAllClients("Status", "Next round in: " .. i .. "s")
            task.wait(1)
        end

        -- Phase 3: Round start
        resetRoundScores()
        resetPlayers()
        gameStatus.Value = "Round in progress"
        roundEvent:FireAllClients("RoundStart", ROUND_TIME)

        -- Phase 4: Round countdown
        for i = ROUND_TIME, 1, -1 do
            roundEvent:FireAllClients("Timer", i)
            task.wait(1)

            -- Check if all players on one team are dead (optional early end)
            if #Players:GetPlayers() < MIN_PLAYERS then
                break
            end
        end

        -- Phase 5: Round end
        gameStatus.Value = "Round over"
        local winningTeam, winScore = getWinningTeam()
        local resultMessage = "Round Over! "

        if winScore == 0 then
            resultMessage = resultMessage .. "No kills -- it is a draw!"
        else
            resultMessage = resultMessage .. winningTeam .. " wins with " .. winScore .. " points!"
        end

        roundEvent:FireAllClients("RoundEnd", resultMessage)

        -- Show results for 5 seconds
        task.wait(5)
    end
end

-- Start the game loop
task.spawn(gameLoop)
```

- Create a client-side script to display round updates on the HUD:

```lua
-- RoundDisplay LocalScript (inside GameHUD ScreenGui)
-- Listens for round updates and displays them on screen

local ReplicatedStorage = game:GetService("ReplicatedStorage")
local roundEvent = ReplicatedStorage:WaitForChild("RoundUpdate")

-- Create a status display
local statusLabel = Instance.new("TextLabel")
statusLabel.Name = "StatusLabel"
statusLabel.AnchorPoint = Vector2.new(0.5, 0)
statusLabel.Position = UDim2.new(0.5, 0, 0, 100)
statusLabel.Size = UDim2.new(0.5, 0, 0, 40)
statusLabel.BackgroundTransparency = 0.5
statusLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
statusLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
statusLabel.Font = Enum.Font.GothamBold
statusLabel.TextScaled = true
statusLabel.Text = "Waiting..."
statusLabel.Parent = script.Parent

local statusCorner = Instance.new("UICorner")
statusCorner.CornerRadius = UDim.new(0, 8)
statusCorner.Parent = statusLabel

-- Handle round events
roundEvent.OnClientEvent:Connect(function(eventType, data)
    if eventType == "Status" then
        statusLabel.Text = data
        statusLabel.TextColor3 = Color3.fromRGB(255, 255, 255)

    elseif eventType == "RoundStart" then
        statusLabel.Text = "ROUND START!"
        statusLabel.TextColor3 = Color3.fromRGB(85, 255, 85)

        task.delay(2, function()
            statusLabel.BackgroundTransparency = 1
            statusLabel.TextTransparency = 1
        end)

    elseif eventType == "Timer" then
        local timeLeft = data
        if timeLeft <= 10 then
            statusLabel.BackgroundTransparency = 0.5
            statusLabel.TextTransparency = 0
            statusLabel.Text = "Time: " .. timeLeft
            statusLabel.TextColor3 = Color3.fromRGB(255, 85, 85)
        end

    elseif eventType == "RoundEnd" then
        statusLabel.BackgroundTransparency = 0.5
        statusLabel.TextTransparency = 0
        statusLabel.Text = data
        statusLabel.TextColor3 = Color3.fromRGB(255, 255, 85)
    end
end)
```

**60-75 min: Extension — Team Score Display GUI**

- Challenge advanced students to add a team score display:

```lua
-- TeamScoreDisplay LocalScript (inside GameHUD ScreenGui)
-- Shows team scores on either side of the screen

local Teams = game:GetService("Teams")
local Players = game:GetService("Players")

-- Create Red Team score display
local redScoreLabel = Instance.new("TextLabel")
redScoreLabel.Name = "RedScore"
redScoreLabel.AnchorPoint = Vector2.new(0, 0)
redScoreLabel.Position = UDim2.new(0, 10, 0, 10)
redScoreLabel.Size = UDim2.new(0, 120, 0, 40)
redScoreLabel.BackgroundColor3 = Color3.fromRGB(200, 50, 50)
redScoreLabel.BackgroundTransparency = 0.3
redScoreLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
redScoreLabel.Font = Enum.Font.GothamBold
redScoreLabel.TextScaled = true
redScoreLabel.Text = "Red: 0"
redScoreLabel.Parent = script.Parent

local redCorner = Instance.new("UICorner")
redCorner.CornerRadius = UDim.new(0, 8)
redCorner.Parent = redScoreLabel

-- Create Blue Team score display
local blueScoreLabel = Instance.new("TextLabel")
blueScoreLabel.Name = "BlueScore"
blueScoreLabel.AnchorPoint = Vector2.new(1, 0)
blueScoreLabel.Position = UDim2.new(1, -10, 0, 10)
blueScoreLabel.Size = UDim2.new(0, 120, 0, 40)
blueScoreLabel.BackgroundColor3 = Color3.fromRGB(50, 50, 200)
blueScoreLabel.BackgroundTransparency = 0.3
blueScoreLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
blueScoreLabel.Font = Enum.Font.GothamBold
blueScoreLabel.TextScaled = true
blueScoreLabel.Text = "Blue: 0"
blueScoreLabel.Parent = script.Parent

local blueCorner = Instance.new("UICorner")
blueCorner.CornerRadius = UDim.new(0, 8)
blueCorner.Parent = blueScoreLabel

-- Update team scores by counting kills from team members
local function updateTeamScores()
    local redTotal = 0
    local blueTotal = 0

    for _, player in ipairs(Players:GetPlayers()) do
        local leaderstats = player:FindFirstChild("leaderstats")
        if leaderstats then
            local kills = leaderstats:FindFirstChild("Kills")
            if kills and player.Team then
                if player.Team.Name == "RedTeam" then
                    redTotal = redTotal + kills.Value
                elseif player.Team.Name == "BlueTeam" then
                    blueTotal = blueTotal + kills.Value
                end
            end
        end
    end

    redScoreLabel.Text = "Red: " .. redTotal
    blueScoreLabel.Text = "Blue: " .. blueTotal
end

-- Update every second
while true do
    updateTeamScores()
    task.wait(1)
end
```

**75-85 min: Sharing and Discussion**

- Have students playtest each other's team games in pairs or small groups.
- Discussion questions:
  - *"Was the round time too short or too long? How would you decide?"*
  - *"What happens if teams are unbalanced (3 vs 1)? How could you fix that?"*
  - *"What other game modes could you build with the same round system?"* (Free-for-all, king of the hill, capture the flag)
- Key takeaway: *"Every multiplayer game is built on the same basic pattern: assign teams, track scores, manage rounds, declare winners. The specific rules change, but the architecture is the same."*

**85-90 min: Closure and Preview**

- Quick check: *"Raise your hand if you have two teams with separate spawn points. Keep it up if your game tracks kills on the leaderboard. Keep it up if you have a round timer."*
- Preview Session 20: *"Your game has features. Next session, we make those features GOOD. Game balancing, playtesting, bug tracking — the difference between a prototype and a polished game."*
- Remind students to save.

##### Differentiation

**Support:**
- Provide the Teams and SpawnLocations pre-configured in a template place file, so struggling students focus on the scripting rather than manual setup.
- Simplify the round system by removing the team scoring component and focusing only on the timer: start round, count down, end round.
- Pair students for playtesting — struggling students can observe how confident students debug multiplayer issues.

**Extension:**
- Challenge advanced students to implement a capture-the-flag mode: place a Part at each team's base, and when a player from the opposing team touches it, they "capture" the flag (Part follows them) and must return to their own base.
- Ask them to add auto-team-balancing: when teams become unbalanced by more than one player, move the most recent joiner to the smaller team.
- Have them implement a spectator mode: when a player dies during a round, they become a ghost (invisible, can fly) until the next round starts.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Teams configuration | Cannot set up Teams service | Creates teams but SpawnLocations are incorrect or missing | Two teams with correct colours and working SpawnLocations | Teams with balanced auto-assignment, correct spawns, and team-colour-coded visuals |
| Scoring system | No scoring implemented | Leaderstats created but kills/deaths not tracked | Full kill/death tracking with leaderboard display | Team scoring with individual stats, team totals, and anti-team-damage logic |
| Round system | No round system | Timer exists but round transitions are broken | Working round loop: intermission, gameplay, results | Smooth round system with client-side display, min-player checks, and clean resets |
| Multiplayer understanding | Cannot explain client-server relationship | Understands server scripts vs local scripts at a basic level | Correctly uses RemoteEvents to communicate round state to clients | Explains why scoring must be server-side and display must be client-side |

##### Teacher Notes

- Testing multiplayer features requires multiple test players. Use the Test tab > Start (2 Players) or Start (4 Players) to simulate. This opens multiple Roblox Studio windows — ensure computers have enough RAM. 8GB minimum recommended for 2-player testing.
- Team colours must match EXACTLY between the Team object and the SpawnLocation. "Bright red" and "Really red" are different BrickColors. This is the number one cause of spawn issues.
- The `creator` tag pattern is the standard Roblox approach for tracking who killed whom. Some students may ask about alternatives — explain that this is the widely accepted convention because it works with Roblox's built-in damage tracking.
- RemoteEvents are used to send data from server to all clients (`FireAllClients`). This is one-way communication. If students need client-to-server communication (e.g., a player requesting to change teams), they will need `FireServer` on the client side and `OnServerEvent` on the server side.
- Round-based systems are complex. If students struggle, focus on getting the timer working first, then add team scoring as a stretch goal. The timer alone is a valuable learning outcome.

---

#### SESSION 19 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 19: Teams, Multiplayer Mechanics & Game Modes**

---

##### Part 1: Teams and Spawns Setup

**Instructions:** Set up a team-based multiplayer system by following each step.

**Part A: Creating Teams**

1. [ ] In the Explorer, find or add the **Teams** service.
2. [ ] Inside Teams, insert a **Team**. Rename it `RedTeam`. Set TeamColor = `Bright red`, AutoAssignable = `true`.
3. [ ] Insert another **Team**. Rename it `BlueTeam`. Set TeamColor = `Bright blue`, AutoAssignable = `true`.

**Part B: Creating Spawn Points**

4. [ ] In Workspace, insert a **SpawnLocation**. Rename it `RedSpawn`.
5. [ ] Set RedSpawn properties: TeamColor = `Bright red`, Neutral = `false`, AllowTeamChangeOnTouch = `false`.
6. [ ] Colour the RedSpawn part red so players can see where it is.
7. [ ] Insert another **SpawnLocation**. Rename it `BlueSpawn`.
8. [ ] Set BlueSpawn properties: TeamColor = `Bright blue`, Neutral = `false`, AllowTeamChangeOnTouch = `false`.
9. [ ] Move the two spawn points at least 100 studs apart.
10. [ ] Press **F5** with the Test tab set to **2 Players**. Do players spawn at different locations? [ ] Yes [ ] No

**Question:** What would happen if you set `Neutral = true` on both SpawnLocations?

> _______________________________________________________________________________

---

##### Part 2: Team Scoring System

**Instructions:** Build a scoring system that tracks kills and deaths per player.

11. [ ] In **ServerScriptService**, insert a **Script**. Rename it `TeamScoreManager`.
12. [ ] Type the following code:

```lua
local Players = game:GetService("Players")

local function setupPlayer(player)
    player.CharacterAdded:Connect(function(character)
        local leaderstats = Instance.new("Folder")
        leaderstats.Name = "leaderstats"
        leaderstats.Parent = player

        local kills = Instance.new("IntValue")
        kills.Name = "Kills"
        kills.Value = 0
        kills.Parent = leaderstats

        local deaths = Instance.new("IntValue")
        deaths.Name = "Deaths"
        deaths.Value = 0
        deaths.Parent = leaderstats

        local humanoid = character:WaitForChild("Humanoid")
        humanoid.Died:Connect(function()
            deaths.Value = deaths.Value + 1

            local creator = humanoid:FindFirstChild("creator")
            if creator and creator.Value then
                local killer = creator.Value
                local killerStats = killer:FindFirstChild("leaderstats")
                if killerStats then
                    local killerKills = killerStats:FindFirstChild("Kills")
                    if killerKills then
                        killerKills.Value = killerKills.Value + 1
                    end
                end
            end
        end)
    end)
end

Players.PlayerAdded:Connect(setupPlayer)
```

13. [ ] Press **F5**. Do you see "Kills" and "Deaths" on the leaderboard (press Tab)? [ ] Yes [ ] No

**Question:** Why do we put the scoring script in **ServerScriptService** instead of in a LocalScript?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 3: Round System

**Instructions:** Build a round-based game system.

14. [ ] In **ReplicatedStorage**, insert a **RemoteEvent**. Rename it `RoundUpdate`.
15. [ ] In **ReplicatedStorage**, insert a **StringValue**. Rename it `GameStatus`. Set Value = `"Waiting"`.
16. [ ] In **ServerScriptService**, insert a **Script**. Rename it `RoundManager`.
17. [ ] Type the round management code (refer to the lesson plan for the full RoundManager script).
18. [ ] In your **GameHUD** ScreenGui, insert a **LocalScript**. Rename it `RoundDisplay`.
19. [ ] Type the client-side display code (refer to the lesson plan for the full RoundDisplay script).
20. [ ] Press **F5** with 2 test players.
   - [ ] Does the intermission countdown appear?
   - [ ] Does "ROUND START!" display when the round begins?
   - [ ] Does the timer show when 10 seconds remain?

---

##### Part 4: Game Mode Design

**Instructions:** Design a game mode for your team game. Answer each question.

**Game Mode Name:** _________________________________

**1. How do players score points?**

> _______________________________________________________________________________

**2. How long does each round last?**

> _______________________________________________________________________________

**3. How does a team win the round?**

> _______________________________________________________________________________

**4. What happens between rounds (intermission)?**

> _______________________________________________________________________________

**5. Are there any special rules (e.g., power-ups, zones, objectives)?**

> _______________________________________________________________________________

**6. Draw a flowchart of your round system:**

```
[Waiting for Players] --> [____________] --> [____________] --> [____________] --> (loop back)
```

---

##### Part 5: Code Prediction

**Instructions:** Read the code and predict what will happen.

```lua
local Teams = game:GetService("Teams")
local Players = game:GetService("Players")

local function countTeamPlayers(teamName)
    local count = 0
    for _, player in ipairs(Players:GetPlayers()) do
        if player.Team and player.Team.Name == teamName then
            count = count + 1
        end
    end
    return count
end

local redCount = countTeamPlayers("RedTeam")
local blueCount = countTeamPlayers("BlueTeam")

if redCount > blueCount + 1 then
    print("Teams are unbalanced! Red has too many players.")
elseif blueCount > redCount + 1 then
    print("Teams are unbalanced! Blue has too many players.")
else
    print("Teams are balanced.")
end
```

**Question 1:** If there are 5 red players and 3 blue players, what will this code print?

> _______________________________________________________________________________

**Question 2:** If there are 4 red players and 4 blue players, what will this code print?

> _______________________________________________________________________________

**Question 3:** What does `+ 1` in the condition check do? Why is it there?

> _______________________________________________________________________________

---

##### Reflection

1. Why is it important to keep scoring logic on the server rather than on the client?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. What is one game mode you would like to build for your capstone project? Describe it in 2-3 sentences.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge

Add team auto-balancing. When a new player joins and one team has 2+ more players than the other, assign them to the smaller team:

```lua
-- Add this to your TeamScoreManager script

local function getSmallestTeam()
    local teams = game:GetService("Teams"):GetTeams()
    local smallestTeam = nil
    local smallestCount = math.huge

    for _, team in ipairs(teams) do
        local playerCount = #team:GetPlayers()
        if playerCount < smallestCount then
            smallestCount = playerCount
            smallestTeam = team
        end
    end

    return smallestTeam
end

Players.PlayerAdded:Connect(function(player)
    local smallest = getSmallestTeam()
    if smallest then
        player.Team = smallest
        print(player.Name .. " assigned to " .. smallest.Name)
    end
end)
```

Did the auto-balancing work when you tested with multiple players? [ ] Yes [ ] No

*Save your project! You will use it in Session 20.*

---

### Session 20: Game Balancing, Playtesting & Quality Assurance

---

#### SESSION 20 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 20 of 24 |
| **Title** | Game Balancing, Playtesting & Quality Assurance |
| **Unit** | Unit 5: Multiplayer Systems & Game Polish |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Define game balance and identify at least four categories of balance issues (damage values, spawn rates, round timing, resource economy) in their own or others' games.
2. Conduct a systematic playtest session using a structured feedback form that captures bugs, balance issues, and player experience observations.
3. Document and categorise bugs using a severity system (critical, major, minor, cosmetic) and create a prioritised bug fix list.
4. Apply at least three performance optimisation techniques (reducing part count, using StreamingEnabled, optimising loops) and explain why each improves game quality.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Project from Sessions 17-19 with GUI, audio, and multiplayer features
- Projector or screen-share software for teacher demonstrations
- Session 20 Worksheet (printed or displayed digitally)
- Printed or digital playtest feedback forms (3 copies per student)
- Whiteboard for group bug tracking board
- Timer for structured playtest sessions
- Optional: sticky notes in four colours (red, orange, yellow, green) for bug severity sorting

##### Procedure

**0-5 min: Warm-Up — "The Worst Bug You Have Ever Seen"**

- Ask: *"Has anyone ever found a hilarious or terrible bug in a game? What happened?"*
- Take 3-4 responses. Students will share stories of falling through floors, infinite money exploits, characters teleporting, or textures breaking.
- Say: *"Every game ships with bugs. The question is not whether bugs exist — it is whether you found and fixed the IMPORTANT ones before players did. That is quality assurance. Today you become QA testers."*

**5-15 min: Introduction — What Is Game Balance?**

- Write "GAME BALANCE" on the board. Define it: *"Game balance means every choice a player can make feels fair and meaningful. No single strategy should be obviously the best. No weapon should be clearly overpowered. No team should have an unfair advantage."*
- Give four categories of balance issues with examples:
  1. **Damage/Health Balance** — *"If a sword does 100 damage and the player has 100 health, the game is a one-hit kill. Is that fun? Maybe for the attacker, but not for the defender."*
  2. **Economy Balance** — *"If coins give 1000 points each but the shop prices are 10 points, the player becomes overpowered in seconds."*
  3. **Timing Balance** — *"If rounds are 10 seconds long, nobody has time to play. If rounds are 30 minutes, players get bored."*
  4. **Spatial Balance** — *"If one team's spawn point is closer to the objective, that team always wins."*
- Show a practical example: open the project from Session 19. Ask: *"In our team game, what values could we change to make the game more balanced?"*
  - Damage per hit (currently 25 — is that right for 100 HP?)
  - Round time (currently 120 seconds — is that too long?)
  - Spawn distance (are teams equally far from each other?)
  - Tool availability (does everyone start with the same tools?)
- Say: *"Balance is not something you guess. You test, measure, and adjust. That brings us to playtesting."*

**15-35 min: Guided Practice — Structured Playtesting**

- Explain the playtesting process:
  1. **Set a goal** — what are you testing? (e.g., "Is the damage balanced?" or "Does the round system work?")
  2. **Play with intention** — do not just play for fun; observe and take notes.
  3. **Record everything** — bugs, frustrations, moments of confusion, moments of delight.
  4. **Categorise findings** — bugs vs balance issues vs feature requests.
  5. **Prioritise** — fix critical bugs first, balance issues second, nice-to-haves last.

- Introduce the bug severity system:
  - **Critical** — game crashes, player cannot play, data loss. Fix immediately.
  - **Major** — feature does not work as intended, significant gameplay impact. Fix before publishing.
  - **Minor** — small issues that do not prevent gameplay but are noticeable. Fix when time allows.
  - **Cosmetic** — visual glitches, typos, minor alignment issues. Fix if time permits.

- Model a playtest: open a student's game (or the demo project) on the projector. Play for 3 minutes. Narrate your observations aloud:
  - *"I spawned at red team spawn — that works. The HUD shows my health — good. I walked to the coin — the sound played but the score did not update. That is a Major bug. I will write it down."*
  - *"The round timer says 2 minutes but the round started before both players spawned. That is a timing issue — Major."*
  - *"The background music is louder than the coin sound. That is a balance issue — Minor."*

- Students pair up. Each pair spends 10 minutes playtesting their partner's game using the structured feedback form from the worksheet:
  - Set a timer for 5 minutes of play.
  - Set a timer for 5 minutes of writing feedback.

- After playtesting, each student shares their top 3 findings with their partner.

**35-60 min: Independent Practice — Bug Fixing and Optimisation**

- Students take their feedback forms and prioritise the bugs they received.

- Walk through common performance optimisation techniques:

  1. **Reduce unnecessary parts:** Delete parts that players cannot see or interact with.
  2. **Use StreamingEnabled:** In Workspace properties, enable `StreamingEnabled`. Say: *"This makes Roblox only load the parts near the player instead of the entire map. For large maps, this massively improves performance."*
  3. **Optimise scripts — avoid polling:**

```lua
-- BAD: Checking every frame (wasteful)
game:GetService("RunService").Heartbeat:Connect(function()
    local health = humanoid.Health
    healthLabel.Text = "Health: " .. health
end)

-- GOOD: Only update when health actually changes (efficient)
humanoid.HealthChanged:Connect(function(newHealth)
    healthLabel.Text = "Health: " .. math.floor(newHealth)
end)
```

  4. **Use debounce properly:**

```lua
-- BAD: No debounce (fires dozens of times)
part.Touched:Connect(function(hit)
    local humanoid = hit.Parent:FindFirstChild("Humanoid")
    if humanoid then
        humanoid:TakeDamage(10)
    end
end)

-- GOOD: Debounce prevents rapid re-triggering
local debounce = false
part.Touched:Connect(function(hit)
    if debounce then return end
    local humanoid = hit.Parent:FindFirstChild("Humanoid")
    if humanoid then
        debounce = true
        humanoid:TakeDamage(10)
        task.wait(1)
        debounce = false
    end
end)
```

  5. **Clean up connections when no longer needed:**

```lua
-- GOOD: Disconnect events when the character is removed
local connection
connection = humanoid.HealthChanged:Connect(function(health)
    healthLabel.Text = "Health: " .. math.floor(health)
end)

humanoid.Died:Connect(function()
    connection:Disconnect()
end)
```

- Students spend 20 minutes fixing bugs from their playtest feedback, starting with Critical and Major issues.
- Circulate and help. Encourage students to use the Output window to identify errors.

**60-75 min: Extension — Advanced Quality Assurance**

- Introduce a game quality checklist that students work through:

```
GAME QUALITY CHECKLIST
========================
[ ] All GUI elements display correctly
[ ] Health bar updates when damaged
[ ] Score updates when earning points
[ ] Timer counts down correctly
[ ] Background music plays and loops
[ ] Sound effects play at appropriate times
[ ] Teams are assigned correctly
[ ] Players spawn at their team's spawn point
[ ] Damage system works (no friendly fire)
[ ] Round system starts, runs, and ends correctly
[ ] No errors in the Output window
[ ] Game does not crash on respawn
[ ] All parts have correct collision settings
[ ] No parts floating without anchoring
[ ] Game runs smoothly (no visible lag)
```

- Challenge advanced students to add an error reporting system:

```lua
-- Error Logger Script (ServerScriptService)
-- Tracks and logs errors that occur during gameplay

local logFolder = Instance.new("Folder")
logFolder.Name = "ErrorLog"
logFolder.Parent = game:GetService("ServerStorage")

local errorCount = 0

local function logError(message, source)
    errorCount = errorCount + 1
    local entry = Instance.new("StringValue")
    entry.Name = "Error_" .. errorCount
    entry.Value = os.date("%H:%M:%S") .. " | " .. source .. " | " .. message
    entry.Parent = logFolder

    warn("[ERROR LOG #" .. errorCount .. "] " .. message)
end

-- Example: Wrap risky operations in pcall
local success, result = pcall(function()
    -- Code that might error goes here
    local value = workspace:FindFirstChild("NonExistentPart").Name
end)

if not success then
    logError(result, "TestScript")
end

print("Error logging system active. Errors so far: " .. errorCount)
```

- Introduce `pcall` (protected call): *"pcall runs code in a safe way. If the code errors, instead of crashing, pcall catches the error and lets you handle it gracefully."*

**75-85 min: Sharing and Discussion**

- Class debrief. Ask each student to share:
  - Their most critical bug and how they fixed it.
  - One balance change they made and why.
- Create a "class bug board" on the whiteboard: students add sticky notes with the most common bugs they found. Group them by category.
- Discussion: *"Professional game studios have dedicated QA teams. Some studios spend more time testing than building. Why do you think that is?"*
- Key takeaway: *"A game is never finished — it is just tested enough to be good enough. Your job is to find the point where the game is polished enough to be enjoyable."*

**85-90 min: Closure and Preview**

- Say: *"Unit 5 is now complete. You have built GUI systems, added audio, created multiplayer mechanics, and learned to test and polish your work. You are ready for the capstone."*
- Preview Session 21: *"Next session begins your capstone project — a game that YOU design from start to finish. You will write a Game Design Document, plan your features, and start building. This is your chance to put everything together."*
- Remind students to save all work.

##### Differentiation

**Support:**
- Provide a simplified playtest form with checkboxes rather than open-ended questions, making it easier for students to record observations quickly.
- Pre-identify 3-5 specific bugs in a template project so struggling students can practise fixing known issues rather than searching for unknown ones.
- Pair weaker students with stronger partners during the peer playtest; the stronger student models how to systematically test features.

**Extension:**
- Challenge advanced students to write a unit testing script that automatically tests game systems (e.g., "create a player, damage them, check if health decreased, check if leaderstats updated").
- Ask them to implement `ContentProvider:PreloadAsync()` to preload all game assets (sounds, images) during a loading screen.
- Have them research Roblox's Developer Console (F9 in-game) and write a summary of the information available there (memory usage, network stats, log messages).

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Game balance understanding | Cannot identify balance issues | Identifies 1-2 balance issues with prompting | Identifies 4+ balance issues across multiple categories | Identifies, analyses, and proposes solutions for balance issues with reasoning |
| Playtesting methodology | Does not follow structured process | Playtests casually without recording findings | Uses structured form, records bugs and balance issues systematically | Conducts multiple targeted test passes, categorises by severity, prioritises fixes |
| Bug fixing ability | Cannot identify or fix bugs | Identifies bugs but cannot fix them independently | Fixes 3+ bugs identified during playtesting | Fixes all critical/major bugs and explains the root cause of each |
| Performance awareness | No understanding of optimisation | Aware of performance but does not apply techniques | Applies 2-3 optimisation techniques (debounce, events over polling, cleanup) | Applies multiple techniques, explains why each matters, and measures improvement |

##### Teacher Notes

- Peer playtesting can be socially sensitive. Establish ground rules before the session: *"Feedback is about the GAME, not the person. Be specific and constructive. Instead of 'your game is bad,' say 'I noticed the health bar does not update when I take damage — that might be a bug.'"*
- Some students will have very few bugs because their game is simple. Redirect them to balance testing: *"Your game works. Now make it FUN. Adjust the numbers until it feels right."*
- The Output window (View > Output in Roblox Studio) is the most important debugging tool. If students are not already checking it habitually, make it a mandatory step: *"Before you call me over for help, read the Output window first and tell me what it says."*
- Performance optimisation is a deep topic. Keep it practical for this age group: avoid polling, use debounce, clean up connections. Do not go into micro-optimisation (table pooling, spatial queries) unless advanced students ask.
- If time is short, the Extension section (error logging, pcall) can be skipped or assigned as homework. The core of this session is the playtest-feedback-fix cycle.

---

#### SESSION 20 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 20: Game Balancing, Playtesting & Quality Assurance**

---

##### Part 1: Game Balance Analysis

**Instructions:** Look at your game (or a classmate's game) and identify balance issues in each category.

| Category | Current Value | Is It Balanced? | Suggested Change |
|----------|--------------|----------------|-----------------|
| **Damage per hit** | _____________ | [ ] Yes [ ] No | _________________ |
| **Player health** | _____________ | [ ] Yes [ ] No | _________________ |
| **Round time** | _____________ seconds | [ ] Yes [ ] No | _________________ |
| **Points per kill** | _____________ | [ ] Yes [ ] No | _________________ |
| **Spawn distance between teams** | _____________ studs | [ ] Yes [ ] No | _________________ |
| **Coin value** | _____________ | [ ] Yes [ ] No | _________________ |

**Question:** What makes a game "balanced"? Write a definition in your own words.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 2: Playtest Feedback Form

**Instructions:** Play your partner's game for 5 minutes. Record every bug, balance issue, and observation below.

**Partner's Name:** _________________________________

**Game Tested:** _________________________________

| # | What Happened | Category | Severity |
|---|--------------|----------|----------|
| 1 | __________________________________ | [ ] Bug [ ] Balance [ ] Feature | [ ] Critical [ ] Major [ ] Minor [ ] Cosmetic |
| 2 | __________________________________ | [ ] Bug [ ] Balance [ ] Feature | [ ] Critical [ ] Major [ ] Minor [ ] Cosmetic |
| 3 | __________________________________ | [ ] Bug [ ] Balance [ ] Feature | [ ] Critical [ ] Major [ ] Minor [ ] Cosmetic |
| 4 | __________________________________ | [ ] Bug [ ] Balance [ ] Feature | [ ] Critical [ ] Major [ ] Minor [ ] Cosmetic |
| 5 | __________________________________ | [ ] Bug [ ] Balance [ ] Feature | [ ] Critical [ ] Major [ ] Minor [ ] Cosmetic |
| 6 | __________________________________ | [ ] Bug [ ] Balance [ ] Feature | [ ] Critical [ ] Major [ ] Minor [ ] Cosmetic |

**Best thing about the game:** _______________________________________________________________

**One thing that would make it much better:** ________________________________________________

---

##### Part 3: Bug Priority List

**Instructions:** Based on the feedback you RECEIVED, list the issues in priority order (most critical first).

| Priority | Bug/Issue Description | How I Plan to Fix It | Fixed? |
|----------|----------------------|---------------------|--------|
| 1 (Critical) | __________________________________ | __________________________________ | [ ] |
| 2 (Major) | __________________________________ | __________________________________ | [ ] |
| 3 (Major) | __________________________________ | __________________________________ | [ ] |
| 4 (Minor) | __________________________________ | __________________________________ | [ ] |
| 5 (Minor) | __________________________________ | __________________________________ | [ ] |

---

##### Part 4: Optimisation Challenge

**Instructions:** Read each code pair. Circle which version is BETTER and explain why.

**Pair 1: Updating a display**

**Version A:**
```lua
game:GetService("RunService").Heartbeat:Connect(function()
    scoreLabel.Text = "Score: " .. score.Value
end)
```

**Version B:**
```lua
score.Changed:Connect(function(newValue)
    scoreLabel.Text = "Score: " .. newValue
end)
```

Better version: ____ Why? _______________________________________________________________

**Pair 2: Handling touch events**

**Version A:**
```lua
part.Touched:Connect(function(hit)
    local humanoid = hit.Parent:FindFirstChild("Humanoid")
    if humanoid then
        humanoid:TakeDamage(10)
    end
end)
```

**Version B:**
```lua
local debounce = false
part.Touched:Connect(function(hit)
    if debounce then return end
    local humanoid = hit.Parent:FindFirstChild("Humanoid")
    if humanoid then
        debounce = true
        humanoid:TakeDamage(10)
        task.wait(1)
        debounce = false
    end
end)
```

Better version: ____ Why? _______________________________________________________________

**Pair 3: Cleaning up connections**

**Version A:**
```lua
humanoid.HealthChanged:Connect(function(health)
    healthLabel.Text = "HP: " .. health
end)
-- Connection stays active forever
```

**Version B:**
```lua
local conn
conn = humanoid.HealthChanged:Connect(function(health)
    healthLabel.Text = "HP: " .. health
end)
humanoid.Died:Connect(function()
    conn:Disconnect()
end)
```

Better version: ____ Why? _______________________________________________________________

---

##### Part 5: Quality Checklist

**Instructions:** Test YOUR game against this checklist. Be honest!

| # | Feature | Works? | Notes |
|---|---------|--------|-------|
| 1 | GUI displays correctly on screen | [ ] Yes [ ] No | _____________ |
| 2 | Health updates when damaged | [ ] Yes [ ] No | _____________ |
| 3 | Score updates when points earned | [ ] Yes [ ] No | _____________ |
| 4 | Timer counts down | [ ] Yes [ ] No | _____________ |
| 5 | Background music plays | [ ] Yes [ ] No | _____________ |
| 6 | Sound effects play correctly | [ ] Yes [ ] No | _____________ |
| 7 | Teams assigned correctly | [ ] Yes [ ] No | _____________ |
| 8 | Players spawn at team spawn | [ ] Yes [ ] No | _____________ |
| 9 | Round system works | [ ] Yes [ ] No | _____________ |
| 10 | No errors in Output window | [ ] Yes [ ] No | _____________ |
| 11 | Game runs without crashing | [ ] Yes [ ] No | _____________ |
| 12 | Game is fun to play | [ ] Yes [ ] No | _____________ |

**Total features working: _______ / 12**

---

##### Reflection

1. What was the most important bug you fixed today? How did you find it and how did you fix it?

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Why is playtesting with OTHER people more valuable than testing your own game by yourself?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

3. Rate your game's readiness for publishing (circle one):

`Not Ready` --- `Needs Work` --- `Almost There` --- `Ready to Publish` --- `Polished and Professional`

---

##### Bonus Challenge

Write a `pcall` (protected call) wrapper for a risky piece of code in your game. `pcall` catches errors without crashing the game.

```lua
-- Example: Safely accessing a part that might not exist
local success, errorMessage = pcall(function()
    local part = workspace:FindFirstChild("SpecialPart")
    local name = part.Name  -- This will error if part is nil!
    print("Found: " .. name)
end)

if not success then
    warn("Safe error caught: " .. errorMessage)
    -- Handle the error gracefully instead of crashing
end
```

**Your turn:** Write a pcall wrapper for one piece of your game code that could potentially error:

```lua
local success, errorMessage = pcall(function()
    -- Your risky code here:
    _______________________________________________________________________________
    _______________________________________________________________________________
    _______________________________________________________________________________
end)

if not success then
    warn("Error: " .. errorMessage)
end
```

*Save your project! The capstone project begins next session!*
# Roblox Studio Intermediate: Lesson Plans & Worksheets
## Unit 6: Capstone Project & Publishing (Sessions 21-24)

### Unit Overview

Unit 6 is the culmination of the entire Roblox Studio Intermediate course, where students transform from guided learners into independent game developers. Session 21 opens with the creation of a Game Design Document (GDD), teaching students the professional planning process that every studio uses before writing a single line of code. Sessions 22 and 23 are dedicated development sprints where students build their core gameplay loop, implement mechanics from across all five previous units, and iterate through playtesting and polish. The unit and course conclude with Session 24, where students publish their games to the Roblox platform, present their work to peers, give and receive structured feedback, and document their projects for a personal portfolio. Every session pairs a detailed teacher-facing lesson plan with a hands-on student worksheet, ensuring that theory and practice remain inseparable.

---

### Session 21: Capstone Project — Planning & Game Design Document

---

#### SESSION 21 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 21 of 24 |
| **Title** | Capstone Project — Planning & Game Design Document |
| **Unit** | Unit 6: Capstone Project & Publishing |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Write a Game Design Document (GDD) that includes a game title, genre, target audience, core mechanic description, feature list, and visual/audio plan.
2. Define a core mechanic for their capstone game and explain why a strong core mechanic is the foundation of every successful game.
3. Prioritise features using the MVP (Minimum Viable Product) approach, distinguishing between must-have, should-have, and nice-to-have features.
4. Set up the Roblox Studio project structure for their capstone game and begin building the core gameplay elements.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Projector or screen-share software for teacher demonstrations
- Session 21 Worksheet / GDD Template (printed or displayed digitally)
- Whiteboard for brainstorming and examples
- Timer or stopwatch for timed activities
- Examples of simple GDDs (teacher prepares 1-2 one-page examples)
- Optional: printed cards with game genre names for brainstorming activity

##### Procedure

**0-5 min: Warm-Up — "Elevator Pitch"**

- Say: *"Imagine you are in a lift with a famous game developer. You have 30 seconds to describe a game idea that will make them say 'Tell me more!' This is called an elevator pitch."*
- Give an example: *"My game is a team-based obstacle course where players race through randomly generated levels. The twist is that each team member has a unique ability — one can fly for 3 seconds, one can build bridges, one can freeze obstacles — so you MUST work together to win."*
- Give students 90 seconds to write their own elevator pitch on a piece of paper. Then ask 3-4 volunteers to read theirs aloud.
- After each pitch, the class gives a thumbs up (interested) or thumbs sideways (needs more detail). No thumbs down — every idea has potential.
- Say: *"That 30-second pitch is the seed of your capstone project. Today we turn that seed into a full plan."*

**5-15 min: Introduction — What Is a Game Design Document?**

- Display a simple one-page GDD example on the projector. Walk through each section:
  1. **Game Title** — the name of the game.
  2. **Genre** — what type of game (obby, tycoon, fighting, simulator, adventure, puzzle).
  3. **Target Audience** — who will play it? (Age range, casual vs competitive)
  4. **Core Mechanic** — the ONE thing the player does most often. This is the heart of the game.
  5. **Game Loop** — what does a typical play session look like? (Join > get assigned > play round > earn rewards > play again)
  6. **Feature List** — everything the game includes, prioritised.
  7. **Visual Style** — what does the game look like? (colours, theme, environment)
  8. **Audio Plan** — what sounds and music will the game have?
  9. **Technical Plan** — what scripts, services, and systems are needed?

- Emphasise the core mechanic: *"Every great game can be described by one verb. In Mario, the core mechanic is JUMP. In Minecraft, it is BUILD. In Roblox Adopt Me, it is COLLECT. What is your one verb?"*

- Introduce the MVP concept:
  - **Must-Have** — without these features, the game does not work at all. The core mechanic, one level, basic controls.
  - **Should-Have** — these features make the game significantly better. GUI, sound effects, scoring.
  - **Nice-to-Have** — these features would be great but the game works without them. Custom animations, save system, multiple game modes.
  - Say: *"Professional developers always start with the MVP. Get the core working FIRST. Then add layers of polish. If you try to build everything at once, you finish nothing."*

**15-35 min: Guided Practice — Writing the GDD**

- Students open the worksheet (GDD template). Walk through each section together, with the teacher filling in a demo GDD on the projector as a model:

  **Demo GDD (teacher fills in live):**
  - Title: "Tower Defense Showdown"
  - Genre: Strategy / Tower Defense
  - Target Audience: Ages 10-14, casual players who enjoy strategy
  - Core Mechanic: PLACE towers to defend against waves of enemies
  - Game Loop: Lobby > select difficulty > place towers > survive waves > earn currency > upgrade > repeat
  - Feature List:
    - Must-Have: Tower placement, enemy waves, health system, wave counter
    - Should-Have: Currency system, tower upgrades, GUI with wave info, background music
    - Nice-to-Have: Multiple maps, boss enemies, leaderboard, save progress
  - Visual Style: Bright colours, cartoon style, green grass map with dirt paths
  - Audio Plan: Upbeat music, tower shooting sound, enemy defeat sound, wave start horn
  - Technical Plan: ServerScriptService for wave logic, ReplicatedStorage for tower data, LocalScript for GUI

- After demonstrating, give students 15 minutes to fill in their own GDD on the worksheet. Circulate and help students who are stuck on their core mechanic or feature prioritisation.

- Common teacher interventions:
  - If a student's scope is too large: *"That sounds amazing, but can you build it in 3 sessions? Let us find the MVP version."*
  - If a student's scope is too small: *"What if you added [feature from a previous unit]? You already know how to build that."*
  - If a student has no idea: *"What was your favourite thing we built this course? What if you took that and made it your own?"*

**35-60 min: Independent Practice — Project Setup and Core Development**

- Students set up their capstone project in Roblox Studio:

  1. Create a new project or a new Place within their existing project. Name it their game title.
  2. Set up the folder structure in the Explorer:

```
game
├── Workspace
│   └── (game world parts go here)
├── ServerScriptService
│   └── (server scripts go here)
├── StarterGui
│   └── (GUI elements go here)
├── StarterPlayerScripts
│   └── (client scripts that run once go here)
├── StarterCharacterScripts
│   └── (scripts that run per character go here)
├── StarterPack
│   └── (tools go here)
├── ReplicatedStorage
│   └── (shared data, RemoteEvents go here)
├── ServerStorage
│   └── (server-only assets go here)
└── SoundService
    └── (music and global sounds go here)
```

- Say: *"Before you write any code, build the structure. Professional developers call this 'scaffolding.' You are building the skeleton that your game will hang on."*

- Students begin building their core mechanic. Guide them with targeted questions based on their game type:
  - **Obby/Platformer:** *"Start with the spawn point and three obstacles. Can the player reach the end?"*
  - **Fighting/Battle:** *"Start with two spawn points and a damage tool. Can players fight?"*
  - **Tycoon/Simulator:** *"Start with one collector and one thing to collect. Does the loop work?"*
  - **Adventure/Quest:** *"Start with one quest NPC and one objective. Can the player complete it?"*

- Provide a basic game template script students can adapt:

```lua
-- GameSetup Script (ServerScriptService)
-- Basic setup for any capstone game

local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

-- Create shared folders for organisation
local eventsFolder = Instance.new("Folder")
eventsFolder.Name = "GameEvents"
eventsFolder.Parent = ReplicatedStorage

local dataFolder = Instance.new("Folder")
dataFolder.Name = "GameData"
dataFolder.Parent = ReplicatedStorage

-- Create a game status value
local gameStatus = Instance.new("StringValue")
gameStatus.Name = "Status"
gameStatus.Value = "Waiting"
gameStatus.Parent = dataFolder

-- Player setup
local function onPlayerAdded(player)
    -- Create leaderstats
    local leaderstats = Instance.new("Folder")
    leaderstats.Name = "leaderstats"
    leaderstats.Parent = player

    local score = Instance.new("IntValue")
    score.Name = "Score"
    score.Value = 0
    score.Parent = leaderstats

    -- Create player data folder for custom stats
    local playerData = Instance.new("Folder")
    playerData.Name = "PlayerData"
    playerData.Parent = player

    print(player.Name .. " joined the game!")
end

local function onPlayerRemoving(player)
    print(player.Name .. " left the game.")
end

Players.PlayerAdded:Connect(onPlayerAdded)
Players.PlayerRemoving:Connect(onPlayerRemoving)

-- Handle players already in the game (for Studio testing)
for _, player in ipairs(Players:GetPlayers()) do
    task.spawn(onPlayerAdded, player)
end

print("Game setup complete!")
```

- Students have 25 minutes of focused development time. Teacher circulates, checking that:
  - The project structure is set up correctly.
  - The core mechanic is being built (not decorating or adding secondary features).
  - Students are not stuck without asking for help.

**60-75 min: Extension — Advanced Planning and Prototyping**

- Students who have completed their GDD and set up their project can begin prototyping their core mechanic.

- For advanced students, introduce a milestone planning approach:

```
MILESTONE PLAN
==============
Session 21 (Today): GDD complete, project set up, core mechanic prototype started
Session 22 (Next):   Core mechanic WORKING, game world built, basic GUI
Session 23:          Polish — audio, effects, playtesting, bug fixing
Session 24:          Publish, present, celebrate
```

- Challenge them to write pseudocode for their main game loop before coding it:

```lua
--[[
PSEUDOCODE FOR MY GAME LOOP
============================

1. Player joins the game
2. Player spawns at the starting area
3. Player walks to the first challenge
4. IF player completes the challenge THEN
     award 100 points
     unlock the next area
   ELSE
     player respawns at last checkpoint
5. REPEAT from step 3 until all challenges complete
6. Display "You Win!" screen with total time and score
7. Add score to leaderboard
--]]
```

- Say: *"Writing pseudocode first is like drawing a map before driving. You might not follow it exactly, but you will never get completely lost."*

**75-85 min: Sharing and Discussion**

- Gallery walk: students spend 5 minutes visiting 3-4 other students' workstations. At each station, they read the GDD and give one piece of constructive feedback on a sticky note: *"One thing I am excited to play"* and *"One suggestion to make it even better."*
- After the gallery walk, ask 2-3 volunteers to share:
  - Their game concept in one sentence.
  - Their core mechanic.
  - Their biggest challenge for the next session.
- Class discussion: *"What did you notice about the GDDs that felt the most clear and achievable? What made them strong?"*

**85-90 min: Closure and Preview**

- Quick check: *"Raise your hand if your GDD is complete. Keep it up if your project is set up in Roblox Studio. Keep it up if you have started building your core mechanic."*
- Preview Session 22: *"Next session is pure development time. You will have 90 minutes to build your core gameplay loop. Come prepared with your GDD — it is your roadmap."*
- Remind students to save their project and their GDD worksheet.

##### Differentiation

**Support:**
- Provide a simplified GDD template with fill-in-the-blank prompts rather than open-ended sections, reducing the writing burden for students who find planning difficult.
- Offer three pre-designed game concepts (a simple obby, a coin collector, a battle arena) that struggling students can choose from, with the GDD already partially completed.
- During development time, provide starter templates (pre-built spawn points, basic terrain, a working tool) so students can focus on customisation rather than building from scratch.

**Extension:**
- Challenge advanced students to create a flowchart diagram of their game loop using boxes and arrows, showing every possible player path including failure states.
- Ask them to write a technical specification listing every script they will need, what service each belongs in, and what events/functions each will contain.
- Have them research and plan a DataStore implementation for saving player progress between sessions (they will implement this in Session 23 if time allows).

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| GDD completeness | No GDD or mostly blank | 3-4 sections filled with vague descriptions | All sections complete with specific, clear descriptions | Comprehensive GDD with detailed feature prioritisation and technical planning |
| Core mechanic definition | Cannot identify a core mechanic | Describes gameplay generally but the core mechanic is unclear | Clearly defines ONE core mechanic and explains why it is fun | Defines core mechanic, explains player motivation, and identifies potential balance issues |
| Feature prioritisation | No prioritisation attempted | Lists features but does not distinguish must-have from nice-to-have | Correctly categorises features into must/should/nice with logical reasoning | Prioritised list with time estimates and dependency awareness |
| Project setup | Project not created | Project created but structure is disorganised | Clean project structure with correct service usage | Professional structure with named folders, starter scripts, and clear organisation |

##### Teacher Notes

- Scope management is the biggest challenge in this session. Most students will want to build something far too ambitious. The teacher's primary role is gentle scope reduction: *"That is a brilliant idea. For Sessions 22-24, let us focus on the core. You can always expand it after the course."*
- Students who freeze during brainstorming often respond well to constraints: *"Pick a genre: obby, fighting, or tycoon. Now pick a twist that makes yours different."* Constraints paradoxically increase creativity.
- The GDD does not need to be long — one page is ideal. Emphasise quality over quantity. A clear, focused GDD is better than a vague, ambitious one.
- Some students may want to work in pairs. Allow this if both students contribute equally. Require separate GDD sections showing what each student is responsible for.
- Take photos of or collect the GDD worksheets. They serve as the assessment artefact for this session and as a reference for teacher check-ins during Sessions 22-23.
- If students ask about game ideas, redirect with: *"What was your favourite project from this course? What would you do differently if you could remake it from scratch?"*

---

#### SESSION 21 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 21: Capstone Project — Planning & Game Design Document**

---

##### Part 1: Elevator Pitch

**Instructions:** Write a 2-3 sentence pitch for your game. Imagine you are explaining it to someone who has never played it.

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 2: Game Design Document (GDD)

**Instructions:** Fill in every section of this GDD. Be as specific as possible. This document is your roadmap for the next three sessions.

---

**GAME TITLE:**

> _______________________________________________________________________________

**GENRE:** (circle one or write your own)

`Obby` --- `Tycoon` --- `Fighting` --- `Simulator` --- `Adventure` --- `Puzzle` --- `Tower Defense` --- `Racing` --- `Other: ____________`

**TARGET AUDIENCE:**

> Age range: _____________ Casual or Competitive? _____________
>
> What type of player will enjoy this game? _______________________________________________

---

**CORE MECHANIC:**

The ONE thing the player does most often. Describe it in one sentence.

> The core mechanic is: _______________________________________________________________________________

Why is this mechanic fun? What makes the player want to keep doing it?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

**GAME LOOP:**

Describe what a typical play session looks like, step by step.

> 1. Player joins and _______________________________________________________________________________
>
> 2. Player _______________________________________________________________________________
>
> 3. Player _______________________________________________________________________________
>
> 4. IF player succeeds: _______________________________________________________________________________
>
> 5. IF player fails: _______________________________________________________________________________
>
> 6. Game ends when: _______________________________________________________________________________

---

**FEATURE LIST:**

Categorise every feature your game will have.

| Priority | Feature | Description | Which Unit Taught This? |
|----------|---------|-------------|------------------------|
| **Must-Have** | ________________________________ | ________________________________ | Unit ____ |
| **Must-Have** | ________________________________ | ________________________________ | Unit ____ |
| **Must-Have** | ________________________________ | ________________________________ | Unit ____ |
| **Must-Have** | ________________________________ | ________________________________ | Unit ____ |
| **Should-Have** | ________________________________ | ________________________________ | Unit ____ |
| **Should-Have** | ________________________________ | ________________________________ | Unit ____ |
| **Should-Have** | ________________________________ | ________________________________ | Unit ____ |
| **Nice-to-Have** | ________________________________ | ________________________________ | Unit ____ |
| **Nice-to-Have** | ________________________________ | ________________________________ | Unit ____ |

---

**VISUAL STYLE:**

What does your game look like? Describe the environment, colours, and theme.

> _______________________________________________________________________________
>
> _______________________________________________________________________________

Sketch your game's main screen in the box below (stick figures are fine!):

```
+---------------------------------------------------------------+
|                                                               |
|                                                               |
|                                                               |
|                     (Draw your game here)                     |
|                                                               |
|                                                               |
|                                                               |
|                                                               |
+---------------------------------------------------------------+
```

---

**AUDIO PLAN:**

| Sound | Type (2D/3D) | When Does It Play? |
|-------|-------------|-------------------|
| Background Music: _____________ | 2D | ________________________ |
| SFX 1: _____________ | ______ | ________________________ |
| SFX 2: _____________ | ______ | ________________________ |
| SFX 3: _____________ | ______ | ________________________ |
| UI Sound: _____________ | ______ | ________________________ |

---

**TECHNICAL PLAN:**

List the scripts you will need and where they go.

| Script Name | Location | What Does It Do? |
|-------------|----------|-----------------|
| ________________________________ | ServerScriptService | ________________________________ |
| ________________________________ | ServerScriptService | ________________________________ |
| ________________________________ | StarterGui (LocalScript) | ________________________________ |
| ________________________________ | StarterPlayerScripts | ________________________________ |
| ________________________________ | ________________________________ | ________________________________ |

---

##### Part 3: Project Setup Checklist

**Instructions:** Set up your capstone project in Roblox Studio. Tick each box as you complete it.

1. [ ] Create a new Roblox Studio project (or new Place). Name it your game title.
2. [ ] Verify these services are visible in the Explorer:
   - [ ] Workspace
   - [ ] ServerScriptService
   - [ ] StarterGui
   - [ ] StarterPlayerScripts
   - [ ] StarterCharacterScripts
   - [ ] StarterPack
   - [ ] ReplicatedStorage
   - [ ] ServerStorage
   - [ ] SoundService
3. [ ] Add a **Script** in ServerScriptService. Rename it `GameSetup`.
4. [ ] Type the basic setup code:

```lua
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

local eventsFolder = Instance.new("Folder")
eventsFolder.Name = "GameEvents"
eventsFolder.Parent = ReplicatedStorage

local dataFolder = Instance.new("Folder")
dataFolder.Name = "GameData"
dataFolder.Parent = ReplicatedStorage

local gameStatus = Instance.new("StringValue")
gameStatus.Name = "Status"
gameStatus.Value = "Waiting"
gameStatus.Parent = dataFolder

local function onPlayerAdded(player)
    local leaderstats = Instance.new("Folder")
    leaderstats.Name = "leaderstats"
    leaderstats.Parent = player

    local score = Instance.new("IntValue")
    score.Name = "Score"
    score.Value = 0
    score.Parent = leaderstats

    print(player.Name .. " joined the game!")
end

Players.PlayerAdded:Connect(onPlayerAdded)

for _, player in ipairs(Players:GetPlayers()) do
    task.spawn(onPlayerAdded, player)
end

print("Game setup complete!")
```

5. [ ] Press **F5** to test. Does "Game setup complete!" appear in the Output? [ ] Yes [ ] No
6. [ ] Begin building your core mechanic (the Must-Have features from your GDD).
7. [ ] Save your project.

**What did you build so far?**

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 4: Milestone Plan

**Instructions:** Plan what you will accomplish in each remaining session.

| Session | What I Will Build | Completion Goal |
|---------|------------------|----------------|
| Session 21 (Today) | GDD + project setup + ________________________ | Core mechanic prototype started |
| Session 22 | ________________________________ | Core mechanic WORKING + basic GUI |
| Session 23 | ________________________________ | Polish + audio + playtesting + bug fixing |
| Session 24 | ________________________________ | Publish + present + portfolio |

---

##### Reflection

1. What is the most challenging part of your game to build? How do you plan to tackle it?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. If you run out of time, which features will you cut? (These should be your Nice-to-Have features.)

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Bonus Challenge

Write pseudocode for your main game loop. Use plain English with some code structure (IF, THEN, REPEAT, WHILE):

```
-- MY GAME LOOP PSEUDOCODE
-- =======================

1. WHEN player joins:
   _______________________________________________________________________________

2. SETUP:
   _______________________________________________________________________________

3. MAIN LOOP:
   WHILE _______________________________________________
       _______________________________________________________________________________
       IF _______________________________________________  THEN
           _______________________________________________________________________________
       ELSE
           _______________________________________________________________________________
       END
   END

4. GAME OVER:
   _______________________________________________________________________________
```

*Save your project and your GDD! You will need both next session.*

---

### Session 22: Capstone Project — Core Development

---

#### SESSION 22 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 22 of 24 |
| **Title** | Capstone Project — Core Development |
| **Unit** | Unit 6: Capstone Project & Publishing |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Build a functional main gameplay loop that includes player input, game state changes, and feedback to the player.
2. Implement at least three game systems learned during the course (e.g., GUI, audio, scoring, physics, events) within their capstone project.
3. Create the game world environment with appropriate parts, terrain, and spatial design that supports the core mechanic.
4. Conduct self-testing during development, identifying and fixing bugs as they arise rather than waiting for external playtesting.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Capstone project from Session 21 with GDD
- Projector or screen-share software for teacher demonstrations
- Session 22 Worksheet (printed or displayed digitally — serves as a development tracker)
- GDD worksheets from Session 21 (students must have these available)
- Timer for milestone check-ins (set for 20-minute intervals)
- Whiteboard for posting common code patterns and troubleshooting tips

##### Procedure

**0-5 min: Warm-Up — "What Is Your Number One Priority Today?"**

- As students settle, display the question: *"Look at your GDD. What is the single most important thing you need to build today to make your game playable?"*
- Give students 60 seconds to write their answer. Then ask 4-5 students to share.
- Say: *"Whatever you just said — that is your entire focus for the first 40 minutes. Do not decorate. Do not add sound effects. Do not build a menu. Build the CORE FIRST. If your core mechanic is not working by the halfway point, nothing else matters."*
- Write on the board: **CORE FIRST. POLISH SECOND.**

**5-15 min: Introduction — Common Game Patterns and Code Reference**

- Before students dive into independent work, provide a quick reference of common code patterns they will likely need. Display each on the projector for 1-2 minutes:

  **Pattern 1: Touched Event with Debounce (collectibles, traps, triggers)**
```lua
local part = script.Parent
local debounce = false

part.Touched:Connect(function(hit)
    if debounce then return end
    local humanoid = hit.Parent:FindFirstChild("Humanoid")
    if humanoid then
        debounce = true
        -- YOUR CODE HERE: what happens when player touches this part?
        print("Player touched: " .. part.Name)
        task.wait(1)
        debounce = false
    end
end)
```

  **Pattern 2: Spawning Objects from ServerStorage**
```lua
local ServerStorage = game:GetService("ServerStorage")

local function spawnObject(templateName, position)
    local template = ServerStorage:FindFirstChild(templateName)
    if template then
        local clone = template:Clone()
        clone.Position = position
        clone.Parent = workspace
        return clone
    end
    return nil
end

-- Example: spawn a coin at position (10, 5, 20)
spawnObject("CoinTemplate", Vector3.new(10, 5, 20))
```

  **Pattern 3: RemoteEvent Communication (server to client)**
```lua
-- SERVER SIDE (ServerScriptService)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local myEvent = Instance.new("RemoteEvent")
myEvent.Name = "GameNotification"
myEvent.Parent = ReplicatedStorage

-- Send a message to all players
myEvent:FireAllClients("Welcome to the game!")

-- Send a message to one specific player
myEvent:FireClient(somePlayer, "You scored a point!")
```

```lua
-- CLIENT SIDE (LocalScript in StarterGui or StarterPlayerScripts)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local myEvent = ReplicatedStorage:WaitForChild("GameNotification")

myEvent.OnClientEvent:Connect(function(message)
    print("Server says: " .. message)
    -- Update GUI with the message
end)
```

  **Pattern 4: Timer System**
```lua
local function startTimer(duration, onTick, onComplete)
    for i = duration, 1, -1 do
        onTick(i)
        task.wait(1)
    end
    onComplete()
end

-- Usage:
startTimer(60,
    function(remaining)
        print("Time left: " .. remaining)
    end,
    function()
        print("Time is up!")
    end
)
```

- Say: *"These four patterns cover about 80% of what you will need. Copy and adapt them — do not reinvent the wheel. Now, build."*

**15-35 min: Independent Practice — Core Mechanic Development (Sprint 1)**

- Students work independently on their capstone projects. This is the primary development sprint.
- Teacher circulates continuously, spending 2-3 minutes with each student. Use this script:
  1. *"Show me your GDD. What are you building right now?"*
  2. *"Is this a must-have feature?"* (If not: *"Save it for later. What is your must-have?"*)
  3. *"What is blocking you? What do you need help with?"*
  4. *"Run your game for me. Does the core mechanic work?"*

- Post common troubleshooting tips on the board:
  - **"Script not running?"** Check if it is a Script (server) or LocalScript (client). Is it in the right location?
  - **"Touched not firing?"** Make sure CanCollide or CanTouch is enabled. Check for debounce issues.
  - **"GUI not showing?"** Is the ScreenGui inside StarterGui? Is ResetOnSpawn set correctly?
  - **"RemoteEvent not working?"** Is the event in ReplicatedStorage? Are you using FireClient/FireServer correctly?
  - **"Parts falling through the floor?"** Check if the part is Anchored.

- At the 20-minute mark (minute 35), ring a bell or set off a timer. Say: *"CHECKPOINT! Everyone stop coding for 30 seconds. Test your game RIGHT NOW by pressing F5. Does your core mechanic work? If yes, you are on track. If no, raise your hand — I am coming to help."*

**35-60 min: Independent Practice — Game World and Systems (Sprint 2)**

- Students who have a working core mechanic move on to building the game world and adding secondary systems:
  - Creating the environment (terrain, parts, decorations)
  - Adding GUI elements (HUD, menus, notifications)
  - Implementing scoring or progression systems
  - Adding collectibles, obstacles, or NPCs

- Students whose core mechanic is NOT working focus exclusively on debugging it with teacher support.

- Provide a world-building checklist on the board:
  ```
  WORLD-BUILDING CHECKLIST
  ========================
  [ ] Spawn point exists and is correctly positioned
  [ ] Player can move and interact with the environment
  [ ] Boundaries exist (invisible walls or kill zones so players don't fall forever)
  [ ] At least 3 interactive elements (collectibles, obstacles, triggers)
  [ ] The environment matches the game theme from the GDD
  ```

- Example: for students building an obby, show how to create kill bricks:

```lua
-- Kill Brick Script (inside a Part)
-- Kills the player when they touch this part

local killBrick = script.Parent

killBrick.Touched:Connect(function(hit)
    local humanoid = hit.Parent:FindFirstChild("Humanoid")
    if humanoid then
        humanoid.Health = 0
    end
end)
```

- Example: for students building a tycoon, show how to create a basic dropper:

```lua
-- Dropper Script (ServerScriptService or inside a Part)
-- Spawns collectible items at regular intervals

local dropperPart = script.Parent
local ServerStorage = game:GetService("ServerStorage")

local DROP_INTERVAL = 2  -- seconds between drops
local ITEM_VALUE = 5     -- points per item collected

while true do
    task.wait(DROP_INTERVAL)

    -- Create a new collectible
    local item = Instance.new("Part")
    item.Name = "Collectible"
    item.Size = Vector3.new(1, 1, 1)
    item.Shape = Enum.PartType.Ball
    item.BrickColor = BrickColor.new("Bright yellow")
    item.Position = dropperPart.Position - Vector3.new(0, 2, 0)
    item.Anchored = false
    item.Parent = workspace

    -- Destroy after 10 seconds if not collected
    game:GetService("Debris"):AddItem(item, 10)

    -- Collection logic
    item.Touched:Connect(function(hit)
        local humanoid = hit.Parent:FindFirstChild("Humanoid")
        if humanoid then
            local player = game:GetService("Players"):GetPlayerFromCharacter(hit.Parent)
            if player then
                local leaderstats = player:FindFirstChild("leaderstats")
                if leaderstats then
                    local score = leaderstats:FindFirstChild("Score")
                    if score then
                        score.Value = score.Value + ITEM_VALUE
                    end
                end
            end
            item:Destroy()
        end
    end)
end
```

- At the 25-minute mark of Sprint 2 (minute 60), another checkpoint: *"CHECKPOINT! Test your game. Is the game world built? Can a player join and play through at least one full game loop?"*

**60-75 min: Extension — Adding GUI and Feedback Systems**

- Students who have a working game loop add GUI and player feedback:

```lua
-- Simple Notification System (LocalScript in StarterGui)
-- Shows temporary messages on screen

local Players = game:GetService("Players")
local player = Players.LocalPlayer

-- Create notification GUI
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "NotificationGui"
screenGui.ResetOnSpawn = false
screenGui.Parent = player:WaitForChild("PlayerGui")

local notificationLabel = Instance.new("TextLabel")
notificationLabel.Name = "NotificationLabel"
notificationLabel.AnchorPoint = Vector2.new(0.5, 0)
notificationLabel.Position = UDim2.new(0.5, 0, 0.15, 0)
notificationLabel.Size = UDim2.new(0.4, 0, 0, 50)
notificationLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
notificationLabel.BackgroundTransparency = 0.4
notificationLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
notificationLabel.Font = Enum.Font.GothamBold
notificationLabel.TextScaled = true
notificationLabel.Text = ""
notificationLabel.Visible = false
notificationLabel.Parent = screenGui

local notifCorner = Instance.new("UICorner")
notifCorner.CornerRadius = UDim.new(0, 10)
notifCorner.Parent = notificationLabel

-- Function to show a notification
local function showNotification(message, duration, colour)
    notificationLabel.Text = message
    notificationLabel.TextColor3 = colour or Color3.fromRGB(255, 255, 255)
    notificationLabel.Visible = true
    task.delay(duration or 3, function()
        notificationLabel.Visible = false
    end)
end

-- Listen for server notifications
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local eventsFolder = ReplicatedStorage:WaitForChild("GameEvents")

-- Create the notification event if it does not exist yet
local notifEvent = eventsFolder:FindFirstChild("Notification")
if not notifEvent then
    -- Wait for server to create it
    notifEvent = eventsFolder:WaitForChild("Notification", 10)
end

if notifEvent then
    notifEvent.OnClientEvent:Connect(function(message, duration, colour)
        showNotification(message, duration, colour)
    end)
end

-- Show a welcome message
showNotification("Welcome to the game!", 3, Color3.fromRGB(85, 255, 85))
```

- Advanced students can add a checkpoint system:

```lua
-- Checkpoint System Script (ServerScriptService)
-- Saves the player's last checkpoint position

local Players = game:GetService("Players")

-- Store checkpoint positions per player
local checkpoints = {}

-- Create checkpoint parts in workspace (name them Checkpoint1, Checkpoint2, etc.)
local function setupCheckpoints()
    for _, part in ipairs(workspace:GetChildren()) do
        if part.Name:sub(1, 10) == "Checkpoint" then
            part.Touched:Connect(function(hit)
                local humanoid = hit.Parent:FindFirstChild("Humanoid")
                if humanoid then
                    local player = Players:GetPlayerFromCharacter(hit.Parent)
                    if player then
                        local checkpointNumber = tonumber(part.Name:sub(11))
                        local currentCheckpoint = checkpoints[player.UserId] or 0

                        -- Only save if this is a NEW checkpoint (higher number)
                        if checkpointNumber and checkpointNumber > currentCheckpoint then
                            checkpoints[player.UserId] = checkpointNumber
                            print(player.Name .. " reached checkpoint " .. checkpointNumber)
                        end
                    end
                end
            end)
        end
    end
end

-- Respawn player at their last checkpoint
local function onCharacterAdded(player, character)
    local checkpointNum = checkpoints[player.UserId]
    if checkpointNum then
        local checkpointPart = workspace:FindFirstChild("Checkpoint" .. checkpointNum)
        if checkpointPart then
            -- Wait for character to fully load
            task.wait(0.5)
            local rootPart = character:FindFirstChild("HumanoidRootPart")
            if rootPart then
                rootPart.CFrame = checkpointPart.CFrame + Vector3.new(0, 5, 0)
            end
        end
    end
end

Players.PlayerAdded:Connect(function(player)
    player.CharacterAdded:Connect(function(character)
        onCharacterAdded(player, character)
    end)
end)

setupCheckpoints()
print("Checkpoint system active!")
```

**75-85 min: Sharing and Discussion**

- Milestone review. Each student answers three questions aloud or written:
  1. *"Is your core mechanic working?"* (Yes/No)
  2. *"What is the biggest challenge you faced today?"*
  3. *"What is your number one priority for Session 23?"*
- Ask 3 students to demo their game on the projector (1-2 minutes each). Class provides one piece of positive feedback and one suggestion.
- Teacher addresses common issues seen during circulation: *"I noticed many of you had trouble with [specific pattern]. Let me show the solution one more time."*

**85-90 min: Closure and Preview**

- Say: *"Session 22 is your biggest development sprint. By now, your game should be PLAYABLE — maybe rough, maybe buggy, but playable. If it is not playable yet, come early next session or stay focused from minute one."*
- Preview Session 23: *"Next session is your LAST development session. You will add polish — GUI, audio, effects — and then playtest with classmates. After Session 23, the game freezes. Session 24 is publishing and presenting."*
- Remind students to save.

##### Differentiation

**Support:**
- Provide code snippet cards — printed cards with common Luau patterns (Touched event, spawning objects, updating GUI, playing sounds) that students can reference without asking the teacher each time.
- For students who are severely behind, offer a pre-built game template with the core mechanic already working, and have them customise it (change values, add levels, redesign the map).
- Assign a "coding buddy" — a more advanced student who checks in every 15 minutes to help debug without doing the work for them.

**Extension:**
- Challenge advanced students to implement DataStoreService for saving player progress between sessions.
- Ask them to create a dynamic difficulty system that adjusts based on player performance (e.g., harder obstacles if the player is doing well, easier if struggling).
- Have them implement a particle effects system using ParticleEmitters for visual feedback (collecting items, taking damage, levelling up).

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Core mechanic implementation | No core mechanic built | Core mechanic partially built but does not function | Core mechanic works — player can perform the main action | Core mechanic is polished, responsive, and feels satisfying to use |
| Game systems integration | No systems from previous units used | 1-2 systems attempted but not connected | 3+ systems integrated (GUI, audio, scoring, physics) and working together | Multiple systems integrated seamlessly with clean code architecture |
| Game world creation | No environment built | Basic environment (flat plane, few parts) | Themed environment with interactive elements and boundaries | Detailed environment that enhances gameplay and matches the GDD vision |
| Development practice | No testing during development | Tests occasionally but does not fix bugs found | Tests regularly, fixes bugs, and iterates on design | Systematic test-fix-iterate cycle with Output window monitoring |

##### Teacher Notes

- This session requires the teacher to be constantly moving. Do not sit at the desk. Visit every student at least twice. The first visit checks direction (are they building the right thing?). The second visit checks progress (is the core mechanic working?).
- Resist the urge to write code for students. Instead, ask guiding questions: *"What are you trying to make happen? What have you tried? What did the Output window say?"* Only write code as a last resort for students who are completely stuck.
- Some students will want to spend the entire session decorating their game world. Redirect firmly but kindly: *"The world looks great, but can a player actually PLAY your game? Build the game first, decorate second."*
- Watch for students who are silently stuck but not asking for help. Signs: staring at the screen, clicking randomly, switching between tabs. Approach these students proactively.
- The code patterns displayed at the beginning of the session should remain on the projector or board for the entire session. Students will reference them repeatedly.
- If a student finishes their core mechanic very quickly, challenge them: *"Can you break it? Play your game and try to find every edge case. What happens if you do something unexpected?"*

---

#### SESSION 22 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 22: Capstone Project — Core Development**

---

##### Part 1: Pre-Development Check

**Instructions:** Before you start coding, answer these questions using your GDD from Session 21.

**My game title:** _______________________________________________

**My core mechanic (one sentence):** _______________________________________________

**My number one priority today:** _______________________________________________

**Three Must-Have features I need to build today:**

| # | Feature | Started? | Working? |
|---|---------|----------|----------|
| 1 | ________________________________ | [ ] | [ ] |
| 2 | ________________________________ | [ ] | [ ] |
| 3 | ________________________________ | [ ] | [ ] |

---

##### Part 2: Development Log

**Instructions:** As you build, record what you do every 20 minutes. This helps you track progress and debug later.

**Sprint 1 (Minutes 15-35): Core Mechanic**

What I built:
> _______________________________________________________________________________
>
> _______________________________________________________________________________

Problems I encountered:
> _______________________________________________________________________________

How I solved them:
> _______________________________________________________________________________

Core mechanic status: [ ] Not started [ ] In progress [ ] Working [ ] Working + polished

---

**Sprint 2 (Minutes 35-60): Game World and Systems**

What I built:
> _______________________________________________________________________________
>
> _______________________________________________________________________________

Problems I encountered:
> _______________________________________________________________________________

How I solved them:
> _______________________________________________________________________________

Systems integrated:
- [ ] GUI (HUD, menus, labels)
- [ ] Audio (music, sound effects)
- [ ] Scoring (leaderstats, points)
- [ ] Physics (collisions, movement)
- [ ] Events (Touched, RemoteEvents)
- [ ] Teams (if multiplayer)
- [ ] Other: _______________________

---

**Sprint 3 (Minutes 60-75): Polish and Extension**

What I added:
> _______________________________________________________________________________
>
> _______________________________________________________________________________

My game can now:
> _______________________________________________________________________________

---

##### Part 3: Self-Testing Checklist

**Instructions:** Test your game by pressing F5. Check each item honestly.

| # | Test | Pass? | Notes |
|---|------|-------|-------|
| 1 | Player can join and spawn correctly | [ ] Yes [ ] No | _____________ |
| 2 | Core mechanic works (player can do the main action) | [ ] Yes [ ] No | _____________ |
| 3 | There are no errors in the Output window | [ ] Yes [ ] No | _____________ |
| 4 | The game has clear boundaries (player cannot fall forever) | [ ] Yes [ ] No | _____________ |
| 5 | The game gives feedback when the player does something (sound, GUI, visual) | [ ] Yes [ ] No | _____________ |
| 6 | Score or progress tracking works | [ ] Yes [ ] No | _____________ |
| 7 | The game has at least one complete loop (start to end of one round/level) | [ ] Yes [ ] No | _____________ |
| 8 | The game does not crash on respawn | [ ] Yes [ ] No | _____________ |

**Tests passed: _______ / 8**

---

##### Part 4: Code I Am Proud Of

**Instructions:** Copy and paste (or write) the most important piece of code you wrote today. Explain what it does in your own words.

```lua
-- My best code from today:
_______________________________________________________________________________
_______________________________________________________________________________
_______________________________________________________________________________
_______________________________________________________________________________
_______________________________________________________________________________
_______________________________________________________________________________
_______________________________________________________________________________
_______________________________________________________________________________
```

**What this code does:**

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 5: Plan for Session 23

**Instructions:** Session 23 is your LAST development session. Plan carefully.

**What I still need to build (Must-Have):**

> _______________________________________________________________________________

**What I want to add (Should-Have):**

> _______________________________________________________________________________

**What I will cut if I run out of time (Nice-to-Have):**

> _______________________________________________________________________________

---

##### Reflection

1. What was the hardest part of building your game today?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. Did your game end up different from your GDD plan? If so, how and why?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

*Save your project! Session 23 is your final development session.*

---

### Session 23: Capstone Project — Polish, Testing & Iteration

---

#### SESSION 23 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 23 of 24 |
| **Title** | Capstone Project — Polish, Testing & Iteration |
| **Unit** | Unit 6: Capstone Project & Publishing |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Add polish elements to their capstone game including GUI interfaces, audio (background music and sound effects), and visual feedback that enhance the player experience.
2. Conduct a structured peer playtesting session, giving and receiving specific, actionable feedback using a playtesting form.
3. Identify, prioritise, and fix bugs discovered during playtesting, demonstrating a systematic approach to quality assurance.
4. Prepare their game for publishing by writing a game description, planning a thumbnail, and reviewing game settings.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Capstone project from Sessions 21-22
- Projector or screen-share software for teacher demonstrations
- Session 23 Worksheet (printed or displayed digitally)
- Playtest feedback forms (2 copies per student — one to give, one to receive)
- Timer for structured playtest sessions (10 minutes per round)
- Whiteboard for tracking class-wide common bugs
- Headphones (recommended for audio testing)

##### Procedure

**0-5 min: Warm-Up — "The Final Sprint"**

- Say: *"This is it. Your last development session. After today, the code freezes. Everything you want in your game must be working by the end of this session."*
- Display the session structure:
  - Minutes 0-5: Planning
  - Minutes 5-40: Final development sprint (35 minutes)
  - Minutes 40-60: Peer playtesting (20 minutes)
  - Minutes 60-75: Bug fixing based on feedback (15 minutes)
  - Minutes 75-85: Publishing preparation
  - Minutes 85-90: Closure
- Ask: *"Look at your plan from Session 22. What is the ONE thing you must finish in the next 35 minutes?"*
- Students write their answer on a sticky note and put it on the side of their monitor where they can see it.

**5-40 min: Independent Practice — Final Development Sprint**

- Students work on their capstone projects. This is their final development time. Teacher circulates with urgency:
  - *"Is your core mechanic working? YES? Good — move to polish. NO? Let me help you right now."*
  - Help students who are stuck with targeted, specific solutions.
  - Redirect students who are decorating instead of fixing broken mechanics.

- For students who are on track, suggest these polish priorities:

  **Priority 1: Add a HUD if you do not have one:**
```lua
-- Quick HUD Setup (LocalScript inside StarterGui ScreenGui)

local Players = game:GetService("Players")
local player = Players.LocalPlayer

local screenGui = script.Parent

-- Create score display
local scoreLabel = Instance.new("TextLabel")
scoreLabel.Name = "ScoreLabel"
scoreLabel.AnchorPoint = Vector2.new(0.5, 0)
scoreLabel.Position = UDim2.new(0.5, 0, 0, 10)
scoreLabel.Size = UDim2.new(0, 200, 0, 40)
scoreLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
scoreLabel.BackgroundTransparency = 0.4
scoreLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
scoreLabel.Font = Enum.Font.GothamBold
scoreLabel.TextScaled = true
scoreLabel.Text = "Score: 0"
scoreLabel.Parent = screenGui

local scoreCorner = Instance.new("UICorner")
scoreCorner.CornerRadius = UDim.new(0, 10)
scoreCorner.Parent = scoreLabel

-- Update score from leaderstats
task.spawn(function()
    local leaderstats = player:WaitForChild("leaderstats")
    local score = leaderstats:WaitForChild("Score")
    score.Changed:Connect(function(newValue)
        scoreLabel.Text = "Score: " .. newValue
    end)
    scoreLabel.Text = "Score: " .. score.Value
end)
```

  **Priority 2: Add background music if you do not have it:**
```lua
-- Quick Music Setup (LocalScript in StarterPlayerScripts)

local SoundService = game:GetService("SoundService")

-- Create background music
local music = Instance.new("Sound")
music.Name = "BGMusic"
music.SoundId = "rbxassetid://YOUR_MUSIC_ID_HERE"
music.Looped = true
music.Volume = 0.3
music.Parent = SoundService

task.wait(1)
music:Play()
```

  **Priority 3: Add a win/lose condition if you do not have one:**
```lua
-- Win Condition Example (ServerScriptService)
-- Fires when a player reaches a certain score

local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

local WIN_SCORE = 100

local winEvent = Instance.new("RemoteEvent")
winEvent.Name = "PlayerWon"
winEvent.Parent = ReplicatedStorage

local function checkWinCondition(player)
    local leaderstats = player:FindFirstChild("leaderstats")
    if leaderstats then
        local score = leaderstats:FindFirstChild("Score")
        if score then
            score.Changed:Connect(function(newValue)
                if newValue >= WIN_SCORE then
                    -- This player wins!
                    winEvent:FireClient(player, "YOU WIN! Final Score: " .. newValue)
                    print(player.Name .. " has won the game!")
                end
            end)
        end
    end
end

Players.PlayerAdded:Connect(function(player)
    player.CharacterAdded:Connect(function()
        checkWinCondition(player)
    end)
end)
```

```lua
-- Win Display (LocalScript in StarterGui ScreenGui)

local ReplicatedStorage = game:GetService("ReplicatedStorage")
local winEvent = ReplicatedStorage:WaitForChild("PlayerWon")

local winLabel = Instance.new("TextLabel")
winLabel.Name = "WinLabel"
winLabel.AnchorPoint = Vector2.new(0.5, 0.5)
winLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
winLabel.Size = UDim2.new(0.6, 0, 0.3, 0)
winLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
winLabel.BackgroundTransparency = 0.3
winLabel.TextColor3 = Color3.fromRGB(255, 215, 0)
winLabel.Font = Enum.Font.GothamBold
winLabel.TextScaled = true
winLabel.Text = ""
winLabel.Visible = false
winLabel.Parent = script.Parent

local winCorner = Instance.new("UICorner")
winCorner.CornerRadius = UDim.new(0, 16)
winCorner.Parent = winLabel

winEvent.OnClientEvent:Connect(function(message)
    winLabel.Text = message
    winLabel.Visible = true
end)
```

- At the 35-minute mark, announce: *"PENS DOWN — well, keyboards down. Save your project NOW. In 5 minutes we start playtesting. Your game is about to face its first real players."*

**40-60 min: Guided Practice — Peer Playtesting Session**

- Organise students into pairs (or triads if odd numbers). Each pair takes turns:
  - **Round 1 (10 minutes):** Student A plays Student B's game for 5 minutes. Student A fills in the playtest feedback form for 5 minutes.
  - **Round 2 (10 minutes):** Student B plays Student A's game for 5 minutes. Student B fills in the playtest feedback form for 5 minutes.

- Display the playtesting rules on the board:
  1. Play the game as a REAL player would — do not ask the developer for instructions.
  2. Try to break the game — test edge cases.
  3. Be specific in feedback — "the score does not update when I collect coins" not "it is broken."
  4. Be constructive — one positive comment for every issue you find.
  5. Write EVERYTHING down — the developer cannot fix what they do not know about.

- Circulate during playtesting. Listen for common issues that you can address to the whole class later.

**60-75 min: Independent Practice — Bug Fixing Sprint**

- Students receive their feedback forms and have 15 minutes to fix as many issues as possible.
- Say: *"Focus on CRITICAL and MAJOR bugs only. If the game crashes or a core feature does not work, fix that. Do not spend time on cosmetic issues."*
- Students work independently. Teacher assists with the most critical bugs.

- For common bugs, offer quick fixes on the board:

  **"Score not updating" fix:**
```lua
-- Make sure you are connecting to the Changed event:
score.Changed:Connect(function(newValue)
    scoreLabel.Text = "Score: " .. newValue
end)
-- AND update it once immediately:
scoreLabel.Text = "Score: " .. score.Value
```

  **"Player falls through the floor" fix:**
```lua
-- Add a kill zone far below the map
local killZone = Instance.new("Part")
killZone.Name = "KillZone"
killZone.Size = Vector3.new(2000, 1, 2000)
killZone.Position = Vector3.new(0, -100, 0)
killZone.Anchored = true
killZone.Transparency = 1
killZone.CanCollide = false
killZone.Parent = workspace

killZone.Touched:Connect(function(hit)
    local humanoid = hit.Parent:FindFirstChild("Humanoid")
    if humanoid then
        humanoid.Health = 0
    end
end)
```

  **"Sound not playing" fix:**
```lua
-- Make sure the SoundId is valid and the sound is parented correctly
-- Check the Output for "Sound failed to load" messages
-- Try preloading the sound:
local ContentProvider = game:GetService("ContentProvider")
ContentProvider:PreloadAsync({sound})
sound:Play()
```

**75-85 min: Extension — Publishing Preparation**

- Guide students through preparing their game for publishing:

  1. **Game Title and Description:**
     - Students write a compelling game description (3-5 sentences) on their worksheet.
     - Good description formula: *"What is the game? What does the player do? What makes it special?"*

  2. **Game Settings Preview:**
     - Show the Game Settings window (File > Game Settings in Roblox Studio).
     - Walk through key settings:
       - **Basic Info:** Title, Description, Genre, Max Players
       - **Permissions:** Who can play? (Public, Friends, Private)
       - **Avatar:** R6 or R15? Character collision type?
     - Say: *"We will finalise these settings and publish next session. For now, think about what your settings should be."*

  3. **Thumbnail Planning:**
     - Say: *"The thumbnail is the first thing a player sees. It needs to be eye-catching and show what your game is about."*
     - Students sketch a thumbnail idea on their worksheet.

- Students who finish early can:
  - Create an in-game title screen with the game name and a "Play" button.
  - Add final audio touches.
  - Fix any remaining minor bugs.

**85-90 min: Closure and Preview**

- Say: *"Your game is now as polished as it is going to be. Tomorrow — Session 24 — we publish to Roblox, present to the class, and celebrate. This is the moment you have been working towards for 24 sessions."*
- Preview Session 24 structure:
  - Publishing your game to Roblox
  - 3-5 minute presentations
  - Peer voting and feedback
  - Course reflection and celebration
- Remind students: *"Save your project. Double-save. Triple-save. And come ready to be proud of what you built."*

##### Differentiation

**Support:**
- For students whose games are still broken, offer a "rescue session" — spend 10 minutes of one-on-one time helping them get their core mechanic working. Even a simple working game is a success.
- Provide pre-written game descriptions that students can adapt rather than writing from scratch.
- During playtesting, pair struggling students with patient, supportive testers who will focus on positive feedback while still noting bugs.

**Extension:**
- Challenge advanced students to implement TweenService animations on their GUI elements (buttons that grow on hover, health bars that animate smoothly).
- Ask them to add a loading screen using `ContentProvider:PreloadAsync()` that shows a progress bar while assets load.
- Have them create a settings menu where players can adjust volume, toggle music, or reset their progress.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Polish elements | No polish added | 1 polish element (GUI or audio) partially implemented | GUI, audio, and visual feedback all present and functional | Polished, cohesive game feel with responsive GUI, immersive audio, and clear feedback |
| Playtesting skills | Does not participate in playtesting | Plays partner's game but provides vague or unhelpful feedback | Provides specific, categorised feedback with severity ratings | Provides detailed feedback, identifies root causes, and suggests specific solutions |
| Bug fixing | No bugs fixed after playtesting | Acknowledges bugs but does not fix them | Fixes 3+ bugs from playtest feedback | Fixes all critical/major bugs and verifies fixes through re-testing |
| Publishing preparation | No preparation for publishing | Game title chosen but no description or thumbnail plan | Complete description, thumbnail sketch, and settings plan | Professional description, polished thumbnail concept, and all settings reviewed |

##### Teacher Notes

- The 35-minute development sprint is the last chance for students to add features. Enforce the deadline strictly — playtesting MUST happen today or there will be no time for it before publishing.
- During playtesting, some students will be sensitive about receiving negative feedback. Remind testers to lead with positives: *"I really liked the way you [X]. One thing I noticed was [Y]."*
- The bug fixing sprint is intentionally short (15 minutes). Students must learn to triage — fix the most important bugs first and accept that some minor issues will ship.
- For the publishing preparation, students do NOT publish today — that happens in Session 24. Today is about planning what the published page will look like.
- If a student's game is not functional at all, help them get ONE working feature. Even a single-room game with one collectible and a score counter is a publishable project. The goal is completion, not perfection.
- Take note of which students have games ready for publishing and which need intervention. Plan your Session 24 time accordingly.

---

#### SESSION 23 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 23: Capstone Project — Polish, Testing & Iteration**

---

##### Part 1: Pre-Sprint Priority

**Instructions:** Before you start coding, identify your exact priorities.

**My number one goal for the 35-minute sprint:**

> _______________________________________________________________________________

**Polish checklist — what does my game still need?**

| Element | Have It? | Priority |
|---------|----------|----------|
| HUD / Score display | [ ] Yes [ ] No | [ ] Must [ ] Should [ ] Nice |
| Background music | [ ] Yes [ ] No | [ ] Must [ ] Should [ ] Nice |
| Sound effects | [ ] Yes [ ] No | [ ] Must [ ] Should [ ] Nice |
| Win/lose condition | [ ] Yes [ ] No | [ ] Must [ ] Should [ ] Nice |
| Instructions/tutorial for new players | [ ] Yes [ ] No | [ ] Must [ ] Should [ ] Nice |
| Kill zone / boundaries | [ ] Yes [ ] No | [ ] Must [ ] Should [ ] Nice |
| Game reset / respawn system | [ ] Yes [ ] No | [ ] Must [ ] Should [ ] Nice |

---

##### Part 2: Development Sprint Log

**Instructions:** Record what you build during the 35-minute sprint.

**What I added/fixed:**

> 1. _______________________________________________________________________________
>
> 2. _______________________________________________________________________________
>
> 3. _______________________________________________________________________________
>
> 4. _______________________________________________________________________________

**What I could not finish:**

> _______________________________________________________________________________

---

##### Part 3: Playtest Feedback Form (You Fill This In For Your PARTNER's Game)

**Partner's Name:** _________________________________

**Game Title:** _________________________________

**Time Played:** ___________ minutes

| # | What Happened | Category | Severity | Suggestion |
|---|--------------|----------|----------|------------|
| 1 | _________________________ | [ ] Bug [ ] Balance [ ] UX | [ ] Critical [ ] Major [ ] Minor | _________________________ |
| 2 | _________________________ | [ ] Bug [ ] Balance [ ] UX | [ ] Critical [ ] Major [ ] Minor | _________________________ |
| 3 | _________________________ | [ ] Bug [ ] Balance [ ] UX | [ ] Critical [ ] Major [ ] Minor | _________________________ |
| 4 | _________________________ | [ ] Bug [ ] Balance [ ] UX | [ ] Critical [ ] Major [ ] Minor | _________________________ |
| 5 | _________________________ | [ ] Bug [ ] Balance [ ] UX | [ ] Critical [ ] Major [ ] Minor | _________________________ |

**What I liked most about the game:**

> _______________________________________________________________________________

**One thing that would make it significantly better:**

> _______________________________________________________________________________

**Overall impression (circle one):**

`Needs Work` --- `Getting There` --- `Fun to Play` --- `Would Play Again` --- `Impressive!`

---

##### Part 4: Bug Fix Tracker

**Instructions:** Based on the feedback you RECEIVED, list and fix the issues.

| # | Bug/Issue | How I Fixed It | Verified? |
|---|----------|---------------|-----------|
| 1 | ________________________________ | ________________________________ | [ ] |
| 2 | ________________________________ | ________________________________ | [ ] |
| 3 | ________________________________ | ________________________________ | [ ] |
| 4 | ________________________________ | ________________________________ | [ ] |

---

##### Part 5: Publishing Preparation

**Instructions:** Prepare your game for publishing in Session 24.

**Game Title (final):** _______________________________________________

**Game Description (3-5 sentences):**

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

**Genre:** _________________________________

**Max Players:** _________________________________

**Avatar Type:** [ ] R6 [ ] R15

**Thumbnail Sketch:**

```
+-----------------------------------------------+
|                                               |
|                                               |
|                                               |
|          (Sketch your thumbnail here)         |
|                                               |
|                                               |
|                                               |
+-----------------------------------------------+
```

---

##### Part 6: Game Feature Summary

**Instructions:** List every feature in your final game. This will help you during your presentation.

| # | Feature | Works? | Learned in Unit |
|---|---------|--------|----------------|
| 1 | ________________________________ | [ ] Yes [ ] Partial [ ] No | Unit ____ |
| 2 | ________________________________ | [ ] Yes [ ] Partial [ ] No | Unit ____ |
| 3 | ________________________________ | [ ] Yes [ ] Partial [ ] No | Unit ____ |
| 4 | ________________________________ | [ ] Yes [ ] Partial [ ] No | Unit ____ |
| 5 | ________________________________ | [ ] Yes [ ] Partial [ ] No | Unit ____ |
| 6 | ________________________________ | [ ] Yes [ ] Partial [ ] No | Unit ____ |
| 7 | ________________________________ | [ ] Yes [ ] Partial [ ] No | Unit ____ |
| 8 | ________________________________ | [ ] Yes [ ] Partial [ ] No | Unit ____ |

---

##### Reflection

1. Compare your final game to your original GDD. What changed? Why?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

2. What is the one feature you are most proud of building yourself?

> _______________________________________________________________________________
>
> _______________________________________________________________________________

*SAVE YOUR PROJECT! Tomorrow you publish and present!*

---

### Session 24: Publishing, Presentation & Portfolio Showcase

---

#### SESSION 24 — LESSON PLAN

| Attribute | Details |
|-----------|---------|
| **Session Number** | 24 of 24 |
| **Title** | Publishing, Presentation & Portfolio Showcase |
| **Unit** | Unit 6: Capstone Project & Publishing |
| **Duration** | 90 minutes |
| **Age Group** | 10-15 years old |
| **Difficulty** | Intermediate |

##### Learning Objectives

By the end of this session, students will be able to:

1. Publish a Roblox game to the platform by configuring Game Settings (title, description, genre, max players, permissions, icon, and thumbnail) and clicking Publish to Roblox.
2. Deliver a structured 3-5 minute presentation covering their game concept, core mechanic, technical implementation, challenges faced, and lessons learned.
3. Provide constructive peer feedback using a structured rubric that evaluates gameplay, polish, creativity, and technical skill.
4. Reflect on their learning journey across the entire course and document their capstone project as a portfolio piece.

##### Materials Needed

- Computer with Roblox Studio installed (one per student or pair)
- Completed capstone project from Sessions 21-23
- Projector or screen-share software for student presentations
- Session 24 Worksheet (printed or displayed digitally)
- Peer feedback forms (one per student per presentation)
- Timer for presentations (visible to presenter — 3-5 minute limit)
- Optional: certificates of completion (teacher prepares in advance)
- Optional: small prizes or recognition for peer-voted categories (Most Creative, Best Gameplay, Best Polish, Most Ambitious)
- Whiteboard for displaying presentation order

##### Procedure

**0-5 min: Warm-Up — "Look How Far You Have Come"**

- Display the course journey on the board:
  ```
  Session 1: "What is Roblox Studio?"
  Session 6: "I can build parts and script basic interactions"
  Session 12: "I can create physics systems and game mechanics"
  Session 18: "I can add audio and GUI to make games feel real"
  Session 24: "I built and published a COMPLETE GAME"
  ```
- Say: *"Twenty-four sessions ago, some of you had never opened Roblox Studio. Today, you are publishing games to a platform with millions of players. Take a moment to appreciate what you have accomplished."*
- Ask: *"By a show of hands — who is proud of what they built?"*
- Say: *"Today is a celebration. We publish, we present, we play each other's games, and we reflect. Let us begin."*

**5-15 min: Guided Practice — Publishing to Roblox**

- Walk through the publishing process on the projector. Every student follows along:

  **Step 1: Open Game Settings**
  - Go to File > Game Settings (or click the Game Settings button in the Home tab).

  **Step 2: Configure Basic Info**
  - **Name:** Enter the game title from the GDD.
  - **Description:** Paste the description written in Session 23.
  - **Genre:** Select the appropriate genre.
  - **Max Players:** Set based on game type (1 for single player, 2-12 for multiplayer).

  **Step 3: Set Permissions**
  - For the showcase: set to **Public** so classmates can play.
  - Discuss privacy: *"If you want only friends to play, you can set it to Friends Only. For today's showcase, let us keep it Public so everyone can try your game."*

  **Step 4: Configure Avatar**
  - Choose R6 or R15 based on the game design.
  - Set collision type if needed.

  **Step 5: Set the Icon and Thumbnail**
  - Show how to upload a custom icon (512x512 image) or use the auto-generated one.
  - Show how to take a screenshot in-game for the thumbnail.
  - Say: *"The icon and thumbnail are the first things players see. Make them count."*

  **Step 6: Publish**
  - Go to File > Publish to Roblox (or Publish to Roblox As if this is the first time).
  - Wait for the upload to complete. Show the confirmation.
  - Say: *"Your game is now LIVE. Anyone in the world with a Roblox account can find and play it. Congratulations."*

- Quick alternative for students without publishing permissions: save the `.rbxl` file and demonstrate the publishing flow without actually going live. The key learning is understanding the process.

- Give students 5 minutes to publish their own games. Circulate and troubleshoot:
  - Common issue: "Cannot publish" — check that the student is logged into Roblox Studio with a valid account.
  - Common issue: "Description rejected" — Roblox filters descriptions for inappropriate content. Help students rephrase.

**15-35 min: Independent Practice — Preparing Presentations**

- Give students 10 minutes to prepare their presentations using the worksheet guide. Each presentation should cover:
  1. **Game Title and Concept** (30 seconds) — What is the game? What inspired it?
  2. **Live Demo** (1-2 minutes) — Play the game on the projector. Show the core mechanic in action.
  3. **Technical Highlights** (1 minute) — What was the most challenging script? What systems did you use? Show one piece of code you are proud of.
  4. **Challenges and Lessons** (30 seconds) — What went wrong? What did you learn?
  5. **What I Would Add Next** (30 seconds) — If you had more time, what would you build?

- Display the presentation structure on the board. Say: *"You have 3 to 5 minutes. Practise timing yourself. I will give you a 1-minute warning."*

- While students prepare, write the presentation order on the board. Options for ordering:
  - Volunteers first, then alphabetical.
  - Random order (draw names from a hat for excitement).
  - By game genre (all obbies, then all fighters, then all tycoons).

- Students may use their GDD and worksheet as notes during the presentation.

**35-75 min: Sharing — Student Presentations**

- Each student presents for 3-5 minutes. With a class of 15-20 students, this takes approximately 40 minutes (aiming for 3-4 minutes average including transition time).

- Presentation protocol:
  - Timer visible to the presenter.
  - 1-minute warning sign held up by the teacher.
  - After each presentation: the class gives 10 seconds of applause, then one student asks one question.
  - Peer feedback forms are filled in quietly during or immediately after each presentation.

- For each presentation, the teacher takes brief notes for the assessment rubric.

- After all presentations, conduct a quick peer vote (by ballot or hand raise):
  - **Most Creative Game** — the most original concept.
  - **Best Gameplay** — the most fun to play.
  - **Best Polish** — the most professional-looking and sounding.
  - **Most Ambitious** — the game that attempted the most challenging features.
  - (Optional: **People's Choice** — overall favourite)

- Announce winners. Emphasise: *"Every game presented today is a game that DID NOT EXIST 24 sessions ago. Every single one of you created something from nothing. That is what game development is."*

**75-85 min: Extension — Course Reflection and Portfolio Documentation**

- Students complete the course reflection section of their worksheet:
  1. Rate their own growth from Session 1 to Session 24.
  2. Identify their three biggest technical skills gained.
  3. Write one paragraph about their capstone game for a portfolio.
  4. Set one goal for continued learning.

- For students interested in continuing:
  - Mention resources: Roblox Creator Documentation, DevForum, YouTube tutorials.
  - Mention possible next steps: Advanced Roblox course, learning another engine (Godot, Unity), game jams.

- Portfolio documentation guide:

```
PORTFOLIO ENTRY TEMPLATE
=========================
Game Title: _______________
Platform: Roblox
Role: Solo Developer (Designer, Programmer, Artist)
Development Time: 4 sessions (approximately 6 hours)
Tools Used: Roblox Studio, Luau scripting language

Description:
[2-3 sentences about the game]

Technical Features:
- [Feature 1]
- [Feature 2]
- [Feature 3]

Skills Demonstrated:
- [Skill 1]
- [Skill 2]
- [Skill 3]

Link: [Roblox game URL]
```

**85-90 min: Closure — Course Celebration**

- Final words: *"When this course started, you were students learning a tool. Today, you are game developers who published a game. That is not just a skill — it is an identity. You are someone who can turn ideas into interactive experiences. Whatever you do next — whether you become a professional developer, a hobbyist, or never touch a game engine again — you now know that you can BUILD things. And that knowledge never goes away."*
- If certificates are prepared, hand them out.
- Final applause for the class.
- Remind students: *"Your published game is live on Roblox. Share the link with friends and family. You earned it."*

##### Differentiation

**Support:**
- For students who are nervous about presenting, allow them to present to the teacher privately or in a small group rather than the whole class.
- Provide presentation cue cards with sentence starters: "My game is called...", "The player's goal is to...", "The hardest part was...", "I am proud of..."
- If a student's game is not publishable, help them save the `.rbxl` file and explain the publishing process verbally. Focus their presentation on what they learned rather than the final product.

**Extension:**
- Challenge advanced students to create a game page trailer: a short in-game recording (using Roblox's built-in recorder or screen capture) showing the best moments of their game.
- Ask them to write a post-mortem document (a professional game development practice): what went right, what went wrong, and what they would do differently.
- Have them plan a "Version 2.0" feature list for continued development after the course.

##### Assessment Criteria

| Criterion | Not Yet (0) | Developing (1) | Proficient (2) | Mastery (3) |
|-----------|-------------|----------------|----------------|-------------|
| Publishing | Game not published or saved | Game saved locally but not published | Game published with title and description | Game published with complete settings, description, genre, appropriate max players, and thumbnail |
| Presentation quality | Does not present | Presents but is unclear, very short, or missing sections | Covers all 5 sections clearly within time limit | Engaging, well-structured presentation with live demo, technical insight, and honest reflection |
| Peer feedback | Does not provide feedback to others | Provides vague or unhelpful feedback | Provides specific, constructive feedback on 3+ presentations | Provides detailed feedback with actionable suggestions and positive observations |
| Course reflection | No reflection completed | Surface-level reflection ("it was fun") | Identifies specific skills gained and honest self-assessment | Deep reflection connecting skills to future goals, with portfolio-quality documentation |

##### Teacher Notes

- Publishing requires students to be logged into Roblox Studio with an account. If students do not have accounts, they can still save the `.rbxl` file and demonstrate the publishing flow. The learning outcome is understanding the process, not necessarily having a live game.
- Presentations are the highlight of the course. Create a positive, celebratory atmosphere. No negative comments during presentations — all feedback goes through the written peer forms.
- Time management is critical. With 20 students at 4 minutes each, presentations alone take 80 minutes. If the class is large, consider splitting presentations across two half-sessions or limiting to 3 minutes strictly.
- Some students will be embarrassed about their game if it is simple or broken. Emphasise repeatedly: *"The goal is not perfection. The goal is completion. A finished simple game is more impressive than an unfinished ambitious one."*
- The peer voting categories are designed so that different students can win different awards. A simple but creative game can win "Most Creative" even if a technically superior game wins "Best Polish."
- Collect all worksheets and feedback forms. These, combined with the published games, form the complete assessment portfolio for the course.
- If time permits at the end, let students play each other's published games on their own devices. This is the most rewarding moment of the course — seeing someone else enjoy what you built.

---

#### SESSION 24 — WORKSHEET

---

**Student Name:** ________________________________________ **Date:** ____________________

**Session 24: Publishing, Presentation & Portfolio Showcase**

---

##### Part 1: Publishing Checklist

**Instructions:** Follow each step to publish your game to Roblox.

1. [ ] Open your capstone project in Roblox Studio.
2. [ ] Go to **File > Game Settings**.
3. [ ] Set the following:
   - Game Name: _______________________________________________
   - Description: (copy from Session 23 worksheet)
   - Genre: _______________________________________________
   - Max Players: _______________
4. [ ] Set Permissions to **Public** (for today's showcase).
5. [ ] Review Avatar settings (R6/R15): _______________
6. [ ] Click **Save** in Game Settings.
7. [ ] Go to **File > Publish to Roblox** (or **Publish to Roblox As**).
8. [ ] Wait for the upload to complete.
9. [ ] Confirmation received? [ ] Yes [ ] No

**My game URL:** _______________________________________________

---

##### Part 2: Presentation Preparation

**Instructions:** Prepare your 3-5 minute presentation. Write notes for each section.

**1. Game Title and Concept (30 seconds):**

> My game is called _______________________________________________
>
> It is a _____________ game where the player _______________________________________________
>
> I was inspired by _______________________________________________

**2. Live Demo Plan (1-2 minutes):**

What will you show during the demo? List the key moments:

> 1. _______________________________________________________________________________
>
> 2. _______________________________________________________________________________
>
> 3. _______________________________________________________________________________

**3. Technical Highlights (1 minute):**

What was the most challenging code you wrote? Describe it in plain language:

> _______________________________________________________________________________
>
> _______________________________________________________________________________

What systems from the course did you use?
- [ ] GUI / ScreenGui
- [ ] SoundService / Audio
- [ ] Teams / Multiplayer
- [ ] Leaderstats / Scoring
- [ ] Touched events / Collisions
- [ ] RemoteEvents / Client-Server
- [ ] Round system / Timer
- [ ] Other: _______________

**4. Challenges and Lessons (30 seconds):**

The biggest challenge I faced was:

> _______________________________________________________________________________

What I learned from it:

> _______________________________________________________________________________

**5. What I Would Add Next (30 seconds):**

If I had 4 more sessions, I would add:

> _______________________________________________________________________________

---

##### Part 3: Peer Feedback Form

**Instructions:** Fill in this form for EACH game presented. Be specific and constructive.

**Presenter's Name:** _________________________________

**Game Title:** _________________________________

| Category | Rating (1-5) | Comments |
|----------|-------------|----------|
| **Gameplay** — Is it fun? Is the core mechanic clear? | _____ | ________________________________ |
| **Polish** — Does it look and sound good? | _____ | ________________________________ |
| **Creativity** — Is the concept original or interesting? | _____ | ________________________________ |
| **Technical Skill** — Does it use multiple systems well? | _____ | ________________________________ |

**Best thing about this game:**

> _______________________________________________________________________________

**One suggestion for improvement:**

> _______________________________________________________________________________

---

*(Copy this form for each presenter — you may need additional paper)*

---

##### Part 4: Peer Voting

**Instructions:** After all presentations, vote for your favourites. You CANNOT vote for yourself.

| Award | My Vote (Student Name) |
|-------|----------------------|
| **Most Creative Game** | ________________________________ |
| **Best Gameplay** | ________________________________ |
| **Best Polish** | ________________________________ |
| **Most Ambitious** | ________________________________ |
| **People's Choice** (overall favourite) | ________________________________ |

---

##### Part 5: Course Reflection

**Instructions:** Look back across all 24 sessions. Answer each question honestly and thoughtfully.

**1. Rate your growth from Session 1 to Session 24:**

`No Growth` --- `Some Growth` --- `Significant Growth` --- `Huge Growth` --- `I Am a Different Developer`

**2. Three technical skills I gained during this course:**

| # | Skill | How confident am I? (1-5) |
|---|-------|--------------------------|
| 1 | ________________________________ | _____ |
| 2 | ________________________________ | _____ |
| 3 | ________________________________ | _____ |

**3. My favourite session of the entire course was Session _____ because:**

> _______________________________________________________________________________
>
> _______________________________________________________________________________

**4. The most difficult concept I learned was:**

> _______________________________________________________________________________
>
> Do I understand it now? [ ] Yes [ ] Mostly [ ] Still learning

**5. One thing I wish we had spent more time on:**

> _______________________________________________________________________________

**6. Advice I would give to a student starting this course next year:**

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Part 6: Portfolio Documentation

**Instructions:** Write a portfolio entry for your capstone game. This can be shown to future teachers, schools, or employers.

```
PORTFOLIO ENTRY
===============

Game Title: _______________________________________________

Platform: Roblox

Role: Solo Developer (Designer, Programmer, Artist)

Development Time: _______ sessions (approximately _______ hours)

Tools Used: Roblox Studio, Luau scripting language

Description (2-3 sentences):
_______________________________________________________________________________
_______________________________________________________________________________
_______________________________________________________________________________

Technical Features:
- _______________________________________________________________________________
- _______________________________________________________________________________
- _______________________________________________________________________________
- _______________________________________________________________________________

Skills Demonstrated:
- _______________________________________________________________________________
- _______________________________________________________________________________
- _______________________________________________________________________________

Challenges Overcome:
- _______________________________________________________________________________
- _______________________________________________________________________________

Game Link: _______________________________________________
```

---

##### Part 7: What Comes Next?

**Instructions:** Game development does not end with this course! Set a goal for your continued learning.

**My next learning goal:**

> _______________________________________________________________________________

**Resources I want to explore:**

- [ ] Roblox Creator Documentation (create.roblox.com/docs)
- [ ] Roblox DevForum (devforum.roblox.com)
- [ ] YouTube tutorials (channel: _______________)
- [ ] Another game engine (Godot, Unity, Unreal)
- [ ] Game jams (build a game in 24-48 hours)
- [ ] Other: _______________________________________________

**One game I want to build next:**

> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

##### Final Reflection

Write a short paragraph (4-6 sentences) about your experience in this course. What did you learn? How did you grow? What are you most proud of?

> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________
>
> _______________________________________________________________________________

---

*Congratulations on completing the Roblox Studio Intermediate course! You are now a game developer. Keep building, keep learning, keep creating.*
