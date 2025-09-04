---
title: "Syringe Pump"
excerpt: "DIY syringe pump with customizable flow rate."
header:
  image: assets/images/pumpRender.png
  teaser: assets/images/pumpRender.png
gallery:
  - url: assets/images/Assembly_2025-Aug-31_07-01-34PM-000_CustomizedView1371566399_png.png
    image_path: assets/images/Assembly_2025-Aug-31_07-01-34PM-000_CustomizedView1371566399_png.png
    alt: "syringe pump view 2"
  - url: assets/images/Assembly_2025-Aug-31_07-01-18PM-000_CustomizedView13917699269_png.png
    image_path: assets/images/Assembly_2025-Aug-31_07-01-18PM-000_CustomizedView13917699269_png.png
    alt: "Final syringe pump photo"
  - url: assets/images/Assembly_2025-Aug-31_06-58-15PM-000_CustomizedView25255171325_png.png
    image_path: assets/images/Assembly_2025-Aug-31_06-58-15PM-000_CustomizedView25255171325_png.png
    alt: "Final syringe pump photo"
---

# Purpose & Features

This syringe pump was designed in DF-2100 as a low-cost, 3D-printed alternative to commercial laboratory pumps.  
It provides **precise, repeatable, and non-pulsatile flow** while remaining compatible with different syringe diameters (10 mL–20 mL).  

**Features include:**
* Stepper motor + lead screw drive for accurate plunger motion  
* Arduino-controlled flow rate (mL/min) set via program variables  
* Compatibility with multiple syringe sizes without tools  
* LED indicators: green (running), yellow (paused), red (out of liquid)  
* Latching pushbutton for start/pause and a limit switch for plunger travel  
* Enclosure that integrates electronics and protects against spills  
* Unique branding and snap-fit/fastener assembly (no glue)

# Final Design

![Final assembly](assets/images/finalPump.png)

# Off-the-Shelf Parts

| Component            | Specification                     | Quantity | Est. Cost (USD) |
|----------------------|-----------------------------------|---------:|----------------:|
| Arduino Uno R3       | Microcontroller board             | 1        | $25.00 |
| NEMA 17 Stepper Motor| 1.8° step angle, 1.5A             | 1        | $15.00 |
| A4988 Stepper Driver | Microstepping driver module       | 1        | $8.00 |
| Lead Screw           | 8 mm diameter, 2 mm pitch, 300 mm | 1        | $12.00 |
| Linear Bearings      | LM8UU 8 mm bearings               | 2        | $6.00 |
| Smooth Rods          | 8 mm diameter, 300 mm length      | 2        | $10.00 |
| Limit Switch         | Micro switch with lever           | 1        | $2.00 |
| Push Buttons         | Momentary tactile switches        | 3        | $3.00 |
| RGB LEDs             | Common cathode, 5 mm              | 3        | $2.00 |
| Power Supply         | 12 V, 2 A adapter                 | 1        | $10.00 |
| Flexible Coupling    | 5 mm to 8 mm shaft coupler        | 1        | $5.00 |
| Misc. Hardware       | Screws, nuts, wires, resistors    | –        | $8.00 |
| **Total**            | —                                 | —        | **$106.00** |

# 3D-Printed Parts

| Part Name               | Description                          | Material |
|--------------------------|--------------------------------------|----------|
| Motor Mount             | Bracket holding NEMA 17 stepper motor | ABS |
| Lead Nut Housing        | Holds brass lead screw nut | ABS |
| Syringe Holder          | Clamp mechanism for 10/20 mL syringes | PLA |
| Plunger Pusher          | Connects lead screw to syringe plunger | PLA |
| Linear Bearing Blocks ×2| Houses LM8UU bearings                | PLA |
| Rod Support Brackets ×4 | End supports for smooth rods         | PLA |
| Base Plate              | Mounting platform for rods & brackets | PLA |
| Electronics Enclosure   | Protects Arduino/driver; avoid warping | PLA |
| Limit Switch Mount      | Adjustable bracket for end stop      | PLA |
| Cable Management Clips  | Wire routing and organization        | PLA |
| Branding Features       | Logos, labels, aesthetic elements    | PLA |
| **Total**               | ~250 g PLA + ~50 g ABS               | — |

# Arduino Code

The Arduino control program is available here:  
👉 [View the code on GitHub](https://github.com/danielmansueto/danielmansueto.github.io/blob/main/assets/SyringeArduinoCode)

# Interactive CAD Model

<iframe src="https://a360.co/4ndD7XO" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true" frameborder="0"></iframe>

{% include gallery caption="Syringe Pump Gallery" %}

# Operation

1. **Insert syringe** into the holder and secure with the clamp.  
2. **Power on** using the external AC-DC supply.  
3. **Press the latching button** to start or pause the pump.  
4. The LED indicates status:  
   * Green = running  
   * Yellow = paused  
   * Red = empty (limit switch triggered)  
5. Flow rate is controlled in the Arduino sketch by adjusting the syringe diameter variable and the target flow rate (mL/min).  
6. To stop, press the button or disconnect power.  
7. Always ensure wiring and electronics remain dry and protected during use.

