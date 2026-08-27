T-Rax
===

A python GUI program for fast visual analysis of spectroscopic data collected mostly during high pressure diamond anvil 
cell experiments.

I includes separate modules for temperature fitting, pressure estimation using ruby peak or the diamond edge and a 
general module for Raman spectroscopy.
 
Currently, the only input files allowed are Princeton Instruments \*.spe file saved either from WinSpec (File Version 2) 
or Lightfield (File Version 3).

Installation
===

### Using uv (recommended)

[uv](https://docs.astral.sh/uv/) automatically manages the Python version and virtual environment from `pyproject.toml`.

```bash
git clone https://github.com/gsecars/T-rax.git
cd T-rax
uv sync
```

Run the program:

```bash
uv run trax
```

### Using conda

```bash
git clone https://github.com/gsecars/T-rax.git
cd T-rax
conda create -n traxENV python=3.14
conda activate traxENV
pip install -e .
```

Run the program:

```bash
trax
```

Maintainers
===

Christofanis Skordas (skordasc@uchicago.edu)  
Stella Chariton (stellachariton@uchicago.edu)  
GSECARS, Center for Advanced Radiation Sources, University of Chicago
