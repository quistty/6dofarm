# Joint 5 and Joint 6: First CAD Rendition Review

## 1. Design Overview

Joint 5 and Joint 6 were designed as a combined wrist module using two connected pulley systems.

The assembly consisted of two main components:

- A Joint 5 housing, which supported the entire Joint 5 and Joint 6 assembly
- A Joint 6 housing, which rotated inside the Joint 5 housing

The Joint 5 housing acted as the main structural support for the wrist and contained the routing paths for both pulley systems.

The complete Joint 5 and Joint 6 module was intended to rotate relative to the rest of the robotic arm through bearings positioned on both sides of the Joint 5 housing.

One side of each bearing was connected to the Joint 5 housing, while the other side was connected to the supporting structure of the rest of the wrist or arm module.

This bearing arrangement allowed the complete wrist assembly to rotate without the housing rubbing directly against the surrounding structure.

---

## 2. Differential Pulley System

The movement of Joint 5 and Joint 6 was controlled using two pulley systems positioned on the left and right sides of the Joint 5 housing.

The intended movement depended on the relative direction of the two pulley systems:

- When both pulley systems moved in the same direction, the complete Joint 5 and Joint 6 housing rotated together.
- When the pulley systems moved in opposite directions, the Joint 5 housing remained stationary while Joint 6 rotated.

The two pulley inputs therefore worked together as a differential mechanism.

Depending on their relative direction of rotation, their motion either combined to rotate the complete wrist assembly or opposed each other at Joint 5 while producing rotation at Joint 6.

The pulley-driving motors and reduction systems were positioned farther back in the robot rather than directly on the wrist.

This reduced the amount of motor mass located at the end of the arm.

Each pulley system included both a gearbox reduction and an additional pulley reduction to produce the required torque and make the system easier to package within the robot.

---

## 3. Joint 6 Support and Bearing Arrangement

The Joint 6 housing was designed to attach to the Joint 5 housing while remaining free to rotate.

The two housings were not intended to slide directly against each other.

Instead, Joint 6 was supported by bearings located between the two housings.

Bolts held the surrounding covers and structural components together, but the rotating surfaces were intended to contact each other only through the bearings.

This allowed the Joint 6 housing to rotate relative to Joint 5 while minimizing friction.

The bearings carried the radial and structural loads, while the bolts maintained the alignment and assembly of the surrounding parts.

---

## 4. Pulley and Belt Routing

Each pulley system entered the Joint 5 housing from below.

Considering one side of the system, the belt travelled through the bottom of the Joint 5 housing and continued toward the centre of the wrist.

The belt then connected to one end of the semicircular Joint 6 drive path.

Idler pulleys routed the belt around the outer edge of the semicircular section so that belt tension could apply rotational force to Joint 6.

The belt continued from one side of the semicircular path to the other, then returned through the same general opening in the Joint 5 housing.

From there, it travelled back toward the pulley reduction and gearbox system farther inside the robot.

The idler pulleys were used to maintain:

- The required belt path
- Belt wrap around the Joint 6 drive section
- Belt alignment
- The required changes in belt direction

---

## 5. Elements That Worked

Several parts of the first rendition were considered successful and should be retained or developed further in the second rendition.

### 5.1 Gearbox Design

The gearbox design and its bearing support arrangement were functional.

The gearbox concept provided a suitable method of producing the required reduction before transferring movement to the pulley system.

### 5.2 Pulley and Idler Concept

The general pulley and idler pulley concept also appeared workable.

The belts could be routed from the lower section of the Joint 5 housing, around the Joint 6 drive section, and back toward the reduction system.

### 5.3 Overall Housing Shape

The overall external shape of the Joint 5 and Joint 6 assembly was acceptable.

The general geometry provided enough space for the wrist mechanism and created a suitable overall appearance for the robot.

### 5.4 Remote Motor Placement

The concept of remotely locating the motors and transmitting motion through belts remained beneficial because it reduced the amount of mass placed directly on the wrist.

---

## 6. Problems Identified in the First Rendition

### 6.1 Excessive Number of Bearings

The main issue with the first rendition was its reliance on too many bearings.

Although bearings were required for the mechanism, the number and placement of the bearings made the design unnecessarily expensive and complicated.

Some bearings were included without a clear structural or mechanical purpose.

Their locations increased:

- Part count
- Cost
- Housing size
- Alignment requirements
- Assembly difficulty

The second rendition should use the minimum number of bearings required to support the mechanism properly.

### 6.2 Unnecessary Joint 6 Mass

The Joint 6 housing contained more material and structure than necessary.

In particular, the lower Joint 6 bracket added mass at the end of the robotic arm without providing enough benefit.

Because Joint 6 is positioned near the end of the arm, unnecessary mass in this area increases the torque requirements for all earlier joints.

Reducing the mass of the Joint 6 assembly is therefore an important requirement for the next rendition.

The lower bracket could be removed or significantly reduced.

The bearing track could instead be incorporated into the upper section of the Joint 6 housing.

Joint 6 could then be connected to Joint 5 using structural mounts and bolts while still rotating through the bearing interfaces.

### 6.3 Incomplete Support of the Entire Wrist Module

The first rendition did not fully account for how the complete Joint 5 and Joint 6 housing would be supported relative to the rest of the robot.

The wrist housing cannot be connected directly to fixed support shafts or surrounding structures if it must rotate.

The complete housing must rotate through properly supported bearings.

One bearing race must connect to the rotating Joint 5 housing, while the opposite race must connect to the stationary structure of the rest of the robot.

This bearing arrangement must be included directly in the second CAD rendition.

### 6.4 Difficult Assembly

The assembly process was more difficult than necessary.

Several parts, bearings, covers, and fasteners had to be installed in a specific order.

Access to internal components was limited, which made the following tasks unnecessarily complicated:

- Belt installation
- Bearing installation
- Idler pulley installation
- Fastener installation
- Belt replacement
- Maintenance
- Disassembly

The second rendition should be designed around a clear and practical assembly sequence.

### 6.5 Poor Internal Access

The first rendition did not provide enough access to the internal belt and idler pulley system.

A hollow or partially open Joint 6 flange would improve visibility and make maintenance easier.

---

## 7. Visibility and Access Requirements

The flange area around Joint 6 should be hollow or partially open in the second rendition.

This would allow the pulley and idler pulley system to remain visible and accessible.

An open flange area would make it easier to:

- Install and remove belts
- Inspect the idler pulleys
- Check belt tracking
- Adjust belt tension
- Replace damaged components
- Diagnose interference
- Diagnose alignment problems

The opening must still maintain enough structural stiffness to support Joint 6 and the end-effector loads.

---

## 8. Encoder Integration

The bearing and housing arrangement could also be used to support the Joint 5 and Joint 6 encoder systems.

The current encoder concept uses magnets for absolute or contactless position sensing.

Magnets could be mounted to the rotating housings, while the encoder sensors could be mounted to the stationary structure on the opposite side of the bearing interface.

This arrangement would allow the encoders to measure the movement of Joint 5 and Joint 6 without interfering with the pulley system.

The exact encoder arrangement still needs to define:

- Magnet position
- Magnet dimensions
- Sensor position
- Sensor mounting method
- Sensor air gap
- Cable routing
- Protection from belt interference
- Protection from moving components

---

## 9. Main Lessons From the First Rendition

The first rendition showed that the combined differential pulley concept for Joint 5 and Joint 6 was possible.

The following concepts were suitable starting points:

- The overall housing shape
- The remote motor arrangement
- The gearbox reduction
- The additional pulley reduction
- The idler pulley routing
- The combined Joint 5 and Joint 6 wrist concept

However, the design became too complicated because of:

- The large number of bearings
- Unnecessary Joint 6 structure
- Poor access to internal components
- An incomplete bearing connection to the rest of the robot
- A difficult assembly sequence

The second rendition should retain the main motion concept while simplifying the mechanical construction.

Every bearing, bracket, fastener, cover, and housing feature should have a clear structural or functional purpose.

---

## 10. Requirements for the Second CAD Rendition

### 10.1 Bearing and Rotation Requirements

- The complete Joint 5 and Joint 6 housing must rotate relative to the rest of the robot through bearings.
- Both sides of the Joint 5 housing should have clearly defined bearing supports.
- The bearing seats must correctly constrain the bearing races.
- The bearings must not move inside the housings during operation.
- Joint 6 must rotate relative to Joint 5 through bearings.
- Joint 6 must not rely on direct plastic-on-plastic sliding contact.
- The number of bearings should be minimized while still providing adequate support and stiffness.

### 10.2 Housing Requirements

- The unnecessary lower Joint 6 bracket should be removed or significantly reduced.
- The Joint 6 bearing track should be integrated into the upper housing where practical.
- The mass of Joint 6 should be reduced.
- The overall external shape of the wrist may be retained.
- The housing must remain stiff enough to support the expected loads.
- The Joint 6 flange should be hollow or partially open for access.
- Open sections must not weaken the housing excessively.

### 10.3 Pulley and Belt Requirements

- The differential pulley concept should be retained.
- The gearbox reduction should remain unless later calculations show that it must be changed.
- The additional pulley reduction should remain unless later calculations show that it must be changed.
- The belt routing should be simplified.
- The system should use the minimum practical number of idler pulleys.
- The belts must remain properly aligned.
- The belts must have sufficient wrap around the driven pulley surfaces.
- The design should include a method of adjusting belt tension.
- The belts should be replaceable without removing the entire wrist assembly.

### 10.4 Assembly Requirements

- The assembly should have a clear installation order.
- Bearings should be installable without damaging the housings.
- Internal bolts should remain accessible with normal tools.
- The belts should be installable without unnecessary disassembly.
- The idler pulleys should be accessible for replacement.
- Covers should be removable without disturbing the main bearing alignment.
- The assembly should use fewer unnecessary parts.
- Repeated fastener and bearing sizes should be used where practical.

### 10.5 Encoder Requirements

- Joint 5 and Joint 6 should have defined encoder mounting locations.
- The rotating magnet should have a secure mounting feature.
- The stationary encoder sensor should have a rigid mounting feature.
- The sensor air gap must remain consistent during rotation.
- Encoder components must not interfere with belts, bearings, or fasteners.
- The design must include a protected cable-routing path.

### 10.6 Structural Requirements

- The housing must support the end-effector and wrist loads.
- The bearing spacing should resist unwanted tilting.
- The structure should minimize deflection.
- Fasteners should provide sufficient clamping force.
- Bearing mounts should not deform significantly under load.
- The final assembly should remain lightweight.

---

## 11. Items Requiring Further Development

The following items still need to be determined before the second rendition is finalized:

- Exact bearing sizes
- Bearing types
- Bearing quantity
- Bearing spacing
- Bearing fit
- Printed bearing-seat tolerances
- Bearing retention method
- Shaft or bolt diameters
- Joint 5 pulley diameter
- Joint 6 pulley diameter
- Pulley tooth count
- Belt width
- Belt tooth profile
- Required belt tension
- Number of idler pulleys
- Idler pulley locations
- Final Joint 5 gear reduction
- Final Joint 6 gear reduction
- Encoder model
- Encoder resolution
- Magnet dimensions
- Magnet placement
- Sensor air gap
- Cable-routing clearances
- Housing wall thickness
- Fastener sizes
- Fastener lengths
- Maximum permitted Joint 6 mass
- Structural stiffness
- Final assembly sequence

---

## 12. Validation Plan

Before the second rendition is approved for full printing, the following checks should be completed.

### 12.1 CAD Checks

- [ ] Run interference detection
- [ ] Test the full Joint 5 range of motion
- [ ] Test the full Joint 6 range of motion
- [ ] Check belt-path clearance
- [ ] Check idler pulley alignment
- [ ] Check fastener access
- [ ] Check bearing retention
- [ ] Check bearing-seat geometry
- [ ] Check encoder clearance
- [ ] Check cable routing
- [ ] Review the assembly sequence
- [ ] Review mass properties
- [ ] Check that the housing connects properly to the rest of the robot

### 12.2 Prototype Checks

- [ ] Print a bearing-seat tolerance test
- [ ] Test pulley and belt fit
- [ ] Test idler pulley alignment
- [ ] Test Joint 5 rotation
- [ ] Test Joint 6 rotation
- [ ] Test combined differential motion
- [ ] Test belt tension
- [ ] Test belt tracking
- [ ] Test encoder magnet and sensor alignment
- [ ] Test housing stiffness
- [ ] Test assembly and disassembly
- [ ] Measure the final wrist mass

---

## 13. Final Conclusion

The first CAD rendition established a workable motion concept for Joint 5 and Joint 6.

The differential pulley system, remote motor placement, gearbox reduction, pulley reduction, and general wrist shape should continue into the next design stage.

The main goal of the second rendition is not to replace the complete concept, but to simplify and strengthen it.

The next design should reduce unnecessary bearings, remove excess Joint 6 mass, improve internal access, define the bearing connection to the rest of the robot, simplify assembly, and integrate the encoder system directly into the housing design.

The second rendition will be treated as the intended printable and functional version of the Joint 5 and Joint 6 wrist assembly.