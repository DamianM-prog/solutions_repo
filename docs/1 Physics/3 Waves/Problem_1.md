# Problem 1

Wave Mechanics and the Doppler Effect
Transverse and Longitudinal Waves
Waves are disturbances that propagate energy through a medium or space. They are classified into two primary types based on the direction of particle oscillation relative to wave propagation:

Transverse Waves: Particles oscillate perpendicular to the direction of wave propagation. For a wave traveling along the $x$-axis, particle displacement occurs in the $y$-direction, described by $y(x,t) = A \sin(kx - \omega t)$, where $A$ is amplitude, $k = \frac{2\pi}{\lambda}$ is the wave number, $\lambda$ is wavelength, and $\omega = 2\pi f$ is angular frequency, with $f$ as frequency. Examples include electromagnetic waves and waves on a string.

Longitudinal Waves: Particles oscillate parallel to the direction of wave propagation. In sound waves traveling along the $x$-axis, particles create compressions and rarefactions, with pressure variations expressed as $p(x,t) = p_0 \sin(kx - \omega t)$. Examples include sound waves and seismic P-waves.


Key Differences:

Oscillation Direction: Transverse waves oscillate perpendicular to propagation; longitudinal waves oscillate parallel.
Polarization: Transverse waves can be polarized; longitudinal waves cannot.
Medium: Transverse waves require shear strength (e.g., solids), while longitudinal waves propagate in solids, liquids, and gases.

Wave Velocity, Frequency, and Wavelength
The velocity $v$ of a wave relates its frequency $f$ and wavelength $\lambda$ via:
$$v = f \lambda$$

Wave Velocity ($v$): Speed of wave propagation, dependent on the medium (e.g., tension for strings, density for sound).
Frequency ($f$): Oscillations per second, in hertz (Hz), where $f = \frac{1}{T}$, with $T$ as the period.
Wavelength ($\lambda$): Distance between consecutive in-phase points (e.g., crests), in meters.

For example, a sound wave in air ($v = 343$ m/s) with $f = 440$ Hz (A4 note) has wavelength:

$$\lambda = \frac{v}{f} = \frac{343}{440} \approx 0.78 , \text{m}$$
Superposition of Waves
Superposition occurs when multiple waves overlap, with their displacements adding algebraically:

$$ y_{\text{total}}(x,t) = y_1(x,t) + y_2(x,t) $$

Example 1: Constructive Interference
Two transverse waves on a string, with $\lambda = 1$ m, $A_1 = A_2 = 0.1$ m, and no phase difference:

$$y_1(x,t) = 0.1 \sin(2\pi x - \omega t)$$ 

$$y_2(x,t) = 0.1 \sin(2\pi x - \omega t)$$

Resultant:
$$ y_{\text{total}}(x,t) = 0.2 \sin(2\pi x - \omega t) $$
The amplitude doubles to 0.2 m due to constructive interference.
Example 2: Destructive Interference
Two waves with $\lambda = 1$ m, $A_1 = 0.1$ m, $A_2 = 0.05$ m, and phase difference $\pi$:
$$ y_1(x,t) = 0.1 \sin(2\pi x - \omega t) $$$$ y_2(x,t) = 0.05 \sin(2\pi x - \omega t + \pi) = -0.05 \sin(2\pi x - \omega t) $$
Resultant:
$$ y_{\text{total}}(x,t) = 0.05 \sin(2\pi x - \omega t) $$
The amplitude reduces to 0.05 m due to partial destructive interference.
Example 3: Beats
Two sound waves with $f_1 = 440$ Hz, $f_2 = 442$ Hz, and $A = 0.1$ Pa:
$$ p_1(x,t) = 0.1 \sin(2\pi \cdot 440 t) $$$$ p_2(x,t) = 0.1 \sin(2\pi \cdot 442 t) $$
Resultant:
$$ p_{\text{total}}(t) = 0.2 \cos(2\pi \cdot 1 t) \sin(2\pi \cdot 441 t) $$
This produces beats with a beat frequency of $f_2 - f_1 = 2$ Hz.
Can Two Speakers Produce Silence?
Yes, two speakers can produce silence at specific points via destructive interference. For sound waves with equal frequency, amplitude, and wavelength but a phase difference of $\pi$:
$$ p_1(x,t) = p_0 \sin(kx - \omega t) $$$$ p_2(x,t) = p_0 \sin(kx - \omega t + \pi) = -p_0 \sin(kx - \omega t) $$
$$ p_{\text{total}}(x,t) = 0 $$
Silence occurs at nodes where waves cancel, though this is position-dependent.
The Doppler Effect
The Doppler Effect describes the change in observed frequency $f'$ due to relative motion between source and observer:
$$ f' = f \left( \frac{v \pm v_o}{v \mp v_s} \right) $$
where $v$ is wave speed, $v_o$ is observer velocity (positive toward source), and $v_s$ is source velocity (positive away from observer). The numerator uses $+$ if the observer moves toward the source, $-$ if away; the denominator uses $-$ if the source moves toward the observer, $+$ if away.
Configurations

Stationary Source, Moving Observer:

Toward source ($v_o > 0$, $v_s = 0$):$$ f' = f \left( \frac{v + v_o}{v} \right) $$Example: For $f = 440$ Hz, $v = 343$ m/s, $v_o = 10$ m/s, $f' = 440 \left( \frac{343 + 10}{343} \right) \approx 452.2$ Hz.
Away: Use $-v_o$, reducing $f'$.


Moving Source, Stationary Observer:

Source toward observer ($v_s > 0$, $v_o = 0$):$$ f' = f \left( \frac{v}{v - v_s} \right) $$Example: $v_s = 10$ m/s, $f' = 440 \left( \frac{343}{343 - 10} \right) \approx 453.5$ Hz.
Away: Use $+v_s$, reducing $f'$.


Both Moving:

Both toward each other ($v_o > 0$, $v_s > 0$):$$ f' = f \left( \frac{v + v_o}{v - v_s} \right) $$Example: $v_o = 10$ m/s, $v_s = 10$ m/s, $f' = 440 \left( \frac{343 + 10}{343 - 10} \right) \approx 465.9$ Hz.



Mathematical Symbols and Units
Below is a summary of the mathematical symbols and their corresponding units used in this note:

$x$: Spatial coordinate, typically along the wave propagation direction, in meters (m).
$t$: Time, in seconds (s).
$y(x,t)$: Displacement in transverse waves, in meters (m).
$p(x,t)$: Pressure variation in longitudinal waves, in pascals (Pa).
$A$, $p_0$: Amplitude of displacement or pressure, in meters (m) or pascals (Pa).
$k$: Wave number, $k = \frac{2\pi}{\lambda}$, in radians per meter (rad/m).
$\lambda$: Wavelength, in meters (m).
$\omega$: Angular frequency, $\omega = 2\pi f$, in radians per second (rad/s).
$f$: Frequency, in hertz (Hz).
$T$: Period, $T = \frac{1}{f}$, in seconds (s).
$v$: Wave velocity, in meters per second (m/s).
$v_o$: Observer velocity, in meters per second (m/s).
$v_s$: Source velocity, in meters per second (m/s).
$f'$: Observed frequency in Doppler Effect, in hertz (Hz).

## Vizualization of Wave Interferece 

### Wave with 1 source

![alt text](Fizyk.gif)

### Wave with 2 sources

![alt text](Fizyk2.gif)

### Wave with 3 sources

![alt text](Fizyk3.gif)

### Pentagonal Wave shape (5 sources)

![alt text](Fizyk4.gif)