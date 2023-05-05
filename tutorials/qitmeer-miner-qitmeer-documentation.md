# Qitmeer Miner :: Qitmeer Documentation

* [Table of Contents](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Prequisite](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Common](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Linux](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [MacOS](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Windows](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
* [Build](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [1. Get Source code](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [2. Install the cuckoo and opencl library](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [3. Build qitmeer-miner](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [4. Verify Build OK](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Windows-additional step](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Linux-additional step](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
* [Usage](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Run with config file](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Command line usage](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
* [FAQ](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [How to create Qitmeer adderss](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Which POW algorithm I should choose to mine ?](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Where I can find more documentation ?](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)

### Mining Tutorial <a href="#font-colorchocolate-size6mining-tutorialfont" id="font-colorchocolate-size6mining-tutorialfont"></a>

### Table of Contents <a href="#table-of-contents" id="table-of-contents"></a>

* [Prequisite](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Common](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Linux](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
    * [Ubuntu](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
    * [Centos](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [macOS](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Windows](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
* [Build](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Windows-additional step](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * \[Linux-additional step]\(#Linux-additional step)
* [Usage](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Run with config file](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Command line usage](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
* [FAQ](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [How to create Qitmeer adderss](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Which POW algorithm I should choose to mine ?](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
  * [Where I can find more documentation ?](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)

#### Prequisite <a href="#prequisite" id="prequisite"></a>

#### Common <a href="#common" id="common"></a>

1. [Git](https://git-scm.com/downloads)
2. [Go](https://golang.org/dl/) version >= 1.12

#### Linux <a href="#linux" id="linux"></a>

**Ubuntu**

```
$ sudo apt-get install beignet-dev nvidia-cuda-dev nvidia-cuda-toolkit
```

**Centos**

```
$ sudo yum install opencl-headers
$ sudo yum install ocl-icd
$ sudo ln -s /usr/lib64/libOpenCL.so.1 /usr/lib/libOpenCL.so
```

#### MacOS <a href="#macos" id="macos"></a>

#### Windows <a href="#windows" id="windows"></a>

Install [**Build Tools for Visual Studio**](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools\&rel=16)

### Build <a href="#build" id="build"></a>

#### 1. Get Source code <a href="#1-get-source-code" id="1-get-source-code"></a>

```
$ git clone git@github.com:Qitmeer/qitmeer-miner.git
```

#### 2. Install the cuckoo and opencl library <a href="#2-install-the-cuckoo-and-opencl-library" id="2-install-the-cuckoo-and-opencl-library"></a>

```
$ cd qitmeer-miner 
$ sh installLibrary.sh
```

#### 3. Build qitmeer-miner <a href="#3-build-qitmeer-miner" id="3-build-qitmeer-miner"></a>

```
//# mac
$ go build
//# linux apt install musl-tools g++ -y
$ CGO_ENABLED=1 CC=musl-gcc CXX=g++ GOOS=linux
//# windows 
$ CGO_ENABLED=1 GOOS=windows GOARCH=amd64 go build -ldflags '-extldflags "-static"' -o win-miner.exe main.go
```

#### 4. Verify Build OK <a href="#4-verify-build-ok" id="4-verify-build-ok"></a>

```
$ ./qitmeer-miner --version
```

#### Windows-additional step <a href="#windows-additional-step" id="windows-additional-step"></a>

Before step 3, do following

```
$ copy lib/cuckoo/target/release/x86_64-pc-windows-gnu/cuckoo.lib to C:/mingw64/lib
$ copy lib/opencl/windows/libOpenCL.a to C:/mingw64/lib
```

#### Linux-additional step <a href="#linux-additional-step" id="linux-additional-step"></a>

Before step 3, do following

```
$ sudo copy lib/cuckoo/target/x86_64-unknown-linux-musl/release/libcuckoo.a /usr/lib/x86_64-linux-musl
$ sudo copy lib/opencl/linux/libOpenCL.a /usr/lib/x86_64-linux-musl
```

### Usage <a href="#usage" id="usage"></a>

#### Run with config file <a href="#run-with-config-file" id="run-with-config-file"></a>

1. go to your
2. create a new config file by copying from the example config file.

```
$ cp example.solo.conf qitmeer-miner.conf
```

3. edit the config file which your create, you might need to change the `mineraddress`. you need to create a Qitmeer address if you don’t have it. Please see [FAQ](https://github.com/objemmanuel/docs/blob/master/tutorials/broken-reference/README.md)
4. run miner with the config file

```
$ ./qitmeer-miner -C qitmeer-miner.conf
```

#### Command line usage <a href="#command-line-usage" id="command-line-usage"></a>

The qitmeer-miner is a command line program. This means you can also launch it by provided valid command line options. For a full list of available command optinos, please run:

```
$ ./qitmeer-miner --help 
Debug Command:
  -l, --listdevices    List number of devices.

The Config File Options:
  -C, --configfile=    Path to configuration file
      --minerlog=      Write miner log file

The Necessary Config Options:
  -P, --pow=           blake2bd|cuckaroo|cuckatoo (blake2bd)
  -S, --symbol=        Symbol (PMEER)
  -N, --network=       network privnet|testnet|mainnet (mainnet)

The Solo Config Option:
  -M, --mineraddress=  Miner Address
  -s, --rpcserver=     RPC server to connect to (127.0.0.1)
  -u, --rpcuser=       RPC username
  -p, --rpcpass=       RPC password
      --randstr=       Rand String,Your Unique Marking. (Come from Qitmeer!)
      --notls          Do not verify tls certificates (true)
      --rpccert=       RPC server certificate chain for validation

The pool Config Option:
  -o, --pool=          Pool to connect to (e.g.stratum+tcp://pool:port)
  -m, --pooluser=      Pool username
  -n, --poolpass=      Pool password

The Optional Config Option:
      --cpuminer       CPUMiner (false)
      --proxy=         Connect via SOCKS5 proxy (eg. 127.0.0.1:9050)
      --proxyuser=     Username for proxy server
      --proxypass=     Password for proxy server
      --trimmerTimes=  the cuckaroo trimmer times (40)
      --intensity=     Intensities (the work size is 2^intensity) per device. Single global value or a comma separated list. (24)
      --worksize=      The explicitly declared sizes of the work to do per device (overrides intensity). Single global value or a comma separated list. (256)
      --timeout=       rpc timeout. (60)
      --use_devices=   all gpu devices,you can use ./qitmeer-miner -l to see. examples:0,1 use the #0 device and #1 device
      --max_tx_count=  max pack tx count (1000)
      --max_sig_count= max sign tx count (5000)
      --log_level=     info|debug|error|warn|trace (debug)
      --stats_server=  stats web server (127.0.0.1:1235)
      --edge_bits=     edge bits (24)
      --local_size=    local size (4096)
      --group_size=    work group size (256)

Help Options:
  -h, --help           Show this help message
 
```

Please see [Qitmeer-Miner User References](https://qitmeer.github.io/docs/en/reference/qitmeer-miner/) for more details

### FAQ <a href="#faq" id="faq"></a>

There are several ways to create a Qitmeer address. you can use [qx](https://qitmeer.github.io/docs/en/reference/qxtools/) command , [qitmeer-wallet](https://github.com/Qitmeer/qitmeer-wallet), etc. The most easy way to download the [kafh wallet](https://www.kahf.io/), which provide a more user friendly GUI to create your address/wallet step by step.

#### Which POW algorithm I should choose to mine ? <a href="#which-pow-algorithm-i-should-choose-to-mine" id="which-pow-algorithm-i-should-choose-to-mine"></a>

Qitmeer test network support mixing minning, which means your can choice from `Cuckaroo`, `Cuckatoo` and `Blake2bd` anyone you like. But the start difficulty targets are quite different. For the most case you might use `Cuckaroo` as a safe choice at the beginning.

#### Where I can find more documentation ? <a href="#where-i-can-find-more-documentation" id="where-i-can-find-more-documentation"></a>

Please find more documentation from the [Qitmeer doc site at https://qitmeer.github.io](https://qitmeer.github.io/docs/en/reference/qitmeer-miner/)
