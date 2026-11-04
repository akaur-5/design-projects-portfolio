# A8 – Gears

## Objective
- Design a gearbox that can be assembled and disassembled.
  
- Analyze and size input and output shafts for strength.

- Design journal bearings to support shafts.

- Create a gearbox housing with proper clearance and fastening.

- Use parametric CAD modeling to generate a final design.

- Document calculations, sketches, and lessons learned.

## Analyze
####Description
- Design a gearbox which can be assembled and disassembled. The spur gears have a gear ratio of 24:9 and are listed in the resource section. The output gear torque and speed are to be 1.25 in-lbf and 1100 rpm relative. The input (pinion,power-transmission) and output (gear, short shaft) shaft diameters are .125 and .25 inches respectively and each have a length of 1 inch. Use the appropriate equations in the Machinery’s Handbook for empirical units. The critical features of the gearbox include the shafts, and the journal bearings.

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

A gearbox is a mechanical system that transfers rotational power from one shaft to another using  gears. The two important components include: 
  1. Pinion: the smaller driving gear connected to the input shaft.
  2. Gear: the larger driven gear connected to the output shaft.

Once the pinion rotates, it's teeth push against the teeth of the larger gear, causing it to rotate in the opposite direction. Gears allow us to change the relationship between rotational speed and torque.

For example: a smaller pinion rotates faster, meanwhile a larger gear rotates slower, however the larger gear produces more torque (speed reduction).

This website contains an interactive animation that presents this phenomena: [Click Here.](https://www.firgelliauto.com/blogs/mechanisms/spur-gears?srsltid=AYCX9vIklASGvxygUrVqilr2I9KkZdLuprjonFHcWoAABqYWqdxKxEUO)

<h5 style="font-size: 18px; color: navy;">GearTerminology</h5>

<div style="text-align: center;">
  <img src="A8_gear_terminology.jpg" alt="Gear Terminology" style="width: 400px; border: 3px solid black;">
</div>

Terminology Description: 
| No. | Gear Terminology | Description and Engineering Significance | Relevant Formulas |
|:---:|---|---|---|
| 1 | **Face Width** | The axial width of the gear tooth, measured parallel to the rotational axis. It determines the width of the tooth surface available to transmit loads. | No direct geometric formula. |
| 2 | **Profile Line** | Represents the geometric profile of the gear tooth. For a standard involute gear, the tooth profile determines how adjacent teeth engage and transmit motion. | Involute function: $\operatorname{inv}(\phi)=\tan(\phi)-\phi$ (angle in radians). |
| 3 | **Flank Line** | Represents the line associated with the flank geometry along the gear tooth. The flank forms part of the working tooth profile. | No direct formula. |
| 4 | **Addendum Circle** | The circle passing through the outermost tips of the gear teeth. It defines the outside diameter of the gear. | $D_a=D+2a$ |
| 5 | **Topland** | The top surface of an individual gear tooth, located between the two tooth flanks. | No direct formula. |
| 6 | **Face** | The portion of the gear tooth surface located above the pitch circle. It extends from the pitch circle toward the tooth tip. | No direct formula. |
| 7 | **Flank** | The portion of the gear tooth surface located below the pitch circle. It extends from the pitch circle toward the tooth root. | No direct formula. |
| 8 | **Pressure Angle** | The angle between the line of action of the transmitted tooth force and the tangent to the pitch circle. It determines the relationship between tangential and radial gear forces. | $F_r=F_t\tan(\phi)$ |
| 9 | **Whole Depth** | The total radial depth of a gear tooth, measured from the addendum circle to the dedendum circle. | $h_t=a+b$ |
| 10 | **Tooth or Working Depth** | The depth of engagement between two mating gear teeth. It is the sum of the addenda of the two mating gears. | $h_w=a_1+a_2$ |
| 11 | **Clearance Circle** | The circle associated with the clearance boundary near the tooth root. It represents the space provided for the mating gear's tooth tips. | Related to clearance: $c=b-a_m$ |
| 12 | **Slot Width** | The width of the space between two adjacent teeth, measured along the pitch circle. | $s=p-t$ (with consistent arc measurements and zero backlash). |
| 13 | **Tooth Thickness** | The width of an individual gear tooth, measured along the pitch circle. It is important for tooth engagement and backlash. | $t\approx p/2$ (standard nominal geometry with zero backlash). |
| 14 | **Clearance** | The radial distance between the tooth tip of one gear and the root of its mating gear when properly meshed. | $c=b-a_m$ |
| 15 | **Dedendum Circle** | The circle passing through the roots of the gear teeth. It defines the root diameter of the gear. | $D_f=D-2b$ |

Additional Gear Terminology

| Gear Terminology | Description and Engineering Significance | Relevant Formulas |
|---|---|---|
| **Pitch Circle / Reference Circle** | The theoretical circle used to establish the rolling relationship between two meshing gears. It is the reference for calculating gear ratios, pitch diameters, and center distance. | $D=\frac{N}{P_d}$ |
| **Circular Pitch** | The distance measured along the pitch circle between corresponding points on adjacent teeth. It determines the spacing between gear teeth. | $p=\frac{\pi D}{N}=\frac{\pi}{P_d}$ |
| **Addendum** | The radial distance between the pitch circle and the addendum circle. It represents the height of the tooth above the pitch circle. | $a=\frac{1}{P_d}$ |
| **Dedendum** | The radial distance between the pitch circle and the dedendum circle. It represents the depth of the tooth below the pitch circle. | $b=\frac{1.2}{P_d}$ |
| **Module** | A metric gear-sizing parameter representing the pitch diameter divided by the number of teeth. It determines the relative size of the gear teeth. | $m=\frac{D}{N}$ |
| **Diametral Pitch** | The number of gear teeth per inch of pitch diameter. It is used in US customary gear design and determines tooth size. | $P_d=\frac{N}{D}$ |
| **Gear Ratio** | The ratio between the number of teeth on the driven gear and the driving pinion. It determines the relationship between input and output speed and torque. | $GR=\frac{N_g}{N_p}=\frac{D_g}{D_p}$ |
| **Center Distance** | The distance between the rotational centerlines of two meshing external spur gears. It determines the positioning of the shafts and bearing locations within the housing. | $C=\frac{D_p+D_g}{2}$ |

<h5 style="font-size: 18px; color: navy;">Gear Ratio</h5>

The gear ratio is responsible for telling us how much the rotational speed and torque change between two gears. 

$GR=\frac{N_g}{N_p}=\frac{D_g}{D_p}$

Where: 
N_g= number of teeth on the output gear
N_p= number of teeth on input pinion
D_g=output gear pitch diameter 
D_p=input pinion pitch diameter

<h5 style="font-size: 18px; color: navy;">Torque</h5>

Torque is the rotational equivalent of force. 

$T=Fr$

Where: 
T= Torque (in-lbf)
F= tangential force (lbf)
r= distance from the center of rotation (in)

If gear train is ideal, torque and speed are related by conservation of power: T_pn_p=T_gn_g

<h5 style="font-size: 18px; color: navy;">Power</h5>
Power describes how quickly work is being performed, for rotational systems it depends on both torque and rotational speed. 

$HP=\frac{T}{n}=\frac{63025}$

Where:
HP= horsepower 
T= torque (in-lbf)
n= rotational speed (rpm)

If the gear train is ideal then: HP_input = HP_output. In an actual gearbox, friction and other losses would cause the output power to be lower. 

## Decide


## Communicate

