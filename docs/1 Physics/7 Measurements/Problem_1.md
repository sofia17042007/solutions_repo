# 🧪 Measuring Earth's Gravitational Acceleration with a Pendulum


---

## 🎯 Motivation

The acceleration due to gravity $$g$$ is a fundamental physical constant 🌍. A classical and elegant method for determining it is by measuring the period of a simple pendulum. This experiment highlights the importance of accurate measurement and uncertainty analysis 🔍.

---

## 🧰 Materials

- 📏 A string (1–1.5 meters)
- 🏋️‍♂️ A small weight (keychain, bag of sugar, etc.)
- ⏱ A stopwatch or smartphone timer
- 📐 A measuring tape or ruler (with known resolution)

---

## 🔧 Setup

1. Attach the weight to the string and fix the other end to a sturdy support.
2. Measure the **length** of the pendulum from the suspension point to the center of the weight:

   $$
   L = 1.000 \pm 0.005 \, \text{m}
   $$

   (The uncertainty is half the smallest division: 1 cm / 2 = 0.5 cm = 0.005 m)
3. Displace the pendulum less than 15° and release gently.

---

## 📊 Data Collection

Measure the time for 10 complete oscillations — repeat this **10 times**:

| Trial | Time for 10 Oscillations $$t_{10}$$ (s) |
|-------|----------------------------------------:|
| 1     | 20.04                                   |
| 2     | 20.10                                   |
| 3     | 19.96                                   |
| 4     | 20.12                                   |
| 5     | 20.05                                   |
| 6     | 20.01                                   |
| 7     | 20.08                                   |
| 8     | 20.03                                   |
| 9     | 20.09                                   |
| 10    | 20.00                                   |

---

## 🧮 Calculations

### 1. Mean and Period

$$
\bar{t}_{10} = \frac{1}{10} \sum t_{10,i} = 20.048 \, \text{s}
$$

Standard deviation:

$$
\sigma = \sqrt{ \frac{1}{n - 1} \sum (t_{10,i} - \bar{t}_{10})^2 } = 0.049 \, \text{s}
$$

Uncertainty in mean time:

$$
\Delta \bar{t}_{10} = \frac{\sigma}{\sqrt{n}} = \frac{0.049}{\sqrt{10}} = 0.016 \, \text{s}
$$

Period of one oscillation:

$$
T = \frac{\bar{t}_{10}}{10} = 2.0048 \, \text{s}, \quad \Delta T = \frac{\Delta \bar{t}_{10}}{10} = 0.0016 \, \text{s}
$$

---

### 2. Calculating $$g$$

Pendulum formula:

$$
T = 2\pi \sqrt{\frac{L}{g}} \Rightarrow g = \frac{4\pi^2 L}{T^2}
$$

Substitute:

$$
g = \frac{4\pi^2 \cdot 1.000}{(2.0048)^2} = 9.82 \, \text{m/s}^2
$$

---

### 3. Propagating Uncertainty

Relative uncertainty:

$$
\frac{\Delta g}{g} = \sqrt{ \left( \frac{\Delta L}{L} \right)^2 + \left( 2 \cdot \frac{\Delta T}{T} \right)^2 }
$$

Substitute:

$$
\frac{\Delta g}{g} = \sqrt{ \left( \frac{0.005}{1.000} \right)^2 + \left( 2 \cdot \frac{0.0016}{2.0048} \right)^2 } \approx 0.0051
$$

Absolute uncertainty:

$$
\Delta g = 9.82 \cdot 0.0051 \approx 0.05 \, \text{m/s}^2
$$

Final result:

$$
g = 9.82 \pm 0.05 \, \text{m/s}^2
$$

---

## 📈 Results Summary

- Pendulum length: $$L = 1.000 \pm 0.005 \, \text{m}$$
- Period: $$T = 2.0048 \pm 0.0016 \, \text{s}$$
- Gravitational acceleration: $$g = 9.82 \pm 0.05 \, \text{m/s}^2$$

---

## 💬 Analysis & Discussion

- ✅ **Comparison**: Standard gravity is $$g = 9.80665 \, \text{m/s}^2$$. Our value is within 0.1% — a great result!
- 📏 **Measurement resolution**: Limits the precision of length measurements.
- ⏱ **Human reaction time**: Manual timing introduces random error.
- 🎯 **Angle assumption**: The small-angle approximation is valid for <15° — any larger and our formula loses accuracy.
- 🌬️ **Neglected factors**: Air resistance and mass of the string are ignored — could introduce systematic errors.

---

## 🧾 Conclusion

We successfully measured the gravitational acceleration using a simple pendulum!  
This experiment demonstrates how classical physics and careful measurements go hand-in-hand — even with everyday tools 😊.

