# fabric-network ( HLF v2.3.3 )

## Objective
3 Org, 3 CA
Org 1 has 2 peers, Org 2 has 1 peer node.
<!-- * 5 endorsing peer nodes, ( additionally 1 peer node reading ledger ) -->
Ordering Service : Raft
* 5 raft nodes

### Features
* [ ] add / delete raft nodes on online
* [ ] add / delete peer nodes on online
* [ ] backup & restore ledger and network
<!-- * [ ] create a new channel -->

### Download docker images and binaries
`curl -sSL https://bit.ly/2ysbOFE | bash -b --`
```
  // export PATH environment variable to use fabric commands
  export PATH=$PWD/bin:$PATH
```


* output
```
===> List out hyperledger docker images
hyperledger/fabric-ca        1.5                 4ea287b75c63        2 months ago        69.8MB
hyperledger/fabric-ca        1.5.2               4ea287b75c63        2 months ago        69.8MB
hyperledger/fabric-ca        latest              4ea287b75c63        2 months ago        69.8MB
hyperledger/fabric-tools     2.3                 98fa0bfb0fd2        2 months ago        445MB
hyperledger/fabric-tools     2.3.3               98fa0bfb0fd2        2 months ago        445MB
hyperledger/fabric-tools     latest              98fa0bfb0fd2        2 months ago        445MB
hyperledger/fabric-peer      2.3                 a491b5ab42f6        2 months ago        53.3MB
hyperledger/fabric-peer      2.3.3               a491b5ab42f6        2 months ago        53.3MB
hyperledger/fabric-peer      latest              a491b5ab42f6        2 months ago        53.3MB
hyperledger/fabric-orderer   2.3                 9e1952b8840d        2 months ago        35.4MB
hyperledger/fabric-orderer   2.3.3               9e1952b8840d        2 months ago        35.4MB
hyperledger/fabric-orderer   latest              9e1952b8840d        2 months ago        35.4MB
hyperledger/fabric-ccenv     2.3                 56fa403e02ee        2 months ago        502MB
hyperledger/fabric-ccenv     2.3.3               56fa403e02ee        2 months ago        502MB
hyperledger/fabric-ccenv     latest              56fa403e02ee        2 months ago        502MB
hyperledger/fabric-baseos    2.3                 b35a8ef578c0        2 months ago        6.87MB
hyperledger/fabric-baseos    2.3.3               b35a8ef578c0        2 months ago        6.87MB
hyperledger/fabric-baseos    latest              b35a8ef578c0        2 months ago        6.87MB
```

### Run a Network
If you downloaded fabric binaries successfully, Now you can start the network.
before construct your first network, check again binaries and config files are located on proper path.
`PATH=${BASE_DIR}/bin`, `FABRIC_CFG_PATH=${BASE_DIR}/config`

Starting Network command is  `./network.sh up -ca -r -s`.

### Create A Channel
You can create a channel with `./network.sh createChannel`.
With `-c` option, you can give a channel name. `./network.sh createChannel -c kingworm_channel`

### Deploy A Chaincode
You can install & deploy a chaincode to the channel with `./network.sh deployCC`.
You should specify name, language, and path of the chaincode.
`./network.sh deployCC -c kingworm_channel -ccn timo_chaincode -ccl typescript -ccv 1.0.0 -ccp ../../timo-chaincode/`
You can get more details with `./nework.sh deployCC --help`.