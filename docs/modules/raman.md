# Raman Module

A general-purpose Raman spectroscopy viewer for spectra collected during DAC experiments. Supports both wavelength and Raman shift display, spectrum overlays for comparison, and automatic export logging.

---

## Workflow

1. Load a Raman spectrum (`.spe` file).
2. Set the **laser line** wavelength to match the excitation source used during acquisition (default: 532 nm).
3. Choose the display mode — **wavelength** (nm) or **Raman shift** (cm⁻¹).
4. Click on the spectrum to place the crosshair marker lines, or use the arrow keys to fine-tune the position.
5. Add overlays to compare the current spectrum against others.

---

## Display Modes

| Mode | X-axis |
|---|---|
| **Raman shift** *(default)* | cm⁻¹ relative to the laser line |
| **Wavelength** | nm (raw detector wavelength) |

Switching modes recalculates the x-axis on the fly — no reload needed. Set the correct laser line before switching to ensure accurate wavenumber values.

---

## Crosshair Markers

Clicking on the plot places a vertical line (x position) and a horizontal line (y position). These are independent markers for annotating peak positions or intensity levels. The current coordinates are displayed in the status bar.

Use the **arrow keys** for fine adjustment after clicking:

- **◀ ▶** — move the vertical line left or right by 0.05 units
- **▲ ▼** — move the horizontal line up or down by 0.1 units

---

## Overlays

Any currently displayed spectrum can be pinned as an overlay. Overlays remain visible when new files are loaded, allowing direct visual comparison between measurements.

Each overlay can be independently:

- **Scaled** — multiply intensity by a constant factor
- **Offset** — shift intensity up or down
- **Shown or hidden** — toggle visibility without removing
- **Recolored** — assign a custom color

---

## Controls

| Control | Description |
|---|---|
| **Load** | Load a Raman `.spe` file |
| **Laser line** | Excitation wavelength in nm |
| **Wavelength / Raman shift** | Toggle the x-axis display mode |
| **◀ ▶ arrow keys** | Nudge the vertical marker line left or right |
| **▲ ▼ arrow keys** | Nudge the horizontal marker line up or down |
| **◀ / ▶ file buttons** | Step to the previous or next file in the directory |
| **Add overlay** | Pin the current spectrum as a persistent overlay |
| **Remove** | Remove the selected overlay |
| **Clear** | Remove all overlays |

---

## Output Log

A `Raman_export_log.txt` file is automatically created in the same directory as the data and appended each time a file is loaded:

```
# File    Path    Exposure Time [sec]    Central WL    x-units    ROI [x_min, x_max] [y_min, y_max]    Detector
```
