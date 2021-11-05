# ButtonToken

The `ButtonToken` is an ERC20 _wrapper_. It takes an underlying asset and creates a new asset which rebases to $1/token while tracking the value of the underlying token.  

There will be an instance per underlying asset, for example:

* buttonETH: An asset where each token is $1, but the value tracks the price of ETH.
* buttonBTC: An asset where each token is $1, but the value tracks the price of BTC.

\---

Example: 

* A user deposits 1 ETH into buttonETH at a current price of $4000. They receive 4000 buttonETH tokens, each worth $1. 
* The price of ETH increases to $6000. The user will now have 6000 buttonETH tokens, each worth $1. 
* The price of ETH decreases to $3000. The user will now have 3000 buttonETH tokens, each worth $1. 

As you can see, the user's _total wallet balance_ remains equivalent to holding the underlying tokens. However, their tokens now have a stable price and are much more fit for creating contracts and interacting with the Buttonwood ecosystem. 

 
