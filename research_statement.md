---
layout: page
title: Research Statement
permalink: /research_statement/
---
<div style="text-align: right">
<form action="https://drive.google.com/file/d/1zSsmA5WV5Xkrt--Yqu8dkOHMg_E-zCnY/view?usp=sharing" method="get" target="_blank"><button type="submit">Download as PDF</button></form>
</div>
<br/>

My fascination with numerical methods, fluid mechanics, and computer science naturally led me to pursue a career in engineering and computational fluid dynamics (CFD).
Since the early days of computing, the speed of computer processors (CPUs) has been doubling approximately every two years.
This trend in performance cannot go on forever, and trying to pack more power in the same chip size is getting considerably more difficult.
Instead of pursuing a brute-force approach to scientific computing, one should seek a more effective approach that balances modeling and computing. 
Such an approach relies heavily on identifying alternative algorithms and numerical methods that optimize the use of the hardware and computing resources.
To that end, I have focused my doctoral research on finding alternative methods to improve the efficiency and performance of high-fidelity fluid dynamics simulations.

In a typical CFD calculation, the solution of the pressure field consumes up to  40% of the total cost.
This cost is further augmented when high time accuracy is required for highly transient flows such as turbulent flows.
One recent example of how this cost can overwhelm a calculation is my work with the Utah Symphony/Utah Opera to understand COVID-19 risk at two of their concert halls in Salt Lake City, UT.
Because singing and playing wind instruments play a fundamental role in transmitting airborne diseases such as COVID-19, CFD simulations were critical in helping USUO assess its risks and identify suitable engineering-based mitigation strategies at a time when vaccines were not available.
At the outset, we used highly accurate CFD calculations to simulate the airflow at Abravanel Hall and Capitol Theater and subsequently developed strategies to reduce the accumulation of disease-carrying respiratory aerosols by two orders of magnitude[^hayden_karam].
The results from this study[^fn1] were critical for USUO in their decision to resume their activities in a safe environment.


While those calculations showed how CFD could play a critical role in understanding airborne disease transmission, they came at a very high cost.
The simulations required 500,000 hours of CPU time on a supercomputer for a total of 3 weeks runtime using 1,000 CPUs. 
Assuming an average cost of 15 cents per CPU hour[^walker2009real], the dollar cost of these simulations is \$75,000 with the cost of computing the pressure amounting to \$30,000 (200,000 CPU hours).
This relatively high cost of the pressure is no surprise because the pressure field is used to enforce mass conservation.


So how do we reduce the cost of CFD simulations? It seems rational to first tackle the most expensive part - the pressure field.
Based on anecdotal evidence, I asked the question: what happens if we do not compute the pressure and instead replace it with a cheap approximation? 
I then tested the hypothesis that {\bf expensive calculations of the pressure can be replaced with cheap approximations without sacrificing accuracy and mass conservation}.
My four-year investigation into this question resulted in a new mathematical framework that untangles the role of the pressure in the numerical simulation of the Navier-Stokes equations resulting in new time integration methods that are 40% cheaper than conventional methods[^Karam_Sutherland_Saad_2021] [^Karam_Saad_2021] [^karam_saad_generalization_2022] [^karam_saad_aiaa_2021]. 
Using the newly proposed methods with the COVID-19 simulations would have saved us 200,000 CPU hours or a cost of \$30,000 dollars, while producing identical results with the same accuracy.

Today, despite the immense advances in user-friendly technologies, CFD is still considered to be within the realm of the well-versed in the field.
However, the CFD of tomorrow will no longer require users to have expert knowledge on how the computation is happening in the background, and artificial intelligent systems will guide the simulation on their behalf. 
Moreover, most of the CFD tools will be hosted online on cloud computing systems where the resources are automatically managed to meet the needs of a simulation.
For this to happen, algorithms will have to evolve in order to efficiently use these environments.
Using the knowledge I accumulated during my doctoral research, I plan to continue developing numerical solvers and methods that lead the way to the new era of highly efficient, scalable, and accessible CFD tools.

[^fn1]: This study was featured in the following media sources: [The New York Times](https://www.nytimes.com/2021/06/23/health/coronavirus-orchestra.html), [New Scientist](https://www.newscientist.com/article/2281794-turning-orchestras-inside-out-could-lower-risk-of-spreading-covid-19/) , [Science News](https://www.sciencenews.org/article/coronavirus-covid-musicians-relocating-reduce-risk-concerts), and [The Student Innovation Report 2021](https://lassonde.utah.edu/keeping-the-symphony-open/) at the University of Utah.

[^hayden_karam]: Hayden A. Hedworth**, Mokbel Karam,** Josh McConnell, James C. Sutherland, and Tony Saad, Mitigation Strategies for Airborne Disease Transmission in Orchestras Using Computational Fluid Dynamics, 2021, Science Advances (Volume 7, number 26, eabg4511, [https://doi.org/10.1126/sciadv.abg4511](https://doi.org/10.1126/sciadv.abg4511)).

[^walker2009real]: E. Walker, The real cost of a cpu hour, Computer 42 (4) (2009) 35–41. [https://doi.org/10.1109/MC.2009.135](https://doi.org/10.1109/MC.2009.135)

[^Karam_Sutherland_Saad_2021]: M. Karam, J. C. Sutherland, T. Saad, Low-cost runge-kutta integrators for incompressible flow simulations, Journal of Computational Physics (2021) 110518 [https://doi.org/10.1016/j.jcp.2021.110518](https://doi.org/10.1016/j.jcp.2021.110518)

[^Karam_Saad_2021]: M. Karam, T. Saad, High-order pressure estimates for projection-based navier-stokes solvers, Journal of Computational Physics (2021) 110925 [https://doi.org/10.1016/j.jcp.2021.110925](https://doi.org/10.1016/j.jcp.2021.110925).


