# Current Mirror Calculations

## Design Specifications

| Parameter | Value |
|---|---:|
| Supply Voltage (VDD) | 1.8 V |
| Reference Current (IREF) | 100 µA |
| NMOS Length (L) | 1 µm |
| NMOS Width (W) | 10 µm |
| W/L | 10 |
| Threshold Voltage (VTH) | [From model] |
| μnCox | [From model] |
| λ | [From model] |

## 1. Overdrive Voltage

The overdrive voltage is:

VOV = VGS - VTH

The required VOV will be determined using the MOSFET model
parameters.

## 2. Reference Current

For a long-channel NMOS:

IREF = (1/2) μnCox (W/L) VOV²

Therefore:

VOV = √(2IREF / (μnCox(W/L)))

## 3. Gate-Source Voltage

Once VOV is known:

VGS = VTH + VOV

This voltage is established by the diode-connected transistor M1.

## 4. Output Current

For matched transistors:

IOUT ≈ IREF

Therefore:

IOUT ≈ 100 µA

## 5. Current Scaling

If the transistor dimensions are different:

IOUT / IREF = (W/L)2 / (W/L)1

For example, if:

(W/L)1 = 10

(W/L)2 = 20

Then:

IOUT / IREF = 20/10 = 2

Therefore:

IOUT = 2 × IREF

For IREF = 100 µA:

IOUT = 200 µA

## 6. Current-Matching Error

The percentage current error is:

Error (%) = |IOUT - IREF| / IREF × 100

The final value will be calculated from the simulation results.

## 7. Compliance Voltage

For the output transistor to remain in saturation:

VOUT ≥ VOV

Therefore, the minimum output voltage is approximately equal
to the overdrive voltage.

## Final Design Values

These values will be updated after simulation.

| Parameter | Calculated | Simulated |
|---|---:|---:|
| VGS | — | — |
| IREF | 100 µA | — |
| IOUT | 100 µA | — |
| Current Error | — | — |
| Minimum VOUT | — | — |
