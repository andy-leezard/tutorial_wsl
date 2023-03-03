# Windows

```shell
wsl --list --online
wsl --install -d Kali-linux
wsl.exe --update
```

# Kali

```bash
sudo apt update && sudo apt upgrade -y
```

- Add more packages [HERE](https://www.kali.org/tools/)

- If you're lazy and you want all tools
```bash
sudo apt install kali-linux-everything
```

- If you're a minimalist...? (2GB)
```bash
sudo apt install kali-tools-top10
```

- If you're like me you'll keep it optimal.

# GUI
```bash
sudo apt install kali-desktop-xfce -y
sudo apt install xrdp -y
sudo service xrdp start
sudo ifconfig
```

- Copy that `inet` value

![Alt text](/wsl/kali/imgsrc/ifconfig.png?raw=true "Optional Title")

- Paste it on the **Remote Desktop Connection**

![Alt text](/wsl/kali/imgsrc/remote_desktop_connection.png?raw=true "Optional Title")

- Login with the same credentials, leave the session `xorg` as is.

# Air

## REQUIREMENT

- Have you got an external wireless lan adapter? If not... you may wanna get one.

```bash
sudo apt install aircrack-ng
sudo apt install pciutils
```