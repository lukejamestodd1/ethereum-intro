### Ethereum Development Environment Setup (Debian-based Linux)

1) Install latest ethereum and geth
```
sudo apt-get install software-properties-common
sudo add-apt-repository -y ppa:ethereum/ethereum
sudo apt-get update
sudo apt-get install ethereum
```

2) Install [node](https://nodejs.org/en/)
```
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
```

3) Install [Ganache](http://truffleframework.com/ganache/)

4) Install [Truffle 4](https://truffleframework.com)
```
npm uninstall -g truffle
npm install -g truffle@4.0.4
truffle version
```

5) Install solidity/ethereum support for your text editor

6) Add [Metamask](https://metamask.io) to your browser