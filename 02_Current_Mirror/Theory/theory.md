# Current Mirror Theory

## 1. Introduction

A current mirror is an analog circuit used to copy a reference current
from one branch of a circuit to another.

It is widely used as a biasing circuit in analog ICs, including
differential amplifiers, operational amplifiers, and other analog
building blocks.

## 2. Basic MOS Current Mirror

A basic current mirror consists of two matched MOSFETs.

- M1 is diode-connected.
- M2 provides the output current.
- The gates of M1 and M2 are connected together.
- The sources are connected to the same potential.

If M1 and M2 are identical and operate in saturation:

I_OUT ≈ I_REF

## 3. MOSFET Saturation Equation

For a long-channel NMOS operating in saturation:

I_D = (1/2) μ_n C_ox (W/L) (V_GS - V_TH)^2

where:

- μ_n = electron mobility
- C_ox = oxide capacitance per unit area
- W = transistor width
- L = transistor length
- V_GS = gate-source voltage
- V_TH = threshold voltage

## 4. Current Mirroring

Since the gates of M1 and M2 are connected:

V_GS1 = V_GS2

For matched MOSFETs:

(W/L)_1 = (W/L)_2

Therefore:

I_OUT ≈ I_REF

For different transistor dimensions:

I_OUT / I_REF = (W/L)_2 / (W/L)_1

## 5. Channel-Length Modulation

In a practical MOSFET, the drain current also depends on V_DS.

The saturation current can be approximated as:

I_D = (1/2) μ_n C_ox (W/L) V_OV² (1 + λV_DS)

where:

V_OV = V_GS - V_TH

and λ is the channel-length modulation coefficient.

Because V_DS1 and V_DS2 may be different:

I_OUT may not be exactly equal to I_REF.

## 6. Output Resistance

The small-signal output resistance is approximately:

r_o ≈ 1/(λI_D)

A larger output resistance makes the current source more ideal.

## 7. Compliance Voltage

The output voltage must be sufficiently high for M2 to remain
in saturation.

For an NMOS current mirror:

V_OUT ≥ V_OV

If V_OUT becomes too low, M2 enters the triode region and the
output current decreases.

## 8. Advantages

- Simple circuit
- Low transistor count
- Useful for bias generation
- Easy to implement in IC technology

## 9. Limitations

- Output current depends on transistor matching
- Channel-length modulation causes current error
- Requires sufficient output voltage
- Threshold-voltage and process variations affect accuracy
