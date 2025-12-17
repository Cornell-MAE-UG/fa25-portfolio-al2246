---
layout: project
title: MAE 4272 Wind Turbine Blade Design
description: MAE 4272 Blade Design
technologies: [Fusion 360, MATLAB, Excel]
image: /assets/images/wind-turbine.png
---

## Project Overview
For this project, we were tasked with designing a wind turbine blade that maximizes aerodynamic efficiency while meeting structural and operational constraints. Our wind turbine blade should be designed to operate at low Reynolds numbers. Our group chose to maximize aerodynamic efficiency to optimize the power output and improve the performance from the baseline design provided in Lab 4. Our blade must also adhere to the following constraints:
- Blade length or rotor radius must be less than 6 in.
- Axial clearance must be less than 2 in. from the nacelle
- In operation the blade rotation rate must be below 3500 RPM, the torque must be less than 3.5 Ncm, and the wind tunnel must operate at less than 15 Hz which is about 9.8 m/s
- Blade must be able to integrate with the provided hub attachment piece
- Maximum bending flexural stress must be less than 44 MPA
In addition to prioritizing the power generation of our blade, we also had to ensure that our design was structurally reliable with a smooth manufacturable geometry. 

## Design Process
From the constraints the blade rotor radius was decided to be 6 in. because a larger radius allows for more power generation. The rated wind speed, tip speed ratio, and rated rotation rate was first chosen. The rated wind speed of 5 m/s was chosen because it was the wind speed with the highest frequency from the provided Weibull distribution. The tip speed ratio was chosen to be 6 which is within the typical range for a 3 bladed horizontal axis wind turbine. And finally the rotation rate was found to be 1880 RPM which is found from the tip speed ratio, rated wind speed, and blade rotor radius. 
The airfoil shape selected was SG6043 based on its high lift coefficient, ease of printability, and structurally strong thickness. The optimal angle of attack is 7° which is where the lift is maximized and the drag is minimized. 
Once these important parameters were decided the blade element momentem (BEM) equations for an optimal rotor without wake rotation were used to find the chord and section twist angle distributions. This distribution was adjusted to an average of the BEM chord distribution with a linear chord taper in order to obtain a higher factor of safety for the flexural stress which was calculated in a MATLAB script that estimates the blade as a rectangular beam. These iterations of the chord distribution helped to give us confidence that our blade would not break during testing so we can obtain the necessary data to quantitavely observe our blades performance. The final blade design CAD model is shown in Figure 1 below. 
<p align="center">
  <img src="{{ '/assets/images/blade.png' | relative_url }}"
       alt="blade"
       width="450"/><br>
  <em><strong>Figure 1.</strong> CAD Model of Final Blade Design</em>
</p>

## Testing Summary
Our blade was tested in the wind tunnel in Upson 256 at the following wind speeds: 3.0 m/s, 4.0 m/s, 4.5 m/s, 5.0 m/s, 5.5 m/s. The torque brake RPM was slowly increased until the blade stalled. The LabView VI from Lab 4 was used to collect data. From the data, the Power (W) was plotted against the Rotation Rate (RPM) at each wind speed to obtain a power curve. All the power curves are compiled into one graph shown in Figure 2. 
<p align="center">
  <img src="{{ '/assets/images/power-curves.png' | relative_url }}"
       alt="power-curves"
       width="450"/><br>
  <em><strong>Figure 2.</strong> Experimental Power Curves for Different Wind Speeds</em>
</p>
The testing allowed us to evaluate the aerodynamic performance and structural reliability of our blade at varying wind speeds that are frequently experienced. An issue that came up in testing was that the blade had trouble starting up and a small force had to be applied by hitting the wind tunnel in order to get the blade rotating. Addtionally, we ran out of time towards the end so the wind tunnel was not given a lot of time to adjust in between rotation rates. 

## Next Steps
Our blade design achieved our objectives of no visable deformations in our printed blades, not failing during testing, and producing more power than the original blade tested in Lab 4. To improve our project the next steps would be to redesign the blade using BEM equations for optimal rotor with wake so the blade is more applicable to real world situations and also to test the blade at more wind speeds to obtain more data to create a full Weibull distribution to find the annual power production. It might also be helpful to perform a computational fluid dynamics simultion in ANSYS Fluent to validate the experimental results with another source.

## Personal Contributions
- Researched different airfoils and analyzed aerodynamic and structural characteristics
- Compiled blade element momentum (BEM) theory equations into Excell sheet to solve for chord and section twist angle distributions
- Operated wind tunnel during experimenent and observed when turbine blade stalls
- Contributed to elevator pitch, presentation, and design report writing
