# Market Making

Currently there is no UI interface for market making. However, it is possible via a couple manual steps.



## Deposit Collateral

The first step of the process is to deposit collateral for TRANCHE tokens. To do this, you can use the `LP` tab on [https://app.mooncake.prl.one](https://app.mooncake.prl.one)

#### Select USDT amount

Firstly, you need to select the amount of AMPL that you want to deposit.&#x20;

![](<../../.gitbook/assets/Screenshot from 2021-12-17 14-23-47.png>)

Then click `Deposit Liquidity` to start the transaction flow.&#x20;

![](<../../.gitbook/assets/Screenshot from 2021-12-17 14-25-37.png>)

Confirm the transaction with your wallet, and you will receive some AMPL-Tranche tokens in return. Now we can use these to deposit liquidity on UniswapV3!





## Provide Liquidity on Uniswap

The main borrowing pools on Uniswap are TRANCHE-A / USDT and TRANCHE-B / USDT. In order to lend, you will need to supply liquidity to these pools.&#x20;

1. Acquire some USDT of equal value to your A and B tranche tokens
2. Go to app.uniswap.org, click "Pool"
3. Click "New Position"
4. Enter TRANCHE-A as the first token, and USDT as the second token
5. Enter the amount of liquidity you want to add, and finish going through the wizard flow
6. Repeat steps 3-5 for your TRANCHE-B tokens.
