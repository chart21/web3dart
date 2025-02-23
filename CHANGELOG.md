# Changelog

## 1.1.0
- Added `getTransactionReceipt` to get more detailed information about a
transaction, including whether it was executed successfully or not.

## 1.0.0
Basically a complete rewrite of the library - countless bug fixes, a more fluent
and consistent api and more features:
- experimental api to perform expensive operations in a background isolate. Set
`enableBackgroundIsolate` to true when creating a `Web3Client` to try it out.
- Events! Use `addedBlocks`, `pendingTransactions` and `events` for auto-updating
streams.
- The client now has a `dispose()` method which should be called to stop the 
background isolate and terminate all running streams.

This version contains breaking changes! Here is an overview listing some of them.

| Before        | Updated API  |
| :------------- | -----:|
| Creating credentials via `Credentials.fromPrivateKeyHex`   | Use the `EthPrivateKey` class or, even better, `client.credentialsFromPrivateKey` |
| Sending transactions or calling contract functions | The api has been changed to just a single methods instead of a transaction builder. See the examples for details. |
| Low-level cryptographic operations like signing, hashing and converting hex <-> byte array <-> integer  | Not available in the core library. Import `package:web3dart/crypto.dart` instead |

If you run into problems after updating, please [create an issue](https://github.com/simolus3/web3dart/issues/new).

## 0.4.4
 - Added `getTransactionByHash` method - thank you, [maxholman](https://github.com/maxholman)!
 - Allow a different N parameter for scrypt when creating new wallets.

## 0.4.0
 - New APIs allowing for a simpler access to wallets, credentials and addresses
 - More examples in the README

## 0.2.1
- More solidity types, not with encoding.

## 0.2
- Send transactions and call messages from smart contracts on the
  Blockchain.

## 0.1
- Create new Ethereum accounts

## 0.0.2
- Send and sign transactions

## 0.0.1

- Initial version, created by Stagehand
