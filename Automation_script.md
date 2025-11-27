## Automation script and project entry point (runall.ps1).

An automation scripts are used to execute many steps in a secuencial form, their objetive is the reproducibility and execution of projects automaticaly without error by anyone even yourself.

There are the typical structure for a runall.ps1:

- Activation of the environtment (venv o conda)
- Installation of Indepencies
- ETL execution
- models or code executions

Here is an example of a runall.ps1, executable in powershell, executing a project which uses python scripts
<pre>
Write-Output "Empezando"

$Pythonscriptpath = "C:\Users\ypalacios\Desktop\Universidad\Taller4\taller4-GPI\"
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
