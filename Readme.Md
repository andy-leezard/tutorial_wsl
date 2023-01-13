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

6. Check that the APT Package Manager is correctly installed by running this simple command: **_sl_**
![Alt text](/imgsrc/linux_sl.png?raw=true "Optional Title")
- Oh look, this train is right on time unlike most real ones.

7. OK IT'S TIME TO GET SERIOUS. Open up the real terminal tab to enter Ubuntu.
![Alt text](/imgsrc/terminal_ubuntu.png?raw=true "Optional Title")

- First thing you should know, is that whenever you start up a new Linux terminal session, it runs a startup script that you can configure in the **_.bashrc_** file. Bash is a programming language used to run codes from the terminal.
- To get to know Bash, create an **environment variable** called "ps1" (Prompt String <sub>value</sub>) in the **_.bashrc_** file.
- Currently you might see something like, **_:mnt/c/Users/UserName$_**. (full working directory, system name, username)
You can change the way it looks by modifying the **_.bashrc_** file located in the Home directory.
- If you're a mega legendary developper expert in **_Vim_**, you would know how to do it: **_vi ~/.bashrc_**
- If you're a VS Code fan like me, as we always do: **_code ~/.bashrc_**

![Alt text](/imgsrc/vscode_first_bash_env_var.png?raw=true "Optional Title")

- Do you see the Prompt String has changed according to the **_.bashrc_** file?
![Alt text](/imgsrc/terminal_ubuntu_ps1_modified.png?raw=true "Optional Title")