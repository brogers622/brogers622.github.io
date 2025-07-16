---
title: Hemodynamics Research Papers
subtitle: Blood and vessel dynamics papers coauthored under Dr. Niema Pahlevan, 2020-2022
[//]: # image:
[//]: # alt: Research

caption:
  title: Hemodynamics Research Papers
  subtitle: Viterbi School of Engineering
  thumbnail: assets/img/portfolio/pahlevan/thumbnail-field.png
---
Between 2020-2022 I had the privilege of working in the biomechanical research lab of [Dr. Niema Pahlevan](https://viterbi.usc.edu/directory/faculty/Pahlevan/Niema). Under the guidance of Dr. Pahlevan and his then-PhD student (now Dr.) [Arian Aghilinejad](https://www.linkedin.com/in/arian-aghilinejad-85828b108/), I coauthored two papers on cardiovascular fluid dynamics.

The [first paper](https://github.com/brogers622/portfolio/blob/18c59b9fa894b4369f521322821fec689fcc526e/1st%20coauthored%20paper.pdf) blood vessel dilation as a noninvasive proxy for vessel pressure over a cardiac cycle for the calculation of a proposed cardiovascular health index. The [second paper](https://github.com/brogers622/portfolio/blob/18c59b9fa894b4369f521322821fec689fcc526e/2nd%20coathored%20paper.pdf) explored the frequency-dependent pumping behavior exhibited by compliant vessels under cyclic axial stretching.
### Paper 1
The first paper investigated **intrinsic frequency** (IF), a novel index of cardiovascular health proposed by Dr. Pahlevan. Calculation of IF requires measurement of pressure inside a vessel as a function of time during a cardiac cycle. Like traditional blood pressure measured by an inflating cuff, IF is proposed as a holistic indicator of overall cardiovascular functioning. Unfortunately, the invasiveness of intravascular blood pressure measurement limits the universality of IF assessment. It would thus be valuable to have a proxy for the intravascular pressure wave that can be measured *noninvasively*. One option for this is the radial displacement of the blood vessel during a cardiac cycle, ie how much the vessel enlarges. This *displacement wave* can be measured non invasively, and inspires the motivating question underlying this paper: **how closely does displacement-based IF approximate pressure-based IF?**

This investigation consisted of an analytical approach handled by my colleagues and a computational approach handled by me. I used computational fluid dynamics tools to simulate an aorta during a cardiac cycle under various physiological conditions, then extracted pressure and displacement data from the simulations for IF analysis.

The figure below shows the simplified axisymmetric aorta model I used, which assumes that aortic branching, turns/twists, and diameter variation all negligibly affect the wave behavior of interest.

![](assets/img/portfolio/pahlevan/model.png)
Using the finite element solver ADINA, I generated a discretized fluid-solid interaction version of the above model. I applied physiologically-relevant boundary and initial conditions, developed vessel wall material models, validated spatial and temporal discretization, ran simulations for multiple cardiac cycles until periodic steady state was reached, then extracted pressure and displacement data and plotted it in Matlab. I executed about 20 different cases, which varied in vessel geometry, vessel wall material properties, and inlet blood velocity waveform.

As shown in the plots below, the simulations suggested that displacement-based and pressure-based IF agree strongly if the vessel wall is purely elastic, but error increases with wall viscoelasticity. My colleague's analytical predictions agreed with the data reported by my simulations.

![](assets/img/portfolio/pahlevan/plots1.png)
### Paper 2
The second paper entailed a similar exploration but with different goals. Whereas the first paper had more immediate clinical relevance, this paper was a fundamental physics exploration of the pumping behavior of compliant vessels under longitudinal stretching.

*Impedence pumping* is a valveless pumping effect in which a net flow arises in a tube due periodic agitation of a flexible vessel wall. The most common type of impedence pump is the *radial impedence pump*, illustrated in the diagram below, in which the vessel wall is compressed radially and released in a periodic fashion. Depending on vessel geometry and compression frequency, this can result in a net flow.

![](assets/img/portfolio/pahlevan/radial-pump.png)

Our paper explored *longitudinal* impedence pumping, illustrated below, in which the cyclic agitation is in the direction of the vessel axis. This type of impedence pump is less studied than its radial counterpart.

![](assets/img/portfolio/pahlevan/longitudinal-pump.png)
Like the first paper, we undertook both analytical and computational approaches, and I was responsible for the simulations. I used the same software and a similar vessel model, although with some new boundary conditions and material definitions. The gif below shows a custom stretch-and-release boundary condition I developed to simulate longitudinal pumping.

![](assets/img/portfolio/pahlevan/vessel.gif)
This investigation required the simulation of >100 unique conditions, as compared to ~20 for the first paper which I generated, executed, and postprocessed manually. Running this many cases by hand was not advisable due to time constraints and risk user error - I thus sought to automate the simulation process.

Fortunately, ADINA can be operated programmatically by feeding it a .txt file of ADINA-language commands. To automate the entire process, I wrote a script in Matlab to generate ADINA command files to preprocess and postprocess a case, and a second Matlab script to clean and plot data that was extracted from a case after its successful execution. Finally, I wrote a main script for the command line that orchestrated the transfer of information between ADINA and Matlab. The diagram below illustrates the interaction of Matlab, ADINA, and the command line in this process.
![](assets/img/portfolio/pahlevan/automation.png)
In the end, the simulations and analytical approach predicted a highly frequency depended pumping behavior of the vessel, which could produce a net flow forward, backward, or not at all depending on the frequency.