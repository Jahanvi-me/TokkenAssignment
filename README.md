# MyToken Smart Contract

This is a simple ERC20 token smart contract called `MyToken` that allows minting and burning of tokens. The contract keeps track of token details, balances, and allows the contract owner to mint new tokens and burn existing tokens.

## Token Details

- Name: Pet Dog
- Abbreviation: P.D.
- Total Supply: 0 (initially)

## Functions

### Mint Function

The `mint` function allows the contract owner to create new tokens and increase the balance of the provided address by the specified amount. The total supply is also increased accordingly.

solidity
function mint(address _theAddress, uint _num) public {
    totalSupply += _num;
    balance[_theAddress] += _num;
}


### Burn Function

The `burn` function allows the contract owner to burn existing tokens from a specific address. It checks if the balance of the address is greater than or equal to the specified amount before burning the tokens. The total supply and the balance of the address are then decreased accordingly.

solidity
function burn(address _theAddress, uint _num) public {
    if (balance[_theAddress] >= _num) {
        totalSupply -= _num;
        balance[_theAddress] -= _num;
    }
}

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

## Author

Jahanvi Sania

