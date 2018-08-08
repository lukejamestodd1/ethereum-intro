# How to create an ERC20 token
## Using Ropsten Test Network

### Setting up your wallet
1) Go to myetherwallet.com and set up a new wallet. This will be the address that owns and deploys the token contract. For the tutorial we will use the Ropsten test network to issue the token. Select Ropsten test network in the right hand coner. Click New Wallet →Enter a password → Download / Save your Keystore file in a safe space → Save your Private Key in a safe space. To view your wallet address, go to →View Wallet Info →Private Key → Enter the saved private key →Unlock your Wallet and it should be there.

2) It costs Ether to deploy the contract onto the blockchain. To receive one free test ehter go to http://faucet.ropsten.be:3001/, enter your wallet address and they will send it to your wallet

### Writing your token contract
3) Copy the code from token.sol and change the info at the top to the info for your token. On Line 6 change the address to your address on MyEtherWallet, change the symbol, name, and total supply. Leave the decimals as 18.

4) Scroll down to line 98 and change the function name to your coin's name. Do the same on line 111 for the function name. Change the symbol and name to your token info on lines 112 and 113
```
line 98 - contract DayByDayToken is ERC20Interface, Owned, SafeMath {
line 111 - function DayByDayToken() public {
```
5) Change the address on lines 116 and 117 to your Ether wallet address

6) change _total supply to the amount of coins you want, plus 18 zeroes on the end. In this example we are issuing 1 billion Day By Day tokens (1,000,000,000 DBD). Therefore total supply is 1 billion with 18 zeroes to make 1000000000000000000000000000. If you wanted 1000 coins your total supply would be 1000000000000000000000. Leave decimals as 18. It is recommended in the ethereum docs that you don't change this. 

### Prepare your contract for deployment
7) Next we must compile the code. Go to http://remix.ethereum.org/ and in the browser/ballot.sol, paste the code from token.sol

8) Under Compile, select the token you will create from the drop down, and press details

9) On ByteCode press the button to copy the ByteCode to the clipboard. Paste this into a text editor. Now delete everything apart from the "object" part of the code. Put 0x in front of the property for Bytecode, so you end up something like this:
```
	0x608060405234801561...(more numbers and letters)..0f0280e2f460029
```

### Deploy your contract to the blockchain
10) Now it's time to deploy the contract. Go back to My Ether Wallet and make sure the correct network (Ropsten test network for this example) is selected on the right. Go to Contracts and press Deploy Contract

11) Paste the bytecode into the ByteCode box. The gas limit should update automatically. If it doesn't check your bytecode is the correct format ie - 
```
0xByteCode
```

12) Access your wallet by selecting private key -> enter private key. Or upload the key store file to open your wallet. Press Sign Transaction then Deploy Contract.

13) Click on the transaction tx or go to  https://ropsten.etherscan.io to make sure the contract deployed.

### Verify and Publish the contract

14) Now we must verify and publish the contract. Click the Overview tab and click the Contract Address. You can also find the contract address by navigating to your wallet address and looking for the contract you deployed in the transactions list. On the contract address go to the Contract Code tab and click Verify and Publish

15) There are 5 things to complete here:


