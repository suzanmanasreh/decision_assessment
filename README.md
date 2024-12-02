Setting Up an environment for this workbook is not easy. It is fairly involved and may vary a bit between OS'es. Colab unfortunately does not work for this due to the specific environment we need to get this to work.

What I suggest is the following set of steps which has successfully worked on Mac OS X (version 16), Ubuntu 22.04 and Windows 11 as of December 2024.

1. Install miniforge3: Go to [miniforge releases](https://github.com/conda-forge/miniforge/releases) and install the latest miniforge3 package (**REMEMBER**: miniforge3 not mambaforge)
2. Create an environment: ```mamba create -n assessment_env python=3.9```. (**NOTE**: You may have path issues, i.e. your terminal may not be able to find mamba - use chatgpt and google to debug this)
3. Activate your environment: ```mamba activate assessment_env```
4. Install packages in order
    - ```mamba install pip```
    - ```pip install numpy pandas matplotlib scikit-learn jupyter scipy```
    - ```mamba install -c conda-forge psychopy wxpython```
5. Install the right version of psychopy.
    - clone the psychopy github [repo](https://github.com/psychopy/psychopy) to a known folder
    - ```cd psychopy``` to get into the right folder.
    - In your _activated_ environment run ```pip install -e .```
6. Your environment should be set up now. Now, in VSCode (or your favorite IDE), open the ```workbook.ipynb``` with the ```assessment_env``` kernel. [Resource](https://code.visualstudio.com/docs/datascience/jupyter-notebooks). Feel free to chatgpt or google for others.
7. You should be good to go!.