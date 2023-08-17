## step 01

#### build the bootnode

`docker build --no-cache -t bootnode .`

#### create the network for connecting the bootnode with other miner nodes

`docker network create blockchain`

#### run the bootnode boot node use port 30310 for udp

`docker run --network=blockchain --name bootnode -p 30310:30310/udp bootnode`

#### build the miner node 1

`docker build --no-cache -t miner-node-01 .`

#### run the miner node 1

`docker run --name miner-node-01 --network=blockchain -p 8040:8040 miner-node-01`

#### build the miner node 2

`docker build --no-cache -t miner-node-02 .`

#### run the miner node 2

`docker run --name miner-node-02 --network=blockchain -p 8041:8041 miner-node-02`

#### build the miner node 3

`docker build --no-cache -t miner-node-03 .`

#### run the miner node 3

`docker run --name miner-node-03 --network=blockchain -p 8042:8042 miner-node-03`
