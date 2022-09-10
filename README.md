# Lesson_21
# Primary application file
Create a fungible token that is ERC-20 compliant and that will be minted by using a Crowdsale contract from the OpenZeppelin Solidity library.

The crowdsale contract that created will manage the entire crowdsale process, allowing users to send ether to the contract and in return receive KAI, or KaseiCoin tokens. Your contract will mint the tokens automatically and distribute them to buyers in one transaction.

---

## Technologies

The following Technologies were used to develop this program:

Solidity

Terminal
    Version 2.12.5 (444)

Visual Studio Code
    Version: 1.66.2 (Universal)
    Commit: dfd34e8260c270da74b5c2d86d61aee4b6d56977
    Date: 2022-04-11T07:49:20.994Z
    Electron: 17.2.0
    Chromium: 98.0.4758.109
    Node.js: 16.13.0
    V8: 9.8.177.11-electron.0
    OS: Darwin x64 21.4.0
    
---

## General information about analysis.
There are four parts to this Lesson:

### Create the KaseiCoin Token Contract:

Import the following contracts from the OpenZeppelin library into KaseiCoin contract:

ERC20

ERC20Detailed

ERC20Mintable

Define a contract for the KaseiCoin token called KaseiCoin, and have the contract inherit the three contracts that you just imported from OpenZeppelin.  Then inside of your KaseiCoin contract, add a constructor with the following parameters: name, symbol, and initial_supply.  After that, as part of your constructor definition, add a call to the ERC20Detailed contract’s constructor, passing the parameters name, symbol, and 18. Recall that 18 is the value for the decimal parameter.  Finally compile the contract using compiler version 0.5.5.

![Compiled](./Execution_Results/KaseiCoin_Compile.png)


### Create the KaseiCoin Crowdsale Contract:

Ensure the crowd sale has the OpenZeppelin contracts for Crowdsale and MintedCrowdsale.  Next with the KaseiCoinCrowdsale constructor provide parameters for all of the features needed for the crowd sale, such as rate, wallet, and token and then configure these parameters for the KaseiCoin token.  Compile the contract using compilier version 0.5.5.

![Compiled](./Execution_Results/Deploy_KaseiCoin_CrowdSale_Contract.png)





### Create the KaseiCoin Deployer Contract:


### Deploy the Crowdsale to a Local Blockchain:
---

## Information about datasets

Contract:

Joint Savings

Variables:

   address:
    
   accountOne
   
   accountTwo
   
   lastToWithdraw
   
   uint:
   
   lastWithdrawAmount
   
   contractbalance
   

Functions:

withdraw

deposit

setAccounts

fallback (external payable)

---

## Libraries used in analysis

pragma solidity ^0.5.0

---

## Contributors


**Chris Miskovich**

Contact Information:

Email: cmiskovich@verizon.net

[LinkedIn](https://www.linkedin.com/in/christopher-miskovich-9a61b0234/) 

---

## License

[MIT](/license.txt)
