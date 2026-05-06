# RhythMania 🎵

**RhythMania** is a custom hardware-based rhythm game engineered on the Alchitry FPGA. Designed as a major 1D hardware project at SUTD, it features a fully custom-built datapath and Finite State Machine (FSM) to handle game logic, input processing, and audio-visual synchronization.

---

## 🕹️ Features
* **Custom Game Logic:** Driven by a bespoke Finite State Machine (FSM) tailored for precise rhythm tracking.
* **Hardware Datapath:** Optimized custom datapath built specifically for high-speed score calculation and input validation.
* **Low-Latency Input:** Direct hardware polling ensures inputs are registered with zero software bloat.


---

## 🛠️ Tech Stack & Hardware
* **Board:** Alchitry FPGA Au
* **Language:** Lucid (Hardware Description Language)
* **Environment:** Alchitry Labs
* **Peripherals:** Arcade buttons, 2 7-Segments (wired directly), 3 Feedback LEDs, 4 Metronome LEDs, 1 Rhythm LED

---

## 🏗️ Architecture Overview
The core of RhythMania is split into two primary hardware components:

1. **The Datapath:** Handles all the mathematical operations, such askeeping track of the score, comparing the player's input timing against the expected beat, and managing scoring system.
2. **The Control Unit (FSM):** Manages the state of the game (e.g., `START_SCREEN`, `PLAYING`, `GAME_OVER`), controls the flow of data through the datapath, and triggers visual/audio outputs based on the current state and player performance.

---

## 🚀 Setup & Installation
1. Clone this repository to your local machine:
   ```bash
   git clone [https://github.com/Jaydenye-jr/2026_Grp_12_CompStruct_1D.git](https://github.com/Jaydenye-jr/2026_Grp_12_CompStruct_1D.git)
