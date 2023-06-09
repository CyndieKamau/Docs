
# MARA Documentation

## Getting Started with Mara Testnet
_________________
## Connecting MARA Testnet to Metamask

Metamask is a digital wallet and bridge that connects users to the decentralized web.

It is a browser extension available for Google Chrome, Firefox, Opera, and Brave browsers, and as a standalone mobile app on iOS and Android. 

MetaMask allows users to interact with the Ethereum blockchain, as well as Ethereum-compatible blockchains like MARA, and manage their digital assets from the convenience of their browser or mobile device.

## 1. CREATING A METAMASK WALLET

Go to Chrome Web store and search for Metamask;

![chromestore](https://github.com/CyndieKamau/Docs/assets/63792575/653e8645-6444-4a44-8562-3a9832c2fa0d)


Click on `Add to Brave/Chrome` button;

![addbrave](https://github.com/CyndieKamau/Docs/assets/63792575/ff83b379-c6e2-4aed-a41c-1c7bbfc9d8f3)


You’ll be directed to Metamask’s home page; Read the policies, select I agree, then click on the `Create a new Wallet` button;

![start2](https://github.com/CyndieKamau/Docs/assets/63792575/8bdbacb7-1447-4334-8b02-6a3124bee9b4)


You will be prompted to create a new password;

![password](https://github.com/CyndieKamau/Docs/assets/63792575/b34a137a-51c0-43f3-adb3-2b3f3a3fa2cf)



Once you've entered your password you can now click on `Create a new wallet` button;



**N.B** It's important to watch the video on how to secure your wallet; Watch the video first before clicking on the `Secure my wallet` button;



![video](https://github.com/CyndieKamau/Docs/assets/63792575/aadc176c-9a4d-4c4e-a900-d9a62fd7446c)


**IMPORTANT: Copy the Recovery Phrase and store it somewhere safe, and don't share it with anyone. You’ll be prompted to confirm the Recovery Phrase, once you reveal the Recovery Phrase, and copy it.**


![recovery](https://github.com/CyndieKamau/Docs/assets/63792575/f2a328cd-9a4b-4943-8456-f0c5a6359cad)


And with that, you’ve successfully created your metamask wallet!!! 

![success](https://github.com/CyndieKamau/Docs/assets/63792575/0ca3e853-cc62-4c8f-af7e-66ef36a399bc)





## 2. CONNECTING MARA TESTNET TO METAMASK

In the previous tutorial we created a new  Metamask wallet. Here we will now connect our Metamask wallet to the `mara-testnet` network;


By default Metamask will be configured to the Ethereum mainnet. We will add the Mara Testnet manually;


In settings first ensure the `Show Test Networks` is `ON`.

![settings](https://github.com/CyndieKamau/Docs/assets/63792575/d80e42b4-3c04-44cc-b9af-442e51890a65)


The `ON` button is to ensure that Metamask can detect both main networks (such as Ethereum mainnet), and test networks (such as Goerli testnet, mara-testnet etc);


Once that's done we can now add `mara-testnet` manually; Click on the `Add a network` button;


![addnet](https://github.com/CyndieKamau/Docs/assets/63792575/8c761861-f843-4e36-b20a-f23fac01164d)


Once that's done you can now add details of the `mara-testnet` network, as follows;


![net](https://github.com/CyndieKamau/Docs/assets/63792575/d4e73493-81a2-4d58-93d7-167b884f402a)


The details are below;


---
### Network Name;         mara-testnet

### RPC URL;              https://mara-testnet.calderachain.xyz/http

### Chain ID;             123456

### Currency Symbol;      MARA

### Block Explorer URL;   https://mara-testnet.calderaexplorer.xyz/
---


Once that's done click on `Save`, and voila! We've added the `mara-testnet` to our Metamask wallet. We will use it when deploying our smart contract to the MARA testnet.


You can now switch to mara-testnet;


![mara0](https://github.com/CyndieKamau/Docs/assets/63792575/2842b838-fcb6-458f-bf83-9fc863d9db74)



## 3. REQUESTING FAUCET FUNDS ON MARA

Faucet funds serve a crucial role, especially for beginners. 

Picture faucet funds as a kind of "free samples" in the blockchain universe. 

They provide users with a small amount of cryptocurrency, enabling them to start interacting with blockchain networks without needing to buy or mine the cryptocurrency themselves.

They are important because interacting with blockchains often involves transaction costs, known as "gas fees" in Ethereum and its compatible blockchains. 

By offering a small amount of free cryptocurrency, faucets enable new users to explore the functionalities of a blockchain, understand how transactions work, and get a feel for the system without having to invest their own money.


-------
On the metamask page, ensure you're still on the `mara-testnet` network, then copy the wallet address above.

You'll then go to the [MARA Site](https://mara.caldera.dev/) and click on the `Request faucet funds on Mara rollup` button;

![funds](https://github.com/CyndieKamau/Docs/assets/63792575/89707898-f553-4a7e-ab93-77b367c29118)


Paste your wallet address, then click on `Receive Funds` button;

Once its successful you’ll receive MARA tokens;

![200](https://github.com/CyndieKamau/Docs/assets/63792575/256f7315-bb2f-4fd7-ae2d-d03ab3a9026c)

We can now use these tokens to interact with the Mara blockchain, deploy our smart contract etc.

**N.B** With MARA you can also request for **GoerliETH** tokens for interacting with the Ethereum Goerli test network!! 

Simply switch to Goerli network, copy wallet address and request for funds;

![0goerli](https://github.com/CyndieKamau/Docs/assets/63792575/bc2ecfda-ce84-4bab-95eb-3feaca57c397)

Once its successful some GoerliETH will be transferred to your Goerli testnet address;

![1goerli](https://github.com/CyndieKamau/Docs/assets/63792575/6bb8b737-1dc0-4fd2-8be4-9487b1190c65)
--------------------------------


# SETTING UP A LOCAL DEVELOPMENT ENVIRONMENT;

# 1. SETTING UP HARDHAT 

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

## N.B SETTING UP HARDHAT FOR MACOS

To install hardhat for macos, we'll first install `npm` and `nodejs`;

* Open your terminal.
* You can install Node.js and npm using Homebrew, which is a package manager for MacOS. If you don't have Homebrew installed, you can install it using the following command:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```
* Once you have installed Homebrew, you can install Node.js and npm using the following command:

```
brew install node

```
* In your project's directory you can now install hardhat;

```
npm install --save-dev hardhat

```

* After the installation is complete, you can verify that Hardhat is installed correctly by typing:

```
npx hardhat

```
This should display the Hardhat help message, which confirms that it was installed correctly.

## SETTING UP HARDHAT FOR WINDOWS

* Install Node.js: Hardhat requires Node.js to run. Visit the Node. js website (https://nodejs.org) and download the latest LTS (Long-Term Support) version for Windows. Run the installer and follow the on-screen instructions to complete the installation.

* Open a command prompt: Press the Windows key, type `cmd`, and select the Command Prompt app to open a command prompt window as administrator.

* Install Hardhat: In the command prompt, run the following command to install Hardhat globally:
    ```
    npm install -g hardhat
    ```
 This command will download and install Hardhat from the Node Package Manager (NPM).

* Verify the installation: After the installation is complete, run the following command to verify that Hardhat is installed correctly:
    ```
    hardhat version
    ```
 This command should display the version of Hardhat installed on your system.

    

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

## N.B Set up a new Hardhat project on Windows; 

* Create a new directory for your Hardhat project. 

* In the command prompt, navigate to the directory you just created. Run the following command to initialize a new Hardhat project:

    ```
    npx hardhat init
    ```
    
 This command will set up the basic structure and configuration files for your Hardhat project.


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



# DEPLOYING SMART CONTRACT

Here's the sample smart contract we deployed on the mara testnet using hardhat;

```
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.9;

// Uncomment this line to use console.log
// import "hardhat/console.sol";

contract Lock {
    uint public unlockTime;
    address payable public owner;

    event Withdrawal(uint amount, uint when);

    constructor(uint _unlockTime) payable {
        require(
            block.timestamp < _unlockTime,
            "Unlock time should be in the future"
        );

        unlockTime = _unlockTime;
        owner = payable(msg.sender);
    }

    function withdraw() public {
        // Uncomment this line, and the import of "hardhat/console.sol", to print a log in your terminal
        // console.log("Unlock time is %o and block timestamp is %o", unlockTime, block.timestamp);

        require(block.timestamp >= unlockTime, "You can't withdraw yet");
        require(msg.sender == owner, "You aren't the owner");

        emit Withdrawal(address(this).balance, block.timestamp);

        owner.transfer(address(this).balance);
    }
}

```

To deploy the smart contract on hardhat, we'll also write the `deploy.js` script in the `scripts` folder to give deployment instructions to hardhat;

```
// We require the Hardhat Runtime Environment explicitly here. This is optional
// but useful for running the script in a standalone fashion through `node <script>`.
//
// You can also run a script with `npx hardhat run <script>`. If you do that, Hardhat
// will compile your contracts, add the Hardhat Runtime Environment's members to the
// global scope, and execute the script.
const hre = require("hardhat");

async function main() {
  const currentTimestampInSeconds = Math.round(Date.now() / 1000);
  const unlockTime = currentTimestampInSeconds + 60;

  const lockedAmount = hre.ethers.utils.parseEther("0.001");

  const Lock = await hre.ethers.getContractFactory("Lock");
  const lock = await Lock.deploy(unlockTime, { value: lockedAmount });

  await lock.deployed();

  console.log(
    `Lock with ${ethers.utils.formatEther(
      lockedAmount
    )}ETH and unlock timestamp ${unlockTime} deployed to ${lock.address}`
  );
}

// We recommend this pattern to be able to use async/await everywhere
// and properly handle errors.
main().catch((error) => {
  console.error(error);
  process.exitCode = 1;
});
``` 
With this we'll first compile our smart contract using `npx hardhat compile`;

```
hp@Cyndie:~/Desktop/maracontract$ npx hardhat compile
Compiled 1 Solidity file successfully
```

After compiling successfully we can now deploy our smart contract specifically on the testnet using this command; `npx hardhat run --network maratestnet scripts/deploy.js`;

```
hp@Cyndie:~/Desktop/maracontract$ npx hardhat run --network maratestnet scripts/deploy.js
Lock with 0.001ETH and unlock timestamp 1684107231 deployed to 0x3640dbE9b48C33b65c5000655be3184103c90648
hp@Cyndie:~/Desktop/maracontract$ 
```

We'll then verify our smart contract on Mara Block explorer;

![block](https://github.com/CyndieKamau/Docs/assets/63792575/32329c4b-83c5-4c6c-84ec-8ac817aeb932)





-----------------------------------------------


# BUILDING DAPPS ON MARA;

# Front-end integration with Mara

When it comes to developing decentralized applications (dApps) that interact seamlessly with Ethereum-based smart contracts, understanding the vital role played by certain JavaScript libraries becomes crucial.

Among these libraries, two stand out as being particularly important: `ethers.js` and `web3.js`.

These libraries act as a bridge, facilitating smooth communication and integration between our frontend application and the blockchain network where our smart contracts reside. 

They offer a collection of robust tools and functionalities that enable developers to write code that can query, inspect, and transact with smart contracts, thereby underpinning the operation of dApps.

For this tutorial we will have a look at `ethers.js`;

# `ethers.js`;

`ethers.js`is a comprehensive library for interacting with the Ethereum blockchain, and it is vital for building Ethereum dApps (decentralized applications). 

When you import ethers via `import { ethers } from 'ethers';`, you are equipping your application with a suite of utilities that will enable you to accomplish a number of important tasks, including but not limited to:

* **Interacting with Smart Contracts:** ethers.js provides an easy-to-use interface to call functions of your smart contracts, send transactions, and query contract states.

* **Connecting to Ethereum Nodes:** ethers.js enables you to connect to Ethereum nodes (such as Infura, Alchemy, or your own local node) using a provider object. This lets you query the blockchain's state, send transactions, and subscribe to blockchain events.

* **Key Management and Wallet Functionality:** ethers.js provides classes for managing Ethereum accounts, signing transactions and messages, and encrypting/decrypting wallets.

* **Parsing and Formatting Transactions:** ethers.js includes functions to parse and format Ethereum transactions and logs, making it easier to interact with blockchain data.

* **Big Number and Fixed Number Operations:** Working with large numbers and fixed point numbers in JavaScript can be tricky. ethers.js provides classes for safely handling these types of values, which is very important when dealing with cryptocurrency values.



## 1. INSTALLATION

We'll install `ethers.js` library in our frontend directory;

```
root@Cyndie:/home/hp/Desktop/maracontract/frontend# npm install --save ethers
up to date, audited 714 packages in 4s

125 packages are looking for funding
  run `npm fund` for details
```

After installation its now ready to use.

## 2. IMPORTING `ethers`;

In your react `index.js` file, you can import `ethers`;

```
import { ethers } from 'ethers';

```

## 3. CONNECTING TO `mara-testnet` via RPC;

[JSON RPC API](https://github.com/ethereum/wiki/wiki/JSON-RPC) is a light-weight, easy-to-use protocol that allows for data exchange between our application and the Ethereum network. 

`ethers.js` leverages JSON-RPC to facilitate these exchanges, allowing our dApp to seamlessly send requests and retrieve responses from the blockchain, thereby enabling a multitude of operations including querying the network state, reading data from smart contracts, and submitting transactions. 

Since the Mara blockchain is EVM (Ethereum Virtual Machine) compatible,   we will implement the `JsonRpcProvider` function from `ethers.js`, instead of `Web3Provider`, which is used on the Ethereum network.

It will provide connection to the `mara-testnet` provider, and it will hold the user's private key for signing transactions.

Here's a React code snippet for initializing the connection to the Mara blockchain on our frontend, in your `App.jsx` file;

```
import { ethers } from 'ethers';
import React, { useEffect, useState } from 'react';
import ContractArtifact from '../artifacts/contracts/Lock.sol/Lock.json'; // path to our contract's ABI JSON file

function App() {
    const [provider, setProvider] = useState(null);
    const [signer, setSigner] = useState(null);
    const [contract, setContract] = useState(null);

    // The network url for Mara testnet 
    const maraTestnetUrl = "https://mara-testnet.calderachain.xyz/http";
    
    // Our deployed contract address
    const contractAddress = '0x3640dbE9b48C33b65c5000655be3184103c90648'; 

    useEffect(() => {
        if (maraTestnetUrl) {
            const provider = new ethers.providers.JsonRpcProvider(maraTestnetUrl);
            const signer = provider.getSigner();
            const contract = new ethers.Contract(contractAddress, ContractArtifact.abi, signer);
            setProvider(provider);
            setSigner(signer);
            setContract(contract);
        } else {
            console.log('Network url is not available');
        }
    }, []);

    return (
        <div className="App">
            {/* Your app logic goes here */}
        </div>
    );
}

export default App;

```

This script is used to connect to a deployed smart contract on a specified blockchain network, using the ethers.js library and React. Here's the breakdown:

### 1. Imports
The first couple of lines are the necessary import statements.

* **import { ethers } from 'ethers';** brings in the ethers.js library, which provides a collection of utility functions to help interact with Ethereum.

* **import React, { useEffect, useState } from 'react';** imports necessary elements from React. useEffect and useState are hooks that enable React state and lifecycle features in functional components.

* **import ContractArtifact from '../artifacts/contracts/Lock.sol/Lock.json';** imports the ABI (Application Binary Interface) of your contract. The ABI is an interface used to interact with the contract, which is generated when the contract is compiled. The path is relative and should lead to your contract's JSON artifact file.

### 2. React Functional Component
This block of code defines a functional component App in React.

* **const [provider, setProvider] = useState(null);** initializes a state variable for provider with its setter function. The provider is used to interact with the Ethereum blockchain.

* **const [signer, setSigner] = useState(null);** initializes a state variable for the signer with its setter function. The signer is derived from the provider and is used to issue transactions.

* **const [contract, setContract] = useState(null);** initializes a state variable for the contract with its setter function. This will hold our contract instance.

* **const maraTestnetUrl = "https://mara-testnet.calderachain.xyz/http";** is the URL for the Mara Testnet RPC node.

* **const contractAddress = '0x3640dbE9b48C33b65c5000655be3184103c90648';** is the address at which your smart contract is deployed.

### 3.useEffect Hook
It invokes the callback function when the component mounts. Here, it is used to create a connection to the blockchain network and the smart contract.

* **const provider = new ethers.providers.JsonRpcProvider(maraTestnetUrl);** creates a new provider instance, using the Mara Testnet URL.

* **const signer = provider.getSigner();** gets a signer instance from the provider. This signer can be used to sign transactions.

* **const contract = new ethers.Contract(contractAddress, ContractArtifact.abi, signer);** creates a contract instance which we can interact with.

* **setProvider(provider); setSigner(signer); setContract(contract);** sets the state variables to our newly created instances.

### 4.React Component Return: 
This is where you define what your component will render. 

Currently, it's just rendering a div containing the text "Your app logic goes here", but this is where you would put your JSX and other components for your app's UI.







------------------------------------------------
# Understanding Mara's Layer-2 Blockchain 
--------------------------------------


Layer 2 is a secondary blockchain network that operates on top of the primary blockchain (Layer 1) to enhance its scalability, security, and speed. 

It reduces the burden on the main chain by offloading some of the transaction processing to a separate layer, thus increasing the network's overall capacity and efficiency.



## Benefits of using Layer-2 solutions

Layer-2 solutions are like add-ons to the main blockchain - think of them as extra lanes on a busy highway. Here are their benefits simplified:

* **More Room, More Speed:** By handling many transactions away from the main blockchain (off-chain), these solutions increase the network's capacity, speeding up transaction times. 

It's like opening up more cash registers in a busy supermarket - customers get served quicker!

* **Pocket-Friendly:** By minimizing the transactions on the main chain, Layer-2 solutions lower the transaction costs. 

That's good news for users as it's like getting a discount on the transaction fee!

* **Better User Experience:** Cheaper, faster transactions mean happier users. 

Layer-2 solutions improve the overall feel of using blockchain networks, enticing more people to use blockchain-based applications.

* **Enhanced Security:** These solutions also improve security. 

They do this by reducing the load on the main chain, thus lowering the risk of network congestion and potential attacks.

It's like having fewer cars on the road, reducing the risk of traffic jams and accidents.

Some even add extra security features like zero-knowledge proofs.

* **Flexibility:** Layer-2 solutions add flexibility to the blockchain.

They allow it to support a wider range of applications and uses. 

It's like having a multi-tool - you can do so much more!


## Comparison with other Layer-2 technologies

Layer-2 technologies are like different brands of cars, each with its own features and quirks. Let's look at a few key players - state channels, sidechains, plasma, rollups, and newcomers Base and Boba - and break them down into simple terms:

### State Channels

Picture state channels as private conversations between two people. They allow multiple exchanges without needing to check in with the main group (blockchain). It's quick and cheap, but it's just for two. So, it's not the best fit for applications needing more participants.

### Sidechains

Sidechains are like siblings to the main blockchain. They play nicely together, allowing devs to try out new things without disturbing the main chain. 

But like all siblings, they have their squabbles: they can be a bit risky security-wise, and transferring things between them and the main chain can be a bit slow and complicated.

### Plasma

Imagine Plasma as a family tree, creating child chains with their own rules and security. It's great for applications needing complex computations or lots of data. 

However, setting up this family tree can be complex, and the children may not be as secure and decentralized as the main chain.

### Rollups

Rollups are like express checkout lanes in a supermarket: they bundle transactions off-chain and then submit a single receipt to the main chain. 

Perfect for applications needing high scalability and low transaction fees. However, they may take longer to settle than other Layer-2 solutions, and there's a balance to strike between scalability and decentralization.

### Base and Boba

Base and Boba are the new kids on the block. They promise high scalability, speed, low transaction fees while maintaining decentralization and security.

Think of them as the latest high-tech cars - faster, more efficient, and packed with features. 

But keep in mind, they're still new and unproven compared to the other, more established brands.

And there you have it - a simple breakdown of some of the Layer-2 technologies!


-----------------------------------------------
# Cross-chain Interoperability with Mara

------------------------------------------------

Cross-chain interoperability refers to the ability for different blockchain networks to interact and communicate with each other. 

Traditionally, blockchains have operated in isolation, meaning that information and assets on one blockchain couldn't be directly accessed or transferred to another.

This isolation can limit the potential of blockchain technology, especially in scenarios where you want to leverage unique capabilities of different blockchains. 

For example, one blockchain might have a particularly effective smart contract capability, while another might be optimized for high-speed transactions.

With cross-chain interoperability, you can:

* **Transfer assets between different blockchains:** For example, a token created on Ethereum could be sent to a Binance Smart Chain wallet.

* **Execute transactions across chains:** A smart contract on one blockchain could trigger a transaction or another action on a different chain.

* **Read and use data from different blockchains:** A DApp (Decentralized Application) on one blockchain could retrieve and use data stored on another blockchain.


------------------------------------------------------

# Bridging assets between Ethereum and Mara

--------------------------------------------

Bridging assets between Ethereum and Layer 2 protocols such as Mara generally involves a bridge contract or a set of smart contracts on both chains.

A bridge is essentially a pathway that allows for the secure and verifiable transfer of tokens between two different blockchain networks.

Here's a high-level overview of how the process usually works:

* **Locking of Assets:** The process starts by locking up the assets on the Ethereum chain. You send the assets you want to transfer to a smart contract (the bridge) on Ethereum. This contract locks up the assets and emits an event or logs a note of your transaction.


* **Relaying the Information:** Once the assets are locked on Ethereum, the transaction information (including how much was sent, who sent it, and the destination address) needs to be communicated to the Layer 2 protocol. This is done by validators or relayers who monitor transactions on both networks.


* **Minting on Layer 2:** After the validators verify that the assets were indeed locked on Ethereum, the equivalent amount of tokens is minted or released on the Layer 2 protocol (in this case, MARA).

* **User Claims the Assets:** At this point, the user can claim or directly use the tokens on the Layer 2 blockchain.

* **Unlocking the Assets:** If the user wants to move back their assets to Ethereum, the reverse process is followed. The tokens on the Layer 2 are burned/locked, an event is emitted, the Ethereum bridge contract recognizes this event, and then unlocks the equivalent amount of assets on the Ethereum chain.


We'll now look a simplified token bridge contract deployed on Ethereum, and the `Transfer` contract deloyed on the Mara blockchain;

## 1. `Bridge Contract` on Ethereum;

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

contract BridgeBase {
    address public admin;
    mapping(address => uint) public amounts;

    event Transfer(
        address indexed from,
        uint amount,
        address to,
        uint date
    );

    constructor(address _admin) {
        admin = _admin;
    }

    function bridgeTokens(address to, uint amount) external {
        amounts[msg.sender] -= amount;
        emit Transfer(msg.sender, amount, to, block.timestamp);
    }

    function lockTokens(uint amount) external {
        amounts[msg.sender] += amount;
    }
}

```


This `BridgeBase` contract includes several key features and functions:

* **admin:** This is a public address variable that stores the address of the admin of this contract. 
The admin role could have special permissions, although in this specific code, the role isn't used for anything.

* **amounts:** This is a mapping that associates addresses with unsigned integer amounts. 
 
In the context of this bridge contract, it could be seen as a record of how many tokens each address has locked in the bridge.

* **Transfer event:** Events in Solidity allow the convenient usage of the EVM logging facilities, which in turn can be used to “call” JavaScript callbacks in the user interface of a dapp, which listen for these events. 

In this case, Transfer event is emitted when a successful bridge of tokens is made.

* **constructor:** The constructor is a special function that is executed during the creation of the contract and cannot be called afterwards. It is used to set the contract admin in this case.

* **bridgeTokens:** This function is used to move tokens to the bridge. It subtracts the bridged amount from the sender's balance (in the amounts mapping), and emits a Transfer event with details of the operation.

* **lockTokens:** This function is used to lock tokens in the bridge. It adds the locked amount to the sender's balance (in the amounts mapping).

We'll also include the `deploy.js` script for deploying our smart contract on Remix IDE;

```
// This script can be used to deploy the "Storage" contract using ethers.js library.
// Please make sure to compile "./contracts/1_Storage.sol" file before running this script.
// And use Right click -> "Run" from context menu of the file to run the script. Shortcut: Ctrl+Shift+S

import { deploy } from './ethers-lib'

(async () => {
    try {
        const result = await deploy('BridgeBase', [])
        console.log(`address: ${result.address}`)
    } catch (e) {
        console.log(e.message)
    }
  })()
```

So on our Remix IDE, we'll first compile our Smart Contract;

![compilesc](https://github.com/CyndieKamau/Docs/assets/63792575/673d30d0-993d-4a75-ad94-f37d77941aff)

You'll click on the `Compile BridgeBase.sol` button to compile the smart contract. When it's compiled successfully a green tick appears on the left-hand side of the Solidity Compiler as shown.

Once it compiles successfully we'll then deploy our smart contract using the `deploy_with_ethers.ts` script;

![deployethers](https://github.com/CyndieKamau/Docs/assets/63792575/baa168e6-cf7c-4495-b1de-f46cca66451f)


We can now deploy our smart contract. On the Ethereum icon we'll now setup our environment;

![options](https://github.com/CyndieKamau/Docs/assets/63792575/70b7c447-9f35-48cd-a8c4-e53561a12c81)

For the environment we'll choose the Remix VM (Virtual Machine) forked to the Ethereum Goerli testnet, to avoid gas fees.

The account address will update itself automatically since we are using the Remix VM.

Just like how the smallest unit of the dollar is the cent, and the smallest unit of bitcoin is the satoshi, the smallest unit of ether is the wei.

At the Address bar next to the Deploy button we'll then add our metamask wallet address connected to the Goerli testnet, to provide the parameter for deploying our smart contract.

![deploygoerli](https://github.com/CyndieKamau/Docs/assets/63792575/2c0a78b6-c645-40f3-a68f-bb0502731290)

It deploys successfully!! You can see the details below;

![hash](https://github.com/CyndieKamau/Docs/assets/63792575/661cedea-9128-49d9-aa02-20064b60f89f)

We can now deploy deploy the `Transfer` smart contract on Mara;

## 2. `Transfer` contract on Mara;

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

contract BridgeMara {
    address public admin;
    mapping(address => uint) public balances;

    event Mint(
        address indexed to,
        uint amount,
        uint date
    );

    constructor(address _admin) {
        admin = _admin;
    }

    // This function would be called when the `Transfer` event is detected on Ethereum
    function mintTokens(address to, uint amount) external {
        require(msg.sender == admin, "Only admin");
        balances[to] += amount;
        emit Mint(to, amount, block.timestamp);
    }

    // This is a simplified token transfer function within the Layer 2
    function transfer(address to, uint amount) external {
        require(balances[msg.sender] >= amount, "Not enough tokens");
        balances[msg.sender] -= amount;
        balances[to] += amount;
    }
}
```

This smart contract deployed on the Mara network will serve as the bridge's counterpart on that network. Let's break it down:

* ### **Variables and Constructor**

```
address public admin;
mapping(address => uint) public balances;

constructor(address _admin) {
    admin = _admin;
}

```
The contract declares two state variables: `admin`, which stores the address of the contract administrator, and `balances`, which is a mapping that tracks the balance of each address in this bridged asset. 

The constructor initializes the `admin` variable to the address passed as a parameter.

* ### **Mint Function**

```
event Mint(
    address indexed to,
    uint amount,
    uint date
);

function mintTokens(address to, uint amount) external {
    require(msg.sender == admin, "Only admin");
    balances[to] += amount;
    emit Mint(to, amount, block.timestamp);
}

```
The `mintTokens` function is what would be called when a `Transfer` event is detected on the Ethereum network. 

It mints new tokens on the Mara network to keep the total supply consistent across both networks. The `Mint` event is emitted each time new tokens are minted. 

It's important to note that only the contract's `admin` is allowed to call this function. 

This would typically be an address controlled by a trusted entity or a decentralized protocol that listens for `Transfer` events on the Ethereum network and calls `mintTokens` accordingly.

* ### **Transfer Function**

```
function transfer(address to, uint amount) external {
    require(balances[msg.sender] >= amount, "Not enough tokens");
    balances[msg.sender] -= amount;
    balances[to] += amount;
}

```

This `transfer` function allows users on the Mara network to transfer the bridged tokens among themselves. 

Before the transfer takes place, the function checks that the sender has enough tokens. 

If this check passes, the function subtracts the amount from the sender's balance and adds it to the recipient's balance.

We'll then follow the same procedure as the Ethereum smart contract. 

![maradeploy](https://github.com/CyndieKamau/Docs/assets/63792575/b756dcf6-1310-4d15-8b0a-05f9be629f0c)

You can see the transaction details below;

![deetshash](https://github.com/CyndieKamau/Docs/assets/63792575/fdf60e71-9907-4939-b8bc-3232919bc0d1)


These contracts will now work together to facilitate the transfer of assets between the two networks.

The smart contract on the Ethereum network will hold assets that are to be transferred to the Layer 2 protocol, which is Mara.

It will listen for transactions that signal a user's intention to move their assets to Mara.

The corresponding smart contract on the MARA network is capable of minting (creating) and burning (destroying) tokens. 

It listens for events from the Ethereum network (through a bridge, oracle or similar mechanism) and mints the appropriate amount of tokens whenever it receives a signal that assets have been locked on the Ethereum network. 

It does the reverse (burns tokens and signals for the Ethereum contract to unlock assets) when assets are moved back to the Ethereum network.








