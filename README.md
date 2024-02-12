## Solidity Token Vault and ERC20

Contained within this repository are two Solidity smart contracts: `Vault` and `ERC20`. These contracts are designed to facilitate the creation of a token vault and a basic ERC-20 token, respectively.

## ERC20 Token Contract (`ERC20.sol`)

The `ERC20` contract serves as a straightforward implementation of the ERC-20 standard, enabling users to create and manage fungible tokens on the Ethereum blockchain. Here are some salient details:

- **Name:** Yashwanth Reddy
- **Symbol:** YR
- **Decimals:** 18

### Functions:

1. **Transfer:**
   - Moves a specified amount of tokens from the sender's account to the recipient's account.
   ```solidity
   function transfer(address recipient, uint amount) external returns (bool);
   ```

2. **Approve:**
   - Authorizes a spender to expend a specific amount of tokens on behalf of the owner.
   ```solidity
   function approve(address spender, uint amount) external returns (bool);
   ```

3. **Transfer From:**
   - Transfers a specified amount of tokens from the owner's account to the recipient's account, given approval.
   ```solidity
   function transferFrom(address sender, address recipient, uint amount) external returns (bool);
   ```

4. **Mint:**
   - Permits the owner to generate new tokens.
   ```solidity
   function mint(uint amount) external;
   ```

5. **Burn:**
   - Enables the owner to eliminate a specified amount of tokens.
   ```solidity
   function burn(uint amount) external;
   ```

## Token Vault Contract (`Vault.sol`)

The `Vault` contract serves as a secure repository for holding ERC-20 tokens. Users can deposit and withdraw tokens, with the contract handling the issuance and burning of vault shares automatically.

### Functions:

1. **Deposit:**
   - Enables users to deposit ERC-20 tokens into the vault and receive vault shares in return.
   ```solidity
   function deposit(uint amount) external;
   ```

2. **Withdraw:**
   - Allows users to withdraw tokens from the vault by providing vault shares.
   ```solidity
   function withdraw(uint shares) external;
   ```

## Usage:

1. Deploy the `ERC20` contract to establish a new ERC-20 token.
2. Deploy the `Vault` contract, passing the address of the ERC-20 token to the constructor.
3. Interact with the ERC-20 token and Vault contracts using standard ERC-20 functions and the custom functions defined in the `Vault` contract.

## Author

Yashwanth Reddy

## Contact

sreddy874690@gmail.com
