# Diamond Pressure Module

Determines pressure from the shift of the first-order diamond Raman edge (zone-center phonon at ~1334 cm⁻¹). A smoothed derivative display is provided to help locate the edge position precisely on broad or noisy spectra.

---

## Workflow

1. Load a diamond Raman spectrum (`.spe` file).
2. Confirm or adjust the **reference position** — the diamond edge wavenumber at ambient conditions (default: 1334 cm⁻¹).
3. Position the **sample line** on the diamond edge by clicking on the spectrum or using the arrow keys. Switch to the **derivative view** if the edge is difficult to locate on the raw spectrum.
4. Read the calculated pressure.

---

## Derivative Display

The derivative spectrum shows the smoothed first derivative of intensity with respect to wavenumber. The inflection point of the diamond edge corresponds to a zero-crossing in the derivative, making the edge position easier to identify when the raw spectrum is broad or overlapping with sample peaks.

The **smoothing** slider controls the width of the Gaussian smoothing kernel applied before differentiation. Increase smoothing on noisy spectra; reduce it if fine structure needs to be resolved.

---

## Controls

| Control | Description |
|---|---|
| **Load** | Load a diamond Raman `.spe` file |
| **Sample position** | Wavenumber of the diamond edge under pressure (cm⁻¹) |
| **Reference position** | Edge position at ambient — default 1334 cm⁻¹ |
| **Show derivative** | Toggle the smoothed derivative spectrum overlay |
| **Smoothing** | Gaussian smoothing width for the derivative |
| **◀ ▶ arrow keys** | Nudge the sample line left or right |
| **◀ / ▶ file buttons** | Step to the previous or next file in the directory |
