---
title: "Syringe Pump"
excerpt: "DIY syringe pump with customizable flow rate."
header:
  image: assets/images/pumpRender.png
  teaser: assets/images/pumpRender.png
gallery:
  - url: assets/images/pumpRender.png
    image_path: assets/images/pumpRender.png
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

![Final assembly](/assets/images/pumpRender.png)

# Off-the-Shelf Parts

| Part                                   | Qty | Notes / Source |
|----------------------------------------|----:|----------------|
| 250 mm lead screw (2 mm or 8 mm lead)  | 1  | Supplied  [oai_citation:0‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| 1/4" × 8 mm flexible coupling          | 1  | Supplied  [oai_citation:1‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| 200 mm linear rod (8 mm Ø)             | 2  | Supplied  [oai_citation:2‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| LM8UU linear bearing                   | 2  | Supplied  [oai_citation:3‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| 2040 aluminum extrusion (1’ length)    | 1  | Supplied  [oai_citation:4‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| NEMA 17 stepper motor                  | 1  | Supplied  [oai_citation:5‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| MEAN WELL RQ-65D AC-DC power supply    | 1  | Quad output (5V/12V/24V)  [oai_citation:6‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| Arduino Uno                            | 1  | Supplied  [oai_citation:7‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| A4988 stepper driver                   | 1  | Supplied  [oai_citation:8‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| Small breadboard                       | 1  | Supplied  [oai_citation:9‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| Panel-mount latching pushbutton        | 1  | Start/pause  [oai_citation:10‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| Limit switch                           | 1  | End-of-stroke stop  [oai_citation:11‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| RGB common-cathode LED                 | 1  | Green/Yellow/Red status  [oai_citation:12‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| Wires, resistors, fasteners, heat shrink | — | Supplied  [oai_citation:13‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |

# 3D-Printed Parts

| Part                      | Qty | Material | Notes |
|---------------------------|----:|----------|-------|
| Motor mount / bracket     | 1  | ABS      | Required for heat near motor  [oai_citation:14‡Syringe-Pump-Project-Final-V6 (1).pdf](file-service://file-1knZUnuktbGRaCvCSv6xuv) |
| Carriage with syringe holder | 1 | PLA     | Holds syringe plunger; includes linear bearings |
| Electronics enclosure     | 1  | PLA/ABS  | Protects Arduino, driver, wiring from liquid |
| Base brackets / supports  | 2+ | PLA      | Attach extrusion and rods together |
| Syringe clamp / clip      | 1  | TPU/PLA  | Flexible, tool-free syringe loading |
| Branding features (logo, label) | optional | PLA | Unique design requirement |

# Arduino Code

The Arduino control program is available here:  
👉 [View the code on GitHub](https://github.com/danielmansueto/danielmansueto.github.io/assets/SyringeArduinoCode)

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

