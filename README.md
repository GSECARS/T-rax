T-Rax
===

A python GUI program for fast visual analysis of spectroscopic data collected mostly during high pressure diamond anvil 
cell experiments.

I includes separate modules for temperature fitting, pressure estimation using ruby peak or the diamond edge and a 
general module for Raman spectroscopy.
 
Currently, the only input files allowed are Princeton Instruments \*.spe file saved either from WinSpec (File Version 2) 
or Lightfield (File Version 3).

Maintainer
===

Clemens Prescher (clemens.prescher@gmail.com)  
Center for Advanced Radiation Sources, University of Chicago


Requirements
===

- Python 3.13
- qtpy
- pyqt5
- numpy
- scipy
- pyqtgraph
- pyshortcuts
- pillow
- pyepics
- python-dateutil
- lmfit
- h5py
    
Installation
===

Updated information for creating a new conda environment and installing all required packages for GSECARS.

```bash
conda create -n traxENV python=3.13
conda activate traxENV
pip install qtpy pyqt5 pyqtgraph lmfit h5py scipy pyshortcuts pyepics numpy scipy python-dateutil pillow

```
    
The program itself can then be run by going into the "t-rax" directory and type:
    
    python run_t_rax.py
