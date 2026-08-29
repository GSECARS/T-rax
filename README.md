T-Rax
===

A python GUI program for fast visual analysis of spectroscopic data collected mostly during high pressure diamond anvil 
cell experiments.

It includes separate modules for temperature fitting, pressure estimation using ruby peak or the diamond edge and a 
general module for Raman spectroscopy.
 
Currently, the only input files allowed are Princeton Instruments \*.spe file saved either from WinSpec or Lightfield.

Installation
===

First, get the source: either clone with [Git](https://git-scm.com/downloads) or [download the ZIP](https://github.com/GSECARS/T-rax/archive/refs/heads/gsecars.zip) and extract it. Then follow one of the options below.

---

### Option 1 — uv (recommended)

**Requires:** [uv](https://docs.astral.sh/uv/getting-started/installation/)

uv automatically manages the Python version and virtual environment. No separate Python install needed.

**Create the desktop shortcut**
```bash
cd T-rax && uv run trax --make_icon
```

This creates a desktop icon. Double-click it to launch T-Rax from then on.

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

This creates a desktop icon. Double-click it to launch T-Rax from then on.

---

Maintainers
===

Christofanis Skordas (skordasc@uchicago.edu)  
Stella Chariton (stellachariton@uchicago.edu)  
GSECARS, Center for Advanced Radiation Sources, University of Chicago
