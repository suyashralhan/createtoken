# Creating a token

The token, referred to as "META" and abbreviated as "MTA," is associated with a project that enables the creation and destruction of tokens.

The project's objectives can vary depending on your specific aims and intentions:

1. Custom Token Creation: If you choose to utilize this project, you can generate a personalized token named "META" on the Ethereum blockchain. This token, symbolized as "MTA," can fulfill a variety of roles, including representing ownership, value, or participation rights within a particular ecosystem or project.

2. Token Minting and Burning: The project offers functionality for the creation (minting) and removal (burning) of tokens. By utilizing the mint function, you can augment the total token supply and allocate them to a designated address. On the other hand, the burn function facilitates the reduction of tokens held by a specific address, subsequently decreasing the overall token supply. This capability proves useful for managing token distribution, rewards, or adjusting token supply based on specific rules or requirements.

3. Token Management and Balances: Within the project, a mapping variable named "balances" is implemented to track the token balances held by various addresses. The balances are publicly accessible through the "public" keyword, ensuring transparency. This feature enables users or external systems to verify token balances, thereby facilitating efficient token management.

## Description

This project entails the creation of a token named "META" with the symbol "MTA" on the Ethereum blockchain. Its purpose is to establish a digital asset that can serve multiple functions within a designated ecosystem or project. The mint function allows for the generation of new tokens, expanding the overall supply and assigning them to a specified address. This functionality can be utilized for tasks like token distribution, rewards, or fundraising efforts. Conversely, the burn function enables the removal of tokens from a particular address, effectively decreasing the total supply. This feature is valuable for managing token availability according to specific rules or requirements. Additionally, the project incorporates a mapping variable named "balances" that keeps track of token holdings across different addresses. This aspect enhances transparency and permits users or external systems to verify the amount of tokens held. Overall, this project provides you with the ability to create, manage, and distribute a customized token on the Ethereum blockchain, presenting various potential applications such as loyalty programs, decentralized finance (DeFi) platforms, or in-app currencies within a specific ecosystem.

## Getting Started

### Installing
Installing an Ethereum development environment - We can set up an Ethereum development environment using Remix Etheruem IDE There are no specific modifications needed to the files. However, it's important to ensure that we have the necessary dependencies and development environment set up correctly.

## Executing a program

To run the provided smart contract code, we can follow these step-by-step instructions:

Set up the Ethereum Development Environment:
Install Remix IDE, a web-based Ethereum development environment, or use another development environment of your choice. 2. Creating a New Solidity File:

Open the Remix IDE . Create a new Solidity file and name it "MyToken.sol". Write the required code into the "MyToken.sol" file. Compile the Smart Contract:

In the Remix IDE, navigate to the "Solidity Compiler" section. Select the "MyToken.sol" file. Click the "Compile" button to compile the smart contract.

Deploy the Smart Contract:
In the Remix IDE, navigate to the "Deploy & Run Transactions" section. Select the "MyToken" contract from the dropdown. Click the "Deploy" button to deploy the smart contract to the selected network. Take note of the deployed contract's address for future interactions.

Interact with the Smart Contract:
In the Remix IDE, navigate to the "Deployed Contracts" section. Select the deployed "MyToken" contract from the list. We will see the contract's public variables (tokenName, tokenAbbrv, totalSupply) and the "balances" mapping. To interact with the contract, you can use the provided functions: To mint new tokens, call the "mint" function and provide an address and the amount to mint as parameters. To burn tokens, call the "burn" function and provide an address and the amount to burn as parameters. After executing a function, you can check the updated state variables and balances.

## Code block:
function mint (address _address, uint _value) public
{
    totalSupply += _value;
    balances[_address] += _value;
}

function burn (address _address, uint _value) public
{
    if(balances[_address] >= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
 }
## Authors
Suyash Ralhan
## License
This project is licensed under the [Suyash Ralhan] License - see the LICENSE.md file for details
