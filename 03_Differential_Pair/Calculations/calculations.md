# Differential Pair Calculations

## Design Specifications

| Parameter | Value |
|---|---:|
| Supply Voltage (VDD) | 1.8 V |
| Tail Current (IT) | 200 µA |
| M1 Drain Current | 100 µA |
| M2 Drain Current | 100 µA |
| NMOS Length (L) | 1 µm |
| NMOS Width (W) | 10 µm |
| Threshold Voltage (VTH) | [From model] |
| μnCox | [From model] |

## 1. Zero Differential Input

For:

VIN1 = VIN2

the differential input is:

VID = VIN1 - VIN2 = 0

Because M1 and M2 are matched:

ID1 = ID2 = IT / 2

For:

IT = 200 µA

we get:

ID1 = ID2 = 100 µA

## 2. Overdrive Voltage

The overdrive voltage is:

VOV = VGS - VTH

For a long-channel MOSFET:

ID = (1/2) μnCox (W/L) VOV²

Therefore:

VOV = √(2ID / (μnCox(W/L)))

The actual μnCox value should be taken from the selected
technology/model.

## 3. Transconductance

The MOSFET transconductance is:

gm = 2ID / VOV

Therefore:

gm = 2(100 µA) / VOV

The numerical value will be calculated after selecting the
actual device model.

## 4. Differential Gain

For a resistively loaded differential pair:

AV ≈ -gm RD / 2

where:

RD = drain load resistance

The final theoretical gain depends on the selected load.

## 5. Common-Mode Gain

The ideal common-mode gain is:

ACM = 0

For a practical circuit:

ACM ≠ 0

because of finite tail resistance and transistor mismatch.

## 6. CMRR

The common-mode rejection ratio is:

CMRR = |AD / ACM|

In decibels:

CMRR(dB) = 20 log10(|AD / ACM|)

The final CMRR will be calculated using simulation results.

## 7. Current Relationship

At all times:

ID1 + ID2 = IT

At zero differential input:

ID1 = ID2 = IT/2

Therefore:

ID1 = ID2 = 100 µA

for IT = 200 µA.

## Final Results

| Parameter | Calculated | Simulated |
|---|---:|---:|
| Tail Current | 200 µA | — |
| ID1 | 100 µA | — |
| ID2 | 100 µA | — |
| VOV | — | — |
| gm | — | — |
| Differential Gain | — | — |
| Common-Mode Gain | — | — |
| CMRR | — | — |
