# A1 – Build Your Professional Portfolio
## Objective
The objective of this Portfolio is to document my development as an engineer. This will be a demonstration of how I am able to analyze engineering problems, make and defend decisions throughout the design process, and communicate technical information to a general audience. Rather than presenting only projects, this will allow the viewer an insight on the reasoning, assumptions, evidence and decisions made throughout my work. 
This page is organized around three core stages of engineering practices: Analyze, Decide and Communicate. The Analysis section demonstrates how problems are investigated and the development of technical understanding. The Decision section explains how alternatives are evaluated and provides a justification for design choices. The Communication section presents the results in a clear format for the intended audience. 

## Analyze 
### Task A - Portfolio Analysis 
I have analyzed two engineering portfolios in order to identify characteristics that build a strong profile, allowing technical work to be useful to an engineering audience. The main criteria throughout this analysis includes: navigability, reproducibility. evidence of reasoning, and professional tone. These criteria are important because they allow the reader to quickly locate technical work while providing enough evidence to understand how conclusions/decisions were reached.
#### Portfolio 1 - [Aidan Bradley's Engineering Portfolio](https://aocb.github.io/)
Navigability: This portfolio applies a simple structure that allows the viewer to clearly identify the owner, their respective engineering disciple, and project information without excess navigation. 

Reproducibility: While this portfolio successfully outlines the author's engineering work, it lacks a detailed level of technical documentation that would be required for the viewer to completely reproduce the design. 

Evidence of Reasoning: The portfolio communicates the projects and interests of the engineer, however the emphasis on presenting the work rather than the documentation of the decisions made throughout the design process. 

Professional Tone: The author maintains appropriate language throughout the portfolio, fit for an engineering audience while focusing on their academic background, engineering interests and technical projects. 

#### Portfolio 2 - [Nathan Sivalingam's Engineering Portfolio](https://engineering-portfolio-website.vercel.app/)
Navigability:  This portfolio uses a simple and intuitive structure that allows the viewer to clearly identify the owner, their engineering discipline, and project information without excessive navigation. The work is organized into distinct categories, allowing the viewer to navigate directly to the details of each project. 

Reproducibility: This portfolio provides a stronger technical demonstration of the projects presented. The viewer is able to inspect the underlying work rather than relying solely on the author's summary. While details about the design process are provided for each project, there is not sufficient information for the viewer to fully reproduce the designs.

Evidence of Reasoning: The portfolio presents each project with descriptions of what was developed and supporting context surrounding the work. The development process and design decisions are justified for most of the projects presented in the portfolio.

Professional Tone: The portfolio communicates the author's technical skills, education, engineering projects, and professional interests. The author maintains an appropriate tone and uses professional language throughout the portfolio, which is further enhanced by the overall organization and presentation of the site.

### Task B: Product Analysis 
The product selected for this analysis is an IKEA multi-bit screwdriver, a hand-operated mechanical tool designed to driver and remove fasteners with different head configurations. Unlike a conventional screwdriver with a permanently attached tip, the multi-bit design allows the user to select and replace the driver bit depending on the fastener being operated. This is useful because it allows one tool to perform the function of several conventional screwdrivers. 

The screwdriver can be analyzed as three primary component groups:

Handle

Shaft/bit holder

Interchangeable driver bit

Although the tool contains multiple individual bits, the bits are treated as a single component category because each bit performs the same functional role and is interchangeable within the screwdriver. This analysis focuses on how the geometry and interaction of these three components allow the screwdriver to transmit torque from the user's hand to a fastener.

#### Primary Function 
The primary function of the screwdriver is:

To transmit an applied torque from the user's hand to a fastener through the handle, shaft, and driver bit in order to rotate the fastener for installation or removal. 

The user's applied force is converted into rotational motion through the geometry of the handle. This torque is then transferred through the shaft and bit holder to the selected driver bit, which engages with the fastener and applies the resulting torque.

#### Governing Model 
The primary governing relationship for this function is:
##### Torque
T = Fr

where:

T = applied torque (N⋅m)

F = force applied by the user's hand (N)

r = perpendicular distance from the axis of rotation to the applied force (m)

Example: 
For example, if a user applies a 50N tangential force at an effective radius of 0.025m:

T=(50)(0.025)=1.25N⋅m

Therefore, the applied force produces approximately 1.25N⋅m of torque.

##### Shaft Torsion
The shaft is primarily subjected to torsional loading during operation. The resulting torsional shear stress can be modeled using:

τ = Tr/J

where:

τ = torsional shear stress

T = applied torque

r = radial distance from the shaft's center

J = polar moment of inertia

For a solid circular shaft:

J = πd^4/32

where 

J = polar moment of inertia

π = mathematical constant 

d = diameter

This relationship shows that shaft diameter has a significant influence on resistance to torsional deformation.

#### Mechanical Model and Identify Variables 

The user applies a tangential force to the screwdriver handle. Because this force acts at a distance from the rotational axis, it produces torque. The handle transfers this torque to the shaft, which transfers it to the selected driver bit. The driver bit then transfers it to the fastener, allowing it to be fastened/removed. 

Basic force path can be represented as: 
User → Handle → Shaft/Bit Holder → Driver Bit → Fastener

The screwdriver must maintain sufficient structural strength throughout this force path so that the components do not experience excessive deformation or failure during normal use. 

##### Modeling Assumption
Assumption: The screwdriver is assumed to operate under quasi-static loading, with the user's applied force producing primarily torsional loading about the longitudinal axis of the tool. The shaft and driver bit are assumed to remain within their elastic range during normal operation.

This assumption allows the screwdriver to be modeled primarily as a torque-transmitting mechanical system. In actual operation, the screwdriver may also experience bending, contact stresses, and localized stresses at the bit-fastener interface. However, these effects are outside the scope of the simplified model because torsional loading is most directly related to the screwdriver's primary function.

#### Component Geometry and Its Mechanical Function
Handle 

The handle has a larger diameter than the shaft, allowing the user to apply force at a greater distance from the rotational axis. According to T = Fr, this increases the torque that can be generated for a given applied force.

The handle geometry also serves an ergonomic purpose by providing a surface that can be comfortably gripped. Therefore, the handle represents a design tradeoff between torque generation, grip comfort, hand size, material usage, and weight.

Shaft / Bit Holder

The shaft and bit holder transfer torque from the handle to the selected driver bit. The shaft must have sufficient torsional strength to resist deformation while remaining compact enough for practical use.

The bit-holder geometry also needs to securely retain the interchangeable bit while allowing it to be removed and replaced. Therefore, the interface must balance reliable torque transmission with ease of bit replacement.

Interchangeable Driver Bit

The driver bit directly interfaces with the fastener and transfers the torque supplied by the screwdriver into the fastener head. Its geometry is determined by the type and size of fastener it is designed to engage.

A properly matched bit maximizes contact between the bit and fastener and reduces the likelihood of slipping or damaging the fastener. The interchangeable design allows the same screwdriver body to accommodate multiple fastener geometries.

#### Patent Research 

A relevant patent for the multi-bit screwdriver concept is U.S. Patent No. 6,502,484, "Screwdriver with Easily Replaceable Bits," by Lee Pao-Hsi. The patent describes a screwdriver designed around replaceable bits, allowing a single screwdriver assembly to accommodate different types of fasteners. The design addresses the limitations of conventional screwdrivers that require a separate tool for different fastener configurations.

This patent is relevant to the IKEA screwdriver because both designs use the concept of an interchangeable driver bit to increase the versatility of a single screwdriver assembly. The patent demonstrates that the use of replaceable bits is an intentional mechanical design approach rather than simply a convenience feature.

[View U.S. Patent No. 6,502,484](https://patents.google.com/patent/US6502484B2/en)

#### Alternative Solutions 
Fixed-Tip Screwdriver 

A conventional fixed-tip screwdriver accomplishes the same primary function of transmitting torque to a fastener but uses a permanently attached driver tip. This design has fewer components and eliminates the need for an interchangeable connection. However, each screwdriver is limited to a particular tip configuration, requiring users to own multiple screwdrivers for different fasteners.

Ratcheting Multi-Bit Driver 
A ratcheting multi-bit driver also uses interchangeable bits but incorporates a ratcheting mechanism. This allows the user to rotate the fastener without repeatedly repositioning their hand. The design provides greater functionality than the IKEA screwdriver but requires additional components and introduces greater mechanical complexity.

Comparison: These alternatives demonstrate that the same primary function can be achieved through different mechanical designs. The fixed-tip screwdriver prioritizes simplicity, while the ratcheting multi-bit driver prioritizes functionality. The IKEA multi-bit screwdriver occupies a middle ground by providing interchangeable bits while maintaining a relatively simple mechanical system.

#### Design Decision

One significant decision in the IKEA screwdriver is the integration of the interchangeable driver bits rather than a permanently attached tip. I believe this decision was made to increase the versatility of the tool while reducing the number of separate components required by the user. 

While a fixed-tip screwdriver has simpler construction, each tool is limited to one fastener configuration. Whereas the interchangeable-bit design allows the same handle and shaft assembly to accommodate multiple fastener types. This reduces storage requirements and allows the user to carry one tool in place of several. 

However, the interchangeable design introduces an additional mechanical interface between the bit and holder. This connection must reliably transmit torque while preventing excessive movement or disengagement during use. Therefore, the designer traded some mechanical simplicity for increased versatility.

Based on the primary function, governing torque relationship, component geometry, and comparison with alternative solutions, I believe the interchangeable-bit configuration is an effective design choice for a general-purpose household tool. It provides multiple functions without requiring a separate handle and shaft for every fastener type.

## Decide 
##### Homepage Identity 
The homepage is designed to give a visitor an immediate understanding of the purpose, organization, and professional standard of this engineering portfolio. Because the intended readers may include instructors, engineers, and potential employers, the homepage should allow them to quickly identify what type of engineering work is documented and locate the information relevant to them without unnecessary navigation. The portfolio will therefore use structure to organize the engineering work and maintain a consistent navigation system throughout the site. Individual projects and assignments will be clearly labeled and organized into descriptive subsections so that a reader can efficiently navigate to specific technical content. The homepage will also include an About Me section that provides the professional context necessary for the reader to understand the author of the work, while the remainder of the site focuses on documenting the engineering process and supporting evidence.

##### Intentional Customization 
I will customize the portfolio's color scheme to use blue and white as the primary colors. This change is intended to improve visual clarity and maintain a professional appearance without distracting the reader from the technical information. Blue will be used selectively for headings, navigation elements, and other visual indicators, while white will provide a clean background that maintains contrast and readability. This better supports the requirement for technical information to be communicated clearly because the visual design establishes hierarchy without competing with the content. The default template did not provide the same intentional visual hierarchy for distinguishing important sections, so the blue-and-white scheme will provide a consistent visual system throughout the portfolio.

##### Documentation Standard 
Every assignment and project will clearly document the engineering problem, any relevant analysis and evidence, decisions made and their justification, along with the final result. This will be conducted with enough detail so that another engineering reader can understand, evaluate and reproduce my work without relying on information that is not included in the portfolio. 

## Communicate
### About Me 
Arsh Kaur 


