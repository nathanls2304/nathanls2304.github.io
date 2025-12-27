---
title: "Project ASTRA"
layout: default
---

# Project ASTRA

<img src="{{ site.baseurl }}/assets/images/astra_pic.png"
     alt="ASTRA logo"
     style="max-width: 520px; width: 100%; height: auto; display: block; margin: 1.25rem auto 2rem auto; border-radius: 12px;" />

<br>

## Atmospheric - Satellite - Trajectory - Repositioning - Attachment
Project A.S.T.R.A. proposes an expandable CubeSat attachment capable of modulating atmospheric drag to perform orbital maneuvers. This drag-based control mechanism aims to facilitate orbital adjustments such as space rendezvous in Low Earth Orbit (LEO) and controlled deorbit of a CubeSat without the use of propulsion systems. 

<br>

### Project Context

Low Earth Orbit is becoming increasingly congested, and many CubeSats lack propulsion systems due to mass, power, and cost constraints. This limits their ability to perform orbital maneuvers, avoid debris, or comply with post-mission deorbit requirements.

Project ASTRA explores an alternative approach: using **controlled atmospheric drag modulation** to enable orbital repositioning and accelerated deorbiting without the need for traditional propulsion.

<br>

### System Overview

ASTRA is a 2U CubeSat attachment designed to modulate aerodynamic drag by deploying and rotating a membrane sail using a single actuator. By varying the sail deployment angle, the system alters the effective drag coefficient and center of pressure, enabling passive orbital maneuvers.

**Key system features:**
- Retractable tape-spring booms with deployable membrane sail
- Single-actuator drag modulation mechanism
- Independent flight computer for deployment and control
- Mechanical, electrical, and control interfaces with a 1U parent CubeSat


<img src="{{ site.baseurl }}/assets/images/astra_curent_design.png"
     alt="ASTRA Current Design"
     style="max-width: 520px; width: 100%; height: auto; display: block; margin: 1.25rem auto 2rem auto; border-radius: 12px;" />
     
<img src="{{ site.baseurl }}/assets/images/astra_modulation.png"
     alt="ASTRA Modulation"
     style="max-width: 520px; width: 100%; height: auto; display: block; margin: 1.25rem auto 2rem auto; border-radius: 12px;" />


<br>

### My Role

I served as a **Controls and Dynamics Engineer**, with responsibilities including:

- Stability analysis of the combined CubeSat + attachment system
- Aerodynamic torque modeling using an Aerotorque MATLAB framework
- Evaluation of passive stability as a function of sail deployment angle
- Control systems trade studies for deployment verification sensors
- Flight computer trade study and interface considerations

<br>

### Stability and Dynamics Analysis

Aerodynamic stability was evaluated by analyzing how the center of pressure shifts relative to the spacecraft center of mass as the sail deployment angle changes. A MATLAB simulation based on Aerotorque computed aerodynamic forces and moments acting on each exposed surface in free molecular flow.

Initial results showed that increasing the sail angle moves the center of pressure downstream, generating restoring aerodynamic moments that passively stabilize the spacecraft. Maximum passive stability occurred at deployment angles between approximately 30° and 40°.

<img src="{{ site.baseurl }}/assets/images/astra_cpwing.png"
     alt="ASTRA CP Wing"
     style="max-width: 520px; width: 100%; height: auto; display: block; margin: 1.25rem auto 2rem auto; border-radius: 12px;" />

<br>

### Modeling and Simulation Tools

- MATLAB (Aerodynamic torque modeling, stability analysis)
- Monte Carlo simulations for uncertainty in mass, area, and deployment angle
- Sentman flat-plate drag theory for free molecular flow
- NRLMSISE-00 atmospheric density model
- Preliminary CFD analysis to assess limitations of continuum assumptions in LEO

<br>

### Initial Results

- Observed controlled variation of effective drag coefficient through sail angle modulation
- Initial passive aerodynamic stability trends through center-of-pressure behavior
- Preliminary predicted deorbit timelines on the order of weeks from ~400 km altitude
- Identified CFD limitations in rarefied flow regimes, reinforcing DSMC/Sentman-based approaches

<br>

### Engineering Tradeoffs and Lessons Learned

- Drag-based maneuvering offers simplicity but limited control authority
- Single-actuator architectures significantly reduce mass and complexity
- Deployment angle control provides meaningful stability benefits with minimal power usage
- CFD tools are poorly suited for free molecular flow without DSMC methods



*This project represents a conceptual and analytical design study and was not intended for flight.*
