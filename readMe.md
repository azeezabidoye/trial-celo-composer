# Celo composer: Create a new customized dApp on the Celo blockchain.

## Azeez Abidoye ✍

_Step-by-step tutorials for creating a new custom dApp with Celo Composer._

## Hello Devs!

We'll break down a blockchain topic into bite-sized pieces in today's post to make it easier for you to study and put your new knowledge to use.

We'll learn how to use the Celo composer to develop and launch new dApps.

### Here is a list of what we have to cover ⌛

- Install Celo composer CLI
- Setup a new dApp
- Develop new project
- Setup and configure Metamask (optional)
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

If you have the Celo composer npm package installed on your computer. Developing new dApps with your preferred frontend framework becomes a snap.

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

If you already have Metamask installed on your browser, feel free to skip this section.

### Visit Metamask URL

Visit
[metamask.io](https://metamask.io)

- Select download

- Select Install Metamask for Chrome

- Click Add to Chrome to add Metamask extension

- Agree with Metamask Private Policy

- Select Create a wallet to create a new Metamask wallet

- Agree with the term of use

- Secret Recovery Phrase
  ⚠ This is the main key to recover your Metamask account. Keep it confidential.

- Confirm your Recovery Phrase. Insert the phrase in order and click Confirm

🔥 Boom! Your Metamask extension is successfully setup.

### Connect to a testnet

- Click the network dropdown at the top right corner of Metamask

- Select _show/hide network_

- Turn **ON** Show Test Network option

- Close Metamask settings page

### Connect Celo Testnet to Metamask

- Visit [chainlist.org](https://chainlist.org/)

- Switch **Testnets** on

- Search for _alfajores_ in the search bar

- Select Add to Metamask

- Click on Approve to enable Metamask connection

- Select Switch network

🎉Celo Alfajores test network has successfully been added to your Metamask testnets.

## Step 5: Fund your testnet wallet

Get funds from
[Celo faucet](https://celo.org/developers/faucet)

### Receive additional fund

- Copy your account address to [Celo faucet](https://celo.org/developers/faucet)

- Paste your Celo Alfajores wallet address

- Select I'm not a robot

- Get started

✅ Your account will get credited with 1 CELO native token.

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

```bash
    PRIVATE_KEY="242a32639923e6292c2d92fcd10853809e9246850b0ee6b2680f6232122b435a"
```

### Create your Smart contract file

- Navigate to `/packages/hardhat/contracts`

- Create a new file named `/Messanger.sol`

- Open `/packages/hardhat/contracts/Greeters.sol` and copy all the code therein

- Paste the code in `/Messanger.sol`

- Refactor the code

### Write your deploy script

- Open `/packages/hardhat/deploy/00-deploy.js`

- Add deployer script like the Greeter contract

- Include new contract in `module.exports` array

## Step 7: Deploy your Smart contract

- Open your terminal and navigate to `/packages/hardhat`

- Run `yarn install` to install project dependencies

- Run `yarn deploy` to compile and deploy contracts

### Check your balance

Open Metamask and check your wallet to see your balance, you will notice that you now have less CELO token. This is due to the gas cost of deploying your Smart contracts to the blockchain.

### Verify Smart contract

To verify your smart contract, go to [Celo Block Explorer](https://explorer.celo.org). Anyone can view your contract and engage with its functions using the Celo Block Explorer.

- Visit [www.explorer.celo.org](https://explorer.celo.org)

- Select Celo Alfajores testnet from the network dropdown in the navigation

- Paste your wallet address in the search bar

- Select the loaded account to view your transactions

### View the Smart contract ABI

Finally, you may view the ABI for your Smart contract in `/deployments/alfajores/Messanger.json`
The ABI is the interface that allows you to access your Smart contract functions from the front-end of your dApp

## Step 8: Interact with your dApp

### Start the front-end

- Open your terminal and navigate to `/packages/react-app`

- Run `yarn install` to install the front-end dependencies

- Run `yarn dev` to start your development environment

- Visit [http://localhost:3000](http://localhost:3000) to view your project

### Test Smart contract

- Select the new contract in the navigation

- Open **writeMessage** function

- Input value and **transact**

- Authorize Metamask

- Verify contract using [Celo block explorer](https://explorer.celo.org)

## Congratulations! 🎉

This concludes the discussion of Creating a new customized dApp on Celo blockchain using Celo composer. You can go over each of the topics we discussed below to make sure you're ready to put your new skills to use.

### Here is a list of what we have covered ⌛

- ✅ Install Celo composer CLI
- ✅ Setup a new dApp
- ✅ Develop new project
- ✅ Setup and configure Metamask (optional)
- ✅ Fund your testnet wallet
- ✅ Develop the Smart contract
- ✅ Deploy Smart contract
- ✅ Interact with your dApp

### Contribute to the project​

Celo welcomes contributions to the repository! If you decide to try this out and find something confusing, consider opening a pull request to make things more clear for the next developer. If you improve the user interface or create new components that you think might be useful for other developers, consider opening a PR.
