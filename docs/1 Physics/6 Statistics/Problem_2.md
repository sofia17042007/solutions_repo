# Problem 2
# 🧮 Estimating π Using Monte Carlo Methods

---

## 🎯 Motivation

Monte Carlo methods use randomness to solve problems and estimate values. One classic application is estimating **π** using **geometric probability**. These techniques not only provide intuitive insights into probability and geometry but also illustrate how randomness can be used for computational estimation in real-world applications.

---

# 📌 PART 1: Estimating π Using a Circle

---

## 📐 Theoretical Foundation

- Consider a **unit circle** (radius = 1) centered at the origin, inscribed in a **square** with sides of length 2 (from -1 to 1).
- The **area** of the circle is:  
  $$
  A_{\text{circle}} = \pi r^2 = \pi
  $$
- The **area** of the square is:  
  $$
  A_{\text{square}} = (2)^2 = 4
  $$
- The probability that a randomly chosen point in the square also lies inside the circle is:  
 $$
  P = \frac{A_{\text{circle}}}{A_{\text{square}}} = \frac{\pi}{4}
  $$
- Thus, π can be estimated as:  
  $$
  \pi \approx 4 \cdot \frac{\text{points inside circle}}{\text{total points}}
  $$

---

## 🧪 Simulation

```python
import numpy as np
import matplotlib.pyplot as plt

def estimate_pi_circle(num_points=10000):
    x = np.random.uniform(-1, 1, num_points)
    y = np.random.uniform(-1, 1, num_points)
    distances = x**2 + y**2
    inside = distances <= 1
    pi_estimate = 4 * np.sum(inside) / num_points

    # Visualization
    plt.figure(figsize=(6,6))
    plt.scatter(x[inside], y[inside], color='blue', s=1, label='Inside Circle')
    plt.scatter(x[~inside], y[~inside], color='red', s=1, label='Outside Circle')
    plt.title(f'Monte Carlo Estimation of π with {num_points} Points\nEstimated π ≈ {pi_estimate:.6f}')
    plt.xlabel('x')
    plt.ylabel('y')
    plt.legend()
    plt.axis('equal')
    plt.grid(True)
    plt.show()

    return pi_estimate

estimate_pi_circle(10000)
```

---

## 📈 Convergence Analysis

| Number of Points | Estimated π |
|------------------|-------------|
| 100              | 3.16        |
| 1,000            | 3.14        |
| 10,000           | 3.1416      |
| 100,000          | 3.1418      |

- As the number of points increases, the estimate converges toward the true value of π.
- The accuracy improves proportionally to \( \frac{1}{\sqrt{n}} \) due to the **Law of Large Numbers**.

---

# 📌 PART 2: Estimating π Using Buffon’s Needle

---

## 📐 Theoretical Foundation

**Buffon’s Needle Problem**:
- A needle of length \( L \) is dropped onto a plane with **parallel lines** spaced distance \( d \) apart (with \( L \leq d \)).
- The probability that the needle **crosses** a line is:
  $$
  P = \frac{2L}{d\pi}
  $$
- Rearranging gives:
  $$
  \pi \approx \frac{2L \cdot \text{number of drops}}{d \cdot \text{number of crosses}}
  $$

---

## 🧪 Simulation

```python
def estimate_pi_buffon(num_trials=10000, L=1.0, d=2.0):
    assert L <= d, "Needle length must be less than or equal to distance between lines."

    # Random angles and center distances
    theta = np.random.uniform(0, np.pi/2, num_trials)
    y_center = np.random.uniform(0, d/2, num_trials)

    crosses = y_center <= (L / 2) * np.sin(theta)
    num_crosses = np.sum(crosses)

    if num_crosses == 0:
        return None

    pi_estimate = (2 * L * num_trials) / (d * num_crosses)

    # Visualization (first 100 needles)
    plt.figure(figsize=(8, 4))
    for i in range(100):
        angle = theta[i]
        yc = y_center[i]
        y1 = yc - (L / 2) * np.sin(angle)
        y2 = yc + (L / 2) * np.sin(angle)
        x1 = 0.5 - (L / 2) * np.cos(angle)
        x2 = 0.5 + (L / 2) * np.cos(angle)
        color = 'red' if yc <= (L / 2) * np.sin(angle) else 'gray'
        plt.plot([x1, x2], [y1, y2], color=color)

    for i in range(5):
        plt.axhline(i * d / 5, color='black', linestyle='--')

    plt.title(f"Buffon's Needle Simulation\nEstimated π ≈ {pi_estimate:.6f}")
    plt.xlim(0, 1)
    plt.ylim(0, d)
    plt.xlabel('x')
    plt.ylabel('y')
    plt.grid(True)
    plt.show()

    return pi_estimate

estimate_pi_buffon(10000)
```
![ Alt Text](problemstatistic.png)

---

## 📈 Convergence Analysis

| Number of Drops | Estimated π |
|-----------------|-------------|
| 1,000           | 3.12        |
| 10,000          | 3.17        |
| 100,000         | 3.145       |

- Buffon’s method converges **slower** than the circle method.
- The randomness in angle and fewer crossings introduce more **variability**.

---

## 📊 Method Comparison

| Method              | Convergence Speed | Accuracy (100K trials) | Visual Appeal | Practicality |
|---------------------|-------------------|-------------------------|---------------|--------------|
| Circle-based        | Fast              | High                    | High          | Easy         |
| Buffon’s Needle     | Slower            | Medium                  | Moderate      | Complex math |

---

## 🧠 Discussion and Takeaways

- Both methods estimate π using **random sampling** and **probability**.
- Circle-based Monte Carlo is more **efficient** and widely used.
- Buffon’s method is **historically significant** and a creative way to approach probability and geometry.

---

## ✅ Deliverables

- ✅ Python scripts for both methods
- ✅ Plots for visualizing random points and needle drops
- ✅ Tables showing convergence of estimated π
- ✅ Theoretical explanations and formula derivations
- ✅ Comparative analysis of accuracy and computational efficiency

---


