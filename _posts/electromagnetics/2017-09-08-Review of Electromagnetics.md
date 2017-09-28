---
layout: post
title:  "numerical methods"
date:   2017-09-08
categories: electromagnetics
comments: false
---

* content
{:toc}

# Numerical Methods

## FDTD
  FDTD : Finite-difference time-domain or Yee's method   

  It is a numerical analysis technique used for modeling computational electrodynamics. Since it is a time-domain method, FDTD solutions can cover a wide frequency range with a single simulation run, and treat nonlinear material properties in a natural way.   
  The FDTD method belongs in the general class of grid-based differential numerical modeling methods. The time-dependent Maxwell's equations are discretized using central-difference approximations to the space and time partial derivatives. The resulting finite-difference equations are solved in either software or hardware in a leapfrog manner: the electric field vector components in a volume of space are solved at a given instant in time; then the magnetic field vector components in the same spatial volume are solved at the next instant in time; and the process is repeated over and over again until the desired transient or steady-state electromagnetic field behavior is fully evolved.   

### Sequence
electric field vector components ->  magnetic field vector components -> electric field vector components -> ...   

### Strengths
- Short development time : It has simple discretization process than any oter methods like Finit Element method
- Ease of understanding : It is intutive, so users can easily understand how to use it and know to expect from a given model
- Explicit nature : No linear algebra or matrix inverstions are required. So, computer time is the only limitation

### Weaknesses
- Stair stepping edges : The orthogonal grid structure of the FDTD method implies that edges of structures within the simulation have edges that follow the grid structure. This can become a problem for curved surfaces
- Computational time : In the FDTD method, the time step at which we advance the solution is limited by the spatial size


## FVTD
  FVTD : Finite-volume time-domain   

  The FVTD became popular in modeling electromagnetic problems due to its flexibility in modeling irregular structures. In this method, small volumes typically taken to be tetrahedra in 3D or triangles in 2D. These shapes simplify the resulting equations and can be designed around curved and complex structures quite well. It then uses the integral forms ( FVM using integral forms ) of Maxwell's eqs to conserve the field quantities.

  ![tetrahedra](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ1BoN3sbU-B-6CC4CXpxDUnb8Gvy3un0eAfzte51_ghYTYny16)  < tetrahedra >
  ![triangle](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSm0xbCqNq6qPoX4GtNwS8RaC0ZkMjyQRnIIFRG0D-maKVvuPC2)  < triangle >

### Strengths
  - Irregular structures can be modeled quite easily
  - The simulation time is typically very similar to the FDTD method

### Weaknesses
  - Need to create and define an irregular grid of cells

## FDFD
  FDFD : Finite-difference frequency-domain method

  The FDFD method are extremely useful when a transient or broadband analysis is required. And in some problems that have scattering pattern, the frequency domain methods can be much more efficient instead time domain. Because, they avoid the need to step im time.

### Strengths
- Highly applicable : It maintains the spatial features of the FDTD method, but remoces time stepping
- useful when solve dispersive materials problems
- It is good for broadband simulations

### Weaknesses
- Requires solving a sparse matrix

# Texts
* U.S. Inan, R.A. Marshall, Numerical Electromagnetics - The FDTD Method, Cambridge, 2011.

# Reference site
* [Finite-difference_time-domain_method](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method)
* [Finite-difference_frequency-domain_method](https://en.wikipedia.org/wiki/Finite-difference_frequency-domain_method)
