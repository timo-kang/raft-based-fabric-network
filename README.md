# fabric-network ( HLF v2.3.3 )

## Objective
3 Org, 3 CA
* 5 endorsing peer nodes, ( additionally 1 peer node reading ledger )
Ordering Service : Raft
* 5 raft nodes

### Features
* [ ] add / reduce raft nodes on online
* [ ] add / reduce endorsing peer nodes on online
* [ * ] create a new channel
* [ ] backup & restore ledger and network

### Download docker images and binaries
`curl -sSL https://bit.ly/2ysbOFE | bash -d -b --`
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
