---
description: Users deposit collateral and receive "Tranche" tokens. How does this work?
---

# Deposit Flow

![Diagram of a user depositing into an AMPL bond in return for tranche tokens](<../../.gitbook/assets/Screenshot from 2021-12-21 10-16-08.png>)



In order to tranche their collateral, a user can deposit it into a ButtonBond. The bond goes through its configured _tranche ratios_, minting tranche tokens proportional to the ratio and the amount of collateral deposited. For example:

* _Tranche ratios_: 20/30/50
* _Collateral_: AMPL
* User deposits 1000 AMPL
  * User receives (1000 \* 0.2) = 200 AMPL-A Tranche
  * User receives (1000 \* 0.3) = 300 AMPL-B Tranche
  * User receives (1000 \* 0.5) = 500 AMPL-Z Tranche



![](<../../.gitbook/assets/Untitled-2021-12-10-1349 (2).png>)

After this interaction, the user's position value is still equivalent to holding their original AMPL. However, they now have separate assets which represent different parts of AMPL's risk:

* The A-tranche represents the safest 20% of AMPL's value
* The B-tranche represents the middle 30% of AMPL's value
* The Z-tranche represents the top 50% of AMPL's value _and_ all of its future upside

The user can now sell some of these tranches to change their risk profile.&#x20;
