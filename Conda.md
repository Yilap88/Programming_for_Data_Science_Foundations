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


### Basic Usage  

<pre>Environment Creation:  
conda create -n environment_name  
  
Environment Activation:  
conda activate environment_name  
  
Environment Deactivation:  
conda deactivate</pre>  
