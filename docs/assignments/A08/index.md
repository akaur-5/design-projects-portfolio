# A8 – Gears

## Objective
- Design a gearbox that can be assembled and disassembled.
  
- Analyze and size input and output shafts for strength.

- Design journal bearings to support shafts.

- Create a gearbox housing with proper clearance and fastening.

- Use parametric CAD modeling to generate a final design.

- Document calculations, sketches, and lessons learned.

## Analyze
#### Description
- Design a gearbox which can be assembled and disassembled. The spur gears have a gear ratio of 24:9 and are listed in the resource section. The output gear torque and speed are to be 1.25 in-lbf and 1100 rpm.

- Assumptions:
Assume appropriate strength of shafts, use Machinery’s Handbook.
The gear train is ideal.
The moment of the radial force from the gear train is small enough to be ignored.

#### Design Constraints 
|Component|Input|Output|
|---------|-----|------|
|Gear|Pinion|Gear|
|Gear Ratio|9 teeth|24 teeth|
|Shaft Diameter|0.125 in|0.250 in|
|Shaft Length| 1 in| 1 in|
|Torque| Calculate| 1.25 in-lbf|
|Speed| Calculate| 1100 rpm|

#### Background Knowledge 
<h5 style="font-size: 18px; color: navy;">What is a Gearbox?</h5>

A gearbox is a mechanical system that transfers rotational power from one shaft to another using gears. The two important components include:
  1. Pinion: the smaller driving gear connected to the input shaft.
  2. Gear: the larger driven gear connected to the output shaft.

Once the pinion rotates, its teeth push against the teeth of the larger gear, causing it to rotate in the opposite direction. Gears allow us to change the relationship between rotational speed and torque.

For example: a smaller pinion rotates faster, while a larger gear rotates slower; however, the larger gear produces more torque (speed reduction).

This website contains an interactive animation that presents this phenomenon: [Click Here.](https://www.firgelliauto.com/blogs/mechanisms/spur-gears?srsltid=AYCX9vIklASGvxygUrVqilr2I9KkZdLuprjonFHcWoAA)

<h5 style="font-size: 18px; color: navy;">Gear Terminology</h5>

<div style="text-align: center;">
  <img src="A8_gear_terminology.jpg" alt="Gear Terminology" style="width: 400px; border: 3px solid black;">
</div>

Terminology Description:

| No. | Gear Terminology | Description and Engineering Significance | Relevant Formulas |
|---|---|---|---|
| 1 | **Face Width** | The axial width of the gear tooth, measured parallel to the rotational axis. It determines the width of the tooth surface available to transmit loads. | No direct geometric formula. |
| 2 | **Profile Line** | Represents the geometric profile of the gear tooth. For a standard involute gear, the tooth profile determines how adjacent teeth engage and transmit motion. | Involute function: $\theta = \tan(\phi) - \phi$ |
| 3 | **Flank Line** | Represents the line associated with the flank geometry along the gear tooth. The flank forms part of the working tooth profile. | No direct formula. |
| 4 | **Addendum Circle** | The circle passing through the outermost tips of the gear teeth. It defines the outside diameter of the gear. | $D_a = D + 2a$ |
| 5 | **Topland** | The top surface of an individual gear tooth, located between the two tooth flanks. | No direct formula. |
| 6 | **Face** | The portion of the gear tooth surface located above the pitch circle. It extends from the pitch circle toward the tooth tip. | No direct formula. |
| 7 | **Flank** | The portion of the gear tooth surface located below the pitch circle. It extends from the pitch circle toward the tooth root. | No direct formula. |
| 8 | **Pressure Angle** | The angle between the line of action of the transmitted tooth force and the tangent to the pitch circle. It determines the relationship between tangential and radial gear forces. | $\phi$ |
| 9 | **Whole Depth** | The total radial depth of a gear tooth, measured from the addendum circle to the dedendum circle. | $h_t = a + b$ |
| 10 | **Tooth or Working Depth** | The depth of engagement between two mating gear teeth. It is the sum of the addenda of the two mating gears. | $h_w = a_1 + a_2$ |
| 11 | **Clearance Circle** | The circle associated with the clearance boundary near the tooth root. It represents the space provided for the mating gear’s tooth tips. | Related to clearance: $c = b - a_m$ |
| 12 | **Slot Width** | The width of the space between two adjacent teeth, measured along the pitch circle. | $s = p - t$ |
| 13 | **Tooth Thickness** | The width of an individual gear tooth, measured along the pitch circle. It is important for tooth engagement and backlash. | $t \approx p/2$ |
| 14 | **Clearance** | The radial distance between the tooth tip of one gear and the root of its mating gear when properly meshed. | $c = b - a_m$ |
| 15 | **Dedendum Circle** | The circle passing through the roots of the gear teeth. It defines the root diameter of the gear. | $D_f = D - 2b$ |

Additional Gear Terminology

| Gear Terminology | Description and Engineering Significance | Relevant Formulas |
|---|---|---|
| **Pitch Circle / Reference Circle** | The theoretical circle used to establish the rolling relationship between two meshing gears. It is the reference for calculating gear ratios, pitch diameters, and tooth spacing. | $D = \frac{N}{P_d}$ |
| **Circular Pitch** | The distance measured along the pitch circle between corresponding points on adjacent teeth. It determines the spacing between gear teeth. | $p = \frac{\pi D}{N} = \frac{\pi}{P_d}$ |
| **Addendum** | The radial distance between the pitch circle and the addendum circle. It represents the height of the tooth above the pitch circle. | $a = \frac{1}{P_d}$ |
| **Dedendum** | The radial distance between the pitch circle and the dedendum circle. It represents the depth of the tooth below the pitch circle. | $b = \frac{1.2}{P_d}$ |
| **Module** | A metric gear-sizing parameter representing the pitch diameter divided by the number of teeth. It determines the relative size of the gear teeth. | $m = \frac{D}{N}$ |
| **Diametral Pitch** | The number of gear teeth per inch of pitch diameter. It is used in US customary gear design and determines tooth size. | $P_d = \frac{N}{D}$ |
| **Gear Ratio** | The ratio between the number of teeth on the driven gear and the driving pinion. It determines the relationship between input and output speed and torque. | $GR = \frac{N_g}{N_p} = \frac{D_g}{D_p}$ |
| **Center Distance** | The distance between the rotational centerlines of two meshing external spur gears. It determines the positioning of the shafts and bearing locations within the housing. | $C = \frac{D_g + D_p}{2}$ |

<h5 style="font-size: 18px; color: navy;">Gear Ratio</h5>

The gear ratio tells us how much the rotational speed and torque change between two gears.

$$
GR = \frac{N_g}{N_p} = \frac{D_g}{D_p}
$$

Where:
- $N_g$ = number of teeth on the output gear
- $N_p$ = number of teeth on the input pinion
- $D_g$ = output gear pitch diameter
- $D_p$ = input pinion pitch diameter

<h5 style="font-size: 18px; color: navy;">Torque</h5>

Torque is the rotational equivalent of force.

$$
T = Fr
$$

Where:
- $T$ = torque (in-lbf)
- $F$ = tangential force (lbf)
- $r$ = distance from the center of rotation (in)

If the gear train is ideal, torque and speed are related by conservation of power:

$$
T_p n_p = T_g n_g
$$

<h5 style="font-size: 18px; color: navy;">Power</h5>

Power describes how quickly work is being performed. For rotational systems, it depends on both torque and rotational speed.

$$
HP = \frac{Tn}{63025}
$$

Where:
- $HP$ = horsepower
- $T$ = torque (in-lbf)
- $n$ = rotational speed (rpm)

If the gear train is ideal, then $HP_{in} = HP_{out}$. In an actual gearbox, friction and other losses would cause the output power to be lower.

<h5 style="font-size: 18px; color: navy;">Gear Tooth Forces</h5>

This is significant because the gear forces are what create bending in the shafts. When two spur gears mesh, the teeth exert a force on one another. This contact force can be resolved into two components:

<div style="text-align: center;">
  <img src="A8_gear_tooth_force.jpg" alt="Gear Force" style="width: 400px; border: 3px solid black;">
</div>

1. Tangential Force ($F_t$)
   This is the force that transmits torque between the gears.

   $$
   F_t = \frac{T}{r}
   $$

   or using the pitch diameter:

   $$
   F_t = \frac{2T}{D}
   $$

2. Radial Force ($F_r$)
   This force pushes the gears away from one another.

   $$
   F_r = F_t \tan(\phi)
   $$

Total tooth Force (F_n)= F_t/cos(phi)

These forces are important because the tangential force produces torque and contributes to shaft bending. Radial force produces a seperating load and also contributes to shaft bending. The bearings react to the forces transmitted through the shafts. 


<h5 style="font-size: 18px; color: navy;">Shaft Design and Stress Analysis</h5>

Shafts transmit rotational power while supporting components such as gears and bearings. They experience two primary types of loading: torsion from transmitted torque and bending from gear forces.

**1. Torsional Shear Stress**

Torsion occurs when torque causes a shaft to twist.

$$
\tau_{max} = \frac{Tc}{J}
$$

For a solid circular shaft:

$$
\tau_{max} = \frac{16T}{\pi d^3}
$$

**2. Bending Stress**

Bending occurs when transverse forces act on the shaft, causing it to deflect.

$$
\sigma_b = \frac{Mc}{I}
$$

For a solid circular shaft:

$$
\sigma_b = \frac{32M}{\pi d^3}
$$

**3. Combined Stress**

Since the shafts experience both bending and torsion, their combined stress must be evaluated. The Von Mises failure criterion can be used to determine the equivalent stress.

$$
\sigma_{VM} = \sqrt{\sigma_b^2+3\tau^2}
$$

**4. Factor of Safety**

The factor of safety compares the material's yield strength with the calculated equivalent stress.

$$
n = \frac{S_y}{\sigma_{VM}}
$$

Where:
- $\tau$ = torsional shear stress (psi)
- $\sigma_b$ = bending stress (psi)
- $\sigma_{VM}$ = Von Mises stress (psi)
- $T$ = applied torque (in-lbf)
- $M$ = maximum bending moment (in-lbf)
- $d$ = shaft diameter (in)
- $S_y$ = material yield strength (psi)

Free-body diagrams (FBDs) and static equilibrium equations are used to determine bearing reactions and bending moments. The calculated stresses are compared against the material's allowable strength to determine whether the specified shaft diameters are sufficient.

<h5 style="font-size: 18px; color: navy;">Journal Bearing Design</h5>

Journal bearings are cylindrical sleeves that support rotating shafts through sliding contact. They maintain shaft alignment while reducing friction and wear.

The primary design considerations include bearing pressure, sliding velocity, and the pressure-velocity (PV) rating.

**1. Projected Bearing Pressure**

Bearing pressure is calculated using the radial load divided by the projected bearing area.

$$
P = \frac{W}{LD}
$$

**2. Sliding Velocity**

Sliding velocity describes how quickly the shaft surface moves against the stationary bearing.

$$
V = \frac{\pi Dn}{12}
$$

**3. Pressure-Velocity Rating**

The PV value combines bearing pressure and sliding velocity to evaluate bearing operating conditions.

$$
PV = P \times V
$$

Where:
- $P$ = projected bearing pressure (psi)
- $W$ = radial bearing load (lbf)
- $L$ = bearing length (in)
- $D$ = shaft diameter (in)
- $V$ = sliding velocity (ft/min)
- $n$ = rotational speed (rpm)

The calculated PV value must remain within the manufacturer's allowable rating for the selected bearing material and operating conditions.

**4. Bearing Material and Thickness**

Bearing materials are selected based on wear resistance, friction, lubrication requirements, temperature limitations, and allowable PV ratings. Common materials include bronze, oil-impregnated bronze, and engineered polymers.

The bearing wall thickness is determined by evaluating the stresses acting on the sleeve and ensuring sufficient material strength.

For a cylindrical sleeve:

$$
t = \frac{D_o-D_i}{2}
$$

Where:
- $t$ = bearing wall thickness (in)
- $D_o$ = bearing outside diameter (in)
- $D_i$ = bearing inside diameter (in)

The final thickness must also account for the loading model and structural requirements specified in the course.

<h5 style="font-size: 18px; color: navy;">Mechanical Fits and Tolerances</h5>

Mechanical fits determine how two components interact when assembled. Proper fits are necessary to maintain alignment, prevent unwanted movement, and allow components to operate as intended.

The gearbox requires two primary fits:

1. **Press Fit (Interference Fit):** The shaft diameter is larger than the gear hub bore, securing the gear to the shaft and preventing relative rotation.

2. **Running Clearance Fit:** The bearing bore is slightly larger than the shaft diameter, allowing the shaft to rotate freely.

**Diametral Clearance:**

$$
C_d = D_{hole}-D_{shaft}
$$

**Radial Clearance:**

$$
C_r = \frac{C_d}{2}
$$

Manufacturing tolerances define the acceptable variation in component dimensions. Critical features, including shaft diameters, bearing bores, and housing pockets, require appropriate tolerances to ensure proper assembly and alignment.

Engineering drawings will follow ASME Y14.5 dimensioning and tolerancing standards.

<h5 style="font-size: 18px; color: navy;">Gearbox Housing Design</h5>

The gearbox housing encloses and supports the internal components while maintaining proper gear alignment and rotational clearance.

The distance between the two shaft centerlines is determined using the gear pitch diameters.

**Gear Center Distance:**

$$
C = \frac{D_p+D_g}{2}
$$

The housing must provide:
- Adequate radial and axial clearance around the gears.
- Properly aligned bearing seats.
- Sufficient structural support for the shafts and bearings.
- Secure fastening between the two housing halves.
- Accessibility for assembly and disassembly.

A two-piece bolted housing with locating features is a suitable design approach because it allows access to the internal components while maintaining alignment.


## Decide
<h5 style="font-size: 18px; color: navy;">Parametric CAD Modeling and Engineering Drawings</h5>

Parametric CAD modeling uses dimensions, constraints, and relationships to create adjustable solid models. Critical dimensions, such as shaft diameters, bearing locations, and gear center distance, should be controlled through defined parameters.

Individual components are modeled or imported before being combined into a complete assembly.

The final CAD assembly should demonstrate:
- Correct positioning and alignment of gears and shafts.
- Proper bearing and housing interfaces.
- Adequate component clearances.
- Functional assembly and disassembly.

Engineering drawings communicate the final design through third-angle orthographic projections, complete dimensions, appropriate tolerances, and assembly details.
## Communicate
