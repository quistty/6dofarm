# Joint 3: First CAD Rendition Review

## 1. Design Overview

Joint 3 connects the lower arm structure to Joint 4 and supports the remaining wrist assembly.

During the first rendition, it became clear that Joint 3 required either:

- A larger total gear reduction, potentially around 64:1
- A larger motor capable of producing more torque

Instead of relying only on a larger reduction, the design was changed from a NEMA 17 motor to a NEMA 23 motor.

The NEMA 23 was selected because Joint 3 must support and move the mass of:

- Joint 4
- Joint 5
- Joint 6
- The end effector
- The payload
- The supporting housings
- The transmission components

The NEMA 23 provides a stronger starting torque than the smaller motor while still allowing a gearbox to increase the available output torque.

A NEMA 23 motor may also be used again for Joint 1 because of the larger loads present at the base of the robotic arm.

---

## 2. Selected Transmission Concept

Joint 3 uses a two-stage planetary gearbox designed specifically for the robotic arm.

The gearbox was designed from scratch, although the general arrangement and operating principles were influenced by planetary gearbox examples and educational material from How To Mechatronics.

The selected gearbox consists of two identical planetary stages.

Each stage produces a reduction of approximately 6:1.

Because planetary gearbox stages multiply their reductions, the total reduction is:

**Total Reduction = Stage 1 Reduction × Stage 2 Reduction**

Therefore:

**Total Reduction = 6 × 6**

**Total Reduction = 36:1**

The first-rendition target for the complete Joint 3 gearbox was therefore approximately 36:1.

Although a reduction closer to 64:1 was initially considered, the use of a larger NEMA 23 motor allowed the gearbox target to remain at 36:1 for the first design.

The final required reduction must still be confirmed using the complete Joint 3 torque and speed calculations.

---

## 3. Planetary Gearbox Geometry

For the selected planetary gearbox arrangement, the stage reduction was based on:

**i = 1 + Zr / Zs**

Where:

- `i` is the reduction ratio
- `Zr` is the number of teeth on the ring gear
- `Zs` is the number of teeth on the sun gear

For a 6:1 stage:

**6 = 1 + Zr / Zs**

Therefore:

**Zr / Zs = 5**

**Zr = 5 × Zs**

The ring gear must therefore contain five times as many teeth as the sun gear for the selected 6:1 arrangement.

The relationship between the sun, planet, and ring gears is:

**Zr = Zs + 2Zp**

Where:

- `Zp` is the number of teeth on each planet gear

This relationship ensures that the sun gear, planet gears, and internal ring gear have compatible pitch diameters.

---

## 4. Planet Gear Spacing

The first rendition used multiple planet gears spaced evenly around the sun gear.

To allow equal angular spacing between the planet gears, the following condition was considered:

**(Zs + Zr) / Np = Whole Number**

Where:

- `Np` is the number of planet gears

When the result is a whole number, the planet gears can be positioned at equal angular intervals while maintaining the correct tooth engagement.

This requirement is important because an invalid tooth-count combination may cause the planets to be correctly positioned geometrically but incorrectly phased relative to the sun and ring gear teeth.

The design must therefore confirm both:

- Physical spacing between the planets
- Correct tooth phasing between the gears

---

## 5. Gear Tooth Selection

Module 1 gears were selected for the first-rendition planetary gearbox.

Module 1 was considered suitable because it provided a reasonable balance between:

- Gear size
- Tooth strength
- Printability
- Available space
- Ease of modelling
- Prototype cost

The first rendition did not fully optimize the tooth counts to reduce repeating tooth-contact patterns.

Future renditions should consider tooth-count combinations that avoid unnecessary common factors where practical.

Using relatively prime or carefully selected tooth counts may help distribute wear across more tooth combinations instead of repeatedly loading the same tooth pairs.

However, the tooth counts must first satisfy the more important requirements for:

- Gear ratio
- Ring, sun, and planet geometry
- Planet spacing
- Minimum tooth count
- Undercut prevention
- Required gearbox diameter

---

## 6. Prototype Development

Prototype versions of the planetary gearbox were printed during the first-rendition development process.

These prototypes were used to better understand:

- How the sun gear drives the planet gears
- How the planets move inside the ring gear
- How the carrier transfers motion
- How the two stages connect
- How printed clearances affect movement
- How gear alignment affects friction
- How assembly order affects the gearbox

Videos and other planetary gearbox examples were reviewed alongside the prototypes to understand the physical operation of the mechanism before finalizing the CAD model.

The printed prototypes confirmed that the basic two-stage planetary gearbox concept could operate.

[This video was very helpful in the process](https://www.youtube.com/watch?v=Ho4AniHtgxM&t=778s)

---

## 7. SolidWorks Configuration Method

The first-rendition development also improved the method used to create test versions of the gearbox.

Instead of producing separate part files for every tolerance, layout, or test condition, SolidWorks configurations can be used inside the same part file.

Configurations can be used to create different versions of:

- Gear backlash
- Bearing-seat tolerance
- Shaft clearance
- Gear thickness
- Planet spacing
- Housing thickness
- Prototype geometry
- Final geometry

The assembly can also use different configurations instead of requiring a separate assembly file for every test version.

This reduces:

- Duplicate files
- Broken references
- Confusion between versions
- Time required to update repeated geometry
- Risk of editing the wrong part

The second rendition should use configurations consistently for both parts and assemblies.

---

## 8. Gear Tolerances and Backlash

The first rendition began accounting for manufacturing tolerances inside the planetary gearbox.

Printed gears cannot be modelled with perfectly touching theoretical tooth profiles because the gears would likely bind after printing.

An initial backlash value of approximately 0.1 mm was considered.

This clearance is intended to account for:

- Printer dimensional error
- Material expansion
- Surface roughness
- Gear misalignment
- Slight deformation
- Layer-line interference

The 0.1 mm value should not automatically be treated as final.

The required backlash depends on:

- Printer calibration
- Print orientation
- Nozzle size
- Layer height
- Gear material
- Gear diameter
- Tooth geometry
- Expected load

The second rendition should preserve a configurable backlash value so that it can be changed without rebuilding the entire gear model.

---

## 9. Joint 3 Gearbox Connection

The planetary gearbox connects Joint 3 to the partial cylindrical arc discussed in the Joint 4 documentation.

The output of the planetary gearbox must rotate the Joint 4 support structure and everything attached beyond it.

This includes:

- Joint 4
- Joint 5
- Joint 6
- The end effector
- The payload

The gearbox must therefore transfer its output torque securely into the Joint 3 output structure.

The first rendition did not fully define how the gearbox output would rotate the complete surrounding assembly.

The second rendition must create a positive mechanical connection between the gearbox output and the Joint 3 structure.

The system should not rely only on friction between printed parts.

---

## 10. Output Connection and Torque Transfer

The first rendition intended to drive the Joint 3 assembly from one side of the gearbox.

The opposite side was expected to follow through the stiffness and friction of the connected structure.

This arrangement creates a risk that the driven side may rotate slightly before the opposite side begins moving.

Possible consequences include:

- Twisting of the housing
- Uneven loading
- Backlash
- Misalignment
- Slipping between components
- Reduced repeatability
- Damage to printed interfaces

The second rendition should mechanically lock the driven components together.

Possible methods include:

- Keyed shafts
- Keyways
- Splines
- Cross pins
- Clamping hubs
- Bolted flanges
- Multiple engagement tabs
- Metal inserts
- Interlocking printed geometry

Four keyed or interlocking engagement features may be used around the output connection to distribute torque more evenly.

The final connection should ensure that the gearbox output, Joint 3 structure, and supporting shafts rotate together without relying on friction alone.

---

## 11. Joint 3 Housing Support

The Joint 3 gearbox and output structure will connect to the Joint 2 housing using four support rods.

The rods will connect the Joint 3 housing to the surrounding structure of Joint 2.

The four-rod arrangement should:

- Maintain alignment between Joint 2 and Joint 3
- Resist separation between the housings
- Support the planetary gearbox
- Provide structural stiffness
- Keep the rotating components clear
- Allow the spacing to be adjusted
- Allow the structure to be tightened after assembly

The rods should use an adjustable retention method so that the housings can be aligned and secured during assembly.

Possible retention methods include:

- Threaded rods with recessed nuts
- Shoulder bolts
- Internally threaded rods
- Captive nuts
- Threaded inserts
- Clamping collars

The rods should not be used to compensate for major misalignment in the CAD geometry.

The bearing seats and housing geometry must still locate the gearbox accurately.

---

## 12. Joint 3 Physical Range of Motion

The planetary gearbox operated successfully as a continuous rotational mechanism, but the first rendition did not properly include the physical movement limits required for Joint 3.

Joint 3 is intended to rotate through a limited range rather than continuously.

The approximate required range is:

**0° to 135°**

The second rendition should incorporate physical geometry that prevents Joint 3 from rotating beyond its safe range.

Possible limiting features include:

- A curved slot
- A rotating stop tab
- Replaceable stop blocks
- A pin moving through an arc
- Housing-to-housing contact surfaces
- An adjustable hard-stop mechanism

The limit should not rely only on motor commands or software.

A physical hard stop can protect the joint if:

- The encoder loses position
- The motor skips
- The controller commands an invalid position
- The robot is moved while unpowered
- The gearbox is assembled in the wrong orientation

The stop must be designed to withstand occasional contact without damaging the gearbox teeth or printed housing.

---

## 13. Encoder Integration

The Joint 3 gearbox must include an encoder that measures the actual output position of the joint.

The encoder should measure the rotation after the gearbox rather than only measuring the motor shaft.

Measuring the gearbox output allows the system to detect:

- Actual joint position
- Gearbox backlash
- Motor skipping
- Unexpected movement
- Position differences between the commanded and physical joint angle

The encoder magnet may be embedded inside or attached directly to the rotating ring or output structure.

The encoder sensor should be mounted to the stationary Joint 3 housing.

The design must define:

- Which component rotates with the Joint 3 output
- Which component remains stationary
- Magnet location
- Magnet orientation
- Sensor location
- Sensor air gap
- Wire routing
- Sensor protection
- Access for replacement

The encoder must not interfere with:

- Planet gears
- The ring gear
- Bearings
- Output fasteners
- Hard stops
- Support rods

The encoder mounting geometry should be included directly in the second CAD rendition rather than added after the gearbox is complete.

---

## 14. Housing Size and Packaging

The bare planetary gearbox concept worked, but the first-rendition holding structure occupied more space than necessary.

The housing should be redesigned to follow the load paths of the gearbox instead of surrounding it with unnecessary solid material.

The second rendition should reduce:

- Housing diameter where possible
- Housing length
- Unnecessary wall thickness
- Empty enclosed spaces
- Oversized brackets
- Excessive fastener bosses
- Unsupported decorative geometry

Material should remain around:

- Bearing seats
- Motor mounts
- Support-rod connections
- Gearbox-stage connections
- Output interfaces
- Hard stops
- Encoder mounts

The goal is not simply to make the walls thinner.

The goal is to remove material that does not contribute significantly to:

- Strength
- Stiffness
- Alignment
- Bearing retention
- Assembly
- Protection

---

## 15. Elements That Worked

Several parts of the Joint 3 first rendition were successful.

### 15.1 Planetary Gearbox Concept

The two-stage planetary gearbox was capable of providing a large reduction in a relatively compact arrangement.

The use of two identical 6:1 stages simplified the design process and produced a total reduction of approximately 36:1.

### 15.2 NEMA 23 Motor Selection

Moving to a NEMA 23 motor provided a stronger motor platform for Joint 3.

This reduced the need to obtain all required torque through an extremely large gearbox reduction.

### 15.3 Module 1 Gear Geometry

Module 1 was suitable for the initial printed prototypes.

The gear size was large enough to model and print while remaining compact enough for the Joint 3 housing.

### 15.4 Printed Prototypes

The printed test gearboxes improved the understanding of the planetary mechanism and exposed issues related to tolerance, assembly, and gear movement.

### 15.5 Configuration-Based Development

Using SolidWorks configurations provided a more organized way to produce tolerance tests and alternate gearbox versions.

### 15.6 Basic Housing and Rod Concept

The use of four rods to connect the Joint 3 structure to Joint 2 provided a simple and adjustable structural arrangement.

---

## 16. Problems Identified in the First Rendition

### 16.1 Reduction Requirement Was Not Fully Confirmed

The project initially considered a reduction near 64:1, but the first-rendition gearbox produced 36:1.

The NEMA 23 may make the lower reduction acceptable, but this must be confirmed using complete torque and speed calculations.

### 16.2 Tooth Counts Were Not Fully Optimized

The selected tooth counts met the basic gear-ratio and geometry requirements, but they were not fully reviewed for repeating tooth-contact patterns, undercut, and long-term wear.

### 16.3 Backlash Was Not Fully Tested

An initial backlash value of approximately 0.1 mm was introduced, but the correct value was not confirmed through sufficient testing.

### 16.4 Output Connection Relied Too Heavily on Friction

The gearbox output did not have a sufficiently positive mechanical connection to the complete Joint 3 structure.

The design should use keys, splines, pins, bolted flanges, or equivalent features.

### 16.5 Physical Joint Limits Were Missing

The geometry did not properly restrict Joint 3 to its intended movement range of approximately 0° to 135°.

### 16.6 Encoder Integration Was Incomplete

The encoder was considered, but its mounting, magnet position, air gap, and wiring were not incorporated fully into the gearbox.

### 16.7 Housing Used Too Much Space

The holding structure was larger than necessary and should be redesigned around the actual load paths and required clearances.

### 16.8 Gearbox-to-Joint Connection Was Incomplete

The first rendition did not clearly define how the gearbox output would rotate every connected component without twisting, slipping, or misalignment.

---

## 17. Requirements for the Second CAD Rendition

### 17.1 Motor and Reduction Requirements

- Joint 3 should use a NEMA 23 motor.
- The required reduction must be confirmed using torque and speed calculations.
- The two-stage 36:1 planetary gearbox may be retained if it satisfies the final calculations.
- A higher reduction should be considered if the 36:1 system cannot meet the required torque safely.
- The final design must balance output torque and joint speed.
- Gearbox efficiency must be included in the calculations.

### 17.2 Planetary Gear Requirements

- The gearbox should use two planetary stages.
- Each stage should target approximately 6:1 reduction.
- The two stages should produce approximately 36:1 total reduction.
- Module 1 may be retained if strength and packaging requirements are satisfied.
- The ring, sun, and planet tooth counts must satisfy the geometric relationship.
- The planet gears must be spaced and phased correctly.
- Tooth counts should be reviewed for undercut.
- Tooth combinations should reduce repeating contact patterns where practical.
- The gearbox should use configurable backlash.
- Gear thickness should be selected based on the expected torque.
- The planet gears must not interfere with one another.

### 17.3 Output-Connection Requirements

- The gearbox output must be positively connected to the Joint 3 structure.
- The connection must not rely only on friction.
- The output should use keys, pins, splines, clamping hubs, interlocking geometry, or a bolted flange.
- Torque should be distributed across multiple engagement points where practical.
- Both sides of the Joint 3 structure must rotate together.
- The housing must resist twisting between the driven and supported sides.
- The connection should be removable for maintenance.

### 17.4 Range-of-Motion Requirements

- Joint 3 should have an approximate physical range of 0° to 135°.
- The design should include mechanical hard stops.
- The hard stops must not interfere with normal motion.
- The hard stops should contact structural housing features rather than gear teeth.
- The stop geometry should be replaceable or adjustable where practical.
- Software limits should also be used, but they should not replace the physical stops.

### 17.5 Encoder Requirements

- Joint 3 must include an output-side encoder.
- The encoder should measure the actual joint angle after the gearbox.
- The magnet may be embedded in the rotating ring or output component.
- The sensor must be mounted to a stationary structure.
- The magnet and sensor must remain concentric.
- The sensor air gap must remain controlled.
- Encoder wiring must be protected from the gears and rotating parts.
- The encoder mount must allow replacement and alignment.
- Encoder geometry must be included before the housing is finalized.

### 17.6 Housing Requirements

- The gearbox housing should occupy less space than the first rendition.
- Unnecessary material should be removed.
- Bearing seats must remain stiff and accurately aligned.
- The housing must support the NEMA 23 motor.
- The motor mount must resist gearbox reaction torque.
- The housing must provide access for assembly.
- The two gearbox stages should be removable where practical.
- The housing should use practical print orientations.
- Fasteners should remain accessible with normal tools.
- The housing must protect the gears without completely preventing inspection or maintenance.

### 17.7 Support-Rod Requirements

- Four rods should connect the Joint 3 structure to the Joint 2 housing.
- The rods should maintain the alignment of the joint structures.
- The rods should be adjustable and capable of being tightened.
- Rod ends should not protrude unnecessarily.
- Washers or metal spacers should distribute clamping forces.
- The printed housing should not be crushed when the rods are tightened.
- The rods must remain clear of the rotating gearbox and joint structure.
- The rod connection points should be reinforced appropriately.

### 17.8 SolidWorks Requirements

- Different prototype geometries should use configurations instead of duplicate files.
- Backlash should be controlled through a configurable parameter.
- Bearing tolerances should be configurable.
- Gear thickness should be configurable.
- Housing dimensions should reference shared variables where possible.
- Assembly configurations should be used for prototype and final layouts.
- Gearbox-stage dimensions should update together when major parameters change.

---

## 18. Items Requiring Further Development

The following details still need to be determined:

- Required Joint 3 output torque
- Required Joint 3 speed
- Final reduction ratio
- NEMA 23 torque-speed performance
- Gearbox efficiency
- Sun gear tooth count
- Planet gear tooth count
- Ring gear tooth count
- Number of planet gears
- Planet spacing condition
- Planet tooth phasing
- Minimum tooth count before undercut
- Final gear module
- Gear face width
- Final backlash value
- Gear material
- Planet pin diameter
- Planet bearing or bushing method
- Carrier thickness
- Carrier-to-output connection
- Ring gear support method
- Output shaft diameter
- Key or spline dimensions
- Number of output engagement points
- Bearing sizes
- Bearing spacing
- Bearing-seat tolerances
- Joint hard-stop geometry
- Hard-stop material
- Encoder model
- Encoder magnet dimensions
- Encoder air gap
- Encoder wire routing
- Support-rod diameter
- Support-rod material
- Support-rod spacing
- Housing wall thickness
- Motor-mount thickness
- Fastener sizes
- Assembly sequence
- Final Joint 3 mass

---

## 19. Main Lessons From the First Rendition

The first rendition demonstrated that a custom two-stage planetary gearbox could be used for Joint 3.

The gearbox concept, module 1 gears, NEMA 23 motor, four-rod housing connection, and configuration-based CAD workflow all provided a useful foundation for the next rendition.

The main concept does not need to be replaced.

However, several important mechanical details were incomplete.

The second rendition must improve:

- Confirmation of the required reduction
- The gearbox output connection
- The physical joint limits
- Encoder integration
- Gear backlash
- Tooth-count selection
- Housing size
- Structural alignment
- Assembly access

The largest issue is that the gearbox cannot simply produce torque internally.

It must transfer that torque into the complete Joint 3 and Joint 4 structure without relying on friction or allowing the two sides of the mechanism to twist independently.

---

## 20. Final Conclusion

The first CAD rendition of Joint 3 established a workable design based on a NEMA 23 motor and a custom two-stage planetary gearbox.

Each planetary stage was designed for approximately 6:1 reduction, producing a combined output reduction of approximately 36:1.

Printed prototypes confirmed that the basic gearbox concept could operate and helped establish the need for configurable gear tolerances and backlash.

The overall concept worked, but the first rendition did not fully define the physical joint limits, encoder integration, output torque connection, or compact housing structure.

The second rendition should retain the two-stage planetary gearbox concept while making the gearbox smaller, mechanically locking the output to the surrounding structure, adding a physical movement range of approximately 0° to 135°, and embedding an output-side magnetic encoder into the joint.

The design should also use SolidWorks configurations to control gear backlash, tolerances, prototype layouts, and final geometry without creating unnecessary duplicate files.