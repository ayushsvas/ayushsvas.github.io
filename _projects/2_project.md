---
layout: page
title: Computational Physics
description: Projects from Methods of Computational Physics
img: 
importance: 2
category: work
---

<h3>Monte-Carlo Simulations in Statistical Physics</h3>
Consider Ising spins, $$s_{i}=\pm 1$$, on a two-dimensional, square lattice, where $$i=1, \cdots N^{2}$$ denotes the lattice index and $N$ is the linear dimension of the square lattice. The Hamiltonian of the 2D Ising model in units of the thermal energy scale, $$k_{\mathrm{B}} T$$, is given by

$$
\frac{\mathcal{H}(\{s\})}{k_{\mathrm{B}} T} \equiv-J \sum_{\langle i j\rangle} s_{i} s_{j}-H \sum_{i} s_{i}
$$

where the first sum runs over all nearest neighbor pairs of the two-dimensional lattice. Periodic boundary conditions are applied in all directions. With $$H=0$$ and $$N=16$$, implemented the Metropolis and Wang-Landau program with questions based on them.

<h3>Molecular Dynamics</h3>
<h5> Harmonic oscillator in a microcanonical ensemble </h5>
Consider the one-dimensional harmonic oscillator with the Hamiltonian

$$
\mathcal{H}^{\prime}\left(q^{\prime}, p^{\prime}\right)=\frac{p^{\prime 2}}{2 m}+\frac{1}{2} m \omega^{2} q^{\prime 2}
$$

where $$q^{\prime}$$ and $$p^{\prime}$$ denote the position and linear momentum of the particle, respectively. $$m$$ is the mass of the particle and $$\omega$$ characterizes the frequency of the oscillator. In this project, we implemented the Hamiltonian dynamcis using Euler, Runga-Kutta, velocity-Verlet algorithms.

<h5> Rouse polymer in the microcanonical and canonical ensemble </h5>
Consider a single, Gaussian polymer (in three spatial dimensions) that is described the coordinates and velocities, $$\left\{\mathbf{r}_{i}, \mathbf{p}_{i}\right\}$$ with $$i=1, \cdots, N$$, of its $$N$$ segments. Neighboring segments are bonded together by entropic, harmonic springs, and the Hamiltonian of the system takes the form

$$
\mathcal{H}=\frac{1}{2 m} \sum_{i=1}^{N} \mathbf{p}_{i}^{2}+\frac{3(N-1) k_{B} T}{2 R_{e}^{2}} \sum_{i=1}^{N-1}\left[\mathbf{r}_{i+1}-\mathbf{r}_{i}\right]^{2}
$$
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/md.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

For the numerics use $$N=64$$ and set the length scale $$R_{e}=1$$, energy scale $$k_{B} T=1$$, and mass $$m=1$$. Again, implemeted the dynamics using the velocity-Verlet. Later, attached an Andersen thermostat and Lowe-Andersen thermostat, and looked at the mean-squared displacement of center of mass of the polymer.

<h3> Rare Events </h3>
<h5> Transitions between two minima </h5>
Consider a particle in two-dimensional space, $$q \in\left[\begin{array}{ll}-1: 2\end{array}\right]\left[\begin{array}{ll}-1: 2]\end{array} \subset \mathbb{R}^{2}\right.$$, that is subjected to the external potential

$$
V(\mathbf{q})=V\left(q_{1}, q_{2}\right)=\left(1-e^{-\left(q_{1}-0.3 q_{2}\right)^{2}-8\left(0.3 q_{1}+q_{2}\right)^{2}}\right)\left(1-e^{-\left(q_{1}-1\right)^{2}-8\left(q_{2}-1\right)^{2}}\right)
$$

depicted below. Periodic boundary conditions are applied. Used Henkelman's dimer methods to calculate the saddle point. Time evolved the particle tranjectory on this free energy landscape via the Monte-Carlo process, and computed the Minimum Energy Path (MEP) via the string method. Also calculated quantities like reactive flux, transition rate using forward-flux sampling and flux-over-population method etc. 
<div class="row">
    <div class="col">
        {% include figure.liquid path="assets/img/landscape.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col">
        {% include figure.liquid path="assets/img/string.gif" title="example image" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<h3> Quantum Monte-Carlo Simulation </h3>
Implemented the Diffusion Quantum Monte-Carlo (DQM ) simulation 
for the one-dimensional harmonic oscillator with mass $$m$$ and frequency $$\omega$$, of which the potential energy takes the form

$$
V(x)=\frac{1}{2} m \omega^{2} x^{2}
$$

to estimate the groundstate wavefunction. Studied the world-lines of the particles in the harmonic potential by the path-integral Monte-Carlo. Also implemeted the Levy-Bridge construction for the free-propagator.

<div class="row">
    <div class="col">   
    </div>
    <div class="col-6">
        {% include figure.liquid path="assets/img/DQMC.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col">
    </div>
</div>


<h3> Linear Algebra </h3>
Implemented the Lanczos method to estimate the lowest eigenvalue of a real symmetric matrix. Plotted the CPU timescale as a function of matrix dimension n. [Missing Plot]

<h3> Partial Differential Equations (PDEs) </h3>
<h5> Modified diffusion equation - Initial value problem </h5>
The Schrödinger equation in imaginary time, $$\tau$$, takes the form

$$
-\frac{\partial \psi}{\partial \tau}=-\frac{\hbar^{2}}{2 m} \frac{\partial^{2} \Psi}{\partial x^{2}}+V \Psi
$$

where $$\Psi(x, \tau)$$ denotes the particle's wavefunction and $$V(x)$$ is the external potential.

$$
V(x)=\frac{1}{2} m \omega^{2}\left[\frac{L}{\pi} \cos \left(\frac{\pi x}{L}\right)\right]^{2}-E_{T}
$$

The potential, $$V(x)$$, is periodic with spatial period $$L$$. Therefore, we only consider the interval $$[0: L]$$ and apply periodic boundary conditions. In the following we rescale all lengths by $$x_{0}^{2}=\frac{\hbar}{m \omega}$$ and all energies by $$\hbar \omega$$. Implemented forward Euler algorithm, Crank-Nicolson methods, pseudo-spectral technique for solution propagation. 

<h5>Laplace equation - Boundary value problem </h5>
Consider the two-dimensional Laplace equation

$$
\triangle \phi(x, y)=0
$$

in a quadratic domain of size $$L \times L$$. The potential $$\phi$$ vanishes on the boundary of the domains. There are $$N$$ circular electrodes inside the domain with center $$\left(x_{i}, y_{i}\right)$$ and radius $$r_{i}$$. The potential on the surface of the electrodes is set to $$V_{i}$$. Computed the potential $$\phi(x,y)$$ using successive over-relaxation (SOR) algorithm.
