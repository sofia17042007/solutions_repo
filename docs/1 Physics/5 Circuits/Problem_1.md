# Problem 1
# 🔌 Circuits

## Problem 1: Equivalent Resistance Using Graph Theory

---

## 🎯 Motivation

Calculating **equivalent resistance** is a foundational concept in circuit analysis. While traditional methods (series/parallel reduction) work well for small circuits, they can become tedious and error-prone for complex networks.

By applying **graph theory**, we can model any circuit as a **weighted graph**:
- **Nodes** → electrical junctions
- **Edges** → resistors (weights = resistance values)

This method:
- Enables **automated analysis** and simplification
- Provides deeper understanding of circuit structure
- Is suitable for integration in simulation tools and optimizers

---

## ✅ Task Options

### 🧩 OPTION 1: Simplified Task – Algorithm Description

- Describe how to compute equivalent resistance using graph theory
- Provide **pseudocode**:
    - Identify series and parallel patterns
    - Iteratively reduce the circuit
    - Handle **nested combinations** of resistors

---

### 💻 OPTION 2: Advanced Task – Full Implementation

- Implement the full algorithm in a language like **Python**
- Use graph libraries like `networkx` for circuit representation
- Ensure that your program:
    - Accepts **circuit graphs**
    - Handles **arbitrary resistor networks**
    - Produces the **total equivalent resistance**
- Include test cases:
    - Series and parallel
    - Nested configurations
    - Complex circuits with cycles

---

## 🧠 Algorithm Outline

```plaintext
function calculate_equivalent_resistance(graph, source, target):
    while graph has more than 2 nodes:
        for each node n in graph:
            if n is neither source nor target:
                if n has exactly 2 neighbors:
                    perform series reduction
                elif node is part of a simple cycle:
                    perform parallel reduction
    return resistance between source and target
