# Current Mirror Calculations

## Design Specifications

| Parameter | Value |
|---|---:|
| Supply Voltage (VDD) | 1.8 V |
| Reference Current (IREF) | 100 µA |
| NMOS Length (L) | 0.15 µm |
| NMOS Width (W) | 1 µm |
| W/L | 6.67 |
| Threshold Voltage (VTH) | 0.7V |
| μnCox | 150µA/V^2 |

## 1. Overdrive Voltage

The overdrive voltage is:

VOV = VGS - VTH

For the selected reference current, VOV is calculated from the
long-channel MOSFET equation:

VOV = √(2IREF / (μnCox(W/L)))

Using the given design parameters:

VOV = √[2(100 µA) / (150 µA/V² × 6.67)]

Therefore:

VOV ≈ 0.447 V

## 2. Reference Current

For a long-channel NMOS:

IREF = (1/2) μnCox (W/L) VOV²

Therefore:

VOV = √(2IREF / (μnCox(W/L)))
VOV = 0.447 V

## 3. Gate-Source Voltage

Once VOV is known:

VGS = VTH + VOV

VGS = 0.7 + 0.447

Therefore:

VGS ≈ 1.147 V

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
| VGS | 0.9V | — |
| IREF | 100 µA | — |
| IOUT | 100 µA | — |
| Current Error | 0 | — |

