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
