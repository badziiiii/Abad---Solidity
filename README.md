
# Solidity MyToken

This Solidity program is about Token Minting and Token Burning. This program was created for Metacrafters program that has a course about solidity beginners course assessment.

## Description

This contract implements a simple token with minting and burning functionality.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension. Copy and paste the following code into the file:


// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;


contract MyToken {


    // public variables here
    string public tokenName = "Itan";
    string public tokenAbbrv = "Nok";
    uint public totalSupply = 0;


    // mapping variable here
    mapping (address => uint) public balances;


    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }


    // burn function
    function burn (address _address, uint _value) public  {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }


}


```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile SolidityAbad.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "SolidityAbad" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed it will show the creation of your token.

## Authors

[NTC-S] Christian Lloyd Abad  
[@badziiiii](https://twitter.com/ChrAbad)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
