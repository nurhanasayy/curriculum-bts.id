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
