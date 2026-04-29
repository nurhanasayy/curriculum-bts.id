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
