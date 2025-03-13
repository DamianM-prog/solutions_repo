# Problem 1

## Discuss the problem of projectile motion. Investigate the dependence of the range on the angle of projection.

## Projectile Motion

Projectile motion refers to the motion of an object that is launched into the air and is influenced only by the force of gravity after its initial launch. The path followed by a projectile is a curved trajectory, typically a parabola, and is determined by its initial velocity, launch angle, and the acceleration due to gravity. Understanding the dynamics of projectile motion involves analyzing key components: the horizontal motion, the vertical motion, and the angle of projection.



## Key Concepts in Projectile Motion

1. **Initial Velocity ($v_0$)**: The speed at which the projectile is launched.
2. **Angle of Projection ($\theta$)**: The angle at which the projectile is launched relative to the horizontal.
3. **Acceleration due to Gravity ($g$)**: The constant acceleration acting downward, approximately $9.81 \, \text{m/s}^2$ near the surface of the Earth.

## Equations of Motion

The motion can be separated into its horizontal ($x$) and vertical ($y$) components. 

- **Horizontal Motion**: 
  - The horizontal component of the initial velocity is given by:
    $$
    v_{0x} = v_0 \cos(\theta)
    $$
  - Since there is no acceleration in the horizontal direction (ignoring air resistance), the horizontal distance (range) covered during the time of flight ($T$) can be expressed as:
    $$
    R = v_{0x} \cdot T = (v_0 \cos(\theta)) \cdot T
    $$

- **Vertical Motion**: 
  - The vertical component of the initial velocity is:
    $$
    v_{0y} = v_0 \sin(\theta)
    $$
  - The vertical motion is influenced by gravity, and can be described using the kinematic equation:
    $$
    y = v_{0y} \cdot t - \frac{1}{2} g t^2
    $$
  - The time of flight ($T$) until the projectile returns to the original level ($y = 0$) can be calculated from the vertical motion equations. Solving yields:
    $$
    T = \frac{2 v_{0y}}{g} = \frac{2 v_0 \sin(\theta)}{g}
    $$

## Dependence of the Range on the Angle of Projection

Substituting $T$ back into the range equation gives us:
$$
R = (v_0 \cos(\theta)) \cdot \left(\frac{2 v_0 \sin(\theta)}{g}\right)
$$
$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$

From this equation, we see that the range ($R$) is dependent on the initial velocity $v_0$ and the sine of $2\theta$.

### Behavior of Range with Varying Projection Angles

1. **Angle of Projection**: The value of $\sin(2\theta)$ varies with $\theta$ ranging from 0 to 90 degrees:
   - $\sin(2\theta)$ is 0 when $\theta = 0^\circ$ (no range) and when $\theta = 90^\circ$ (again, no horizontal range).
   - The value of $\sin(2\theta)$ reaches its maximum when $\theta = 45^\circ$, yielding a maximum range.

2. **Optimal Angle**: The optimal angle for maximum range in a vacuum (ignoring air resistance) is 45°. This is the angle where the horizontal and vertical components of the projectile’s motion create the longest distance due to the highest combination of height and distance traveled horizontally.

3. **Range at Other Angles**: The range decreases as the angle moves away from 45°, either toward 0° (where the projectile travels straight and falls almost immediately) or toward 90° (where it goes straight up and comes straight down).

## Conclusion

In summary, projectile motion is affected by the angle of projection, with a specific relationship that defines how far a projectile will travel. The maximum horizontal range is achieved at a projection angle of 45 degrees. Understanding these principles is crucial in fields ranging from sports science to engineering and military applications.

### Projectile Motion Chart Code

To visualize the trajectory of a projectile for different angles of projection, you can use the following Python code. This code utilizes `matplotlib` and `numpy` to plot the projectile motion paths.

```python
import numpy as np
import matplotlib.pyplot as plt

# Constants
g = 9.81  # Acceleration due to gravity (m/s^2)
v0 = 50   # Initial velocity (m/s)

# Angles of projection in degrees
angles = [15, 30, 45, 60, 75]

# Create a figure
plt.figure(figsize=(10, 6))

# Calculate and plot the trajectory for each angle
for angle in angles:
    # Convert angle to radians
    theta = np.radians(angle)
    
    # Time of flight
    T = (2 * v0 * np.sin(theta)) / g
    
    # Time intervals
    t = np.linspace(0, T, num=500)
    
    # Equations of motion
    x = v0 * np.cos(theta) * t               # Horizontal distance
    y = v0 * np.sin(theta) * t - 0.5 * g * t**2  # Vertical distance
    
    # Plotting
    plt.plot(x, y, label=f'Angle: {angle}°')

# Set up the plot limits and labels
plt.title('Projectile Motion Trajectories for Different Angles')
plt.xlabel('Horizontal Distance (m)')
plt.ylabel('Vertical Distance (m)')
plt.axhline(0, color='black', lw=0.5, ls='--')  # Ground line
plt.axvline(0, color='black', lw=0.5, ls='--')  # Initial launch line
plt.grid()
plt.legend()
plt.xlim(0, 300)  # Adjust based on expected range
plt.ylim(0, 50)   # Adjust based on expected max height

# Show the plot
plt.show()
```

![alt text](chart.png)
