# Joint 2: First CAD Rendition Review

## 1. Design Overview

Joint 2 is one of the primary load-bearing joints of the robotic arm.

It is responsible for rotating the main upper-arm structure and supporting the mass of:

- Joint 3
- Joint 4
- Joint 5
- Joint 6
- The upper-arm and forearm links
- The end effector
- The payload
- The motors, gearboxes, bearings, and housings located farther along the arm

Because Joint 2 supports most of the robotic arm against gravity, it requires considerably more output torque than the wrist joints.

The intended range of motion for Joint 2 is:

**-90° to +90°**

This gives Joint 2 a total motion range of approximately:

**180°**

During the first rendition, calculations suggested that Joint 2 required a reduction of at least approximately 70:1.

Rather than producing the entire reduction using one planetary gearbox, the design used a combination of:

- A planetary gearbox
- A belt and pulley reduction

This allowed the reduction to be distributed between two different transmission systems.

---

## 2. Selected Motor and Transmission Concept

Joint 2 uses a larger motor and a combined planetary and pulley transmission.

The intended transmission consists of:

1. A NEMA 23 stepper motor
2. A planetary gearbox
3. A small driving pulley
4. A large driven pulley
5. A timing belt
6. A Joint 2 output structure connected to the upper arm

The motor first transfers power through the planetary gearbox.

The output of the planetary gearbox then drives the small pulley.

The small pulley transfers motion through a timing belt to the larger Joint 2 pulley.

The combined reduction increases the torque available at Joint 2 while decreasing its output speed.

The general transmission sequence is:

**Motor → Planetary Gearbox → Small Pulley → Timing Belt → Large Pulley → Joint 2 Output**

---

## 3. Original Reduction Requirement

The initial target reduction for Joint 2 was approximately:

**70:1**

This value was selected because Joint 2 must generate enough torque to lift and hold the complete upper portion of the arm.

A reduction greater than 70:1 was considered acceptable as long as:

- The joint still moved at a practical speed
- The gearbox remained compact enough
- The motor operated inside a useful torque-speed range
- The transmission did not introduce excessive backlash
- The complete mechanism fit inside the available Joint 2 space

The first rendition attempted to obtain a total reduction between approximately 83:1 and 100:1.

However, the calculations used during development contained a discrepancy that must be resolved before the final design.

---

## 4. Planetary Gearbox Design

The Joint 2 planetary gearbox was based on the same general design principles used for Joint 3.

The selected tooth counts were:

| Gear | Number of Teeth |
|---|---:|
| Sun gear | 17 |
| Planet gear | 40 |
| Ring gear | 97 |

The basic planetary geometry relationship is:

**Zr = Zs + 2Zp**

Substituting the selected tooth counts:

**97 = 17 + 2(40)**

**97 = 17 + 80**

**97 = 97**

The selected sun, planet, and ring gears therefore satisfy the required geometric relationship.

This means the gears can physically mesh at their theoretical pitch diameters when the same module is used.

---

## 5. Planetary Reduction Calculation

For the planetary arrangement previously used in the project, the reduction equation was:

**i = 1 + Zr / Zs**

Where:

- `i` is the planetary reduction
- `Zr` is the number of ring gear teeth
- `Zs` is the number of sun gear teeth

Using the selected tooth counts:

**i = 1 + 97 / 17**

**i = 1 + 5.7059**

**i ≈ 6.7059**

The planetary gearbox ratio produced by these tooth counts is therefore approximately:

**6.71:1**

The selected tooth counts do not produce an 8:1 reduction under this arrangement.

For an exact 8:1 reduction using this equation:

**8 = 1 + Zr / Zs**

Therefore:

**Zr / Zs = 7**

**Zr = 7Zs**

The final rendition must either:

- Retain the `17/40/97` tooth combination and document the planetary reduction as approximately 6.71:1
- Select new tooth counts that produce a true 8:1 reduction
- Change the constrained and driven planetary members, then recalculate the ratio using the correct equation

The reduction must be calculated from the actual operating arrangement rather than only from the gear tooth counts.

---

## 6. Pulley Reduction

The pulley system used:

- An approximately 8 mm driving pulley outer diameter
- An approximately 100 mm driven pulley outer diameter

The approximate pulley reduction was calculated as:

**Pulley Reduction = Driven Pulley Diameter / Driving Pulley Diameter**

**Pulley Reduction = 100 / 8**

**Pulley Reduction = 12.5:1**

The pulley system therefore produces an approximate reduction of:

**12.5:1**

The small pulley is driven by the planetary gearbox output.

The large pulley is connected to the Joint 2 output structure and rotates the upper arm.

The large pulley also provides a convenient method of transferring torque over a relatively large diameter.

---

## 7. Total Reduction

Gearbox and pulley reductions multiply.

The total reduction is calculated using:

**Total Reduction = Planetary Reduction × Pulley Reduction**

### 7.1 Total Using the Selected Tooth Counts

Using the calculated planetary reduction of approximately 6.71:1:

**Total Reduction = 6.7059 × 12.5**

**Total Reduction ≈ 83.82:1**

The current tooth counts and pulley dimensions therefore produce an approximate total reduction of:

**83.8:1**

This is reasonably close to the previously discussed target of approximately 83:1.

### 7.2 Total Using an Assumed 8:1 Planetary Gearbox

If the planetary gearbox were redesigned to provide a true 8:1 reduction:

**Total Reduction = 8 × 12.5**

**Total Reduction = 100:1**

A true 8:1 planetary gearbox combined with the 12.5:1 pulley system would therefore produce:

**100:1**

### 7.3 Reduction Discrepancy

The first-rendition notes referred to both:

- Approximately 83:1
- Approximately 100:1

These values represent two different gearbox specifications.

| Planetary Reduction | Pulley Reduction | Total Reduction |
|---:|---:|---:|
| 6.71:1 | 12.5:1 | 83.8:1 |
| 8:1 | 12.5:1 | 100:1 |

The final rendition must select one of these systems based on the required Joint 2 torque and speed.

---

## 8. Joint 2 Output and Upper-Arm Connection

The upper sections of the robotic arm were designed to connect to the Joint 2 output bracket.

The large driven pulley rotates together with the Joint 2 output structure.

The output bracket then transfers that rotation into the upper arm and the remaining joints.

The bracket must support:

- The static weight of the complete upper-arm assembly
- The payload load
- Dynamic loads during acceleration and deceleration
- Reaction torque from the gearbox and belt system
- Bending loads caused by the arm extending away from Joint 2
- Side loads caused by imperfect alignment or external forces

The upper arm must be positively connected to the output bracket.

The connection should not rely only on friction between printed surfaces.

Suitable connection methods may include:

- Multiple bolts
- Through-shafts
- Keyed shafts
- Splines
- Interlocking tabs
- Clamping hubs
- Bolted flanges
- Metal inserts
- Cross pins

The bracket must rotate as one rigid structure with the large driven pulley.

---

## 9. Joint 2 Range of Motion

Joint 2 is intended to rotate from:

**-90° to +90°**

The total range of motion is therefore:

**180°**

The second rendition must include geometry that supports this movement without interference.

The range must be checked against:

- The Joint 1 housing
- The Joint 2 gearbox
- The upper-arm structure
- The pulley and belt
- The motor
- The support rods
- Encoder wiring
- Joint 3
- Mechanical hard stops

Joint 2 should include both:

- Software-defined movement limits
- Physical mechanical limits

Software limits should prevent normal commands from exceeding the intended range.

Physical hard stops should prevent destructive movement if:

- The encoder loses its reference
- The motor skips
- The controller sends an incorrect command
- The robot is moved while powered off
- The software limits fail

The hard stops should contact reinforced structural features rather than gear teeth or delicate encoder components.

---

## 10. Planet Gear Spacing

If multiple planet gears are used, their spacing and tooth phasing must be valid.

The equal-spacing condition is:

**(Zs + Zr) / Np = Whole Number**

Where:

- `Zs` is the number of sun gear teeth
- `Zr` is the number of ring gear teeth
- `Np` is the number of planet gears

For the selected gears:

**Zs + Zr = 17 + 97**

**Zs + Zr = 114**

The number of planets must therefore divide 114 evenly for this simplified spacing condition to produce a whole number.

Examples include:

| Number of Planets | Calculation | Valid Whole Number |
|---:|---:|---|
| 3 | 114 / 3 = 38 | Yes |
| 4 | 114 / 4 = 28.5 | No |
| 6 | 114 / 6 = 19 | Yes |

The final number of planets must also satisfy:

- Physical clearance between planet gears
- Load-sharing requirements
- Carrier strength
- Printability
- Assembly access
- Available housing diameter

At least three planets should be used for balanced support.

---

## 11. Pulley Design Considerations

The first rendition estimated the pulley reduction using outer diameters.

However, timing pulley ratios should ultimately be calculated using:

- Pulley tooth counts
- Pitch diameters

The outside diameter is useful for estimating packaging, but it is not the most accurate value for determining a toothed-belt reduction.

The final pulley ratio should be calculated using:

**Pulley Reduction = Driven Pulley Teeth / Driving Pulley Teeth**

The selected pulleys must use:

- The same belt pitch
- The same tooth profile
- A compatible belt width
- Sufficient tooth engagement
- Adequate clearance from the surrounding housing

The small driving pulley must also have enough teeth to prevent:

- Excessive belt bending
- Poor tooth engagement
- Premature belt wear
- Tooth skipping
- Excessive stress in the belt

An 8 mm outside diameter may be too small for some timing-belt profiles and shaft sizes.

The final design must confirm that the small pulley can physically include:

- The required shaft bore
- Sufficient material around the bore
- A set screw, key, or clamping feature
- Enough timing-belt teeth
- Adequate strength

---

## 12. Belt Loading and Tension

The belt must transmit the output torque of the planetary gearbox to the large driven pulley.

The required belt force is related to the pulley torque and pitch radius.

A smaller driving pulley produces a larger belt force for the same transmitted torque.

The final design must therefore confirm:

- Maximum belt tension
- Belt tooth strength
- Pulley tooth engagement
- Pulley shaft loading
- Bearing loading
- Motor mount stiffness
- Housing stiffness
- Safety factor against belt skipping

The design must also include a method of adjusting belt tension.

Possible tensioning methods include:

- Adjustable motor position
- Slotted motor-mount holes
- An eccentric tensioner
- A dedicated idler pulley
- A movable gearbox mount

The selected tensioning system should not introduce unnecessary bearings or excessive assembly complexity.

---

## 13. Bearing and Shaft Support

The Joint 2 output must be supported independently from the motor and gearbox shafts.

The motor shaft should transmit torque, but it should not carry the full bending load of the upper arm.

The large driven pulley and Joint 2 output should therefore rotate through dedicated bearings.

The bearing arrangement must support:

- Radial loads
- Axial loads where applicable
- Bending moments
- Belt tension
- Weight of the upper-arm assembly
- Dynamic loading during movement

The output should preferably use bearings spaced apart along the axis.

Increasing bearing spacing can improve resistance to tilting and bending.

The final design must define:

- Bearing type
- Bearing size
- Bearing spacing
- Shaft diameter
- Shaft material
- Bearing-seat tolerance
- Axial-retention method
- Spacers
- Washers
- Locknuts or retaining rings

The bearing arrangement must not rely on printed plastic alone to resist high concentrated loads where metal shafts or spacers would be more appropriate.

---

## 14. Encoder Integration

Joint 2 requires an output-side encoder.

The encoder should measure the actual Joint 2 output angle after both:

- The planetary gearbox
- The pulley reduction

Measuring only the motor shaft would not detect:

- Planetary gearbox backlash
- Belt stretch
- Belt skipping
- Pulley slipping
- Output-bracket movement
- Motor skipping

The encoder magnet should rotate with the actual Joint 2 output.

The sensor should remain fixed to the stationary Joint 2 housing.

The design must define:

- Magnet location
- Magnet orientation
- Sensor location
- Sensor air gap
- Sensor mounting method
- Wire routing
- Wire strain relief
- Protection from belt contact
- Protection from the moving upper arm

The encoder must cover the full motion range from `-90°` to `+90°`.

The encoder mounting position should be included before the final housing geometry is completed.

---

## 15. Housing and Support Structure

The Joint 2 housing must contain or support:

- The NEMA 23 motor
- The planetary gearbox
- The small driving pulley
- The timing belt
- The large driven pulley
- The output bearings
- The encoder
- The Joint 2 output bracket
- The connection to Joint 1
- The connection to Joint 3 and the upper arm

Because Joint 2 carries large loads, the housing must be stiff enough to maintain alignment between the pulley and gearbox components.

Material should be concentrated around:

- Bearing seats
- Shaft supports
- Motor mounts
- Gearbox mounts
- Pulley supports
- Upper-arm bracket connections
- Joint 1 mounting points
- Hard stops

Unnecessary material should be removed from low-stress regions.

The housing should use ribs, webs, and reinforced load paths instead of relying only on thick solid walls.

---

## 16. Elements That Worked

Several features of the Joint 2 first rendition provided a useful foundation.

### 16.1 Combined Reduction Concept

Using both a planetary gearbox and a pulley system allowed a large total reduction without requiring an extremely large planetary gearbox.

### 16.2 High Total Reduction

The selected tooth counts and pulley dimensions produced an estimated total reduction of approximately 83.8:1.

This exceeded the original minimum target of approximately 70:1.

### 16.3 Valid Planetary Gear Geometry

The selected tooth counts satisfied:

**Zr = Zs + 2Zp**

The sun, planet, and ring gears were therefore geometrically compatible.

### 16.4 Large Driven Pulley

The large Joint 2 pulley provided both reduction and a broad interface for connecting the output to the upper-arm structure.

### 16.5 Upper-Arm Bracket Concept

The concept of connecting the upper arm directly to a Joint 2 output bracket provided a clear path for transferring the joint rotation into the rest of the robot.

### 16.6 Limited Joint Range

Defining Joint 2 as a `-90°` to `+90°` joint made it possible to use a limited-rotation output, physical hard stops, and a non-continuous encoder wiring arrangement.

---

## 17. Problems and Unresolved Issues

### 17.1 Conflicting Reduction Values

The design notes described the planetary gearbox as 8:1, but the selected tooth counts produce approximately 6.71:1 using the stated planetary equation.

The total reduction is therefore either:

- Approximately 83.8:1 with the existing tooth counts
- 100:1 with a true 8:1 planetary gearbox

The final design cannot use both values.

### 17.2 Pulley Ratio Based on Outer Diameter

The pulley ratio was estimated using outside diameters.

The final ratio must be defined using pulley tooth counts or pitch diameters.

### 17.3 Very Small Driving Pulley

An 8 mm outside diameter driving pulley may create packaging, strength, and belt-engagement problems.

The bore and attachment method may leave insufficient material for the pulley teeth.

### 17.4 Output Bearing Arrangement Was Incomplete

The first rendition did not fully define how the large driven pulley and upper-arm bracket would be supported against bending and belt loads.

### 17.5 Output Connection Must Be Positive

The large pulley, shaft, and upper-arm bracket must rotate together through a positive mechanical connection.

The design should not depend only on friction.

### 17.6 Physical Joint Limits Were Not Fully Defined

Joint 2 requires physical limits at `-90°` and `+90°`.

The first rendition did not fully incorporate these limits.

### 17.7 Encoder Integration Was Incomplete

The encoder was required but not fully incorporated into the output housing and pulley arrangement.

### 17.8 Final Torque and Speed Were Not Confirmed

The selected reduction must be checked against:

- Required output torque
- Required Joint 2 speed
- Motor torque at operating speed
- Gearbox efficiency
- Belt efficiency
- Safety factor

---

## 18. Requirements for the Second CAD Rendition

### 18.1 Motion Requirements

- Joint 2 must rotate from approximately `-90°` to `+90°`.
- The total range of motion must be approximately 180°.
- The joint must move without interference with Joint 1, Joint 3, or the upper-arm structure.
- Software movement limits must be included.
- Physical hard stops must also be included.
- Hard stops must contact reinforced structural features.

### 18.2 Reduction Requirements

- The total reduction must be at least approximately 70:1 unless updated calculations establish a different requirement.
- The final design must select either the approximately 83.8:1 or 100:1 system.
- The planetary ratio must be calculated using the actual constrained, input, and output members.
- The pulley ratio must be calculated using tooth counts or pitch diameters.
- Gearbox and belt efficiency must be included in the final torque calculation.
- The final output speed must remain practical for the robot.

### 18.3 Planetary Gearbox Requirements

- The sun, planet, and ring tooth counts must satisfy the required geometric relationship.
- The number of planet gears must satisfy the spacing and phasing condition.
- At least three planet gears should be used.
- The planet gears must not interfere with each other.
- Tooth counts should be checked for undercut.
- Gear backlash must be configurable.
- The gear face width must be selected based on the transmitted torque.
- The gearbox housing must maintain gear alignment.
- The carrier and output connection must not rely only on friction.

### 18.4 Pulley Requirements

- Both pulleys must use the same belt pitch and tooth profile.
- The pulley ratio must be based on tooth count.
- The driving pulley must fit the selected shaft.
- The driving pulley must have enough material around its bore.
- The driving pulley must provide adequate belt engagement.
- The driven pulley must be rigidly attached to the Joint 2 output.
- The pulley system must include a belt-tension adjustment method.
- The belt must remain clear of all housing and bracket components.
- The belt must be replaceable without disassembling the entire robot.

### 18.5 Output-Connection Requirements

- The large pulley, output shaft, and upper-arm bracket must rotate together.
- The connection must not rely only on friction between printed parts.
- A key, spline, clamping hub, bolted flange, pin, or interlocking interface should be used.
- The connection must transfer the full Joint 2 output torque.
- The connection must resist reversing loads.
- The connection should be removable for maintenance.

### 18.6 Bearing and Shaft Requirements

- The Joint 2 output must use dedicated bearings.
- The motor shaft must not support the upper-arm bending load.
- The bearings must support belt force and arm loads.
- Bearing spacing should resist tilting of the output.
- The output shaft must have sufficient strength and stiffness.
- The bearing races must be retained axially.
- The shaft must not move inside the pulley or bracket.
- Metal spacers should be used where clamping forces could crush printed parts.

### 18.7 Upper-Arm Bracket Requirements

- The upper-arm structure must connect securely to the Joint 2 output bracket.
- The bracket must support the complete distal arm assembly.
- The bracket must resist bending and twisting.
- The bracket should distribute load across multiple fasteners or engagement features.
- Fastener holes should have sufficient surrounding material.
- Washers, inserts, bushings, or metal plates should be used where appropriate.
- The bracket should remain as lightweight as possible without compromising stiffness.

### 18.8 Encoder Requirements

- Joint 2 must use an output-side encoder.
- The encoder must measure the joint after the complete reduction system.
- The magnet must rotate with the Joint 2 output.
- The sensor must remain stationary.
- The sensor air gap must remain controlled.
- The encoder must measure the full `-90°` to `+90°` range.
- Encoder wiring must remain clear of the belt and pulley.
- The encoder mount must be accessible for adjustment and replacement.

### 18.9 Housing Requirements

- The housing must support the NEMA 23 motor and planetary gearbox.
- The housing must maintain pulley alignment.
- The motor and gearbox mounts must resist reaction torque.
- The housing must include access for belt installation and tensioning.
- Bearing seats must remain stiff.
- Unnecessary solid material should be removed.
- Structural ribs should follow the primary load paths.
- Fasteners must remain accessible using normal tools.
- The housing must connect securely to Joint 1.
- The housing must provide the output connection to the upper arm and Joint 3.

### 18.10 SolidWorks Requirements

- Gear tooth counts should be controlled using parameters or equations.
- Backlash should be configurable.
- Pulley tooth counts should be configurable.
- Bearing-seat tolerances should be configurable.
- Prototype and final geometries should use configurations.
- Assembly configurations should be used instead of duplicate assemblies.
- Joint limits should be represented in the assembly.
- The full `-90°` to `+90°` movement should be checked in CAD.
- Interference detection should be completed before printing.

---

## 19. Items Requiring Further Development

The following details must still be confirmed:

- Final required Joint 2 torque
- Final required Joint 2 speed
- NEMA 23 motor model
- Motor torque-speed curve
- Motor shaft diameter
- Final planetary reduction
- Final total reduction
- Whether the target is 83.8:1 or 100:1
- Sun gear tooth count
- Planet gear tooth count
- Ring gear tooth count
- Number of planet gears
- Planet spacing and phasing
- Gear module
- Gear face width
- Gear backlash
- Gearbox efficiency
- Belt efficiency
- Driving pulley tooth count
- Driven pulley tooth count
- Belt pitch
- Belt width
- Belt length
- Minimum small-pulley tooth count
- Belt-tension requirement
- Belt-tension adjustment method
- Large pulley attachment method
- Output shaft diameter
- Output shaft material
- Bearing size
- Bearing type
- Bearing spacing
- Bearing-seat tolerance
- Axial-retention method
- Upper-arm bracket geometry
- Bracket fastener sizes
- Hard-stop geometry
- Hard-stop strength
- Encoder model
- Magnet dimensions
- Sensor air gap
- Encoder cable routing
- Housing wall thickness
- Structural rib thickness
- Final Joint 2 mass
- Assembly sequence

---

## 20. Main Lessons From the First Rendition

The first rendition established that Joint 2 could use a combined planetary gearbox and pulley reduction to achieve the high torque multiplication required for the shoulder joint.

The selected `17/40/97` planetary gear geometry was physically compatible and produced an estimated planetary reduction of approximately 6.71:1 under the previously used operating arrangement.

Combined with the estimated 12.5:1 pulley reduction, the system produced approximately 83.8:1 total reduction.

The main concept was successful, but the numerical specifications were not recorded consistently.

The most important lesson is that the planetary reduction, pulley reduction, and total reduction must all be calculated from the final physical geometry.

The second rendition must also improve:

- Output bearing support
- Belt tensioning
- Pulley sizing
- Output torque transfer
- Upper-arm bracket strength
- Physical joint limits
- Encoder integration
- Housing efficiency
- Assembly access

---

## 21. Final Conclusion

The first CAD rendition of Joint 2 used a NEMA 23 motor, a custom planetary gearbox, and a belt-driven pulley reduction.

The selected planetary gear tooth counts were:

- 17-tooth sun gear
- 40-tooth planet gears
- 97-tooth ring gear

These tooth counts satisfy the required planetary geometry relationship and produce an estimated reduction of approximately 6.71:1 using the previously selected operating arrangement.

The 8 mm and 100 mm pulley diameters produce an estimated pulley reduction of approximately 12.5:1.

Together, these values produce an estimated total reduction of approximately:

**83.8:1**

A true 8:1 planetary gearbox would instead produce a total reduction of:

**100:1**

The final rendition must resolve this discrepancy before the gearbox and pulleys are finalized.

The next design should retain the combined planetary and pulley concept while defining the final reduction, strengthening the output connection, supporting the large pulley with dedicated bearings, integrating an output-side magnetic encoder, and adding physical limits for the required `-90°` to `+90°` movement range.