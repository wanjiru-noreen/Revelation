# Epiphony: Survive the Four Seals

> *Knowledge is your greatest weapon. Every answer raises a new question.*

A psychological survival horror game where players endure the collapse of the world through four escalating Seals. Explore abandoned locations, survive earthquakes, evade mutated creatures, and uncover unsettling mysteries while reality slowly unravels around you.

---

## Table of Contents

- [Overview](#overview)
- [Game Vision](#game-vision)
- [Gameplay](#gameplay)
- [The Four Seals](#the-four-seals)
- [Player Systems](#player-systems)
- [Psychological Systems](#psychological-systems)
- [Enemy Design](#enemy-design)
- [World & Locations](#world--locations)
- [Visual Style](#visual-style)
- [Audio Design](#audio-design)
- [Project Structure](#project-structure)
- [Development Roadmap](#development-roadmap)
- [Tech Stack](#tech-stack)

---

## Overview

| | |
|---|---|
| **Genre** | Psychological Horror · Survival · Exploration |
| **Engine** | Godot 4.x |
| **Language** | GDScript |
| **Platform** | PC — Windows & Linux |
| **Perspective** | Top-down |
| **Status** | Pre-production |

---

## Game Vision

EPIPHONY is built on three pillars:

- **Fear over combat** — the player never becomes a superhero. Surviving means avoiding, not defeating.
- **Knowledge as progression** — understanding the world's rules is the real advancement.
- **Psychological instability** — the player should stop trusting their senses.

The world decays across four Seals. Each one introduces new threats, new environmental horror, and a visual palette that reflects the unraveling of reality.

---

## Gameplay

The core loop:

```
Explore → Search buildings → Find resources → Avoid threats → Survive events → Reach shelter → Advance Seal
```

The game rewards players who observe carefully, remember what they've learned across runs, and resist the urge to trust everything they see or hear.

---

## The Four Seals

### Seal I — Conquest
*Color palette: gray, faded green, light fog*

The world feels almost normal. Almost. People are missing. Sounds come from empty rooms. Warnings are found scrawled on walls — some true, some not. The horror here is psychological: the player begins to question reality before anything explicitly dangerous appears.

### Seal II — War
*Color palette: dark orange, smoke, dust*

Infrastructure collapses. Roads crack open. Emergency broadcasts conflict with one another — shelter here, avoid that zone, trust no one. The horror is distrust: of the environment, of information, of other survivors.

### Seal III — Wild Beasts
*Color palette: deep blue, black forests, heavy shadows*

Mutated animals have emerged. They track sound, hunt at night, and move unpredictably. The horror is being hunted — the shift from observer to prey.

### Seal IV — Judgement
*Color palette: pale white, black skies, distorted environments*

Reality itself has stopped cooperating. Structures appear where none existed. Earthquakes reshape the map. The horror is cosmic dread: the sense that no rule can be trusted anymore.

---

## Player Systems

### Health
Affected by injuries, creature attacks, earthquakes, and starvation. The player must eat regularly.

### Stamina
Running drains stamina — there is no infinite sprint. Pacing and route planning matter.

### Inventory
Limited slots. Every item is a decision. Nothing is filler.

### Flashlight
Battery-powered. Darkness becomes a resource management problem, not just an atmosphere choice.

### Corruption Meter
Tracks how deeply the player has been affected by the apocalypse. Reaching **666** ends the run. Certain actions raise it — including ones the player may not initially recognize as dangerous.

---

## Psychological Systems

### Dynamic notes
Handwritten warnings are scattered across the world:

> *DON'T ENTER THE CHURCH*

Some are true. Some are false. The ratio is never stated. Players learn — or don't.

### Radio system
Broadcasts cycle through emergency alerts, contradictory instructions, and voices that shouldn't be transmitting anything. Distinguishing signal from noise is part of the game.

### Memory system
Rarely, the game references previous deaths. No explanation is given. The implication is left to the player.

---

## Enemy Design

### The Watcher
Appears infrequently. Never attacks. Simply observes. Its purpose is never explained.

### Mutated Human
Fast, aggressive, and unpredictable. Close-range threat with no readable pattern.

### Mutated Animal
Tracks sound. Hunts at night. Requires patience and silence to avoid.

---

## World & Locations

Each run changes details. Locations include:

- Town
- Church
- School
- Forest
- Gas station
- Farm
- Abandoned homes
- Shelter bunkers

Some exits are fake. Some warnings are true. Some safe-looking buildings are not.

---

## Visual Style

**Low-poly + stylized realism.** The aesthetic draws from:

- *Darkwood* — oppressive atmosphere, top-down dread
- *The Long Dark* — isolation, sparse environments
- *Silent Hill 2* — psychological distortion, meaningful decay

Horror often works better when details are hidden. The visual style is chosen to serve that principle, not to compensate for it.

---

## Audio Design

Audio is where the horror lives.

**Ambient:** wind, distant screams, rustling trees, footsteps, radio static, creaking wood.

**Psychological:** knocking, whispering, breathing, the player's name being called.

Some sounds are real. Some are not. Players should stop trusting their ears.

**Music:** minimal. Drones, low frequencies, isolated piano notes, and silence. Silence is used deliberately — it signals safety less than it signals anticipation.

---

## Project Structure

```
REVELATION/
│
├── scenes/
│   ├── Main.tscn
│   ├── Seal1.tscn — Seal4.tscn
│   ├── player/
│   ├── enemies/
│   ├── world/
│   └── ui/
│
├── scripts/
│   ├── GameManager.gd       # Autoload singleton
│   ├── Player.gd
│   ├── Corruption.gd
│   ├── SealBase.gd
│   ├── Seal1.gd — Seal4.gd
│   └── systems/
│       ├── Medals.gd
│       ├── Insight.gd
│       └── Events.gd
│
├── assets/
│   ├── audio/
│   ├── sprites/
│   └── fonts/
│
├── data/
│   ├── notes/
│   ├── events/
│   └── lore/
│
└── saves/
```

---

## Development Roadmap

### Month 1 — Prototype
- [ ] Player movement
- [ ] Inventory system
- [ ] Flashlight mechanic
- [ ] One map, one building

### Month 2 — Alpha
- [ ] Save system
- [ ] Hunger mechanic
- [ ] Stamina system
- [ ] Dynamic notes
- [ ] Radio system

### Month 3 — Beta
- [ ] Earthquakes
- [ ] Mutant enemies
- [ ] Enemy AI
- [ ] Full sound system

### Release Candidate
- [ ] All four Seals
- [ ] Lore integration
- [ ] Multiple endings
- [ ] Polish pass

---

## Tech Stack

| Component | Choice | Notes |
|---|---|---|
| Engine | Godot 4.x | Primary development environment |
| Language | GDScript | All gameplay, UI, AI, and events |
| Platform | PC (Windows + Linux) | Mobile deferred intentionally |
| Optional | C# | Only if performance requires it — later |

---
