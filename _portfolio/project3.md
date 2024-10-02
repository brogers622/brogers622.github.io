---
title: Flexible Wave Energy Converter
subtitle: senior design project - design, fabrication, testing, and analysis of a novel compliant-membrane-based hydroelectric generator
[//]: # image: assets/img/portfolio/02-full.jpg
[//]: # alt: Keep Exploring

caption:
  title: Flexible Wave Energy Converter
  subtitle: design, fabrication, testing
  thumbnail: assets/img/portfolio/wec/thumbnail-wec.png
---
In the final semester of our mechanical engineering bachelors at USC, two other students and I designed and fabricated a novel device that converted water wave energy to electrical energy. The process is summarized below; for more detailed descriptions feel free to check out the [final report](assets/img/portfolio/wec/report.pdf) and [presentation slides](assets/img/portfolio/wec/slides.pdf).
### Design
The goal of the device was to convert a portion of a water wave's kinetic and potential energy to electrical energy by leveraging pressure variation over it's wavelength. A diagram of the device is shown below:

![](assets/img/portfolio/wec/diagram.png)
The system consists of two rigid boxes connected by a rigid tube. The top of each rigid box has a large orifice covered by a compliant membrane. Because the boxes are sealed by these membranes, the fluid inside the system is closed off from the external environment and thus maintains a constant volume. Inside the tube is a piston that may slide with relatively little and separates the internal system volume into two equal volumes.

The system is submerged in shallow water, and waves propagate from left to right over the system. The boxes are separated such that they are subjected to pressure waves that are out of phase with each other. This results in a periodic pressure differential across both membranes, which causes the the membranes to bulge in and out cyclically, which pushes the piston back and forth through the tube.

The piston has a magnet inside of it, and a solenoid is coiled around the exterior of the tube. Consequently, as the piston-magnet oscillates in the tube, a portion of its kinetic energy is converted electromagnetically to electrical energy.

Some of the main design considerations included box/orifice dimensions, how to seal membrane over orifice, tube diameter, box separations distance, and material selection.
### Fabrication
Acrylic was selected to construct most of the system due to its low cost, water proofness, and ease of laser cutting. Rubber sheet was used as the compliant membrane. A piston was machined out of an acrylic rod. The piston with magnets and a box are shown below.

![](assets/img/portfolio/wec/piston.png)
![](assets/img/portfolio/wec/box.png)
The assembled system is shown below.

![](assets/img/portfolio/wec/assembled.png)
### Data Collection
To test the system, we placed it in a pre-existing water channel with a mechanical rectifier and damper in the Viterbi School of Engineering. We used a phone camera to measure incident wave size, an oscillioscope to measure the voltage output of the device, and a differential pressure sensor to measure the difference in pressure on either side of the piston. Data collection instrumentation and example outputs are shown below.

![](assets/img/portfolio/wec/data-collection.png)
We wrote a script in NI LabVIEW to control our instrumentation and orchestrate data collection. Below is a video of the system in action!

[![wec-test](assets/img/portfolio/wec/wec-test.png)](https://youtu.be/ptgLmCBFp4U?si=9ab0IVuo7szTsavc)
### Data Analysis and Presentation

[poster](assets/img/portfolio/wec/poster.svg)

Here's a picture of my teammates (David and Yifan) and me with our poster!
![](assets/img/portfolio/wec/team.png)



