# Godot Engine Intermediate Game Development Curriculum
## Cambridge-Aligned Computing Course

---

## Table of Contents

- [Course Overview](#course-overview)
- [Cambridge Computing Standards Alignment](#cambridge-computing-standards-alignment)
- [Learning Objectives](#learning-objectives)

### Unit 1: Godot Fundamentals & GDScript Foundations (Sessions 1-4)
- [Session 1: Course Introduction & Godot Environment](#session-1-course-introduction--godot-environment)
- [Session 2: Nodes, Scenes, and the Scene Tree](#session-2-nodes-scenes-and-the-scene-tree)
- [Session 3: GDScript Fundamentals - Variables and Data Types](#session-3-gdscript-fundamentals---variables-and-data-types)
- [Session 4: GDScript Control Flow and Functions](#session-4-gdscript-control-flow-and-functions)

### Unit 2: 2D Game Development Essentials (Sessions 5-8)
- [Session 5: Sprites, Animation, and Movement](#session-5-sprites-animation-and-movement)
- [Session 6: Input Handling and Player Control](#session-6-input-handling-and-player-control)
- [Session 7: Collision Detection and Physics Bodies](#session-7-collision-detection-and-physics-bodies)
- [Session 8: Project 1 - Top-Down Shooter](#session-8-project-1---top-down-shooter)

### Unit 3: Signals and Game Architecture (Sessions 9-12)
- [Session 9: Understanding Signals](#session-9-understanding-signals)
- [Session 10: Scene Instancing and Management](#session-10-scene-instancing-and-management)
- [Session 11: Game State and Autoloads](#session-11-game-state-and-autoloads)
- [Session 12: Project 2 - Space Invaders Clone](#session-12-project-2---space-invaders-clone)

### Unit 4: Platformer Development (Sessions 13-16)
- [Session 13: CharacterBody2D and Platformer Physics](#session-13-characterbody2d-and-platformer-physics)
- [Session 14: Tilemaps and Level Design](#session-14-tilemaps-and-level-design)
- [Session 15: Enemies, AI, and Hazards](#session-15-enemies-ai-and-hazards)
- [Session 16: Project 3 - Platformer Game](#session-16-project-3---platformer-game)

### Unit 5: Polish and Game Systems (Sessions 17-20)
- [Session 17: User Interface Design](#session-17-user-interface-design)
- [Session 18: Audio Implementation](#session-18-audio-implementation)
- [Session 19: Save/Load Systems and Data Persistence](#session-19-saveload-systems-and-data-persistence)
- [Session 20: Particle Effects and Visual Polish](#session-20-particle-effects-and-visual-polish)

### Unit 6: Capstone Project & Publishing (Sessions 21-24)
- [Session 21: Capstone Project - Planning and Setup](#session-21-capstone-project---planning-and-setup)
- [Session 22: Capstone Project - Core Development](#session-22-capstone-project---core-development)
- [Session 23: Capstone Project - Polish and Testing](#session-23-capstone-project---polish-and-testing)
- [Session 24: Exporting, Publishing, and Portfolio Showcase](#session-24-exporting-publishing-and-portfolio-showcase)

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
| **Subject** | Game Development with Godot Engine 4 |
| **Level** | Intermediate |
| **Age Group** | 12-15 years old |
| **Total Sessions** | 24 sessions |
| **Session Duration** | 1 hour per session |
| **Total Hours** | 24 hours |
| **Prerequisites** | Basic programming concepts, familiarity with variables and loops |
| **Software** | Godot Engine 4.x (free, open-source) |

---

### Cambridge Computing Standards Alignment

This curriculum aligns with the **Cambridge Lower Secondary Computing (0860)** and prepares students for **Cambridge IGCSE Computer Science (0478)** through the following strands:

| Cambridge Strand | Coverage in This Course |
|------------------|-------------------------|
| **Computational Thinking** | Algorithm design, decomposition, abstraction, pattern recognition, debugging |
| **Programming** | GDScript syntax, variables, functions, classes, OOP concepts |
| **Managing Data** | Data types, arrays, dictionaries, file I/O, save systems |
| **Networks & Digital Communication** | Game exporting, distribution platforms, asset sharing |
| **Computer Systems** | Game engine architecture, rendering pipeline, physics simulation |

---

### Learning Objectives

By the end of this course, students will be able to:

1. **Programming Proficiency**
   - Write clean, organized GDScript code following best practices
   - Implement object-oriented programming concepts (classes, inheritance)
   - Use typed variables and understand data type management
   - Debug code using print statements, breakpoints, and the debugger

2. **Godot Engine Mastery**
   - Navigate and utilize the Godot 4 editor efficiently
   - Understand the node-scene architecture and scene tree
   - Implement signals for decoupled communication
   - Create reusable scenes and manage scene instancing

3. **Game Development Skills**
   - Build complete 2D games from concept to export
   - Implement player controls, physics, and collision detection
   - Design game systems (health, scoring, save/load)
   - Create polished games with UI, audio, and visual effects

4. **Computational Thinking**
   - Decompose complex problems into manageable components
   - Design algorithms using pseudocode and flowcharts
   - Test and debug programs systematically
   - Evaluate and optimize solutions

---

## Unit 1: Godot Fundamentals & GDScript Foundations
### Sessions 1-4

---

### Session 1: Course Introduction & Godot Environment

**Cambridge Alignment:** Computer Systems, Computational Thinking

**Learning Objectives:**
- Understand course structure and assessment criteria
- Navigate the Godot 4 editor interface
- Create and save a new project

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Introduction | Course overview, what we'll build, expectations |
| 10-20 min | Discussion | Why Godot? Open-source, industry adoption, career paths |
| 20-40 min | Interface Tour | Editor panels: Scene, FileSystem, Inspector, Node |
| 40-55 min | Practical | Create first project, explore the interface |
| 55-60 min | Reflection | Learning journal setup, questions |

**Key Concepts:**
- Godot's MIT license (free, no royalties)
- Editor layout and customization
- Project structure and file management
- Documentation and help resources

**Godot Interface Overview:**

| Panel | Purpose |
|-------|---------|
| Scene | View and manage node hierarchy |
| FileSystem | Browse project files and assets |
| Inspector | Edit properties of selected nodes |
| Node | Add new nodes to scene |
| Output | View print statements and errors |

**Assessment:**
- Formative: Interface navigation quiz
- Learning journal: Personal goals for the course

**Resources:**
- Godot Engine 4.x installed
- Learning journal template
- [Godot Documentation](https://docs.godotengine.org/)

---

### Session 2: Nodes, Scenes, and the Scene Tree

**Cambridge Alignment:** Computer Systems, Computational Thinking

**Learning Objectives:**
- Understand Godot's node-based architecture
- Create and organize scenes
- Explain the scene tree hierarchy

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Concept Introduction | Building blocks metaphor for nodes |
| 10-25 min | Theory | Node types, inheritance, scene tree |
| 25-45 min | Practical | Build a simple scene with multiple nodes |
| 45-55 min | Experimentation | Parent-child relationships, transforms |
| 55-60 min | Exit Ticket | Identify node types from descriptions |

**Key Concepts:**

```
Scene Tree Structure:
Root (Node2D)
├── Player (Sprite2D)
│   ├── CollisionShape2D
│   └── AnimatedSprite2D
├── Enemy (Sprite2D)
└── UI (CanvasLayer)
    └── ScoreLabel (Label)
```

**Common Node Types:**

| Node Type | Purpose | Example Use |
|-----------|---------|-------------|
| Node2D | Base for 2D objects | Parent containers |
| Sprite2D | Display images | Characters, items |
| CharacterBody2D | Physics character | Player, enemies |
| Area2D | Detect overlaps | Triggers, pickups |
| Camera2D | Game camera | Follow player |
| CanvasLayer | UI layer | Menus, HUD |

**Node Inheritance Chain:**
```
Node → CanvasItem → Node2D → Sprite2D
```

**Assessment:**
- Create a scene with proper node hierarchy
- Written: Explain parent-child relationships

---

### Session 3: GDScript Fundamentals - Variables and Data Types

**Cambridge Alignment:** Programming, Managing Data

**Learning Objectives:**
- Declare and use variables in GDScript
- Understand data types and type hints
- Write and attach scripts to nodes

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Connection | Compare GDScript to Python syntax |
| 10-25 min | Theory | Variables, types, constants, exports |
| 25-45 min | Practical | Create a script with various data types |
| 45-55 min | Challenge | Type conversion exercises |
| 55-60 min | Review | Common errors and debugging |

**GDScript Variable Declaration:**

```gdscript
extends Node2D

# Basic variables
var player_name = "Hero"        # Inferred as String
var health = 100                # Inferred as int
var speed = 5.5                 # Inferred as float
var is_alive = true             # Inferred as bool

# Typed variables (recommended)
var score: int = 0
var position_x: float = 0.0
var player_tag: String = "player"

# Constants (cannot change)
const MAX_HEALTH: int = 100
const GRAVITY: float = 9.8

# Export variables (editable in Inspector)
@export var jump_force: float = 400.0
@export var lives: int = 3
```

**Data Types Reference:**

| Type | Example | Description |
|------|---------|-------------|
| int | `42` | Whole numbers |
| float | `3.14` | Decimal numbers |
| String | `"Hello"` | Text |
| bool | `true/false` | Boolean values |
| Vector2 | `Vector2(10, 20)` | 2D coordinates |
| Array | `[1, 2, 3]` | List of values |
| Dictionary | `{"key": "value"}` | Key-value pairs |

**Assessment:**
- Script with 5+ correctly typed variables
- Debug challenge: Fix type-related errors

---

### Session 4: GDScript Control Flow and Functions

**Cambridge Alignment:** Programming, Computational Thinking

**Learning Objectives:**
- Implement conditional statements (if/elif/else)
- Use loops (for, while) effectively
- Define and call custom functions

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Algorithm Design | Pseudocode for game logic |
| 10-25 min | Theory | Conditionals, loops, functions |
| 25-45 min | Practical | Implement player health system |
| 45-55 min | Extension | Functions with parameters and returns |
| 55-60 min | Peer Review | Code review in pairs |

**Control Flow Examples:**

```gdscript
# Conditionals
func check_health():
    if health <= 0:
        die()
    elif health < 25:
        show_warning()
    else:
        continue_playing()

# For loop
func spawn_enemies(count: int):
    for i in range(count):
        var enemy = enemy_scene.instantiate()
        add_child(enemy)

# While loop
func wait_for_input():
    while not input_received:
        await get_tree().process_frame

# Functions with parameters and return
func calculate_damage(base: int, multiplier: float) -> int:
    var damage = int(base * multiplier)
    return damage
```

**Built-in Callback Functions:**

```gdscript
# Called when node enters scene tree
func _ready():
    print("Node is ready!")

# Called every frame (use for visuals)
func _process(delta: float):
    position.x += speed * delta

# Called at fixed intervals (use for physics)
func _physics_process(delta: float):
    move_and_slide()

# Called when input is detected
func _input(event: InputEvent):
    if event.is_action_pressed("jump"):
        jump()
```

**Assessment:**
- Implement a complete health system with functions
- Algorithm design: Write pseudocode before coding

---

## Unit 2: 2D Game Development Essentials
### Sessions 5-8

---

### Session 5: Sprites, Animation, and Movement

**Cambridge Alignment:** Programming, Computer Systems

**Learning Objectives:**
- Import and display sprites
- Create sprite animations with AnimatedSprite2D
- Implement basic movement with code

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Asset Preparation | Importing sprites and spritesheets |
| 10-25 min | Theory | Sprite2D vs AnimatedSprite2D, animation frames |
| 25-45 min | Practical | Create animated character with idle/walk |
| 45-55 min | Movement | Basic position-based movement |
| 55-60 min | Polish | Flip sprite based on direction |

**Animation Setup:**

```gdscript
extends Node2D

@onready var animated_sprite = $AnimatedSprite2D

func _ready():
    animated_sprite.play("idle")

func _process(delta):
    var direction = Input.get_axis("ui_left", "ui_right")

    if direction != 0:
        animated_sprite.play("walk")
        animated_sprite.flip_h = direction < 0
        position.x += direction * speed * delta
    else:
        animated_sprite.play("idle")
```

**Animation Best Practices:**
- Use consistent frame sizes in spritesheets
- Set appropriate animation speeds (FPS)
- Create smooth transitions between states
- Use AnimationPlayer for complex animations

**Assessment:**
- Character with 2+ animation states
- Smooth movement with direction flipping

---

### Session 6: Input Handling and Player Control

**Cambridge Alignment:** Programming, Computational Thinking

**Learning Objectives:**
- Configure the Input Map
- Handle keyboard, mouse, and gamepad input
- Create responsive player controls

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Input Map Setup | Project Settings > Input Map |
| 10-25 min | Theory | Input actions, polling vs events |
| 25-45 min | Practical | 8-directional movement system |
| 45-55 min | Extension | Mouse aiming and clicking |
| 55-60 min | Testing | Test with keyboard and controller |

**Input Map Configuration:**

| Action Name | Key Binding | Purpose |
|-------------|-------------|---------|
| move_left | A, Left Arrow | Move left |
| move_right | D, Right Arrow | Move right |
| move_up | W, Up Arrow | Move up |
| move_down | S, Down Arrow | Move down |
| jump | Space | Jump action |
| shoot | Left Mouse, Z | Fire weapon |
| pause | Escape | Pause game |

**Input Handling Code:**

```gdscript
extends CharacterBody2D

@export var speed: float = 200.0

func _physics_process(delta):
    # Get input direction as Vector2
    var direction = Input.get_vector(
        "move_left", "move_right",
        "move_up", "move_down"
    )

    # Normalize for consistent diagonal speed
    if direction.length() > 1:
        direction = direction.normalized()

    # Apply movement
    velocity = direction * speed
    move_and_slide()

func _input(event):
    if event.is_action_pressed("shoot"):
        shoot()

    if event.is_action_pressed("pause"):
        toggle_pause()
```

**Input Methods Comparison:**

| Method | When to Use |
|--------|-------------|
| `Input.is_action_pressed()` | Continuous checking (holding) |
| `Input.is_action_just_pressed()` | Single press detection |
| `Input.get_axis()` | 1D input (-1 to 1) |
| `Input.get_vector()` | 2D input (Vector2) |
| `_input(event)` | Event-based, one-time actions |

**Assessment:**
- Complete 8-directional movement
- At least 3 different input actions working

---

### Session 7: Collision Detection and Physics Bodies

**Cambridge Alignment:** Programming, Computer Systems

**Learning Objectives:**
- Understand collision layers and masks
- Differentiate between physics body types
- Implement collision responses

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Physics Concepts | Real-world collision examples |
| 10-25 min | Theory | Body types, layers, masks |
| 25-45 min | Practical | Player colliding with walls and pickups |
| 45-55 min | Signals | Using Area2D for overlap detection |
| 55-60 min | Debugging | Visualizing collision shapes |

**Physics Body Types:**

| Body Type | Purpose | Example |
|-----------|---------|---------|
| StaticBody2D | Immovable objects | Walls, platforms |
| CharacterBody2D | Controllable characters | Player, enemies |
| RigidBody2D | Physics-driven objects | Falling boxes, balls |
| Area2D | Overlap detection | Pickups, triggers |

**Collision Layers Setup:**

| Layer | Name | Contains |
|-------|------|----------|
| 1 | Player | Player character |
| 2 | Enemies | Enemy characters |
| 3 | World | Walls, platforms |
| 4 | Pickups | Collectibles |
| 5 | Projectiles | Bullets, weapons |

**Collision Code Examples:**

```gdscript
# Area2D for pickups
extends Area2D

signal collected(value)

@export var point_value: int = 10

func _ready():
    # Connect signal in code
    body_entered.connect(_on_body_entered)

func _on_body_entered(body):
    if body.is_in_group("player"):
        collected.emit(point_value)
        queue_free()
```

```gdscript
# CharacterBody2D collision response
extends CharacterBody2D

func _physics_process(delta):
    velocity.y += gravity * delta
    move_and_slide()

    # Check what we collided with
    for i in get_slide_collision_count():
        var collision = get_slide_collision(i)
        var collider = collision.get_collider()

        if collider.is_in_group("hazard"):
            take_damage(10)
```

**Assessment:**
- Player that collides with walls
- Working pickup system with Area2D

---

### Session 8: Project 1 - Top-Down Shooter

**Cambridge Alignment:** All Strands (Integration)

**Learning Objectives:**
- Apply all concepts from Unit 1-2
- Complete a playable game prototype
- Practice systematic debugging

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Planning | Game design document, feature list |
| 10-15 min | Setup | Project structure, scene organization |
| 15-50 min | Development | Build core gameplay loop |
| 50-55 min | Testing | Playtesting and bug fixes |
| 55-60 min | Showcase | Quick demo to partner |

**Project Requirements:**

- [ ] Player with 8-directional movement
- [ ] Mouse aiming for shooting direction
- [ ] Bullets that travel and destroy on impact
- [ ] At least 3 enemies with basic movement
- [ ] Collision detection (bullets hit enemies)
- [ ] Score counter
- [ ] Game over condition

**Scene Structure:**

```
Game (Node2D)
├── Player (CharacterBody2D)
│   ├── Sprite2D
│   ├── CollisionShape2D
│   └── Marker2D (gun position)
├── Enemies (Node2D)
│   └── [Enemy instances]
├── Bullets (Node2D)
│   └── [Bullet instances]
└── UI (CanvasLayer)
    ├── ScoreLabel
    └── GameOverPanel
```

**Bullet Spawning Pattern:**

```gdscript
# In Player script
@export var bullet_scene: PackedScene
@onready var gun_marker = $Marker2D

func shoot():
    var bullet = bullet_scene.instantiate()
    bullet.position = gun_marker.global_position
    bullet.rotation = global_position.angle_to_point(get_global_mouse_position())
    get_parent().get_node("Bullets").add_child(bullet)
```

**Assessment Rubric:**

| Criteria | Emerging (1) | Developing (2) | Proficient (3) | Advanced (4) |
|----------|--------------|----------------|----------------|--------------|
| Movement | Basic | Smooth | Polished | Juicy feedback |
| Shooting | Functional | Aimed | Rate-limited | Effects added |
| Enemies | Static | Moving | Patterns | AI behavior |
| Code Quality | Disorganized | Some structure | Well-organized | Commented |

---

## Unit 3: Signals and Game Architecture
### Sessions 9-12

---

### Session 9: Understanding Signals

**Cambridge Alignment:** Programming, Computational Thinking

**Learning Objectives:**
- Understand the observer pattern through signals
- Connect signals in editor and code
- Create custom signals

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Concept | "Call down, signal up" principle |
| 10-25 min | Theory | Built-in signals, custom signals |
| 25-45 min | Practical | Connect health changes to UI updates |
| 45-55 min | Extension | Signals with parameters |
| 55-60 min | Best Practices | When to use signals vs direct calls |

**Signal Fundamentals:**

```gdscript
# Defining custom signals
signal health_changed(new_health: int)
signal player_died
signal score_updated(score: int, multiplier: float)

# Emitting signals
func take_damage(amount: int):
    health -= amount
    health_changed.emit(health)

    if health <= 0:
        player_died.emit()
```

**Connecting Signals:**

```gdscript
# Method 1: In code (recommended for runtime)
func _ready():
    var player = get_node("Player")
    player.health_changed.connect(_on_player_health_changed)
    player.player_died.connect(_on_player_died)

func _on_player_health_changed(new_health: int):
    health_bar.value = new_health

func _on_player_died():
    show_game_over()

# Method 2: Editor connection (for static scenes)
# Use the Node panel > Signals tab > double-click to connect
```

**Signal Flow Diagram:**

```
Player (emits)          UI (receives)
    │                       │
    ├── health_changed ────►├── update_health_bar()
    │                       │
    ├── player_died ───────►├── show_game_over()
    │                       │
    └── score_updated ─────►└── update_score_label()
```

**Assessment:**
- Implement health system with signal-connected UI
- Diagram signal flow in your project

---

### Session 10: Scene Instancing and Management

**Cambridge Alignment:** Programming, Computational Thinking

**Learning Objectives:**
- Create reusable scenes
- Instance scenes at runtime
- Manage scene lifecycle

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Reusability | Why create separate scenes? |
| 10-25 min | Theory | PackedScene, instancing, freeing |
| 25-45 min | Practical | Enemy spawner system |
| 45-55 min | Advanced | Object pooling concept |
| 55-60 min | Optimization | When to use queue_free() |

**Scene Instancing:**

```gdscript
extends Node2D

@export var enemy_scene: PackedScene
@export var spawn_interval: float = 2.0

var spawn_timer: float = 0.0

func _process(delta):
    spawn_timer += delta
    if spawn_timer >= spawn_interval:
        spawn_timer = 0.0
        spawn_enemy()

func spawn_enemy():
    # Create instance from scene
    var enemy = enemy_scene.instantiate()

    # Set position
    enemy.position = get_random_spawn_position()

    # Connect signals before adding to tree
    enemy.died.connect(_on_enemy_died)

    # Add to scene tree
    add_child(enemy)

func get_random_spawn_position() -> Vector2:
    var viewport_size = get_viewport_rect().size
    return Vector2(
        randf_range(0, viewport_size.x),
        randf_range(-50, -10)  # Spawn above screen
    )

func _on_enemy_died(points: int):
    # Handle enemy death, update score, etc.
    GameManager.add_score(points)
```

**Scene Lifecycle:**

| Stage | Method | Use Case |
|-------|--------|----------|
| Created | `instantiate()` | Object exists in memory |
| Added | `add_child()` | `_ready()` called |
| Active | `_process()` | Every frame |
| Removed | `queue_free()` | Safe deletion at frame end |

**Assessment:**
- Create enemy spawner with configurable settings
- Properly clean up instances when destroyed

---

### Session 11: Game State and Autoloads

**Cambridge Alignment:** Programming, Managing Data

**Learning Objectives:**
- Implement global game state
- Use Autoload for persistent data
- Manage scene transitions

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Problem | How to share data between scenes? |
| 10-25 min | Theory | Autoloads (singletons), scene changing |
| 25-45 min | Practical | Create GameManager autoload |
| 45-55 min | Scene Transitions | Main menu to gameplay |
| 55-60 min | Best Practices | What belongs in autoloads |

**GameManager Autoload:**

```gdscript
# game_manager.gd - Add as Autoload in Project Settings
extends Node

# Signals for global events
signal score_changed(new_score: int)
signal game_over
signal game_paused(is_paused: bool)

# Game state
var score: int = 0
var high_score: int = 0
var current_level: int = 1
var is_paused: bool = false

func _ready():
    # Load saved high score
    load_high_score()

func add_score(points: int):
    score += points
    score_changed.emit(score)

    if score > high_score:
        high_score = score

func reset_game():
    score = 0
    current_level = 1
    is_paused = false

func toggle_pause():
    is_paused = !is_paused
    get_tree().paused = is_paused
    game_paused.emit(is_paused)

func change_scene(scene_path: String):
    get_tree().change_scene_to_file(scene_path)

func reload_current_scene():
    get_tree().reload_current_scene()
```

**Scene Management:**

```gdscript
# Main Menu
extends Control

func _on_play_button_pressed():
    GameManager.reset_game()
    GameManager.change_scene("res://scenes/game.tscn")

func _on_quit_button_pressed():
    get_tree().quit()

# In-game pause
func _input(event):
    if event.is_action_pressed("pause"):
        GameManager.toggle_pause()
```

**Autoload Setup:**
1. Go to Project > Project Settings > Autoload
2. Add script path
3. Set node name (e.g., "GameManager")
4. Access anywhere: `GameManager.score`

**Assessment:**
- Working GameManager with score tracking
- Scene transitions between menu and game

---

### Session 12: Project 2 - Space Invaders Clone

**Cambridge Alignment:** All Strands (Integration)

**Learning Objectives:**
- Build a complete arcade-style game
- Implement wave-based enemy spawning
- Create a full game loop (menu → play → game over)

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Planning | Game design, wave system design |
| 10-50 min | Development | Build Space Invaders clone |
| 50-55 min | Testing | Balance and bug fixes |
| 55-60 min | Showcase | Demo to class |

**Project Requirements:**

- [ ] Player ship with horizontal movement
- [ ] Shooting mechanic with cooldown
- [ ] Grid of enemies that move and descend
- [ ] Enemies shoot back at player
- [ ] Lives system (3 lives)
- [ ] Score system with high score
- [ ] Wave progression (increasing difficulty)
- [ ] Main menu and game over screens
- [ ] Sound effects for shooting and explosions

**Wave System:**

```gdscript
extends Node2D

signal wave_completed

@export var enemy_scene: PackedScene
@export var rows: int = 5
@export var columns: int = 11
@export var spacing: Vector2 = Vector2(50, 40)

var enemies_remaining: int = 0
var current_wave: int = 1

func spawn_wave():
    enemies_remaining = rows * columns

    for row in range(rows):
        for col in range(columns):
            var enemy = enemy_scene.instantiate()
            enemy.position = Vector2(
                col * spacing.x + 100,
                row * spacing.y + 50
            )
            # Increase speed based on wave
            enemy.speed *= 1.0 + (current_wave * 0.1)
            enemy.died.connect(_on_enemy_died)
            add_child(enemy)

func _on_enemy_died(_points: int):
    enemies_remaining -= 1
    if enemies_remaining <= 0:
        current_wave += 1
        wave_completed.emit()
        # Spawn next wave after delay
        await get_tree().create_timer(2.0).timeout
        spawn_wave()
```

**Assessment Rubric:**

| Criteria | Points | Requirements |
|----------|--------|--------------|
| Core Gameplay | 25 | Player, enemies, shooting works |
| Wave System | 20 | Multiple waves with progression |
| Polish | 20 | UI, audio, visual feedback |
| Game Loop | 20 | Menu, play, game over states |
| Code Quality | 15 | Organized, signals used properly |

---

## Unit 4: Platformer Development
### Sessions 13-16

---

### Session 13: CharacterBody2D and Platformer Physics

**Cambridge Alignment:** Programming, Computer Systems

**Learning Objectives:**
- Implement platformer movement with CharacterBody2D
- Apply gravity and jumping mechanics
- Handle slopes and one-way platforms

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Physics Concepts | Gravity, velocity, acceleration |
| 10-25 min | Theory | CharacterBody2D methods, floor detection |
| 25-45 min | Practical | Build platformer controller |
| 45-55 min | Refinement | Coyote time, jump buffering |
| 55-60 min | Feel Testing | Adjust values for good game feel |

**Platformer Controller:**

```gdscript
extends CharacterBody2D

@export var speed: float = 300.0
@export var jump_velocity: float = -400.0
@export var gravity: float = 980.0

# Advanced movement feel
@export var acceleration: float = 2000.0
@export var friction: float = 1500.0
@export var air_resistance: float = 200.0

# Jump improvements
var coyote_time: float = 0.1
var coyote_timer: float = 0.0
var jump_buffer_time: float = 0.1
var jump_buffer_timer: float = 0.0

func _physics_process(delta: float):
    # Apply gravity
    if not is_on_floor():
        velocity.y += gravity * delta
        coyote_timer -= delta
    else:
        coyote_timer = coyote_time

    # Handle jump buffer
    if Input.is_action_just_pressed("jump"):
        jump_buffer_timer = jump_buffer_time
    jump_buffer_timer -= delta

    # Jump with coyote time and buffer
    if jump_buffer_timer > 0 and coyote_timer > 0:
        velocity.y = jump_velocity
        jump_buffer_timer = 0
        coyote_timer = 0

    # Horizontal movement
    var direction = Input.get_axis("move_left", "move_right")
    var target_velocity = direction * speed

    if is_on_floor():
        if direction != 0:
            velocity.x = move_toward(velocity.x, target_velocity, acceleration * delta)
        else:
            velocity.x = move_toward(velocity.x, 0, friction * delta)
    else:
        velocity.x = move_toward(velocity.x, target_velocity, air_resistance * delta)

    move_and_slide()
```

**Physics Parameters:**

| Parameter | Range | Effect |
|-----------|-------|--------|
| Speed | 200-400 | Horizontal movement speed |
| Jump Velocity | -300 to -500 | Jump height (negative = up) |
| Gravity | 800-1200 | Fall speed |
| Coyote Time | 0.05-0.15 | Forgiveness for late jumps |
| Jump Buffer | 0.05-0.15 | Forgiveness for early jumps |

**Assessment:**
- Platformer controller with smooth movement
- Implement at least one advanced feature (coyote time or variable jump)

---

### Session 14: Tilemaps and Level Design

**Cambridge Alignment:** Computer Systems, Computational Thinking

**Learning Objectives:**
- Create and configure TileMap layers
- Design levels using the tilemap editor
- Implement auto-tiling for efficient level creation

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Tileset Introduction | Importing and configuring tilesets |
| 10-25 min | Theory | TileMap layers, physics, auto-tiles |
| 25-45 min | Practical | Create a complete game level |
| 45-55 min | Level Design | Principles of good level design |
| 55-60 min | Iteration | Playtest and refine level |

**TileMap Setup:**

```
TileMapLayer Node Configuration:
├── Tile Set: Create from spritesheet
├── Tile Size: 16x16 or 32x32 (match your art)
├── Physics Layer: Add collision for solid tiles
└── Terrain Sets: Configure for auto-tiling
```

**Level Design Principles:**

| Principle | Description | Example |
|-----------|-------------|---------|
| Teach through play | Introduce mechanics safely | First jump over small gap |
| Progressive difficulty | Gradual challenge increase | Wider gaps later |
| Safe spaces | Areas to recover | Checkpoints |
| Visual clarity | Clear communication | Hazards look dangerous |
| Rhythm | Flow of challenges | Platforming → combat → rest |

**Multiple TileMap Layers:**

```
Level (Node2D)
├── Background (TileMapLayer) - z_index: -1
├── Terrain (TileMapLayer) - z_index: 0, has collision
├── Decorations (TileMapLayer) - z_index: 1
└── Foreground (TileMapLayer) - z_index: 2
```

**Assessment:**
- Create a complete level with proper collision
- Apply at least 3 level design principles

---

### Session 15: Enemies, AI, and Hazards

**Cambridge Alignment:** Programming, Computational Thinking

**Learning Objectives:**
- Create enemy types with different behaviors
- Implement simple AI patterns
- Design environmental hazards

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | AI Design | State machines for enemy behavior |
| 10-25 min | Theory | Patrol, chase, attack patterns |
| 25-45 min | Practical | Walking enemy, flying enemy |
| 45-55 min | Hazards | Spikes, moving platforms |
| 55-60 min | Balance | Enemy placement and difficulty |

**Enemy State Machine:**

```gdscript
extends CharacterBody2D

enum State { IDLE, PATROL, CHASE, ATTACK }

@export var patrol_speed: float = 50.0
@export var chase_speed: float = 100.0
@export var detection_range: float = 200.0
@export var attack_range: float = 30.0

var current_state: State = State.PATROL
var patrol_direction: int = 1
var player: Node2D = null

func _ready():
    player = get_tree().get_first_node_in_group("player")

func _physics_process(delta):
    match current_state:
        State.PATROL:
            patrol(delta)
        State.CHASE:
            chase(delta)
        State.ATTACK:
            attack()

    move_and_slide()

func patrol(delta):
    velocity.x = patrol_direction * patrol_speed

    # Check for walls or ledges
    if is_on_wall() or not $FloorChecker.is_colliding():
        patrol_direction *= -1

    # Check for player
    if player and position.distance_to(player.position) < detection_range:
        current_state = State.CHASE

func chase(delta):
    var direction = sign(player.position.x - position.x)
    velocity.x = direction * chase_speed

    if position.distance_to(player.position) < attack_range:
        current_state = State.ATTACK
    elif position.distance_to(player.position) > detection_range * 1.5:
        current_state = State.PATROL

func attack():
    # Play attack animation, deal damage
    velocity.x = 0
    # Return to chase after attack
    await get_tree().create_timer(0.5).timeout
    current_state = State.CHASE
```

**Hazard Types:**

| Hazard | Behavior | Implementation |
|--------|----------|----------------|
| Spikes | Instant damage | Area2D with damage signal |
| Moving Platform | Carries player | AnimatableBody2D with AnimationPlayer |
| Falling Platform | Falls after stepped on | Timer + RigidBody2D conversion |
| Projectile Trap | Shoots periodically | Timer + instance bullets |

**Assessment:**
- Create 2 enemy types with different behaviors
- Implement 1 environmental hazard

---

### Session 16: Project 3 - Platformer Game

**Cambridge Alignment:** All Strands (Integration)

**Learning Objectives:**
- Build a complete platformer game
- Implement multiple levels
- Create a cohesive game experience

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Planning | Level design sketches, feature priority |
| 10-50 min | Development | Build platformer with 2+ levels |
| 50-55 min | Testing | Playtesting, balance adjustments |
| 55-60 min | Peer Feedback | Exchange games for feedback |

**Project Requirements:**

- [ ] Player with full platformer controls
- [ ] At least 2 complete levels
- [ ] 2 enemy types with unique behaviors
- [ ] Environmental hazards (spikes, pits)
- [ ] Collectibles (coins, gems)
- [ ] Health/lives system
- [ ] Level transitions
- [ ] Checkpoints or respawn system
- [ ] Win condition (reach goal)

**Project Structure:**

```
res://
├── scenes/
│   ├── player/
│   │   └── player.tscn
│   ├── enemies/
│   │   ├── walker.tscn
│   │   └── flyer.tscn
│   ├── levels/
│   │   ├── level_1.tscn
│   │   └── level_2.tscn
│   └── ui/
│       ├── hud.tscn
│       └── pause_menu.tscn
├── scripts/
│   ├── player.gd
│   ├── enemy_base.gd
│   └── game_manager.gd
├── assets/
│   ├── sprites/
│   ├── audio/
│   └── tilesets/
└── autoload/
    └── game_manager.gd
```

**Assessment Rubric:**

| Criteria | Emerging (1) | Developing (2) | Proficient (3) | Advanced (4) |
|----------|--------------|----------------|----------------|--------------|
| Controls | Functional | Responsive | Polished | Excellent feel |
| Level Design | Basic | Interesting | Well-paced | Teaches mechanics |
| Enemies | Single type | Two types | Unique behaviors | AI states |
| Systems | Basic | Complete | Polished | Interconnected |

---

## Unit 5: Polish and Game Systems
### Sessions 17-20

---

### Session 17: User Interface Design

**Cambridge Alignment:** Programming, Managing Data

**Learning Objectives:**
- Create responsive UI with Control nodes
- Implement HUD elements
- Design menu systems with proper navigation

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | UI/UX Principles | Clarity, consistency, feedback |
| 10-25 min | Theory | Control nodes, anchors, containers |
| 25-45 min | Practical | Build game HUD and pause menu |
| 45-55 min | Theming | StyleBox and custom themes |
| 55-60 min | Accessibility | Font sizes, color contrast |

**Control Node Hierarchy:**

```
UI (CanvasLayer)
├── HUD (Control)
│   ├── MarginContainer
│   │   └── HBoxContainer
│   │       ├── HealthBar (TextureProgressBar)
│   │       └── ScoreLabel (Label)
│   └── LivesContainer (HBoxContainer)
│       └── [Heart icons]
└── PauseMenu (Control)
    └── CenterContainer
        └── VBoxContainer
            ├── Label ("PAUSED")
            ├── ResumeButton
            ├── SettingsButton
            └── QuitButton
```

**HUD Script:**

```gdscript
extends CanvasLayer

@onready var health_bar = $HUD/HealthBar
@onready var score_label = $HUD/ScoreLabel
@onready var pause_menu = $PauseMenu

func _ready():
    # Connect to GameManager signals
    GameManager.score_changed.connect(_on_score_changed)
    GameManager.game_paused.connect(_on_game_paused)

    # Connect to player signals
    var player = get_tree().get_first_node_in_group("player")
    if player:
        player.health_changed.connect(_on_health_changed)

    pause_menu.visible = false

func _on_score_changed(new_score: int):
    score_label.text = "Score: %d" % new_score

func _on_health_changed(new_health: int):
    health_bar.value = new_health

func _on_game_paused(is_paused: bool):
    pause_menu.visible = is_paused
```

**Common Control Nodes:**

| Node | Purpose |
|------|---------|
| Label | Display text |
| Button | Clickable button |
| TextureRect | Display images |
| ProgressBar | Health/loading bars |
| HBoxContainer | Horizontal layout |
| VBoxContainer | Vertical layout |
| MarginContainer | Add padding |
| CenterContainer | Center content |

**Assessment:**
- Complete HUD with health, score, lives
- Working pause menu with navigation

---

### Session 18: Audio Implementation

**Cambridge Alignment:** Programming, Computer Systems

**Learning Objectives:**
- Import and play sound effects
- Implement background music with crossfading
- Create an audio manager for volume control

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Audio in Games | Importance of sound design |
| 10-25 min | Theory | AudioStreamPlayer, buses, formats |
| 25-45 min | Practical | Add SFX and music to game |
| 45-55 min | Audio Manager | Volume controls, muting |
| 55-60 min | Polish | Audio feedback for all actions |

**Audio Setup:**

```gdscript
# AudioManager Autoload
extends Node

@onready var music_player = $MusicPlayer
@onready var sfx_players: Array[AudioStreamPlayer] = []

const MAX_SFX_PLAYERS = 8

func _ready():
    # Create pool of SFX players
    for i in range(MAX_SFX_PLAYERS):
        var player = AudioStreamPlayer.new()
        player.bus = "SFX"
        add_child(player)
        sfx_players.append(player)

func play_sfx(sound: AudioStream, volume_db: float = 0.0):
    for player in sfx_players:
        if not player.playing:
            player.stream = sound
            player.volume_db = volume_db
            player.play()
            return
    # All players busy, use first one
    sfx_players[0].stream = sound
    sfx_players[0].play()

func play_music(music: AudioStream, fade_duration: float = 1.0):
    var tween = create_tween()
    tween.tween_property(music_player, "volume_db", -40, fade_duration)
    await tween.finished

    music_player.stream = music
    music_player.play()

    tween = create_tween()
    tween.tween_property(music_player, "volume_db", 0, fade_duration)

func set_music_volume(value: float):
    AudioServer.set_bus_volume_db(
        AudioServer.get_bus_index("Music"),
        linear_to_db(value)
    )

func set_sfx_volume(value: float):
    AudioServer.set_bus_volume_db(
        AudioServer.get_bus_index("SFX"),
        linear_to_db(value)
    )
```

**Audio Bus Setup:**
1. Go to bottom panel > Audio
2. Add buses: Master, Music, SFX
3. Route Music and SFX to Master
4. Add effects if needed (reverb, compression)

**Assessment:**
- All player actions have sound feedback
- Background music with proper transitions
- Volume controls in settings menu

---

### Session 19: Save/Load Systems and Data Persistence

**Cambridge Alignment:** Managing Data, Programming

**Learning Objectives:**
- Save game data to files
- Load and validate saved data
- Implement settings persistence

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Data Design | What to save, file formats |
| 10-25 min | Theory | FileAccess, JSON, ConfigFile |
| 25-45 min | Practical | Implement save/load system |
| 45-55 min | Settings | Persist audio/video settings |
| 55-60 min | Error Handling | What if file is corrupted? |

**Save System Implementation:**

```gdscript
# save_manager.gd (Autoload)
extends Node

const SAVE_PATH = "user://savegame.json"
const SETTINGS_PATH = "user://settings.cfg"

func save_game():
    var save_data = {
        "player": {
            "position_x": player.position.x,
            "position_y": player.position.y,
            "health": player.health,
            "lives": player.lives
        },
        "game": {
            "score": GameManager.score,
            "current_level": GameManager.current_level,
            "unlocked_levels": GameManager.unlocked_levels
        },
        "timestamp": Time.get_unix_time_from_system()
    }

    var file = FileAccess.open(SAVE_PATH, FileAccess.WRITE)
    if file:
        file.store_string(JSON.stringify(save_data, "\t"))
        file.close()
        print("Game saved!")
        return true
    return false

func load_game() -> bool:
    if not FileAccess.file_exists(SAVE_PATH):
        print("No save file found")
        return false

    var file = FileAccess.open(SAVE_PATH, FileAccess.READ)
    if file:
        var json_string = file.get_as_text()
        file.close()

        var json = JSON.new()
        var error = json.parse(json_string)
        if error == OK:
            var save_data = json.get_data()
            apply_save_data(save_data)
            return true

    print("Failed to load save file")
    return false

func apply_save_data(data: Dictionary):
    GameManager.score = data.game.score
    GameManager.current_level = data.game.current_level
    # Apply other data...

func save_settings():
    var config = ConfigFile.new()
    config.set_value("audio", "music_volume", AudioManager.music_volume)
    config.set_value("audio", "sfx_volume", AudioManager.sfx_volume)
    config.set_value("video", "fullscreen", DisplayServer.window_get_mode() == DisplayServer.WINDOW_MODE_FULLSCREEN)
    config.save(SETTINGS_PATH)

func load_settings():
    var config = ConfigFile.new()
    if config.load(SETTINGS_PATH) == OK:
        AudioManager.set_music_volume(config.get_value("audio", "music_volume", 1.0))
        AudioManager.set_sfx_volume(config.get_value("audio", "sfx_volume", 1.0))
        # Apply other settings...
```

**Save Data Validation:**

```gdscript
func validate_save_data(data: Dictionary) -> bool:
    # Check required keys exist
    if not data.has("player") or not data.has("game"):
        return false

    # Validate data types and ranges
    if not data.player.health is int:
        return false
    if data.player.health < 0 or data.player.health > 100:
        data.player.health = clamp(data.player.health, 0, 100)

    return true
```

**Assessment:**
- Working save/load system for game progress
- Settings persistence (audio volumes)

---

### Session 20: Particle Effects and Visual Polish

**Cambridge Alignment:** Programming, Computer Systems

**Learning Objectives:**
- Create particle effects with GPUParticles2D
- Implement screen shake and visual feedback
- Apply tweening for animations

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-10 min | Juice Concepts | What makes games feel good? |
| 10-25 min | Theory | Particles, tweens, shaders basics |
| 25-45 min | Practical | Add particles and screen effects |
| 45-55 min | Tweening | Smooth animations for UI and gameplay |
| 55-60 min | Before/After | Compare polished vs unpolished |

**Particle System Setup:**

```gdscript
# Explosion particles
extends GPUParticles2D

func _ready():
    emitting = true
    one_shot = true

    # Auto-destroy after animation
    await get_tree().create_timer(lifetime).timeout
    queue_free()
```

**Screen Shake:**

```gdscript
# Add to Camera2D
extends Camera2D

var shake_intensity: float = 0.0
var shake_decay: float = 5.0

func shake(intensity: float, duration: float = 0.3):
    shake_intensity = intensity

    var tween = create_tween()
    tween.tween_property(self, "shake_intensity", 0.0, duration)

func _process(delta):
    if shake_intensity > 0:
        offset = Vector2(
            randf_range(-shake_intensity, shake_intensity),
            randf_range(-shake_intensity, shake_intensity)
        )
    else:
        offset = Vector2.ZERO
```

**Tweening for Polish:**

```gdscript
# Collectible pickup effect
func collect():
    var tween = create_tween()
    tween.set_parallel(true)

    # Scale up then disappear
    tween.tween_property(self, "scale", Vector2(1.5, 1.5), 0.1)
    tween.tween_property(self, "modulate:a", 0.0, 0.2)

    await tween.finished
    queue_free()

# UI element entrance
func show_score_popup(amount: int, pos: Vector2):
    var label = score_popup_scene.instantiate()
    label.text = "+%d" % amount
    label.position = pos
    add_child(label)

    var tween = create_tween()
    tween.tween_property(label, "position:y", pos.y - 50, 0.5)
    tween.parallel().tween_property(label, "modulate:a", 0.0, 0.5).set_delay(0.3)

    await tween.finished
    label.queue_free()
```

**Polish Checklist:**

- [ ] Particles for: explosions, pickups, footsteps
- [ ] Screen shake on impacts
- [ ] Tweened UI transitions
- [ ] Hit flash on enemies
- [ ] Squash/stretch on jumps
- [ ] Trail effects on fast movement

**Assessment:**
- Add 3+ particle effects to game
- Implement screen shake on impacts
- Tween at least 2 UI elements

---

## Unit 6: Capstone Project & Publishing
### Sessions 21-24

---

### Session 21: Capstone Project - Planning and Setup

**Cambridge Alignment:** All Strands, Project Management

**Learning Objectives:**
- Design a complete game from concept
- Create a project plan with milestones
- Set up project architecture

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-15 min | Ideation | Brainstorm game concepts |
| 15-30 min | Design Document | Define scope, features, goals |
| 30-50 min | Setup | Create project, establish architecture |
| 50-60 min | Planning | Break down into tasks, set milestones |

**Game Design Document Template:**

```
GAME TITLE: _______________

CONCEPT:
- Genre: _______________
- Core mechanic: _______________
- Target experience: _______________

FEATURES (Priority Order):
Must Have:
1. _______________
2. _______________
3. _______________

Nice to Have:
1. _______________
2. _______________

TECHNICAL SCOPE:
- Scenes needed: _______________
- Enemy types: _______________
- Power-ups/items: _______________
- Levels: _______________

VISUAL STYLE:
- Art direction: _______________
- Color palette: _______________

AUDIO:
- Music style: _______________
- Key sound effects: _______________
```

**Project Milestones:**

| Session | Milestone | Deliverable |
|---------|-----------|-------------|
| 21 | Planning | GDD, project setup |
| 22 | Core Loop | Playable prototype |
| 23 | Polish | Complete, tested game |
| 24 | Export | Published game |

**Assessment:**
- Complete Game Design Document
- Project structure set up

---

### Session 22: Capstone Project - Core Development

**Cambridge Alignment:** All Strands (Integration)

**Learning Objectives:**
- Implement core gameplay mechanics
- Create a playable prototype
- Apply rapid iteration

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-5 min | Check-in | Review GDD, clarify scope |
| 5-55 min | Development | Build core game loop |
| 55-60 min | Progress Report | Demonstrate current state |

**Development Priorities:**

1. **Player controller** - Movement feels good
2. **Core mechanic** - Main interaction works
3. **Basic enemy/challenge** - Something to overcome
4. **Win/lose condition** - Game has completion
5. **Minimum UI** - Player can understand state

**Troubleshooting Session:**

| Common Issue | Solution |
|--------------|----------|
| Scope creep | Return to GDD, cut features |
| Bug blocking progress | Simplify, isolate problem |
| Art taking too long | Use placeholders |
| Feature not working | Check documentation, ask for help |

---

### Session 23: Capstone Project - Polish and Testing

**Cambridge Alignment:** All Strands, Testing

**Learning Objectives:**
- Add polish to improve game feel
- Conduct systematic testing
- Iterate based on feedback

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-5 min | Status Check | What's working, what's needed |
| 5-30 min | Polish | Audio, particles, UI improvements |
| 30-45 min | Peer Testing | Play each other's games |
| 45-55 min | Feedback Integration | Quick fixes based on testing |
| 55-60 min | Final Prep | Prepare for export |

**Testing Checklist:**

```
FUNCTIONALITY:
[ ] All controls work as expected
[ ] No crashes or freezes
[ ] Win/lose conditions trigger correctly
[ ] Score/lives update properly
[ ] All menus navigate correctly

BALANCE:
[ ] Difficulty feels fair
[ ] Progression makes sense
[ ] No impossible situations

POLISH:
[ ] All actions have audio feedback
[ ] Visual effects enhance gameplay
[ ] UI is clear and readable
[ ] No placeholder art remains

EDGE CASES:
[ ] What if player does nothing?
[ ] What if player spams input?
[ ] What if player goes out of bounds?
```

**Peer Testing Feedback Form:**

1. What was the most fun part?
2. What was confusing?
3. Did you encounter any bugs?
4. What would you add/change?
5. Rate overall experience (1-5)

---

### Session 24: Exporting, Publishing, and Portfolio Showcase

**Cambridge Alignment:** Networks & Digital Communication, Presentation

**Learning Objectives:**
- Export game for different platforms
- Create marketing materials
- Present and showcase portfolio

**Lesson Structure:**

| Time | Activity | Description |
|------|----------|-------------|
| 0-15 min | Export Process | Export to web/desktop |
| 15-25 min | Marketing | Screenshots, description, itch.io page |
| 25-45 min | Presentations | 3-minute game showcases |
| 45-55 min | Celebration | Play each other's games |
| 55-60 min | Reflection | Course wrap-up, next steps |

**Export Settings:**

```
Project > Export > Add Preset:

Web (HTML5):
├── Export Type: Regular
├── Custom HTML Shell: default
└── Output: game.html + game.pck

Windows Desktop:
├── Export Type: Regular
├── 64 Bits: Yes
└── Output: game.exe

Note: First export requires downloading templates
```

**Publishing Checklist:**

- [ ] Game icon (512x512 PNG)
- [ ] Cover image (630x500 for itch.io)
- [ ] 3-5 screenshots
- [ ] Game description (genre, controls, features)
- [ ] Credits (assets, music, tools used)
- [ ] Control instructions

**Portfolio Components:**

1. **Project 1:** Top-Down Shooter
2. **Project 2:** Space Invaders Clone
3. **Project 3:** Platformer Game
4. **Capstone Project:** Original game

**Final Reflection Questions:**

1. What was your biggest technical challenge and how did you overcome it?
2. Which programming concept was most valuable to learn?
3. How has your approach to problem-solving improved?
4. What type of game would you like to create next?

---

## Assessment Framework

### Summative Assessments

| Assessment | Weight | Session | Description |
|------------|--------|---------|-------------|
| Project 1: Top-Down Shooter | 15% | 8 | First complete game prototype |
| Project 2: Space Invaders | 20% | 12 | Game with signals and systems |
| Project 3: Platformer | 25% | 16 | Complex game with multiple levels |
| Capstone Project | 30% | 21-24 | Original game from concept to export |
| Learning Journal | 10% | Ongoing | Reflection and documentation |

### Formative Assessments

- Weekly code review
- Exit tickets after each session
- Debugging challenges
- Peer testing sessions
- Algorithm design exercises (pseudocode/flowcharts)

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
| **Code Quality** | Disorganized, many errors | Some structure, some errors | Well-organized, runs correctly | Clean, efficient, well-commented |
| **Gameplay** | Barely functional | Works but unpolished | Smooth and enjoyable | Excellent game feel |
| **Creativity** | Template only | Minor modifications | Unique elements | Innovative design |
| **Technical Depth** | Basic features | Standard implementation | Advanced features | Exceeds expectations |
| **Completion** | Incomplete | Missing elements | All requirements met | Extra features added |

---

## Resources and Materials

### Required Software
- Godot Engine 4.x ([godotengine.org](https://godotengine.org/))
- Web browser for documentation
- Code editor (built-in or VS Code with Godot plugin)

### Recommended Learning Resources

**Official Documentation:**
- [Godot Documentation](https://docs.godotengine.org/)
- [GDScript Reference](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_basics.html)

**Tutorials:**
- [GDQuest](https://www.gdquest.com/) - High-quality tutorials
- [Godot Tutorials](https://godottutorials.com/) - Free video series
- [KidsCanCode Godot Recipes](https://kidscancode.org/godot_recipes/)

**Asset Sources:**
- [Kenney.nl](https://kenney.nl/) - Free game assets
- [OpenGameArt.org](https://opengameart.org/) - Community assets
- [itch.io Game Assets](https://itch.io/game-assets)
- [Freesound.org](https://freesound.org/) - Audio

**Cambridge Resources:**
- [Cambridge IGCSE Computer Science](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-igcse-computer-science-0478/)
- [Cambridge Lower Secondary Computing](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-lower-secondary/curriculum/computing/)

---

## Differentiation Strategies

### Support for Struggling Learners
- Provide starter projects with partial code
- Pair programming opportunities
- Step-by-step visual guides
- Extended time for projects
- Simplified project requirements
- One-on-one debugging sessions

### Extension for Advanced Learners
- 3D game development introduction
- Shader programming
- Custom plugin development
- Multiplayer networking basics
- Mentor role for peers
- Advanced AI implementations

### Accessibility Considerations
- High contrast editor themes
- Keyboard-only navigation options
- Clear code commenting
- Audio descriptions for visual content
- Flexible assessment formats

---

## Teacher Notes

### Preparation Before Course

1. Install Godot 4.x on all classroom computers
2. Create template projects for each session
3. Prepare asset packs (sprites, sounds)
4. Set up submission/sharing system
5. Review Cambridge assessment objectives
6. Test all project requirements

### Session Structure Recommendations

- **First 10 minutes:** Review, concept introduction
- **Middle 35-40 minutes:** Hands-on practical work
- **Final 10-15 minutes:** Reflection, troubleshooting, preview

### Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| GDScript syntax errors | Use built-in error highlighting |
| Node paths not working | Check scene tree, use `$` shortcuts |
| Signals not connecting | Verify connection in editor/code |
| Physics not working | Check collision layers/masks |
| Export fails | Download export templates first |
| Performance issues | Reduce particle count, optimize code |

### Classroom Management Tips

- Establish debugging protocol (try 3 things first)
- Create peer helper system
- Regular save reminders
- Celebrate small wins
- Build in catch-up time during project sessions
- Use version control for advanced groups

---

## Appendices

### Appendix A: GDScript Quick Reference

```gdscript
# Variables
var my_var = 10
var typed_var: int = 10
const MY_CONST = 100
@export var exported: float = 5.0

# Functions
func my_function(param: int) -> String:
    return "Result: " + str(param)

# Conditionals
if condition:
    pass
elif other_condition:
    pass
else:
    pass

# Loops
for i in range(10):
    print(i)

for item in array:
    print(item)

while condition:
    pass

# Classes
class_name MyClass
extends Node2D

# Signals
signal my_signal(value: int)
my_signal.emit(42)

# Common methods
_ready()
_process(delta)
_physics_process(delta)
_input(event)
```

### Appendix B: Common Node Reference

| Node | Purpose | Key Properties |
|------|---------|----------------|
| Node2D | 2D object base | position, rotation, scale |
| Sprite2D | Display image | texture, flip_h, flip_v |
| AnimatedSprite2D | Sprite animations | animation, playing |
| CharacterBody2D | Kinematic character | velocity, move_and_slide() |
| RigidBody2D | Physics object | mass, gravity_scale |
| Area2D | Overlap detection | body_entered signal |
| CollisionShape2D | Collision definition | shape |
| Camera2D | Game camera | zoom, offset, current |
| TileMapLayer | Tile-based levels | tile_set |
| AudioStreamPlayer | Play audio | stream, play() |
| Label | Display text | text |
| Button | Clickable button | pressed signal |

### Appendix C: Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Ctrl+S | Save scene |
| Ctrl+Shift+S | Save all |
| F5 | Run project |
| F6 | Run current scene |
| F7 | Pause running game |
| Ctrl+D | Duplicate node |
| Delete | Delete node |
| Ctrl+A | Add node |
| Ctrl+Shift+A | Instance scene |

### Appendix D: Vocabulary Glossary

| Term | Definition |
|------|------------|
| Node | Basic building block of Godot games |
| Scene | Collection of nodes saved as reusable file |
| Script | GDScript code attached to a node |
| Signal | Event system for communication between nodes |
| Instance | Copy of a scene created at runtime |
| Delta | Time elapsed since previous frame |
| Autoload | Singleton script accessible globally |
| Export | Variable editable in Inspector |

---

## Document Information

| Field | Value |
|-------|-------|
| **Curriculum Version** | 1.0 |
| **Created** | February 2026 |
| **Target Standard** | Cambridge Lower Secondary Computing (0860) |
| **Game Engine** | Godot Engine 4.x |
| **Programming Language** | GDScript |
| **Review Date** | August 2026 |

---

## Sources and References

- [Godot Engine Official Website](https://godotengine.org/)
- [Godot Engine Features](https://godotengine.org/features/)
- [Godot Documentation](https://docs.godotengine.org/)
- [GDScript Reference](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_basics.html)
- [Godot Education Page](https://godotengine.org/education/)
- [GDQuest Learning Platform](https://www.gdquest.com/)
- [GDQuest - Nodes, Scenes, and Signals](https://school.gdquest.com/courses/learn_2d_gamedev_godot_4/to_space_and_beyond/scenes_nodes_scripts_and_signals)
- [KidsCanCode - Godot in the Classroom](https://kidscancode.org/blog/2017/11/godot_classroom_1/)
- [KidsCanCode - Node Communication](https://kidscancode.org/godot_recipes/4.x/basics/node_communication/index.html)
- [Godot Tutorials](https://godottutorials.com/)
- [Zenva Academy Godot Courses](https://academy.zenva.com/product-category/all/game-development/godot/)
- [Cambridge IGCSE Computer Science (0478)](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-igcse-computer-science-0478/)
- [Cambridge Lower Secondary Computing (0860)](https://www.cambridgeinternational.org/programmes-and-qualifications/cambridge-lower-secondary/curriculum/computing/)
