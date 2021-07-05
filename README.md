# Go with the Flow

Set of go scripts to make it easer to run a Story consisting of creating accounts, deploying contracts, executing transactions and running scripts on the Flow Blockchain.

Feel free to ask questions to @bjartek in the Flow Discord.

v2 of GoWithTheFlow removed a lot of the code in favor of `flowkit` in the flow-cli. Some of the code from here was
contributed by me into flow-cli like the goroutine based event fetcher.

Breaking changes between v1 and v2:
 - Multisign is currently not supported in v2
 - the SignProposeAndPayAsService() method is removed since the concept of a serviceAccount is not really there anymore. Replace with using the `emulator-account` account manually
 - v1 had a config section for discord webhooks. That has been removed since the flow-cli will remove extra config things in flow.json. Store the webhook url in an env variable and use it as argument when creating the DiscordWebhook struct.

Special thanks to @sideninja for helping me get my changes into flow-cli.

## How to configure devnet
Create a ~/.flow.json file and specify testnet accounts and addresses

## How to write contracts
Put contracts in the contract folder and name the file the same as the contract.

## Examples

In order to run the demo example you only have to run `make` in the example folder of this project. 
The emulator will be run in memory. 

If you want to have a standalone emulator to get logs as then the `examples/script/main.go` file can be run while running
and emulator

## Credits

This project is a rewrite of https://github.com/versus-flow/go-flow-tooling 
