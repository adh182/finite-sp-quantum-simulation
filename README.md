<h1 align="center">
  <br>
    SIMULATION OF PARTICLE IN FINITE SQUARE
    <br>POTENTIAL USING IBM QUANTUM
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

Time-Evolution Operator was obtained by deriving [Time-Dependent Schroedinger Equations (TDSE)](https://en.wikipedia.org/wiki/Schr%C3%B6dinger_equation).
The solution of TDSE is a wavefunction in analytical form, manipulated using quantum algorithm and third order [Trotter Decomposition](https://en.wikipedia.org/wiki/Lie_product_formula).
The result was a wavefunction in quantum representation known as Time-Evolution Operator as follows:

![equation](https://latex.codecogs.com/svg.image?|\psi&space;(t)\rangle&space;=&space;(QFT^{\dagger}&space;~e^{-i&space;p^2&space;\Delta&space;t}&space;~QFT)&space;e^{-i&space;V&space;\Delta&space;t}&space;(QFT^{\dagger}&space;~e^{-i&space;p^2&space;\Delta&space;t}&space;~QFT)&space;e^{-i&space;V&space;\Delta&space;t}&space;~|\Psi&space;(0)\rangle)

Above equation then used to construct quantum circuits using IBM Quantum by initializing kinetic energy form and potential form to produce quantum gates.

## Quantum Circuits

Probability distributions of particle in finite square potential were obtained by simulating Time-Evolution Operator quantum circuits as follows:

![alt text](https://github.com/adh182/finite-sp-quantum-simulation/blob/master/data/time-evolution-operator-circuit.png?raw=true)
<!-- <img src="https://render.githubusercontent.com/render/math?math=|\psi (t)\rangle = (QFT^{\dagger} ~e^{-i p^2 \Delta t} ~QFT) e^{-i V \Delta t} (QFT^{\dagger} ~e^{-i p^2 \Delta t} ~QFT) e^{-i V \Delta t} ~|\Psi (0)\rangle"> -->

<!-- <img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1"> -->
