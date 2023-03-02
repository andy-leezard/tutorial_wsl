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

After the script completes, you'll need to refresh your terminal for the changes to take effect. You can do this by either opening a new terminal window or executing shell (`exec $SHELL`) or running the following command if you wanna stay in the same terminal session:

- Using Bash
```bash
source ~/.bashrc
```
- Using Zsh

```zsh
source ~/.zshrc
```

This will reload your bash profile and update the environment variables.

Verify that nvm is installed by running the following command:

```bash
nvm --version
```

This should output the version of nvm that you just installed.

Congratulations! You have successfully installed nvm on your Debian Linux machine.

You can now use nvm to manage multiple Node.js versions on your system.

# Installing Node

Most of the time, naturally I'd recommend to use the lts version.

```bash
nvm install --lts
nvm use --lts
node --version
```

If you know what you're doing, (mostly switching between projects...) search for available versions.
And Install a specific version you want.
If you like danger, take the most recent one from the (list)[https://nodejs.org/en/download/releases/]

```bash
nvm ls
nvm install 19.7.0
nvm use 19.7.0
node --version
```

# Switching between Node versions

(Example)
```bash
nvm list
nvm use 18.13.0
node --version
```

# Checking & updating npm version

```bash
npm --version
```

You got a feeling that it could get some updates? Run this command:

```bash
npm install -g npm@latest
```

# Installing Yarn

No need to mention that Yarn Package Manager makes the node dev env a lot easier.

```bash
npm install --global yarn
```

# Installing TypeScript

In order to run `node` commands for typescript projects, you need to install **TypeScript** globally.
(Doc)[https://code.visualstudio.com/docs/typescript/typescript-compiling]

```bash
npm install -g typescript
```

or 

```bash
yarn global add typescript
```

```bash
exec $SHELL
tsc --version
tsc --help
```

# When you wonder what global packages you got

```bash
npm list -g --depth=0
```

# Creating a Vite Project

```bash
yarn create vite
```

# Creating a Next Project

```bash
yarn create next-app
```

# Creating an Express Project

- Create a project root directory and `cd` inside that folder.

- Install dependencies
```bash
npm install express @types/express ts-node typescript
```

- Create a tsconfig.json file in your project root directory:

```json
{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "outDir": "dist",
    "strict": true,
    "esModuleInterop": true
  },
  "exclude": ["node_modules"]
}
```

- Create an app.ts file and add the following code:

```typescript
import express from 'express';

// Create a new Express application
const app = express();

// Define a route handler for the root path
app.get('/', (req, res) => {
  res.send('Hello, world!');
});

// Start the server
const port = process.env.PORT || 3000;
app.listen(port, () => {
  console.log(`Server listening on port ${port}`);
});

```

This code imports the express module and creates a new Express application. It defines a route handler for the root path (/) that sends a simple text response. Finally, it starts the server and listens on the specified port.
You can run the app using the following command:

```bash
npx ts-node app.ts
```

- Install frequently used global packages

```bash
yarn global add serve firebase-tools eas-cli
yarn global add firebase-tools
yarn global add eas-cli
```

# Creating a React Native (Expo Managed Workflow) Project

1. install : `npx expo -h`
2. authenticate : `npx expo login`
3. create an [Expo](https://expo.dev/) account : `npx expo register`
4. check auth status : `npx expo whoami`
5. 

# Building & Deploying a React Native (Expo Managed Workflow) Project

- Using EAS CLI [(Expo Application Services CLI)]((https://expo.dev/eas))
1. install : `yarn global add eas-cli` or `npm install -g eas-cli`
2. authenticate using your expo account: `eas login`

