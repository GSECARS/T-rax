# Diamond Module

The Diamond module determines pressure from the shift of the first-order diamond Raman edge (zone-center phonon). It uses the second-order Birch–Murnaghan equation of state parameterised for diamond.

## Workflow

1. Load a diamond Raman spectrum (`.spe` file).
2. Set the **reference position** (diamond edge wavenumber at ambient, default 1334 cm⁻¹).
3. Move the **sample cursor line** to the diamond edge, using the derivative display to locate the peak precisely.
4. Read the pressure.

## Pressure equation

$$P = K \frac{\Delta\nu}{\nu_0} \left[ 1 + \frac{K' - 1}{2} \frac{\Delta\nu}{\nu_0} \right]$$

where:

- $\nu_0 = 1334\ \text{cm}^{-1}$ — reference edge position  
- $\Delta\nu = \nu - \nu_0$ — shift under pressure  
- $K = 547\ \text{GPa}$  
- $K' = 3.75$

## Derivative display

The module can display the **derivative spectrum** (smoothed first derivative of intensity with respect to wavenumber). This is useful for locating the inflection point of the diamond edge when the raw spectrum is broad or noisy. Smoothing is adjustable.

## Controls

| Control | Description |
|---|---|
| Load | Load a diamond Raman `.spe` file |
| Sample position | Wavenumber of the diamond edge under pressure |
| Reference position | Edge position at ambient (default 1334 cm⁻¹) |
| Show derivative | Toggle the smoothed derivative spectrum |
| Smoothing | Gaussian smoothing width for the derivative |
| ◀ ▶ arrow keys | Nudge the cursor line left/right |
