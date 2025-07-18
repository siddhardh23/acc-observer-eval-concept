# 🚗 Adaptive Cruise Control (ACC) Observer Evaluation – Conceptual Thesis Overview

> ⚠️ **Disclaimer:** This repository contains a **summary of my academic thesis**.  
> No proprietary code, data, or internal tooling from Continental AG or the University of Koblenz is included.

---

## 📌 Objective

Develop a framework to assess and enhance Adaptive Cruise Control (ACC) behavior in automatic driving systems — with a focus on **'CutIn'** and **'CutOut'** traffic maneuvers. The project aims to bridge the gap between theoretical control logic and real-world safety/comfort metrics.

---

## 🧠 Core Concept

The thesis introduces:
- **Mathematical observers** to evaluate ego vehicle response in dynamic traffic scenarios
- A **custom scoring algorithm** benchmarking system performance against human driving standards
- Integration into a Cruise Validation Framework for system-level testing

---

## 🛠 Key Tasks

- Modeled and simulated ego vehicle response during critical maneuvers
- Quantified performance using metrics like:
  - Reaction time
  - Relative velocity
  - Acceleration profiles
  - Time-to-collision (TTC)
- Compared system behavior to optimal driving profiles
- Identified areas of improvement in the controller logic

---

## 📈 Observers and Evaluation Metrics

### Reaction and Behavior Metrics:
```text
• Relative Velocity: v_rel = v_ego - v_lead
• Time-To-Collision (TTC) = d_rel / v_rel
• Acceleration Profile: a(t) over maneuver window
