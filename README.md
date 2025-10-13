# Quantum-Grover-CPBO
# Grover Marker Oracle for Constrained Polynomial Binary Optimization

A Qiskit implementation of a Grover marker oracle for constrained polynomial binary optimization, as described in the paper "*Grover Adaptive Search for Constrained Polynomial Binary Optimization*".

# Overview

This project implement a quantum oracle that marks solutions satisfying both:
- **Objective**: `f(x) > t` (pseudo-Boolean function exceeds threshold)
- **Constraint**: `C(x) ≥ 0` (constraint function is non-negative)
The Qiskit function :


Imput:
1) $f: \mathbb{F}_2^n \to \mathbb{Z}   $.
2) $t \in \mathbb{Z}   $.
3)  $  C: \mathbb{F}_2^n\to \mathbb{Z}   $.

Output:  $ U_{f,t,C}   $ st:

$   U_{f,t,C} |x\rangle_n |y\rangle_1 = |x\rangle_n |y \oplus 1\rangle_1   $      if $   f(x) > t $ and $   C(x) \geq 0   $.


$ U_{f,t,C} |x\rangle_n |y\rangle_1 = |x\rangle_n |y\rangle_1   $ otherwise.


The oracle implements:
\[
U_{f,t,C} |x\rangle_n |y\rangle_1 = 
\begin{cases} 
|x\rangle_n |y \oplus 1\rangle_1, & \text{if } f(x) > t \text{ and } C(x) \geq 0 \\
|x\rangle_n |y\rangle_1, & \text{otherwise}
\end{cases}
\]


# Installation

```bash
git clone https://github.com/your-username/grover-marker-oracle.git
cd grover-marker-oracle
pip install -r requirements.txt
