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

## `onAfterRebase()`

## `initialize(address underlying_, string name_, string symbol_, address oracle_)` (public)

ram underlying\_ The underlying ERC20 token address.

## `updateOracle(address oracle_)` (public)

heritdoc IButtonToken fu

## `decimals() → uint8` (external)

heritdoc IERC20Metadata fu

## `totalSupply() → uint256` (external)

heritdoc IERC20 fu

## `balanceOf(address account) → uint256` (external)

heritdoc IERC20 fu

## `scaledTotalSupply() → uint256` (external)

heritdoc IRebasingERC20 fu

## `scaledBalanceOf(address account) → uint256` (external)

heritdoc IRebasingERC20 fu

## `allowance(address owner_, address spender) → uint256` (external)

heritdoc IERC20 fu

## `totalUnderlying() → uint256` (external)

heritdoc IButtonWrapper fu

## `balanceOfUnderlying(address who) → uint256` (external)

heritdoc IButtonWrapper fu

## `underlyingToWrapper(uint256 uAmount) → uint256` (external)

heritdoc IButtonWrapper fu

## `wrapperToUnderlying(uint256 amount) → uint256` (external)

heritdoc IButtonWrapper fu

## `transfer(address to, uint256 amount) → bool` (external)

heritdoc IERC20 fu

## `transferAll(address to) → bool` (external)

heritdoc IRebasingERC20 fu

## `transferFrom(address from, address to, uint256 amount) → bool` (external)

heritdoc IERC20 fu

## `transferAllFrom(address from, address to) → bool` (external)

heritdoc IRebasingERC20 fu

## `approve(address spender, uint256 amount) → bool` (external)

heritdoc IERC20 fu

## `increaseAllowance(address spender, uint256 addedAmount) → bool` (external)

## `decreaseAllowance(address spender, uint256 subtractedAmount) → bool` (external)

## `rebase()` (external)

heritdoc IRebasingERC20 fu

## `mint(uint256 amount) → uint256` (external)

heritdoc IButtonWrapper fu

## `mintFor(address to, uint256 amount) → uint256` (external)

heritdoc IButtonWrapper fu

## `burn(uint256 amount) → uint256` (external)

heritdoc IButtonWrapper fu

## `burnTo(address to, uint256 amount) → uint256` (external)

heritdoc IButtonWrapper fu

## `burnAll() → uint256` (external)

heritdoc IButtonWrapper fu

## `burnAllTo(address to) → uint256` (external)

heritdoc IButtonWrapper fu

## `deposit(uint256 uAmount) → uint256` (external)

heritdoc IButtonWrapper fu

## `depositFor(address to, uint256 uAmount) → uint256` (external)

heritdoc IButtonWrapper fu

## `withdraw(uint256 uAmount) → uint256` (external)

heritdoc IButtonWrapper fu

## `withdrawTo(address to, uint256 uAmount) → uint256` (external)

heritdoc IButtonWrapper fu

## `withdrawAll() → uint256` (external)

heritdoc IButtonWrapper fu

## `withdrawAllTo(address to) → uint256` (external)

heritdoc IButtonWrapper fu
