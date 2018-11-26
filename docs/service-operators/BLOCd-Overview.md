# **What is BLOCd**

A daemon is a program that runs in the background. The BLOC wallet requires a node running BLOCd to connect to. That process: BLOCd, is the daemon. It can run on your computer or on a remote computer. Think of a daemon as a service. Its doing stuff in the background so you can do stuff in the foreground.

BLOCd is responsible for P2P connections and consensus for any communication with the network :

- Interaction with the blockchain, e.g. blocks relaying, getting informations about the block
- It can assemble transactions into blocks and check transactions validity
- Peer list & Connections look up
- Transaction pool information and relaying
- Synchronize and grow blockchain
- But it cannot look inside transactions to see transfers between addresses, because this requires access to user secrets wallets to do so.

BLOCd daemon provides a Command Line Interface with Command line arguments but also an HTTP RPC API and a JSON RPC API to receive informations from the blockchain allowing it to be controlled locally or remotely which makes it useful for integration with other software or in larger payment systems.

Various commands are made available by the API described on this page.

## **Screenshot**

Here's a quick image of `BLOCd MAIN NET` in action:

![BLOCd MAIN NET](images/BLOCd-MAIN-NET-v3.0.1.png)

Here's a quick image of `BLOCd TEST NET` in action:

![BLOCd TEST NET](images/BLOCd-TEST-NET-v3.0.1.png)

## **Source code**

* [Source Code](https://github.com/furiousteam/BLOC.git)

## **BLOC-DEVELOPER**

The [BLOC-DEVELOPER](https://github.com/furiousteam/BLOC.git) website documents the public APIs of BLOC.
You can test your application with your own BLOCd node and view code examples in different programming language.

- [BLOCd Daemon Configuration Arguments](https://bloc-developer.com/api_BLOCd/cli_arguments)
- [BLOCd Command Line Options](https://bloc-developer.com/api_BLOCd/options)
- [BLOCd JSON RPC API](https://bloc-developer.com/api_BLOCd/json)
- [BLOCd HTTP RPC API](https://bloc-developer.com/api_BLOCd/http)

## **BLOCd RPC Clients**

We also have some specific language bindings to make integration easier.

* [Javascript](https://github.com/furiousteam/bloc-rpc): A JavaScript wrapper for the BLOCd daemon RPC interface.
* [NodeJS](https://www.npmjs.com/package/bloc-rpc): This project is designed to make it very easy to interact with various RPC APIs available within the BLOC  Project. This entire project uses Javascript Promises to make things fast, easy, and safe.
* [Go](https://github.com/furiousteam/bloc-rpc-go): A Golang wrapper for the BLOCd RPC API. This project makes it easy to send requests to particular RPC server and returns a clear response without any abrupt termination.
* [PHP](https://github.com/furiousteam/bloc-rpc-php): A PHP wrapper for BLOC's RPC interfaces.

See [Daemon HTTP RPC API](BLOCd-daemon-http-rpc-api.md) and [Daemon JSON RPC API](BLOCd-daemon-json-rpc-api.md) for usage.

## **Downloading**

If you wish to compile **BLOCd** yourself you can download the [source Code](https://github.com/furiousteam/BLOC.git).

Binary distributions can be found: [here](https://github.com/furiousteam/BLOC/releases/latest).

Select the appropriate file for the target platform (Windows, Mac, Linux).

Binaries are provided in `.zip` format, while source code is provided in `.zip` and `.tar.gz` format.

## **Installing**

### Installing on Windows

Extract the *.zip* file (`BLOC-...-windows.zip`).

### Installing on Mac

Extract the *.zip* file:

```bash
unzip BLOC-...-mac.zip
```

### Installing on Linux

Extract the *.zip* file:

```bash
unzip BLOC-...-linux.zip
```

## Starting BLOCd

Make sure you visit the [BLOCd Command Line Arguments](BLOCd-Daemon-arguments.md) to find how to start BLOCd following different configurations.

## **Synchronizing the Blockchain**

Running `BLOCd` will start the **BLOCd** network daemon, which will connect to the network and begin downloading and verifying the BLOC blockchain.  

Because the blockchain is constantly growing, the file size always increases (the blockchain is currently over 2 GB), and **BLOCd must verify every block**, which is both CPU and disk intensive. An SSD with at least this much free disk space is recommended, unless you plan to use [remote nodes](../BLOC-servic#remote-node-options). 

### Using Checkpoints

You can sync a fresh chain from block 0 much quicker by using checkpoints. Follow [this guide](../API/Using-checkpoints-for-BLOCd.md) to learn more.