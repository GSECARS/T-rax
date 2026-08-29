# Ruby Module

The Ruby module determines pressure from the shift of the ruby R1 fluorescence line using established pressure scales. It supports real-time pressure reading as the cursor line is moved, automatic peak fitting, and temperature correction.

## Workflow

1. Load a ruby fluorescence spectrum (`.spe` file).
2. Set the **reference position** (R1 wavelength at ambient conditions, typically 694.35 nm).
3. Move the **sample cursor line** to the R1 peak position, or use **Fit** to locate it automatically.
4. Read the pressure.

## Pressure scales

Three scales are available:

| Scale | A (GPa) | B | Notes |
|---|---|---|---|
| Dewaele (default) | 1920 | 9.61 | Recommended for most experiments |
| Hydrostatic | 1904 | 7.665 | For hydrostatic or quasi-hydrostatic media |
| Non-hydrostatic | 1904 | 5 | For non-hydrostatic conditions |

All scales use the Mao et al. form:

$$P = \frac{A}{B} \left[ \left(\frac{\lambda}{\lambda_0}\right)^B - 1 \right]$$

where $\lambda$ is the measured R1 wavelength and $\lambda_0$ is the reference wavelength.

## Temperature correction

When sample temperature is known (e.g., from the Temperature module), a thermal correction is applied to both the reference wavelength and the scale factor $A$.

## Controls

| Control | Description |
|---|---|
| Load | Load a ruby `.spe` file |
| Sample position | Wavelength of the R1 line under pressure |
| Reference position | R1 wavelength at ambient (default 694.35 nm) |
| Sample / Reference temperature | Used for thermal correction |
| Scale | Select the pressure scale |
| Fit | Auto-fit two pseudo-Voigt peaks (R1 and R2) |
| Auto fit | Re-fit automatically each time a new file loads |
| ◀ ▶ arrow keys | Nudge the cursor line left/right by 0.02 nm |
