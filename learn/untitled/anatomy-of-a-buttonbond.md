# Anatomy of a ButtonBond

The _tranche_ protocol is enabled by collateralized, zero-coupon, liquidation-free _bonds_. These bonds are very configurable and have the following parameters:

* **Collateral asset**: The asset which we are tranching. Its price volatility is what generates the risk that is distributed from senior tranche holders to junior tranche holders.
* **Maturity date:** These bonds _mature_ after some period of time. After the maturity date passes, the price changes of the _collateral asset_ are settled among the holders of tranche tokens. This essentially means that holders of tranche tokens are making a bet about the price changes of the collateral _between now and maturity_.&#x20;
* **Tranche ratios:** These define the way that risk is transferred from more senior tranches to more junior tranches. They are generally denoted in terms of percent, i.e. a "20/30/50" bond represents a 20% A-tranche, 30% B-tranche and 50% Z-tranche.&#x20;
