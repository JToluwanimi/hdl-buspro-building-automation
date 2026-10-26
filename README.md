# HDL Buspro Building Automation System Analysis

## 1. What is this?
A comprehensive technical analysis of the HDL Buspro system, a modular building automation solution. This repository documents the system architecture, communication protocols (RS485, UDP/IP), component integration, and wiring topologies required for smart home and commercial building management.

## 2. Why was it built?
During my SIWES at H & O Automation Systems Ltd, I conducted a deep-dive study into the HDL Buspro system. To synthesize this knowledge and demonstrate my understanding of industrial automation protocols, I developed and delivered a technical presentation to peers and supervisors. This repository serves as the permanent technical documentation of that study.

## 3. System Architecture
The HDL Buspro system operates on a decentralized bus network.
- **Backbone:** UDP/IP network for device identification and gateway communication.
- **Fieldbus:** Industry-standard RS485 twisted-pair cabling for bidirectional data transmission between controllers, actuators, and sensors.
- **Topology:** Supports Single Subnet (up to 63 devices) and Multi-Subnet configurations (up to 254 subnets, identified by IDs like "1/2").

## 4. Key Components Analyzed
- **Power Supply Modules:** (e.g., MSP750.431) – Calculated load distribution to ensure total device current stays under 70% of module rating.
- **Buspro Gateway:** Bridges the RS485 bus to the UDP/IP network.
- **Actuators/Controllers:** Relay Modules (4/8/12 channel), LED Dimmers, Curtain Controllers (DC15-30V), and AC Control Modules (0-10V fan control).
- **Sensors:** Multifunctional sensors (PIR, LUX, Temperature) for logic-based automation.
- **User Interfaces:** Granite Display Control Panel, HDL ON Mobile App.
- **Specialty Controllers:** 512CH DMX Scene Controller for advanced RGB lighting management.

## 5. Communication Protocols & Wiring
- **RS485:** Utilizes twisted-pair cables (e.g., HDL-MCL04P.40) with 120 Ohm impedance for reliable data transfer over 1,200m.
- **Wiring Best Practices:** Documented the "Hand-in-Hand" (daisy-chain) connection method vs. Star Topology. Proved that Star Topology is not recommended for networks exceeding 1000m due to low signal-to-noise ratio.

## 6. Software Configuration
- **HDL Buspro Setup Tool (HBST):** Windows-based software used for configuring IP addresses, parameters, and logic conditions.
- **HDL ON:** iOS/Android app for remote control and programming.

## 7. Presentation & Technical Communication
This repository includes the presentation slides and photographic evidence of the technical delivery. 
*(Insert the presentation photos here)*

## 8. Limitations & Future Development
- This repository documents the *analysis and presentation* of the HDL Buspro system. It does not contain custom firmware or original hardware designs for the HDL Buspro modules.
- **Future Work:** Investigate the integration of HDL Buspro with third-party IoT platforms (e.g., Home Assistant) via the RS232/RS485 converter.

## 9. Lessons Learned
- **System Integration:** Building automation requires seamless interoperability between hardware from different manufacturers.
- **Protocol Hierarchy:** Understanding the difference between the physical layer (RS485) and the network layer (UDP/IP) is critical for troubleshooting.
- **Technical Communication:** Explaining complex bus topologies to a non-technical audience requires clear diagrams and structured analogies.
