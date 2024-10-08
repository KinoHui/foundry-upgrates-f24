# Foundry UUPS Upgradeable Contracts

Welcome to this section of the Cyfrin Foundry Solidity Course!

*[⭐️ (4:47:00) | Lesson 13: Foundry Upgradeable Contracts](https://www.youtube.com/watch?v=wUjYK5gwNZs&t=17220s)*

> **Note**: This is for demonstration purposes only. Upgradeable contracts can be tricky, and they’re generally best to avoid unless you really know what you’re doing.

## Table of Contents

- [Foundry UUPS Upgradeable Contracts](#foundry-uups-upgradeable-contracts)
- [Getting Started](#getting-started)
  - [Requirements](#requirements)
  - [Quickstart](#quickstart)
    - [Optional Gitpod](#optional-gitpod)
- [Usage](#usage)
  - [Start a Local Node](#start-a-local-node)
  - [Deploy](#deploy)
  - [Deploy - Other Network](#deploy---other-network)
  - [Testing](#testing)
    - [Test Coverage](#test-coverage)
- [Deployment to a Testnet or Mainnet](#deployment-to-a-testnet-or-mainnet)
  - [Estimate Gas](#estimate-gas)
- [Formatting](#formatting)
- [Thank You!](#thank-you)

## Getting Started

### Requirements

- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  - You’ll know you’ve done it right if you run `git --version` and see a response like `git version x.x.x`.
- [Foundry](https://getfoundry.sh/)
  - You’ll know you’re good to go if you run `forge --version` and see something like `forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)`.

### Quickstart

To get started, open up your terminal and run:

```bash
git clone https://github.com/Cyfrin/foundry-upgrades-cu
cd foundry-upgrades-cu
forge build
```

#### Optional Gitpod

If you prefer not to install and run everything locally, you can easily work with this repo in Gitpod. This way, you can skip the cloning part!

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#github.com/Cyfrin/foundry-upgrades-cu)

## Usage

### Start a Local Node

To start your local node, simply run:

```bash
make anvil
```

### Deploy

Deploying will default to your local node, so make sure it’s running in another terminal for the deployment to work.

```bash
make deploy
```

### Deploy - Other Network

For deploying to other networks, check out the [Deployment to a Testnet or Mainnet](#deployment-to-a-testnet-or-mainnet) section below.

### Testing

To run tests, use:

```bash
forge test
```

#### Test Coverage

To check your test coverage, run:

```bash
forge coverage
```

For coverage-based testing, you can use:

```bash
forge coverage --report debug
```

## Deployment to a Testnet or Mainnet

1. **Setup Environment Variables**

   You’ll need to set your `SEPOLIA_RPC_URL` and `PRIVATE_KEY` as environment variables. You can add them to a `.env` file, similar to how it’s done in `.env.example`.

   - `PRIVATE_KEY`: This is your account's private key (like the one from [Metamask](https://metamask.io/)). **NOTE:** For development purposes, please use a key that doesn’t have any real funds associated with it.
     - [Learn how to export it here](https://metamask.zendesk.com/hc/en-us/articles/360015289632-How-to-Export-an-Account-Private-Key).
   - `SEPOLIA_RPC_URL`: This is the URL of the Goerli testnet node you’ll be working with. You can get one for free from [Alchemy](https://alchemy.com/?a=673c802981).

   Optionally, you can add your `ETHERSCAN_API_KEY` if you want to verify your contract on [Etherscan](https://etherscan.io/).

2. **Get Testnet ETH**

   Head over to [faucets.chain.link](https://faucets.chain.link/) and grab some testnet ETH. You should see it show up in your Metamask wallet.

3. **Deploy**

   To deploy to the Sepolia network, run:

   ```bash
   make deploy ARGS="--network sepolia"
   ```

### Estimate Gas

If you want to estimate how much gas your transactions will cost, you can run:

```bash
forge snapshot
```

This will generate an output file called `.gas-snapshot`, which you can review for insights.

## Formatting

To ensure your code is neatly formatted, run:

```bash
forge fmt
```

This will help keep your code clean and consistent!

## Thank You!
