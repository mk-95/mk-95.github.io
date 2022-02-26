---
layout: post
title: High-order pressure estimates for projection-based Navier-Stokes solvers
tags: [Navier-Stokes,Projection-Based Solvers,High-order]
---

Explaining how to construct high-order instantaneous pressures for Navier-Stokes solvers.

**Abstract**

We derive high-order estimates of the instantaneous pressure for projection-type solvers of the incompressible Navier-Stokes equations. Projection methods play a central role in incompressible and low-Mach fluid flow simulations. However, these methods are known to produce a first-order instantaneous pressure at the end of a timestep, even when used with high-order integrators such as Runge-Kutta or Adams-Bashforth methods. In many instances, a high-order pressure is needed when the application demands it, such as turbulent aerodynamic flows, fluid-structure interaction, membrane filtration, and pressure-dependent boundary conditions. The common strategy to circumvent this limitation is to perform a so-called “post-processing” projection which results in an instantaneous pressure of the same order as the time integrator. However, this additional projection adds more cost to a simulation, especially in the context of high-performance computing. For example, in a third-order Runge-Kutta integration, requiring a post-processing projection increases the computational cost by 33%. Therefore, it is desirable to find high-order consistent estimates for the instantaneous pressure without the need for a post-processing projection. In this paper, we introduce a novel approximation to compute high-order estimates for the instantaneous pressure for arbitrary high-order time integrators, without the need for a post-processing projection. Our proposed approximations are independent of the time integration methodology or boundary conditions. We validate our results using various implicit and explicit integrators on different benchmark problems with periodic and time-dependent boundary conditions.

* Main article in Journal of Computational Physics: [https://doi.org/10.1016/j.jcp.2021.110925](https://doi.org/10.1016/j.jcp.2021.110925)

* Cite as: *Karam, M., & Saad, T. (2021). High-order pressure estimates for projection-based Navier-Stokes solvers. Journal of Computational Physics, 110925.* 

### Explainer Video By Prof. Tony Saad
---
<iframe width="700" height="450" src="https://www.youtube.com/embed/c54oATeNkdo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Summary Slides 
---
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSZraf11xWCun4DKR7qzeRahnBpTsP-w7d1HxCel2BK8M_3UN_kb2h_8YSxq8ROLhA9WX3PMh97efQw/embed?start=false&loop=false&delayms=5000" frameborder="0" width="700" height="450" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>