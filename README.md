[![Automatic Releaser](https://github.com/vultr/vultr-node/actions/workflows/release.yml/badge.svg?branch=master)](https://github.com/vultr/vultr-node/actions/workflows/release.yml)
[![Code Coverage test](https://github.com/vultr/vultr-node/actions/workflows/coverage.yml/badge.svg)](https://github.com/vultr/vultr-node/actions/workflows/coverage.yml)
[![npm version](https://badge.fury.io/js/%40vultr%2Fvultr-node.svg)](https://badge.fury.io/js/%40vultr%2Fvultr-node)
[![license](https://img.shields.io/github/license/vultr/vultr-node)](https://github.com/vultr/vultr-node/blob/master/LICENSE.md)

# cryptfire-node

Official Cryptfire client node module. We now run our own high-performance, well-structured, Open Source NodeJS API and provide Cloud infrastructure for KVM Servers on 6 geographically distributed Bare Metal Nodes. We also rent out Bare Metal Nodes from Colocations around the world.

## Installation

```sh
npm install @cryptfire/cryptfire-node
```

## Usage

An API Key can be generated and acquired with curl, or the Cryptfire CLI.

### Initialize

```js
const cryptfireNode = require('@cryptfire/cryptfire-node')

// Initialize the instance with your configuration
const cryptfire = cryptfireNode.initialize();

// export this as CRYPTFIRE_API_KEY to .bashrc
cryptfire.account.registerAccount().then((response) =>
  console.log(apiKey);
);
```

### Calling Endpoints

```js
// Get Account Info
cryptfire.account.getAccountInfo().then((response) => {
  console.log(response)
})

// Get Ethereum Wallet
cryptfire.funding.getECryptoWallets().then((response) => {
  console.log(response)
})

// Deploy a minimal cloud server
cryptfire.cloud.deployMinimalInstance().then((response) => {
  console.log(response)
})
```

## Documentation

This implements Cryptfire API V1. For documentation on all endpoints, please visit https://docs.cryptfire.io/api/. 

For documentation specific to this client please visit the Github wiki.

## Contributing

Feel free to send pull requests our way! Please see the [contributing guidelines](CONTRIBUTING.md).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

## Cryptfire Authors

- [**z**](https://github.com/zdanl)

## Vultr Authors

- [**Spencer Kordecki**](https://github.com/spencerkordecki)
- [**Fady Farid**](https://github.com/afady)
- [**Glenn Dobson**](https://github.com/afatalerrror)
