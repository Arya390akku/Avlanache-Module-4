
---

# DegenToken

`DegenToken` is a custom ERC20 token built on the Ethereum blockchain. The token allows users to mint, transfer, burn, and redeem tokens for items. The contract also provides functionality to view available items in the store and the items owned by individual accounts.

## Features

- **ERC20 Compliance**: The contract follows the ERC20 standard, allowing standard token operations such as transfer, minting, and burning.
- **Item Redemption**: Users can redeem their tokens for in-game items such as MTB, HYBRID, and ROADBIKE.
- **Item Tracking**: The contract tracks item quantities available in the store and items owned by each user.
- **Ownership Control**: The owner of the contract has exclusive rights to mint new tokens.

## Contract Details

### Enumerations

- `ItemType`: Defines three types of items available for redemption:
  - `MTB`
  - `HYBRID`
  - `ROADBIKE`

### Mappings

- `itemPrices`: Stores the price of each item type in AVAX.
- `itemQuantities`: Tracks the available quantities of each item type in the store.
- `accountItems`: Tracks the quantities of each item type owned by each account.

### Main Functions

- `mint(address to, uint256 amount)`: Allows the owner to mint new tokens and assign them to a specific address.
- `transferTokens(address recipient, uint256 amount)`: Allows users to transfer tokens to another address.
- `redeemTokens(ItemType itemType, uint256 quantity)`: Allows users to redeem tokens for in-game items.
- `burnTokens(uint256 amount)`: Allows users to burn (destroy) their tokens.
- `viewInStoreItems()`: Displays the quantities of items available in the store.
- `viewOwnedItems(address account)`: Displays the quantities of items owned by a specific account.

### Helper Functions

- `toString(uint256 value)`: Converts a `uint256` value to its string representation.

## Setup and Deployment

### Prerequisites

- [Remix IDE](https://remix.ethereum.org/): An online Solidity IDE.
- MetaMask or other Ethereum wallet for deploying and interacting with the contract.

### Steps

1. **Open Remix IDE**

   Visit [Remix IDE](https://remix.ethereum.org/) in your web browser.

2. **Create a New File**

   - In the Remix IDE, create a new file named `DegenToken.sol`.
   - Copy and paste the Solidity code into the file.

3. **Compile the Contract**

   - Click on the "Solidity Compiler" tab in Remix.
   - Select `0.8.18` (or the version you're using) from the compiler version dropdown.
   - Click on the "Compile DegenToken.sol" button.

4. **Deploy the Contract**

   - Click on the "Deploy & Run Transactions" tab in Remix.
   - Select the environment (e.g., "Injected Web3" if you're using MetaMask).
   - Make sure the contract `DegenToken` is selected in the contract dropdown.
   - Provide the constructor parameters (e.g., the initial owner address).
   - Click the "Deploy" button and confirm the transaction in your wallet.

##Author

Arya390Akku


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

