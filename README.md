# Lab_00-Write-Up
- Brian Luu  <br>
- Pasadena City College  <br>
## Installing Git/Cmake/VSC && VSC extensions.
### PowerShell Pre-req.
Type PowerShell in the search bar and run it as administrator.  <br>
Then inside the shell type "Set-ExecutionPolicy RemoteSigned"   <br><br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/49548807-5faa-4540-bc73-0e02c820cb4e)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/096d0394-8dd9-4f2d-bd70-e7862d27f29c)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/0c866b2a-4caa-479d-9400-74c2b3640074)  <br><br>
Type in y and press enter. <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/42110158-bccb-4700-a8c0-9a5bfa94e50f)  <br><br>

### Batch File Creation.
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
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/43e2eb3f-75bd-447b-87b1-04290df99c09)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/04b4c3b8-78f4-49dc-b39c-c6967ccd8a36)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/2fe13bc3-4e20-405b-bd1e-068f731880c4)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/b244b240-0cfd-4e94-9675-f915f8f1e46c)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/6aeb78b8-3c32-4b25-b481-cfe642b33cd9)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/73babd0b-5e37-4216-b74c-6057e2ac4424)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/e12ef783-d520-4a73-9aef-6b2a828d6f8c)  <br>


<br><br><br>
## MinGW Installation
Click on this link and follow the installation instructions. [MinGW install](https://sourceforge.net/projects/mingw/) <br> 

Right click and press mark for installation for all of the packages.  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/0bd0c2d4-26c4-4f53-a583-d44567adbeb0)  <br><br>

Now click installation and press apply changes. <br>
Then wait for the prompt to say "All changes were applied successfully; you may now close this dialoug." <br>
or <br>
Click the checkbox to close the dialouge after the installation finishes <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/56c6c43e-7164-4ea5-b86f-d514cb9168c2)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/690b2147-54e1-49c3-8698-9c3db0fb037b)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/e2c889df-c254-4319-8188-735268e40f63)  <br>

## MinGW Setup
Now we will set the MinGW path. <br> 
1.) Go to the search bar and type in Path <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/61f74c36-b6eb-433a-a801-3781b11aef14)  <br>

2.) Click on the Path in System variables then click edit <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/55fd7249-ad4e-4c38-98ed-f61cc4b68b89)  <br>

3a.) Click New on the top right. <br> 
3b.) Then type in C:\MinGW\bin <br> 
3c.) Click ok. <br><br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/90bdfef4-9718-4f5e-a1e8-806589878683)  <br>
