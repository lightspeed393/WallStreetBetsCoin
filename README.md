## Welcome to WallStreetBets Coin (WSB)

Here is a community built cryptocurrency coin made for WallStreetBets fans. Following are the details:

- Built using Komodo's Antara Smartchain technology
- Independent blockchain
- Block time aprox 60 seconds.
- Blocks are mined with Proof of Work (Equihash)
- Block reward is 1 WSB
- Premine supply of 90,000,000,000 WSB
- Premine airdropped to KMD holders 100:1

# Features

Coming from Komodo Platform, it is capable of doing all DeFi things one can possible do using Antara Smartchain's CryptoConditions technology.
- **Tokens Exchange**, which can be used to create and trade NFTs. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/assets.html)
- **Dilithium** type transactions can make Quantum Resistant transactions [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/dilithium.html)
- **Decentralised Faucet**, to give away free WSB coins to people who wants to try things out on this chain. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/faucet.html)
- **Heir**, can help manage funds in a way that it can be passed on to heir for inheridence. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/heir.html)
- **Oracles**, to link real world data to blockchain based decentralised applications. Oracles are what powers DeFi. It is very powerful technology. And it works already available to Antara Smartchains. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/oracles.html)
- **Pegs**, to make decentralised stablecoins or making pegged cryptocurrencies to other kind of assets in financial world. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/pegs.html)


# Getting Started for command line
Download pre-compiled komodo binaries for your operating system from [here](https://github.com/KomodoPlatform/komodo/releases/tag/0.6.1).
Extract the binaries, and execute "fetch-params" script from command line terminal to fetch the required chain params.

# Connect with WSB Blockchain
Use the following command to connect to WSB chain's network:

```bash
./komodod -ac_name=WSB -ac_supply=90000000000 -ac_cc=3 -ac_reward=100000000 -addnode=94.130.38.173 -addnode=178.63.47.105
```

# Mine WSB blockchain
Use "-gen" and "-genproclimit" to enable mining. Value for "-genproclimit" is the value of how many CPU threads you have on your system.

```bash
./komodod -ac_name=WSB -ac_supply=90000000000 -ac_cc=3 -ac_reward=100000000 -addnode=94.130.38.173 -addnode=178.63.47.105 -gen -genproclimit=4
```

# Wallet comands

```bash
# Get wallet and blockchain info
./komodo-cli -ac_name=WSB getinfo


# Get wallet information
./komodo-cli -ac_name=WSB getwalletinfo


# Get mining information
./komodo-cli -ac_name=WSB getmininginfo


# Generate a new Public address
./komodo-cli -ac_name=WSB getnewaddress


# To backup the private key of a public address
./komodo-cli -ac_name=WSB dumpprivkey


# To import private key of public address
./komodo-cli -ac_name=WSB importprivkey "PRIVATE_KEY_STRING_FROM_DUMPPRIVKEY_COMMAND"


# Generate a new Z/Private address
./komodo-cli -ac_name=WSB z_getnewaddress


# To backup the private key of a z address
./komodo-cli -ac_name=WSB z_exportkey "zaddr"


# To mine with CPU and enable staking
./komodo-cli -ac_name=WSB setgenerate true 0

# To only stake and not CPU mining
./komodo-cli -ac_name=WSB setgenerate false 0

# To disable staking and disable CPU mining
./komodo-cli -ac_name=WSB setgenerate false 1


# To send mined coins to a z address
./komodo-cli -ac_name=WSB "fromaddress" "tozaddress" ( fee ) ( limit )

# Example 1:
./komodo-cli -ac_name=WSB z_shieldcoinbase "FROM_YOUR_ADDRESS" "TO_Z_ADDRESS"

# Example 2:
./komodo-cli -ac_name=WSB z_shieldcoinbase "*" "TO_Z_ADDRESS"


# To send a transaction from your z address to another z address
./komodo-cli -ac_name=WSB z_sendmany "fromaddress" [{"address":... ,"amount":...},...] ( minconf ) ( fee )

# Example:
komodo-cli -ac_name=WSB z_sendmany "FROM_Z_ADDRESS" '[{"address": "TO_Z_ADDRESS" ,"amount": 5.9999}]'
```

## WSB Halving detaiils
The detailed halving estimation sheet can be accessed from here:
[https://docs.google.com/spreadsheets/d/1ItLK8xtTjzSyYRgonMKvT1RZQ4lsl1ebnRIFcydVVsQ](https://docs.google.com/spreadsheets/d/1ItLK8xtTjzSyYRgonMKvT1RZQ4lsl1ebnRIFcydVVsQ)

## Help/Support Guides
TODO

## Explorer
[http://wsb.explorer.dexstats.info/](http://wsb.explorer.dexstats.info/)

## Wallets
TODO

## Connect with WSB community
TODO

## Mining Pools
[https://mining.spaceworks.co](https://mining.spaceworks.co)

## Trading Exchanges
[AtomicDEX-Desktop](https://github.com/KomodoPlatform/atomicDEX-Desktop/releases)
