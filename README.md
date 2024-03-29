<!-- <h1 align="center">Aleo Workshop</h1> -->
<img alt="workshop" width="1412" src="./.resources/readme.png">
<h3 align="center">📜 A starter guide to build applications on Aleo 📜</h3>

<p align="center">
    <a href="https://twitter.com/AleoHQ"><img src="https://img.shields.io/twitter/url/https/twitter.com/AleoHQ.svg?style=social&label=Follow%20%40AleoHQ"></a>
    <a href="https://aleo.org/discord"><img src="https://img.shields.io/discord/700454073459015690?logo=discord"/></a>
</p>

## Table of Contents
- [Build Guide](#build-guide)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
- [IDE Support](#ide-support)
    - [VSCode](#vscode-preferred)
    - [Sublime Text](#sublime-text)
    - [IntelliJ IDEA](#intellij-idea)
- [Deploy Program](#deploy-program)
    - [Command](#command)
    - [Result](#Result)
- [ARC20](#arc20)
## Build Guide

The following steps will install Aleo and Leo on your machine. This workshop is compatible on macOS, Linux, and Windows machines.

### Prerequisites

This workshop requires the following prerequisites.
1.  [Install Git](https://git-scm.com/downloads)
2.  [Install Rust](https://www.rust-lang.org/tools/install)
3.  [Install Leo](https://developer.aleo.org/leo/installation)
4.  [Install snarkos](https://developer.aleo.org/testnet/getting_started/installation/)

	For Windows: [snasrkOS releases](https://github.com/AleoHQ/snarkOS/releases) Using unzip and run with cmd/pw.
    Note: Can export enviroment to path.
    
5.  [Install Leo Wallet](https://leo.app/)
6.  [Install VSCode](https://code.visualstudio.com/download)


## Aleo Testnet

[greenlist](https://faucetgreenlist.snarkos.net/) Make address valid.

[Aleo Discord](https://discord.com/invite/aleohq) Using faucet to get Aleo.

`/sendcredits {WalletAddress} 15`

### Installation

To install Aleo and Leo, run:
```
./install.sh
```

## IDE Support

This workshop requires one of the following IDEs.
- [VSCode](https://bit.ly/start-vscode)
- [Sublime Text](https://bit.ly/start-sublime)
- [IntelliJ IDEA](https://bit.ly/start-intellij)

### VSCode (Preferred)

Start by installing `VSCode` with [bit.ly/start-vscode](https://bit.ly/start-vscode).

#### Next, in VSCode, open the **VSCode Marketplace**, type **Leo** into the search bar, and proceed to install the Leo plugin.
![Leo VSCode](./.resources/leo-vscode.png)

### Sublime Text

<details><summary>Installation Steps</summary>

Start by installing `Sublime Text` with [bit.ly/start-sublime](https://bit.ly/start-sublime).

#### Next, in Sublime Text, install [Package Control](https://packagecontrol.io):
- On Windows/Linux: `ctrl + shift + p`, type **Install Package Control**, and press **Enter**.
- On macOS: `cmd + shift + p`, type **Install Package Control**, and press **Enter**.

#### Next, in Sublime Text, install [LSP](https://packagecontrol.io/packages/LSP):
- On Windows/Linux: `ctrl + shift + p`, select **Package Control: Install Package**, type **LSP**, and press **Enter**.
- On macOS: `cmd + shift + p`, select **Package Control: Install Package**, type **LSP**, and press **Enter**.

#### Lastly, in Sublime Text, install [LSP-leo](https://packagecontrol.io/packages/LSP-leo):
- On Windows/Linux: `ctrl + shift + p`, select **Package Control: Install Package**, type **LSP-leo**, and press **Enter**.
- On macOS: `cmd + shift + p`, select **Package Control: Install Package**, type **LSP-leo**, and press **Enter**.

</details>

### IntelliJ IDEA

<details><summary>Installation Steps</summary>

Start by installing `IntelliJ IDEA` with [bit.ly/start-intellij](https://bit.ly/start-intellij).

#### Next, in IntelliJ IDEA, open the **IntelliJ Marketplace** and select `Plugins`:
- On Windows/Linux: `ctrl + ,` and select `Plugins` on the left hand bar
- On macOS: `cmd + ,` and select `Plugins` on the left hand bar

Lastly, type **Leo** into the search bar, and install the official Leo plugin.

</details>

## Deploy Program

### Command (no fee)
For Macos/ Linux:
```
PRIVATEKEY="${PRIVATEKEY}"
APPNAME="<project_name>"

snarkos developer deploy "${APPNAME}.aleo" --private-key "${PRIVATEKEY}" --query "https://api.explorer.aleo.org/v1" --path "./${APPNAME}/build/" --broadcast "https://api.explorer.aleo.org/v1/testnet3/transaction/broadcast" --priority-fee 0

```

For Windows (Using direct .exe file):
```
.\snarkos developer deploy "${APPNAME}.aleo" --private-key "${PRIVATEKEY}" --query "https://api.explorer.aleo.org/v1" --path "./${APPNAME}/build/" --broadcast "https://api.explorer.aleo.org/v1/testnet3/transaction/broadcast" --priority-fee 0
```

### Result
Result (demo):
![](./.resources/deployToken.png)

### Command
For Macos/ Linux:
```
PRIVATEKEY="${PRIVATEKEY}"
APPNAME="<project_name>"
RECORD=""
snarkos developer deploy "${APPNAME}.aleo" --private-key "${PRIVATEKEY}" --query "https://api.explorer.aleo.org/v1" --path "./${APPNAME}/build/" --broadcast "https://api.explorer.aleo.org/v1/testnet3/transaction/broadcast" --priority-fee 100000 --record "${RECORD}"

```

For Windows (Using direct .exe file):
```
.\snarkos developer deploy "${APPNAME}.aleo" --private-key "${PRIVATEKEY}" --query "https://api.explorer.aleo.org/v1" --path "./${APPNAME}/build/" --broadcast "https://api.explorer.aleo.org/v1/testnet3/transaction/broadcast" --priority-fee 100000 --record "${RECORD}"
```

### Result
Result (demo):
![](./.resources/deployTokenFee.png)

### ARC20:
- [ERC20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/)
- [ARC20 from Lambdaclass](https://github.com/lambdaclass/ARC20_leo)
