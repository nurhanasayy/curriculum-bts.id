# Roblox Studio Intermediate Game Development Curriculum
## Cambridge-Aligned Computing Course

---

## Table of Contents

- [Course Overview](#course-overview)
- [Cambridge Computing Standards Alignment](#cambridge-computing-standards-alignment)
- [Learning Objectives](#learning-objectives)

### Unit 1: Roblox Studio Fundamentals & Luau Scripting Foundations (Sessions 1-4)
- [Session 1: Course Introduction & Roblox Studio Environment](#session-1-course-introduction--roblox-studio-environment)
- [Session 2: Explorer, Properties, Parts, and Models](#session-2-explorer-properties-parts-and-models)
- [Session 3: Luau Scripting Fundamentals - Variables and Data Types](#session-3-luau-scripting-fundamentals---variables-and-data-types)
- [Session 4: Control Flow and Functions in Luau](#session-4-control-flow-and-functions-in-luau)

### Unit 2: Game Mechanics & Player Interaction (Sessions 5-8)
- [Session 5: Player Character and Humanoid](#session-5-player-character-and-humanoid)
- [Session 6: Touched Events, Tools, and Weapons](#session-6-touched-events-tools-and-weapons)
- [Session 7: Collectibles, Scoring, and Leaderboards](#session-7-collectibles-scoring-and-leaderboards)
- [Session 8: Project 1 - Obstacle Course (Obby) with Scoring](#session-8-project-1---obstacle-course-obby-with-scoring)

### Unit 3: Advanced Scripting & Data Systems (Sessions 9-12)
- [Session 9: Tables and Arrays](#session-9-tables-and-arrays)
- [Session 10: ModuleScripts and Code Organization](#session-10-modulescripts-and-code-organization)
- [Session 11: RemoteEvents and Client-Server Model](#session-11-remoteevents-and-client-server-model)
- [Session 12: Project 2 - Tycoon Game](#session-12-project-2---tycoon-game)

### Unit 4: Game World Design & Advanced Mechanics (Sessions 13-16)
- [Session 13: Terrain Editor and World Building](#session-13-terrain-editor-and-world-building)
- [Session 14: Lighting, Atmosphere, and Visual Effects](#session-14-lighting-atmosphere-and-visual-effects)
- [Session 15: TweenService and NPC Creation with Pathfinding](#session-15-tweenservice-and-npc-creation-with-pathfinding)
- [Session 16: Project 3 - Adventure/RPG Game](#session-16-project-3---adventurerpg-game)

### Unit 5: Multiplayer Systems & Game Polish (Sessions 17-20)
- [Session 17: GUI Design - ScreenGui, TextLabel, TextButton, Frame](#session-17-gui-design---screengui-textlabel-textbutton-frame)
- [Session 18: SoundService and Audio Implementation](#session-18-soundservice-and-audio-implementation)
- [Session 19: Teams and Multiplayer Mechanics](#session-19-teams-and-multiplayer-mechanics)
- [Session 20: Game Balancing and Playtesting](#session-20-game-balancing-and-playtesting)

### Unit 6: Capstone Project & Publishing (Sessions 21-24)
- [Session 21: Capstone Project - Game Design Document and Planning](#session-21-capstone-project---game-design-document-and-planning)
- [Session 22: Capstone Project - Core Development](#session-22-capstone-project---core-development)
- [Session 23: Capstone Project - Polish and Testing](#session-23-capstone-project---polish-and-testing)
- [Session 24: Publishing to Roblox and Portfolio Showcase](#session-24-publishing-to-roblox-and-portfolio-showcase)

### Assessment & Resources
- [Assessment Framework](#assessment-framework)
- [Resources and Materials](#resources-and-materials)
- [Differentiation Strategies](#differentiation-strategies)
- [Teacher Notes](#teacher-notes)
- [Appendices](#appendices)
- [Sources and References](#sources-and-references)

---

### Course Overview

| Attribute | Details |
|-----------|---------|
| **Subject** | Game Development with Roblox Studio |
| **Level** | Intermediate |
| **Age Group** | 10-15 years old |
| **Total Sessions** | 24 sessions |
| **Session Duration** | 90 minutes per session |
| **Total Hours** | 36 hours |
| **Prerequisites** | Basic computer literacy, familiarity with gaming concepts, introductory programming concepts (variables, basic logic) |
| **Software** | Roblox Studio (free, requires Roblox account) |
| **Programming Language** | Luau (Roblox's Lua variant) |

---

### Cambridge Computing Standards Alignment

This curriculum aligns with the **Cambridge Lower Secondary Computing (0860)** and prepares students for **Cambridge IGCSE Computer Science (0478)** through the following strands:

| Cambridge Strand | Coverage in This Course |
|------------------|-------------------------|
| **Computational Thinking** | Algorithm design, decomposition, abstraction, pattern recognition, debugging game logic |
| **Programming** | Luau syntax, variables, functions, tables, ModuleScripts, client-server architecture |
| **Managing Data** | Data types, tables/arrays, DataStoreService for persistence, leaderboards |
| **Networks & Digital Communication** | Client-server model, RemoteEvents, multiplayer networking, game publishing |
| **Computer Systems** | Game engine architecture, rendering, physics simulation, server-client execution model |

---

### Learning Objectives

By the end of this course, students will be able to:

1. **Programming Proficiency**
   - Write clean, organized Luau code following best practices
   - Implement modular programming with ModuleScripts
   - Use tables, arrays, and data structures effectively
   - Debug code using print statements, the Output window, and the Script Analysis tool

2. **Roblox Studio Mastery**
   - Navigate and utilize the Roblox Studio editor efficiently
   - Understand the Explorer hierarchy and Properties panel
   - Work with Parts, Models, Services, and the data model
   - Implement client-server communication with RemoteEvents

3. **Game Development Skills**
   - Build complete 3D games from concept to publication
   - Implement player mechanics, scoring, and game systems
   - Design game worlds using the Terrain Editor and building tools
   - Create polished games with GUI, audio, and visual effects

4. **Computational Thinking**
   - Decompose complex problems into manageable components
   - Design algorithms using pseudocode and flowcharts
   - Test and debug programs systematically
   - Evaluate and optimize solutions for performance

---

## Unit 1: Roblox Studio Fundamentals & Luau Scripting Foundations
### Sessions 1-4

---

### Session 1: Course Introduction & Roblox Studio Environment

**Cambridge Alignment:** Computer Systems, Computational Thinking

**Learning Objectives:**
- Understand course structure and assessment criteria
- Navigate the Roblox Studio interface
- Create and save a new place (project)

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Icebreaker: favourite Roblox games and what makes them fun |
| 10-25 min | Introduction | Course overview, what we will build, expectations, portfolio goals |
| 25-35 min | Discussion | Why Roblox Studio? Free platform, massive player base, career paths in game development |
| 35-60 min | Guided Practice | Interface tour: Explorer, Properties, Toolbox, Output, Command Bar |
| 60-80 min | Independent Practice | Create first place, add Parts, change colours and materials, test play |
| 80-85 min | Extension | Explore the Toolbox and insert free models; examine their Explorer structure |
| 85-90 min | Closure | Learning journal setup, reflection on personal goals for the course |

**Key Concepts:**
- Roblox Studio is free and publishes directly to the Roblox platform
- The data model: Workspace, Players, ServerScriptService, ReplicatedStorage, StarterGui, StarterPack
- Place vs. game (experience) terminology
- Documentation and help resources (Roblox Creator Hub)

**Roblox Studio Interface Overview:**

| Panel | Purpose |
|-------|---------|
| Explorer | View and manage the instance hierarchy (all objects in the game) |
| Properties | Edit attributes of the selected instance (size, colour, material, etc.) |
| Toolbox | Browse and insert free models, plugins, and assets |
| Output | View print statements, warnings, and errors |
| Command Bar | Execute Luau code directly for quick testing |
| Asset Manager | Manage imported images, meshes, audio, and other assets |

**Assessment:**
- Formative: Interface navigation quiz (identify panels and their purposes)
- Learning journal: Write three personal goals for the course

**Resources:**
- Roblox Studio installed with student Roblox accounts
- Learning journal template
- [Roblox Creator Hub Documentation](https://create.roblox.com/docs)

---

### Session 2: Explorer, Properties, Parts, and Models

**Cambridge Alignment:** Computer Systems, Computational Thinking

**Learning Objectives:**
- Understand the Explorer hierarchy and parent-child relationships
- Create, manipulate, and group Parts into Models
- Use the Properties panel to modify instance attributes

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Quick review: name three panels in Roblox Studio and their purposes |
| 10-25 min | Introduction | The data model explained: everything is an instance with a parent |
| 25-40 min | Guided Practice | Create Parts (Block, Sphere, Cylinder, Wedge), resize, rotate, recolour |
| 40-65 min | Independent Practice | Build a small structure (house or tower) using Parts grouped into Models |
| 65-75 min | Guided Practice | Anchoring, CanCollide, Transparency, and other essential properties |
| 75-85 min | Extension | Add a SpawnLocation and test the game with a player character |
| 85-90 min | Closure | Exit ticket: draw and label the Explorer hierarchy of your structure |

**Key Concepts:**

```
Explorer Hierarchy:
Workspace
├── Baseplate (Part)
├── SpawnLocation
├── House (Model)
│   ├── Wall1 (Part)
│   ├── Wall2 (Part)
│   ├── Roof (Part)
│   └── Door (Part)
├── Camera
└── Terrain
```

**Common Part Properties:**

| Property | Purpose | Example Values |
|----------|---------|----------------|
| Size | Dimensions in studs (X, Y, Z) | Vector3.new(4, 1, 2) |
| Position | Location in 3D space | Vector3.new(0, 5, 0) |
| BrickColor | Colour of the Part | BrickColor.new("Bright red") |
| Material | Surface appearance | Enum.Material.Wood |
| Anchored | Whether physics affects it | true / false |
| CanCollide | Whether players can pass through | true / false |
| Transparency | Visibility (0 = opaque, 1 = invisible) | 0.5 |

**Instance Hierarchy Concepts:**
```
Instance Relationships:
- Parent: the container that holds an object
- Children: objects contained within a parent
- Descendants: all objects nested at any depth
- Ancestors: all parents up the hierarchy chain

Example:
game.Workspace.House.Door  -- full path to Door
Door.Parent                -- returns House (Model)
House:GetChildren()        -- returns {Wall1, Wall2, Roof, Door}
```

**Assessment:**
- Build a structure with at least 6 Parts grouped into a Model
- Written: Explain parent-child relationships using your own project as an example

---

### Session 3: Luau Scripting Fundamentals - Variables and Data Types

**Cambridge Alignment:** Programming, Managing Data

**Learning Objectives:**
- Declare and use variables in Luau
- Understand data types (string, number, boolean, nil)
- Write and insert Scripts; use print() and comments

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Discussion: what is a script and why do games need them? |
| 10-25 min | Introduction | Luau overview: Roblox's version of Lua, typed and fast |
| 25-40 min | Guided Practice | Insert a Script into Workspace, write first print("Hello, World!") |
| 40-65 min | Independent Practice | Declare variables of each type, print results to Output |
| 65-80 min | Guided Practice | String concatenation, arithmetic operations, type() function |
| 80-85 min | Extension | Type conversion with tostring() and tonumber() |
| 85-90 min | Closure | Debug challenge: fix five broken code snippets |

**Luau Variable Declaration:**

```lua
-- Single-line comment

--[[
    Multi-line comment
    Block comments for longer explanations
]]

-- Variables (local is best practice)
local playerName = "Hero"       -- string
local health = 100              -- number (integer)
local speed = 5.5               -- number (float)
local isAlive = true            -- boolean
local weapon = nil              -- nil (no value)

-- Constants (naming convention: UPPER_CASE)
local MAX_HEALTH = 100
local GRAVITY = 196.2

-- Printing to Output
print("Player name:", playerName)
print("Health:", health)
print("Type of speed:", type(speed))

-- String concatenation
local greeting = "Welcome, " .. playerName .. "!"
print(greeting)

-- Arithmetic operations
local damage = 25
health = health - damage
print("Health after damage:", health)
```

**Data Types Reference:**

| Type | Example | Description |
|------|---------|-------------|
| string | `"Hello"` | Text enclosed in quotes |
| number | `42` or `3.14` | Whole numbers and decimals |
| boolean | `true` / `false` | Logical true or false |
| nil | `nil` | Represents no value or absence |
| table | `{1, 2, 3}` | Collection of values (covered in Unit 3) |
| function | `function() end` | Reusable block of code |
| Instance | `game.Workspace.Part` | Roblox object reference |

**Script Types in Roblox:**

| Script Type | Runs On | Location |
|-------------|---------|----------|
| Script | Server | ServerScriptService, Workspace |
| LocalScript | Client | StarterPlayerScripts, StarterGui, StarterPack |
| ModuleScript | Wherever required | ReplicatedStorage, ServerScriptService |

**Assessment:**
- Script with 5+ correctly declared variables of different types
- Debug challenge: fix type-related errors in provided code

---

### Session 4: Control Flow and Functions in Luau

**Cambridge Alignment:** Programming, Computational Thinking

**Learning Objectives:**
- Implement conditional statements (if/elseif/else)
- Use loops (for, while, repeat-until) effectively
- Define and call custom functions with parameters and return values

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Algorithm design: write pseudocode for a health check system |
| 10-25 min | Introduction | Conditionals: if, elseif, else; comparison and logical operators |
| 25-45 min | Guided Practice | Implement a health checker that prints different messages |
| 45-65 min | Independent Practice | Loops: numeric for, generic for (ipairs/pairs), while, repeat-until |
| 65-80 min | Guided Practice | Functions with parameters and return values |
| 80-85 min | Extension | Nested conditionals and functions calling other functions |
| 85-90 min | Closure | Peer review: swap scripts with a partner and trace through the logic |

**Control Flow Examples:**

```lua
-- Conditionals
local function checkHealth(health)
    if health <= 0 then
        print("Player has been defeated!")
    elseif health < 25 then
        print("Warning: Low health!")
    elseif health < 50 then
        print("Health is moderate.")
    else
        print("Health is good!")
    end
end

-- Comparison operators: ==, ~= (not equal), <, >, <=, >=
-- Logical operators: and, or, not

-- Numeric for loop
for i = 1, 10 do
    print("Count:", i)
end

-- Numeric for loop with step
for i = 10, 1, -1 do
    print("Countdown:", i)
end

-- While loop
local count = 0
while count < 5 do
    count = count + 1
    print("While count:", count)
end

-- Repeat-until loop (runs at least once)
local attempts = 0
repeat
    attempts = attempts + 1
    print("Attempt:", attempts)
until attempts >= 3
```

**Functions:**

```lua
-- Basic function
local function greetPlayer(name)
    print("Welcome to the game, " .. name .. "!")
end

greetPlayer("Alex")

-- Function with return value
local function calculateDamage(baseDamage, multiplier)
    local totalDamage = baseDamage * multiplier
    return totalDamage
end

local damage = calculateDamage(10, 1.5)
print("Damage dealt:", damage)

-- Function with multiple returns
local function getPlayerStats()
    return 100, 50, 3  -- health, mana, lives
end

local health, mana, lives = getPlayerStats()
print("Health:", health, "Mana:", mana, "Lives:", lives)
```

**Common Roblox Callback Patterns:**

```lua
-- Script that runs when the game starts
local Players = game:GetService("Players")

-- Function called when a player joins
Players.PlayerAdded:Connect(function(player)
    print(player.Name .. " has joined the game!")
end)

-- Function called when a player leaves
Players.PlayerRemoving:Connect(function(player)
    print(player.Name .. " has left the game.")
end)
```

**Assessment:**
- Implement a complete health check system using conditionals and functions
- Algorithm design: write pseudocode before coding, then implement in Luau

---

## Unit 2: Game Mechanics & Player Interaction
### Sessions 5-8

---

### Session 5: Player Character and Humanoid

**Cambridge Alignment:** Programming, Computer Systems

**Learning Objectives:**
- Understand the Player and Character model structure
- Access and modify Humanoid properties (WalkSpeed, JumpPower, Health)
- Respond to player join and character spawn events

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Explore the Explorer tree: what objects appear when a player spawns? |
| 10-25 min | Introduction | Player vs. Character, Humanoid service, character model hierarchy |
| 25-45 min | Guided Practice | Script to modify WalkSpeed and JumpPower on character spawn |
| 45-70 min | Independent Practice | Create speed boost pads and low-gravity zones |
| 70-80 min | Extension | Humanoid.Died event: respawn messages and effects |
| 80-85 min | Extension | Health regeneration system using a while loop |
| 85-90 min | Closure | Reflection: diagram the Character model hierarchy |

**Character Model Hierarchy:**

```
Player (in Players service)
└── Character (Model, in Workspace when spawned)
    ├── Head (MeshPart)
    ├── Torso / UpperTorso (MeshPart)
    ├── Left Arm / LeftUpperArm (MeshPart)
    ├── Right Arm / RightUpperArm (MeshPart)
    ├── Left Leg / LeftUpperLeg (MeshPart)
    ├── Right Leg / RightUpperLeg (MeshPart)
    ├── HumanoidRootPart (Part) -- the root, controls position
    ├── Humanoid -- controls health, speed, jump, animations
    └── Animate (LocalScript)
```

**Humanoid Properties:**

| Property | Default | Description |
|----------|---------|-------------|
| Health | 100 | Current health points |
| MaxHealth | 100 | Maximum health points |
| WalkSpeed | 16 | Movement speed (studs/sec) |
| JumpPower | 50 | Jump force |
| JumpHeight | 7.2 | Alternative to JumpPower (UseJumpPower must be false) |

**Player and Character Script:**

```lua
-- ServerScriptService > Script
local Players = game:GetService("Players")

local function onCharacterAdded(character)
    local humanoid = character:WaitForChild("Humanoid")

    -- Modify properties
    humanoid.WalkSpeed = 20
    humanoid.JumpPower = 60

    -- Listen for death
    humanoid.Died:Connect(function()
        print(character.Name .. " has been defeated!")
    end)
end

local function onPlayerAdded(player)
    print(player.Name .. " joined the game!")

    -- Handle current character and future respawns
    player.CharacterAdded:Connect(onCharacterAdded)

    -- If character already exists
    if player.Character then
        onCharacterAdded(player.Character)
    end
end

Players.PlayerAdded:Connect(onPlayerAdded)
```

**Speed Boost Pad:**

```lua
-- Script inside a Part (the speed pad)
local speedPad = script.Parent
local BOOST_SPEED = 50
local BOOST_DURATION = 3
local NORMAL_SPEED = 16

speedPad.Touched:Connect(function(hit)
    local humanoid = hit.Parent:FindFirstChildOfClass("Humanoid")
    if humanoid then
        humanoid.WalkSpeed = BOOST_SPEED
        task.wait(BOOST_DURATION)
        humanoid.WalkSpeed = NORMAL_SPEED
    end
end)
```

**Assessment:**
- Modify player properties on spawn (WalkSpeed, JumpPower)
- Create at least one interactive pad (speed boost or low-gravity zone)

---

### Session 6: Touched Events, Tools, and Weapons

**Cambridge Alignment:** Programming, Computational Thinking

**Learning Objectives:**
- Use the Touched event for player-object interaction
- Implement debounce to prevent event spam
- Create basic Tools for the player's inventory

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Review: what happens when a Part fires the Touched event? |
| 10-25 min | Introduction | Touched and TouchEnded events, debounce pattern |
| 25-45 min | Guided Practice | Build a kill brick and a healing zone with debounce |
| 45-65 min | Guided Practice | Creating a Tool: Handle, Script, activation with Equipped/Activated |
| 65-80 min | Independent Practice | Create a custom sword or wand Tool |
| 80-85 min | Extension | Add visual effects (particle emitter) to the Tool on activation |
| 85-90 min | Closure | Exit ticket: explain why debounce is important |

**Debounce Pattern:**

```lua
-- Kill brick with debounce
local killBrick = script.Parent
local debounce = false

killBrick.Touched:Connect(function(hit)
    if debounce then return end

    local humanoid = hit.Parent:FindFirstChildOfClass("Humanoid")
    if humanoid then
        debounce = true
        humanoid.Health = 0
        task.wait(1)  -- cooldown period
        debounce = false
    end
end)
```

**Healing Zone:**

```lua
-- Healing zone: heals players while they stand inside
local healZone = script.Parent
local HEAL_RATE = 5  -- health per second

healZone.Touched:Connect(function(hit)
    local humanoid = hit.Parent:FindFirstChildOfClass("Humanoid")
    if humanoid then
        while humanoid and humanoid.Health < humanoid.MaxHealth do
            humanoid.Health = math.min(humanoid.Health + HEAL_RATE, humanoid.MaxHealth)
            task.wait(1)
        end
    end
end)
```

**Tool Creation:**

```lua
--[[
    Tool Structure (in StarterPack):
    Tool
    ├── Handle (Part) -- required, this is what the player holds
    └── Script (server script for tool logic)
]]

-- Tool Script
local tool = script.Parent
local DAMAGE = 25
local RANGE = 5
local debounce = false

tool.Activated:Connect(function()
    if debounce then return end
    debounce = true

    local character = tool.Parent  -- character holds the tool
    local humanoidRootPart = character:FindFirstChild("HumanoidRootPart")

    if humanoidRootPart then
        -- Find nearby enemies
        for _, obj in pairs(workspace:GetChildren()) do
            if obj:FindFirstChildOfClass("Humanoid") and obj ~= character then
                local distance = (obj.PrimaryPart.Position - humanoidRootPart.Position).Magnitude
                if distance <= RANGE then
                    obj.Humanoid:TakeDamage(DAMAGE)
                end
            end
        end
    end

    task.wait(0.5)  -- attack cooldown
    debounce = false
end)
```

**Tool Events:**

| Event | Description |
|-------|-------------|
| Equipped | Fires when the player selects the Tool |
| Unequipped | Fires when the player deselects the Tool |
| Activated | Fires when the player clicks/taps while holding the Tool |
| Deactivated | Fires when the player releases the click/tap |

**Assessment:**
- Working kill brick and healing zone with proper debounce
- Custom Tool with Activated event handling

---

### Session 7: Collectibles, Scoring, and Leaderboards

**Cambridge Alignment:** Programming, Managing Data

**Learning Objectives:**
- Create collectible items that disappear on pickup
- Implement a leaderboard using leaderstats
- Track and display player scores in real time

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Brainstorm: what data should a game track about each player? |
| 10-25 min | Introduction | The leaderstats convention in Roblox: folder structure and IntValues |
| 25-45 min | Guided Practice | Create leaderstats on PlayerAdded with Score and Coins |
| 45-65 min | Independent Practice | Build collectible coins that increment the player's score |
| 65-80 min | Guided Practice | Respawning collectibles using task.wait() and Transparency |
| 80-85 min | Extension | Multiple leaderboard stats (Score, Coins, Level) |
| 85-90 min | Closure | Reflection: how does leaderstats connect to the data model? |

**Leaderstats Setup:**

```lua
-- ServerScriptService > Script
local Players = game:GetService("Players")

local function onPlayerAdded(player)
    -- Create leaderstats folder (name must be exactly "leaderstats")
    local leaderstats = Instance.new("Folder")
    leaderstats.Name = "leaderstats"
    leaderstats.Parent = player

    -- Create Score value
    local score = Instance.new("IntValue")
    score.Name = "Score"
    score.Value = 0
    score.Parent = leaderstats

    -- Create Coins value
    local coins = Instance.new("IntValue")
    coins.Name = "Coins"
    coins.Value = 0
    coins.Parent = leaderstats
end

Players.PlayerAdded:Connect(onPlayerAdded)
```

**Collectible Coin Script:**

```lua
-- Script inside a coin Part
local coin = script.Parent
local COIN_VALUE = 10
local RESPAWN_TIME = 5
local debounce = false

coin.Touched:Connect(function(hit)
    if debounce then return end

    local character = hit.Parent
    local player = game:GetService("Players"):GetPlayerFromCharacter(character)

    if player then
        debounce = true

        -- Award points
        local leaderstats = player:FindFirstChild("leaderstats")
        if leaderstats then
            leaderstats.Coins.Value = leaderstats.Coins.Value + COIN_VALUE
            leaderstats.Score.Value = leaderstats.Score.Value + COIN_VALUE
        end

        -- Hide the coin
        coin.Transparency = 1
        coin.CanCollide = false

        -- Respawn after delay
        task.wait(RESPAWN_TIME)
        coin.Transparency = 0
        coin.CanCollide = true
        debounce = false
    end
end)
```

**Leaderstats Hierarchy:**

```
Players
└── Player1
    └── leaderstats (Folder)
        ├── Score (IntValue) = 150
        └── Coins (IntValue) = 15
```

**Value Types for Leaderstats:**

| Value Type | Luau Type | Use Case |
|------------|-----------|----------|
| IntValue | number (integer) | Score, coins, levels |
| NumberValue | number (float) | Time, percentages |
| StringValue | string | Player class, team name |
| BoolValue | boolean | Flags (hasKey, isVIP) |

**Assessment:**
- Working leaderstats with at least two stats displayed on the leaderboard
- Collectible coins that award points and respawn

---

### Session 8: Project 1 - Obstacle Course (Obby) with Scoring

**Cambridge Alignment:** All Strands (Integration)

**Learning Objectives:**
- Apply all concepts from Units 1-2 to build a complete game
- Design and build an obstacle course with multiple stages
- Implement scoring, checkpoints, and a complete player experience

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Planning: sketch your Obby layout on paper, list features |
| 10-20 min | Introduction | Game design document: define stages, obstacles, scoring |
| 20-30 min | Guided Practice | Set up project structure: stages, checkpoints, spawn system |
| 30-70 min | Independent Practice | Build 5+ stages with varied obstacles and challenges |
| 70-80 min | Extension | Add collectible coins, kill bricks, speed pads, and moving platforms |
| 80-85 min | Independent Practice | Playtesting and bug fixes |
| 85-90 min | Closure | Quick showcase: demo your Obby to a partner |

**Project Requirements:**

- [ ] At least 5 obstacle stages with increasing difficulty
- [ ] Checkpoints at each stage (SpawnLocation with AllowTeamChangeOnTouch)
- [ ] Kill bricks that reset player to last checkpoint
- [ ] At least 3 collectible coins that award points
- [ ] Leaderstats displaying Stage and Score
- [ ] Moving or disappearing platforms (at least one dynamic obstacle)
- [ ] Visual variety: different colours, materials, and Part shapes

**Checkpoint System:**

```lua
-- ServerScriptService > CheckpointScript
local Players = game:GetService("Players")

local function onPlayerAdded(player)
    local leaderstats = player:FindFirstChild("leaderstats")
    if not leaderstats then
        leaderstats = Instance.new("Folder")
        leaderstats.Name = "leaderstats"
        leaderstats.Parent = player

        local stage = Instance.new("IntValue")
        stage.Name = "Stage"
        stage.Value = 1
        stage.Parent = leaderstats

        local score = Instance.new("IntValue")
        score.Name = "Score"
        score.Value = 0
        score.Parent = leaderstats
    end
end

Players.PlayerAdded:Connect(onPlayerAdded)
```

```lua
-- Script inside each checkpoint Part
local checkpoint = script.Parent
local STAGE_NUMBER = 2  -- set for each checkpoint

checkpoint.Touched:Connect(function(hit)
    local player = game:GetService("Players"):GetPlayerFromCharacter(hit.Parent)
    if player then
        local stage = player.leaderstats:FindFirstChild("Stage")
        if stage and stage.Value < STAGE_NUMBER then
            stage.Value = STAGE_NUMBER
            player.RespawnLocation = checkpoint  -- checkpoint must be a SpawnLocation
        end
    end
end)
```

**Moving Platform:**

```lua
-- Script inside a moving platform Part
local platform = script.Parent
local TweenService = game:GetService("TweenService")

local startPos = platform.Position
local endPos = startPos + Vector3.new(20, 0, 0)  -- move 20 studs on X axis

local tweenInfo = TweenInfo.new(
    3,                          -- duration
    Enum.EasingStyle.Sine,      -- easing style
    Enum.EasingDirection.InOut,  -- easing direction
    -1,                         -- repeat count (-1 = infinite)
    true                        -- reverses
)

local tween = TweenService:Create(platform, tweenInfo, {Position = endPos})
tween:Play()
```

**Assessment Rubric:**

| Criteria | Emerging (1) | Developing (2) | Proficient (3) | Advanced (4) |
|----------|--------------|----------------|----------------|--------------|
| Stage Design | 1-2 basic stages | 3-4 stages | 5+ varied stages | Creative, well-themed stages |
| Mechanics | Kill bricks only | Checkpoints work | Dynamic obstacles | Moving platforms, collectibles |
| Scoring | No scoring | Basic leaderstats | Score + stage tracking | Multiple stats, respawning coins |
| Code Quality | Disorganized | Some structure | Well-organized | Clean, commented, DRY |

---

## Unit 3: Advanced Scripting & Data Systems
### Sessions 9-12

---

### Session 9: Tables and Arrays

**Cambridge Alignment:** Programming, Managing Data

**Learning Objectives:**
- Create and manipulate tables (arrays and dictionaries)
- Use ipairs and pairs for iteration
- Apply table methods (insert, remove, find, sort)

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Discussion: why would we need to store collections of data? |
| 10-25 min | Introduction | Tables as the universal data structure in Luau: arrays and dictionaries |
| 25-45 min | Guided Practice | Create arrays, add/remove items, iterate with ipairs |
| 45-65 min | Independent Practice | Create dictionaries for player inventories and item databases |
| 65-80 min | Guided Practice | Nested tables: arrays of dictionaries for complex data |
| 80-85 min | Extension | Table methods: table.insert, table.remove, table.find, table.sort |
| 85-90 min | Closure | Challenge: build an inventory system using tables |

**Arrays (Indexed Tables):**

```lua
-- Array: ordered list with numeric indices (starting at 1)
local fruits = {"Apple", "Banana", "Cherry"}

-- Accessing elements
print(fruits[1])  -- "Apple"
print(fruits[3])  -- "Cherry"

-- Adding elements
table.insert(fruits, "Dragonfruit")     -- adds at end
table.insert(fruits, 2, "Blueberry")   -- inserts at position 2

-- Removing elements
table.remove(fruits, 1)  -- removes first element

-- Finding elements
local index = table.find(fruits, "Cherry")
print("Cherry is at index:", index)

-- Length of array
print("Number of fruits:", #fruits)

-- Iterating with ipairs (ordered, numeric keys)
for index, fruit in ipairs(fruits) do
    print(index, fruit)
end
```

**Dictionaries (Key-Value Tables):**

```lua
-- Dictionary: key-value pairs
local playerData = {
    name = "Alex",
    health = 100,
    level = 5,
    inventory = {"Sword", "Shield", "Potion"}
}

-- Accessing values
print(playerData.name)          -- "Alex"
print(playerData["health"])     -- 100

-- Modifying values
playerData.level = 6
playerData.health = playerData.health - 10

-- Adding new keys
playerData.score = 500

-- Iterating with pairs (all keys, unordered)
for key, value in pairs(playerData) do
    print(key, "=", value)
end
```

**Nested Tables:**

```lua
-- Item database
local items = {
    {name = "Health Potion", type = "consumable", value = 50, price = 10},
    {name = "Iron Sword", type = "weapon", value = 25, price = 100},
    {name = "Shield", type = "armour", value = 15, price = 75},
}

-- Accessing nested data
for _, item in ipairs(items) do
    print(item.name .. " costs " .. item.price .. " coins")
end

-- Finding a specific item
local function findItem(itemName)
    for _, item in ipairs(items) do
        if item.name == itemName then
            return item
        end
    end
    return nil  -- not found
end

local sword = findItem("Iron Sword")
if sword then
    print("Found:", sword.name, "Damage:", sword.value)
end
```

**Assessment:**
- Create an inventory system using tables with add/remove functionality
- Implement an item database using nested tables

---

### Session 10: ModuleScripts and Code Organization

**Cambridge Alignment:** Programming, Computational Thinking

**Learning Objectives:**
- Understand the purpose of ModuleScripts for code reuse
- Create and require ModuleScripts from other scripts
- Organize game code into logical modules

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Discussion: what problems arise when all code is in one script? |
| 10-25 min | Introduction | ModuleScripts: shared code, require(), return tables |
| 25-45 min | Guided Practice | Create a GameConfig ModuleScript for shared constants |
| 45-65 min | Independent Practice | Create a PlayerManager module with helper functions |
| 65-80 min | Guided Practice | Organizing code: ReplicatedStorage vs. ServerScriptService for modules |
| 80-85 min | Extension | Module with state: creating an inventory module |
| 85-90 min | Closure | Refactor an existing script to use ModuleScripts |

**ModuleScript Basics:**

```lua
-- ReplicatedStorage > GameConfig (ModuleScript)
local GameConfig = {}

GameConfig.MAX_HEALTH = 100
GameConfig.WALK_SPEED = 16
GameConfig.JUMP_POWER = 50
GameConfig.COIN_VALUE = 10
GameConfig.RESPAWN_TIME = 5

GameConfig.DIFFICULTIES = {
    Easy = {enemySpeed = 10, spawnRate = 5},
    Medium = {enemySpeed = 20, spawnRate = 3},
    Hard = {enemySpeed = 30, spawnRate = 1},
}

return GameConfig
```

```lua
-- Using the ModuleScript in a Server Script
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local GameConfig = require(ReplicatedStorage:WaitForChild("GameConfig"))

print("Max health is:", GameConfig.MAX_HEALTH)
print("Coin value is:", GameConfig.COIN_VALUE)
```

**PlayerManager Module:**

```lua
-- ServerScriptService > PlayerManager (ModuleScript)
local Players = game:GetService("Players")

local PlayerManager = {}

-- Store active player data
PlayerManager.playerData = {}

function PlayerManager.setupPlayer(player)
    -- Create leaderstats
    local leaderstats = Instance.new("Folder")
    leaderstats.Name = "leaderstats"
    leaderstats.Parent = player

    local coins = Instance.new("IntValue")
    coins.Name = "Coins"
    coins.Value = 0
    coins.Parent = leaderstats

    local level = Instance.new("IntValue")
    level.Name = "Level"
    level.Value = 1
    level.Parent = leaderstats

    -- Store reference
    PlayerManager.playerData[player.UserId] = {
        joinTime = os.time(),
        totalCoins = 0,
    }
end

function PlayerManager.addCoins(player, amount)
    local leaderstats = player:FindFirstChild("leaderstats")
    if leaderstats then
        leaderstats.Coins.Value = leaderstats.Coins.Value + amount
        PlayerManager.playerData[player.UserId].totalCoins =
            PlayerManager.playerData[player.UserId].totalCoins + amount
    end
end

function PlayerManager.cleanupPlayer(player)
    PlayerManager.playerData[player.UserId] = nil
end

return PlayerManager
```

```lua
-- ServerScriptService > Main (Script) -- uses the module
local Players = game:GetService("Players")
local ServerScriptService = game:GetService("ServerScriptService")
local PlayerManager = require(ServerScriptService:WaitForChild("PlayerManager"))

Players.PlayerAdded:Connect(function(player)
    PlayerManager.setupPlayer(player)
end)

Players.PlayerRemoving:Connect(function(player)
    PlayerManager.cleanupPlayer(player)
end)
```

**Module Location Guide:**

| Location | Accessible From | Use Case |
|----------|-----------------|----------|
| ReplicatedStorage | Server + Client | Shared config, shared utilities |
| ServerScriptService | Server only | Server-only logic, secure modules |
| StarterPlayerScripts | Client only | Client-only utilities |

**Assessment:**
- Create a GameConfig ModuleScript with at least 5 shared constants
- Create a PlayerManager module with setup, add coins, and cleanup functions

---

### Session 11: RemoteEvents and Client-Server Model

**Cambridge Alignment:** Programming, Networks & Digital Communication

**Learning Objectives:**
- Understand Roblox's client-server architecture
- Use RemoteEvents for client-to-server and server-to-client communication
- Implement DataStoreService for saving player data

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Discussion: why can't the client just change its own score? |
| 10-25 min | Introduction | Client-server model: why it exists, security, trust |
| 25-45 min | Guided Practice | Create RemoteEvents: client fires, server listens and validates |
| 45-60 min | Independent Practice | Implement a shop system: client requests purchase, server validates |
| 60-75 min | Guided Practice | DataStoreService: saving and loading player data |
| 75-85 min | Independent Practice | Save coins and level on player leave; load on join |
| 85-90 min | Closure | Diagram the flow of a RemoteEvent from client to server |

**Client-Server Architecture:**

```
Roblox Client-Server Model:

CLIENT (LocalScript)              SERVER (Script)
+---------------------+           +---------------------+
| - Player input      |           | - Game logic        |
| - GUI updates       |  Remote   | - Data validation   |
| - Visual effects    |  Events   | - DataStores        |
| - Camera control    | ------->  | - Score tracking    |
| - Animations        | <-------  | - Spawning          |
+---------------------+           +---------------------+
```

**RemoteEvent Communication:**

```lua
-- ReplicatedStorage > PurchaseEvent (RemoteEvent) -- create this instance

-- CLIENT: StarterPlayerScripts > ShopClient (LocalScript)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local purchaseEvent = ReplicatedStorage:WaitForChild("PurchaseEvent")

-- When player clicks a buy button
local function onBuyButtonClicked(itemName)
    purchaseEvent:FireServer(itemName)  -- send request to server
end

-- Listen for server responses
purchaseEvent.OnClientEvent:Connect(function(success, message)
    print(message)
end)
```

```lua
-- SERVER: ServerScriptService > ShopServer (Script)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local purchaseEvent = ReplicatedStorage:WaitForChild("PurchaseEvent")

local ITEM_PRICES = {
    SpeedBoost = 50,
    DoubleJump = 100,
    SuperSword = 200,
}

purchaseEvent.OnServerEvent:Connect(function(player, itemName)
    -- ALWAYS validate on the server!
    local price = ITEM_PRICES[itemName]
    if not price then
        purchaseEvent:FireClient(player, false, "Item does not exist!")
        return
    end

    local coins = player.leaderstats.Coins.Value
    if coins >= price then
        player.leaderstats.Coins.Value = coins - price
        -- Grant the item to the player
        print(player.Name .. " purchased " .. itemName)
        purchaseEvent:FireClient(player, true, "Purchased " .. itemName .. "!")
    else
        purchaseEvent:FireClient(player, false, "Not enough coins!")
    end
end)
```

**DataStoreService:**

```lua
-- ServerScriptService > DataStoreScript (Script)
local Players = game:GetService("Players")
local DataStoreService = game:GetService("DataStoreService")
local playerDataStore = DataStoreService:GetDataStore("PlayerData")

local function loadData(player)
    local success, data = pcall(function()
        return playerDataStore:GetAsync("Player_" .. player.UserId)
    end)

    if success and data then
        player.leaderstats.Coins.Value = data.coins or 0
        player.leaderstats.Level.Value = data.level or 1
        print("Loaded data for " .. player.Name)
    else
        print("New player or failed to load: " .. player.Name)
    end
end

local function saveData(player)
    local data = {
        coins = player.leaderstats.Coins.Value,
        level = player.leaderstats.Level.Value,
    }

    local success, err = pcall(function()
        playerDataStore:SetAsync("Player_" .. player.UserId, data)
    end)

    if success then
        print("Saved data for " .. player.Name)
    else
        warn("Failed to save data for " .. player.Name .. ": " .. err)
    end
end

Players.PlayerAdded:Connect(function(player)
    -- Wait for leaderstats to be created first
    player:WaitForChild("leaderstats")
    loadData(player)
end)

Players.PlayerRemoving:Connect(saveData)

-- Save all on server shutdown
game:BindToClose(function()
    for _, player in ipairs(Players:GetPlayers()) do
        saveData(player)
    end
end)
```

**RemoteEvent vs. RemoteFunction:**

| Feature | RemoteEvent | RemoteFunction |
|---------|-------------|----------------|
| Direction | One-way fire | Request-response (returns value) |
| Use case | Notifications, actions | Queries, confirmations |
| Risk | Safer (no yield) | Can hang if client disconnects |
| Recommendation | Preferred | Use with caution |

**Assessment:**
- Working RemoteEvent shop system with server-side validation
- DataStore implementation that saves and loads player data

---

### Session 12: Project 2 - Tycoon Game

**Cambridge Alignment:** All Strands (Integration)

**Learning Objectives:**
- Build a complete tycoon game using all concepts from Units 1-3
- Implement income generation, purchasing, and progression systems
- Apply ModuleScripts, RemoteEvents, and DataStores in a real project

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Planning: sketch your tycoon layout, list buyable items |
| 10-20 min | Introduction | Game design document: income sources, upgrades, progression |
| 20-30 min | Guided Practice | Set up tycoon base plate, dropper, and collector |
| 30-70 min | Independent Practice | Build core tycoon systems: dropper, collector, buttons |
| 70-80 min | Extension | Add upgrades that increase income speed or value |
| 80-85 min | Independent Practice | Playtesting and balancing |
| 85-90 min | Closure | Demo to class, peer feedback |

**Project Requirements:**

- [ ] Tycoon base plate with player ownership
- [ ] Income dropper that generates resources automatically
- [ ] Collector that converts resources into currency
- [ ] At least 4 purchasable items/buildings (buy buttons)
- [ ] Leaderstats for Cash and items owned
- [ ] Data saving with DataStoreService
- [ ] Visual feedback when purchasing (parts appear)
- [ ] Progressive unlocks (item B requires item A first)

**Tycoon Dropper System:**

```lua
-- ServerScriptService > TycoonManager (ModuleScript)
local TycoonManager = {}

function TycoonManager.createDropper(tycoon, dropperPart, collectPart, owner)
    local DROP_INTERVAL = 2
    local DROP_VALUE = 5

    task.spawn(function()
        while tycoon and tycoon.Parent do
            -- Create a resource drop
            local drop = Instance.new("Part")
            drop.Size = Vector3.new(1, 1, 1)
            drop.Position = dropperPart.Position - Vector3.new(0, 2, 0)
            drop.BrickColor = BrickColor.new("Bright yellow")
            drop.Material = Enum.Material.Neon
            drop.Parent = workspace

            -- Clean up after a while
            game:GetService("Debris"):AddItem(drop, 10)

            -- Detect collection
            drop.Touched:Connect(function(hit)
                if hit == collectPart then
                    if owner and owner.leaderstats then
                        owner.leaderstats.Cash.Value += DROP_VALUE
                    end
                    drop:Destroy()
                end
            end)

            task.wait(DROP_INTERVAL)
        end
    end)
end

return TycoonManager
```

**Buy Button System:**

```lua
-- Script inside a buy button Part
local button = script.Parent
local ITEM_NAME = "ConveyorBelt"
local PRICE = 100
local ITEM_TO_SHOW = workspace.TycoonItems:FindFirstChild(ITEM_NAME)

local purchased = false

button.Touched:Connect(function(hit)
    if purchased then return end

    local player = game:GetService("Players"):GetPlayerFromCharacter(hit.Parent)
    if player and player.leaderstats then
        local cash = player.leaderstats.Cash

        if cash.Value >= PRICE then
            cash.Value = cash.Value - PRICE
            purchased = true

            -- Show the purchased item
            if ITEM_TO_SHOW then
                ITEM_TO_SHOW.Transparency = 0
                ITEM_TO_SHOW.CanCollide = true
            end

            -- Remove the buy button
            button:Destroy()
        end
    end
end)
```

**Assessment Rubric:**

| Criteria | Points | Requirements |
|----------|--------|--------------|
| Core Loop | 25 | Dropper, collector, income works |
| Purchases | 25 | At least 4 buyable items with visual feedback |
| Data Persistence | 20 | Saves and loads player progress |
| Polish | 15 | Visual variety, clear pricing, logical layout |
| Code Quality | 15 | ModuleScripts used, organized, commented |

---

## Unit 4: Game World Design & Advanced Mechanics
### Sessions 13-16

---

### Session 13: Terrain Editor and World Building

**Cambridge Alignment:** Computer Systems, Computational Thinking

**Learning Objectives:**
- Use the Terrain Editor to sculpt landscapes
- Generate terrain procedurally with regions and biomes
- Combine terrain with Parts for detailed level design

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Show examples of Roblox games with impressive terrain |
| 10-25 min | Introduction | Terrain Editor overview: Generate, Sculpt, Paint, Region tools |
| 25-45 min | Guided Practice | Generate a terrain with hills, water, and different materials |
| 45-65 min | Independent Practice | Sculpt and paint custom terrain for your game world |
| 65-80 min | Guided Practice | Adding structures (Parts/Models) to complement terrain |
| 80-85 min | Extension | Terrain scripting: manipulating terrain with code |
| 85-90 min | Closure | Gallery walk: view each other's game worlds |

**Terrain Editor Tools:**

| Tool | Purpose | Key Settings |
|------|---------|--------------|
| Generate | Create terrain from noise | Size, seed, biome type |
| Add | Place terrain voxels | Material, brush size, shape |
| Subtract | Remove terrain | Brush size, strength |
| Grow | Expand terrain surface | Brush size, strength |
| Erode | Smooth and wear terrain | Brush size, strength |
| Smooth | Soften rough edges | Brush size, strength |
| Flatten | Level terrain to a plane | Height, brush size |
| Paint | Change terrain material | Material type, brush size |
| Sea Level | Set water level | Height of water plane |
| Region | Select, copy, paste, fill areas | Material, region size |

**Terrain Materials:**

| Material | Visual | Best For |
|----------|--------|----------|
| Grass | Green ground | Plains, meadows |
| Sand | Yellow/tan ground | Beaches, deserts |
| Rock | Grey stone | Mountains, cliffs |
| Snow | White ground | Tundra, mountain tops |
| Water | Blue liquid | Lakes, rivers, oceans |
| Mud | Brown ground | Swamps, paths |
| Ice | Reflective blue-white | Frozen lakes, caves |
| Slate | Dark grey | Underground, caves |
| Ground | Brown earth | Paths, farmland |

**Terrain via Script:**

```lua
-- Fill a region with terrain material
local terrain = workspace.Terrain

-- Define a region (minimum corner, maximum corner)
local region = Region3.new(
    Vector3.new(-50, 0, -50),   -- min corner
    Vector3.new(50, 10, 50)     -- max corner
)

-- Align region to terrain grid (4-stud resolution)
region = region:ExpandToGrid(4)

-- Fill with grass
terrain:FillRegion(region, 4, Enum.Material.Grass)

-- Fill a sphere with water
terrain:FillBall(Vector3.new(0, 5, 0), 20, Enum.Material.Water)
```

**Assessment:**
- Create a game world with sculpted terrain including at least 3 materials
- Add structural elements (buildings or landmarks) to complement the terrain

---

### Session 14: Lighting, Atmosphere, and Visual Effects

**Cambridge Alignment:** Computer Systems, Computational Thinking

**Learning Objectives:**
- Configure Lighting properties for mood and atmosphere
- Use Atmosphere, Sky, and post-processing effects
- Create particle effects with ParticleEmitter

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Show contrasting lighting setups: bright day, spooky night, sunset |
| 10-25 min | Introduction | Lighting service properties, time of day, shadows |
| 25-45 min | Guided Practice | Configure Atmosphere (haze, glare, colour) and Sky (skybox) |
| 45-60 min | Guided Practice | Post-processing: Bloom, ColorCorrection, SunRays, DepthOfField |
| 60-75 min | Independent Practice | Create a custom atmosphere for your game theme |
| 75-85 min | Guided Practice | ParticleEmitter for fire, smoke, sparkle effects |
| 85-90 min | Closure | Before/after comparison: plain vs. atmospheric game world |

**Lighting Properties:**

| Property | Description | Default |
|----------|-------------|---------|
| ClockTime | Time of day (0-24) | 14 (2:00 PM) |
| Brightness | Overall light intensity | 2 |
| Ambient | Shadow fill colour | Color3(0.5, 0.5, 0.5) |
| OutdoorAmbient | Outdoor ambient light | Color3(0.5, 0.5, 0.5) |
| GeographicLatitude | Sun angle | 41.7 |
| EnvironmentDiffuseScale | Environment lighting mix | 1 |
| EnvironmentSpecularScale | Reflective environment mix | 1 |
| Technology | Rendering method | ShadowMap or Future |

**Atmosphere Setup:**

```
Lighting
├── Atmosphere
│   ├── Density: 0.3 (0 = clear, 1 = thick fog)
│   ├── Offset: 0 (fog distance offset)
│   ├── Color: Color3(200, 200, 230) (fog/haze tint)
│   ├── Decay: Color3(100, 100, 120) (distant haze tint)
│   ├── Glare: 0 (sun glare intensity)
│   └── Haze: 0 (horizon haze)
├── Sky
│   └── SkyboxBk/Dn/Ft/Lf/Rt/Up: custom skybox images
├── Bloom
│   ├── Intensity: 0.5
│   ├── Size: 24
│   └── Threshold: 0.8
├── ColorCorrectionEffect
│   ├── Brightness: 0
│   ├── Contrast: 0.1
│   ├── Saturation: 0.2
│   └── TintColor: Color3(255, 245, 240)
└── SunRaysEffect
    ├── Intensity: 0.1
    └── Spread: 0.5
```

**ParticleEmitter Setup:**

```lua
-- Script to create a fire effect on a Part
local firePart = script.Parent

local particles = Instance.new("ParticleEmitter")
particles.Parent = firePart

-- Particle properties
particles.Texture = "rbxassetid://288958475"  -- fire texture
particles.Rate = 50
particles.Lifetime = NumberRange.new(0.5, 1.5)
particles.Speed = NumberRange.new(3, 6)
particles.SpreadAngle = Vector2.new(15, 15)
particles.RotSpeed = NumberRange.new(-100, 100)

-- Size over lifetime (starts medium, shrinks)
particles.Size = NumberSequence.new({
    NumberSequenceKeypoint.new(0, 2),
    NumberSequenceKeypoint.new(0.5, 3),
    NumberSequenceKeypoint.new(1, 0),
})

-- Colour over lifetime (yellow to orange to red)
particles.Color = ColorSequence.new({
    ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 0)),
    ColorSequenceKeypoint.new(0.5, Color3.fromRGB(255, 100, 0)),
    ColorSequenceKeypoint.new(1, Color3.fromRGB(200, 0, 0)),
})

-- Transparency over lifetime
particles.Transparency = NumberSequence.new({
    NumberSequenceKeypoint.new(0, 0),
    NumberSequenceKeypoint.new(0.8, 0.3),
    NumberSequenceKeypoint.new(1, 1),
})

particles.LightEmission = 1  -- glow effect
```

**Lighting Presets:**

| Preset | ClockTime | Brightness | Atmosphere Density | Mood |
|--------|-----------|------------|-------------------|------|
| Bright Day | 14 | 2 | 0.2 | Cheerful, adventure |
| Golden Hour | 17.5 | 1.5 | 0.4 | Warm, cinematic |
| Night | 0 | 0.5 | 0.5 | Spooky, mysterious |
| Overcast | 12 | 1 | 0.6 | Moody, dramatic |
| Underwater | 12 | 0.3 | 0.9 | Blue tint, mysterious |

**Assessment:**
- Configure a complete lighting and atmosphere setup matching your game's theme
- Create at least 2 particle effects (fire, smoke, sparkle, or custom)

---

### Session 15: TweenService and NPC Creation with Pathfinding

**Cambridge Alignment:** Programming, Computational Thinking

**Learning Objectives:**
- Animate objects smoothly using TweenService
- Create NPCs with basic AI using PathfindingService
- Implement interactive NPCs with dialogue

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Discussion: what is the difference between instant teleporting and smooth movement? |
| 10-25 min | Introduction | TweenService: TweenInfo, easing styles, properties you can tween |
| 25-45 min | Guided Practice | Tween a door opening, a platform moving, a light fading |
| 45-60 min | Introduction | PathfindingService: creating paths, following waypoints |
| 60-80 min | Guided Practice | Create an NPC that walks between patrol points using pathfinding |
| 80-85 min | Extension | NPC chases nearest player when they get close |
| 85-90 min | Closure | Reflection: compare TweenService vs. manual position updates |

**TweenService Fundamentals:**

```lua
local TweenService = game:GetService("TweenService")

-- Object to animate
local door = workspace.Door

-- TweenInfo parameters
local tweenInfo = TweenInfo.new(
    1,                              -- duration (seconds)
    Enum.EasingStyle.Quad,          -- easing style
    Enum.EasingDirection.Out,       -- easing direction
    0,                              -- repeat count (0 = no repeat)
    false,                          -- reverses?
    0                               -- delay before starting
)

-- Goal: final property values
local goal = {
    CFrame = door.CFrame * CFrame.new(0, 7, 0)  -- move up 7 studs
}

-- Create and play the tween
local tween = TweenService:Create(door, tweenInfo, goal)
tween:Play()

-- Listen for completion
tween.Completed:Connect(function()
    print("Door is now open!")
end)
```

**Easing Styles:**

| Style | Behaviour |
|-------|-----------|
| Linear | Constant speed |
| Quad | Gentle acceleration |
| Cubic | Medium acceleration |
| Quart | Strong acceleration |
| Sine | Smooth, natural feel |
| Bounce | Bounces at the end |
| Elastic | Springy overshoot |
| Back | Pulls back before moving |

**Tweening Multiple Properties:**

```lua
-- Tween colour, size, and transparency simultaneously
local tweenInfo = TweenInfo.new(2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut)
local goal = {
    Color = Color3.fromRGB(255, 0, 0),
    Size = Vector3.new(8, 8, 8),
    Transparency = 0.5,
}

local tween = TweenService:Create(part, tweenInfo, goal)
tween:Play()
```

**NPC Pathfinding:**

```lua
-- Script inside an NPC Model (must have Humanoid and HumanoidRootPart)
local PathfindingService = game:GetService("PathfindingService")
local npc = script.Parent
local humanoid = npc:WaitForChild("Humanoid")
local rootPart = npc:WaitForChild("HumanoidRootPart")

-- Patrol points (Parts in Workspace)
local patrolPoints = workspace.PatrolPoints:GetChildren()

local function walkTo(destination)
    local path = PathfindingService:CreatePath({
        AgentRadius = 2,
        AgentHeight = 5,
        AgentCanJump = true,
    })

    path:ComputeAsync(rootPart.Position, destination)

    if path.Status == Enum.PathStatus.Success then
        local waypoints = path:GetWaypoints()
        for _, waypoint in ipairs(waypoints) do
            if waypoint.Action == Enum.PathWaypointAction.Jump then
                humanoid.Jump = true
            end
            humanoid:MoveTo(waypoint.Position)
            humanoid.MoveToFinished:Wait()
        end
    else
        warn("Path failed!")
        humanoid:MoveTo(destination)
    end
end

-- Patrol loop
local function patrol()
    while true do
        for _, point in ipairs(patrolPoints) do
            walkTo(point.Position)
            task.wait(2)  -- pause at each point
        end
    end
end

patrol()
```

**NPC Chase Behaviour:**

```lua
local Players = game:GetService("Players")
local DETECTION_RANGE = 30

local function getNearestPlayer()
    local nearest = nil
    local nearestDist = DETECTION_RANGE

    for _, player in ipairs(Players:GetPlayers()) do
        if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
            local dist = (player.Character.HumanoidRootPart.Position - rootPart.Position).Magnitude
            if dist < nearestDist then
                nearest = player
                nearestDist = dist
            end
        end
    end
    return nearest
end

-- Main AI loop
while true do
    local target = getNearestPlayer()
    if target and target.Character then
        walkTo(target.Character.HumanoidRootPart.Position)
    else
        -- No target, patrol instead
        local randomPoint = patrolPoints[math.random(1, #patrolPoints)]
        walkTo(randomPoint.Position)
        task.wait(2)
    end
    task.wait(0.5)
end
```

**Assessment:**
- Create at least 2 tweened objects (door, platform, or visual effect)
- Build an NPC with pathfinding that patrols between 3+ points

---

### Session 16: Project 3 - Adventure/RPG Game

**Cambridge Alignment:** All Strands (Integration)

**Learning Objectives:**
- Build a complete adventure or RPG game with a designed world
- Implement NPCs, combat, and quest/progression systems
- Create a cohesive game experience with atmosphere and polish

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Planning: sketch your game world, define NPCs and objectives |
| 10-20 min | Introduction | Game design document: world layout, quest structure, progression |
| 20-30 min | Guided Practice | Set up world with terrain, lighting, atmosphere |
| 30-70 min | Independent Practice | Build core gameplay: exploration, NPCs, combat or quests |
| 70-80 min | Extension | Add dialogue system, loot drops, or boss encounter |
| 80-85 min | Independent Practice | Playtesting and balance adjustments |
| 85-90 min | Closure | Peer feedback: exchange games and give written feedback |

**Project Requirements:**

- [ ] Game world with sculpted terrain and atmosphere
- [ ] Custom lighting setup that matches the game's mood
- [ ] At least 2 NPCs (one patrol, one interactive/quest-giver)
- [ ] Combat system or challenge-based progression
- [ ] Collectibles or loot with inventory tracking (tables)
- [ ] At least 2 TweenService animations (doors, bridges, platforms)
- [ ] Leaderstats tracking progress (Level, Coins, or Quests)
- [ ] Clear objective or win condition

**Project Structure:**

```
Game Explorer Hierarchy:
Workspace
├── Terrain (sculpted world)
├── Map (Model)
│   ├── Buildings (Model)
│   ├── Landmarks (Model)
│   └── SpawnLocation
├── NPCs (Folder)
│   ├── QuestGiver (Model)
│   └── EnemyPatrol (Model)
├── Collectibles (Folder)
│   └── [Coin instances]
└── InteractiveObjects (Folder)
    ├── Door (Part with TweenService)
    └── Treasure Chest (Model)

ServerScriptService
├── GameManager (ModuleScript)
├── NPCController (Script)
└── DataManager (Script)

ReplicatedStorage
├── GameConfig (ModuleScript)
├── PurchaseEvent (RemoteEvent)
└── QuestEvent (RemoteEvent)

StarterGui
└── GameUI (ScreenGui)
```

**Assessment Rubric:**

| Criteria | Emerging (1) | Developing (2) | Proficient (3) | Advanced (4) |
|----------|--------------|----------------|----------------|--------------|
| World Design | Flat, plain | Some terrain | Rich, atmospheric | Immersive, themed world |
| NPCs | Static | Basic patrol | Pathfinding + interact | AI with chase/dialogue |
| Systems | Basic scoring | Collectibles work | Full progression | Quest system, data saving |
| Code Quality | Single script | Some modules | Well-organized | Clean, modular, commented |

---

## Unit 5: Multiplayer Systems & Game Polish
### Sessions 17-20

---

### Session 17: GUI Design - ScreenGui, TextLabel, TextButton, Frame

**Cambridge Alignment:** Programming, Managing Data

**Learning Objectives:**
- Create responsive GUI elements using ScreenGui
- Implement HUD elements (health bar, score display, inventory)
- Design menu systems with proper navigation and styling

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Analyse GUI design in popular Roblox games: what works and what does not |
| 10-25 min | Introduction | GUI hierarchy: ScreenGui, Frame, TextLabel, TextButton, ImageLabel |
| 25-45 min | Guided Practice | Build a HUD with health bar, score display, and coin counter |
| 45-65 min | Independent Practice | Create a main menu with Play, Settings, and Credits buttons |
| 65-80 min | Guided Practice | Styling: UICorner, UIStroke, UIGradient, UIPadding, UIListLayout |
| 80-85 min | Extension | Animate GUI elements with TweenService (slide in, fade, scale) |
| 85-90 min | Closure | Accessibility check: is your GUI readable at different screen sizes? |

**GUI Hierarchy:**

```
StarterGui
└── GameHUD (ScreenGui)
    ├── TopBar (Frame)
    │   ├── UIListLayout (horizontal)
    │   ├── HealthFrame (Frame)
    │   │   ├── HealthBar (Frame, inner fill)
    │   │   └── HealthLabel (TextLabel, "100/100")
    │   ├── CoinDisplay (Frame)
    │   │   ├── CoinIcon (ImageLabel)
    │   │   └── CoinLabel (TextLabel, "0")
    │   └── ScoreLabel (TextLabel, "Score: 0")
    └── MainMenu (Frame)
        ├── Title (TextLabel, "MY GAME")
        ├── PlayButton (TextButton)
        ├── SettingsButton (TextButton)
        └── CreditsButton (TextButton)
```

**GUI Sizing and Positioning:**

| Property | Type | Description |
|----------|------|-------------|
| Size | UDim2 | `UDim2.new(scaleX, offsetX, scaleY, offsetY)` |
| Position | UDim2 | Position relative to parent |
| AnchorPoint | Vector2 | Pivot point (0,0 = top-left; 0.5,0.5 = centre) |

```lua
-- Common sizing patterns
UDim2.new(0, 200, 0, 50)     -- 200px wide, 50px tall (fixed)
UDim2.new(0.5, 0, 0.1, 0)    -- 50% of parent width, 10% of parent height (responsive)
UDim2.new(1, -20, 0, 40)     -- full width minus 20px padding, 40px tall
```

**HUD Script (LocalScript in StarterGui):**

```lua
-- StarterGui > GameHUD > HUDScript (LocalScript)
local player = game:GetService("Players").LocalPlayer
local leaderstats = player:WaitForChild("leaderstats")
local coins = leaderstats:WaitForChild("Coins")
local score = leaderstats:WaitForChild("Score")

-- GUI references
local gui = script.Parent
local coinLabel = gui.TopBar.CoinDisplay.CoinLabel
local scoreLabel = gui.TopBar.ScoreLabel
local healthBar = gui.TopBar.HealthFrame.HealthBar
local healthLabel = gui.TopBar.HealthFrame.HealthLabel

-- Update coin display when value changes
coins.Changed:Connect(function(newValue)
    coinLabel.Text = tostring(newValue)
end)

-- Update score display
score.Changed:Connect(function(newValue)
    scoreLabel.Text = "Score: " .. tostring(newValue)
end)

-- Update health bar
local function updateHealth()
    local character = player.Character
    if character then
        local humanoid = character:FindFirstChildOfClass("Humanoid")
        if humanoid then
            local healthPercent = humanoid.Health / humanoid.MaxHealth
            healthBar.Size = UDim2.new(healthPercent, 0, 1, 0)
            healthLabel.Text = math.floor(humanoid.Health) .. "/" .. humanoid.MaxHealth

            -- Colour based on health
            if healthPercent > 0.5 then
                healthBar.BackgroundColor3 = Color3.fromRGB(0, 200, 0)
            elseif healthPercent > 0.25 then
                healthBar.BackgroundColor3 = Color3.fromRGB(255, 200, 0)
            else
                healthBar.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
            end
        end
    end
end

-- Connect to health changes on character spawn
player.CharacterAdded:Connect(function(character)
    local humanoid = character:WaitForChild("Humanoid")
    humanoid.HealthChanged:Connect(updateHealth)
    updateHealth()
end)
```

**GUI Styling Components:**

| Component | Purpose | Example |
|-----------|---------|---------|
| UICorner | Rounded corners | CornerRadius = UDim.new(0, 8) |
| UIStroke | Border outline | Thickness = 2, Color = white |
| UIGradient | Gradient fill | Two-colour blend |
| UIPadding | Inner spacing | PaddingLeft = UDim.new(0, 10) |
| UIListLayout | Auto-layout children | Horizontal or vertical |
| UIAspectRatioConstraint | Maintain aspect ratio | DominantAxis, AspectRatio |

**Button Click Handler:**

```lua
local playButton = gui.MainMenu.PlayButton
local mainMenu = gui.MainMenu

playButton.MouseButton1Click:Connect(function()
    -- Animate menu sliding out
    local tween = game:GetService("TweenService"):Create(
        mainMenu,
        TweenInfo.new(0.5, Enum.EasingStyle.Quad, Enum.EasingDirection.In),
        {Position = UDim2.new(0, 0, -1, 0)}  -- slide up off screen
    )
    tween:Play()
    tween.Completed:Connect(function()
        mainMenu.Visible = false
    end)
end)
```

**Assessment:**
- Complete HUD with health bar, score, and coin counter
- Working main menu with at least 3 styled buttons

---

### Session 18: SoundService and Audio Implementation

**Cambridge Alignment:** Programming, Computer Systems

**Learning Objectives:**
- Import and play sound effects and background music
- Use SoundService and SoundGroups for volume management
- Add audio feedback to game events

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Play a game clip with and without sound: discuss the impact of audio |
| 10-25 min | Introduction | Sound objects, SoundService, SoundGroups, audio properties |
| 25-45 min | Guided Practice | Add background music and basic SFX (coin pickup, jump, damage) |
| 45-65 min | Independent Practice | Add sound effects to all major game interactions |
| 65-80 min | Guided Practice | SoundGroups for volume categories, settings menu integration |
| 80-85 min | Extension | Positional audio: 3D sounds that fade with distance |
| 85-90 min | Closure | Audio checklist: does every action in your game have audio feedback? |

**Sound Properties:**

| Property | Description | Example |
|----------|-------------|---------|
| SoundId | Asset ID for the audio file | "rbxassetid://123456789" |
| Volume | Loudness (0 to 10) | 0.5 |
| PlaybackSpeed | Speed/pitch (1 = normal) | 1.2 |
| Looped | Whether the sound repeats | true (for music) |
| Playing | Whether the sound is currently playing | true / false |
| RollOffMode | How 3D sound fades | Enum.RollOffMode.Linear |
| RollOffMaxDistance | Maximum hearing distance | 100 |

**Background Music Setup:**

```lua
-- Script in ServerScriptService or a LocalScript in StarterPlayerScripts
local SoundService = game:GetService("SoundService")

-- Create background music
local bgMusic = Instance.new("Sound")
bgMusic.Name = "BackgroundMusic"
bgMusic.SoundId = "rbxassetid://1234567890"  -- replace with your audio ID
bgMusic.Volume = 0.3
bgMusic.Looped = true
bgMusic.Parent = SoundService

bgMusic:Play()
```

**SFX Manager Module:**

```lua
-- ReplicatedStorage > SFXManager (ModuleScript)
local SoundService = game:GetService("SoundService")

local SFXManager = {}

-- Sound IDs (replace with actual asset IDs)
SFXManager.sounds = {
    coinPickup = "rbxassetid://1111111111",
    jump = "rbxassetid://2222222222",
    damage = "rbxassetid://3333333333",
    buttonClick = "rbxassetid://4444444444",
    levelUp = "rbxassetid://5555555555",
    death = "rbxassetid://6666666666",
}

function SFXManager.play(soundName, parent)
    local soundId = SFXManager.sounds[soundName]
    if not soundId then
        warn("Unknown sound: " .. soundName)
        return
    end

    local sound = Instance.new("Sound")
    sound.SoundId = soundId
    sound.Volume = 0.5
    sound.Parent = parent or SoundService

    sound:Play()

    -- Auto-cleanup after playing
    sound.Ended:Connect(function()
        sound:Destroy()
    end)

    return sound
end

function SFXManager.playAtPosition(soundName, position)
    -- Create a Part to anchor the sound in 3D space
    local soundPart = Instance.new("Part")
    soundPart.Anchored = true
    soundPart.CanCollide = false
    soundPart.Transparency = 1
    soundPart.Size = Vector3.new(1, 1, 1)
    soundPart.Position = position
    soundPart.Parent = workspace

    local sound = SFXManager.play(soundName, soundPart)
    if sound then
        sound.RollOffMaxDistance = 50
        sound.Ended:Connect(function()
            soundPart:Destroy()
        end)
    end
end

return SFXManager
```

**SoundGroup Setup:**

```
SoundService
├── MusicGroup (SoundGroup)
│   ├── Volume: 0.5
│   └── BackgroundMusic (Sound)
├── SFXGroup (SoundGroup)
│   ├── Volume: 0.8
│   └── [dynamically created sounds]
└── UIGroup (SoundGroup)
    ├── Volume: 0.6
    └── [button click sounds]
```

```lua
-- Volume control in settings menu
local function setMusicVolume(value)  -- value is 0 to 1
    SoundService.MusicGroup.Volume = value
end

local function setSFXVolume(value)
    SoundService.SFXGroup.Volume = value
end
```

**Assessment:**
- Background music that loops continuously
- Sound effects for at least 4 game events (pickup, damage, jump, button click)
- Volume control for music and SFX separately

---

### Session 19: Teams and Multiplayer Mechanics

**Cambridge Alignment:** Programming, Networks & Digital Communication

**Learning Objectives:**
- Configure Teams service for team-based gameplay
- Implement team-specific spawning and scoring
- Create multiplayer game mechanics (tag, capture, race)

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Brainstorm: what multiplayer modes exist in games you play? |
| 10-25 min | Introduction | Teams service, TeamColor, SpawnLocations with team settings |
| 25-45 min | Guided Practice | Set up 2 teams with colour-coded spawns and team leaderboards |
| 45-65 min | Independent Practice | Implement a team-based game mechanic (capture the flag or king of the hill) |
| 65-80 min | Guided Practice | Round system: timers, win conditions, resetting |
| 80-85 min | Extension | Auto-balance teams when players join or leave |
| 85-90 min | Closure | Playtest with classmates; observe multiplayer interactions |

**Teams Setup:**

```
Teams (Service)
├── Red Team (Team)
│   ├── TeamColor: "Bright red"
│   └── AutoAssignable: true
└── Blue Team (Team)
    ├── TeamColor: "Bright blue"
    └── AutoAssignable: true
```

**Team Assignment Script:**

```lua
-- ServerScriptService > TeamManager (Script)
local Players = game:GetService("Players")
local Teams = game:GetService("Teams")

local redTeam = Teams["Red Team"]
local blueTeam = Teams["Blue Team"]

local function getSmallestTeam()
    local redCount = #redTeam:GetPlayers()
    local blueCount = #blueTeam:GetPlayers()

    if redCount <= blueCount then
        return redTeam
    else
        return blueTeam
    end
end

Players.PlayerAdded:Connect(function(player)
    -- Assign to smallest team for balance
    player.Team = getSmallestTeam()
    print(player.Name .. " assigned to " .. player.Team.Name)
end)
```

**Team-Based Scoring:**

```lua
-- Team score tracking
local teamScores = {
    ["Red Team"] = 0,
    ["Blue Team"] = 0,
}

local function addTeamScore(teamName, points)
    teamScores[teamName] = teamScores[teamName] + points

    -- Check win condition
    if teamScores[teamName] >= 100 then
        announceWinner(teamName)
    end
end

-- When a player scores a point for their team
local function onPlayerScored(player, points)
    if player.Team then
        addTeamScore(player.Team.Name, points)
    end
end
```

**Round System:**

```lua
-- ServerScriptService > RoundManager (Script)
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

local ROUND_TIME = 120  -- seconds
local INTERMISSION_TIME = 15

local roundEvent = ReplicatedStorage:WaitForChild("RoundEvent")

local function startRound()
    -- Notify clients
    roundEvent:FireAllClients("RoundStart", ROUND_TIME)

    -- Countdown
    for timeLeft = ROUND_TIME, 0, -1 do
        roundEvent:FireAllClients("TimeUpdate", timeLeft)
        task.wait(1)
    end

    -- Round over
    local winner = getWinningTeam()
    roundEvent:FireAllClients("RoundEnd", winner)

    -- Intermission
    task.wait(INTERMISSION_TIME)

    -- Reset scores and start again
    resetScores()
    startRound()
end

task.spawn(startRound)
```

**SpawnLocation Team Settings:**

| Property | Purpose |
|----------|---------|
| TeamColor | Which team spawns here |
| AllowTeamChangeOnTouch | Changes player's team when touched |
| Neutral | Any team can spawn here |
| Duration | How long spawn animation lasts |

**Assessment:**
- Working team system with balanced assignment
- Team-based scoring and win condition
- At least one round of multiplayer gameplay tested

---

### Session 20: Game Balancing and Playtesting

**Cambridge Alignment:** Computational Thinking, Managing Data

**Learning Objectives:**
- Apply systematic playtesting methodology
- Gather and analyse player feedback
- Balance game difficulty, economy, and pacing

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Discussion: what makes a game too easy, too hard, or just right? |
| 10-25 min | Introduction | Balancing principles: economy curves, difficulty ramps, player psychology |
| 25-40 min | Guided Practice | Create a spreadsheet/table for game economy: costs, rewards, progression |
| 40-55 min | Independent Practice | Adjust your game based on balancing calculations |
| 55-75 min | Guided Practice | Structured playtesting: each student tests 2 classmates' games |
| 75-85 min | Independent Practice | Integrate feedback: fix top 3 issues from playtesting |
| 85-90 min | Closure | Reflection: what changed after balancing and testing? |

**Balancing Checklist:**

```
ECONOMY BALANCE:
[ ] Income rate feels rewarding but not too fast
[ ] Prices create meaningful choices
[ ] Progression curve keeps players engaged
[ ] No way to get stuck with zero resources

DIFFICULTY BALANCE:
[ ] First minute is easy and teaches mechanics
[ ] Difficulty increases gradually
[ ] Hard challenges have clear solutions
[ ] Failure is frustrating but fair

PACING:
[ ] Action and calm moments alternate
[ ] New mechanics are introduced regularly
[ ] Game length matches content depth
[ ] No long periods of nothing happening
```

**Economy Balancing Table:**

| Item | Cost | Income Boost | Time to Earn | Order |
|------|------|-------------|--------------|-------|
| Basic Dropper | Free | 5/sec | 0 sec | 1st |
| Upgraded Dropper | 100 | 10/sec | 20 sec | 2nd |
| Conveyor Belt | 250 | 0 (QoL) | 25 sec | 3rd |
| Super Dropper | 1000 | 25/sec | 40 sec | 4th |
| Golden Dropper | 5000 | 75/sec | 67 sec | 5th |

**Playtesting Feedback Form:**

| Question | Rating (1-5) | Notes |
|----------|-------------|-------|
| Was the game fun? | | |
| Were the controls intuitive? | | |
| Was the difficulty fair? | | |
| Did you encounter any bugs? | | |
| Was the goal clear? | | |
| Would you play again? | | |
| What was the best part? | | |
| What should be changed? | | |

**Common Balancing Mistakes:**

| Mistake | Problem | Solution |
|---------|---------|----------|
| Prices too cheap | Players buy everything instantly | Increase prices, reduce income |
| Prices too expensive | Players quit from boredom | Reduce prices, add interim rewards |
| Flat difficulty | Game feels monotonous | Progressive challenge curve |
| Difficulty spikes | Players hit a wall | Smooth the difficulty ramp |
| No feedback | Players don't know what happened | Add visual and audio feedback |

**Assessment:**
- Complete economy balancing document for your game
- Playtest 2 classmates' games and provide written feedback
- Implement at least 3 changes based on feedback received

---

## Unit 6: Capstone Project & Publishing
### Sessions 21-24

---

### Session 21: Capstone Project - Game Design Document and Planning

**Cambridge Alignment:** All Strands, Project Management

**Learning Objectives:**
- Design a complete game from concept using a Game Design Document
- Create a project plan with milestones and task breakdown
- Set up project architecture and folder structure

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Brainstorm game concepts: genre, theme, core mechanic |
| 10-25 min | Introduction | What makes a good GDD? Scope management and feature prioritisation |
| 25-45 min | Guided Practice | Complete the Game Design Document template |
| 45-65 min | Independent Practice | Set up project in Roblox Studio: folder structure, base world, modules |
| 65-80 min | Guided Practice | Break features into tasks, estimate time, set milestones |
| 80-85 min | Extension | Peer review of GDDs: feasibility check |
| 85-90 min | Closure | Planning: commit to milestones for Sessions 22, 23, and 24 |

**Game Design Document Template:**

```
GAME TITLE: _______________

CONCEPT:
- Genre: _______________
- Core mechanic: _______________
- Target experience: _______________
- Theme/Setting: _______________

FEATURES (Priority Order):
Must Have:
1. _______________
2. _______________
3. _______________
4. _______________

Nice to Have:
1. _______________
2. _______________

TECHNICAL SCOPE:
- World type: _______________
- NPC types: _______________
- Collectibles/items: _______________
- GUI screens: _______________
- Data to save: _______________

VISUAL STYLE:
- Terrain style: _______________
- Lighting mood: _______________
- Colour palette: _______________

AUDIO:
- Music style: _______________
- Key sound effects: _______________

MULTIPLAYER:
- Single player / Multiplayer / Both: _______________
- Team-based? _______________
- Competitive or cooperative? _______________
```

**Project Milestones:**

| Session | Milestone | Deliverable |
|---------|-----------|-------------|
| 21 | Planning | Completed GDD, project setup, folder structure |
| 22 | Core Loop | Playable prototype with core mechanic working |
| 23 | Polish | Complete, tested game with audio and GUI |
| 24 | Publish | Published to Roblox, portfolio presentation |

**Recommended Project Structure:**

```
Game Explorer:
Workspace
├── Terrain
├── Map (Model)
├── NPCs (Folder)
├── Collectibles (Folder)
└── InteractiveObjects (Folder)

ServerScriptService
├── Main (Script)
├── PlayerManager (ModuleScript)
├── GameManager (ModuleScript)
└── DataManager (ModuleScript)

ReplicatedStorage
├── GameConfig (ModuleScript)
├── RemoteEvents (Folder)
│   ├── PurchaseEvent (RemoteEvent)
│   └── GameEvent (RemoteEvent)
└── Assets (Folder)

StarterGui
└── GameUI (ScreenGui)

StarterPack
└── [Tools]

StarterPlayerScripts
└── ClientController (LocalScript)
```

**Assessment:**
- Complete Game Design Document with all sections filled
- Project setup in Roblox Studio with proper folder structure

---

### Session 22: Capstone Project - Core Development

**Cambridge Alignment:** All Strands (Integration)

**Learning Objectives:**
- Implement core gameplay mechanics from the GDD
- Create a playable prototype
- Apply rapid iteration and scope management

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-5 min | Warm-up | Check-in: review GDD, clarify scope, identify blockers |
| 5-10 min | Introduction | Development priorities: what makes it playable? |
| 10-75 min | Independent Practice | Build core game loop: player, world, main mechanic |
| 75-80 min | Guided Practice | One-on-one troubleshooting rotations with instructor |
| 80-85 min | Independent Practice | Quick iteration: test, fix, improve |
| 85-90 min | Closure | Progress report: demonstrate current state to a partner |

**Development Priorities:**

1. **Player controller** - Movement and basic interactions work
2. **Core mechanic** - The main game activity is functional
3. **Win/lose condition** - The game has a clear goal
4. **Basic challenge** - Something for the player to overcome
5. **Minimum GUI** - Player can understand game state

**Troubleshooting Guide:**

| Common Issue | Solution |
|--------------|----------|
| Scope creep | Return to GDD, cut Nice to Have features |
| Bug blocking progress | Simplify the feature, isolate the problem, use print() |
| World looks empty | Use Toolbox models temporarily, focus on gameplay |
| Script not running | Check script type (Script vs. LocalScript) and location |
| RemoteEvent not firing | Verify it exists in ReplicatedStorage, check client vs. server |
| DataStore not saving | Enable Studio API access in Game Settings |

**Assessment:**
- Playable prototype demonstrating core mechanic
- Progress against GDD milestone targets

---

### Session 23: Capstone Project - Polish and Testing

**Cambridge Alignment:** All Strands, Testing

**Learning Objectives:**
- Add polish to improve game feel and presentation
- Conduct systematic testing and gather feedback
- Iterate on the game based on peer testing results

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-5 min | Warm-up | Status check: what is working, what needs finishing |
| 5-30 min | Independent Practice | Polish: add audio, particles, GUI improvements |
| 30-40 min | Guided Practice | Testing methodology: what to test and how to report bugs |
| 40-60 min | Independent Practice | Peer testing: play each other's games, fill feedback forms |
| 60-75 min | Independent Practice | Feedback integration: fix top 3 issues from testing |
| 75-85 min | Independent Practice | Final bug fixes and preparation for publishing |
| 85-90 min | Closure | Readiness check: is the game ready to publish? |

**Testing Checklist:**

```
FUNCTIONALITY:
[ ] All controls work as expected
[ ] No crashes, freezes, or infinite loops
[ ] Win/lose conditions trigger correctly
[ ] Score and stats update properly
[ ] All GUI elements are functional
[ ] Data saving works (if implemented)

MULTIPLAYER (if applicable):
[ ] Works with 2+ players simultaneously
[ ] No desync or replication issues
[ ] Team assignment is balanced

BALANCE:
[ ] Difficulty feels fair and progressive
[ ] Economy is balanced (not too fast, not too slow)
[ ] No impossible or trivially easy challenges

POLISH:
[ ] All actions have audio feedback
[ ] Visual effects enhance gameplay
[ ] GUI is clear and readable
[ ] No placeholder assets remain
[ ] Lighting and atmosphere are configured

EDGE CASES:
[ ] What if player does nothing?
[ ] What if player spams input?
[ ] What if player goes out of bounds?
[ ] What if player disconnects and reconnects?
```

**Peer Testing Feedback Form:**

1. What was the most fun part of the game?
2. What was confusing or unclear?
3. Did you encounter any bugs? Describe them.
4. What would you add or change?
5. Rate overall experience (1 to 5)
6. Was the game too easy, too hard, or just right?

**Assessment:**
- All items on the testing checklist addressed
- Playtest 2 classmates' games and provide written feedback
- Implement at least 3 changes based on feedback

---

### Session 24: Publishing to Roblox and Portfolio Showcase

**Cambridge Alignment:** Networks & Digital Communication, Presentation

**Learning Objectives:**
- Publish a game to the Roblox platform
- Create a game description, icon, and thumbnail
- Present and showcase a portfolio of all course projects

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Warm-up | Publishing checklist: review what is needed to go live |
| 10-25 min | Guided Practice | Configure Game Settings: title, description, icon, permissions |
| 25-35 min | Independent Practice | Publish to Roblox: File > Publish to Roblox, set access |
| 35-45 min | Guided Practice | Game page: write compelling description, upload thumbnail |
| 45-70 min | Presentations | 3-4 minute game showcases: each student presents their capstone |
| 70-80 min | Celebration | Play each other's published games on Roblox |
| 80-85 min | Reflection | Course wrap-up: final reflection questions |
| 85-90 min | Closure | Certificates, next steps, advanced course pathways |

**Publishing Checklist:**

- [ ] Game title is clear and appropriate
- [ ] Game description explains genre, objective, and controls
- [ ] Game icon (512x512 image, represents the game)
- [ ] Thumbnail/screenshots (1920x1080, showcasing gameplay)
- [ ] Access permissions set (Public or Friends)
- [ ] Game Settings configured (max players, genre, devices)
- [ ] All content follows Roblox Community Standards
- [ ] Credits included (assets, music, tools used)
- [ ] Play-tested on target devices (PC, mobile if applicable)

**Game Page Description Template:**

```
[GAME TITLE]

[One-sentence pitch: what is this game about?]

HOW TO PLAY:
- [Control 1]
- [Control 2]
- [Objective]

FEATURES:
- [Feature 1]
- [Feature 2]
- [Feature 3]

Created by [Student Name] as part of the Roblox Studio Intermediate Course.

CREDITS:
- Music: [source]
- Sound effects: [source]
- Models: [source if applicable]
```

**Publishing Steps:**

```
1. File > Publish to Roblox (or File > Publish to Roblox As... for new)
2. Enter game name and description
3. Set genre and devices
4. Game Settings > Permissions: set to Public
5. Game Settings > Basic Info: upload icon and thumbnails
6. Game Settings > Monetization: configure or leave default
7. Click "Create" or "Update"
8. Access your game page at roblox.com/games/[gameId]
```

**Portfolio Components:**

1. **Project 1:** Obstacle Course (Obby) with Scoring
2. **Project 2:** Tycoon Game
3. **Project 3:** Adventure/RPG Game
4. **Capstone Project:** Original game

**Final Reflection Questions:**

1. What was your biggest technical challenge and how did you overcome it?
2. Which programming concept was most valuable to learn?
3. How has your approach to problem-solving improved since Session 1?
4. What type of game would you like to create next?
5. How might you use the skills from this course outside of game development?

---

## Assessment Framework

### Summative Assessments

| Assessment | Weight | Session | Description |
|------------|--------|---------|-------------|
| Project 1: Obstacle Course (Obby) | 15% | 8 | First complete game with stages, scoring, and checkpoints |
| Project 2: Tycoon Game | 20% | 12 | Game with ModuleScripts, DataStores, and economy |
| Project 3: Adventure/RPG | 25% | 16 | Complex game with terrain, NPCs, and progression |
| Capstone Project | 30% | 21-24 | Original game from concept to published Roblox experience |
| Learning Journal | 10% | Ongoing | Reflection, pseudocode, planning documentation |

### Formative Assessments

- Weekly code review and script analysis
- Exit tickets after each session
- Debugging challenges with provided broken scripts
- Peer testing sessions with written feedback
- Algorithm design exercises (pseudocode and flowcharts)
- Explorer hierarchy diagrams

### Grading Scale

| Grade | Percentage | Description |
|-------|------------|-------------|
| A* | 90-100% | Exceptional work, exceeds all requirements |
| A | 80-89% | Excellent, meets all requirements with quality |
| B | 70-79% | Good, meets most requirements |
| C | 60-69% | Satisfactory, meets minimum requirements |
| D | 50-59% | Developing, partially meets requirements |
| U | Below 50% | Ungraded, does not meet minimum |

### Project Assessment Rubric

| Criteria | 1 (Emerging) | 2 (Developing) | 3 (Proficient) | 4 (Advanced) |
|----------|--------------|----------------|----------------|--------------|
| **Code Quality** | Disorganized, many errors | Some structure, some errors | Well-organized, runs correctly | Clean, efficient, well-commented, uses ModuleScripts |
| **Gameplay** | Barely functional | Works but unpolished | Smooth and enjoyable | Excellent game feel, polished |
| **Creativity** | Template only | Minor modifications | Unique elements | Innovative design and mechanics |
| **Technical Depth** | Basic features only | Standard implementation | Advanced features used | Exceeds expectations, client-server mastery |
| **Completion** | Incomplete | Missing elements | All requirements met | Extra features and polish added |

---

## Resources and Materials

### Required Software
- Roblox Studio ([create.roblox.com](https://create.roblox.com/))
- Roblox account for each student (free)
- Web browser for documentation and asset library

### Recommended Learning Resources

**Official Documentation:**
- [Roblox Creator Hub](https://create.roblox.com/docs)
- [Luau Language Reference](https://luau-lang.org/)
- [Roblox API Reference](https://create.roblox.com/docs/reference/engine)

**Tutorials:**
- [Roblox Education](https://education.roblox.com/) - Official lesson plans and tutorials
- [Roblox Creator Hub Tutorials](https://create.roblox.com/docs/tutorials) - Step-by-step official guides
- [TheDevKing YouTube Channel](https://www.youtube.com/@TheDevKing) - Beginner-friendly Roblox scripting
- [AlvinBlox YouTube Channel](https://www.youtube.com/@AlvinBlox) - Comprehensive scripting tutorials

**Asset Sources:**
- [Roblox Toolbox](https://create.roblox.com/marketplace) - Free models, meshes, audio, and plugins
- [Roblox Creator Store](https://create.roblox.com/marketplace) - Community assets and plugins
- [Freesound.org](https://freesound.org/) - Free audio effects
- [Pixabay](https://pixabay.com/) - Royalty-free images for GUI

**Cambridge Resources:**
- [Cambridge IGCSE Computer Science (0478)](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-igcse-computer-science-0478/)
- [Cambridge Lower Secondary Computing (0860)](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-lower-secondary/curriculum/computing/)

---

## Differentiation Strategies

### Support for Struggling Learners
- Provide starter places with partial scripts and pre-built structures
- Pair programming opportunities with stronger peers
- Step-by-step visual guides with annotated screenshots
- Extended time for projects across catch-up sessions
- Simplified project requirements (fewer stages, simpler features)
- One-on-one debugging sessions during independent practice time
- Pre-written code snippets to copy and modify (scaffolded learning)

### Extension for Advanced Learners
- Advanced Luau: metatables, coroutines, and OOP patterns
- Custom plugin development for Roblox Studio
- Monetisation concepts: game passes and developer products
- Advanced pathfinding and AI behaviour trees
- Mentor role: assist struggling peers during independent practice
- Marketplace asset creation: build and share models or plugins
- Explore Roblox game analytics and player retention strategies

### Accessibility Considerations
- High contrast Studio themes for visual accessibility
- Keyboard-only navigation alternatives for all game mechanics
- Clear code commenting and consistent naming conventions
- Audio descriptions and visual alternatives for all feedback
- Flexible assessment formats (oral presentation, recorded demo, written report)
- Font size and colour contrast in all GUI elements
- Mobile-friendly GUI design for tablet accessibility

---

## Teacher Notes

### Preparation Before Course

1. Install Roblox Studio on all classroom computers (requires Roblox account login)
2. Create a class group or team for sharing places and collaboration
3. Prepare starter places (templates) for each unit project
4. Curate approved Toolbox assets (models, sounds) for student use
5. Review Cambridge assessment objectives and map to session content
6. Test all project requirements on classroom hardware
7. Enable Studio API access for DataStoreService testing
8. Set up a submission system (shared folder, learning management system, or Roblox group)

### Session Structure Recommendations

- **First 10-15 minutes:** Warm-up activity, review previous session, introduce new concept
- **Middle 50-60 minutes:** Guided practice followed by independent practice (hands-on coding)
- **Final 10-15 minutes:** Extension activity, reflection, exit ticket, preview of next session
- The 90-minute format allows deeper exploration and more independent practice time than shorter sessions

### Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| Luau syntax errors | Use Script Analysis (View > Script Analysis) for real-time error checking |
| Script in wrong location | Verify Script vs. LocalScript; check parent service |
| Instance paths not working | Use WaitForChild() for objects that load asynchronously |
| Touched event firing too many times | Implement debounce pattern with a boolean flag |
| RemoteEvent not working | Confirm event exists in ReplicatedStorage; check client vs. server |
| DataStore not saving in Studio | Enable Studio API Access in Game Settings > Security |
| Performance lag | Reduce Part count, use streaming, limit particle emitters |
| Student account restrictions | Ensure parental permissions are set for Studio access |

### Classroom Management Tips

- Establish a debugging protocol: try three things before asking for help (read error, check spelling, use print())
- Create a peer helper system: assign experienced students as table mentors
- Regular save reminders: Ctrl+S every 10 minutes, publish periodically
- Celebrate small wins: showcase interesting solutions to the class
- Build in catch-up time during project sessions for students who fall behind
- Use Roblox's Team Create for collaborative projects (advanced groups)
- Monitor student Roblox accounts for appropriate use during class time
- Maintain a "common bugs" board visible in the classroom

---

## Appendices

### Appendix A: Luau Quick Reference

```lua
-- Variables
local myVar = 10
local typedVar: number = 10
local MY_CONST = 100  -- convention: UPPER_CASE for constants

-- Functions
local function myFunction(param: number): string
    return "Result: " .. tostring(param)
end

-- Conditionals
if condition then
    -- code
elseif otherCondition then
    -- code
else
    -- code
end

-- Numeric for loop
for i = 1, 10 do
    print(i)
end

-- Generic for loop (array)
for index, value in ipairs(myArray) do
    print(index, value)
end

-- Generic for loop (dictionary)
for key, value in pairs(myDict) do
    print(key, value)
end

-- While loop
while condition do
    -- code
end

-- Repeat-until loop
repeat
    -- code
until condition

-- Tables (arrays)
local fruits = {"Apple", "Banana", "Cherry"}
table.insert(fruits, "Date")
table.remove(fruits, 1)

-- Tables (dictionaries)
local player = {name = "Alex", health = 100}
player.score = 0

-- String operations
local str = "Hello, " .. "World!"
local len = string.len(str)   -- or #str
local upper = string.upper(str)
local sub = string.sub(str, 1, 5)

-- Math operations
local rounded = math.floor(3.7)   -- 3
local random = math.random(1, 10)
local clamped = math.clamp(value, 0, 100)

-- Common callbacks
game:GetService("Players").PlayerAdded:Connect(function(player) end)
part.Touched:Connect(function(hit) end)
button.MouseButton1Click:Connect(function() end)
```

### Appendix B: Common Roblox Services Reference

| Service | Purpose | Key Methods/Properties |
|---------|---------|----------------------|
| Players | Manage connected players | PlayerAdded, GetPlayers(), LocalPlayer |
| Workspace | Contains all visible game objects | FindFirstChild(), GetChildren() |
| ReplicatedStorage | Shared assets (client + server) | WaitForChild() |
| ServerScriptService | Server-only scripts | Secure server logic |
| StarterGui | Template for player GUI | ScreenGui instances |
| StarterPack | Template for player tools | Tool instances |
| StarterPlayerScripts | Template for client scripts | LocalScript instances |
| TweenService | Smooth animations | Create(), TweenInfo |
| SoundService | Audio management | SoundGroup, playback |
| DataStoreService | Persistent data saving | GetDataStore(), GetAsync(), SetAsync() |
| PathfindingService | NPC navigation | CreatePath(), ComputeAsync() |
| Teams | Team management | GetTeams(), Team objects |
| Lighting | Visual atmosphere | ClockTime, Atmosphere, Sky |
| Debris | Timed cleanup | AddItem(instance, lifetime) |

### Appendix C: Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Ctrl+S | Save place |
| Ctrl+Shift+S | Save place as |
| F5 | Play (test the game) |
| F6 | Play Here (test at current camera position) |
| F8 | Stop playtest |
| Ctrl+Z | Undo |
| Ctrl+Y | Redo |
| Ctrl+D | Duplicate selected |
| Delete | Delete selected |
| Ctrl+G | Group selected into Model |
| Ctrl+U | Ungroup Model |
| Alt+P | Toggle Properties panel |
| Alt+X | Toggle Explorer panel |
| Ctrl+Shift+X | Toggle Output panel |

### Appendix D: Vocabulary Glossary

| Term | Definition |
|------|------------|
| Instance | Any object in the Roblox data model (Parts, Scripts, Values, etc.) |
| Part | A basic 3D building block (Block, Sphere, Cylinder, Wedge) |
| Model | A container that groups multiple Parts and other instances |
| Script | Server-side Luau code that runs on the Roblox server |
| LocalScript | Client-side Luau code that runs on the player's device |
| ModuleScript | Reusable code that can be required by Scripts and LocalScripts |
| Humanoid | Controls character health, speed, jumping, and animations |
| Service | A top-level singleton in the data model (Players, Lighting, etc.) |
| RemoteEvent | Enables communication between client and server |
| DataStore | Persistent storage for saving player data between sessions |
| Leaderstats | A Folder convention under Player that auto-displays on the leaderboard |
| Debounce | A pattern to prevent an event from firing too rapidly |
| Touched | An event that fires when two Parts come into contact |
| CFrame | A data type representing position and orientation in 3D space |
| UDim2 | A data type for GUI sizing and positioning (scale + offset) |
| TweenInfo | Configuration for smooth property animations via TweenService |
| Luau | Roblox's programming language, a fast typed variant of Lua |
| Place | A single game world within a Roblox experience |
| Experience | A published Roblox game (may contain multiple places) |

---

## Document Information

| Field | Value |
|-------|-------|
| **Curriculum Version** | 1.0 |
| **Created** | March 2026 |
| **Target Standard** | Cambridge Lower Secondary Computing (0860) / IGCSE Computer Science (0478) |
| **Game Engine** | Roblox Studio |
| **Programming Language** | Luau |
| **Review Date** | September 2026 |

---

## Sources and References

- [Roblox Creator Hub](https://create.roblox.com/docs) - Official documentation and tutorials
- [Roblox Education](https://education.roblox.com/) - Educator resources and lesson plans
- [Luau Language Reference](https://luau-lang.org/) - Official Luau programming language documentation
- [Roblox API Reference](https://create.roblox.com/docs/reference/engine) - Complete API documentation
- [Roblox Creator Hub Tutorials](https://create.roblox.com/docs/tutorials) - Step-by-step guided tutorials
- [Roblox Community Standards](https://en.help.roblox.com/hc/en-us/articles/203313410) - Content guidelines for published games
- [Roblox for Educators](https://education.roblox.com/en-us/resources) - Classroom integration resources
- [TheDevKing Roblox Tutorials](https://www.youtube.com/@TheDevKing) - Video tutorial series
- [AlvinBlox Roblox Tutorials](https://www.youtube.com/@AlvinBlox) - Scripting tutorial series
- [DevForum Roblox](https://devforum.roblox.com/) - Developer community and knowledge base
- [Cambridge IGCSE Computer Science (0478)](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-igcse-computer-science-0478/)
- [Cambridge Lower Secondary Computing (0860)](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-lower-secondary/curriculum/computing/)
