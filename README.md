
# RhythMania

RhythMania is an FPGA rhythm game built for [`50.002 Computation Structures`](https://natalieagus.github.io/50002/) on the Alchitry Au board.  
It challenges players to match beats accurately using a single large button, with real-time audio/visual feedback and hardware-scored timing precision.

## Overview

- **Tagline:** A beat matching rhythm game
- **Core idea:** Listen to the rhythm call, then reproduce it on beat
- **Platform:** Alchitry Au FPGA
- **Language:** Lucid
- **Environment:** Alchitry Labs

## How The Game Works

1. Press the main button to start.
2. Countdown/metronome LEDs pulse to prepare the player.
3. The system plays rhythm cues (LED + buzzer).
4. After countdown, the player reproduces the rhythm with the button.
5. The FPGA checks timing offset in real time and updates score.
6. Feedback LEDs indicate hit quality:
   - Green: Good
   - Yellow: OK
   - Red: Miss

## Hardware I/O

- **Input**
  - 1x large arcade push button
- **Outputs**
  - 1x main rhythm LED
  - 1x passive buzzer
  - 2x 1-digit 7-segment displays (score)
  - 3x hit feedback LEDs (good/ok/miss)
  - 4x metronome/countdown LEDs

## Architecture

- **Control Unit (FSM):** Handles game states, sequencing, and control signals.
- **Datapath:** Handles timestamp arithmetic, comparisons, score updates, ROM access, and register flow.
- **Timing:** Uses millisecond-scale timing for beat windows and hit classification.

## Documentation And Media

- **Full Report:** [`documentation/2026 50.002 Project Group Report Team 12.pdf`](documentation/2026%2050.002%20Project%20Group%20Report%20Team%2012.pdf)
- **Virtual Showcase (Primary):** [SUTD Design Exhibition - Team 12](https://natalieagus.net/2026/term4-design-exhibition/50002/team12)
- **Virtual Showcase (Fallback):** [`documentation/RhythMania (Virtual Showcase).pdf`](documentation/RhythMania%20%28Virtual%20Showcase%29.pdf)
- **Poster (PDF):** <img width="1587" height="2245" alt="poster-1" src="https://github.com/user-attachments/assets/ea4bf386-eb48-4c28-bf55-a7425b867fe3" />

- **Demo Video (MP4):**
<video src="documentation/video.mp4" width="100%" controls></video>

https://github.com/user-attachments/assets/643e7915-2741-46ff-831d-6c97da0e85ee





If the embedded video does not render in your viewer, open it directly: [Open Demo Video MP4](documentation/video.mp4)

> If the virtual showcase page cannot be viewed, use the files in `documentation/` as the full offline backup.

## Quick Access Links

- [Open Poster PDF](documentation/poster.pdf)
- [Open Demo Video MP4](documentation/video.mp4)
- [Open Virtual Showcase PDF](documentation/RhythMania%20%28Virtual%20Showcase%29.pdf)
- [Open Full Report PDF](documentation/2026%2050.002%20Project%20Group%20Report%20Team%2012.pdf)

## Team And Contributors

- Wei Xian ([WeiXian042901](https://github.com/WeiXian042901))
- Jayden ([Jaydenye-jr](https://github.com/Jaydenye-jr))
- Elroy ([TanYuanXiangElroy](https://github.com/TanYuanXiangElroy))
- Jarrod ([Jaelucard](https://github.com/Jaelucard))
- Wong Kysin Natalie ([bataliee](https://github.com/bataliee))
- Eilees ([eilees-3](https://github.com/eilees-3))
- Salman ([Sslenderman](https://github.com/Sslenderman))

## Repository Structure

- `source/` - Lucid modules (FSM, datapath, ALU, peripherals, top-level)
- `constraint/` - board pin/timing constraints
- `cores/` - generated/managed IP core files
- `build/` - build artifacts
- `documentation/` - report, poster, showcase sheet, and demo video

## Setup

```bash
git clone https://github.com/TanYuanXiangElroy/2026_Grp_12_CompStruct_1D.git
```

Then open `Rhythm Heaven.alp` in Alchitry Labs and build/program from there.
