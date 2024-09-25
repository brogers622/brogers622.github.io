---
title: Hemodynamics Research Papers
subtitle: Blood and vessel dynamics papers coauthored under Dr. Niema Pahlevan
[//]: # image:
[//]: # alt: Research

caption:
  title: Hemodynamics Research Papers
  subtitle: Viterbi School of Engineering
  thumbnail: assets/img/portfolio/thumbnail-field.png
---
Between 2020-2022 I had the privilege of working in the biomechanical research lab of [Dr. Niema Pahlevan](https://viterbi.usc.edu/directory/faculty/Pahlevan/Niema). Under the guidance of Dr. Pahlevan and his then-PhD student (now Dr.) [Arian Aghilinejad](https://www.linkedin.com/in/arian-aghilinejad-85828b108/), I coauthored two papers on cardiovascular fluid dynamics.

The [first paper](https://github.com/brogers622/portfolio/blob/18c59b9fa894b4369f521322821fec689fcc526e/1st%20coauthored%20paper.pdf) compared vessel pressure and vessel wall displacement during a cardiac cycle in calculating a novel cardiovascular index. The [second paper](https://github.com/brogers622/portfolio/blob/18c59b9fa894b4369f521322821fec689fcc526e/2nd%20coathored%20paper.pdf) explored the frequency-dependent pumping behavior due to cyclic stretching of compliant vesselsin in the direction of their central axis.
### Paper 1
The first paper investigated intrinsic frequency (IF), a novel index of cardiovascular health proposed by Dr. Pahlevan. The calculation of one's IF frequency requires a measurement of intravascular pressure as a function of time during a cardiac cycle. Like traditional blood pressure measured by a cuff at home or in a clinic, IF is proposed as a holistic indicator of overall cardiovascular functioning. Unfortunately, the invasiveness of measuring intravascular blood pressure limits the universality of IF measurement. It would thus be valuable to have an alternative means of calculating IF that did not require an invasiv intravascular pressure measurement. One potential option is the derivation of IF not from a pressure wave, but rather the radial enlargement of a blood vessel that accompanies the pressure changes over a cardiac cycle. This *displacement wave* can be measured non invasively, and inspires the motivating question underlying this paper: *how closely does displacement-based IF approximate pressure-based IF?*

This investigation consisted of an analytical approach handled by my colleagues and a computational approach handled by me. I was responsible for using computational fluid dynamics tools to simulate an aorta undergoing a cardiac cycle under various physiological conditions, and to extract pressure and displacement data from the simulations for IF analysis.

The figure below shows the simplified axisymmetric aorta model I arrived at by assuming that aortic branching, turns/twists, and diameter variation were all negligible.
![](assets/img/portfolio/model.png)
Using the finite element solver ADINA, I generated a discretized, fluid-solid interaction version of the above model. I applied physiologically-relevant boundary and initial conditions, developed and applied vessel wall material models, validated spatial and temporal discretization, ran simulations for multiple cardiac cycles until periodic steady state was reached, then extracted and plotted pressure and displacement data. I executed about 20 different cases manually. Parameters varied between cases included vessel geometry, vessel wall material properties, and inlet blood velocity waveform.

As shown in the plots below, the simulations suggested that displacement-based and pressure-based IF agree strongly if the vessel wall is purely elastic, but error increases with wall viscoelasticity. My colleague's analytical predictions agreed with the data reported by my simulations.
![](assets/img/portfolio/plots1.png)
### Paper 2
The second paper entailed a similar exploration but with different goals. Whereas the first paper had more immediate clinical relevance, this paper was a fundamental physics exploration of the impedence pumping behavior of compliant vessels due to longitudinal stretching.

An impedence pump is a type of valveless pump in which the wall of a compliant tube is agitated cyclically and a net flow develops as a results. The most common type of impedence pump is a radial impedence pump, in which the vessels is compressed and released radially in a cyclic fashion. Depending on vessel geometry and compression frequency, this can result in a net flow. This paper explored a *longitudinal* impedence pump, in which the cyclic agitation is in the direction of the vessel axis, which is much less studied than its radian counterpart.

Like the first paper, we undertook both analytical and computational approaches, and I was responsible for the simulations. I used the same software and a similar vessel model, although with some new boundary conditions and material definitions. The video below shows a custom periodic stretch and release boundary condition I developed for this study.
![](assets/img/portfolio/vessel.gif)
The primary difference in my experience of and contribution to this paper was the number of cases I needed to simulate. For the first paper I ran about 20 cases manually, which was quite labor intensive and also allowed room for user error in naming files, writing the in the correct parameters, etc. In the second paper, I needed to run well over 100 cases with different stretch frequencies, stretch magnitudes, vessel wall stiffnesses, and vessel lengths. Knowing that manual execution of all these cases was not feasible, I sought to automate the process.

Fortunately, ADINA can be operated manually via its UI *or* programmitally by feeding it a .txt file of ADINA commands. I ultimately automated the generation, execution, and postprocessing of >100 cases using Matlab to generate .txt files of commands and to analyze data, ADINA to run the cases, and the command line to orchestrate the transfer of information between the two softwares. The diagram below illustrates the interaction of Matlab, ADINA, and the command line.
![automation](assets/img/portfolio/automation.png)
In the end, the simulations and analytical approach predicted a highly frequency depended pumping behavior of the vessel, which could produce a net flow forward, backward, or not at all depending on the frequency.
### Acoustic Streaming Research + Presentation
Before working with Dr. Pahlevan, I also worked with [Dr. Anita Penkova](https://viterbi.usc.edu/directory/faculty/Penkova/Anita) to investigate the fluid dynamics of [acoustic streaming](https://en.wikipedia.org/wiki/Acoustic_streaming#:~:text=Acoustic%20streaming%20is%20a%20steady,waves%20within%20a%20Kundt's%20tube.), a net flow induced by sounds waves in a fluid. I investigate the phenomenon using the open source computational fluid dynamics tool OpenFOAM, and presented my team's findings in a virtual undergraduate symposium [Google Drive video link here](https://drive.google.com/file/d/1xZN7Vfau2ATikSEVXnsze9H4Ha9w9JrO/view?usp=drive_link).