# SETTING UP HARDHAT

Hardhat is an Ethereum development environment, ideal for developers who aim to create smart contracts or DApps. 

It simplifies the process by providing a platform for testing, debugging, and deployment, offering a more streamlined development experience.


## PRE-REQUISITES

To begin interacting with hardhat, the following need to be setup;

`nodejs`.

`npm`

To setup `nodejs` and `npm`, follow these instructions [here.](https://nodejs.org/en/download/package-manager)

For successful installation, checking the node and npm version should give you this;

```
hp@Cyndie:~$ npm -v
9.1.3
hp@Cyndie:~$ node -v
v18.16.0
hp@Cyndie:~$ 

```
## 1. INSTALLING HARDHAT

We'll now install hardhat to setup our environment for deploying our smart contract on the `mara-testnet`;

### Initialize `npm`
  
 We'll first create an empty directory (you can also clone your desired github repository). I called mine `maracontract`;
 
 You can now open the directory in your desired IDE, can be VSCode or Remix IDE. For this tutorial we'll use VSCode.
 
We'll first initialize `npm` by running the `npm init` command inside our `maracontract` directory;

```
root@Cyndie:/home/hp/Desktop/maracontract# npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (maracontract) 
version: (1.0.0) 
description: deploying test smart contract on mara-testnet
entry point: (index.js) 
test command: 
git repository: 
keywords: mara-testnet
author: Cyndie
license: (ISC) 
About to write to /home/hp/Desktop/maracontract/package.json:

{
  "name": "maracontract",
  "version": "1.0.0",
  "description": "deploying test smart contract on mara-testnet",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [
    "mara-testnet"
  ],
  "author": "Cyndie",
  "license": "ISC"
}


Is this OK? (yes) 
root@Cyndie:/home/hp/Desktop/maracontract# npm install --global hardhat
```
As you can see above, it walks you through a series of questions so as to generate an appropriate `package.json` file;

```
package name:
version:
description:
entry point:
test command:
git repository:
keywords:
author:
license:

```
You can skip through this section if you would like to tailor the `package.json` file much more. 

### Install hardhat

Once `npm` is initialized, we can now install hardhat globally using this command;

`npm install --global hardhat`

Successful installation should show something like this;

```
changed 323 packages in 43s

76 packages are looking for funding
  run `npm fund` for details
```

**NB** If you come across such an error while installing hardhat, try running the command again as root;

```
....
npm ERR! Error: EACCES: permission denied, mkdir '/usr/local/lib/node_modules/hardhat'
npm ERR!  [Error: EACCES: permission denied, mkdir '/usr/local/lib/node_modules/hardhat'] {
npm ERR!   errno: -13,
npm ERR!   code: 'EACCES',
npm ERR!   syscall: 'mkdir',
npm ERR!   path: '/usr/local/lib/node_modules/hardhat'
npm ERR! }
npm ERR! 
npm ERR! The operation was rejected by your operating system.
npm ERR! It is likely you do not have the permissions to access this file as the current user
npm ERR! 
npm ERR! If you believe this might be a permissions issue, please double-check the
npm ERR! permissions of the file and its containing directories, or try running
npm ERR! the command again as root/Administrator.
....
```
And with that we have installed hardhat!! We can now go to step 2.

## 2. CREATING A NEW HARDHAT PROJECT

While still in the `maracontract` directory, we'll now create a new hardhat project using the `npx hardhat` command;

```
root@Cyndie:/home/hp/Desktop/maracontract# npx hardhat
888    888                      888 888               888
888    888                      888 888               888
888    888                      888 888               888
8888888888  8888b.  888d888 .d88888 88888b.   8888b.  888888
888    888     "88b 888P"  d88" 888 888 "88b     "88b 888
888    888 .d888888 888    888  888 888  888 .d888888 888
888    888 888  888 888    Y88b 888 888  888 888  888 Y88b.
888    888 "Y888888 888     "Y88888 888  888 "Y888888  "Y888

Welcome to Hardhat v2.14.0

✔ What do you want to do? · Create a JavaScript project
✔ Hardhat project root: · /home/hp/Desktop/maracontract
✔ Do you want to add a .gitignore? (Y/n) · y
✔ Help us improve Hardhat with anonymous crash reports & basic usage data? (Y/n) · y
✔ Do you want to install this sample project's dependencies with npm (hardhat @nomicfoundation/hardhat-toolbox)? (Y/n) · y


npm install --save-dev hardhat@^2.14.0 @nomicfoundation/hardhat-toolbox@^2.0.0
```
You can decide to create a Javascript/Typescript project depending on your project, or create an empty hardhat configuration file `hardhat.config.js` with your own specifications.

**N.B** It's important to include the `.gitignore` file as well, as you don't want to push some secret files we'll interact with later on, such as the `.env` file holding your private key.

The `hardhat-toolbox` is also necessary so we can install all the dependencies needed at once.

The message below indicates that the project was created successfully;

```
Project created

See the README.md file for some example tasks you can run

Give Hardhat a star on Github if you're enjoying it!

     https://github.com/NomicFoundation/hardhat
```

### Hardhat Network Plugin

**N.B.** For a seamless experience, it's also recommended to install the Hardhat Network Plugin, so that Hardhat can interact with other networks as well aside from its own. Which in our case, will be the `mara-testnet`.

You'll use the `npm install --save-dev @nomiclabs/hardhat-ethers ethers` command to install the `hardhat-ethers` plugin.

It will integrate the `Ethers.js` library, which we'll use when interacting with Ethereum-based applications.

### `dotenv` module

We'll also install `dotenv` module, which will load our private key from the `.env` file we discussed earlier on;

You'll use the `npm install dotenv` command to install the module.

```
root@Cyndie:/home/hp/Desktop/maracontract# npm install dotenv

added 1 package, and audited 714 packages in 13s
....
```

## 3. CONFIGURING HARDHAT

We'll then configure Hardhat, through the `hardhat.config.js` file, so we can specify the network we'll deploy our smart contract in.

### Getting the private key

We'll first go to our Metamask wallet (it should still be configured to the mara-testnet network), and click on the 3 dots on the upper right to get into **Account Details**;

![accdeets](https://github.com/CyndieKamau/Docs/assets/63792575/b58f35f6-dfcd-40a2-9dff-259ee06ac5cf)

We'll then be directed to our wallet details, click on the `Export Private Key` button;

![exportkey](https://github.com/CyndieKamau/Docs/assets/63792575/3f7892db-71f7-4742-b0cc-001aac4f80d0)

You'll then be prompted to type in your password to show your private key, remember not to share it with anyone!!!

![confirm](https://github.com/CyndieKamau/Docs/assets/63792575/e91c41a9-a440-479a-8692-84574109148d)

Copy the private key, then back in our workspace, you'll create a `.env` file; You'll paste the private key as follows;

```
PRIVATE_KEY="abcdef"
```
Save the file, and ensure its listed in the `.gitignore` file;

```
node_modules
.env
coverage
coverage.json
typechain
typechain-types

# Hardhat files
cache
artifacts
```

### Configuring the `hardhat.config.js` file;

So here's how our `hardhat.config.js` file will look like;

```
require("@nomicfoundation/hardhat-toolbox");
require('dotenv').config({path: '.env'});

/** @type import('hardhat/config').HardhatUserConfig */
module.exports = {
  defaultNetwork: "maratestnet",
  networks: {
    maratestnet: {
      url: "https://mara-testnet.calderachain.xyz/http",
      accounts: [process.env.PRIVATE_KEY],
      chainId: 123456,
    },
  },
  solidity: {
    version: '0.8.9',
    settings: {
      optimizer: {
        enabled: true,
        runs: 200,
      },
    },
  },
};


```

Here's the breakdown;

* `require("@nomicfoundation/hardhat-toolbox");` - This line imports the Hardhat toolbox plugin, which adds additional tools and functionalities to our Hardhat environment.


* `require('dotenv').config({path: '.env'});` - This line loads our `PRIVATE_KEY` from our `.env` file.

* `defaultNetwork: "maratestnet"` - It sets the default network for Hardhat to use when executing our scripts to `maratestnet`.

* `networks: {...}` - This object contains the configuration for our mara testnet. It specifies the URL to connect to the `maratestnet` network, the account private key for transactions (loaded from `.env`), and the network's chain ID.

* `solidity: {...}` - This object sets up the Solidity compiler. It specifies our Solidity language version, and enables an optimizer that attempts to reduce the cost of our contract by minimizing the amount of bytecode it contains.








