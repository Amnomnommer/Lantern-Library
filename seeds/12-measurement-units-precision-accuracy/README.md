# Seed Package 12 — Measurement, Units, Precision and Accuracy

**Package ID:** `foundation.measurement_units_precision_accuracy`  
**Inheritance:** `CONCEPTUAL_CORE` / `CORE`  
**Version:** 0.1.0 candidate

## Purpose

Teach Lantern that a measurement is not merely a number.

A useful measurement representation carries, where applicable:

```
target quantity
value
unit
uncertainty
instrument/method
time/place/scope
calibration/traceability
```

## Accuracy vs precision

**Precision** concerns repeatability/fineness.

**Accuracy** concerns closeness to the relevant reference/true value.

A broken scale can report 70.000 kg every time and be highly precise while systematically wrong.

## False precision

Calculation cannot manufacture information absent from the measurements that entered it.

Lantern should not turn a rough input into an output with many apparently meaningful decimal places simply because a calculator can produce them.

Exact significant-figure/uncertainty propagation is delegated to deterministic quantitative code; this package supplies the epistemic constraint.

## Units and dimensions

Unit conversion is valid only between compatible quantity dimensions.

`5 meters` and `5 seconds` share a numeral but are not measurements of the same kind.

Conversion changes representation—not accuracy, precision or evidence quality.

## Calibration

Calibration compares an instrument/procedure with an appropriate reference and creates evidence about its behavior. It does not make the instrument error-free forever.

## Random vs systematic error

Repeated measurements can help characterize/reduce random uncertainty.

Repeating a systematically biased measurement many times can produce a very precise estimate of the wrong value.

## Construct validity

An instrument output does not automatically establish that the intended property was measured. This becomes particularly important in psychology, medicine and social science, where operational definitions and latent constructs require methodological justification.

## Computational boundary

Schema/Methodology decides what quantities and conversions mean. Deterministic numerical code performs unit conversion and uncertainty/error propagation. Lantern interprets the result.

## Review checklist

- [ ] Measurement records retain unit/type and available uncertainty.
- [ ] Accuracy and precision remain distinct.
- [ ] Resolution is not total uncertainty.
- [ ] Dimension mismatches are rejected.
- [ ] Conversion cannot increase evidence quality.
- [ ] False numerical precision is prevented.
- [ ] Repetition cannot erase systematic bias automatically.
- [ ] Calibration is evidence, not infallibility.
- [ ] Instrument output requires measurement/construct validity.
