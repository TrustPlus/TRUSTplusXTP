
## TRUSTplusXTP

Official initial implementation of the TRUSTplus XTP core.

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

```
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev libboost-all-dev software-properties-common libdb4.8-dev libdb4.8++-dev libminiupnpc-dev libzmq3-dev software-properties-common -y
```

If you are making a headless server, please skip this next step.

```
sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler libqrencode-dev libzmq3-dev
```

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

It is recommended to run trustplusd or trustplus-qt in terminal with the flag -printtoconsole for Ubuntu. 

## Running TrustPlus-QT

It is also recommended to use CMD for windows to run trustplusd.exe or trustplus-qt.exe with the -printtoconsole flag. 

### Configuration

The configuration file is inside the Unix folder ~/.trustpluscore or Windows %appdata%/TRUSTplusCore as trustplus.conf

```
rpcuser=rpcUser
rpcpassword=<changeMe>
rpcport=37001
rpcallowedip=127.0.0.1
addnode=seed1.trustplus.com
addnode=seed2.trustplus.com
addnode=seed3.trustplus.com
addnode=seed4.trustplus.com
addnode=seed5.trustplus.com
addnode=seed6.trustplus.com
addnode=miner1.trustplus.com
addnode=miner2.trustplus.com
addnode=mn1.trustplus.com
```

#### Mining

Create an XTP Wallet. Setup your trustplus.conf file. Use cpuminer-opt from https://github.com/JayDDee/cpuminer-opt 

Example commandline for cpuminer is:

./cpuminer -a x16s -o http://127.0.0.1:37001/ -u rpcUserXX -p rpcPasswprdXX --coinbase-add=TmmDpEvmgrxxxxxxxxxxxxxxxxxxxxxxx --no-getwork --debug

Coinbase address is the wallet address you would like the reward to goto. Debug is always helpful.

#### Building a masternode

We created a Wiki page here. https://github.com/TrustPlus/TRUSTplusXTP/wiki/Making-an-XTP-MasterNode-Step-by-Step Please suggest adds and comment.

## Contribution
!! working Document !! Original Layout belongs to EthereumGo https://github.com/ethereum/go-ethereum

## License

MIT License

Copyright (c) 2018 XTP-Chain

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

=======
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
