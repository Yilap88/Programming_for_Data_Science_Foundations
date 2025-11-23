### Basic Guide of cmd

#### What is cmd?
cmd stands for command and is the command console for Windows. It allows you to execute instructions without using graphic windows interfaces. It is useful for browsing folders, creating files, executing programs and managing networks, among other things

#### How to execute cmd?

There are three ways:  
- Press Win + R, type cmd and press enter.  
- Write cmd in the Windows Search bar.  
- In a folder → Shift + rigth clic → "Open command window here"

#### Basic Commands in cmd

1- View Current Folder  
<pre>
cd
</pre>

2- View Files and Folders  
<pre>
dir
</pre>

3- Change Folder   
<pre>
Open a Folder  
cd folder_name  
  
Move up a level  
cd..
  
Open Unit D:  
D:
</pre>

4- Create Folders and files  
<pre>
Folder  
mkdir my_folder  
  
File  
type nul > file.txt
</pre>

5- Erase Folders and files  
<pre>
Folder  
rmdir folder /s /q
  
File  
del file.txt
</pre>

6- Rename  
<pre>
ren file.txt new_name.txt
</pre>

7- Viewing the contents of a file
<pre>
type file.txt
</pre>

#### Programs Execution

1- In your current directory, just call the program  
<pre>
python
</pre>

2- In other directory
<pre>
"C:\Ruta\program.exe"
</pre>
