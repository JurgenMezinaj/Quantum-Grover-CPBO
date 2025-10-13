# Quantum-Grover-CPBO
# Grover Marker Oracle for Constrained Polynomial Binary Optimization

A Qiskit implementation of a Grover marker oracle for constrained polynomial binary optimization, as described in the paper "*Grover Adaptive Search for Constrained Polynomial Binary Optimization*".

# Overview

This project implement a quantum oracle that marks solutions satisfying both:
- **Objective**: `f(x) > t` (pseudo-Boolean function exceeds threshold)
- **Constraint**: `C(x) ≥ 0` (constraint function is non-negative)

The oracle implements:
\[
U_{f,t,C} |x\rangle_n |y\rangle_1 = 
\begin{cases} 
|x\rangle_n |y \oplus 1\rangle_1, & \text{if } f(x) > t \text{ and } C(x) \geq 0 \\
|x\rangle_n |y\rangle_1, & \text{otherwise}
\end{cases}
\]

# Features

- **Minimal Implementation**: Only 3 qubits for n=2 case
- **Verified Correctness**: All test cases pass with quantum simulation
- **Qiskit Compatible**: Ready for integration with Grover's algorithm

# Installation

```bash
git clone https://github.com/your-username/grover-marker-oracle.git
cd grover-marker-oracle
pip install -r requirements.txt
