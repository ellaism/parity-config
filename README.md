# Ellaism

Ellaism is an Ethereum-like network with no pre-mine and no contentious hard forks. Additional features are:

* Monetary policy. A reduction of 20% mining rewards happens every 10 million blocks. The total number of coins will be around 280 million Ella.
* No difficulty bomb.
* Replay protection enabled by default.

## Installation

Install [Parity](https://github.com/paritytech/parity/releases) from Parity's official website. Download the [Ellaism config file](https://raw.githubusercontent.com/ellaism/parity-config/master/ellaism.json). Run Parity with `parity --chain ellaism.json`.

If you're running Parity for a mining pool, it is recommended to run with `--usd-per-tx 0` because Parity cannot calculate the correct ELLA-USD rate.

```
parity --chain "/path/to/ellaism.json" --usd-per-tx 0
```

To set it in your Parity config file, add the following:

```
[mining]
usd_per_tx = "0"
```

## Windows Mining Instruction

Install [Parity](https://github.com/paritytech/parity/releases) from Parity's official website. After installation, please first close the auto-started Parity from the system tray.

Download the [zipped files](https://github.com/ellaism/parity-config/archive/master.zip) of this repository. Unpack it. Start `start-parity.bat`. Go to `http://localhost:8180` and follow the instructions to create a new account. Remember your account address. Close Parity. Edit `start-parity.bat`, Change the address after `--author` to the account address you've just created. Start `start-partiy.bat` to open Parity again.

Download [ethminer](https://github.com/ethereum-mining/ethminer/releases). Unpack `ethminer.exe` to the same folder as the above zipped file. Start `start-miner.bat`.

## Basic Information

* Coin generation: 5 Ella per block with 20% reward reduction happens every 10 million blocks. Block time is 10 seconds.
* The total number of coins will be around 280 million Ella.
* Network ID and chain ID is 0x40.
* Most other parameters are the same as Ethereum.
