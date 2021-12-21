# Redemption Flow

![](<../../.gitbook/assets/Screenshot from 2021-12-21 10-23-37.png>)

The actual difference in risk profile between different tranches comes from the behavior of the bond at maturity. When the bond matures, it returns the collateral to the tranche holders, _in a waterfall fashion._ The most senior tranches (i.e. the A-tranche) get paid back _in full 1:1_ first, then the most junior tranche (the Z-tranche) gets paid back last, but receives all of the leftover funds.&#x20;



## Slight Decrease in Value

![](<../../.gitbook/assets/Untitled-2021-12-10-1349 (3).png>)

In the example above, the AMPL value has decreased a bit between bond creation and maturity. In this case, the following would happen upon maturity:

* A-tranches get paid back 1 AMPL per A-tranche, in full.
* B-tranches get paid back 1 AMPL per B-tranche, in full.
* Z-tranches get paid the rest, \~0.5 AMPL per Z-tranche

Any A- or B-tranche holders are entirely whole after this process, even though the value of AMPL dropped over the lifetime of the bond. Z-tranche holders suffer all of the value lost.&#x20;

## Increase in Value

![](<../../.gitbook/assets/Untitled-2021-12-10-1349 (6).png>)

In the example above, the AMPL value has increased a bit between bond creation and maturity. In this case, the following would happen upon maturity:&#x20;

* A-tranches get paid back 1 AMPL per A-tranche, in full.&#x20;
* B-tranches get paid back 1 AMPL per B-tranche, in full.&#x20;
* Z-tranches get paid the rest, \~1.2 AMPL per Z-tranche

Any A- or B-tranche holders are entirely whole after this process, but they do not get any of the benefit of the increase in AMPL value. Z-tranche holders receive all of the upside in return for their extra risk.

##
