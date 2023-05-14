
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









-----------------------------------------------







------------------------------------------------
SECTION 2
--------------------------------------

# Understanding Mara's Layer-2 Blockchain
> Layer 2 is a secondary blockchain network that operates on top of the primary blockchain (Layer 1) to enhance its scalability, security, and speed. It reduces the burden on the main chain by offloading some of the transaction processing to a separate layer, thus increasing the network's overall capacity and efficiency.

## Benefits of using Layer-2 solutions

* **Scalability:** Layer 2 solutions can significantly increase the scalability of blockchain networks by processing a large number of transactions off-chain. This can reduce the load on the main blockchain, leading to faster transaction processing times and increased network throughput.
* **Cost-effectiveness:** Layer 2 solutions can reduce the cost of transactions on the blockchain by minimizing the number of transactions that need to be processed on the main chain. This can lead to lower fees for users and make the blockchain more accessible to a wider range of people.
* **Improved user experience:** By reducing the time and cost of transactions, Layer 2 solutions can improve the overall user experience of interacting with blockchain networks. This can lead to increased adoption and usage of blockchain-based applications.
* **Increased security:** Layer 2 solutions can enhance the security of blockchain networks by reducing the number of transactions that are processed on the main chain, thus reducing the risk of network congestion and potential attacks. Additionally, Layer 2 solutions can implement additional security measures, such as multi-party computation and zero-knowledge proofs.
* **Flexibility:** Layer 2 solutions can provide greater flexibility to blockchain networks, allowing them to support a wider range of use cases and applications. This can lead to greater innovation and development within the blockchain ecosystem.

## Comparison with other Layer-2 technologies

> There are various Layer-2 technologies available in the market, including state channels, sidechains, plasma, rollups, and more recently, Base and Boba. Here's how Base and Boba compare to some of the other Layer-2 technologies:

1. **State Channels** 
     - State channels are off-chain channels between two parties that enable them to conduct multiple transactions without requiring the main blockchain's intervention. They are best suited for high-frequency, low-value transactions, such as micropayments. While state channels provide instant settlement and low fees, they are limited to only two parties, making them less suitable for applications that require multiple parties.
2. **Sidechains** 
    -  Sidechains are independent blockchains that are interoperable with the main blockchain. They allow developers to experiment with new features and functionalities without affecting the main chain's security and performance. However, sidechains are still susceptible to security risks, and transferring assets between sidechains and the main chain can be complex and slow.

3. **Plasma** 
    - Plasma is a Layer-2 scaling solution that enables the creation of child chains, each with their own set of rules and security measures. Plasma is best suited for applications that require complex computations or large amounts of data. However, the setup process for Plasma can be complex, and the child chains may not have the same level of security and decentralization as the main chain.

4. **Rollups** 
    - Rollups are Layer-2 solutions that batch transactions off-chain and then submit a single transaction to the main chain. Rollups are best suited for applications that require high scalability and low transaction fees. However, rollups can have longer settlement times than other Layer-2 solutions, and there may be a tradeoff between scalability and decentralization.

5. **Base and Boba**
    - Base and Boba are more recent Layer-2 solutions that aim to provide high scalability, low latency, and low transaction fees while maintaining decentralization and security. Base uses a novel consensus mechanism called Proof of State, while Boba uses a variant of the Proof of Stake consensus mechanism. Both solutions aim to provide faster transaction processing times, lower fees, and greater flexibility compared to other Layer-2 solutions. However, they are still relatively new and untested compared to some of the more established Layer-2 technologies.
