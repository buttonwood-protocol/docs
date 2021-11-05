## `IButtonWrapper`






### `mint(uint256 amount) → uint256` (external)

Transfers underlying tokens from {msg.sender} to the contract and
        mints wrapper tokens.




### `mintFor(address to, uint256 amount) → uint256` (external)

Transfers underlying tokens from {msg.sender} to the contract and
        mints wrapper tokens to the specified beneficiary.




### `burn(uint256 amount) → uint256` (external)

Burns wrapper tokens from {msg.sender} and transfers
        the underlying tokens back.




### `burnTo(address to, uint256 amount) → uint256` (external)

Burns wrapper tokens from {msg.sender} and transfers
        the underlying tokens to the specified beneficiary.




### `burnAll() → uint256` (external)

Burns all wrapper tokens from {msg.sender} and transfers
        the underlying tokens back.




### `burnAllTo(address to) → uint256` (external)

Burns all wrapper tokens from {msg.sender} and transfers
        the underlying tokens back.




### `deposit(uint256 uAmount) → uint256` (external)

Transfers underlying tokens from {msg.sender} to the contract and
        mints wrapper tokens to the specified beneficiary.




### `depositFor(address to, uint256 uAmount) → uint256` (external)

Transfers underlying tokens from {msg.sender} to the contract and
        mints wrapper tokens to the specified beneficiary.




### `withdraw(uint256 uAmount) → uint256` (external)

Burns wrapper tokens from {msg.sender} and transfers
        the underlying tokens back.




### `withdrawTo(address to, uint256 uAmount) → uint256` (external)

Burns wrapper tokens from {msg.sender} and transfers
        the underlying tokens back to the specified beneficiary.




### `withdrawAll() → uint256` (external)

Burns all wrapper tokens from {msg.sender} and transfers
        the underlying tokens back.




### `withdrawAllTo(address to) → uint256` (external)

Burns all wrapper tokens from {msg.sender} and transfers
        the underlying tokens back.




### `underlying() → address` (external)





### `totalUnderlying() → uint256` (external)





### `balanceOfUnderlying(address who) → uint256` (external)





### `underlyingToWrapper(uint256 uAmount) → uint256` (external)





### `wrapperToUnderlying(uint256 amount) → uint256` (external)






