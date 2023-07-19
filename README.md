
# MyToken Smart Contract

This repository contains the source code for the `MyToken` smart contract

This Solidity program is a simple "Hello World" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

The MyToken smart contract is a basic implementation of a custom token with functionalities to mint (create) and burn (destroy) tokens. It allows users to manage the total token supply and individual token balances for different addresses.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., test.sol). 

# Public Variables

The contract has the following public variables:

tokenName: A string representing the name of the token (e.g., "SetKal").
tokenAbbvr: A string representing the abbreviated name of the token (e.g., "KAL").
totalSupply: An unsigned integer representing the total supply of tokens. The initial value is set to 0.

# Mapping Variable

The contract uses a mapping to keep track of token balances for different addresses:

mapping(address => uint) public tokenHolders;

The ''tokenHolders'' mapping associates each address with its corresponding token balance.

# Mint Function

The mint function allows the contract owner or a designated address to create new tokens. It takes two parameters:

_address: The address to which the newly minted tokens will be assigned.
_value: The number of tokens to mint and add to the address balance.
The function increases the total supply by the specified _value and increases the balance of the provided _address by the same amount.

# Burn Function

The burn function allows the contract owner or a designated address to destroy tokens. It takes two parameters:

_address: The address from which the tokens will be burned.
_value: The number of tokens to burn from the address balance.
The function checks if the balance of the _address is greater than or equal to the _value. If the condition is met, it deducts the _value from the total supply and reduces the _address balance accordingly. If the condition is not met, the function will revert with an error message indicating that burning more tokens than the available balance is not allowed.

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.


## Authors

Metacrafter Chris  
[@metacraftersio](https://twitter.com/metacraftersio)

## License

This project is licensed under the MIT License. See the [LICENCE](https://github.com/Aksingh-16/ETH-PROOF-METACRAFT/blob/main/LICENCE) file for details.

## Credits

This project is a solution to the project task provided by MetaCrafters.
