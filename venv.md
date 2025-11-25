## venv - Environment Config for Python Projects for VSCode

This Markdown document outlines the main instructions for installing, using and managing Python project environments in VS Code.

For CMD and Powershell usage, click here...  
[cmd](cmd.md)  
[Powershell](Powershell.md)


## venv Manager
venv is a Python tool that enables you to create virtual environments: isolated spaces in which you can install libraries without affecting the rest of the system.

With venv you can:
- Having projects with different versions of libraries
- Avoid conflicts between dependencies.
- Keep each project clean and organized

To use venv you need python 3 installed, you can check the version as follows in PowerShell:

<pre>
python --version
or
py --version
</pre>

### Environment creation

Command:
<pre>
python -m venv my_environment
</pre>

This creates a folder called 'my_environment' that contains:
- Local Python for the environment
- scripts to activate it;
- A site-packages folder for your libraries.
  
You can use any name, such as env, .venv or virtual.

### Environment activation

Powershell
<pre>
.\my_environment\Scripts\Activate.ps1
</pre>

cmd
<pre>
my_environment\Scripts\activate.bat
</pre>

Gitbash
<pre>
source my_environment/bin/activate
</pre>

Once activated, the name of the environment will appear at the beginning of the code line as follows:
*(my_environment) PS C:\Users\Yilmer>*

### Installation of libraries inside the environment

Once the environment is active, type:
<pre>
pip install name_of_library
pip install numpy
</pre>
*The libraries are isolated within their environment.  *

The next command will show you what is installed:
<pre>
pip list
</pre>

### Environment deactivation
<pre>
deactivate
</pre>

### Environment erasure
<pre>
Remove-Item my_environment -Recurse -Force
</pre>

### Environment creation with a specific Python version
<pre>
py -3.11 -m venv env311
</pre>

### Practical tips

**- Use the name ".venv" for your environment:** Many tools detect it automatically.  

**- Agregar .venv al .gitignore si usas Git:** You should not upload the environment to the repository.
<pre>
.venv/
</pre>

**- Crear un requirements.txt:** 
To save your libraries:
<pre>
pip freeze > requirements.txt
</pre>

And then reinstall them:
<pre>
pip install -r requirements.txt
</pre>







