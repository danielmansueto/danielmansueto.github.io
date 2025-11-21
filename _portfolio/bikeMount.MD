---
title: "Bike Phone Mount"
excerpt: "Top-down modeled rotating phone holder with portrait-landscape lockable mechanism."
thumbnail: '/assets/images/bikeMount/perspective.jpg'
header:
  image: /assets/images/bikeMount/perspective.jpg
---


This project made use of top down modeling in Fusion 360 to design a bike phone mount. In top down modeling, individual components are created withing the context of the full model (in the same file). This allows components to be made according to their relationship to other parts in a model, something very difficult to do when components are located in seperate files. For any assembly, this method also makes editing components, like changing dimensions, much faster as changes can be viewed in the context of the full assembly/use case.

In this project, top down modeling was leveraged to design the bike phone mount around the bike handle bars and phone that would be used. Handlebars and phone were modeled and the assembly was created in the same file around them. Each part of the phone mount were made as individual components designed in relation to one another.


---

# Design Rationale

### Design Philosophy
I aimed to keep the phone mount as small in footprint as possible. I know many bikes have limited room left for phone mounts as grips/handle bar tap and brake/shifting assemblies can take up loads of room on the handlebars. I strived for a small and minimal design. My thinking being with simpler parts and the whole assembly being contained closer to the handlebars, there would be less movement of the assembly from bumps and the phone better contained.

### Rotation Mechanism
I used a detent rotation mechanism to allow the phone to be positioned in both portrait and landscape orientations. A cutout in the base of the phone mount allows for a spring to be inserted pushing against a ball. The part that attaches to the phone slots into the base (in a cyclinder shape) and has cutouts for the spring and ball to push into. Multiple of these cutouts (every 90 degrees) in the cylinder allow for the phone to be rotated. The spring and ball push into the cutouts to secure the position.

### Multiple Materials
It became apparent after my first prototype that multiple materials would be necessary: a rigid one for the base/clamp and a softer/elastic one to hold the phone. This realization mainly changed the phone mount part. I measured my phone with calipers and designed a tight fit with genrous overhangs around the edges to securley grip it. Using 95A TPU allowed for a tight fitting design to still be easy to snap my phone into.

---

# Design Iterations

### First Iteration
My first iteration proved to have many problems, but was a good starting point and one I learened a lot from. As mentioned above, I realized the phone mount should be made of a soft material (I could not get my phone into this iteration). I also learned that my whole assembly was too small. I somehow managed to be able to fit a spring and ball in and have my detent mechanism work. The design of the detent mechanism here proved to be an issue later.


### Second Iteration
My second iteration focused on fixing the phone mount. I designed a new holder to be made out of TPU. This change required me to seperate the phone mount into two seperate pieces: one to be inserted to the base (out of rigid plastic) and the phone holder (out of TPU). I doubled the width of the whole assembly because it looked too narrow to begin with.

I ran into the issue of not being able to assemble my detent mechanism with this iteration. There was no way to insert the rigid part of the phone holder into the base with the spring and ball.

### Third Iteration
To fix the assembly of the detent mechanism, I sliced the detent mechanism into two parts, making the top part a lid so the mechanism could be assembled. This required widening of the body further to allow clearnace for four M3 bolts and heat sinking nuts to be installed so the lid could attach to the base.

I also minorly updated my phone holder to account for my new iPhone 17 Pro's huge camera bump.

---

### Printing Technology and Material Choices
I used filament 3D printing for this project as it allowed for the fastest prototyping and range of materials.

| Part | Printing Technology | Material | Reason |
|------|---------------------|----------|--------|
| Clamp Base | FDM | PETG | Rigid, yet not brittle |
| Clamp Lid | FDM | PETG | Rigid, yet not brittle |
| Phone Mount Base | FDM | PETG | Rigid, yet not brittle |
| Phone Holder | FDM | 95A TPU | Flexible for easy insertion of phone |


---

# Assembly & Use Instructions

### Assembly
1. Heat sink nuts into clamp base, shown below
2. Fit phone mount base into clamp lid and place spring and ball inside
3. Use M3 (8mm) bolts to attach clamp lid +  phone mount base into clamp base.
4. Use M3 (16mm) bolt to secure phone mount base into clamp base.
5. Use M3 bolts and nuts to fit TPU phone holder to phone mount base.

### Use instructions
1. Use M3 bolts and nuts to secure assembly to handlebars
2. Slip phone into holder

---

# Interactive CAD Model

<iframe src="https://a360.co/4rhvgvq"
        width="800" height="600"
        allowfullscreen="true"
        frameborder="0"></iframe>

---

# Figures


---