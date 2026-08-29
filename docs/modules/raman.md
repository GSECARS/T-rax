# Raman Module

The Raman module is a general-purpose spectroscopy viewer for Raman spectra collected during DAC experiments. It supports wavelength and wavenumber display, overlay comparison, and automatic export logging.

## Workflow

1. Load a Raman spectrum (`.spe` file).
2. Set the **laser line** wavelength (default 532 nm).
3. Choose the display mode: wavelength (nm) or Raman shift (cm⁻¹).
4. Use the crosshair lines to mark peak positions.
5. Add overlays to compare multiple spectra.

## Display modes

| Mode | X-axis units |
|---|---|
| Wavelength | nm |
| Raman shift | cm⁻¹ (reverse centimetres relative to laser line) |

The conversion is:

$$\tilde{\nu} = \left(\frac{1}{\lambda_\text{laser}} - \frac{1}{\lambda}\right) \times 10^7$$

## Overlays

Any currently loaded spectrum can be saved as an overlay for side-by-side comparison. Overlays can be independently scaled and offset, shown or hidden, and assigned custom colors.

## Controls

| Control | Description |
|---|---|
| Load | Load a Raman `.spe` file |
| Laser line | Excitation wavelength in nm (used for wavenumber conversion) |
| Wavelength / Raman shift | Toggle display mode |
| Crosshair | Click to place the vertical and horizontal marker lines |
| ◀ ▶ arrow keys | Nudge the vertical line left/right by 0.05 units |
| ▲ ▼ arrow keys | Nudge the horizontal line up/down by 0.1 units |
| ◀ / ▶ file buttons | Step to the previous/next file in the same directory |
| Add overlay | Snapshot the current spectrum as an overlay |
| Remove / Clear | Remove selected or all overlays |

## Output log

A `Raman_export_log.txt` file is automatically created in the same directory as the data and appended each time a file is loaded:

```
# File    Path    Exposure Time [sec]    Central WL    x-units    ROI [x_min, x_max] [y_min, y_max]    Detector
```
