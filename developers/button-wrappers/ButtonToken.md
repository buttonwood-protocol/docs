# ButtonToken

The ButtonToken is a rebasing wrapper for fixed balance ERC-20 tokens.

## Functionality

Users deposit the "underlying" (wrapped) tokens and are minted button (wrapper) tokens with elastic balances which change up or down when the value of the underlying token changes.

For example: Manny “wraps” 1 Ether when the price of Ether is $1800. Manny receives 1800 ButtonEther tokens in return. The overall value of their ButtonEther is the same as their original Ether, however each unit is now priced at exactly $1. The next day, the price of Ether changes to $1900. The ButtonEther system detects this price change, and rebases such that Manny’s balance is now 1900 ButtonEther tokens, still priced at $1 each.

The ButtonToken math is almost identical to Ampleforth's μFragments.

For AMPL, internal balances are represented using `gons` and

* internal account balance `_gonBalances[account]`
* internal supply scalar `gonsPerFragment = TOTAL_GONS / _totalSupply`
* public balance `_gonBalances[account] * gonsPerFragment`
* public total supply `_totalSupply`

In our case internal balances are stored as 'bits'.

* underlying token unit price `p_u = price / 10 ^ (PRICE_DECIMALS)`
* total underlying tokens `_totalUnderlying`
* internal account balance `_accountBits[account]`
* internal supply scalar `_bitsPerToken` `= TOTAL_BITS / (MAX_UNDERLYING*p_u)` `= BITS_PER_UNDERLYING*(10^PRICE_DECIMALS)/price` `= PRICE_BITS / price`
* user's underlying balance `_accountBits[account] / BITS_PER_UNDERLYING`
* public balance `_accountBits[account] * _bitsPerToken`
* public total supply `_totalUnderlying * p_u`

``

## API Documentation

## `validRecipient(address to)`

Validates that the address is a valid recipient for tokens:

* Is not the 0 address
* Is not the token contract's address

## `onAfterRebase()`

Modifier to perform a rebase before executing token transfers, deposits, or withdrawals. Refetches the latest price data and rebases the supply around the new price.

## `initialize(address underlying_, string name_, string symbol_, address oracle_)` (public)

Initializes the token contract with the given parameters.&#x20;

## `updateOracle(address oracle_)` (public)

Updates the oracle to the new oracle address.&#x20;

Only callable by the contract owner.

## `decimals() → uint8` (external)

Get the number of decimals of precision for this token. This is derived from the decimals of the underlying token.

## `totalSupply() → uint256` (external)

Get the current total supply of the token contract.

## `balanceOf(address account) → uint256` (external)

Get the current balance of the user.

## `scaledTotalSupply() → uint256` (external)

Get the current total supply of the token contract, scaled to the underlying amount. In other words, returns the total amount of collateral locked in the contract.

## `scaledBalanceOf(address account) → uint256` (external)

Get the current balance of the user, scaled to the underlying amount.

## `allowance(address owner_, address spender) → uint256` (external)

Returns the remaining number of tokens that `spender` will be allowed to spend on behalf of `owner` through `transferFrom`. This is zero by default.

## `totalUnderlying() → uint256` (external)

Returns the number of underlying collateral tokens stored in the contract.

## `balanceOfUnderlying(address who) → uint256` (external)

Returns the user's current balance in terms of the underlying collateral tokens.

## `underlyingToWrapper(uint256 uAmount) → uint256` (external)

Returns the equivalent number of wrapper tokens for a given underlying amount.

## `wrapperToUnderlying(uint256 amount) → uint256` (external)

Returns the equivalent number of underlying tokens for the given amount of wrapper tokens.

## `transfer(address to, uint256 amount) → bool` (external)

Moves `amount` tokens from the caller's account to `to`.

Returns a boolean value indicating whether the operation succeeded

## `transferAll(address to) → bool` (external)

Moves all of the caller's tokens to `to`.

Returns a boolean value indicating whether the operation succeeded

## `transferFrom(address from, address to, uint256 amount) → bool` (external)

Moves `amount` of tokens from `from` to `to` using the allowance mechanism.

`Amount` is deducted from the caller's allowance.

Returns a boolean value indicating whether the operation succeeded.

## `transferAllFrom(address from, address to) → bool` (external)

Moves all tokens from `from` to `to` using the allowance mechanism.

Returns a boolean value indicating whether the operation succeeded.

## `approve(address spender, uint256 amount) → bool` (external)

Sets `amount` as the allowance of `spender` over the caller's tokens.

Returns a boolean indicating whether the operatino succeeded

## `increaseAllowance(address spender, uint256 addedAmount) → bool` (external)

## `decreaseAllowance(address spender, uint256 subtractedAmount) → bool` (external)

## `rebase()` (external)

Fetch new price from the oracle and rebase the token's supply accordingly

## `mint(uint256 amount) → uint256` (external)

Mint `amount` wrapper tokens, taking the required number of collateral tokens to do so.

## `mintFor(address to, uint256 amount) → uint256` (external)

Mint `amount` wrapper tokens for `to`, taking the required number of collateral tokens to do so

## `burn(uint256 amount) → uint256` (external)

Burn `amount` wrapper tokens, returns the equivalent value of collateral tokens to the caller.

## `burnTo(address to, uint256 amount) → uint256` (external)

Burn `amount` wrapper tokens, returns the equivalent value of collateral tokens to `to`.

## `burnAll() → uint256` (external)

Burn all wrapper tokens held by caller, returns equivalent value of collateral tokens to caller.

## `burnAllTo(address to) → uint256` (external)

Burn all wrapper tokens held by caller, returns equivalent value of collateral tokens to `to`.

## `deposit(uint256 uAmount) → uint256` (external)

Deposit `uAmount` collateral tokens, minting the equivalent value of wrapper tokens to the caller.

## `depositFor(address to, uint256 uAmount) → uint256` (external)

Deposit `uAmount` collateral tokens, minting the equivalent value of wrapper tokens to `to`

## `withdraw(uint256 uAmount) → uint256` (external)

Withdraw `uAmount` collateral tokens, minting the equivalent value of wrapper tokens to the caller.

## `withdrawTo(address to, uint256 uAmount) → uint256` (external)

Withdraw `uAmount` collateral tokens, minting the equivalent value of wrapper tokens to `to`.

## `withdrawAll() → uint256` (external)

Withdraw all collateral tokens from the contract.

## `withdrawAllTo(address to) → uint256` (external)

Withdraw all collateral tokens from the contract, sending them to `to`.
