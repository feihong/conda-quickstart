# Feihong's conda quickstart

I think the best way to install conda is via Mambaforge, which pulls from `conda-forge` channel and includes mamba, a faster, drop-in replacement for the conda CLI tool.

## Installation

    curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-$(uname)-$(uname -m).sh"
    bash Mambaforge-$(uname)-$(uname -m).sh
    
## Commands

Create new environment called py310 that includes Python 3.10

    mamba create -n py310 python=3.10
    
List all environments you currently have installed

    mamba env list

Don't allow base environment to automatically be activated

    conda config --set auto_activate_base false
    
Run something inside virtual environment without activating the environment

    mamba run -n py310 python --version
    
Install packages from requirements.txt file

    mamba install --file requirements.txt
