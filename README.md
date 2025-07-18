# 🚗 Adaptive Cruise Control (ACC) Observer Evaluation – Thesis Overview

> ⚠️ **Disclaimer:** This repository summarizes my academic thesis work.  
> No proprietary code, internal documentation, or confidential data from Continental AG or the University of Koblenz is included.

---

## 📌 Objective

The goal of this thesis was to evaluate the performance of Adaptive Cruise Control (ACC) systems using mathematical observers. These observers detect the behavior of the ego vehicle in Cut-In and Cut-Out scenarios and calculate a maneuver score based on multiple performance criteria.

---

## 🧠 Core Concept

- Developed **observers** to detect vehicle behavior in complex highway scenarios.
- Evaluated ACC reaction quality in terms of **time gap**, **acceleration**, and **velocity**.
- Created a **scoring function** to quantify maneuver performance using weighted error metrics.
- Enabled a reproducible evaluation framework within the Cruise Validation System.

---

## 🧮 Scoring Model (From Thesis)

The scoring system is calculated as:

\[
S = \omega_1 \cdot |TG_{\text{measured}} - TG_{\text{reference}}| + \omega_2 \cdot |v_{\text{measured}} - v_{\text{reference}}| + \omega_3 \cdot \text{Jerk}_{\text{max}}
\]

Where:
- \( TG \): Time Gap between ego and lead vehicle
- \( v \): Ego vehicle velocity
- \( \text{Jerk}_{\text{max}} \): Maximum longitudinal jerk during the maneuver
- \( \omega_1, \omega_2, \omega_3 \): Weight factors assigned to each metric

This score represents deviation from optimal behavior — **lower is better**.

---

## 📈 Observer Metrics

1. **Time Gap Error**  
   \[
   E_{TG} = |TG_{\text{measured}} - TG_{\text{reference}}|
   \]

2. **Velocity Error**  
   \[
   E_{v} = |v_{\text{measured}} - v_{\text{reference}}|
   \]

3. **Maximum Jerk**  
   \[
   J_{\text{max}} = \max \left( \frac{da(t)}{dt} \right)
   \]

---

## 🛠 Tools Used

- **Python** – signal processing, observer logic, metrics calculation
- **MTS (Measurement & Testing System)** – logging and simulation data
- **Power BI** – KPI dashboards for visualization
- **Excel** – manual review and intermediate scoring checks

---

## 🎯 Outcome

- Developed and implemented a **generic scoring system** to evaluate ACC response quality.
- Provided engineers with **quantitative feedback** for tuning longitudinal control.
- Integrated observer logic into an existing validation pipeline for future scalability.

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

> This repository is meant to present methodology and high-level insights from my thesis under NDA-safe conditions. Please contact me for further discussion.


