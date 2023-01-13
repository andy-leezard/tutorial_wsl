**WELCOME, WE DON'T HAVE TIME, LET'S GET TO THE POINT.**

# REQUIREMENTS

1. Windows 10 Pro and your discipline

# STEPS

1. Open PowerShell. Run this command : **_Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux_**
![Alt text](/imgsrc/powershell_enable_feature.png?raw=true "Optional Title")

2. Your computer will ask to restart, let it.

3. Go to Microsoft Store -> Search for Ubuntu, **get it**.
![Alt text](/imgsrc/ms_store_ubuntu.png?raw=true "Optional Title")

- (OPTIONAL) Download Terminal for Windows. Use this fancy terminal.
![Alt text](/imgsrc/ms_store_terminal.png?raw=true "Optional Title")

4. The magic word is **_wsl_**. This will take you to the Linux world on your Windows machine.

![Alt text](/imgsrc/terminal_run_wsl.png?raw=true "Optional Title")

- (OPTIONAL) Run command: **_lsb_release -a_** to check your Ubuntu version.
- (OPTIONAL) Run command: **_htop_** to monitor your machine.

5. Get APT Package Manager by running this command: **_sudo apt-get install sl_**

- (TROUBLESHOOT) It doesn't work? Let me guess, "**_E: Unable to locate package package_name_**"?
- Don't worry, update the repository cache with this new command, and then retry the previous command.: **_sudo apt update_**

