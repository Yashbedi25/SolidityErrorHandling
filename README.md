# Error Handling

This Solidity program is a simple Error handling program that demonstrates the essential condition which must be checked before a function is executed in the Solidity programming language.
The primary purpose of this program is to handle errors in the function or code encountered while running and executing the code.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. 
The contract has 4 functions to handle the error in a different manner or by using different functions require(), revert(), assert() and the one function is just to set the age.
In this Eligible Criteria contract basically, it will check whether your age limit is eligible or not for the vote through this 3 error handling function.
This program serves as a simple and straightforward introduction to Error handling and can be used as a stepping stone for more complex projects in the future for handling error in the contract.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol).

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

import "hardhat/console.sol";

contract AssertionExample {
    uint public age;
    function setAgeLimit(uint _age) public{
        age=_age;
    }

    function requireExample() public view  {
        require(age >= 18, "NOT ELIGIBLE FOR VOTE");
        console.log("YOU ARE ELIGIBLE FOR VOTE");
    }
    
    function assertExample() public view {
        assert(age >=18);
        console.log("YOU ARE ELIGIBLE FOR VOTE");
    }
    
    function revertExample() public view {
        if (age>=18) {
            revert("YOU ARE ELIGIBLE FOR VOTE");
        }
        else{
            console.log("YOU ARE NOT ELIGIBLE FOR VOTE");
        }
    }
}


```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "ASSERTIONEXAMPLE" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the 4 functions. Click on the "ASSERTIONEXAMPLE" contract in the left-hand sidebar, then set the age limit by typing, and then see age by clicking age after that click on the three functions check the console to check the output, and also check if the error is encounter or not. 

Finally, the transaction occurred and some transactions revert back to their initial state.



## Authors

Metacrafter Chris  
[@metacraftersio](https://twitter.com/metacraftersio)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
