# Lab_00-Write-Up
- Brian Luu  <br>
- Pasadena City College  <br>
## Installing Git/Cmake/VSC && VSC extensions.
Copy and paste this into  a new txt document and then change the namme so the ___.txt is now ___.bat <br>
Now we will right click the bat file and run it as an administrator. We will do this 3x just to be sure everything is installed.
```
REM Install Chocolatey (if needed)
where choco.exe > nul 2>&1 || powershell.exe -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))"

REM refreshing environment. 
call refreshenv.cmd

REM Install Git version control system (if needed)
where git.exe > nul 2>&1 || choco install git -y

REM Install CMake build system (if needed)
where cmake.exe > nul 2>&1 || choco install cmake --installargs 'ADD_CMAKE_TO_PATH=User'

REM Install Clang C++ compiler (if needed)
where clang.exe > nul 2>&1 || choco install llvm -y

REM Install Google Chrome web browser (if needed)
where chrome.exe > nul 2>&1 || choco install googlechrome -y

REM Install TightVNC VNC server (if needed)
where tvnserver.exe > nul 2>&1 || choco install tightvnc -y

REM Install Visual Studio Code text editor (if needed)
where code.exe > nul 2>&1 || choco install vscode -y

REM refreshing environment.
call refreshenv.cmd

REM Install Visual Studio Code C++ extension (if needed)
code --list-extensions | findstr /C:"ms-vscode.cpptools" > nul 2>&1 || code --install-extension ms-vscode.cpptools

REM Install Visual Studio Code Cmake Tools Extension (if needed)
code --list extensions | findstr /C:"ms-vscode.cmake-tools" > nul 2>&1 || code --install-extension ms-vscode.cmake-tools
``` 
<br><br><br>
## MinGW Installation and Setup.
Click on this link and follow the installation instructions.
[MinGW install](sourceforge.net/projects/mingw/)

![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/820e4ec0-957d-4bdb-be69-45acb0c4c663) <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/86749944-451d-4292-a601-aa5960b537d1) <br>

Right click and press mark for installation for all of the packages.  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/718dd8e5-94eb-4eb3-81f1-2c56a18294cd)  <br><br>
Now click installation and press apply changes. <br>
Then wait for the prompt to say "All changes were applied successfully; you may now close this dialoug." <br>
or <br>
Click the checkbox to close the dialouge after the installation finishes <br><br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/14dd5d96-5792-488a-82dd-379243dd6c5f)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/05b6205a-d126-4361-9e0f-f290b95358b6)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/0e17e5f6-bfe6-4c5f-aaeb-90e726653401)  <br>



Now we will set the MinGW path. <br> 
1.) Go to the search bar and type in Path <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/7c032643-4e18-4b9b-89f0-a04f1e77dd07)  <br>

2.) Click on the Path in System variables then click edit <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/ece471cc-ba96-4403-bf07-96a3b98a0752)  <br>

3a.) Click New on the top right. <br> 
3b.) Then type in C:\MinGW\bin <br> 
3c.) Click ok. <br><br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/3e706a6c-8bac-4644-b257-dc201b1fc807)  <br>
