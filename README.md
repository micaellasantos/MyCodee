# Solidity

Solidity is essential for creating smart contracts that can handle burning and minting operations in a secure and transparent manner.

## Description 

Solidity is a programming language used for developing smart contracts on the Ethereum blockchain. Burning and minting are two common operations that are performed on tokens in these smart contracts.

## Getting Started

### Executing program

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension. Copy and paste the following code into the file:

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/. 
To start, you should compile the code first then deploy and in deploy and run transactions you will copy the address then paste it on burn, mint and balances. Next, for example you will mint 300, burn 20, and then transact after that the remaining uint balance and the other remaining value will then appear.

Code:

//SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract ModuleThree {

    // public variables here
    string public tokenName = "Books";
    string public tokenAbbrv = "Heartless";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances [_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}


## Authors

Mica Ella Santos

## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details 
