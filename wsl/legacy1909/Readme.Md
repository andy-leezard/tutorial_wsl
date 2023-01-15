**WELCOME, WE DON'T HAVE TIME, LET'S GET TO THE POINT.**

# REQUIREMENTS

1. **Windows 10 Pro** - **Version 1909** <sup>(November 2019 update)</sup> **or older**

# STEPS

1. Open PowerShell. Run this command : **_Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux_**
![Alt text](/wsl/legacy1909/imgsrc/powershell_enable_feature.png?raw=true "Optional Title")

2. Your computer will ask to restart, let it.

3. Go to Microsoft Store -> Search for Ubuntu, **get it**.
![Alt text](/wsl/legacy1909/imgsrc/ms_store_ubuntu.png?raw=true "Optional Title")

- If you want other distros, you can: **wsl --list --online**
- Please keep in mind that in this tutorial, I am using Ubuntu. Some commands may not work in other distros.

4. The magic word is **_wsl_**. This will take you to the Linux world on your Windows machine.

![Alt text](/wsl/legacy1909/imgsrc/terminal_run_wsl.png?raw=true "Optional Title")

- (OPTIONAL) Run command: **_lsb_release -a_** to check your Ubuntu version.
- (OPTIONAL) Run command: **_htop_** to monitor your machine.

5. Update APT by running these commands:

- **_sudo apt update_**
- **_sudo apt upgrade_**
- Tip for beginners: APT (Advanced Packaging Tool) is a command-line tool used to manage softwares.

- (OPTIONAL FOR FUN) To check that your apt is operational, install **_sl_** by running this command: **_sudo apt-get install sl_**
![Alt text](/wsl/legacy1909/imgsrc/linux_sl.png?raw=true "Optional Title")

- Oh look! this train is right on time unlike most real ones.


6. OK IT'S TIME TO GET SERIOUS. Open up the real terminal tab to enter Ubuntu.
![Alt text](/wsl/legacy1909/imgsrc/terminal_ubuntu.png?raw=true "Optional Title")

- First thing you should know, is that whenever you start up a new Linux terminal session, it runs a startup script that you can configure in the **_.bashrc_** file. Bash is a programming language used to run codes from the terminal.
- To get to know Bash, create an **environment variable** called "ps1" (Prompt String <sub>value</sub>) in the **_.bashrc_** file.
- Currently you might see something like, **_:mnt/c/Users/UserName$_**. (full working directory, system name, username)
  You can change the way it looks by modifying the **_.bashrc_** file located in the Home directory.
- If you're a mega legendary developper expert in **_Vim_**, you would know how to do it: **_vi ~/.bashrc_**
- If you're a VS Code fan like me, as we always do: **_code ~/.bashrc_**

![Alt text](/wsl/imgsrc/vscode_first_bash_env_var.png?raw=true "Optional Title")

- Do you see the Prompt String has changed according to the **_.bashrc_** file?
![Alt text](/wsl/legacy1909/imgsrc/terminal_ubuntu_ps1_modified.png?raw=true "Optional Title")

7. Using **_zsh_**.

- Is **_zsh_** already installed on your system? Ask it by running this command: **_zsh --version_**
- If not, it will kindly guide you to install it.
- Change your default shell to **_zsh_** running this command : **_chsh -s $(which zsh)_**

- (RECOMMENDED) While you're at it, install [**_OH MY ZSH_**](https://github.com/ohmyzsh/ohmyzsh), the powerful interactive framework that helps you with **_zsh_** configuration. Use the curl request.

![Alt text](/wsl/imgsrc/github_oh_my_zsh.png?raw=true "Optional Title")
![Alt text](/wsl/imgsrc/zsh_oh_my_zsh.png?raw=true "Optional Title")
![Alt text](/wsl/imgsrc/zsh_which_shell.png?raw=true "Optional Title")

- (OPTIONAL) Get to know .zshrc config by changing theme. Just make it random for fun.

![Alt text](/wsl/imgsrc/vscode_zshrc_theme_random.png?raw=true "Optional Title")

8. Hook things up with VS Code. Get this extension.

![Alt text](/wsl/imgsrc/vscode_wsl_extension.png?raw=true "Optional Title")

- Open VS Code in the WSL. Ignore the message that you're not using WSL2 if you see one, you can upgrade your WSL kernel later.

![Alt text](/wsl/imgsrc/vscode_open_wsl_window.png?raw=true "Optional Title")

- Boom, now you're building in Linux.

![Alt text](/wsl/imgsrc/vscode_using_wsl.png?raw=true "Optional Title")