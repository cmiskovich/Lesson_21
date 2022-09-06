# Lesson_21
# Primary application file
Completing the JointSavings smart contract in solidity.  Then create a folder named Execution_Results that contains eight images.  The images will confirm that the deposit and withdrawl transactions that test the JointSavings functionality in the JavaScript VM, worked as expected.

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
There are three parts to this Lesson:

### Create a Joint Savings Account Contract in Solidity:

Define a new contract named JointSavings and define the following variables in the new contract:

   Two variables of type address payable named accountOne and accountTwo

   A variable of type address public named lastToWithdraw

   Two variables of type uint public named lastWithdrawAmount and contractBalance

Define a function named withdraw that accepts two arguments: 
    amount of type uint and recipient of type payable address. 
    
   In this function, code the following:

   Define a require statement that checks if recipient is equal to either accountOne or accountTwo. If it isn’t, the require statement returns the “You      don't own this account!” text.

Define a require statement that checks if balance is sufficient for accomplishing the withdrawal operation. If there are insufficient funds, it returns the “Insufficient funds!” text.

Add an if statement to check if lastToWithdraw is not equal (!=) to recipient. If it’s not equal, set it to the current value of recipient.

Call the transfer function of the recipient, and pass it the amount to transfer as an argument.

Set lastWithdrawAmount equal to amount.

Set the contractBalance variable equal to the balance of the contract by using address(this).balance to reflect the new balance of the contract.

Define a public payable function named deposit. In this function, code the following:

Set the contractBalance variable equal to the balance of the contract by using address(this).balance.
Define a public function named setAccounts that takes two address payable arguments, named account1 and account2. In the body of the function, set the values of accountOne and accountTwo to account1 and account2, respectively.

Add a fallback function so that your contract can store ether that’s sent from outside the deposit function.



### Compile and Deploy Your Contract in the JavaScript VM:

Compile the file in Solidity and then click the Deploy button to deploy your smart contract, and then confirm that it successfully deployed.

You can now interact with your smart contract.




### Interact with Your Deployed Smart Contract:

Use the setAccounts function to define the authorized Ethereum address that will be able to withdraw funds from your contract.

![Set_Accounts](./Execution_Results/Step3_1_Set_Accounts.png)

Test the deposit functionality of your smart contract by sending the following amounts of ether. After each transaction, use the contractBalance function to verify that the funds were added to your contract:

Transaction 1: Send 1 ether as wei:

![Transaction1](./Execution_Results/Step3_2_T1A_EUC_1ETH.png)
![Transaction1](./Execution_Results/Step3_2_T1B_1ETH_AS_WEI.png)
![Transaction1](./Execution_Results/Step3_2_T1C_1ETH_IN_WEI_CONTRACTBALANCE.png)


Transaction 2: Send 10 ether as wei:

![Transaction2](./Execution_Results/Step3_2_T2A_EUC_10ETH.png)
![Transaction2](./Execution_Results/Step3_2_T2B_ADDING_10ETH_AS_WEI.png)
![Transaction2](./Execution_Results/Step3_2_T2C_11ETH_AFTER_10ETH_WEI_ADDED.png)

Transaction 3: Send 5 ether:

![Transaction3](./Execution_Results/Step3_2_T3A_SEND_5ETH.png)
![Transaction3](./Execution_Results/Step3_2_T3B_16ETH_AFTER3TRANSACTIONS.png)


Test the contract’s withdrawal functionality by withdrawing 5 ether into accountOne:

![accountOne](./Execution_Results/Step3_3_Acct1A.png)
![accountOne](./Execution_Results/Step3_3_Acct1B.png)
![accountOne](./Execution_Results/Step3_3_Acct1C.png)


Test the contract’s withdrawal functionality by withdrawing 10 ether into accountTwo:

![accountTwo](./Execution_Results/Step3_3_Acct2A.png)
![accountTwo](./Execution_Results/Step3_3_Acct2B.png)
![accountTwo](./Execution_Results/Step3_3_Acct2C.png)
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
