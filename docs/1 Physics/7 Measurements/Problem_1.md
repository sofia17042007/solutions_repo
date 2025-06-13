# Problem 1
# 🪀 Physics Experiment

## Problem 1: Measuring Earth's Gravitational Acceleration with a Pendulum

---

## 🎯 Motivation

The acceleration due to gravity, denoted **g**, is a key constant in physics. This experiment uses a simple pendulum to measure **g** and emphasizes:
- Accurate measurement techniques
- Uncertainty analysis
- Comparison with the standard value:  
  $$
  g_{\text{standard}} = 9.806 \, \text{m/s}^2
  $$

---

## 🧪 Materials

- String (length: ~1–1.5 m)
- Small weight (e.g., metal washer, keychain)
- Stopwatch or smartphone
- Measuring tape or ruler

---

## 🔧 Setup

- Attach the weight to the string and suspend from a fixed point.
- Measure pendulum length from the pivot to the **center of mass** of the weight:
  $$
  L = \text{__} \, \text{m}, \quad \Delta L = \frac{\text{resolution}}{2} = \text{__} \, \text{m}
  $$

---

## 📊 Data Collection

| Trial | Time for 10 Oscillations (T₁₀) [s] |
|-------|----------------------------|
| 1     | __                        |
| 2     | __                        |
| 3     | __                        |
| 4     | __                        |
| 5     | __                        |
| 6     | __                        |
| 7     | __                        |
| 8     | __                        |
| 9     | __                        |
| 10    | __                        |

### 🧮 Calculations:

1. **Mean Time for 10 Oscillations:**
   $$
   \bar{T}_{10} = \frac{\sum T_{10}}{10} = \text{__} \, \{s}
   $$

2. **Standard Deviation (s):**
   $$
   s = \sqrt{\frac{1}{n-1} \sum (T_{10,i} - \bar{T}_{10})^2} =  \text{s}
   $$

3. **Uncertainty in Mean Time (ΔT₁₀):**
   $$
   \Delta \bar{T}_{10} = \frac{s}{\sqrt{n}} =  \text{s}
   $$

4. **Period of Pendulum (T):**
   $$
   T = \frac{\bar{T}_{10}}{10} = \text{__} \, \text{s}, \quad \Delta T = \frac{\Delta \bar{T}_{10}}{10}
   $$

5. **Calculate g:**
   $$
   g = \frac{4\pi^2 L}{T^2} = \text{__} \, \text{m/s}^2
   $$

---

## 📉 Uncertainty Propagation

$$
\frac{\Delta g}{g} = \sqrt{
\left( \frac{\Delta L}{L} \right)^2 +
\left( 2 \cdot \frac{\Delta T}{T} \right)^2
}
\quad \Rightarrow \quad
\Delta g = g \cdot \frac{\Delta g}{g} = \text{__} \, \text{m/s}^2
$$

Final result:
$$
g = \boxed{\text{__} \pm \text{__} \, \text{m/s}^2}
$$

---

## 🧠 Discussion

### 1. Comparison with Standard Value
- Measured vs. expected value:
  $$
  g_{\text{measured}} \quad \text{vs.} \quad g_{\text{standard}} = 9.806 \, \text{m/s}^2
  $$

- Is the standard value within your uncertainty range?

---

### 2. Sources of Uncertainty
- Measurement error in length $$ \Delta L $$
- Human reaction time in timing $$ \Delta T $$
- Assumption of small angle$$ (<15°)$$
- Air resistance and friction

---

### 3. Experimental Limitations
- Difficulty in timing exactly 10 oscillations
- Non-rigid or stretching string
- Assumption of a point mass

---

## 📦 Conclusion

This experiment demonstrates how a simple pendulum can be used to **measure gravitational acceleration** using basic tools and rigorous uncertainty analysis. By comparing the result to the standard value of **9.806 m/s²**, one can assess experimental accuracy and understand the importance of error propagation in physical measurements.

---


