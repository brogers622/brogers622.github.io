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

The [first paper](https://github.com/brogers622/portfolio/blob/18c59b9fa894b4369f521322821fec689fcc526e/1st%20coauthored%20paper.pdf) compared vessel pressure and vessel wall displacement during a cardiac cycle in calculating a novel cardiovascular index. The [second paper](https://github.com/brogers622/portfolio/blob/18c59b9fa894b4369f521322821fec689fcc526e/2nd%20coathored%20paper.pdf) explored the frequency-dependent pumping behavior due to cyclic stretching of compliant vesselsin in the direction of their central axis.
### Paper 1
The first paper investigated intrinsic frequency (IF), a novel index of cardiovascular health proposed by Dr. Pahlevan. The calculation of one's IF requires a measurement of intravascular pressure as a function of time over a cardiac cycle. Like traditional blood pressure measured by a cuff at home or in a clinic, IF is proposed as a holistic indicator of overall cardiovascular functioning. Unfortunately, the invasiveness of measuring intravascular blood pressure limits the universality of IF measurement. It would thus be valuable to have an alternative means of calculating IF that did not require an invasive intravascular pressure measurement. One potential option is the derivation of IF not from a pressure wave, but rather the radial enlargement of a blood vessel that accompanies the pressure changes over a cardiac cycle. This *displacement wave* can be measured non invasively, and inspires the motivating question underlying this paper: *how closely does displacement-based IF approximate pressure-based IF?*

This investigation consisted of an analytical approach handled by my colleagues and a computational approach handled by me. I was responsible for using computational fluid dynamics tools to simulate an aorta undergoing a cardiac cycle under various physiological conditions, and to extract pressure and displacement data from the simulations for IF analysis.

The figure below shows the simplified axisymmetric aorta model I arrived at by assuming that aortic branching, turns/twists, and diameter variation all negligibly affected the wave behavior of interest.

![](assets/img/portfolio/pahlevan/model.png)
Using the finite element solver ADINA, I generated a discretized fluid-solid interaction version of the above model. I applied physiologically-relevant boundary and initial conditions, developed and applied vessel wall material models, validated spatial and temporal discretization, ran simulations for multiple cardiac cycles until periodic steady state was reached, then extracted pressure and displacement data and plotted it using Matlab. I executed about 20 different cases manually. Parameters varied between cases included vessel geometry, vessel wall material properties, and inlet blood velocity waveform.

As shown in the plots below, the simulations suggested that displacement-based and pressure-based IF agree strongly if the vessel wall is purely elastic, but error increases with wall viscoelasticity. My colleague's analytical predictions agreed with the data reported by my simulations.

![](assets/img/portfolio/pahlevan/plots1.png)
### Paper 2
The second paper entailed a similar exploration but with different goals. Whereas the first paper had more immediate clinical relevance, this paper was a fundamental physics exploration of the impedence pumping behavior of compliant vessels due to longitudinal stretching.

*Impedence pumping* is a valveless pumping effect in which a net flow arises in a compliant tube due periodic agitation of the vessel wall. The most common type of impedence pump is the *radial impedence pump*, illustrated in the diagram below, in which the vessel wall is compressed radially and released in a periodic fashion. Depending on vessel geometry and compression frequency, this can result in a net flow.

![](assets/img/portfolio/pahlevan/radial-pump.png)
Our paper explored *longitudinal* impedence pumping, illustrated below, in which the cyclic agitation is in the direction of the vessel axis. This type of impedence pump is less studied than its radial counterpart.

![](assets/img/portfolio/pahlevan/longitudinal-pump.png)
Like the first paper, we undertook both analytical and computational approaches, and I was responsible for the simulations. I used the same software and a similar vessel model, although with some new boundary conditions and material definitions. The video below shows a custom stretch-and-release boundary condition I developed to simulate longitudinal pumping.

![](assets/img/portfolio/pahlevan/vessel.gif)
The primary difference in my experience of and contribution to this paper was the number of cases I needed to simulate. For the first paper I ran about 20 cases manually, which was quite labor intensive and allowed room for user error in naming files, typing parameter values correctly, etc. In the second paper, I needed to generate, execute, and postprocess well over 100 cases with different stretch frequencies, stretch magnitudes, vessel wall stiffnesses, and vessel lengths. Knowing that manual execution of this many cases was not feasible, I sought to automate the process.

Fortunately, ADINA can be operated manually via its UI *or* programmatically by feeding it a .txt file of ADINA commands. In order to automate the entire process, I wrote a script in Matlab to generate two .txt files containing ADINA commands to preprocess and postprocess a case, and a second Matlab script to clean and plot data that was extracted from a case after its successful execution. Finally, I wrote a main script for the command line that fed the parameters of the case to Matlab and orchestrated the transfer of information between ADINA and Matlab. The diagram below illustrates the interaction of Matlab, ADINA, and the command line in this process.
![](assets/img/portfolio/pahlevan/automation.png)
In the end, the simulations and analytical approach predicted a highly frequency depended pumping behavior of the vessel, which could produce a net flow forward, backward, or not at all depending on the frequency.