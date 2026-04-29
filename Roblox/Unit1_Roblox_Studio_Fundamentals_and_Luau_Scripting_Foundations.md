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
