# Engine Mode: Logic Modification System

## Overview

**Engine Mode** is the core meta-narrative mechanic of `project_name`. It represents a specialized interface that allows the player to bypass the "broken" nature of the game world by directly modifying its internal logic.

In this mode, the player transitions from a controlled entity to a pseudo-developer, injecting movement, interaction, and physics parameters into the environment to overcome obstacles that are otherwise impossible to clear.

---

# Core Workflow

To resolve a level obstacle using the Engine Mode, follow these steps:

1. **Initiation**
   Press `E` to overlay the Editor UI. Interaction with the physical world is suspended while the editor is active.

2. **Selection**
   Browse the **Mechanic Library** to find a suitable logic block (e.g., `Movement`).

3. **Injection**
   Drag the chosen mechanic into an available **Execution Slot**.

4. **Configuration**
   Open the **Property Editor** for the placed mechanic to fine-tune parameters (e.g., adjusting `Speed` or `Direction`).

5. **Validation**
   The system automatically checks if the configuration is functional.

6. **Execution**
   Press `E` or `ESC` to return to the game world. The environment will immediately react to the new logic parameters.

---

# User Interface Layout

The Engine Mode interface consists of three primary functional zones:

## 1. Mechanic Library Panel

A repository of available logic modules discovered or "recovered" during the narrative. These are represented as icons that can be dragged into the workspace.

## 2. Execution Slot Panel

The "active memory" of the current game scene. Slots define when and how a mechanic is executed.

### Slot Types

* **PerFrame Slots**
  Mechanics placed here run every frame (useful for constant movement).

* **Event-Based Slots**
  Reserved for specific trigger-based logic.

## 3. Mechanic Property Editor

A contextual menu that appears when a mechanic is selected within a slot. It allows for precise control over the logic.

### Supported Controls

* **Sliders**
  For continuous values like `Speed` (`0 - 10`).

* **Enums**
  For categorical choices like `Direction` (`Left / Right`).

---

# Technical Specifications & Validation

The system is designed to be robust; incorrect configurations will not "crash" the game but will fail to produce the desired physical result.

| Feature           | Description                                                                            | Feedback Type         |
| ----------------- | -------------------------------------------------------------------------------------- | --------------------- |
| Snap Effect       | Visual confirmation when a mechanic is correctly aligned with a slot.                  | Visual / SFX          |
| Invalid Placement | Occurs if a mechanic type is incompatible with a slot type.                            | Shake Animation / SFX |
| Logic Validation  | Warnings appear if parameters are set to values that don't resolve the current puzzle. | UI Text Message       |

---

# Parameter Example: Movement Mechanic

* **Speed (`v`)**: Range `0.0` to `10.0`
* **Direction**: Boolean / Enum (`Left` / `Right`)
* **Requirement**: Must be placed in a `PerFrame` execution slot to function.

---

# Control Mapping

| Action                 | Input                                    |
| ---------------------- | ---------------------------------------- |
| Toggle Engine Mode     | `E` / `ESC`                              |
| Select / Pick Mechanic | Left Mouse Button                        |
| Place / Drop Mechanic  | Release Left Mouse Button                |
| Adjust Parameters      | Mouse Drag (Sliders) / Keyboard (Values) |
| Remove Mechanic        | Right Mouse Button                       |

---

# Narrative Integration

## Dialogue Hints

NPCs (other trapped students) may provide hints regarding the specific parameters (`v`, `x`, `y`) needed to bypass "glitched" areas.

## Evolution

As the story progresses, the player may unlock more complex slots or find "corrupted" mechanics that require careful calibration to use safely.
