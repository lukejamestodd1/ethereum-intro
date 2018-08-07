# How to create an ERC20 token

1) Go to myetherwallet.com and set up a new wallet. This will be the address that owns and deploys the token contract.
For the tutorial we will use the Ropsten test network to issue the token so you don’t end up spending real Ether. Select Ropsten test network in the right hand side coner. 
→ click the New Wallet →Enter a password → Download / Save your Keystore file in a safe space → Save your Private Key in a safe space.
To view your wallet address, go to →View Wallet Info →Private Key → Enter the saved private key →Unlock your Wallet and it should be there.

2) It costs Ether to deploy the contract to the blockchain. If you are on the Ropsten Network go to http://faucet.ropsten.be:3001/, enter your wallet address and they will send you one test ether

3) Copy the code from token.sol and change the info at the top to the info for your token. On Line 6 change the address to your address on MyEtherWallet, change the symbol, name, and total supply. Leave the decimals as 18.

4) Scroll down to line 98 and change the function name to your coin's name. Do the same on line 111 for the function name. Change the symbol and name to your token info on lines 112 and 113
line 98 - contract DayByDayToken is ERC20Interface, Owned, SafeMath {
line 111 - function DayByDayToken() public {

5) Change the address on lines 116 and 117 to your Ether wallet address

6) change _total supply to the amount of coins you want, plus 18 zeros on the end. In this example we are issuing 1 billion Day By Day tokens (1,000,000,000 coins). Therefore total supply is 1 billion with 18 zeroes, to make 1000000000000000000000000000. If you wanted 1000 coins you would have total supply as '1000000000000000000000' - 1000 with 18 extra zeros. Leave decimals as 18. It is recommended in the ethereum docs that you don't change this. 

7) Now we will deploy the contract
