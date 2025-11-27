## Automation Script and Project Entry Point (runall.ps1).

Automation scripts are used to execute many steps sequentially in Powershell or cmd. Their objective is to enable the reproducible and error-free automation of projects by anyone, including yourself.

The typical structure of a runall.ps1 is as follows:

- Activation of the environment (venv or conda)
- Installation of dependencies
- Execution of ETL
- Execution of models or code

Here is an example of a runAll.ps1 executable in PowerShell that runs a project using Python scripts.

<pre>
# Welcome message
Write-Output "Empezando"

# Read the current directory (where the script is)
$Pythonscriptpath = $PSScriptRoot

# Set the current directory
& set-location $Pythonscriptpath

# environment managemente
& conda env create -f environment.yml
& conda activate myenvironment

# Set "scripts" folder as current directory and execute the python scripts
& cd ./scripts
& python Import_data_Zenodo.py
& python RL_Energia_gas.py
& python RL_Energia_carbon.py
& python RL_Energia_petroleo.py
& python RL_Energia_embalses.py
& cd ../

Write-Output "Listo!"
</pre>
