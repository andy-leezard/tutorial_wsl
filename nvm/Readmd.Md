# Installing nvm on Debian Linux

Open a terminal window on your Debian Linux machine.

Update your package manager's cache by running the following command:

```bash
sudo apt-get update
```

Install the dependencies needed to run nvm by running the following command:

```bash
sudo apt-get install build-essential libssl-dev
```

Download the nvm installation script using curl:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

This will download and run the nvm installation script. The script will clone the nvm repository from Github and add the necessary environment variables to your shell profile.

Note: You can specify a different version of nvm by changing the URL to the installation script. Check the nvm releases page for the latest version.

After the script completes, you'll need to refresh your terminal for the changes to take effect. You can do this by either opening a new terminal window or running the following command:

```bash
source ~/.bashrc
```

This will reload your bash profile and update the environment variables.

Verify that nvm is installed by running the following command:

```
nvm --version
```

This should output the version of nvm that you just installed.

Congratulations! You have successfully installed nvm on your Debian Linux machine.

You can now use nvm to manage multiple Node.js versions on your system.