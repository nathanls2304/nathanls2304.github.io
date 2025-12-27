---
title: "Synthetic Aperture Radar Mission Proposal"
layout: default
---

# JSSAR – Jack Sparrow Synthetic Aperture Radar

This project was a university-based mission design and systems engineering exercise focused on developing a conceptual Low Earth Orbit (LEO) Synthetic Aperture Radar (SAR) satellite constellation for maritime monitoring.

The work emphasized system-level trade studies, subsystem interfaces, and mission feasibility rather than flight-ready implementation. All analyses were conducted using publicly available data and open literature and were not intended for operational deployment.


<img src="{{ site.baseurl }}/assets/images/jssar_patch.png"
     alt="JSSAR Mission Patch"
     style="max-width: 520px; width: 100%; height: auto; display: block; margin: 1.25rem auto 2rem auto; border-radius: 12px;" />


<br>

### My Role – Communications Engineer

I was responsible for the **communications and ground segment architecture**, including:

- S-band TT&C uplink/downlink architecture
- X-band payload data downlink strategy for SAR imagery
- Ground station selection and coverage analysis
- Data storage and processing pipeline design
- Identification of bandwidth, latency, and congestion risks


<br>

### Ground Segment and Data Flow

The mission architecture separates low-rate command and telemetry from high-rate SAR data downlink:

- **S-band** used for TT&C to ensure reliability and global availability
- **X-band** used for high-throughput SAR payload data
- Distributed ground stations selected to minimize data latency
- Data archived and processed using cloud-based storage and analytics

<br>

### Key Communications Challenges

- High SAR data volumes creating onboard storage and downlink bottlenecks
- Frequency congestion in S-band and X-band over high-traffic regions
- Limited ground contact times requiring efficient scheduling
- Atmospheric losses (e.g., rain fade) impacting X-band reliability

<br>

### Engineering Trade Studies

Several trade studies were conducted at a system level, including:

- S-band vs X-band allocation for command vs payload data
- Centralized vs distributed ground station architectures
- Onboard data storage vs real-time downlink prioritization
- Cost, complexity, and scalability tradeoffs for constellation growth

<br>

### Systems Engineering Perspective

This project required balancing competing constraints across propulsion, power, communications, thermal control, and operations. Design decisions in one subsystem directly impacted others, reinforcing the importance of interface definition and early trade studies in large-scale space missions.

<br>

### Lessons Learned

- SAR payloads drive mission architecture more than any other subsystem
- Communications is often the limiting factor in Earth-observation missions
- Early ground segment design is critical for constellation scalability
- Academic mission studies must balance ambition with realism

<br>

<br>

*This project represents an academic mission concept study and does not reflect an operational or deployed system.*
