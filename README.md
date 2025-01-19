# WinTaskbarKill
Kills Win11/10 Taskbar Permantly (Silent)


Go download nircmd https://www.nirsoft.net/utils/nircmd.html

Create a folder and name it "HideTaskbar" in the root of your OS (Commonly >C:\...)

Extract nircmd into the folder.

Create a .txt file and imput:
        Set-Location -Path "C:\HideTaskbar"
		
Under the line, imput these two
        .\nircmd.exe win trans class Shell_TrayWnd 255
        .\nircmd.exe win trans class Shell_TrayWnd 256
		
Save as HideTaskbar.ps1 and have it in the root folder of "HideTaskbar"

##########################################################################

Now do win+R and imput "shell:startup"

Create a new shortcut in the folder and imput:
        powershell.exe -ExecutionPolicy Bypass -File "C:\HideTaskbar\HideTaskbar.ps1"

Save and dont rename
		
So, everytime you startup your system, it will run this shortcut, enabling you to bypass permission and to run the powershell file.
You can create a folder in any dir, but change the dir in the code for all.
