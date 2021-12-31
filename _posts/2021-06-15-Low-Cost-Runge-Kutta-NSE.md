---
layout: post
title: Low-Cost Runge-Kutta Integrators for Incompressible Flow Simulations
tags: [Navier-Stokes,Projection-Based Solvers,Low-Cost]
---

Achieving faster incompressible fluid simulations by dropping the pressure projections at the intermediate stages of Runge-Kutta integrators 

**Abstract**

We derive a novel class of low-cost explicit Runge-Kutta (RK) methods for the incompressible Navier-Stokes equations using pressure-based methods. Pressure-based methods require the solution of a Poisson equation for the pressure which is subsequently used to enforce mass conservation. In most cases, the Poisson equation is an expensive proposition, especially in the context of high-performance computing, where the cost of data transfers for global linear solvers can reduce scalability. In addition, when coupled with an RK scheme to achieve high accuracy in time, pressure-based methods require a Poisson solve at each intermediate RK stage, rendering pressure-based methods quite costly on large supercomputers. The proposed time integrators eliminate the need for a pressure-Poisson equation at intermediate stages while retaining formal order of accuracy. This is accomplished by deriving rational interpolants of the pressure from previous timesteps while preserving formal order of accuracy. For example, we will show that only one pressure Poisson equation is needed for second, third, and fourth-order Runge-Kutta schemes. We also find that while the proposed schemes impact stability, overall cost savings of up to 40% are still achievable over a wide range of Reynolds numbers. All the proposed integrators result in the same stability regions for cell Reynolds numbers of up to 10 while producing lower stability for larger cell Reynolds numbers.

* Main article in Journal of Computational Physics: [https://doi.org/10.1016/j.jcp.2021.110518](https://doi.org/10.1016/j.jcp.2021.110518)

* Cite as: *Karam, M., Sutherland, J. C., & Saad, T. (2021). Low-cost Runge-Kutta integrators for incompressible flow simulations. Journal of Computational Physics, 110518.* 

### Summary Slides 
---
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSOUD8mv0wq4rnCeo5H8q_rDTLyq0l1lLpo6rbfiPORj8e5Xh8y-w7Tvxh4beHQaEwXMChz4xg08jGo/embed?start=true&loop=true&delayms=5000" frameborder="0" width="700" height="450" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
