---
layout: post
title: Stable timestep formulas for high-order advection–diffusion and Navier–Stokes solvers
tags: [Navier-Stokes,Stability,timestep sizes, adaptive timestepping]
---

New Stability rules for Navier-Stokes equation. No more worring about your solution blowing up!!

**Abstract**

We derive three-dimensional stable timestep formulas for high-order explicit time integration of the advection–diffusion equation. The proposed formulas cover explicit first, second, third, and fourth-order Runge–Kutta integrators in time as well as upwind, central, second-order, high-order upwind (-schemes), and flux-limiters for the advection term along with central discretization on the diffusion term. The stability rules are then compared to numerical computations of stable timesteps of the advection–diffusion equation and show excellent agreement. Finally, the formulas are implemented in a finite volume Navier–Stokes code and used to guide stable timestep selection to assess their suitability for Navier–Stokes solvers. All cases that were tested showed stable non-diverging solutions and significant improvement over common CFL-type stability specification. Despite its basis in the linear advection–diffusion equation, this work could be useful in providing a starting point for stable timestep selection for nonlinear evolutionary-type PDEs such as the Navier–Stokes equations.

* Main article in Journal of Computer \& Fluids: [https://doi.org/10.1016/j.compfluid.2022.105564](https://doi.org/10.1016/j.compfluid.2022.105564)

* Cite as: *Saad, T., & Karam, M. (2022). Stable timestep formulas for high-order advection–diffusion and Navier–Stokes solvers. Journal of Computers & Fluids, 105564.* 

### Explainer Video By Prof. Tony Saad
---
<iframe width="700" height="450" src="https://www.youtube.com/embed/adHsFXa2qp4" title="Stable Timestep Formulas for Navier-Stokes and Advection Diffusion Solvers" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>