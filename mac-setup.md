### Ethereum Development Environment Setup (Mac)

1) Update MacOS

2) Install `Xcode` from the App Store

3) Install `Xcode Command Line Tools`
```
xcode-select --install
```

4) Install `Homebrew`
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew --version
```

5) Install the latest versions of `Ethereum` and `Geth`
```
brew update
brew tap ethereum/ethereum
brew install ethereum
brew upgrade ethereum
```

6) Install [Ganache](https://truffleframework.com/ganache)


7) Install `Node` and `NPM`
```
brew install node
```

8) Install [Truffle 4](https://truffleframework.com)
```
npm uninstall -g truffle
npm install -g truffle@4.0.4
truffle version
```

9) Install solidity/ethereum support for your text editor

10) Add [Metamask](https://metamask.io) to your browser