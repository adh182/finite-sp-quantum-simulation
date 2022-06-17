<h1 align="center">
  <br>
    SIMULATION OF PARTICLE IN FINITE SQUARE POTENTIAL 
    <br> USING IBM QUANTUM
  <br>
</h1>

## Overview
Simulations of particles in finite square potential were performed on quantum circuit constructed based on time-evolution operator from wavefunction derived from time dependent Schroedinger equation. 
This research determines the probability distribution of particles in a finite square potential and its energy estimation by applying Quantum Phase Estimation algorithm.
Quantum circuits were constructed with Qiskit and simulations were performed on a quantum simulator provided by IBM Quantum. 
The simulation results show changes in the probability distribution over time indicate time evolution occurs. This shows the ability of the quantum circuit to simulate the system. 
Different potentials and sigma values show no significant changes in the probability distribution. 
However, quantum circuit constructed with QPE algorithm cannot obtain proper energy estimation due to nonconvergance value in higher iterations.


$F = m \dot a$
\begin{align}
    p_j^2 &= (2\pi N)^2 \left( \frac{j}{N} + \frac{1}{2N} - \frac{1}{2} \right)^2 \notag \\
    &\simeq (2\pi N)^2 \left( \frac{j}{N} - \frac{1}{2} \right)^2 \notag \\
    &= (2\pi N)^2 \left( \frac{j^2}{N^2} - \frac{j}{N} + \frac{1}{4} \right).
\end{align}
