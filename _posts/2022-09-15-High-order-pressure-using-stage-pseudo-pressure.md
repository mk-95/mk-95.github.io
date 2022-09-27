---
layout: post
title: High-order pressure estimates for Navier-Stokes Runge-Kutta solvers using stage pseudo-pressures
tags: [Navier-Stokes,low-cost integrators,Runge-Kutta, Stage Pseudo-pressure]
---

New formulas for high order instantaneous approximations using stage pseudo-pressures.

**Abstract**

This note addresses the question of whether stage pseudo-pressures can be used to build high-accuracy instantaneous pressure estimates in the context of projection-based Navier-Stokes solvers. The construction of such estimates using inter-stage pseudo-pressures is not straightforward, especially when time-dependent boundary conditions are present. New formulas are introduced that circumvent the limitation imposed by this type of boundary condition. While additional numerical costs might be involved in the construction of such estimates, the formulas are robust and show how one is able to recover high-order estimates of the pressure from within a Runge-Kutta pressure-projection scheme. The proposed formulas are then numerically tested on a two-dimensional channel flow simulation with unsteady inflow condition and show expected convergence rates.

* Main article in Journal of Computational Physics: [https://doi.org/10.1016/j.jcp.2022.111602](https://doi.org/10.1016/j.jcp.2022.111602)

* Cite as: *Karam, M., & Saad, T. (2022). High-order pressure estimates for Navier-Stokes Runge-Kutta solvers using stage pseudo-pressures. Journal of Computational Physics, 111602.* 
