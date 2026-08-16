# Bandgap Voltage Reference

## Overview

This project presents the design and simulation of a **Bandgap Voltage Reference (BGR)** using **Cadence Virtuoso** and **GPDK 180 nm** technology.

The circuit generates a temperature-independent reference voltage by combining **PTAT (Proportional To Absolute Temperature)** and **CTAT (Complementary To Absolute Temperature)** voltage components.

The BGR is designed to provide a stable reference suitable for analog and mixed-signal circuits such as ADCs, LDOs, and operational amplifiers.

## Objectives

* Design a temperature-independent bandgap voltage reference.
* Generate and analyze PTAT and CTAT voltage components.
* Combine PTAT and CTAT components to obtain a stable reference voltage.
* Analyze closed-loop stability using loop-gain analysis.
* Evaluate gain, phase margin, gain margin, and temperature coefficient.
* Study the stability of the reference circuit under operating variations.

## Tools and Technology

| Parameter           | Details                             |
| ------------------- | ----------------------------------- |
| EDA Tool            | Cadence Virtuoso                    |
| Technology          | GPDK 180 nm                         |
| Circuit             | Bandgap Voltage Reference           |
| Reference Principle | PTAT + CTAT                         |
| Analyses            | AC, Stability, Temperature Analysis |

## Circuit Principle

A bandgap reference combines two voltage components with opposite temperature coefficients:

* **CTAT voltage:** decreases with increasing temperature.
* **PTAT voltage:** increases with increasing temperature.

By appropriately scaling and combining these two components, their temperature dependencies can partially cancel, producing a relatively temperature-independent reference voltage.

The designed BGR targets a reference voltage of approximately **1.2 V** under typical operation.

## Schematic

![Bandgap Reference Schematic](schematic.png)

## PTAT and CTAT Analysis

The PTAT and CTAT branches were analyzed to study their temperature dependence.

The PTAT component increases with temperature, while the CTAT component decreases with temperature. Their combination produces the required temperature-compensated reference.

![PTAT and CTAT Analysis](ptat_ctat.png)

## Closed-Loop Stability Analysis

The stability of the BGR was evaluated using **loop-gain analysis**.

An **iProbe** was placed in the feedback path of the operational amplifier to isolate the loop and measure the loop response without disturbing the DC bias conditions.

The loop gain was analyzed to determine the phase margin and gain margin of the BGR feedback system.

![Stability Analysis](stability_analysis.png)

### Stability Results

| Parameter    |   Result |
| ------------ | -------: |
| Loop Gain    | 69.85 dB |
| Phase Margin |   75.55° |
| Gain Margin  | 21.46 dB |

The measured phase margin of **75.55°** indicates a stable feedback loop under the simulated conditions.

## AC Analysis

AC analysis was performed to evaluate the frequency response and stability characteristics of the BGR.

![AC Analysis](ac_analysis.png)

## Temperature Performance

The temperature coefficient of the reference voltage was evaluated to determine how effectively the PTAT and CTAT components compensate for temperature dependence.

### Temperature Coefficient

**23.1 ppm/°C**

A lower temperature coefficient indicates better temperature stability of the generated reference voltage.

![Temperature Sweep](temperature_sweep.png)

> If a temperature-sweep image is not available in the repository, remove this image section.

## Performance Summary

| Parameter               |         Result |
| ----------------------- | -------------: |
| Reference Voltage       | ~1.2 V typical |
| Gain                    |       69.85 dB |
| Phase Margin            |         75.55° |
| Gain Margin             |       21.46 dB |
| Temperature Coefficient |    23.1 ppm/°C |

## Key Design Concepts

This project provided practical experience with:

* Bandgap voltage reference design
* PTAT voltage generation
* CTAT voltage generation
* Temperature compensation
* Reference voltage generation
* Operational amplifier based feedback
* Loop-gain analysis
* Phase-margin analysis
* Gain-margin analysis
* Temperature coefficient evaluation
* Analog biasing
* PVT stability considerations

## Applications

Bandgap voltage references are commonly used as stable voltage references in analog and mixed-signal systems.

Potential applications include:

* ADCs
* DACs
* LDOs
* Operational amplifiers
* Power-management circuits
* Mixed-signal ICs

## Conclusion

A **Bandgap Voltage Reference** was designed and simulated using **Cadence Virtuoso with GPDK 180 nm technology**.

The design combines PTAT and CTAT voltage components to generate a temperature-compensated reference voltage. Closed-loop stability analysis achieved a **75.55° phase margin** and **21.46 dB gain margin**, while the simulated temperature coefficient was **23.1 ppm/°C**.

The project provided practical experience in **bandgap reference design, temperature compensation, analog feedback, loop stability, and mixed-signal reference generation**.
