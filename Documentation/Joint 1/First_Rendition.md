# Joint 1: First CAD Rendition Review

## 1. Design Overview

Joint 1 forms the base rotational joint of the robotic arm.

The purpose of Joint 1 is to rotate the complete robotic arm around the vertical axis. This includes the movement of:

- Joint 2
- Joint 3
- Joint 4
- Joint 5
- Joint 6
- The arm links
- The end effector
- The payload

The first rendition of Joint 1 used a simple circular base with an approximate diameter of:

**100 mm**

The rotating section was supported by a bearing, allowing the upper structure of the robot to rotate relative to the stationary base.

The original design focused primarily on creating a basic rotating platform. Additional mounting and retention features were then added around the circular structure to keep the base properly secured.

---

## 2. Joint Motion

Joint 1 was intended to rotate continuously around the vertical axis.

Unlike the limited rotation of Joint 2 and Joint 3, Joint 1 did not initially include a defined mechanical stopping point.

The bearing allowed the rotating upper structure to move around the base without direct sliding contact between the two main housing components.

The intended movement was therefore:

**Continuous rotation around the Joint 1 axis**

However, continuous mechanical rotation also creates additional requirements for:

- Cable routing
- Motor wiring
- Encoder wiring
- Power delivery
- Prevention of cable twisting
- Bearing retention
- Output-position measurement

These requirements were not fully addressed in the first rendition.

---

## 3. Circular Base Structure

The primary Joint 1 structure was based on a circular platform approximately 100 mm in diameter.

The circular geometry was selected because:

- It matched the rotational movement of the joint
- It provided a symmetrical base
- It allowed the bearing to remain concentric with the rotational axis
- It provided mounting space around the circumference
- It created a simple starting geometry for the robot base

The first rendition added several mounting features to the circular housing to secure the rotating and stationary sections.

These features were intended to:

- Prevent the bearing from leaving its seat
- Prevent the upper structure from separating from the base
- Maintain alignment between the rotating and stationary components
- Provide mounting locations for fasteners
- Connect Joint 1 to Joint 2
- Connect Joint 1 to the supporting surface or robot base

The basic circular form was functional, but the additional mounting features were not developed into a fully organized retention system.

---

## 4. Bearing-Supported Rotation

The rotating section of Joint 1 was supported using a bearing.

The bearing allowed the upper assembly to rotate while carrying the weight of the rest of the robotic arm.

The bearing arrangement must separate the stationary and rotating structures:

- One bearing race must connect to the stationary base.
- The opposite bearing race must connect to the rotating Joint 1 output.
- The two housing sections must not clamp both races together.
- The bearing must remain concentric with the Joint 1 axis.
- The bearing must be retained axially.

The first rendition demonstrated the basic bearing-supported movement, but it did not fully define how the bearing would support all of the expected loads.

Joint 1 may experience:

- Axial load from the weight of the robot
- Radial load from off-centre loading
- Bending moments from the extended arm
- Dynamic loads during acceleration and deceleration
- Reaction torque from the motor and gearbox
- External forces applied to the end effector

The second rendition must select a bearing arrangement capable of supporting these loads.

---

## 5. Gearbox Selection

The Joint 1 design reused the planetary gearbox concept developed for Joint 3.

The Joint 3 gearbox used a two-stage planetary arrangement with approximately:

**6:1 reduction per stage**

The total reduction was approximately:

**6 × 6 = 36:1**

Using the same general gearbox design for Joint 1 provided several benefits:

- Reduced CAD development time
- Reuse of tested planetary gear geometry
- Reuse of common parts
- Easier manufacturing
- Easier replacement of components
- Fewer unique gear and bearing sizes
- Consistent gearbox assembly methods

The Joint 1 planetary gearbox was intended to provide enough torque to rotate the complete robot while maintaining a practical output speed.

However, the final Joint 1 reduction must be confirmed separately.

Joint 1 and Joint 3 do not experience the same loading conditions. Joint 3 must lift the distal arm against gravity, while Joint 1 primarily rotates the complete arm around the vertical axis.

Therefore, the Joint 3 gearbox can be reused as a starting point, but it should not automatically be treated as the final Joint 1 gearbox without additional calculations.

---

## 6. Motor and Gearbox Connection

The motor drives the planetary gearbox, and the gearbox output rotates the upper Joint 1 structure.

The intended power path is:

**Motor → Planetary Gearbox → Joint 1 Output → Remaining Robot**

The gearbox output must be positively connected to the rotating base.

The connection should not rely only on friction between printed components.

Possible methods include:

- Keyed shafts
- Splines
- Bolted flanges
- Cross pins
- Clamping hubs
- Interlocking tabs
- Metal inserts
- Multiple engagement features

The output connection must transfer the complete Joint 1 torque without slipping or twisting.

The gearbox housing must also be prevented from rotating with the output. The stationary section of the gearbox must be securely connected to the stationary Joint 1 base so that the reaction torque is transferred into the robot base.

---

## 7. Joint 1 Retention

The first rendition added several features around the circular structure to keep the rotating assembly secured.

The Joint 1 retention system must perform two separate functions:

1. Allow the upper structure to rotate.
2. Prevent the upper structure from separating from the base.

The second rendition requires a more clearly defined retention method.

Possible retention components include:

- A central retaining shaft
- A shoulder bolt
- A threaded retaining cap
- A locknut
- A bearing spacer
- A retaining ring
- A bolted bearing cover
- An external clamping plate

The retention feature must not apply excessive force across the bearing races.

It should control axial movement while allowing the bearing to rotate freely.

---

## 8. Elements That Worked

Several parts of the first Joint 1 rendition were successful.

### 8.1 Simple Circular Geometry

The 100 mm circular platform provided a simple and appropriate foundation for the rotational base.

### 8.2 Bearing-Supported Rotation

Using a bearing allowed the upper robot structure to rotate without relying on direct plastic-on-plastic contact.

### 8.3 Continuous-Rotation Concept

The absence of immediate physical stops allowed Joint 1 to rotate through a large range.

### 8.4 Reuse of the Joint 3 Gearbox

Reusing the Joint 3 planetary gearbox concept reduced the number of completely unique mechanisms required for the robot.

### 8.5 Limited Mechanical Complexity

The original Joint 1 concept did not depend on a large number of separate moving components.

The main mechanism consisted of:

- A circular base
- A rotating platform
- A bearing
- A motor
- A planetary gearbox
- Mounting and retention features

---

## 9. Problems Identified in the First Rendition

### 9.1 Joint 1 Was Not Fully Developed

The first rendition established the basic shape and rotation, but many important details were not fully designed.

The Joint 1 model requires significant modification before it can be treated as a printable and functional assembly.

### 9.2 Bearing Selection Was Incomplete

The first rendition used a bearing concept without fully determining whether the bearing could support:

- The weight of the robot
- Overturning moments
- Radial loading
- Axial loading
- Dynamic loading

A single bearing may not provide enough resistance to tilting depending on its type and mounting arrangement.

### 9.3 Retention Features Were Unorganized

Several features were added to secure the joint, but the design did not use one clearly defined system for:

- Axial retention
- Bearing retention
- Gearbox mounting
- Output-shaft retention
- Connection to Joint 2
- Connection to the stationary base

The second rendition should simplify these features and give each component a specific purpose.

### 9.4 Gearbox Suitability Was Not Confirmed

The Joint 3 planetary gearbox was connected to Joint 1, but the required Joint 1 ratio was not confirmed independently.

The gearbox may provide more reduction than Joint 1 requires, which could unnecessarily reduce the rotational speed.

Alternatively, the gearbox may not provide enough torque if the arm experiences large rotational inertia or external loads.

### 9.5 Continuous Rotation Was Not Fully Supported

The mechanical structure allowed continuous rotation, but the electrical system did not account for indefinite rotation.

Without a slip ring or another rotary electrical interface, continuous rotation could twist:

- Motor wires
- Encoder wires
- End-effector wiring
- Sensor cables
- Power cables

The final design must either:

- Include a slip ring
- Use a limited rotation range
- Use cable-management geometry that safely limits the movement

### 9.6 Encoder Integration Was Missing

The first rendition did not fully incorporate an encoder for measuring the actual Joint 1 output position.

The encoder should measure the joint after the gearbox so that the controller can detect:

- Actual base position
- Gearbox backlash
- Motor skipping
- Unexpected movement
- Differences between commanded and actual motion

### 9.7 Connection to Joint 2 Was Incomplete

The rotating Joint 1 output must provide a strong and accurately aligned mounting interface for Joint 2.

This connection must support the complete upper structure while transferring Joint 1 rotation into the rest of the robot.

The first rendition did not fully define this interface.

---

## 10. Continuous Rotation and Cable Management

The first rendition allowed Joint 1 to rotate indefinitely from a mechanical perspective.

For true continuous rotation, a slip ring would likely be required.

A slip ring would allow electrical power and signals to pass between the stationary base and the rotating robot structure without continuously twisting the wires.

The slip ring would need to support the required:

- Voltage
- Current
- Number of conductors
- Encoder signals
- Communication signals
- Motor power
- Sensor wiring

The Joint 1 shaft or centre opening should remain hollow if a slip ring or cable-routing path will pass through the middle of the joint.

If a slip ring is not used, Joint 1 should be given a limited movement range and a controlled cable loop.

For example, the motion could be limited to approximately:

**-180° to +180°**

The final movement requirement must therefore be selected before the second rendition is completed.

---

## 11. Encoder Integration

Joint 1 requires an output-side encoder.

The encoder should measure the actual rotation of the Joint 1 output after the planetary gearbox.

The magnet should rotate with the upper Joint 1 structure.

The encoder sensor should remain attached to the stationary base.

The encoder design must define:

- Magnet location
- Magnet orientation
- Sensor location
- Sensor mounting method
- Sensor air gap
- Wire routing
- Protection from the gearbox
- Protection from the bearing
- Access for replacement

If the joint rotates continuously, the encoder must support continuous angular measurement without losing its absolute reference.

The encoder mount should remain concentric with the Joint 1 axis.

---

## 12. Connection to Joint 2

The Joint 2 housing and support structure must mount directly to the rotating Joint 1 output.

The Joint 1 output plate must therefore provide:

- A flat mounting surface
- Accurate alignment features
- Multiple fastener locations
- Sufficient material around the fasteners
- Resistance to bending and twisting
- Clearance for the Joint 2 motor and gearbox
- A cable-routing opening
- Access for assembly tools

The connection should use alignment features in addition to bolts.

Bolts provide clamping force, but they should not be the only features responsible for positioning the Joint 2 housing.

Possible alignment features include:

- Locating pins
- A central boss
- A circular recess
- A shoulder
- Interlocking tabs
- A pilot diameter

This will help keep Joint 2 concentric and prevent the connection from shifting under load.

---

## 13. Base Mounting

The stationary section of Joint 1 must connect securely to the robot base, table, or support platform.

The mounting arrangement should prevent:

- Rotation of the stationary housing
- Tilting of the base
- Translation across the supporting surface
- Loosening caused by repeated direction changes

The stationary base should include:

- Multiple mounting holes
- Adequate spacing between fasteners
- Reinforcement around the mounting locations
- Tool access
- Flat contact with the supporting surface
- Clearance for bolt heads and nuts

The base connection must resist the reaction torque created when Joint 1 accelerates or reverses direction.

---

## 14. Housing Improvements

The Joint 1 housing should be redesigned so that its features follow the actual structural load paths.

Material should be concentrated around:

- Bearing seats
- Gearbox mounts
- Motor mounts
- Base-mounting holes
- Joint 2 mounting locations
- Output-shaft connections
- Retention features

Unnecessary solid material should be removed from low-load areas.

The design may use:

- Ribs
- Webs
- Circular reinforcement
- Radial supports
- Hollow internal sections
- Removable covers

The housing should remain simple while providing enough access for:

- Gearbox installation
- Bearing installation
- Encoder installation
- Cable routing
- Maintenance
- Fastener tightening

---

## 15. Requirements for the Second CAD Rendition

### 15.1 Motion Requirements

- Joint 1 must rotate the complete robotic arm around the vertical axis.
- The final design must define whether Joint 1 uses continuous or limited rotation.
- If rotation is limited, the exact angular range must be defined.
- If rotation is continuous, a slip ring or equivalent rotary electrical connection must be included.
- The rotating structure must not interfere with the stationary base.
- The joint must rotate smoothly through its complete range.

### 15.2 Motor and Reduction Requirements

- The final motor size must be selected based on Joint 1 torque and speed calculations.
- The Joint 3 planetary gearbox may be reused as a starting point.
- The final Joint 1 reduction must be calculated independently.
- Gearbox efficiency must be included in the torque calculation.
- The final reduction must provide enough torque without making Joint 1 unnecessarily slow.
- The motor must remain securely mounted to the stationary structure.
- The gearbox housing must resist reaction torque.

### 15.3 Bearing Requirements

- The Joint 1 bearing arrangement must support the complete weight of the robot above the base.
- The bearing system must resist radial loads and overturning moments.
- The bearing races must connect to the correct rotating and stationary components.
- The bearing must remain concentric with the Joint 1 axis.
- The bearing must be retained axially.
- The housing must not clamp both bearing races together.
- The bearing arrangement should prevent noticeable tilting of the upper assembly.
- A second bearing or larger bearing should be considered if one bearing is insufficient.

### 15.4 Retention Requirements

- The rotating Joint 1 assembly must not separate from the stationary base.
- A dedicated retention feature must control axial movement.
- The retention feature must not prevent rotation.
- The system should use a shoulder, retaining cap, locknut, spacer, retaining ring, or similar method.
- The retention system must be removable for maintenance.
- Fasteners should not protrude unnecessarily.
- Thread-locking or mechanical locking features should prevent loosening.

### 15.5 Output-Connection Requirements

- The gearbox output must be positively connected to the Joint 1 rotating structure.
- The connection must not rely only on friction.
- The output connection must transfer the required torque in both directions.
- The Joint 2 housing must mount securely to the Joint 1 output.
- Alignment features should locate Joint 2 independently of the fasteners.
- The output structure must resist bending and twisting.
- The connection should remain removable.

### 15.6 Encoder Requirements

- Joint 1 must include an output-side encoder.
- The encoder must measure the actual Joint 1 position after the gearbox.
- The magnet must rotate with the Joint 1 output.
- The sensor must remain attached to the stationary base.
- The magnet and sensor must remain concentric.
- The sensor air gap must remain controlled.
- Encoder wiring must remain protected.
- The encoder must support the selected angular range.

### 15.7 Cable-Management Requirements

- A central cable-routing path should be included.
- Motor, encoder, and sensor wires must not rub against rotating components.
- Continuous rotation requires a slip ring or equivalent device.
- Limited rotation requires enough cable length and controlled strain relief.
- Wires must not enter the gearbox or bearing path.
- Cable access should remain available during maintenance.

### 15.8 Housing Requirements

- The circular base concept may be retained.
- The approximate 100 mm diameter may be retained if it satisfies bearing and gearbox packaging.
- The housing must support the gearbox and bearing arrangement.
- Unnecessary mounting features should be removed.
- Every fastener boss and bracket must have a defined purpose.
- The housing should include removable access covers where practical.
- The housing should use efficient ribs instead of unnecessary solid material.
- The design should be printable with minimal support material.
- The housing must connect securely to the stationary base.

### 15.9 SolidWorks Requirements

- Gearbox configurations should be reused where practical.
- Joint 1-specific motor and reduction configurations should be created.
- Bearing-seat tolerances should be configurable.
- Encoder clearances should be included in the assembly.
- Continuous or limited rotation should be represented in the assembly.
- Joint 2 should be assembled onto Joint 1 to check the complete interface.
- The mass and centre of mass of the upper assembly should be included in later calculations.
- Interference between rotating and stationary parts must be checked.

---

## 16. Items Requiring Further Development

The following details must still be determined:

- Final Joint 1 rotation range
- Whether continuous rotation is required
- Slip-ring requirement
- Required Joint 1 torque
- Required Joint 1 speed
- Rotational inertia of the complete arm
- Selected motor
- Motor torque-speed curve
- Final planetary reduction
- Gearbox efficiency
- Gear tooth counts
- Gear backlash
- Gear face width
- Bearing type
- Bearing size
- Number of bearings
- Bearing spacing
- Bearing-seat tolerance
- Bearing-retention method
- Output-shaft diameter
- Output-shaft material
- Gearbox-output connection
- Joint 2 mounting pattern
- Joint 2 alignment features
- Encoder model
- Magnet dimensions
- Sensor air gap
- Cable-routing diameter
- Slip-ring dimensions
- Base-mounting pattern
- Housing wall thickness
- Rib thickness
- Retaining fastener sizes
- Final Joint 1 diameter
- Final Joint 1 height
- Final Joint 1 mass
- Assembly sequence

---

## 17. Main Lessons From the First Rendition

The first rendition demonstrated that Joint 1 could be built around a simple circular bearing-supported base.

The 100 mm circular structure provided an appropriate starting point, and the bearing allowed the complete upper robot assembly to rotate relative to the stationary base.

Reusing the Joint 3 planetary gearbox also provided a practical starting point for the Joint 1 transmission.

However, the design remained incomplete.

The main improvements required for the second rendition are:

- Confirming the required reduction
- Selecting the correct motor
- Designing a complete bearing arrangement
- Creating a proper axial-retention system
- Positively connecting the gearbox output
- Creating a strong Joint 2 interface
- Integrating an output encoder
- Resolving cable twisting
- Deciding between continuous and limited rotation
- Simplifying the added mounting features

The second rendition should not add more features to the original circular plate without a clear plan.

The Joint 1 assembly should instead be redesigned as a complete system containing a stationary base, rotating output, bearing support, gearbox, encoder, retention system, Joint 2 interface, and cable-management path.

---

## 18. Final Conclusion

The first CAD rendition of Joint 1 used a simple 100 mm circular platform supported by a bearing.

This allowed the complete robotic arm to rotate around the vertical axis.

The Joint 3 planetary gearbox concept was connected to Joint 1 to provide a substantial reduction without requiring the development of a completely separate gearbox.

The general concept was simple and functional, but the Joint 1 design requires significant refinement.

The second rendition must define how the bearing carries the complete robot load, how the rotating platform remains connected to the stationary base, how the gearbox output transfers torque, how Joint 2 mounts to the output, and how the encoder and wiring are integrated.

The final design must also determine whether Joint 1 will rotate continuously or use a limited range. Continuous rotation will require a slip ring or another method of preventing cable twisting.

The circular base and reused planetary gearbox remain useful starting points, but Joint 1 must be redesigned as a complete structural and rotational assembly before it is ready for printing.