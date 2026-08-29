# T-Rax

A Python GUI program for fast visual analysis of spectroscopic data collected during high-pressure diamond anvil cell (DAC) experiments.

T-Rax provides four independent modules:

| Module | Purpose |
|---|---|
| [Temperature](modules/temperature.md) | Two-color pyrometry from thermal emission spectra |
| [Ruby](modules/ruby.md) | Pressure from the ruby R1 fluorescence line |
| [Diamond](modules/diamond.md) | Pressure from the diamond Raman edge |
| [Raman](modules/raman.md) | General Raman spectroscopy with overlay support |

**Supported input format:** Princeton Instruments `.spe` files (WinSpec v2 and LightField v3).

---

## Installation

First, get the source: either clone with [Git](https://git-scm.com/downloads) or [download the ZIP](https://github.com/GSECARS/T-rax/archive/refs/heads/gsecars.zip) and extract it. Then follow one of the options below.

---

### Option 1 — uv (recommended)

**Requires:** [uv](https://docs.astral.sh/uv/getting-started/installation/)

uv automatically manages the Python version and virtual environment. No separate Python install needed.

**Run the program**
```bash
cd T-rax && uv run trax --make_icon
```

---

### Option 2 — conda

**Requires:** [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/download)

All commands below must be run in a **conda-enabled terminal**: on Windows use the *Anaconda Prompt* (found in the Start menu); on macOS/Linux use your regular terminal after conda has been initialized.

**1. Enter the directory**
```bash
cd T-rax
```

**2. Create the environment**
```bash
conda create -n traxENV python=3.14
```

**3. Activate the environment**
```bash
conda activate traxENV
```

**4. Install the package**
```bash
pip install -e .
```

**5. Create the desktop shortcut**
```bash
trax --make_icon
```

---

After running `--make_icon`, a **T-Rax** desktop icon is created. Double-click it to launch from then on — no terminal needed.

---

## Maintainers

Christofanis Skordas (skordasc@uchicago.edu)  
Stella Chariton (stellachariton@uchicago.edu)  
GSECARS, Center for Advanced Radiation Sources, University of Chicago
