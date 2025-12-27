---
title: "Satellite ADCS Simulator"
layout: default
---

# Satellite ADCS Simulator

<img src="{{ site.baseurl }}/assets/images/svc_image.png"
     alt="NASA PIA11448"
     style="max-width: 520px; width: 100%; height: auto; display: block; margin: 1.25rem auto 2rem auto; border-radius: 12px;" />




<br>


## Satellite Attitude Determination and Control System (ADCS) Simulator

Designed and simulated a full 3-axis Attitude Determination and Control System (ADCS) for a Low Earth Orbit (LEO) spacecraft, focusing on the Early Orbit Phase (EOP). The system autonomously detumbles the spacecraft after injection, transitions actuator modes based on power constraints, and achieves nadir-pointing using a Lyapunov-based control law.

The simulation was implemented in MATLAB/Simulink and includes rigid-body dynamics, quaternion kinematics, realistic sensor models, actuator saturation, and orbital mechanics.

<br>

### System Architecture

The ADCS simulation is composed of the following subsystems:

- Rigid-body rotational dynamics
- Quaternion attitude kinematics
- B-dot detumbling controller (MTQs)
- Lyapunov attitude controller (Reaction Wheels)
- Gravity-gradient torque disturbance
- Orbital propagation and nadir reference generation
- Sensor models (gyro, sun sensor, magnetometer)
- Actuator models with torque and speed saturation

<br>

### Control Strategy

During the Early Orbit Phase, the spacecraft initially tumbles after deployment. A B-dot controller using three magnetorquers is employed to reduce angular velocity to below 0.25 RPM while conserving power.

After 15 orbital periods, magnetorquers are disabled and a Lyapunov-based control law activates a redundant four-wheel reaction wheel array in a pyramidal configuration. The controller drives the spacecraft toward a nadir-pointing attitude by aligning the +b̂3 body axis with the Earth-center direction.

This staged control approach reflects realistic mission constraints where high-power actuators are deferred until the spacecraft is sufficiently detumbled.

<br>

### Results & Performance

- Spacecraft angular velocity reduced below 0.25 RPM within the first orbit
- Successful detumbling achieved using magnetorquers alone
- Stable transition from MTQ to reaction wheel control after 15 orbits
- Quaternion convergence confirms achievement of the desired nadir-pointing attitude
- Actuator saturation limits respected for both MTQs and reaction wheels

Observed torque and angular velocity spikes during mode transition highlight areas for future controller refinement.


