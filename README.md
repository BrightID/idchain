## Go Ethereum

Th Official Golang implementation of the Ethereum protocol with a small hack to burn gas fees instead of awarding them to the block sealers, to be able to use it for IDChain.

## Joining IDChain Network

### Building the source on Ubuntu

```shell
$ sudo snap install go --classic
$ sudo apt-get install -y build-essential
$ git clone https://github.com/BrightID/go-ethereum.git
$ cd go-ethereum
$ make geth
$ sudo ln -sf $PWD/build/bin/geth /usr/bin/geth
```

### Running the node


```shell
$ mkdir idchain
$ cd idchain
# Initializing the node by genesis file
$ wget http://idchain.brightid.org/files/idchain.json
$ geth --datadir . init idchain.json
# Setting static peers
$ wget idchain.brightid.org/files/static-nodes.json
# Running the node
$ geth --datadir . --networkid 74
```
