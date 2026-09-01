<div style="background-color: navy; color: white; padding: 20px; text-align: center;">
  <h1>A2 – Truss Stress Analysis</h1>
</div>

## Objective
Design a lightweight planar truss using A500 steel or an alternative material.

Create free body diagrams (FBDs) for joints and critical pins.

Calculate the required cross-sectional area of truss elements with a safety factor.

Determine pin sizes based on shear forces with a safety factor.

Solve equations symbolically and numerically for both truss and pin design.

Estimate the total weight of the truss and pins.

Create a CAD model with accurate dimensions and connections.

Compare CAD weight predictions with hand calculations.

Document key engineering lessons learned from the process.

## Analyze
#### Description
This project involves developing a complete engineering design and stress analysis of a lightweight planar truss. The analysis begins by interpreting the given loading, support and geometric constraints and using them to develop a stable and statically determinate truss geometry. Free body diagrams (FBDs) and equilibrium equations are utilized to determine support reactions and internal forces within each truss member. 

The calculated member forces will then be used to determine the required cross- sectional area of the truss. The connecting pins wall also be analyzed for shear. Both of these factors will be sized using their specific material properties and factors of safety. The analytical design is translated into a 3D CAD model, allowing the calculated weight to be compared with the mass  predicted by the CAD Software for comparison. 

Throughout the course of this project, I will be documenting every step of the design process, including sketches, calculations, design decisions, revisions, mistakes and observations. 

#### Design Constraints 
Cross sectional area of each element is to be identical. 

The pins are to be identical to each other and each element is to have the same cross-sectional geometry. 

Truss must remain stable and struturally sound under the applied loading. 

The design should minimize weight while satisfying the required safety factor. 

#### Force and Geometric Constrains
<div style="text-align: center;">
  <img src="A2_Design_Constraint.png" alt="Design_Constraint" style="width: 400px; border: 3px solid black;">
</div>

P = Choose a value between 20 - 30 kN 

a = 0.4m

b - 0.3m 

Point A = Pin 

Point B = Roller

#### Background Knowledge 
##### What is a Truss? 
A truss is a structural framework made of straight members connected at joints. In an ideal truss, members are assumed to be connected by frictionless pins, meaning that each member carries either tension or compression. These members work in unison to transfer externally applied loads to supports.

Key Characteristics: 

1. Shape: the design of the truss is crucial as it prevents distortion under stress and offers stability to the structure.
2. Load: trusses are designed to carry axial loads (meaning the forces are balanced along the length of the members).
3. Material: trusses can be composed of various materials, the material composition affects the performance of the overall design.
   
Trusses are essential in engineering and architecture for creating lightweight yet strong structures that can support a significant loading across a large spaces. Trusses are commonly used in applications such as bridges, roofs, towers, etc. 

##### Truss Stability 
A truss must be geometrically stable so that it can support applied loads without deformation (changing shape or behaving like a mechanism). Triangular arrangements are commonly used since it maintains it's shape and the member lengths remain fixed. 

Why Triangles are stronger and more stable than rectangles: 

Triangular geometry makes a truss stable because when a force is applied to one point, the three members work in unison to resist the load primarily through tension and compression. 

Example: 

If a downward force is applied at point A, the force is transferred through the two angled members towards point B and point C. One of more members experience compression, while others experience tension, allowing these forces to balance out within themselves. Since all three sides are connected, the triangle cannot change shape without changing the length of at least one member. 

In comparison rectangles behave differently, if a sideways force is applied to a rectangle it can deform into a parallelogram without changing the length of the members. 

Example: 

If a sideways force is applied to point D, the joints can rotate while the four members remain approximately the same length. This means that a rectangle by itself does not have enough geometric constraint to maintain it's original shape. This also allows the members to experience significant bending when the joints are not properly braced. 

This issue can be easily combated by simply adding a diagonal member to the truss design. 

Example: 

The additional diagonal divides the rectangle into two separate triangles, this change prevents the structure from easily deforming into a parallelogram because the diagonal member constraints the relative position of the joints.  

Moreover, supports provide additional stability to the overall structure. A pin support provides two reaction components, while a roller support provides one reaction component. Together, the three reaction components prevent rigid-body translation and rotation of the truss. 

## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

## Communicate

