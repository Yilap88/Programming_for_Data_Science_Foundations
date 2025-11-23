### Basic Guide of PowerShell

#### What is PowerShell?

PowerShell is an advanced terminal  for windows, this is more potent than cmd and it allows: 

- Browse Files
- Exexute Programs
- Automate Tasks
- Work with objects, not only text

#### How to execute cmd?

There are three ways:  
- Press Win + X → “Windows PowerShell”.
- Look up PowerShell in the Windows Search Bar.
- In a folder → Shift + rigth clic → "Open in a Terminal"

#### Rules for basic commands
- In Power Shell, the commands are structured by: Verb-Noun (ex: Set-Location)
- Some commands of cmd works in PS, because PS uses "alias"

#### Basic Commands in cmd

1- Browse by Files

Location:
<pre>
Get-Location

alias:
pwd
</pre>

Look files and folders:
<pre>
Get-ChildItem

alias:
dir
ls
gci
</pre>

Cambiar de carpeta:
<pre>
Set-Location My_Folder

alias:
cd My_folder
</pre>

Move up a Folder and Set Units alias:
<pre>
cd..
D:
</pre>


2- Create and Erase files

- Create a Folder
<pre>
New-Item -ItemType Directory MyFolder

alias:
mkdir MiCarpeta
</pre>

- Create a File
<pre>
New-Item -ItemType File archivo.txt

or

"" | Out-File archivo.txt
</pre>

- Erase a File or Folder
<pre>
File:
Remove-Item archivo.txt

Folder with it content
Remove-Item MyFolder -Recurse -Force

alias:
del archivo.txt
rm archivo.txt
</pre>

3- View File Content

<pre>
Get-Content archivo.txt
  
alias:
cat archivo.txt
</pre>

4- Copy and Move Files

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


#### Variables y Objects (Basics)

1- Create a Variable
<pre>
$nombre = "Yilmer"
</pre>

2- Print a Variable
<pre>
$nombre
</pre>

3- PowerShell works with objects, for example:
<pre>
Get-ChildItem | Select-Object Name, Length
</pre>

#### Environment Manage

1- Activate an Conda Environment
<pre>
conda activate mi_env
</pre>

2- Deactivate an Environment
<pre>
conda deactivate
</pre>

3- Activate a venv:
<pre>
.\mi_env\Scripts\Activate.ps1
</pre>

