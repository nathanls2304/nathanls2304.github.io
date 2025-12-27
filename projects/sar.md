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

## My Role – Communications and Avionics Engineer

I served as the Communications and Avionics Engineer, responsible for:

- S-band TT&C architecture for command and telemetry
- X-band payload downlink strategy for SAR data
- Inter-satellite link (ISL) concept development
- Ground station and data routing architecture
- On-board avionics trade studies and interface definition
- Identification of bandwidth, latency, and data-handling constraints

My work focused on ensuring reliable data flow across the spacecraft, constellation, and ground infrastructure while balancing performance, complexity, and scalability.


<br>

### Ground Segment and Data Flow

The mission architecture separates low-rate command and telemetry from high-rate SAR data downlink:

- S-band used for TT&C to ensure reliability and global availability
- X-band used for high-throughput SAR payload data
- Distributed ground stations selected to minimize data latency
- Data archived and processed using cloud-based storage and analytics

<br>

### Inter-Satellite Links (ISL)

The constellation architecture incorporated inter-satellite links to improve data routing efficiency and reduce reliance on immediate ground contact. ISLs enable satellites with limited ground visibility to relay data through neighboring spacecraft with active downlink opportunities.

Key considerations included:
- Use of high-data-rate SDR-based transceivers for inter-satellite communication
- Reduction of onboard data backlog by distributing payload data across the constellation
- Improved responsiveness for time-sensitive maritime monitoring
- Increased resilience against temporary ground station outages

The ISL concept was evaluated at a system level to assess scalability, cost, and operational complexity.

<br>

### Key Communications Challenges

- High SAR data volumes create onboard storage and downlink bottlenecks
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

- Communications and data handling are often the limiting factors in Earth-observation missions
- Inter-satellite links can significantly improve constellation responsiveness and flexibility
- Early definition of avionics interfaces reduces integration risk across subsystems
- Ground segment design is as critical as space segment design for mission success
- Redundancy and fault tolerance must be considered early in constellation-scale systems


<br>

<br>

*This project represents an academic mission concept study and does not reflect an operational or deployed system.*
