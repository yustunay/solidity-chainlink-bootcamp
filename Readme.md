## Add Following Dependencies Using With Yarn

```json
  "dependencies": {
    "dotenv": "^16.0.3",
    "ethers": "^5.7.2",
    "fs-extra": "^10.1.0",
    "prettier": "^2.7.1",
    "prettier-plugin-solidity": "^1.0.0-beta.24",
    "solc": "0.8.7-fixed"
  }
```

```
yarn add dotenv ethers fs-extra prettier prettier-plugin-solidity solc
```

## Install all the dependencies in your project

```
$ npm install
or
$ yarn
```

### Compile script was created in package.json file (generates abi and binary files)

```json
  "scripts": {
    "compile": "yarn solcjs --bin --abi --include-path node_modules/ --base-path . -o . SimpleStorage.sol"
  }
```

## Compile project

```
$ yarn compile
```

## Run project

```
$ node deploy.js
```

## Create .env file and store parameters inside or you can set on demand as a run command

```
$ RPS_URL=http://0.0.0.0:8545 PRIVATE_KEY=PARAM_PRIVATE_KEY node deploy.js
```

## Encrypt Private Key

```
node encryptKey.js
```

### Sample Output

```json
{
  "address": "c3fc67454323e009c5bd3d57be5b7dd156a4f785",
  "id": "0abcc90b-2d1e-433e-ab04-fdef90be964e",
  "version": 3,
  "crypto": {
    "cipher": "aes-128-ctr",
    "cipherparams": {
      "iv": "6d2d5c5e9798ec73d9f9f32033b9bfa1"
    },
    "ciphertext": "b7760a627954dbfd09d66757d2ca503487ea80d66eaa84a8fbd95f3cf757060a",
    "kdf": "scrypt",
    "kdfparams": {
      "salt": "77df3aeed437cf7522914e1b44df0afa656a6c4b54374210a064b77789a407c8",
      "n": 131072,
      "dklen": 32,
      "p": 1,
      "r": 8
    },
    "mac": "6f42957c6d2aeadf27ccce5b31e7a43d69a9b89052e8662804d676d18795c79c"
  }
}
```

## Run with private key password

```
$ PRIVATE_KEY_PASSWORD=password node deploy.js
```

## Open Preview File of Readme In VSCode Editor

```
⌘ + ⇧ + V
```

## Open Command Pallette In VSCode Editor

```
⌘ + ⇧ + P
```

## Creating your own blockchain on local

- [Ganache](https://trufflesuite.com/ganache/)

## Some Web3 Testnet/Mainnets On Cloud

- [Alchemy](https://www.alchemy.com/)
- [Quicknode](https://www.quicknode.com/)
- [Infura](https://infura.io/)

## Add Auto Format In Open User Setting(JSON) - settings.json (Common Setting)

```json
{
  "hardhat.telemetry": true,
  "[solidity]": {
    "editor.defaultFormatter": "NomicFoundation.hardhat-solidity"
  },
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

## Format Files On Save

### Create a file named .prettierrc (Overrides common settings)

```json
{
  "tabWith": 4,
  "semi": false,
  "useTabs": false,
  "singleQuote": false
}
```

## Converting Javascript Files to Typescript (Uses private key from env file or as run parameter. Not encrypted one!)

- Change file type from js to js for deploy.js and encryptKey.js
- Change dependency definition from usage of require to import
- Install typescript and ts-node packages globally if not installed (npm install -g typescript ts-node)
- Add "type": "module" in package.json (for node command) OR add typescript and ts-node packages using with yarn (yarn add typescript ts-node)
- Add typescript version (yarn add @types/fs-extra)
- Set Environment variables as undefined with using ! at the end. (f.e. process.env.PRIVATE_KEY!)
- Run to deploy (ts-node deploy.ts AND ts-node encryptKey.ts)

## Web3 Frameworks

- Brownie
- Hardhat
- Foundry
- Anchor (Solana)

### Hardhat Development Environment

- Flexible JS based development environment to compilr, deploy, test and debug EVM based smart contracts
- Enables easy integration of code and external tools
- Local Hardhat network to simulate Ethereum
- Extensible plugin features
- High level of debugging features

## Links

- [etherscan.io](https://etherscan.io/)
- Open source developer platform - [gitpod.io](https://gitpod.io)
