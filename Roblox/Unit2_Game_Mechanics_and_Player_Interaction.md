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
