---
title: Hard Tech for Climate
subtitle: Overview of my work at three sustainability-oriented hard tech startups in NYC
[//]: # image: assets/img/portfolio/02-full.jpg
[//]: # alt: Keep Exploring

caption:
  title: Hard Tech for Climate
  subtitle: sustainability-oriented hard tech startups in NYC
  thumbnail: assets/img/portfolio/startups/thumbnail-startups.png
---
I've worked at three early-stage climate tech companies since moving to NYC at the beginning of 2023: **Edge Foods**, **CarbonBridge**, and **TômTex**.
### CarbonBridge, Mechanical Engineer
[CarbonBridge](https://carbonbridge.io/) is a pre-seed startup currently headquartered at the [HAX space in Newark](https://hax.co/). CarbonBridge converts methane waste gas to liquid methanol fuel via direct-gas bacterial fermentation.

My responsibilities as a mechanical engineer included bioreactor design, fluid control, temperature control, downstream process design, scaling planning, and miscellaneous engineering and experimentation support tasks. Show below left is an off-the shelf membrane filter holder I selected as an early bioreactor for CarbonBridge's methanol producing bacteria. Below right is this filter holder in a fluid control circuit with a syringe pump programmed to deliver gas and liquid at predtermined intervals. This system allowed the biology team to run experiments quickly and repeatedly, and produced significantly higher titers of methanol than were previously produced.

![](assets/img/portfolio/startups/small-reactor.png)

The above reactor has a diameter of about 5cm. Once its successful use was demonstrated, I designed and manufactured an 8in diameter version, shown below alone and attached to its fluid control circuit. The fluid control was performed by a peristaltic pump and an Arduino microcontroller. In part due to the success of this system, CarbonBridge was selected for a [Greenwells grant by ARPA-E](https://www.linkedin.com/posts/carbonbridge_arpaegreenwells-decarbonize-methanol-activity-7226101649805635585-ts0E?utm_source=share&utm_medium=member_desktop).

![](assets/img/portfolio/startups/big-reactor.png)

#### Temperature Control System for Bacteria Incubators
Additionally, I built a temperature feedback control system for three bacteria incubators, shown below. Each control system consisted of heated blanket wrapped around the incubator, a thermocouple sensor to measure incubator temperature, a relay to switch on/off power to a blanket, and a programmable PID controller to control the relay.

![](assets/img/portfolio/startups/temp-control.png)

### Edge Foods, Lead Biomechanical Engineer
Edge Foods was an early stage food tech startup that produced growth factors for lab grown meat using genetically engineered mammalian cells. As Lead Biomechanical Engineer, I led bioreactor design, downstream process design, technoeconomic analysis of our product, and scaling plans. I also assisted with the biology and cell caretaking, but I wasn't as good at that.

#### Electrostatic Bead Generator
[This video](https://drive.google.com/file/d/1kzXjkDQjnFX54C98xueHYXS3qzKWPLHM/view?usp=drive_link) demonstrates the functioning of an electrostatic bead generator I designed and assembled. The system dropped droplets of sodium alginate out of a syringe into a bath of calcium chloride. When the sodium alginate contacts the calcium chloride it congeals into a solid gel almost instantly. The size of the beads could be modulated by adjusting the voltage applied between the bath and the syringe, which created an electric force on the beads that pulled them off the syringe tip.

By suspending cells in the sodium alginate before it is extruded in the bath, cells could be encapsulate by the gel beads. This allows the cells to survive higher shear stresses in a stirred bioreactor while still allowing nutrient transport into the bead and waste transport out.

#### Bioreactor Design
At lab scale, we used a simple shaken bioreactor geometry. By integrating sensors I developed a cost effective bioreactor that collected pH and dissolved oxygen data in real time and used these readings to control an automated feeding mechanism. 

#### Suspension and serum-free adaptation of mammalian cell clumps
By default, most mammalian cells require a surface to adhere to supplementation with fetal bovine serum - a cell culture supplement that is highly popular but has questionable cost and ethics. Together with the biology team, I successfully adapted adherent mammalian cells (HEK cells and CHO cells) to be serum-free and suspended in clumps. This adaptation enables ethical, affordable scaling of our process in suspension bioreactors.

### TômTex, Process Engineer
TômTex is a biomaterials startup that makes a sustainable leather alternative out of shrimp shells. Below is an example of the leather material (which I did not make). After the sheets of raw leather are produced they require several downstream processing steps, mostly consisting of chemical soaks. As a process engineer, I design and assemble hardware systems for the automation and scale up of these chemical processing steps.

![](assets/img/portfolio/startups/wallet.png)

My primary project has been to design and build a 50+ gallon automated chemical bath to treat rolls of leather. The system consists of one main drum with a roll of leather placed inside it vertically, 4 drums of treatment chemicals (acid, base, etc), and mechanics+electronics+controls to automatically fill and drain the main barrel in the correct sequence.

The project is ongoing - most of the design is complete and early assembly has begun. The model below shows the approximate layout of the hydraulics, electronics, and chemical drums.

![](assets/img/portfolio/startups/layout.png)

Below the partially assembled tubing, valves, pumps, and frame are shown.

![](assets/img/portfolio/startups/progress.png)
