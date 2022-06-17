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

##  Time-Evolution Operator

<img src="https://render.githubusercontent.com/render/math?math={\ket{\psi (t)} = &(QFT^{\dagger} ~e^{-i p^2 \Delta t} ~QFT) e^{-i V \Delta t} \notag &(QFT^{\dagger} ~e^{-i p^2 \Delta t} ~QFT) e^{-i V \Delta t} ~\ket{\Psi (0)}}">

<img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1">
