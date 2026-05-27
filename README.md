# Webots Robot Simulation — EN2532

> Autonomous virtual robot for the **EN2532 Robot Design Competition** — line following, wall following, gate navigation, box detection + catching, and colour recognition in [Webots](https://cyberbotics.com/).

[![Webots](https://img.shields.io/badge/Webots-simulator-1976D2?style=flat-square)](https://cyberbotics.com/)
[![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)](https://en.wikipedia.org/wiki/C%2B%2B)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

Built for the **EN2532 Robot Design Competition** at the University of Moratuwa.

---

## Capabilities

- **Line following** — IR sensors track and follow arena floor markings
- **Wall following** — distance sensors maintain a safe gap from boundaries
- **Gate navigation** — detects and interacts with arena gates via a secondary controller
- **Box catching** — robotic arm picks and places boxes detected in the arena
- **Colour detection** — dual cameras (front + bottom) identify markings and coloured boxes

## Simulated hardware

- Distance sensors, IR sensors, encoders, position sensors
- DC motors, robotic arm motors
- Dual cameras (front + bottom)

## Project structure

```
Webots-Robot-Simulation/
├── controllers/
│   ├── Final/                # Main robot controller (C++)
│   │   └── Final.cpp
│   └── gate_controller/      # Secondary controller for gate logic
│       └── gate_controller.cpp
├── worlds/                   # Webots worlds + objects
│   ├── arena.wbt
│   ├── gate.wbo
│   ├── robot.wbo
│   └── *.stl
├── Video/                    # Demonstration videos
└── README.md
```

## Run it

```bash
git clone https://github.com/Anjanamb/Webots-Robot-Simulation.git
cd Webots-Robot-Simulation
```

1. Install the latest [Webots release](https://cyberbotics.com/) (requires a C++ toolchain to compile controllers)
2. Open `worlds/arena.wbt` in Webots
3. Press **Play**; the robot executes the behaviour defined in `controllers/Final/Final.cpp`

### Customising

- Different arenas → open any other `.wbt` in `worlds/`
- Behaviour tuning → edit `controllers/Final/Final.cpp` (line-following thresholds, wall distances, arm logic)
- Gate logic → `controllers/gate_controller/`

## Demo

A sample run lives in [`Video/`](./Video/).

## Authors

- **Anjana Bandara** ([@Anjanamb](https://github.com/Anjanamb))
- **Ayesh Rajakaruna** ([@Ayesh-Rajakaruna](https://github.com/Ayesh-Rajakaruna))

Thanks to the EN2532 organisers and teammates.

## License

[MIT](LICENSE) — see [anjanamb.github.io](https://anjanamb.github.io/) for more projects.
