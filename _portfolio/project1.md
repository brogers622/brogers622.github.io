---
title: Hard Tech for Climate
subtitle: Overview of my work at four sustainability-oriented hard tech startups in NYC
[//]: # image: assets/img/portfolio/02-full.jpg
[//]: # alt: Keep Exploring

caption:
  title: Hard Tech for Climate
  subtitle: sustainability-oriented hard tech startups in NYC
  thumbnail: assets/img/portfolio/startups/thumbnail-startups.png
---
I've worked at four early-stage climate tech companies since moving to NYC in 2023: **Edge Foods**, **CarbonBridge**, **TômTex**, and **SIMULATE®**.
### SIMULATE | Mechanical Engineering Lead
After its successful launch of Nuggs, [Simulate](https://simulate.com/) embarked on a new R&D mission to develop a whole plant-based chicken breast product via fiber spinning. The product, pictured below, is made of [wet spun](https://en.wikipedia.org/wiki/Spinning_(polymers)) soy protein - an unusual process that marries the food and textile industries. I joined the team as Mechanical Engineering Lead to improve and scale this process.

![](assets/img/portfolio/startups/chicken.PNG)
Our core process was continuous fiber handling, which at a high level consisted of extrusion, in line fiber conditioning, and finally collection. The media below show several unit processes executed by machines that I was responsible to procure off the shelf or design+assemble in house.
Our soy protein solution is extruded through a spinneret into coagulation bath to make fibers. At this point the process transforms from continuous fluid handling to continuous solid fiber handling. 
![](assets/img/portfolio/startups/fiber-extrusion.gif)

Fibers are washed, then excess water is pressed out.
![](assets/img/portfolio/startups/press-roller.gif)

Conditioning of fibers by heated roller
![](assets/img/portfolio/startups/heated-godet.gif)

Fibers are coated; this coating is later cured to emulate the connective tissue among muscle fibers in a real chicken breast.
![](assets/img/portfolio/startups/emulsion-application.gif)

Several process variables required tight control to achieve product consistency, such as coagulation bath pH and extrusion mass flow rate. To attain process consistency and legibility, I took the lead on controls+data collection.

I used an ESP32, shown below with other process elctronics in a housing, to log data and control the process. I felt an ESP32 would be more appropriate than a PLC due to cost, non-proprietary flexibility, and relatively low need for IO pins and processing power at our scale.

![](assets/img/portfolio/startups/junction-box.jpg)

Autonomous+remote data collection was established in 3 steps:
1 - In line sensors (pH, conductivity, mass flow, pressure) take a measurement and transmit it via wired digital or analog signal to the ESP32
2 - ESP32 transmits the data via WiFi to our Google Drive
3 - The data is plotted live in a dashboard for real-time process monitoring.
The gif below shows an off-line demo of live data collection.
![](assets/img/portfolio/startups/dashboard-demo.gif)
### CarbonBridge | Mechanical Engineer
At the time of my employment, [CarbonBridge](https://carbonbridge.io/) was a pre-seed startup based in the [HAX space in Newark](https://hax.co/). CarbonBridge converts methane waste gas to liquid methanol fuel via direct-gas bacterial fermentation.

My responsibilities as a mechanical engineer included bioreactor design, fluid control, temperature control, downstream process design, scaling planning, and miscellaneous engineering and experimentation support tasks. Shown below left is an off-the shelf membrane filter holder I selected as an early bioreactor for CarbonBridge's methanol producing bacteria. Below right is this filter holder in a fluid control circuit with a syringe pump programmed to deliver gas and liquid at predetermined intervals. This system allowed the biology team to run experiments quickly and repeatedably, and produced significantly higher titers of methanol than were previously produced.

![](assets/img/portfolio/startups/small-reactor.png)
The above reactor has a diameter of about 5cm. Once its successful use was demonstrated, I designed and manufactured an 8in diameter version, shown below alone and attached to its fluid control circuit. The fluid control was performed by a peristaltic pump and an Arduino microcontroller. In part due to the success of this system, CarbonBridge was selected for a [Greenwells grant by ARPA-E](https://www.linkedin.com/posts/carbonbridge_arpaegreenwells-decarbonize-methanol-activity-7226101649805635585-ts0E?utm_source=share&utm_medium=member_desktop).

![](assets/img/portfolio/startups/big-reactor.png)
##### Temperature Control System for Bacteria Incubators
I built a temperature feedback control system for three bacteria incubators, shown below. Each control system consisted of a heated blanket wrapped around the incubator, a thermocouple sensor to measure incubator temperature, a relay to switch on/off power to the blanket, and a programmable PID controller to control the relay.

![](assets/img/portfolio/startups/temp-control.png)
### Edge Foods | Lead Biomechanical Engineer
Edge Foods was an early stage food tech startup that produced growth factors for lab grown meat using genetically engineered mammalian cells. As Lead Biomechanical Engineer, I led bioreactor design, downstream process design, technoeconomic analysis of our product, and scaling planning. I also assisted with the biology and cell caretaking.

##### Electrostatic Bead Generator
The video below demonstrates an electrostatic bead generator I designed and assembled. The system extruded droplets of sodium alginate out of a syringe into a bath of calcium chloride using a syringe pump. Upon contact with the bath, Ca ions cause the sodium alginate to rapidly gel. A voltage applied between the syringe and bath creates an electric force that pulls the beads off the syringe tip. This voltage could be  modulated to control bead size.

By suspending cells in the sodium alginate before extrusion, cells could be encapsulated by the gel beads. This allowed the cells to survive higher shear stresses in a stirred bioreactor while still allowing nutrient transport into and waste transport out of the permeable bead.

[![](assets/img/portfolio/startups/electrostatic.png)](https://youtu.be/DudUC4S9mcY?si=iVcPpXFxJVsZcAIo)
##### Bioreactor Design
At lab scale, we used a simple shaken 'bioreactor'. By integrating sensors I developed a cost effective growth system that collected pH and dissolved oxygen data in real time and used these readings to control an automated feeding mechanism. 

![](assets/img/portfolio/startups/edge-reactor.png)
##### Suspension and serum-free adaptation of mammalian cell clumps
By default, most mammalian cells require a surface to adhere to and supplementation with fetal bovine serum - a cell culture supplement that is highly popular but has questionable cost and ethics. Together with the biology team, I successfully adapted adherent mammalian cells (HEK cells and CHO cells) to be serum-free and suspended in clumps. This adaptation enabled ethical, affordable scaling of our process in suspension bioreactors.

### TômTex | Process Engineer
TômTex is a biomaterials startup that makes a sustainable leather alternative out of shrimp shells. Below is an example of the leather material. After the sheets of raw leather are produced they require several downstream processing steps, mostly consisting of chemical soaks. As a process engineer, I designed and assembled hardware systems for the automation and scale up of these chemical processing steps.

![](assets/img/portfolio/startups/wallet.png)
My primary project was to design and build a 50+ gallon automated chemical bath to treat rolls of leather. The system consists of one main drum with a roll of leather placed inside it vertically, 4 drums of treatment chemicals (acid, base, etc), and mechanics+electronics+controls to automatically fill and drain the main barrel in the correct sequence. Below are a 3D sketch of the finished system and two photos plumbing assembly.

![](assets/img/portfolio/startups/layout.png)

![](assets/img/portfolio/startups/progress.png)