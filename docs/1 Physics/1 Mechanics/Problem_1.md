# Problem 1

# **Investigating the Range as a Function of the Angle of Projection**  

### Theoretical Foundation:

In projectile motion, the **range** of a projectile is the horizontal distance it travels before hitting the ground. The range depends on several factors, including the **initial velocity (v₀)**, the **angle of projection (\( \theta \))**, and the **acceleration due to gravity (g)**. The study of how range varies with angle helps in optimizing launch conditions for various applications, such as sports, military ballistics, and engineering.

#### **Mathematical Representation**  
The equation for the range (\( R \)) of a projectile launched from the ground with an initial velocity \( v_0 \) at an angle \( \theta \) is given by:

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$



Since the range is determined by both horizontal velocity and time of flight, the product of these values gives the range formula.  

### **Applications**  
- **Sports**: Optimizing throwing angles in javelin, shot put, or basketball.  
- **Engineering**: Designing launch angles for projectiles or water fountains.  
- **Military**: Calculating artillery firing angles for maximum efficiency.  

Would you like a more detailed breakdown of any specific aspect?

```python
import numpy as np
import matplotlib.pyplot as plt

# Constants
g = 9.81  # Acceleration due to gravity (m/s²)
v0 = 20   # Initial velocity (m/s)

# Angles from 0 to 90 degrees
angles = np.linspace(0, 90, 100)  # Generate 100 points between 0 and 90 degrees
theta_rad = np.radians(angles)  # Convert degrees to radians

# Compute range for each angle
ranges = (v0**2 * np.sin(2 * theta_rad)) / g

# Plot the results
plt.figure(figsize=(8, 5))
plt.plot(angles, ranges, label=f'v₀ = {v0} m/s', color='b')
plt.axvline(45, color='r', linestyle='--', label='Max Range at 45°')

# Labels and Title
plt.xlabel('Angle of Projection (°)')
plt.ylabel('Range (m)')
plt.title('Projectile Range vs. Angle of Projection')
plt.legend()
plt.grid()

# Show the plot
plt.show()

```

![alt text](image.png)