## `IButtonToken`






### `oracle() → address` (external)



The reference to the oracle which feeds in the
     price of the underlying token.

### `lastPrice() → uint256` (external)



Most recent price recorded from the oracle.

### `updateOracle(address oracle_)` (external)



Update reference to the oracle contract and resets price.


### `initialize(address underlying_, string name_, string symbol_, address oracle_)` (external)



Contract initializer


### `OracleUpdated(address oracle)`



Log to record changes to the oracle.


