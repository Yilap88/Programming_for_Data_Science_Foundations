## Automation script and project entry point (runall.ps1).

Automation scripts are used to execute many steps sequentially in Powershell or cmd. Their objective is to enable the reproducible and error-free automation of projects by anyone, including yourself.

The typical structure of a runall.ps1 is as follows:

- Activation of the environment (venv or conda)
- Installation of dependencies
- Execution of ETL
- Execution of models or code

Here is an example of a runAll.ps1 executable in PowerShell that runs a project using Python scripts.

<pre>
Write-Output "Empezando"

$Pythonscriptpath = "C:\Users\ypalacios\Desktop\energy\"
& set-location $Pythonscriptpath

& conda env create -f environment.yml
& conda activate myenvironment
& cd ./scripts
& python Import_data_Zenodo.py
& python RL_Energia_gas.py
& python RL_Energia_carbon.py
& python RL_Energia_petroleo.py
& python RL_Energia_embalses.py
& cd ../

Write-Output "Listo!"
</pre>
