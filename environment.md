### Environment Config for Python Projects for VSCode

This markdown is for document the main instructions for installation, usage and manage of the enviroments for python projects in VS Code. There are the main points of this md:

1- cmd usage
2 - Conda manager
3 - venv manager

### 1- CMD and Powershell usage
for more info, click here...  
[cmd](cmd.md)  
[Powershell](Powershell.md)


### 2- Conda Manager

#### Instalation

You have to install Conda or minicoda in [Anaconda](https://anaconda.org/anaconda/conda)

Conda is a package manager and open code environments, used mainly in data science for version and library managing. It allows to install, execute and update packages, and to create separated virtual environments for different projects, that allows to avoid conflicts betwen dependecies. It is compatible with R and Python.

Main functions:
- Package managing
- Environment managing
- Multiplatforms: Win, MacOS y Linux

#### Basic Usage  

<pre>Environment Creation:  
conda create -n environment_name  
  
Environment Activation:  
conda activate environment_name  
  
Environment Deactivation:  
conda deactivate</pre>  

### 3- venv Manager
venv is a Python tool that enables you to create virtual environments: isolated spaces in which you can install libraries without affecting the rest of the system.

With venv you can:
- Having projects with different versions of libraries
- Avoid conflicts between dependencies.
- Keep each project clean and organized

To use venv you need python 3 installed, you can check the version as follows in PowerShell:

<pre> ´´´powershell py´´´
</pre>


