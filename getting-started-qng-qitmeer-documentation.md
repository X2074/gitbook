# Getting Started QNG :: Qitmeer Documentation

### Prerequisites <a href="#prerequisites" id="prerequisites"></a>

#### Introduction <a href="#introduction" id="introduction"></a>

The Qitmeer network implementation with the plug-able VMs under the MeerDAG consensus.

### Run QNG <a href="#run-qng" id="run-qng"></a>

#### Install <a href="#install" id="install"></a>

* Build from source

```
~ git clone https://github.com/Qitmeer/qng.git
~ make
```

or

* Install the latest qng available here: [https://github.com/Qitmeer/qng/releases](https://github.com/Qitmeer/qng/releases)

or

* Build with Docker:

#### Run <a href="#run" id="run"></a>

* We take the construction of network nodes as an example:

```
~ cd ./build/bin
~ ./qng 
or
~ docker run --rm -it --name qng qng:latest ./build/bin/qng --acceptnonstd --modules=qitmeer --modules=p2p
```

#### MeerEVM <a href="#meerevm" id="meerevm"></a>

* If you want to use our MeerEVM function, the required interface information can be queried in this RPC:

```
~ cd ./script
~ ./cli.sh vmsinfo
```

* If you don’t need the default configuration, we provide an environment configuration parameter to meet your custom configuration for MeerEVM:

```
~ ./qng --evmenv="--http"
or
~ ./qng --evmenv="--http --http.port=8545 --ws --ws.port=8546"
or
~ ./qng --evmenv="--syncmode=full --gcmode=archive --http --http.addr=0.0.0.0 --http.port=8545 --ws --ws.port=8546 --ws.addr=0.0.0.0 --http.api=eth,web3,net,debug,txpool --ws.api=eth,web3,net,debug,txpool"
```
