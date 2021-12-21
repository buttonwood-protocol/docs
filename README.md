---
description: Buttonwood is rebuilding the DeFi stack from first principles
---

# Buttonwood

Complex systems become much easier to reason about when they can be formalized and broken down into a set of primitive arguments and a set of operations over those arguments.

![](<.gitbook/assets/Screenshot from 2021-12-21 09-42-17.png>)

DeFi takes this concept to the extreme, as it allows for these composition relationships to be codified and openly built upon.

## Tranching

Buttonwood is built upon the insight that there is a very important operation currently missing from the DeFi ecosystem: _tranching_.&#x20;

Tranching in this context is to split some asset up into portions by risk. It turns out that most financial products are actually just [some form of tranching](https://www.bloomberg.com/opinion/articles/2021-10-07/matt-levine-s-money-stuff-looking-for-tether-s-money), for example:

* Ownership of a business is broken down into debt and equity.
  * Debt-holders own a senior (safe) tranche of the business. They always get paid out first, before equity holders. However, their upside is limited to the debt + some interest.&#x20;
  * Equity-holders own a junior (risky) tranche of the business. They get paid out last, if the business is sold or goes public. In return for this extra risk, they are rewarded with all of the upside that the business generated.
* Home mortgages are have the lender and the borrower (home purchaser)
  * The lender has a senior claim to the house. If the borrower stops making payments, the lender can repossess the home and sell it to make back their losses. If the borrower sells the home with a balance on the mortgage, the lender gets paid back with the proceeds first.
  * The borrower has a junior claim to the house. If the house is sold for a profit, they get all of the profit after paying back the lender. If it is sold for a loss, they incur the loss.&#x20;



## Buttonwood DeFi

Buttonwood has generalized this concept with its new DeFi primitive: [Tranche](learn/untitled/). From this primitive, Buttonwood plans to rebuild a wide variety of financial products in a simple, robust, and composable way:

* Bond markets
* Liquidation-free, fixed-rate lending: [Mooncake](user-guides/borrow-app/)
* Options markets
* Yield splitting assets
* And more :)



## Where to next?

Detailed explanations about _Tranche_

{% content-ref url="learn/untitled/" %}
[untitled](learn/untitled/)
{% endcontent-ref %}



User guide for [Mooncake](https://mooncake.prl.one)

{% content-ref url="user-guides/borrow-app/" %}
[borrow-app](user-guides/borrow-app/)
{% endcontent-ref %}
