# Differential Pair

## Objective

To design and analyze a basic MOSFET differential pair and understand
its differential operation, common-mode operation, gain, biasing,
and important design parameters.

## Circuit

The differential pair consists of two matched MOSFETs sharing a common
tail current source.

The input signals are applied to the gates of the two transistors.
The circuit amplifies the difference between the two input voltages.

## Key Concepts

- Differential input voltage
- Common-mode input voltage
- Tail current
- Differential gain
- Common-mode gain
- Common-mode rejection ratio (CMRR)
- Transconductance
- Output resistance
- MOSFET matching

## Contents

- [Theory](Theory/theory.md)
- [Calculations](Calculations/calculations.md)
- [Simulation](Simulation/simulation.md)

## Design Flow

1. Select supply voltage and tail current.
2. Select MOSFET dimensions.
3. Calculate the required bias voltage.
4. Determine the operating point.
5. Calculate differential gain.
6. Simulate the differential pair.
7. Measure differential gain and common-mode gain.
8. Calculate CMRR.
9. Compare theoretical and simulated results.

## Results

Simulation results will be added after completing the design.

## Tools

- Circuit simulator: [Tool name]
- Technology/PDK: [Technology]
- MOSFET model: [Model]
