---
description: >-
  Learning materials about elastic supply assets, and the ButtonToken and
  UnButtonToken wrappers
---

# Elastic Supply Assets

Elastic supply assets (AKA rebasing assets) were originally constructed by [Ampleforth](https://www.ampleforth.org) as a mechanism to provide stable price, without losing exposure to value gains. Changes in the value of the asset are exposed as changes to the asset's _supply_, rather than the asset's _price_. 

This mechanism has a very nice quality in that it allows for stable contracts. For example (taken from the AMPL website):

> Imagine Evan and Micah enter into a bet:\
> \
> _"If the Lakers make it to the 2022 NBA conference finals, Micah will pay Evan 10 coins. Otherwise, Evan will pay Micah 10 coins."_
>
> We would not want to denominate this bet using Bitcoin, because Bitcoin's price volatility makes for an unstable contract obligation.

Rebasing assets' price stability make them great assets for contract denomination.

## Clean Integrations

Another very important benefit of rebasing assets is that they naturally _abstract price information_ away from integrations. 

For example, a traditional DeFi lending platform like Aave needs a complex oracle system to calculate collateralization and relative values of assets. This adds extra complexity and risk to the system - If the oracle goes wrong, users could be wrongfully liquidated and pools could be drained.

Lending applications build with rebasing assets don't actually need price data - they only need access to the balances of the asset. Value is expressed directly in the contract's changing balance - the price can always be assumed to be stable and around $1.  

## Buttonwood Rebasing Tokens

Buttonwood extends this concept with the `ButtonToken` - an asset that can turn any crypto-asset into a rebasing asset, as long as it has a solid price-feed oracle. 

{% content-ref url="buttontoken.md" %}
[buttontoken.md](buttontoken.md)
{% endcontent-ref %}

Buttonwood also created the `UnbuttonToken` - the inverse of the `ButtonToken`. It turns elastic supply assets into fixed-supply assets. 

{% content-ref url="unbuttontoken.md" %}
[unbuttontoken.md](unbuttontoken.md)
{% endcontent-ref %}
