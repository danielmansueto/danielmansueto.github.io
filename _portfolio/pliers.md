---
title: "Multi Material Pliers"
excerpt: "Pliers made of TPU and PLA."
header:
  image: '/assets/images/pliers/sideView.jpg'
  teaser: /assets/images/pliers/sideView.jpg
gallery:
  - url: /assets/images/pliers/sideView.jpg
    image_path: /assets/images/pliers/sideView.jpg
    alt: "Iteration 1"
---

# Multi Material Pliers Project

**Goal:** Design and fabricate pliers that can grip through-hole resistors reliably. Pliers return to the open position via a flexible spring made of 95A TPU. 

**Format:** Multi Material (rigid and elastic filament) 3D printed parts to create pliers through print-in-place or 3-part hand-press assembly (2 rigid handles + 1 elastic spring) that can be pieced together without tools.


---

# What is Print-in-Place?
A print-in-place model is a 3D printed model made up of seperate parts that interact mechanically that can be prrinted in one continuous print. Moving and interlocking parts in print-in-place models are designed with clearances that allow the model to function as a whole without any post processing. Print-in-place models can be combined with multi material printing to combnine flexible hinges and joints with rigid frames.

A major benefit to print-in-place is the simplicity of assembly (or lack of assembly at all) and not having to deal with exterior fasteners. They also 

However, print-in-place can make 3D printing a bit more complicated due to the tight tolerances it requires. It is easy to ruin the functionality of print-in-place models from overextrusion or dimensional inaccuracies. 

## Applications of Print-in-Place
Most print-in-place models online lend themselves to toy or fidget like designs, such as spring loaded boxes or fidget cubes. This project provides a bit more of a functional angle to the print-in-place technique.

## Multi Material and Print-in-Place 
A combination of different materials makes lots of sense for print-in-place designs as different material properities can help determine final mechanical movements of a print-in-place model. Rigid plastics like PLA and ABS can be used for the body or frame for the structure of a part while flexible plastics like TPU can serve as joints or hinges for movement. 


---

# Design
I found inspiration for my design online as well as from in-class examples shown to us that combined rigid and flexible components. 

Online Inspiration:
![inspiration](/assets/images/pliers/onlinePlier.avif)
https://all3dp.com/3d-printed-flexible-pliers/#google_vignette

The central spring is a flexible joint of TPU that connects handles and jaws made out of rigid PLA. The TPU joint was printed with a grid infill pattern and no top or bottom walls to flex under compression and return to its neutral position when released. The joint is connected to the handles/jaws by dovetail-like joinery that allow for easy assembly and a secure fit during use.

Early iterations in CAD focused on refining the geometry of the dovetail joinery, specifically the number, spacing, and angle of dovetails. I started with classic dovetail geometry and later shifted to a more squared off version. 

I had to print the flexible joint and jaws twice and the handles three times to dial in the correct fitment of the joinery and flexibility. 


## First Iteration
I started my prototyping process using a 0.25mm offset around the dovetail joinery to allow for clearance so the parts could fit together easily. This turned out to be too much and the handles and jaws were not secured to the joint.

The first iteration of the TPU joint used a 23% infill from Superslicer. Though the handles were not secure, I could tell it was a bit stiff and felt a little difficult to actuate.

The height of the pliers was 10mm and this felt appropriate for picking up resistors, which are very small. Any taller and I think the difficulty of picking up the resistors would greatly increase.

## Second Iteration
Removing the clearance offset proved to provide a secure fit between the TPU joint and  handles and jaws. I lessened the infill percetage of the TPU joint to 18% and this felt much better. With the jaws having full range of movement now, I could see one further problem: the inside corners of the handles were colliding with each other before the tips of the jaws, slightly restricting the range of movement

![infill](/assets/images/pliers/jointSlicer.png)
23% infill shown on left and 18% infill shown on right


## Third Iteration
To correct the range of movement from the second iteration, I cut back the corners of the handles to allow for more travel. The pliers now fully close.


---

# Specifications

| Feature | Size | Notes |
|---|---:|---|
| **Jaw length** | 43.5 mm | From top of flex joint to end of jaw
| **Jaw capacity (max opening at tips)** | 15mm  | 17.4mm in CAD model
| **Plier Height** | 10mm | 

---


# Print Settings

**Rigid handles (PLA)**  
- Layer height: **0.20 mm**  
- Walls: 3 layers; Top/Bottom: 4 layers
- Infill: **15%** grid/gyroid (stiffness over weight)  

**Joint TPU 95A**  
- Layer height: **0.20–0.24 mm**  
- Perimeter Walls: **3**; 
- No top/bottom layers
- Infill: 18% (consistent spring)  
- Infill pattern: grid
- 0.4mm nozzle

---

# Testing


---


# Gallery

![WIP 1](/assets/images/pliers/topDown.jpg)
![WIP 2](/assets/images/pliers/sideView.jpg)

---

# References & Assignment

- CHBE 4200 — **GitHub Project #2: Print-in-Place Pliers** (assignment PDF).  [oai_citation:6‡Github2-MultiMaterial-Pliers.pdf](sediment://file_00000000cb44722fbb4713bcea7db672)
- All3DP: *3D-Printed Flexible Pliers* — background inspiration. <https://all3dp.com/3d-printed-flexible-pliers/>