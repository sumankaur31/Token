# Token
This solidity program demonstrates the creation of a simple token using a smart contract. The purpose of the program is to give a basic idea for creation of smart contracts in solidity and see how they work,
## Description
This solidity program is used to create a token using smart contract. The smart contract created has state variables associated with the token namely token_name, token_abbrv, total_supply and a mapping. There are also functions namely mint and burn for the transactions of tokens.
## Executing program
Use remix, an online solidity IDE to run the below code:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public token_name= "Vision";
    string public token_abbrv="VS";
    uint public total_supply=0;

    // mapping variable here
    mapping(address => uint) public balance;
    
    // mint function
    function mint(address _add, uint value) public{
        total_supply += value;
        balance[_add] += value;
    }

    // burn function
    function burn(address _add, uint value) public{
        if (balance[_add]>= value){
            total_supply -= value;
            balance[_add] -= value;
        }
    }

}
```
## Author
Sumanpreet Kaur
