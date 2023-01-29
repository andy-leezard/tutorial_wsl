**WELCOME, WE DON'T HAVE TIME, LET'S GET TO THE POINT.**

# REQUIREMENTS

1. **Windows 10 Pro** **Version 2004** <sup>(May 2020 update)</sup> **or higher**
- Install available Windows updates if you have a lesser version.
- In this tutorial, I used the version **_22H2_**.
- If you really need to use an outdated version of Windows, use the [legacy method](/wsl/legacy1909/Readme.Md). However that will result in installing WSL1 kernel by default. You'll need to configure that separately.

# STEPS (RENEWED FOR WSL2)

1. Run this command as admin: **`wsl --list --online`**
- Choose one from the list of available distros. I'll go with **Debian**.
 ![Alt text](/wsl/imgsrc/terminal_wsl_list_online.png?raw=true "Optional Title")

2. Your system needs to reboot, let it.

 ![Alt text](/wsl/imgsrc/installing_debian.png?raw=true "Optional Title")

- This will litterally take few minutes. You have time to do some neck and shoulder stretches. Maybe some push-ups while you're at it. Health is important 💪.

3. Update the WSL Kernel by running this command as admin on the regular Windows terminal: **`wsl --update`**

4. Now on the Linux terminal, run this command to check the installed Linux version: **`cat /etc/issue`**

- There are also other ways to check it up depending on the distro you're using, but this is one simple way to go on Debian.

5. Get to know **_BASH_** by taking a look at **_.bashrc_**.

- Tip for beginners: whenever you start up a new Linux terminal session, it runs a startup script that you can configure in the **_.bashrc_** file. Bash is a programming language used to run codes from the terminal.
- To get to know Bash, create an **environment variable** called "ps1" (Prompt String <sub>value</sub>) in the **_.bashrc_** file.
- Currently you might see something like **`:mnt/c/Users/UserName$`**.
  You can change the way it looks by modifying the **_.bashrc_** file located in the Home directory.
- If you're a mega legendary developper expert in **_Vim_**, you would know how to do it: **`vi ~/.bashrc`**
- If you're a VS Code fan like me, as we always do: **`code ~/.bashrc`**

![Alt text](/wsl/imgsrc/vscode_first_bash_env_var.png?raw=true "Optional Title")

- Notice that the Prompt String has changed according to the **_.bashrc_** file.

![Alt text](/wsl/imgsrc/debian_ps1_modified.png?raw=true "Optional Title")

6. Update APT by running these commands:
```
sudo apt update
sudo apt upgrade
```
- Tip for beginners: APT (Advanced Packaging Tool) is a command-line tool used to manage softwares.

7. Install **_curl_**: **`sudo apt install curl`**

- Test if it's correctly installed and operational: **`curl help`**

8. Install **_git_**: **`sudo apt install git`**

- Test if it's correctly installed and operational: **`git --version`**

- Config Git
```
git config --global user.name "YOUR USERNAME"
git config --global user.email "YOUR EMAIL ADDRESS"
git config --global core.autocrlf input
```

- NOTE: ```git config --global core.autocrlf input``` will prevent _carriage-return_ flags (**_\r_**) confusing git state when worked both on Windows and Linux.
- Likewise, on Windows System, the ```input``` part should be ```true``` when globally configuring git.

9. Install **_clang_**: **`sudo apt install clang`**

- Test if it's correctly installed and operational: **`clang --version`**

9. Using **_zsh_**.

- Is **_zsh_** already installed on your system? Ask it by running this command: **`zsh --version`**

- If not, install **_zsh_** by running this command: **`sudo apt install zsh`**

- Test if it's correctly installed and operational by running this command: **`zsh --version`**

- (RECOMMENDED) While you're at it, install [**_OH MY ZSH_**](https://github.com/ohmyzsh/ohmyzsh), the powerful interactive framework that helps you with **_zsh_** configuration. Use the curl request as instructed on the Github page.

- Change your default shell to **_zsh_** if you haven't already with **_OH MY ZSH_**: **`chsh -s $(which zsh)`**

![Alt text](/wsl/imgsrc/github_oh_my_zsh.png?raw=true "Optional Title")
![Alt text](/wsl/imgsrc/zsh_oh_my_zsh.png?raw=true "Optional Title")

- (OPTIONAL) Get to know .zshrc config by changing theme. Just make it random for fun. If you find an interesting theme, you can change it to that later.

![Alt text](/wsl/imgsrc/vscode_zshrc_theme_random.png?raw=true "Optional Title")
![Alt text](/wsl/imgsrc/zsh_which_shell.png?raw=true "Optional Title")

9. Hook things up with VS Code. Get this extension.

![Alt text](/wsl/imgsrc/vscode_wsl_extension.png?raw=true "Optional Title")

- Open VS Code in the WSL.

![Alt text](/wsl/imgsrc/vscode_open_wsl_window.png?raw=true "Optional Title")

- Boom, now you're building in Linux.

![Alt text](/wsl/imgsrc/vscode_using_wsl.png?raw=true "Optional Title")