# Lab_00-Write-Up
- Brian Luu  <br>
- Pasadena City College  <br>

# Index:
- ### [Powershell Prerequesite](#Powershell-Prerequesite) 
- ### [Manual Batchfile Creation](#BatchFile-Creation)
- ### [Download Batchfile](#Batchfile-Download)

<br><br><br><br><br><br><br>

<span style="color:red"> red text</span>.

## Powershell Prerequesite
Type PowerShell in the search bar and run it as administrator.  <br>
Then inside the shell type "Set-ExecutionPolicy RemoteSigned"   <br><br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/49548807-5faa-4540-bc73-0e02c820cb4e)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/096d0394-8dd9-4f2d-bd70-e7862d27f29c)  <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/0c866b2a-4caa-479d-9400-74c2b3640074)  <br><br>
Type in y and press enter. <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/42110158-bccb-4700-a8c0-9a5bfa94e50f)  <br><br>

<br><br><br><br><br><br><br>

## Batch File Creation.
### Batch File Creation.
To create a batch file create a new .txt file and rename it so that it ends with .bat.

#### Chocolatey
```
REM Install Chocolatey (if needed)
where choco.exe > nul 2>&1 || powershell.exe -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))"
```
<br>

#### Build
```
REM Install Git version control system (if needed)
where git.exe > nul 2>&1 || choco install git -y

REM Install CMake build system (if needed)
where cmake.exe > nul 2>&1 && choco upgrade cmake|| choco install cmake --installargs 'ADD_CMAKE_TO_PATH=User'

REM Install Clang C++ compiler (if needed)
where clang.exe > nul 2>&1 || choco install llvm -y

REM Install Google Chrome web browser (if needed)
where chrome.exe > nul 2>&1 || choco install googlechrome -y

REM Install TightVNC VNC server (if needed)
where tvnserver.exe > nul 2>&1 || choco install tightvnc -y
```

<br>

#### VSCode 
```
REM Install Visual Studio Code text editor (if needed)
where code.exe > nul 2>&1 || choco install vscode -y

REM refreshing environment.
call refreshenv.cmd

cd /d %~dp0
for /F "tokens=*" %%A in (name of text file .txt) do %%A
```
Create a text file with these comamnds and put the name of the text file between the bracket in the command above.

```
REM Install Visual Studio Code C++ extension (if needed)
code --list-extensions | findstr /C:"ms-vscode.cpptools" > nul 2>&1 || code --install-extension ms-vscode.cpptools

REM Install Visual Studio Code Cmake Tools Extension (if needed)
code --list extensions | findstr /C:"ms-vscode.cmake-tools" > nul 2>&1 || code --install-extension ms-vscode.cmake-tools
```
You should end up with three .bat files and a .txt file. <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/d3a6b6b4-2cab-4cbe-affa-41cca276bef2) <br>
![image](https://github.com/Nairbuul/Lab_00-Write-Up/assets/42011526/ad6b4671-8c25-4af5-86e7-8381233cab0f) <br>
