# Differential Pair Theory

## 1. Introduction

A differential pair is an important analog building block used to
amplify the difference between two input signals.

It is widely used in operational amplifiers, comparators, mixers,
and other analog integrated circuits.

## 2. Basic Structure

A basic MOS differential pair contains:

- Two matched MOSFETs M1 and M2
- A common tail current source
- Two input terminals
- Two output terminals

The sources of M1 and M2 are connected together and biased using
a tail current source.

## 3. Differential Input

The differential input voltage is:

V_ID = V_IN1 - V_IN2

If:

V_IN1 > V_IN2

then M1 conducts more current than M2.

If:

V_IN1 < V_IN2

then M2 conducts more current than M1.

For:

V_IN1 = V_IN2

the tail current is ideally divided equally:

I_D1 = I_D2 = I_T / 2

where I_T is the tail current.

## 4. Common-Mode Input

The common-mode input voltage is approximately:

V_CM = (V_IN1 + V_IN2) / 2

A differential pair ideally responds to the difference between
the inputs while rejecting signals common to both inputs.

## 5. MOSFET Transconductance

For a MOSFET operating in saturation:

g_m = 2I_D / V_OV

where:

V_OV = V_GS - V_TH

is the overdrive voltage.

## 6. Differential Gain

For a simple resistively loaded differential pair, the
single-ended differential gain can be approximated as:

A_V ≈ -g_m R_D / 2

The exact gain depends on the output configuration and load.

For an active-load differential pair, the gain is determined by
the transistor transconductance and effective output resistance.

## 7. Common-Mode Gain

Ideally:

A_CM = 0

In a practical circuit, finite tail-source resistance and transistor
mismatch produce a non-zero common-mode gain.

## 8. CMRR

The Common-Mode Rejection Ratio is:

CMRR = |A_D / A_CM|

In decibels:

CMRR(dB) = 20 log10(|A_D / A_CM|)

A higher CMRR indicates better rejection of common-mode signals.

## 9. Tail Current

For a symmetrical differential pair:

I_D1 + I_D2 = I_T

When both input voltages are equal:

I_D1 = I_D2 = I_T / 2

The tail current determines the bias current of the differential pair
and therefore affects transconductance and gain.

## 10. Advantages

- Rejects common-mode signals
- Provides differential amplification
- Useful as the input stage of an op-amp
- Relatively good noise performance
- Suitable for integrated-circuit implementation

## 11. Limitations

- Requires proper transistor matching
- Limited input common-mode range
- Gain depends on transistor parameters
- Mismatch produces offset voltage
- Finite tail resistance reduces CMRR

## 12. Applications

Differential pairs are used in:

- Operational amplifiers
- Comparators
- Instrumentation amplifiers
- Analog-to-digital converters
- Mixers
- Current-mode circuits
