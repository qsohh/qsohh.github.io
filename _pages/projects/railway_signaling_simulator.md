---
title: "Petit Metro Simulator"
permalink: /projects/railway_signaling_simulator/
layout: single
author_profile: true
---

This project is a simulation prototype of railway signaling systems developed during my final-year internship at ENSTA Paris (2019).  
It simulates train behavior under both traditional fixed-block and CBTC (Communication-Based Train Control) systems, with emphasis on modularity and extensibility.

<img src="/assets/images/projects_railway_signaling_simulator/ex_simulation.png" width="50%">

[GitHub repo](https://github.com/qsohh/PetitMetroHao)

---

## Objectives

- Simulate multi-train operation under different signaling protocols.
- Model core elements: stations, terminus, tracks, junctions, nodes.
- Implement train dynamics: acceleration, braking, coasting, station stop, dwell time.
- Compare fixed-block and CBTC signaling behaviors.
- Visualize results: position-time curves, speed-distance plots, train gaps.

---

## Architecture

```plaintext
railway-signal-simulator/
├── main.py               # Simulation entry point
├── DefClass/             # Core classes: Train, Dummy, Track, Station...
├── InitData/             # Configurable scenario setups
├── PlotTool/             # Data visualization tools (matplotlib)
├── Generator/            # Track/train generator modules
├── Simulator/            # Runtime simulation process
├── tests/                # Test scenarios and edge case checks
├── figs/                 # Generated charts
└── README.md
```

---

## Key Modules

| **Module**                | **Description**                                                                         |
| ------------------------- | --------------------------------------------------------------------------------------- |
| `Train` / `Dummy`         | Implements the train logic and its virtual proxy used for spacing calculations.         |
| `Line` / `Track` / `Node` | Defines the track network topology, including connections, direction, and speed limits. |
| `Station` / `Terminus`    | Models station stops, arrivals/departures, and turnaround behavior.                     |
| `Measure` / `Balise`      | Handles location sensing and feedback mechanisms (e.g., RFID, position markers).        |
| `PlotTool`                | Visualizes outputs: position vs. time, speed vs. distance, train gaps, etc.             |
| `InitData`                | Stores preset simulation configurations (e.g., multi-train scenarios, terminal layout). |

---

## Sample Outputs

<div style="display: flex; flex-direction: column; gap: 10px;">
  <img src="/assets/images/projects_railway_signaling_simulator/2stations_v_d.png" width="70%">
  <p style="margin-top: -5px; font-style: italic;">
    Speed adaptation curve: one train adjusting to multiple speed limits and targets along the track.
  </p>

  <img src="/assets/images/projects_railway_signaling_simulator/many_trains_5000.png" width="150%">
  <p style="margin-top: -5px; font-style: italic;">
    Multi-train operation simulation (7 trains, 2 termini): position vs. time chart showing cyclic dispatching and safe spacing control.
  </p>
</div>

---

## Technical Notes
- Developed in Python, with modular design across simulation, plotting, and train dynamics.
- Project is intended as a prototype — suitable for experimentation, research, and educational use.

---

[Back to Projects](/projects/)