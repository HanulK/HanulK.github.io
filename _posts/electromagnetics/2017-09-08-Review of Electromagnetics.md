---
layout: post
title:  "Review of Electromagnetics"
date:   2017-09-08
categories: electromagnetics
comments: false
---

* content
{:toc}

## Contents

### Introduction
#### FDTD
  FDTD : Finite-difference time-domain or Yee's method   
  
  It is a numerical analysis technique used for modeling computational electrodynamics. Since it is a time-domain method, FDTD solutions can cover a wide frequency range with a single simulation run, and treat nonlinear material properties in a natural way.   
  The FDTD method belongs in the general class of grid-based differential numerical modeling methods. The time-dependent Maxwell's equations are discretized using central-difference approximations to the space and time partial derivatives. The resulting finite-difference equations are solved in either software or hardware in a leapfrog manner: the electric field vector components in a volume of space are solved at a given instant in time; then the magnetic field vector components in the same spatial volume are solved at the next instant in time; and the process is repeated over and over again until the desired transient or steady-state electromagnetic field behavior is fully evolved.   

  electric field vector components ->  magnetic field vector components -> electric field vector components -> ...   


#### FVTD


#### FDFD


#### FEM



### Review of electromagnetic theory
#### Constitutive relations and material properties

#### Time-Harmonic Maxwell's equations

#### Complex permittivity : dielectric losses

#### Complx permeability : magnetic losses

#### Equivalent magnetic currents

#### Electromagnetic potentials

#### Electromagnetic boudary conditions

#### Electromagnetic waves

#### the electromagnetic spectrum


## Texts
* U.S. Inan, R.A. Marshall, Numerical Electromagnetics - The FDTD Method, Cambridge, 2011. 1 - 68p

## Reference site
* [Finite-difference_time-domain_method](https://en.wikipedia.org/wiki/Finite-difference_time-domain_method)
