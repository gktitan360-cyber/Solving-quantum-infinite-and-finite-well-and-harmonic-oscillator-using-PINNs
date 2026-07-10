# Physics-Informed Neural Networks (PINNs) for the Schrödinger Equation

This repository implements **Physics-Informed Neural Networks (PINNs)** to solve the time-independent and time-dependent Schrödinger equation for classic quantum mechanics problems. It also includes **Finite Element Method (FEM)** solutions to serve as a benchmark for evaluating the accuracy and performance of the neural network models.

---

## 🚀 Overview

Solving quantum mechanical systems traditionally relies on numerical methods like Finite Differences or Finite Element Methods (FEM). This project explores an alternative paradigm: using deep learning constrained by physical laws (Schrödinger's equation) to approximate the wavefunctions ($\psi$) and energy eigenvalues ($E$) of fundamental quantum systems.

---

## 📁 Repository Structure

The repository consists of the following Jupyter Notebooks:

| File Name | Description |
| :--- | :--- |
| `Infinite Quantum Well Problem.ipynb` | PINN implementation for a particle in a 1D box with infinite potential walls. |
| `Finite Quantum Well.ipynb` | PINN implementation for a particle in a finite potential well, capturing both bound and scattering states. |
| `Quantum Harmonic Oscillator.ipynb` | PINN implementation for the quadratic potential well, capturing quantized energy levels. |
| `FEM solutions.ipynb` | Standard Finite Element Method numerical solutions used to validate the PINN models. |

---

## 🧠 Problems Covered

### 1. Infinite Quantum Well (Particle in a Box)
* **Potential:** $V(x) = 0$ for $0 < x < L$, and $\infty$ otherwise.
* **Objective:** Learn the sinusoidal wavefunctions and discrete energy levels while strictly enforcing zero-boundary conditions at the walls.

### 2. Finite Quantum Well
* **Potential:** $V(x) = -V_0$ for $-a < x < a$, and $0$ otherwise.
* **Objective:** Resolve the transcendental equations implicitly through network optimization to find bound states and handle wave penetration into the classically forbidden regions.

### 3. Quantum Harmonic Oscillator
* **Potential:** $V(x) = \frac{1}{2}m\omega^2x^2$
* **Objective:** Approximate the Hermite-Gaussian wavefunctions and equidistant energy steps ($E_n = (n + \frac{1}{2})\hbar\omega$).

---

## 🛠️ Requirements & Installation

To run these notebooks locally, you need Python 3.8+ along with the following primary libraries:

* NumPy
* SciPy
* Matplotlib
* PyTorch (or TensorFlow, depending on your backend choice)
* FEniCS / SfePy (for the FEM benchmarks)

You can install the dependencies via pip:

```bash
pip install numpy scipy matplotlib torch
