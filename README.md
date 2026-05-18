# Project Overview
Two-stage reduction gearbox with target ratio 13:1 designed in SOLIDWORKS

Below is the kinematic demonstration of the gearbox, with initial pinion speed of 100rpm
![Kinematics_demo](gearbox_movement_gif.gif)

Below is one of the photos, which demonstrates the exploded view of the gearbox
![Blueprint_demo](./screenshots/v1.png)

Below is one of the blueprints, which demonstrates the technical drawing of lower housing part
![Blueprint_demo](./blueprints/Lower_Housing_Part-1.png)

# Technical Notice
1. Actual bearings were replaced to the simplified bearing placeholders based on standard envelope dimensions
2. Material is assigned for CAD visualization only. Final material selection was not part of this study.
3. Actual ratio of the gearbox is 13.36:1, which gives 2.77% deviation from the target ratio
4. Normal internal clearance, standard precision and concept-level material assumptions were used.
5. Tight-fit for housing fastener bolts was assumed
6. Lubrication assumption: Lithium-EP 2

# BOM (Bills Of Materials)
| Item No. | Part Name | File Name | Qty. | Category | Material / Assumption | Notes |
|---:|---|---|---:|---|---|---|
| 1 | Lower housing part | `lower_part.SLDPRT` | 1 | Custom designed part | Aluminum 6061-T6 / aluminum alloy | Lower half of split gearbox housing |
| 2 | Upper housing part | `upper_part.SLDPRT` | 1 | Custom designed part | Aluminum 6061-T6 / aluminum alloy | Upper half of split gearbox housing |
| 3 | Gear A / input pinion, 17T | `gear_a.SLDPRT` | 1 | Custom gear | C45 steel / AISI 1045 steel | First-stage driving pinion, module 2 |
| 4 | Gear B / first-stage driven gear, 56T | `gear_b.SLDPRT` | 1 | Custom gear | C45 steel / AISI 1045 steel | First-stage driven gear, module 2 |
| 5 | Gear C / second-stage pinion, 18T | `gear_c.SLDPRT` | 1 | Custom gear | C45 steel / AISI 1045 steel | Second-stage driving pinion, module 2 |
| 6 | Gear D / output gear, 73T | `gear_d.SLDPRT` | 1 | Custom gear | C45 steel / AISI 1045 steel | Second-stage output gear, module 2 |
| 7 | Output shaft | `output_shaft.SLDPRT` | 1 | Custom shaft | C45 steel / AISI 1045 steeld | Supports output gear and transmits output torque |
| 8 | Output shaft spacer tube | `output_shaft_stopper_tube.SLDPRT` | 1 | Custom spacer | C45 steel / AISI 1045 steel | Axial positioning component |
| 9 | Third gear shaft spacer tube | `a_gear_shaft_stopper_tube.SLDPRT` | 1 | Custom spacer | C45 steel / AISI 1045 steel | Axial positioning component for intermediate shaft |
| 10 | Bearing placeholder 6004 | `cosmetic_bearing_20-42-12.SLDPRT` | 4 | Simplified standard component | Bearing steel | Standard envelope: 20×42×12 mm, CN |
| 11 | Bearing placeholder 6005 | `cosmetic_bearing_25-47-12.SLDPRT` | 4 | Simplified standard component | Bearing steel | Standard envelope: 25×47×12 mm, CN |
| 12 | Retaining ring for 20 mm shaft, DIN471 | `retaining_ring_1.SLDPRT` | 4 | Simplified standard component | Spring steel | Used for axial retention |
| 13 | Retaining ring for 25 mm shaft, DIN 471 | `retaining_ring_2.SLDPRT` | 2 | Simplified standard component | Spring steel | Used for axial retention |
| 14 | M5 hex head bolt | 7 | Standard hardware | Steel, class 8.8, zinc-plated | Used to fasten upper and lower housing parts |
| 15 | M5 washer | 14 | Standard hardware | Steel, zinc-plated | Optional washer under bolt head |
| 16 | M5 hex nut | 7 | Standard hardware | Steel, class 8.8 / zinc-plated | Required if the lower housing is not threaded |

# Bearings information
The bearing geometry in this project is simplified and used as placeholder geometry for CAD layout purposes.
The selected envelope dimensions correspond approximately to standard deep groove ball bearings:
1. 6004: 20×42×12 mm
2. 6005: 25×47×12 mm

# Gear calculations
Stage 1: 56 / 17 = 3.294
Stage 2: 73 / 18 = 4.056
Total ratio: 3.294 $\cdot$ 4.056 = 13.36:1
Deviation from target 13:1 = +2.77%

# Gears Info
Dimension are specified in mm and deg

Gear A (pinion):
1. No. of Teeth: 17
2. Module: 2
3. Pressure Angle: 20
4. Pitch diameter: 34
5. Outside diameter: 38
6. Root diameter: 29
7. Base diameter: 31.95
8. Face width: 15

Gear B:
1. No. of Teeth: 56
2. Module: 2
3. Pressure Angle: 20
4. Pitch diameter: 112
5. Outside diameter: 116
6. Root diameter: 107
7. Base diameter: 107
8. Face width: 15

Gear C:
1. No. of Teeth: 18
2. Module: 2
3. Pressure Angle: 20
4. Pitch diameter: 36
5. Outside diameter: 40
6. Root diameter: 31
7. Base diameter: 33.825
8. Face width: 15

Gear D:
1. No. of Teeth: 73
2. Module: 2
3. Pressure Angle: 20
4. Pitch diameter: 146
5. Outside diameter: 150
6. Root diameter: 140.98
7. Base diameter: 137.2
8. Face width: 15
