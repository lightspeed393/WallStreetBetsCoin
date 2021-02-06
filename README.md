# WallStreetBets Coin (WSB)

A cryptocurrency coin made for the WallStreetBets community.

![WallStreetBets](/wsb.png)

## Technical Details

- Komodo's Antara Smartchain Technology
- Independent blockchain
- Block time : ~ 60 seconds
- Block generation: Proof of Work
- Mining algorithm: Equihash
- Block reward - 1 WSB
- Premine: 90,000,000,000 WSB
- Privacy: zk-SNARKS


## Features

Built using Komodo Platform tech, WSB is capable of doing all DeFi things one can possible do using Antara Smartchain's CryptoConditions.
- **Tokens Exchange**, can be used to create and trade tokens/NFTs. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/assets.html)
- **Dilithium** type transactions can make Quantum Resistant transactions. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/dilithium.html)
- **Decentralized Faucet**, to give away free WSB coins to people who wants to try things out on the chain. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/faucet.html)
- **Heir**, can help manage funds in a way that it can be passed on to heir for inheridence. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/heir.html)
- **Oracles**, to link real world data to blockchain based decentralised applications. Oracles are what powers DeFi. It is very powerful technology. And it works already available to Antara Smartchains. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/oracles.html)
- **Pegs**, to make decentralised stablecoins or making pegged cryptocurrencies to other kind of assets in financial world. [Link](https://developers.komodoplatform.com/basic-docs/antara/antara-api/pegs.html)


## Resources

#### Explorer
- [wsb.explorer.dexstats.info](http://wsb.explorer.dexstats.info/)

#### Wallets
- [AtomicDEX-Desktop](https://github.com/KomodoPlatform/atomicDEX-Desktop/releases)
- [Command Line](#Using-Command-Line)

#### WSB Coin Community
- [#wsb channel on Komodo Discord](https://discord.gg/JcNqhUxAxh)
- [@CoinWSB on Twitter](https://twitter.com/CoinWsb)

#### Mining Pools
- [mining.spaceworks.co](https://mining.spaceworks.co)
- [chickenpool.com](http://chickenpool.com)

#### Exchanges
- [AtomicDEX-Desktop](https://github.com/KomodoPlatform/atomicDEX-Desktop/releases)

#### Faucets
- [AtomicExplorer](https://www.atomicexplorer.com/#/faucet/wsb)
- [On-chain Faucet](https://developers.komodoplatform.com/basic-docs/antara/antara-api/faucet.html)


## Komodo Airdrop

All Komodo holders were airdropped WSB 100:1 from the premine. If you have an address with KMD in it, you now own WSB in the same address but on the WallStreetBets blockchain.


### Using Command Line
Download pre-compiled komodo binaries for your operating system from [here](https://github.com/KomodoPlatform/komodo/releases/tag/0.6.1).
Extract the binaries, and execute "fetch-params" script from command line terminal to fetch the required chain params.

#### Launch WSB Blockchain
Use the following command to launch WSB coin's blockchain daemon:

```bash
./komodod -ac_name=WSB -ac_supply=90000000000 -ac_cc=3 -ac_reward=100000000 -addnode=94.130.38.173 -addnode=178.63.47.105
```

#### Mine WSB blockchain
Use "-gen" and "-genproclimit" to enable mining. Value for "-genproclimit" is the value of how many CPU threads you have on your system.

```bash
./komodod -ac_name=WSB -ac_supply=90000000000 -ac_cc=3 -ac_reward=100000000 -addnode=94.130.38.173 -addnode=178.63.47.105 -gen -genproclimit=4
```

#### Wallet comands

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
