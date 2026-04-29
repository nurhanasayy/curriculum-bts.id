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
