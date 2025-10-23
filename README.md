# Shallow Water Simulation (Unity HDRP)

This project implements real-time fluid simulation based on the **Shallow Water Equations (SWE)**.

This project uses Unity **HDRP + Compute Shader** to simulate and render large-scale water effects.

---

## Background

The Shallow Water Equations (SWE) are an approximation of the equations in a two-dimensional height field. By assuming that the water depth is smaller than the horizontal scale, it significantly reduces computational complexity while preserving key phenomena such as wave propagation, reflection, and overflow.

The method proposed in the reference paper is widely used in games and interactive applications, enabling real-time rendering of large areas of sea and lake.

---

## Features

- **Shallow Water Equation (SWE) Based on Height Field**

- **Boundary Conditions and External Forces**


- **Render Integration (HDRP)**

- **Real-time Performance**


- **Not Guaranteed Infinite Stability**

    - Even with the infinitely stable MacCormack fallback semi-Lagrange advection method, unreasonable dx and dt values ​​can still lead to failure to meet CFL conditions, resulting in water surface explosions.

---

## Equations and Code Flow

### Control Equations


$$∂h/∂t + ∇·(h v) = 0$$

$$∂v/∂t = -g ∇η + a_ext$$




![Example](Example.png)