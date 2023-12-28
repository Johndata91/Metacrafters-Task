# Metacrafters-Task

## Project Overview 
The smart contract for the vault has been deployed on my local Subnet named `johnSubnet`.

## Contract Details
- **Contract Address:** 0x5DB9A7629912EBF95876228C24A848de0bfB43A9
- **Network:** JohnSUBNET

## Vault Functionality
### 1. Deposit Function
Users have the ability to deposit ERC-20 tokens into the vault by invoking the deposit function. This function determines the number of shares to be minted based on the deposited amount and the current total supply of shares.

```solidity
function deposit(uint _amount) external
```

### 2. Withdraw Function
Users can withdraw their tokens from the vault by executing the withdraw function. The function calculates the withdrawal amount based on the number of shares burned and the current total supply of shares.

```solidity
function withdraw(uint _shares) external
```

### 3. ERC-20 Interface
The contract features an interface for ERC-20 functionality, offering fundamental token operations such as balance checking, token transfers, and approval for token transfers.

```solidity
interface IERC20 {
    // ERC-20 functions...
}
```

## Usage Guidelines
1. **Token Approval:** Before making a deposit, ensure that you have granted the contract permission to spend your ERC-20 tokens. Utilize the ERC-20 approve function to provide the necessary authorization.

2. **Deposit:** Execute the deposit function with the desired amount of tokens to mint the corresponding shares.

3. **Withdraw:** Invoke the withdraw function with the number of shares to burn, receiving the proportional amount of tokens in return.

4. **Monitor Balances:** Keep track of your token balances and shares to effectively manage deposits and withdrawals.
