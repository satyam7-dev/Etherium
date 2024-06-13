# Etherium

```markdown
# MyToken Solidity Contract

This Solidity contract implements a simple ERC20-like token with minting and burning functionality. The contract includes public variables to store the token's name, abbreviation, and total supply, as well as a mapping to keep track of each address's balance.

## Contract Details

- **Token Name:** Ether
- **Token Abbreviation:** ETH
- **Total Supply:** The total number of tokens in circulation.

## Functions

### Public Variables

- `string public tokenName` - The name of the token.
- `string public tokenAbbreviation` - The abbreviation of the token.
- `uint public totalSupply` - The total supply of the token.

### Mapping

- `mapping(address => uint) public balances` - A mapping that stores the balance of each address.

### Mint Function

```solidity
function mint(address to, uint value) public
```

Increases the total supply of the token by the specified value and adds the same amount to the balance of the specified address.

**Parameters:**
- `to` - The address to which the minted tokens will be added.
- `value` - The number of tokens to mint.

### Burn Function

```solidity
function burn(address from, uint value) public
```

Decreases the total supply of the token by the specified value and subtracts the same amount from the balance of the specified address.

**Parameters:**
- `from` - The address from which the tokens will be burned.
- `value` - The number of tokens to burn.

**Requirements:**
- The balance of the `from` address must be greater than or equal to the value to be burned.

## Deployment

To deploy this contract, follow these steps:

1. Install [Solidity](https://docs.soliditylang.org/en/v0.8.0/installing-solidity.html) and a suitable development environment like [Remix](https://remix.ethereum.org/) or [Truffle](https://www.trufflesuite.com/truffle).

2. Copy the contract code into a new file with a `.sol` extension, e.g., `MyToken.sol`.

3. Compile the contract using the Solidity compiler.

4. Deploy the contract to the Ethereum network using Remix, Truffle, or any other deployment tool of your choice.

## Usage

Once the contract is deployed, you can interact with it using the following methods:

- Call `mint(address to, uint value)` to mint new tokens and add them to the balance of the specified address.
- Call `burn(address from, uint value)` to burn tokens and subtract them from the balance of the specified address.

## Example

```solidity
// Deploy the contract
MyToken token = new MyToken();

// Mint 100 tokens to address 0x123...
token.mint(0x123..., 100);

// Burn 50 tokens from address 0x123...
token.burn(0x123..., 50);
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```

