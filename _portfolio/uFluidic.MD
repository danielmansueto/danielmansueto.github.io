---
title: "Pinch Flow Fractionation Micro Fluidic Device"
excerpt: "Microfluidic device for particle sorting using laminar flow and size-dependent displacement."
header:
  image: /assets/images/pffDevice.jpg
  teaser: /assets/images/pffDevice.jpg
gallery:
  - url: /assets/images/pffDevice.jpg
    image_path: /assets/images/pffDevice.jpg
    alt: "Final PFF device"
---

# Introduction

**What is pinch flow fractionation?**  
Pinch flow fractionation (PFF) is a technique allowing for the continuous separation of particles based on size using the laminar flow of particles suspended in liquid through
a designed microchannel geometry. Particles in liquid flow through a pinched section where they are pushed against a wall alongside another stream without particles, forcing smaller 
particles towards the wall and larger ones toward the center of the device. The pinched section opens up to a broad one where the flow expands, we can predict where
particles will flow wihtin the broad section according to the flow profiles defined by equation (1). 

**Applications and advantages**  
PFF is used in a variety of biomedical applications and even in food science. One application of PFF is the seperation of extracellular vesicles (EV) from biological fluids. 
EVs are nanoscale particles secreted by cells that carry proteins, lipids, and nucleic acids. Traditional filtration methods often clog or damage delicate vesicles, but PFF enables 
a gentle and continuous separation wihtout clogging. As described by [Cui et al., *Lab on a Chip* (2025)](https://pubmed.ncbi.nlm.nih.gov/40747581/?utm_source=chatgpt.com), PFF is 
well suited for biocompatible separation of microplastic particles or EVs with minimal sample handling and without requiring external fields. Alternative methods like field flow fractionation (FFF), 
hydrodynamic chromatography (HDC), and capillary hydrodynamic fractionation (CHDF) require external fields like gravitational, centrifugal, electrical, thermal, or cross-flow field. A major 
benefit of PFF is the continuous seperation and lack of external fields needed for use.

---

# Design

![Front of Device](/assets/images/ufluidicImgs/IMG_0011.JPG)

**Symmetric or asymmetric approach**  
My design uses an asymmetric approach.  In traditional PFF devices, the flow field and outlet resistances are uniform across the channel, which can lead to poor resolution and overlap between particle streams. The asymmetric configuration intentionally maintains one fixed pinch wall while allowing the opposite wall to expand asymmetrically into a wider region. This asymmetry, described by Takagi et al. (2005), enhances size-based separation by directing particle trajectories further apart under laminar flow, 
particularly improving resolution for smaller particles. In this design, the pinch section is 0.7 mm wide and expands asymmetrically to a broad section width of 38 mm providing a large field for particle spreading while preserving smooth, stable flow.

My design also 

**Outlet boundary placement**  
The placement of outlets and internal splitter features was determined using the scaling relationship from Yamada’s PFF model,

![Equation](/assets/images/ufluidicImgs/equation.png)

This equation predicts the lateral position of each size band in the broadened region. With a pinch width of 0.7 mm, a broad section of 38 mm, and bead diameters of approximately 0.46 mm (large) 
and 0.14 mm (small), the band centers were calculated to be 25.5 mm and 34.2 mm from the pinch wall, respectively. These points divide the flow into three distinct outlet lanes: a 25 mm-wide 
buffer zone near the pinch wall, a 7.7 mm-wide large-particle window between the noses, and a 3.3 mm-wide small-particle region near the far wall. Each of these regions transitions through tapered 
outlet necks 8 mm for the 1.2 mm buffer outlet and 6 mm for each 0.7 mm particle outlet—followed by short straight segments to ensure undisturbed laminar flow before the channels bend toward their 
outlet posts.

![Device Dimensions](/assets/images/ufluidicImgs/uFluidicDimensions-1.jpg)

**Flow balancing**  
To maintain balanced flow between outlets, the design incorporates hydraulic-resistance matching consistent with the design principles outlined for AsPFF geometries. The buffer channel was designed as the low-resistance “drain,” remaining short and wide so that most of the sheath fluid exits through it. Both particle outlets were made narrower and longer, each with identical serpentine paths to equalize flow resistance and preserve the relative outlet flow fractions. This strategy ensures that the particle lanes carry only the desired fraction of the total flow without distorting the interface position within the broad section. Channel dimensions were confirmed by extruding each lane in CAD, measuring their volumes, and verifying that the two particle outlets had equal volumes (19.237 mm³), confirming identical hydraulic lengths.

**Other Design Notes**
I designed my device with the intention of using rigid pipes instead of the typical flexible tubes used in hopes that the consistency of the rigid tubes would not create any unwanted pressures in the device. 


**How I would Iterate on the Design**
I would elongate the tapers connecting the wide section to the three outlet channels, 
particularly for the buffer outlet. A more gradual contraction can reduce flow resistance 
at the junction, allowing smoother transitions between the separated streams. This
adjustment would minimize pushback from sudden pressure changes, 
helping to  maintain stable separation through the outlet region.


---

# Instructions for Creating a Resin Printed μFluidic Device

![Mold](/assets/images/ufluidicImgs/IMG_0010.JPG)

Resin printing offers an easier and less expensive alternative to manufacturing μFluidic devices compared to traditional manufacturing methods. The steps I took to create my μFluidic device:

1. Designed the mold (negative) of the device in CAD.
2. The mold was printed, rinsed, and post-cured (pictured above).
3. Resin molds are prepped with a coat of parylene to prevent PDMS curing inhibition and adhesion to the resin surface. During casting, unreacted photoinitiators and monomers in the resin can leach into PDMS, blocking crosslinking and leaving a sticky or uncured layer. The parylene coating allows the cured PDMS layer to peel cleanly from the mold without tearing or residue.
4. PDMS is then poured into the mold to create the device.

![Plasma](/assets/images/ufluidicImgs/Plasma-Treating-Image.jpg)


---

# Discussion

**Why resin printing?**  
Resin printing provides high feature resolution (<100 µm) needed for microfluidic channels and is faster and cheaper than traditional manufacturing methods like soft lithography.

**Scaling up**  
To handle a wider range of particle sizes, the device could be scaled by increasing the pinched width and broad section width proportionally.
The design could be scaled up by increasing channel height and flow rate to handle larger sample volumes or particle sizes.

**Lower size limits**  
The smallest separable particle size is limited by Brownian motion and surface roughness of the channel—typically around 1 µm for this printing process. As particle size decreases below ~0.5 µm, Brownian diffusion becomes significant compared to hydrodynamic forces, causing particles to deviate from predictable laminar streamlines. 

In resin printed microfluidic devices, the minimum reliable feature size of roughly 1 mm means smaller geometries cannot be reproduced with sufficient precision to maintain laminar flow and clean pinch alignment. So, while PFF theoretically allows separation of particles down to the sub-micrometer range, the actual limit in this device is set by the 1 mm feature constraint of the resin-printed mold, which restricts how small the pinch region and outlet necks can be fabricated without distortion or blockage.

---

# Testing and Results
Ultimetly, the device was not able to sort the particles correctly. This could be due to a number of issues but a leading thought is that the channel height of the model (1.5mm) contributed to vortexes created in the broad seciton of the device, inhibiting laminar flow.

# Interactive CAD Model

<iframe src="https://a360.co/4hO1J8l" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true" frameborder="0"></iframe>
