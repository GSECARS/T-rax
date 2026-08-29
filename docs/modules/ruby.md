# Ruby Pressure Module

Determines pressure from the shift of the ruby R1 fluorescence line. Pressure updates in real time as the cursor line is moved, and an automatic peak fitter is available for precise positioning.

---

## Workflow

1. Load a ruby fluorescence spectrum (`.spe` file).
2. Confirm or adjust the **reference position** — the R1 wavelength at ambient conditions (default: 694.35 nm).
3. Position the **sample line** on the R1 peak by clicking on the spectrum, using the arrow keys to fine-tune, or clicking **Fit** to locate it automatically.
4. Select the appropriate **pressure scale** for your experimental conditions.
5. Read the calculated pressure.

---

## Pressure Scales

| Scale | Conditions |
|---|---|
| **Dewaele** *(default)* | Recommended for most experiments |
| **Hydrostatic** | Hydrostatic or quasi-hydrostatic pressure media |
| **Non-hydrostatic** | Non-hydrostatic conditions |

All three scales relate pressure to the R1 wavelength shift relative to the ambient reference. The Dewaele scale is selected by default and is appropriate for the majority of DAC experiments.

---

## Temperature Correction

When sample and reference temperatures differ from 298 K, a thermal correction is automatically applied to both the reference wavelength and the scale factor. Enter the known sample temperature in the **Sample temperature** field to enable this correction.

---

## Controls

| Control | Description |
|---|---|
| **Load** | Load a ruby fluorescence `.spe` file |
| **Sample position** | Wavelength of the R1 peak under pressure (nm) |
| **Reference position** | R1 wavelength at ambient — default 694.35 nm |
| **Sample temperature** | Sample temperature for thermal correction (K) |
| **Reference temperature** | Reference temperature — default 298 K |
| **Scale** | Pressure scale selection |
| **Fit** | Fit two pseudo-Voigt peaks (R1 and R2) automatically |
| **Auto fit** | Re-fit automatically each time a new file is loaded |
| **◀ ▶ arrow keys** | Nudge the sample line left or right by 0.02 nm |
| **◀ / ▶ file buttons** | Step to the previous or next file in the directory |
