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
The solution of TDSE is a wavefunction in analytical form, manipulated using quantum algorithm, [Quantum Fourier Transform (QFT)](https://en.wikipedia.org/wiki/Quantum_Fourier_transform) and third order [Trotter Decomposition](https://en.wikipedia.org/wiki/Lie_product_formula).
The result was a wavefunction in quantum representation known as Time-Evolution Operator as follows:

![equation](https://latex.codecogs.com/svg.image?|\psi&space;(t)\rangle&space;=&space;(QFT^{\dagger}&space;~e^{-i&space;p^2&space;\Delta&space;t}&space;~QFT)&space;e^{-i&space;V&space;\Delta&space;t}&space;(QFT^{\dagger}&space;~e^{-i&space;p^2&space;\Delta&space;t}&space;~QFT)&space;e^{-i&space;V&space;\Delta&space;t}&space;~|\Psi&space;(0)\rangle)

Above equation then used to construct quantum circuits using IBM Quantum by initializing kinetic energy form and potential form to produce quantum gates.

## Quantum Circuits

Probability distributions of particle in finite square potential were obtained by simulating Time-Evolution Operator quantum circuits as follows:

![alt text](https://github.com/adh182/finite-sp-quantum-simulation/blob/master/data/time-evolution-operator-circuit.png?raw=true)

The energy of the sistem was calculated from estimated phase by applying [Quantum Phase Estimation (QPE)](https://en.wikipedia.org/wiki/Quantum_phase_estimation_algorithm) algorithm on Time-Evolution Operator.
The quantum circuit consists of two quantum registers: first quantum register acts as work register for estimating phase, and second quantum register acts as simulation register for simulating the Time-Evolution Operator circuit.

![alt text](https://github.com/adh182/finite-sp-quantum-simulation/blob/master/data/qpe-gate.png?raw=true)

## Parameters and Initializations

Gaussian wavefunctions were used as inputs to initialize the Time-Evolution Operator circuits.
The circuits simulate even wavefunction $|\psi_0\rangle = e^{-\sigma x^2}$ 
and odd wavefunction $|\psi_0\rangle = x e^{-\sigma x^2}$, and then determined how it evolves over time.

![alt text](https://github.com/adh182/finite-sp-quantum-simulation/blob/master/data/init-wvfunc.png?raw=true)

The sistem was calculated in the region $x=-0.5$ to $x=0.5$, and the potential barriers locate at $x=-0.25$ and $x=0.25$.

## Results
### Energy Estimation
### Probability distribution with 4, 5 and 6 qubits
### Probability distribution with different sigma values

Sigma values $\sigma = 10$ 
and $\sigma = 25$ used in the wavefunctions produce similar probability distributions.

### Probability distribution with different potential values

System that simulated with different potential values; $V_1=10$, $V_1=50$, $V_1=100$, and $V_1=150$ show no significant changes in the probability distributions. This indicates that the chosen potential values have no important effect on the system.
However, systems with potential values $V_1=500$ and $V_1=1000$ show extremely different probability distributions compared to the probability distributions simulated with lower potentials.
This is due to the systems behave as infinite potential well that have too high potential values that can be considered as infinite.

