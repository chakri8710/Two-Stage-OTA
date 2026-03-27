# 2-Stage Operational Transconductance Amplifier (OTA)

## Abstract
This project presents the design and simulation of a two-stage Operational Transconductance Amplifier (OTA) using MOSFET technology. The objective is to achieve high gain, proper biasing, and stable frequency response while understanding the trade-offs involved in analog circuit design. The circuit is implemented and analyzed using LTspice through DC, AC, and transient simulations.

---

## Introduction
Operational Transconductance Amplifiers (OTAs) are fundamental building blocks in analog integrated circuits. Unlike traditional op-amps, an OTA converts a differential input voltage into an output current, making it highly suitable for applications such as filters, oscillators, and data converters.

The performance of an OTA depends on parameters such as gain, bandwidth, slew rate, and stability. Multi-stage amplifiers are often used to achieve higher gain, but they introduce additional poles, making stability a critical design concern.

---

## Theory

### Transconductance Principle
The OTA operates on the principle:

\[
I_{out} = g_m (V^+ - V^-)
\]

where:
- \( g_m \) is the transconductance
- \( V^+ \), \( V^- \) are input voltages

---

### Two-Stage Amplifier Design

#### 1. Differential Amplifier (First Stage)
- Provides initial gain
- Converts input voltage difference into current
- Improves Common Mode Rejection Ratio (CMRR)
- Typically implemented using a current mirror load

#### 2. Common Source Amplifier (Second Stage)
- Converts current into voltage
- Provides additional gain
- Determines output swing and driving capability

---

### Frequency Response and Stability
A two-stage OTA introduces multiple poles:
- Dominant pole (low frequency)
- Non-dominant poles (higher frequency)

This leads to:
- Gain roll-off
- Phase shift
- Potential instability

Phase margin is used to evaluate stability. Compensation techniques (e.g., Miller compensation) are often required.

---

## Circuit Implementation
The OTA is implemented using MOSFETs operating in the saturation region. Proper biasing ensures linear operation and desired gain characteristics.

Key design considerations:
- Transistor sizing (W/L ratio)
- Bias current selection
- Load capacitance

---

## Simulation Results

### DC Analysis
- Verified operating points of all MOSFETs
- Ensured saturation region operation
- Confirmed proper biasing conditions

---

### AC Analysis
- Gain observed approximately 30 dB
- Frequency response analyzed
- Phase shift indicates multi-stage behavior

#### AC Gain and Phase Plot
![AC Response](results/ac_response.png)

---

### Transient Analysis
- Output waveform observed for input excitation
- Slew rate behavior analyzed
- Verified time-domain response

#### Transient Response Plot
![Transient Response](results/transient_response.png)

---

## Results and Discussion
- The amplifier achieves moderate gain (~30 dB)
- Gain is limited by transistor sizing and output resistance
- Phase response shows expected multi-stage characteristics
- Biasing significantly affects overall performance
- Trade-off observed between gain and bandwidth

---

## Challenges Faced
- Low gain due to initial design parameters
- Singular matrix errors in LTspice simulations
- Output offset under common-mode input conditions
- Phase not starting at 0° due to pole effects

---

## Tools Used
- LTspice
- SPICE Netlist Modeling
- MOSFET Level-1 Models

---

## Project Structure
