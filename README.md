# T<sub>c</sub>plotter code description and instructions for use

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/HUGG/tcplotter/HEAD?urlpath=lab/tree/tcplotter.ipynb)
[![Documentation Status](https://readthedocs.org/projects/tcplotter/badge/?version=latest)](https://tcplotter.readthedocs.io/en/latest/?badge=latest) 

The instructions below are actively being written. If you would like to test out plotting using this code you can do so using the Binder button above.

## Installation

The easiest option for installing the tcplotter package is to install it using conda.

```bash
conda install -c conda-forge tcplotter
```

This will install tcplotter and all required Python dependencies (see list below).

### Optional graphical progress bar

It is possible to enable a graphical progress bar with tcplotter when using it in a Jupyter notebook. This requires the [ipywidgets library](https://ipywidgets.readthedocs.io/). ipywidgets can also be installed using conda.

```bash
conda install -c conda-forge ipywidgets
```

### Installing the latest version from GitHub

If you prefer to install the latest version of the T<sub>c</sub>plotter package from GitHub or to manually install without conda, the process is slightly more involved.

First, you will need the several items in order to compile the software used for thermochronometer age and closure temperature calculations.

- [cmake](https://cmake.org/)
- a compatible C compiler
- a compatible C++ compiler

You can find more information about which compilers are able to be used with cmake from the [cmake documentation page](https://cmake.org/documentation/).

In addition, tcplotter requires on the following Python libraries.

- numpy
- matplotlib-base
- scipy

Once the required ...

First, you can download the software from the [tcplotter GitHub page](https://github.com/HUGG/tcplotter) by clicking on the **Code** button and then selecting **Download ZIP**. Unzip the 

Installati

## Usage

## Attribution

## License

*Ignore everything below here...*

The programs provided for use with this manuscript will allow you to reproduce and customize the plots for your use.
This document provides some basic instructions for using the plotting programs, assuming you have some basic familiarity with using programming languages such as Python.

## Dependencies

### Age prediction algorithms

- Apatite and Zircon RDAAM algorithm requires a C++ compiler.
- AFT age and track length distribution algorithm requires a C compiler.

### Plotting software

The plotting software is available in the form of Python scripts. The following
libraries are needed for their use:

- NumPy
- Matplotlib
- SciPy

## Creating plots using the programs

### Preparations

#### All figures

All figures rely on having Python 3 installed with the libraries listed above.
If you do not have Python installed, you can install [Anaconda](https://www.anaconda.com/products/individual#Downloads), for example.

#### Figures 2 and 3

In order to reproduce Figures 2 and 3 you will first need to compile the `RDAAM_He` program.
For Linux or macOS, you can do the following (assuming you have a C++ compiler installed):

```bash
cd cpp
make
make install
cd ..
```

This will compile the program and copy it to the `bin` subdirectory.

Windows users should compile things using the equivalent commands in a Windows shell.

#### Figure 4

In addition to the step needed for Figures 2 and 3 you should compile the `ketch_aft` program.
For Linux or macOS, you can do the following (assuming you have a C compiler installed):

```bash
cd c
make
make install
cd ..
```

This will compile the program and copy it to the `bin` subdirectory.

Windows users should compile things using the equivalent commands in a Windows shell.

## Making the plots

Once you have done the necessary preparations, you can create the plots by simply running the Python programs in the `py` subdirectory.
For example, you can create Figure 2 by running:

```bash
python plot_age_tc_contours_figure2.py
```

## Modifying the plots

If you would like to customize the plots, simply edit the corresponding Python script for the plot of interest, save your changes, and run the script as shown above.
