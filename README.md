# 🚗 Adaptive Cruise Control (ACC) Observer Evaluation – Conceptual Thesis Overview

> ⚠️ **Disclaimer:** This repository contains a **conceptual summary** of my academic thesis.  
> It includes no proprietary code, data, or internal tooling from Continental AG or the University of Koblenz.

---

## 📌 Objective

To develop a reusable observer framework that evaluates Adaptive Cruise Control (ACC) behavior in real-time simulation scenarios — specifically focusing on **cut-in** and **cut-out** maneuvers.  
The aim was to monitor and score system performance using measurable safety and comfort indicators.

---

## 🧠 Core Concept

The thesis introduces:

- Observer models that monitor **ego vehicle response** during dynamic traffic situations
- **Behavioral scoring** for performance evaluation (relative velocity, time-to-collision, jerk, etc.)
- A custom scoring algorithm designed to **compare system behavior against human driving standards**
- Automated dashboards to support validation engineers in identifying edge-case issues

---

## 🛠 Tools Used

- 🐍 **Python** – data preprocessing, metric calculation, observer logic
- 🖥 **MTS (Measurement & Testing System)** – time-series extraction & processing
- 📊 **Power BI** – KPI visualization & maneuver scoring dashboards
- 📄 **Excel** – manual analysis, signal inspection, benchmark comparisons

---

## 📈 Observer Metrics and Evaluation Formulas

### Relative Velocity
\[
v_{\text{rel}} = v_{\text{ego}} - v_{\text{lead}}
\]

### Time-To-Collision (TTC)
\[
TTC = \frac{d_{\text{rel}}}{v_{\text{rel}}}
\]

### Acceleration and Jerk
\[
a(t) = \frac{dv(t)}{dt}, \quad j(t) = \frac{da(t)}{dt}
\]

---

## 🧮 Scoring Model

A weighted evaluation score was computed to assess each maneuver:

\[
S = \alpha \cdot E_{\text{TTC}} + \beta \cdot E_{\text{gap}} + \gamma \cdot J_{\text{max}}
\]

Where:
- \( E_{\text{TTC}} \): Time-to-collision error
- \( E_{\text{gap}} \): Deviation from target time gap
- \( J_{\text{max}} \): Peak longitudinal jerk
- \( \alpha, \beta, \gamma \): Tunable weights based on safety/comfort balance

---

## 🎯 Outcome

- ✅ Built a reusable observer system that plugs into validation pipelines
- 📉 Reduced manual analysis time by auto-scoring critical maneuvers
- 🚦 Flagged edge cases where ACC behavior diverged from safe driving norms
- 🔁 Enabled better feedback loops between control algorithm teams and testers

---


---

## 🙋‍♂️ Author

**Siddhardha Naidu Gorja**  
Master’s Thesis – University of Koblenz  
In collaboration with **Continental AG**  
Supervisors: *Dr. Christian Kahle*, *Mr. Armin Stecher*

📫 [siddhardh23@gmail.com](mailto:siddhardh23@gmail.com)  
🔗 [GitHub](https://github.com/siddhardha23g)

---

> This documentation-only repository is designed for professional demonstration of methodology under NDA constraints. No confidential assets are included. Contact me for further technical discussions.

