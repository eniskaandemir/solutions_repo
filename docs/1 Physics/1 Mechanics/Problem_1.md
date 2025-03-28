# Problem 1
# Problem 1: Investigating the Range as a Function of the Angle of Projection

## 🎯 Motivation
Projectile motion offers a rich playground for exploring fundamental principles of physics. The horizontal range of a projectile depends on various parameters including initial velocity, launch angle, and gravitational acceleration.

## 🧠 Theoretical Foundation

The horizontal range \( R \) for a projectile launched from ground level is given by:

\[
R = \frac{v_0^2 \sin(2\theta)}{g}
\]

Where:
- \( v_0 \) is the initial velocity
- \( \theta \) is the launch angle
- \( g \) is the gravitational acceleration

Let’s derive this from basic motion equations.

## 🔢 Python Simulation
```python
import numpy as np
import matplotlib.pyplot as plt

v0 = 20  # Initial velocity (m/s)
g = 9.81  # Acceleration due to gravity (m/s^2)

angles = np.linspace(0, 90, 100)
ranges = (v0**2 * np.sin(2 * np.radians(angles))) / g

plt.figure(figsize=(8, 5))
plt.plot(angles, ranges)
plt.title("Range vs. Angle of Projection")
plt.xlabel("Angle (degrees)")
plt.ylabel("Range (meters)")
plt.grid(True)
plt.show()

