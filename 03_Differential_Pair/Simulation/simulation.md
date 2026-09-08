# Differential Pair Simulation

## Simulation Objective

The differential pair will be simulated to determine:

- DC operating point
- Drain currents
- Differential gain
- Common-mode gain
- CMRR
- Input common-mode range
- Output behavior

## 1. DC Operating Point

Set:

VIN1 = VIN2

This corresponds to:

VID = 0

The expected result is:

ID1 ≈ ID2 ≈ IT/2

For a 200 µA tail current:

ID1 ≈ ID2 ≈ 100 µA

## 2. Differential Input Sweep

Apply complementary input signals:

VIN1 = VCM + VID/2

VIN2 = VCM - VID/2

Sweep VID over a suitable range.

Measure:

- ID1
- ID2
- VOUT1
- VOUT2

The difference between the output voltages demonstrates
differential amplification.

## 3. Differential Gain

Apply a small differential input and measure the output response.

The differential gain is:

AD = ΔVOUT / ΔVID

The measured gain will be compared with the theoretical value.

## 4. Common-Mode Gain

Apply the same signal to both inputs:

VIN1 = VIN2 = VCM

The common-mode gain is:

ACM = ΔVOUT / ΔVCM

Ideally, ACM should be very small.

## 5. CMRR

Calculate:

CMRR = |AD / ACM|

and:

CMRR(dB) = 20 log10(|AD / ACM|)

## 6. Input Common-Mode Range

The common-mode input voltage will be swept while monitoring
the transistor operating regions and output voltage.

The valid input range is the region where both input MOSFETs
remain properly biased and the required output swing is maintained.

## 7. Simulation Results

| Parameter | Theoretical | Simulated |
|---|---:|---:|
| Tail Current | 200 µA | — |
| ID1 | 100 µA | — |
| ID2 | 100 µA | — |
| Differential Gain | — | — |
| Common-Mode Gain | — | — |
| CMRR | — | — |

## 8. Plots

### Differential Input vs Output

Add plot here.

### Drain Current vs Differential Input

Add plot here.

### Common-Mode Input vs Output

Add plot here.

### CMRR

Add calculated result here.

## Observation

When the two input voltages are equal, the tail current is
approximately divided equally between the two MOSFETs.

When a differential input is applied, the current is steered
between the two branches.

The circuit therefore converts a differential voltage into a
differential current/output voltage.

## Conclusion

The MOS differential pair demonstrates differential amplification
and rejection of common-mode signals. The simulation results will
be compared with theoretical calculations to evaluate the effects
of practical MOSFET parameters and non-idealities.
