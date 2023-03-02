# Getting Started :: Qitmeer Documentation

* Prerequisites
  * [Introduction](./)
  * [Development Environment](tutorials/development-environment-qitmeer-documentation.md)
* Run Qitmeer
  * [Install](tutorials/qitmeer-installation-qitmeer-documentation.md)
  * Run
* Run Wallet
  * [Install](tutorials/qitmeer-installation-qitmeer-documentation.md)
  * [create wallet](wallet-json-prc/ui-api/createwallet-qitmeer-documentation.md)
  * [get address](wallet-json-prc/wallet-api/getaddressesbyaccount-qitmeer-documentation.md)
  * [update db](wallet-json-prc/qitmeerd-api/update-qitmeer-documentation.md)
  * Run Miner
* [Send Transaction](commands-references/qitmeer-cli-qitmeer-documentation/blockchain/sendrawtransaction-qitmeer-documentation.md)

### Prerequisites <a href="#prerequisites" id="prerequisites"></a>

#### Introduction <a href="#introduction" id="introduction"></a>

This tutorial gives a quick practice on how to use qitmeer to send a transaction from scratch. It covers 3 core roles in the network: qitmeer, miner, wallet. So, it would help you get a basic concept of qitmeer network in short time.

It includes four sections: first we launch a Qitmeer test node as server to provide the fundamental blockchain service; then we launch the qitmeer command line wallet to generate wallet for miner; in the next step, we run a miner node to win the mining reward from the network; lastly, we use wallet to send a transaction to an arbitrary recipient using our mining reward.

Note: this tutorial is just targeted for beginners to experience the core functionality of Qitmeer network as soon as possible. So we tried to skip some steps which should have been best practice. Such as , TLS , strong password, saving important information, etc. So, after gone through this tutorial, please dive into the our documents of each project to get a better practice.

#### Development Environment <a href="#development-environment" id="development-environment"></a>

Follow Development Environment

### Run Qitmeer <a href="#run-qitmeer" id="run-qitmeer"></a>

Open a new terminal window

#### Install <a href="#install" id="install"></a>

* Docker\
  Follow Qitmeer Installation to install docker

```
alias qitmeer="docker run -it -p 18130:18130 -p 18131:18131 qitmeer/qitmeerd"  
```

* Build from Source

```
export QITMEER_URI=github.com/Qitmeer/qitmeer

git clone https://${QITMEER_URI} ~/${QITMEER_URI} 
cd ~/${QITMEER_URI} 
go build

alias qitmeer="~/${QITMEER_URI}/qitmeer"
```

#### Run <a href="#run" id="run"></a>

```
 qitmeer --notls --rpcuser=test --rpcpass=test
```

### Run Wallet <a href="#run-wallet" id="run-wallet"></a>

Open a new terminal window

#### Install <a href="#install-1" id="install-1"></a>

```
export WALLET_URI=github.com/Qitmeer/qitmeer-wallet
git clone https://${WALLET_URI} ~/${WALLET_URI} --depth=1
cd ~/${WALLET_URI}
go build

alias qc="~/${WALLET_URI}/qitmeer-wallet --qserver=127.0.0.1:18131 --qpass=test --quser=test qc"
alias qx="~/${WALLET_URI}/qitmeer-wallet qx"
```

#### create wallet <a href="#create-wallet" id="create-wallet"></a>

```
$ wallet qc create
Enter the private passphrase for your new wallet: [WALLET_PASSWORD]
Confirm passphrase: [WALLET_PASSWORD]
Do you want to add an additional layer of encryption for public data? (n/no/y/yes) [no]:
pubPass: public
Do you have an existing wallet seed you want to use? (n/no/y/yes) [no]:
Your wallet generation seed is:
[GENERATION_SEED]
IMPORTANT: Keep the seed in a safe place as you
will NOT be able to restore your wallet without it.
Please keep in mind that anyone who has access
to the seed can also restore your wallet thereby
giving them access to all your funds, so it is
imperative that you keep it in a secure location.
Once you have stored the seed in a safe and secure location, enter "OK" to continue: OK
Creating the wallet...
pri:[PRIVATE_KEY]
The wallet has been created successfully.
createWallet succ
```

#### get address <a href="#get-address" id="get-address"></a>

```
export PRIVATE_KEY=[PRIVATE_KEY]
export WALLET_PASSWORD=[WALLET_PASSWORD]
qx pritoaddr $PRIVATE_KEY testnet
```

This will return the corresponding address, assume it is \[MINER\_ADDRESS]

#### update db <a href="#update-db" id="update-db"></a>

This process will last a little bit long time, you may process the following steps

#### Run Miner <a href="#run-miner" id="run-miner"></a>

Open a new terminal window

**Install**

Follow Qitmeer Miner to install dependencies of Miner

```
# replace MINER_URI with your miner directory
export MINER_URI=github.com/qitmeer/qitmeer-miner
git clone https://${MINER_URI} ~/${MINER_URI} --depth=1
alias miner="~/${MINER_URI}/qitmeer-miner"
```

**Run**

```
# replace MINER_ADDRESS with your miner address
export MINER_ADDRESS=[MINER_ADDRESS]
miner --mineraddress=${MINER_ADDRESS} --network=testnet --rpcuser=test --rpcpass=test --rpcserver=127.0.0.1:18131
```

### Send Transaction <a href="#send-transaction" id="send-transaction"></a>

Switch to wallet terminal

```
export RECIPIENT_MNEMONIC=$(qx generatemnemonic)
export RECIPIENT_ADDRESS=$(qx mnemonictoaddr "${RECIPIENT_MNEMONIC}" testnet)

#  make sure your mining reward matured before executing this command
qc sendtoaddress $RECIPIENT_ADDRESS 9 $WALLET_PASSWORD

```
