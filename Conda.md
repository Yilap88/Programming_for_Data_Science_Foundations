## Conda/miniconda/Anaconda - Environment Config for Python Projects for VSCode

This Markdown document outlines the main instructions for installing, using and managing Python project environments in VS Code.

For CMD and Powershell usage, click here...  
[cmd](cmd.md)  
[Powershell](Powershell.md)


## What is conda?

Conda is both an environment and a package manager. It is used to:

- create isolated environments (like venv, but more powerful).
- Install specific versions of Python
- Install libraries (NumPy, Pandas, Scikit-Learn, etc.).
- manage system dependencies (C, Fortran, BLAS, etc.).

It is widely used in data science and machine learning.

## Should I install Anaconda or Miniconda?

- Anaconda comes with hundreds of libraries and is heavy.
- Miniconda only comes with Conda and Python, making it lightweight and recommended.

## Conda Installation

Download conda in the URL: https://www.anaconda.com/download
Once Installed you have to activate it in cmd or powershell, to do this in "Windows Search bar" open the "Anaconda prompt" command window.

### cmd
To activate it:
<pre>
conda init cmd.exe
</pre>
To deactivate it:
<pre>
conda config --set auto_activate_base false
</pre>

### Powershell
To activate it (in Anaconda prompt):
<pre>
conda init powershell
</pre>
To deactivate the automatic opening of conda(in powershell):
<pre>
conda config --set auto_activate_base false
</pre>
To deactivate permanently (in powershell):
<pre>
conda init --reverse powershell
</pre>


## Basic Usage  

To view command list:
<pre>
conda env list
</pre>

### Environment Management
Environment Creation:
<pre>conda create -n mi_env
</pre>

Environment Creation with a specific python version:
<pre>conda create -n mi_env python=3.10
</pre> 
  
Environment Activation:  
<pre>conda activate mi_env
</pre> 

Environment Deactivation:  
<pre>conda deactivate
</pre>

Environment Erasure:  
<pre>conda remove -n mi_env --all
</pre>

### Package Management
Package Installation:
<pre>conda install numpy pandas scikit-learn
</pre>

Package Installation with a specific version:
<pre>conda install numpy=1.26
</pre>

Look for package
<pre>conda search numpy
</pre>

Update package
<pre>conda update numpy
</pre>

### Environment Recreaction (yaml)

Environment export to a yaml file
<pre>conda env export > environment.yml
</pre>

Export the environment to a replicable YAML file (without including the prefix or internal dependencies; just include what you have installed).
<pre>conda env export --from-history > environment.yml
</pre>



Environment creation importing yml file
<pre>conda env create -f environment.yml
</pre>

### Package Installation for conda forge

<pre>conda install -c conda-forge numpy
</pre>

Using conda forge always
<pre>conda config --add channels conda-forge
conda config --set channel_priority strict
</pre>

Mixed with pip
<pre>pip install plotly
</pre>

### Erasure of unnecesary package with conda
<pre>
conda clean --all
</pre>







