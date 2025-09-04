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
It provides **precise and repeatable flow** while remaining compatible with different syringe diameters (10 mL–20 mL).  

**Features include:**
* Stepper motor + lead screw drive for accurate plunger motion  
* Arduino-controlled flow rate (mL/min) set via program variables  
* Compatibility with multiple syringe sizes without tools  
* LED indicators: green (running), yellow (paused), red (out of liquid)  
* Latching push button for start/pause and a limit switch for plunger travel  
* Enclosure that integrates electronics and protects against spills   

# Final Design

![Final assembly](/assets/images/finalPump.png)

# Off-the-Shelf Parts

| Component                        | Specification / Notes                                | Quantity |
|----------------------------------|------------------------------------------------------|---------:|
| Lead screw (250 mm, 2 mm lead)   | Provided                                             | 1 |
| Lead screw (250 mm, 8 mm lead)   | Provided                                             | 1 |
| Flexible coupling                | 1/4" × 8 mm                                          | 1 |
| Linear rods                      | 200 mm length, 8 mm Ø                                | 2 |
| Linear bearings                  | LM8UU for 8 mm rods                                  | 2 |
| Aluminum extrusion               | 2040 profile, 1' length                              | 1 |
| Stepper motor                    | NEMA 17                                              | 1 |
| Power supply                     | MEAN WELL RQ-65D AC-DC, quad output (5V, 12V, 24V)   | 1 |
| Arduino Uno                      | R3 board                                             | 1 |
| Stepper driver                    | A4988                                               | 1 |
| Breadboard                       | Small prototyping board                              | 1 |
| Latching push button             | Panel mount, on/off                                  | 1 |
| Limit switch                     | Mechanical, lever-actuated                           | 1 |
| RGB LED                          | Common cathode                                       | 1 |
| Miscellaneous hardware           | Wires, fasteners, resistors, heat shrink             | — |

# 3D-Printed Parts

### 3D-Printed Parts

| Part Name                 | Description                                      | Material |
|----------------------------|--------------------------------------------------|----------|
| Enclosure                  | Main housing for Arduino and driver electronics  | PLA |
| Enclosure Lid              | Cover for electronics enclosure                  | PLA |
| End Support                | Standard support for smooth rods and lead screw  | PLA |
| End Support (Motor Mount)  | Support with integrated motor mounting plate      | ABS |
| Modified End Supports ×2   | End supports adapted to hold syringe body         | PLA |
| Carriage                   | Sliding carriage that holds syringe plunger       | PLA |

# Arduino Code

The Arduino control program is available here:  
👉 [View the code on GitHub](https://github.com/danielmansueto/danielmansueto.github.io/blob/main/assets/SyringeArduinoCode)

# Interactive CAD Model

<iframe src="https://a360.co/4ndD7XO" width="800" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true" frameborder="0"></iframe>

{% include gallery caption="Syringe Pump Gallery" %}

# Operation

1. **Insert syringe** into the holder.
2. **Power on** power supply.  
3. **Press the latching button** to start or pause the pump.  
4. The LED indicates status:  
   * Green = running  
   * Yellow = paused  
   * Red = empty (limit switch triggered)  
5. Flow rate is controlled in the Arduino code by adjusting the flow rate (mL/min) variable.  
6. To stop, press the button or disconnect power.  

