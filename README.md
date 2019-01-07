
## TRUSTplusXTP

Official inital implementation of the TRUSTplus XTP core.

[![Discord](https://img.shields.io/badge/Chat-on%20Discord-blue.svg)](https://discord.gg/56Dfku) 
[![Slack](https://img.shields.io/badge/Chat-on%20Slack-red.svg)](https://join.slack.com/t/trustplus/shared_invite/enQtNTE3MjU1MTM2MzA4LTMwNWRjMDAxMDI1NWMwZDY0YWNjYWRhNDNjNzA3Y2VlNDkxOGM2MDkzNjc5Zjk5ZGQxZTQ0MWNiN2RiYzRhY2M) 
[![IRCchat](https://img.shields.io/badge/Chat-on%20IRCchat-brightgreen.svg)](http://webchat.freenode.net/?channels=trustpluscoin)

## Rewards
TrustPlusXTP is strait forward: 10 XTP per block, 50% is created for the winning masternode, halving in increments of 500,000 blocks.

There is a 35,000,000 XTP block reward at block 1 to fund the TRUST swap.
The first 9600 blocks rewards are 0.1 with 1% of the reward going to Masternodes.

Source: https://github.com/TrustPlus/TRUSTplusXTP/blob/20896def5c5166206c818a4583c2f73c27c8c6c7/src/main.cpp#L1746

## Building the source

`sudo add-apt-repository ppa:bitcoin/bitcoin`

`sudo apt-get update`

`sudo apt-get install git zip unzip -y`

`sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev libboost-all-dev software-properties-common libdb4.8-dev libdb4.8++-dev libminiupnpc-dev libzmq3-dev software-properties-common -y`

If you would like to create QT or the GUI interface please add this step.

`sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler libqrencode-dev libzmq3-dev`

`git clone git://github.com/TrustPlus/TRUSTplusXTP`

`cd TRUSTplusXTP`

`./autogen.sh`

`./configure`

`make`

**Note some Servers will require sudo**

## Executables

Source should be inside ~/TRUSTplusXTP/src folder
QT files are inside ~/TRUSTplusXTP/src/qt folder

## Running trustplusd

## Running TrustPlus-QT

### Configuration

#### Running a private miner

#### Running a masternode

## Contribution
!! working Document !! Original Layout belongs to EthereumGo https://github.com/ethereum/go-ethereum

## License
