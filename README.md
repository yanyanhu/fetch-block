Clone the fetch-block to ```$GOPATH/src```

```cd $GOPATH/src```
```git clone https://github.com/cendhu/fetch-block``

To compile the fetch-block tool, run the following command

```$ cd fetch-block/src```

```$ make```

After successful compilation, we can run the tool using ```$ ./fetch-block``` 

Default configurations are given in ```config.yaml```. Update config file as per the need. Make sure that the peer and fetch-block use the same MSP configuration.

When we start executing transaction on blockchain, each block is stroed in a file (with name ChannelId_blk#.json) as JSON format. In order to collect read/write set for each transaction, please replace ```fabric/events/producer/eventhelper.go``` with ```fetch-block/events/producer/eventhelper.go``` and recompile peer.  

Refer to https://blockchain-fabric.blogspot.in/ for understanding the block structure.
