# 🧪 Problem 1: Measuring Earth's Gravitational Acceleration with a Pendulum

## 🔍 Motivation

The acceleration due to gravity $ g $ is a fundamental physical constant influencing countless phenomena. A simple and effective method to measure it involves analyzing the oscillations of a pendulum, where the period of oscillation is related to the gravitational field.

---

## 🎯 Task

- Measure $ g $ using a pendulum.
- Analyze uncertainties in all measurements.
- Emphasize experimental accuracy and proper error analysis.

---

## 🛠️ Materials

- String (~1.00 m)
- Small weight (e.g., keychain, coins)
- Stopwatch or smartphone timer (resolution = 0.01 s)
- Measuring tape or ruler (resolution = 0.01 m)

---

## 🔧 Setup

- Length of pendulum:  
  $ L = 1.00 \, \text{m} $  
  Uncertainty:  
  $ \Delta L = \frac{0.01}{2} = 0.005 \, \text{m} $

- Displacement angle: less than 15° to satisfy small-angle approximation.

---

## 📋 Data Collection

Measured time for **10 oscillations**, repeated 10 times:

| Trial | Time for 10 Oscillations $ t_i $ [s] |
|-------|--------------------------------------|
| 1     | 20.13                                |
| 2     | 20.08                                |
| 3     | 20.15                                |
| 4     | 20.09                                |
| 5     | 20.11                                |
| 6     | 20.10                                |
| 7     | 20.14                                |
| 8     | 20.12                                |
| 9     | 20.07                                |
| 10    | 20.13                                |

- Mean time for 10 oscillations:  
  $ \bar{t} = 20.112 \, \text{s} $

- Standard deviation:  
  $ \sigma_t = 0.025 \, \text{s} $

- Uncertainty in mean time:  
  $ \Delta \bar{t} = \frac{\sigma_t}{\sqrt{n}} = \frac{0.025}{\sqrt{10}} = 0.0079 \, \text{s} $

---

## 🧮 Calculations

### 1. Period of one oscillation

$$
T = \frac{\bar{t}}{10} = \frac{20.112}{10} = 2.0112 \, \text{s}
$$
$$
\Delta T = \frac{\Delta \bar{t}}{10} = \frac{0.0079}{10} = 0.00079 \, \text{s}
$$

---

### 2. Gravitational acceleration \( g \)

$$
g = \frac{4\pi^2 L}{T^2} = \frac{4\pi^2 \cdot 1.00}{(2.0112)^2} = 9.78 \, \text{m/s}^2
$$

---

### 3. Uncertainty in \( g \)

$$
\frac{\Delta g}{g} = \sqrt{ \left( \frac{\Delta L}{L} \right)^2 + \left( 2 \cdot \frac{\Delta T}{T} \right)^2 }
= \sqrt{ \left( \frac{0.005}{1.00} \right)^2 + \left( 2 \cdot \frac{0.00079}{2.0112} \right)^2 } = 0.0051
$$
$$
\Delta g = 0.0051 \cdot 9.78 = 0.050 \, \text{m/s}^2
$$
$$
\boxed{g = 9.78 \pm 0.05 \, \text{m/s}^2}
$$

---

## 📈 Analysis

### 1. Comparison

- Standard $$ g = 9.81 \, \text{m/s}^2 $$
- Measured $$ g = 9.78 \pm 0.05 \, \text{m/s}^2 $$ 
  → Difference is within uncertainty → ✅ acceptable result

---

### 2. Discussion of Uncertainties

- **Measurement Resolution**:
    - Ruler (±0.005 m) and stopwatch (±0.01 s) directly impact the precision of \( g \).

- **Human Reaction Time**:
    - Affects timing accuracy → using 10 full oscillations reduces this error.

- **Assumptions**:
    - Small-angle approximation is valid under 15°.
    - No energy loss due to air resistance or friction.
    - String is massless and inextensible.

- **Limitations**:
    - Better accuracy possible with more oscillations or automated timing.
    - Mass distribution and pendulum swing symmetry were assumed ideal.

---

## ✅ Final Result

$$
\boxed{g = 9.78 \pm 0.05 \, \text{m/s}^2}
$$

---
