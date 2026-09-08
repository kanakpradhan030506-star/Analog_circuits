# Current Mirror Simulation

## Simulation Objective

To verify the operation of the MOS current mirror and determine:
- Reference current
- Output current
- Current matching
- Output resistance
- Compliance voltage
- Effect of output voltage

## Schematic
The basic current mirror consists of:

- M1: diode-connected NMOS
- M2: output NMOS
- VDD: supply voltage
- IREF: reference current
- VOUT: output node

## Simulation Type

### DC Operating Point
The operating point simulation is used to determine:

- VGS
- VDS1
- VDS2
- IREF
- IOUT

### DC Sweep
VOUT is swept over a suitable voltage range while measuring
the output current.

This allows the output characteristic of the current mirror
to be observed.

## Measurements

### Reference Current

IREF = ______ µA

### Output Current

IOUT = ______ µA

### Current Error

Error (%) = |IOUT - IREF| / IREF × 100

Error =  0 %

### Minimum Compliance Voltage

VOUT(min) = ______ V

### Output Resistance

rout ≈ ΔVOUT / ΔIOUT

rout = ______ Ω

## Results

| Parameter | Expected | Simulated |
|---|---:|---:|
| VGS | — | — |
| IREF | 100 µA | — |
| IOUT | ≈100 µA | — |
| Current Error | Low | — |
| VOUT(min) | ≈VOV | — |
| Output Resistance | High | — |

## Waveforms / Plots

### Output Current vs Output Voltage

Add simulation plot here.

### DC Operating Point

Add operating-point results here.

## Observation

The output current remains approximately constant over the
saturation region of the output transistor.

When VOUT falls below the required compliance voltage, the
output transistor leaves saturation and the output current
deviates from the reference current.

## Conclusion

The basic MOS current mirror successfully mirrors the reference
current. Practical current mismatch occurs because of channel-length
modulation and transistor non-idealities.
