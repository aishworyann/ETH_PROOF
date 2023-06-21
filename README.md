# CREATING MY OWN TOKEN : META_COIN 

The project involves the creation of a custom token using the Solidity programming language. Tokens are a fundamental aspect of the Ethereum blockchain ecosystem, representing digital assets that can be transferred and exchanged. By developing your own token, you can explore the underlying concepts of blockchain, smart contracts, and decentralized finance.

## Description
This project focuses on creating a custom token using the Solidity programming language within the Remix IDE. Remix is a popular web-based development environment that provides a user-friendly interface for writing, compiling, and deploying smart contracts on the Ethereum blockchain.

## Getting Started

### Executing program

The project will involve the following steps:

Setting up Remix:

1. Open the Remix IDE in your web browser.
* go to the Remix website at https://remix.ethereum.org/.

2. Creating the Token Contract:

* Start a new file in the code editor within Remix. Copy and paste the following code into the file:




'''
 
    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;
    contract MyToken {
    // public variables here
    string public Tname = "META_COIN";
    string public Tabbr= "MYCOIN";
    uint public supply = 1;
    // mapping variable here
    mapping(address => uint) public AddrToBal;
    
    // mint function
    function mint (address addr, uint value) public  {
        supply+= value;
        AddrToBal[addr] += value;
    }
    // burn function
    function burn (address addr , uint value) public {
        if(AddrToBal[addr] >= value){
            supply-= value;
            AddrToBal[addr] -= value;
        }
       
    }

    }




3. Compiling the Contract:

* Use the Remix compiler to compile your contract.
* Select the appropriate compiler version according to you.

4. Deploying the Contract:

* Switch to the "Deploy & run transactions" tab in Remix.
* Deploy the compiled contract by clicking the "Deploy" button.

5. Interacting with the Token:

* Utilize the Remix IDE to interact with the deployed token contract.
* Use the Addresstobalance, mint and burn functions in the "Deployed Contracts" section to perform actions like transferring tokens, checking balances, and burning tokens.
* Input the adress and value and click on the corresponding function buttons to execute our contract.


## Authors

Aishworyann
 
 @https://www.linkedin.com/in/aishworyann/
