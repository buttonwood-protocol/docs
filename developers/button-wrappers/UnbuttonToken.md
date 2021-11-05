## `UnbuttonToken`

/**


The UnbuttonToken wraps elastic balance (rebasing) tokens like
     AMPL, Chai and AAVE's aTokens, to create a fixed balance representation.

     The ratio of a user’s balance to the total supply represents
     their share of the total deposit pool.

/
c


### `initialize(address underlying_, string name_, string symbol_, uint256 initialRate)` (public)

/ @param underlying_ The underlying ERC20 token address.




### `mint(uint256 amount) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `mintFor(address to, uint256 amount) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `burn(uint256 amount) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `burnTo(address to, uint256 amount) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `burnAll() → uint256` (external)

/ @inheritdoc IButtonWrapper



### `burnAllTo(address to) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `deposit(uint256 uAmount) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `depositFor(address to, uint256 uAmount) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `withdraw(uint256 uAmount) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `withdrawTo(address to, uint256 uAmount) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `withdrawAll() → uint256` (external)

/ @inheritdoc IButtonWrapper



### `withdrawAllTo(address to) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `totalUnderlying() → uint256` (external)

/ @inheritdoc IButtonWrapper



### `balanceOfUnderlying(address owner) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `underlyingToWrapper(uint256 uAmount) → uint256` (external)

/ @inheritdoc IButtonWrapper



### `wrapperToUnderlying(uint256 amount) → uint256` (external)

/ @inheritdoc IButtonWrapper




