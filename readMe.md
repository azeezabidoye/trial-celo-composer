# Celo composer: Create a new customized dApp on the Celo blockchain.

## Azeez Abidoye ✍

_Step-by-step tutorials for creating a new custom dApp with Celo Composer._

## Hello Dev!

We'll break down a blockchain topic into bite-sized pieces in today's post to make it easier for you to study and put your new knowledge to use.

We'll learn how to use the Celo composer to develop and launch new dApps.

### Here is a list of what we have to cover ⌛

- Install Celo composer CLI
- Setup a new dApp
- Develop new project
- Setup and configure Metamask
- Fund your testnet wallet
- Develop the Smart contract
- Deploy Smart contract
- Interact with your dApp

By the end of this post, you’ll be able to create, deploy, interact with, and host your new Dapp using Celo Composer.

Let’s go! 🚀

## Step 1: Install Celo composer CLI

Open your terminal to install Celo composer CLI globally on your computer. This allows you to quickly create new dApps using Celo composer!

Run `npm install @celo/celo-composer -g`

### TIP:

You can view the list of NPM Packages that are globally installed.

Run `npm list -g`

If you have the celo composer npm package installed on your computer. Developing new dApps with your preferred frontend framework becomes a snap.

## Step 2: Setup a new dApp

### Navigate to your project folder

`cd project-folder-example`

### Create a new Celo composer project

`npx @celo/celo-composer create`

### Select your desired frontend framework

➡ **React** (with examples, requires hardhat deploy) is the default. In my case I will select the default.

### Choose Smart contract framework

➡ **Hardhat** (default)

### Create a Sub-graph

➡ **No** (default)

### Insert the project name

➡ custom_celo_dapp

You may always use the processes outlined above to create a new dApp that is deployable on the Celo blockchain and any other network of your choice. 🎉

### TIP:

A new dApp may be set up in just six steps using the chosen frameworks. This makes the project less bulky. No further frameworks will be set up. Both frameworks can be found in the `/package` directory.

## Step 3: Develop new project

Navigate to the new project directory
`cd custom_celo_dapp`

Launch your code editor
`code .`

## Step 4: Setup and configure Metamask

If you already have Metamask installed on your browser, you can skip this section.

### Visit Metamask URL

Visit metamask.io
[Metamask](https://metamask.io)

- Select download

- Select Install Metamask for Chrome

- Click Add to Chrome to add Metamask extension

- Agree with Metamask Private Policy

## Step 5: Fund your testnet wallet

Get funds from Celo faucet
[Celo faucet](https://celo.org/developers/faucet)

### Receive additional fund

- Paste your Celo Alfajores wallet address

- Select I'm not a robot

- Get started

Your account will get credited with 1 CELO native token.

## Step 6: Develop the Smart contract

### Connect your wallet to the Smart contract

- Open [Metamask](https://metamask.io)

- Click on the three-dots at the top right corner

- Select account details

- Select export private key to reveal private key

- Copy the private key and click done to close account setting

- Navigate to `/packages/hardhat/`

- Rename `/packages/hardhat/.envexample` to `/packages/hardhat/.env`

- Paste your private key as a value of PRIVATE_KEY

### Create your Smart contract file

- Navigate to `/packages/hardhat/contracts`

- Create a new file named `/Messanger.sol`

- Open `/packages/hardhat/contracts/Greeters.sol` and copy all the code therein

- Paste the code in `/Messanger.sol`

- Rafactor the code

### Write your deploy script

- Open `/packages/hardhat/deploy/00-deploy.js`

- Add deployer script like the Greeter contract

- Include new contract in `module.exports` array
