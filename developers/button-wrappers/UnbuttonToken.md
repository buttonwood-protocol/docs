# UnbuttonToken



The UnbuttonToken wraps elastic balance (rebasing) tokens like AMPL, Chai and AAVE's aTokens, to create a fixed balance representation.

The ratio of a user's balance to the total supply represents their share of the total deposit pool.



## API Documentation

## `initialize(address underlying_, string name_, string symbol_, uint256 initialRate)` (public)

Initializes the token with the given parameters.

## `mint(uint256 amount) → uint256` (external)

Mints the given amount of Unbutton tokens for the user. Transfers an equivalent value of underlying tokens from the user to the contract.

## `mintFor(address to, uint256 amount) → uint256` (external)

Mints the given amount of Unbutton tokens for `to`. Transfers an equivalent value of underlying tokens from the caller to the contract.

## `burn(uint256 amount) → uint256` (external)

Burns the given amount of Unbutton tokens from the caller. Transfers an equivalent value of underlying tokens from the contract to the caller.

## `burnTo(address to, uint256 amount) → uint256` (external)

Burns the given amount of Unbutton tokens from the caller. Transfers an equivalent value of underlying tokens from the contract to `to`.

## `burnAll() → uint256` (external)

Burns all Unbutton tokens from the caller. Transfers an equivalent value of underlying tokens from the contract to the caller.

## `burnAllTo(address to) → uint256` (external)

Burns all Unbutton tokens from the caller. Transfers an equivalent value of underlying tokens from the contract to `to`.

## `deposit(uint256 uAmount) → uint256` (external)

Deposit the given number of underlying tokens from the caller to the contract. Mints an equivalent value of Unbutton tokens to the caller.

## `depositFor(address to, uint256 uAmount) → uint256` (external)

Deposit the given number of underlying tokens from the caller to the contract. Mints an equivalent value of Unbutton tokens to `to`.

## `withdraw(uint256 uAmount) → uint256` (external)

Withdraw the given number of underlying tokens from the contract. Transfers an equivalent value of Unbutton tokens from the caller to the contract.

## `withdrawTo(address to, uint256 uAmount) → uint256` (external)

Withdraw the given number of underlying tokens to `to` from the contract. Transfers an equivalent value of Unbutton tokens from the caller to the contract.

## `withdrawAll() → uint256` (external)

Withdraw caller's entire balance of underlying tokens. Transfers an equivalent value of Unbutton tokens from the caller to the contract.

## `withdrawAllTo(address to) → uint256` (external)

Withdraw caller's entire balance of underlying tokens for `to`. Transfers an equivalent value of Unbutton tokens from the caller to the contract.

## `totalUnderlying() → uint256` (external)

The total number of underlying tokens held by the contract.

## `balanceOfUnderlying(address owner) → uint256` (external)

Returns `owner`'s balance in terms of the underlying token.

## `underlyingToWrapper(uint256 uAmount) → uint256` (external)

Returns the equivalent value of Unbutton tokens for the given amount of underlying tokens.

## `wrapperToUnderlying(uint256 amount) → uint256` (external)

Returns the equivalent value of Unbutton tokens for the given amount of underlying tokens.
