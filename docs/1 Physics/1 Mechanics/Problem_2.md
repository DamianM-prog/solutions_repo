# Problem 2: Analyze the Dynamics of a Damped Pendulum

## 1. Scope and Objectives

- **Definition of a Damped Pendulum**:
  - A damped pendulum consists of a mass oscillating under gravity, attached to a pivot via a massless string or rod.
  - Unlike an ideal pendulum, it experiences energy dissipation due to damping forces (e.g., friction at the pivot or air resistance), causing the amplitude to decrease over time.
- **Goal of the Analysis**:
  - To investigate how damping alters the pendulum’s motion compared to the undamped case.
  - To explore this through:
    - Theoretical predictions of motion behavior.
    - Analytical mathematical solutions for the linear case.
    - Simulated behavior using numerical methods.
- **Real-World Relevance**:
  - Damped pendulums model systems like:
    - Mechanical clocks, where damping controls oscillation decay.
    - Shock absorbers in vehicles, mitigating vibrations.
  - Understanding damping is key to designing stable oscillatory systems.

## 2. Theoretical Framework

- **Simple Pendulum (Undamped)**:
  - Serves as the baseline for comparison.
  - **Governing Equation**:
    $$
    \frac{d^2 \theta}{dt^2} + \frac{g}{L} \sin(\theta) = 0
    $$
  - **Small-Angle Approximation**:
    - For small $ \theta $, $ \sin(\theta) \approx \theta $, simplifying to:
      $$
      \frac{d^2 \theta}{dt^2} + \omega_0^2 \theta = 0
      $$
    - Where $ \omega_0 = \sqrt{\frac{g}{L}} $ is the natural angular frequency.
  - **Solution**:
    - Harmonic motion: $ \theta(t) = \theta_0 \cos(\omega_0 t + \phi) $.
    - Period: $ T = 2\pi \sqrt{\frac{L}{g}} $.

- **Damped Pendulum**:
  - Introduces energy loss through damping.
  - **Governing Equation**:
    $$
    \frac{d^2 \theta}{dt^2} + b \frac{d \theta}{dt} + \frac{g}{L} \sin(\theta) = 0
    $$
  - **Linear Approximation**:
    - For small $ \theta $, $ \sin(\theta) \approx \theta $, yielding:
      $$
      \frac{d^2 \theta}{dt^2} + b \frac{d \theta}{dt} + \omega_0^2 \theta = 0
      $$

- **Parameters with Units**:
  - $\theta$: Angular displacement (radians, rad)
  - $t$: Time (seconds, s)
  - $b$: Damping coefficient (per second, s⁻¹)
  - $g$: Gravitational acceleration (meters per second squared, m/s²)
  - $L$: Pendulum length (meters, m)
  - $\omega_0$: Natural frequency (radians per second, rad/s), $\omega_0 = \sqrt{\frac{g}{L}}$

  ![alt text](image-4.png)

## 3. Mathematical Analysis

- **Solving the Linear Damped Equation**:
  - **Characteristic Equation**:
    $$
    r^2 + b r + \omega_0^2 = 0
    $$
  - **Roots**:
    - $ r = \frac{-b \pm \sqrt{b^2 - 4 \omega_0^2}}{2} $
  - **Damping Regimes**:
    - *Overdamped* ($ b^2 > 4 \omega_0^2 $):
      - Real, distinct roots \( r_1 \) and \( r_2 \).
      - Solution:
        $$
        \theta(t) = A e^{r_1 t} + B e^{r_2 t}
        $$
      - Motion decays exponentially without oscillation.
    - *Critically Damped* ($ b^2 = 4 \omega_0^2 $):
      - Repeated root \( r = -\frac{b}{2} \).
      - Solution:
        $$
        \theta(t) = (A + B t) e^{-\frac{b}{2} t}
        $$
      - Fastest return to equilibrium without oscillating.
    - *Underdamped* ($ b^2 < 4 \omega_0^2 $):
      - Complex roots \( r = -\gamma \pm i \omega \), where:
        - $ \gamma = \frac{b}{2} $ (damping factor, s⁻¹)
        - $ \omega = \sqrt{\omega_0^2 - \gamma^2} $ (damped frequency, rad/s)
      - Solution:
        $$
        \theta(t) = C e^{-\gamma t} \cos(\omega t + \phi)
        $$
      - Oscillatory motion with exponentially decaying amplitude.

- **Additional Variables**:
  - $ \theta' $: Angular velocity (radians per second, rad/s)
  - $ \theta'' $: Angular acceleration (radians per second squared, rad/s²)
  - $ T $: Damped period (seconds, s), $ T = \frac{2\pi}{\omega} $

- **Nonlinear Case**:
  - The full equation $ \frac{d^2 \theta}{dt^2} + b \frac{d \theta}{dt} + \frac{g}{L} \sin(\theta) = 0 $ is nonlinear due to $ \sin(\theta) $.
  - Analytical solutions are not feasible for large angles; numerical methods (e.g., Runge-Kutta) are required to capture the true dynamics.

### Vizualization available in my colab

[Simulation of several pendulum in my colab](https://colab.research.google.com/drive/14HV1BIjMX1YDGW0z-BtBkJoUXG2uz6u2#scrollTo=_k1Bu9c5w4-S)
## 4. Results Analysis

- **Comparison of Damping Regimes**:
  - *Underdamped*:
    - Oscillates with decaying amplitude.
    - Damped period $ T = \frac{2\pi}{\omega} $ slightly longer than undamped $ T_0 = 2\pi \sqrt{\frac{L}{g}} $.
  - *Critically Damped*:
    - Returns to $ \theta = 0 $ fastest without oscillation.
    - Optimal damping for stability.
  - *Overdamped*:
    - Slow, monotonic decay to $ \theta = 0 $ without oscillation.
    - Excessive damping delays equilibrium.

- **Energy Dissipation**:
  - Damping coefficient $ b $ controls the rate of energy loss.
  - Underdamped: Energy dissipates gradually via oscillations.
  - Critically/overdamped: Energy dissipates directly to zero.

- **Validation**:
  - Compare simulated decay rate $ e^{-\gamma t} $ (where $ \gamma = \frac{b}{2} $) to theoretical predictions.
  - Check period $ T = \frac{2\pi}{\sqrt{\omega_0^2 - \left(\frac{b}{2}\right)^2}} $ in underdamped case.
  