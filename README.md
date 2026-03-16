# Alfven-wave-using-PIC
Particle and Field Response to an antenna-driven Alfvén wave in PIC simulation

Course final project for PHY118 - Computational Plasma Dynamics (WI26)


This project studies the particle response to an antenna-driven Alfven wave using Particle-in-Cell (PIC) simulations.
The simulations were run using the GPU-accelerated electromagnetic PIC code Entity. The setup is based on the problem generator in epaco-dartmouth/entity-pgens/mode_conversion/o_mode_periodic, with project-specific simulation parameters and analysis collected here.

## Simulation Notes
The simulations use periodic boundary conditions and an external antenna driver. Key physical and numerical parameters are specified partly in the `.toml`
files and partly in the underlying problem generator used for compilation.

## Simulation Setup
- Background magnetic field: $B_0 = (1,0,0)$ along the x-direction
- Periodic domain: $L_x = L_y = 2$
- Grid resolution: $800 \times 800$
-Antenna driving frequency chosen near the Alfven eigenmode

Different simulations explore the effect of:
- plasma temperature
- wave number
- driving frequency

## Analysis
The analysis notebooks in `analysis/` perform:  
- field visualization  
- wave energy evolution

Wave energy is computed as

$$
E_{\text{wave}} = \frac{1}{2}\int (E^2 + (B - B_0)^2)\ dV
$$

which isolates the energy of the propagating wave from the background magnetic field.


