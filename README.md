# VSWR to Return Loss Calculator

A free, single-file web tool for RF engineering that converts in any direction between **VSWR**, **return loss (dB)**, **reflection coefficient |Γ|** and **mismatch loss (dB)**. It also computes reflected power percentage from forward/reverse power readings.

## Online use

Open the tool directly in your browser (no install, no dependencies, all math runs client-side):

**https://xiaokeni2.github.io/vswr-return-loss-calculator/**

## What it does

- Enter a value in **any** field — VSWR, return loss, |Γ| or mismatch loss — and the other three update instantly.
- Enter forward and reflected power (any unit, same unit in both fields) to get |Γ| = √(P_ref / P_fwd), reflected power percentage and the full conversion.
- Built-in VSWR conversion table (1.0 / 1.1 / 1.2 / 1.5 / 2.0 / 3.0 / 5.0 / 10.0) and formula reference.
- Input validation, dark engineering UI, mobile friendly.

## Formulas

```
Γ                  = (VSWR − 1) / (VSWR + 1)
Return Loss (dB)   = −20·log₁₀(|Γ|)
Mismatch Loss (dB) = −10·log₁₀(1 − |Γ|²)
VSWR               = (1 + |Γ|) / (1 − |Γ|)
Reflected power %  = |Γ|² × 100
```

## Usage

1. Open the page and type a value into any of the four converter fields (e.g. VSWR = 1.5 → return loss 13.98 dB, |Γ| = 0.2000, mismatch loss 0.177 dB, 4.00% reflected power).
2. Or measure forward/reverse power with a directional coupler and power meter, enter both values, and the converter fills in all four quantities.
3. Valid ranges: VSWR ≥ 1, return loss ≥ 0 dB, 0 ≤ |Γ| ≤ 1, mismatch loss ≥ 0 dB.

## Related

More RF tools: [BRIDZA RF Component Selector](https://rf.bridza.com/) · [OCXO / TCXO Parametric Search](https://xiaokeni2.github.io/rf-component-selector/)
