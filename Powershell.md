## Basic Guide of PowerShell

### What is PowerShell?

PowerShell is an advanced terminal  for Windows, that is more powerful than cmd, it allows you to: 

- Browse files
- Execute programs
- Automate tasks
- Work with objects, not just text

### How to execute PowerShell?

There are three ways:  
- Press Win + X → “Windows PowerShell”.
- Look up PowerShell in the Windows Search Bar.
- In a folder → Shift + rigth click → "Open in a Terminal"

### Rules for basic commands
- In Power Shell, commands are structured as follows: Verb-Noun (e.g. Set-Location).
- Some cmd commands work in PowerShell, because PowerShell uses "aliases"

### Basic Commands in cmd

**1- Browse by Files**

Location:
<pre>
Get-Location

alias:
pwd
</pre>

Look files and folders:
<pre>
Get-ChildItem

aliases:
dir
ls
gci
</pre>

Change Folder:
<pre>
Set-Location My_Folder

alias:
cd My_folder
</pre>

Note: If the directory contain spaces, you must use quotation marks.
<pre>
Set-Location "C:\Users\ypalacios\Desktop\Universidad\Gas Insight Project>"

alias:
cd "C:\Users\ypalacios\Desktop\Universidad\Gas Insight Project>"
</pre>

Move up a folder and set Units alias:
<pre>
cd..
D:
</pre>


**2- Create and erase files**

- Create a folder
<pre>
New-Item -ItemType Directory MyFolder

alias:
mkdir MiCarpeta
</pre>

- Create a file
<pre>
New-Item -ItemType File archivo.txt

or

"" | Out-File archivo.txt
</pre>

- Erase a file or folder
<pre>
File:
Remove-Item archivo.txt

Folder with it content
Remove-Item MyFolder -Recurse -Force

alias:
del archivo.txt
rm archivo.txt
</pre>

**3- View file content.**

<pre>
Get-Content archivo.txt
  
alias:
cat archivo.txt
</pre>

**4- Copy and move files**

Copy:
<pre>
Copy-Item archivo.txt .\backup\
  
alias:
cp archivo.txt .\backup\
</pre>

Move:
<pre>
Move-Item archivo.txt .\Documentos\
  
alias:
mv archivo.txt .\Documentos\
</pre>


### Variables y Objects (Basics)

**1- Create a variable**
<pre>
$nombre = "Yilmer"
</pre>

**2- Print a variable**
<pre>
$nombre
</pre>

**3- PowerShell works with objects, for example:**
<pre>
Get-ChildItem | Select-Object Name, Length
</pre>

### Environment Management

**1- Activate an Conda environment**
<pre>
conda activate mi_env
</pre>

**2- Deactivate an environment**
<pre>
conda deactivate
</pre>

**3- Activate a venv:**
<pre>
.\mi_env\Scripts\Activate.ps1
</pre>

