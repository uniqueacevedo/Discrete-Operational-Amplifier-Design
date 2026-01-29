# Discrete Operational Amplifier Design

## Overview
This repository contains discrete analog circuit designs focused on operational amplifier architecture, built and analyzed from the transistor level up. The projects in this repository emphasize how real operational amplifiers are constructed internally, exploring biasing strategies, gain staging, frequency response, and output drive capability using bipolar junction transistors (BJTs).

Rather than treating op-amps as black-box components, this work investigates their internal building blocks through practical circuit implementation, measurement, and integration. The primary case study documented here is a full transistor-level dissection and reconstruction of the LM741 operational amplifier.

---

## Flagship Project: LM741 Operational Amplifier Dissection

The LM741 project reconstructs the internal architecture of a classic operational amplifier by independently building and integrating each of its major functional blocks. The project was completed as a multi-part Electronic Devices Laboratory assignment, with each stage verified experimentally before being combined into a complete operational amplifier.

---

## Project Breakdown

### 1. Push-Pull Power Amplifier & Speaker Drive
The project began with practical signal testing using a speaker load and an examination of bipolar junction transistor operation. A push-pull (class AB) output stage was constructed to provide low output impedance and sufficient current drive for real loads.

Initial testing revealed crossover distortion at the zero-crossing region. This distortion was mitigated through biasing adjustments, demonstrating a common real-world issue in power amplifier design and its standard correction techniques. This block corresponds to the output stage of the LM741.

**Key topics:**
- BJT operation and conduction regions  
- Push-pull (class AB) power amplification  
- Crossover distortion and bias correction  
- Load driving behavior  

---

### 2. Biasing Networks & Constant Current Sources
To ensure stable operating points across the amplifier, biasing circuits were introduced. The stage began with a diode-connected transistor and was extended into constant current sources and sinks using current mirror configurations.

These circuits provided predictable bias currents and improved stability across operating conditions, replicating how internal biasing networks are implemented in integrated operational amplifiers.

**Key topics:**
- Diode-connected BJTs  
- Current mirror circuits  
- Constant current sources and sinks  
- Bias stability and current control  

---

### 3. Voltage Gain Stage & Frequency Response Analysis
A discrete voltage gain stage was implemented to replace the function generator previously used in the signal path. This stage provided the majority of the amplifier’s open-loop voltage gain.

Frequency response was analyzed using a Bode plotter operating through a Windows-based analyzer running on a Linux environment. The effects of Miller capacitance, bandwidth limitations, and dominant pole behavior were examined. Darlington pair operation was also studied as part of the gain-stage analysis.

Once characterized, the gain stage was integrated with the existing biasing networks and push-pull output stage.

**Key topics:**
- Common-emitter voltage amplification  
- Miller effect and bandwidth limitations  
- Darlington pair behavior  
- Frequency response and Bode plot analysis  

---

### 4. Differential Pair Input Stage
The final stage involved constructing the differential input amplifier that forms the front end of the operational amplifier. A tail current source was used to bias the differential pair, enabling differential signal amplification and rejection of common-mode signals.

With this stage integrated, the operational amplifier was complete, closely mirroring the internal architecture of the LM741.

**Key topics:**
- Differential amplifier operation  
- Tail current biasing  
- Input symmetry  
- Common-mode rejection  

---

## Final Integrated System
All four stages were successfully integrated into a single discrete operational amplifier. The completed system demonstrated stable biasing, significant voltage gain, realistic frequency response behavior, and the ability to drive real loads.

This project highlights how classical operational amplifiers are built from fundamental transistor-level building blocks and how design tradeoffs between gain, bandwidth, and stability manifest in real circuits.

---
