# Temperature Module

The Temperature module fits thermal emission spectra to the Planck radiation function to determine sample temperature during laser-heated DAC experiments. Both the downstream (DS) and upstream (US) sides of the sample are measured independently.

## Workflow

1. Load a data image (`.spe` file containing the thermal emission spectrum).
2. Load DS and US calibration images (lamp or blackbody reference spectra).
3. Set the ROI for each side to isolate the emission signal.
4. Read the fitted temperatures for DS and US.

## Key concepts

**Two-color pyrometry** — The sample temperature is extracted by fitting the measured spectral radiance to the Planck function:

$$B(\lambda, T) = \frac{C_1}{\lambda^5 \left(e^{C_2 / \lambda T} - 1\right)}$$

where $C_1$ and $C_2$ are the first and second radiation constants.

**Calibration** — A reference spectrum (tungsten lamp or blackbody) is used to correct for the wavelength-dependent efficiency of the spectrometer and detector.

**DS / US** — Downstream and upstream refer to the two optical paths through the DAC. Each side has its own ROI and calibration, and temperatures are fitted and displayed separately.

## Controls

| Control | Description |
|---|---|
| Load Data | Load the thermal emission `.spe` file |
| Load DS Calibration | Load the downstream calibration image |
| Load US Calibration | Load the upstream calibration image |
| ROI | Adjust the region of interest on the 2D detector image for each side |
| ◀ / ▶ | Step to the previous/next file in the same directory |
| Frame | Navigate frames within a multi-frame `.spe` file |

## Output log

A `T_log.txt` file is automatically created in the same directory as the data file and appended with each measurement:

```
# File    Path    T_DS    T_US    Detector    Exposure Time [sec]
```
