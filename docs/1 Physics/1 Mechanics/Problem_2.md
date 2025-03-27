# Damped Pendulum Analysis

## Introduction
A pendulum is a mass on a pivot, oscillating under gravity. Without damping, it swings indefinitely, but forces like friction introduce **damping**, reducing amplitude over time. This project analyzes damped pendulum dynamics theoretically, with optional simulation or experimental components.

## Theoretical Framework

### Simple Pendulum (Undamped)
The undamped pendulum’s motion is:

$$
\frac{d^2 \theta}{dt^2} + \frac{g}{L} \sin(\theta) = 0
$$

For small θ, sin(θ) ≈ θ, simplifying to:

$$
\frac{d^2 \theta}{dt^2} + \omega_0^2 \theta = 0
$$

#### Symbols and Units
- θ: Angular displacement (radians, rad)  
- t: Time (seconds, s)  
- g: Gravitational acceleration (meters per second squared, m/s²), typically 9.81 m/s²  
- L: Pendulum length (meters, m)  
- ω₀: Natural angular frequency (radians per second, rad/s), where ω₀ = √(g/L)  
- T: Period (seconds, s), where T = 2π √(L/g)

### Damped Pendulum
With damping, the equation becomes:

$$
\frac{d^2 \theta}{dt^2} + b \frac{d \theta}{dt} + \frac{g}{L} \theta = 0
$$

#### Symbols and Units
-  b : Damping coefficient (per second, s⁻¹), representing resistance per unit velocity

The equation describes underdamped, critically damped, or overdamped motion based on $ b $.

## Mathematical Analysis
For:

$$
\theta'' + b \theta' + \omega_0^2 \theta = 0
$$

the characteristic equation is:

$$
r^2 + b r + \omega_0^2 = 0
$$

Roots: $ r = \frac{-b \pm \sqrt{b^2 - 4 \omega_0^2}}{2} $ (units: s⁻¹).

### Solutions
- **Overdamped** ($ b^2 - 4 \omega_0^2 > 0 $):

$$
\theta(t) = A e^{r_1 t} + B e^{r_2 t}
$$

- **Critically damped** ($ b^2 - 4 \omega_0^2 = 0 $):

$$
\theta(t) = (A + B t) e^{-\frac{b}{2} t}
$$

- **Underdamped** ($ b^2 - 4 \omega_0^2 < 0 $):

$$
\theta(t) = C e^{-\gamma t} \cos(\omega t + \phi)
$$

#### Symbols and Units
- θ': Angular velocity (rad/s)  
- θ'': Angular acceleration (rad/s²)  
- r: Characteristic root (s⁻¹)  
- A, B, C: Constants (rad), determined by initial conditions  
- γ: Damping factor (s⁻¹), where γ = b/2  
- ω: Damped angular frequency (rad/s), where ω = √(ω₀² - γ²)  
- φ: Phase angle (rad)  
- T: Damped period (s), where T = 2π / ω

## Simulation or Numerical Modeling (Optional)
Simulate with:
- Initial angle $ \theta_0 $ (rad)
- Damping coefficient $ b $ (s⁻¹)
- Length $ L $ (m)

Plot $ \theta(t) $ (rad) vs. $ t $ (s) or phase space ($ \theta $ vs. $ \theta' $).

## Experimental Setup (If Applicable)
Build a pendulum with:
- Mass on a string (length $ L $ in m)
- Damping via air or a vane

Measure $ \theta(t) $ (rad) and $ t $ (s), fitting amplitude decay to $ e^{-\gamma t} $ to find $ b $ (s⁻¹).

## Results and Discussion
Damping reduces amplitude exponentially (e.g., via $ e^{-\gamma t} $), with $ T $ (s) increasing slightly in underdamped cases. Larger $ b $ (s⁻¹) speeds decay. Compare theory to simulations/experiments if included.

## Conclusion
Damping, governed by $ b $ (s⁻¹), shapes pendulum motion, with practical uses in engineering and physics. Future work could explore nonlinear dynamics.