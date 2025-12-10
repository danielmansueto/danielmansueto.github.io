---
title: "Generative Design Chair"
excerpt: "Chair created using Fusion 360 Generative Design"
thumbnail: '/assets/images/chair/chairAngled.png'
header:
  image: '/assets/images/chair/chairAngled.png'
  teaser: assets/images/chair/chairAngled.png
galleryTop:
  - url: /assets/images/chair/chairAngleFront.png
    image_path: /assets/images/chair/chairAngleFront.png
    alt: "front angle"
  - url: /assets/images/chair/chairSide.png
    image_path: /assets/images/chair/chairSide.png
    alt: "side angle"
  - url: /assets/images/chair/chairBackAngle.png
    image_path: /assets/images/chair/chairBackAngle.png
    alt: "back angle"
  - url: /assets/images/chair/chairBack.png
    image_path: /assets/images/chair/chairBack.png
    alt: "back"  
  - url: /assets/images/chair/chairFront.png
    image_path: /assets/images/chair/chairFront.png
    alt: "front"
  - url: /assets/images/chair/chairTop.png
    image_path: /assets/images/chair/chairTop.png
    alt: "Top"
galleryBottom:
  - url: /assets/images/chair/IMG_0528.JPG
    image_path: /assets/images/chair/IMG_0528.JPG
    alt: "powder"
  - url: /assets/images/chair/IMG_0535.JPG
    image_path: /assets/images/chair/IMG_0535.JPG
    alt: "raw"
  - url: /assets/images/chair/IMG_0564.JPG
    image_path: /assets/images/chair/IMG_0564.JPG
    alt: "back angle"
  - url: /assets/images/chair/IMG_0556.JPG
    image_path: /assets/images/chair/IMG_0556.JPG
    alt: "side"  
  - url: /assets/images/chair/IMG_0561.JPG
    image_path: /assets/images/chair/IMG_0561.JPG
    alt: "other side"     
  - url: /assets/images/chair/IMG_0562.JPG
    image_path: /assets/images/chair/IMG_0562.JPG
    alt: "back"     
  - url: /assets/images/chair/IMG_0565.JPG
    image_path: /assets/images/chair/IMG_0565.JPG
    alt: "close"     
  - url: /assets/images/chair/IMG_0566.JPG
    image_path: /assets/images/chair/IMG_0566.JPG
    alt: "closer"  
---

This project explores the intersection of generative design and powder bed fusion through the creation of a lightweight, high-stiffness chair frame. Generative design utilizes algorithms to explore solutions to a defined set of criteria. 

Using Fusion 360's Generative Design feature, I defined preserve geometries, areas to be kept in the design, obstacle geometries, areas where material should not be generated, and provided the the direction and magnitudes of forces applied to the preserve geometries.

The outcomes of generative design modeling are often organic looking stuctures that would be very difficult or impossible to create using traditional methods of manufacturing. Powder bed fusion works especially well to create these organic, irregular geometries from generative design because it does not require any support material and can print parts in any orientation.

{% include gallery gallery=page.galleryTop caption="Fusion 360 Renders" class="gallery-two-col" %}

## Generative Design Example for Part Consolidation


Nasa used Generative Design in its EXoplanet Climate Infrared TElescope (EXCITE) that studies exoplanets orbiting distant stars. The telescope is the size of a car and contains two generatively designed parts: a titanium scaffold and a "optical bench" that holds a variety of optical instruments. The optical bench design is drastically different from others of its kind and is superior structrually and consolidated a mechanism that is usually ten parts into one. 


---

# Load Cases and Boundary Conditions

![loads](/assets/images/chair/loads.png)

Applying proper load cases was essential to ensuring that the generative chair works structurally. Generative design is highly sensitive to the location of applied forces and to the placement of structural constraints, so careful reasoning was necessary.

### Determining Forces  
To determine appropriate loads for a chair, I used approximate values based on human interaction:
- **Vertical load on the seat:** 3600 ounceforce* (200 lbs) on all four seat posts, representing a seated person  
- **Backrest load:** 1600 ounceforce* (100 lbs) horizontal (inclined 20 degree up) load to account for leaning  

*Safety factor of 2 was used.

These values produce realistic stress conditions that guide the generative tool toward functional results.

### Placement of Structural Constraints  
The chair’s structural constraints are applied at the floor contact points because this is where the frame transfers load into the ground. These locations act as the fixed supports for the system: they represent the points that cannot move, rotate, or deflect under load.  In a real chair, the legs are the only elements that anchor the structure, so constraining the floor surfaces accurately captures how forces travel from the seat, through the frame, and into the ground. By fixing the legs at the floor plane, the generative design algorithm produces a topology that reflects realistic load paths and seating behavior.


### Obstacle Geometry

The obstacle geometry ended up shaping the design the most. Throughout my process, I kept adding more obstacles, reducing the area where material could be generated. This helped give me a level of control over the generated designs and shape the chair to my liking.

![obstacle](/assets/images/chair/obstacle.png)

Obstacles filled the area above the seat, where one would sit as well as below the seat/between the four legs. A ground was added so the chair would rest flat on the ground.

![obstacle2](/assets/images/chair/obstacle1.png)

Later on, I added walls all around the the preserve geometry to constrain the chair to a smaller footprint.

---

# Comparison: Different Material Outcomes

![outcomes](/assets/images/chair/outcomes.png)

I generated a few different material outcomes: nylon PA12 (top left), aluminum ALSi10Mg (bottom left), Titanium 6AI-4V (top right), and Galvanized Steel (bottom right).

As seen from the image above, all the outcomes are relatively similar. I believe this is because Generative Design is stiffness driven, not strength driven. Given the same load cases and preserve geometeries, the optimal path is the same regardless of material. The material strenght would then have more effect on thickness of the optimal path. From the generated results above, the nylon has a slightly higher concentration of material between the front and back legs of the chair, compared to the metal results.

*Note this is not the final generated design I used. I unfortunetly generated more designs after the final one, and the rest of the outcomes from the final design were not saved. However, the range of outcomes were similar to the picture above.

---

# Pros and Cons of Generative Design

### Usefulness
- Consolidating assemblies, reducing part count  
- Helps discover non-intuitive, high-performance structures  
- Integrates naturally with additive manufacturing  

### Drawbacks
- Produces shapes that are difficult to manufacture without additive processes  
- Can require extensive post-processing or redesign for real-world constraints  
- Results can be “over-optimized” and lose practicality  
- Computationally intensive and time-consuming  

### Best Applications
I think the best applications of generative design are when mass reduction/lightweighting is the goal or necessary or when complex assembles can be consolidated and made simpler. 

For more aesthetic purposes, it can create cool designs you may otherwise not think of, but generally I found myself frustrated with the designs it generated and kept adding obstacle geometry to force the designs to try and look a certain way. This is obviously not its best use case as there is no real world inspiration or story behind the designs. It is purely utilitarian, maximixing stiffness and mimizing material.

For furniture design, it brings a unique aesthetic and performance-driven rationale but may require significant adjustment for ergonomics, comfort, and cost.

---

# CAD Model  
<iframe src="https://a360.co/4rFdX7v"  
width="800" height="600" allowfullscreen frameborder="0"></iframe>

---

# Powder Printed Model Photos

{% include gallery gallery=page.galleryBottom caption="pSLS printed model straight out of printer, cleaned, and model photos after spray painting." class="gallery-two-col" %}