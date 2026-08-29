# Temperature Module

Determines sample temperature from thermal emission spectra using two-color pyrometry. The downstream (DS) and upstream (US) sides of the sample are fitted independently, each with its own region of interest and calibration spectrum.

---

## Workflow

1. Load a **data image** — a `.spe` file containing the thermal emission spectrum of the heated sample.
2. Load a **DS calibration** and a **US calibration** — reference spectra from a known source (tungsten lamp or blackbody) used to correct for the detector and spectrometer response.
3. Set the **ROI** for each side to isolate the emission signal from the sample and exclude contributions from the diamond anvils or gasket.
4. Read the fitted DS and US temperatures.

---

## Calibration

The raw emission spectrum is divided by the calibration spectrum to produce a corrected spectral radiance. This corrected spectrum is then fitted to the Planck function to extract temperature. Accurate calibration is essential — a mismatch between the calibration and data (e.g., different grating position or ROI) will produce incorrect temperatures.

---

## DS and US Sides

In a laser-heated DAC experiment, the sample is illuminated from both sides. T-Rax fits each side independently:

- **DS (downstream)** — the side facing the downstream beam direction
- **US (upstream)** — the side facing the upstream beam direction

Both temperatures are displayed simultaneously. A significant DS/US difference may indicate a temperature gradient across the sample or a misaligned ROI.

---

## Controls

| Control | Description |
|---|---|
| **Load Data** | Load the thermal emission `.spe` file |
| **Load DS Calibration** | Load the downstream calibration image |
| **Load US Calibration** | Load the upstream calibration image |
| **ROI** | Adjust the detector region of interest for each side |
| **◀ / ▶ file buttons** | Step to the previous or next file in the directory |
| **Frame** | Navigate frames within a multi-frame `.spe` file |

---

## Output Log

A `T_log.txt` file is automatically created in the same directory as the data file and appended with each measurement:

```
# File    Path    T_DS    T_US    Detector    Exposure Time [sec]
```
