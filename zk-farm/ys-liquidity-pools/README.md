---
description: This page introduces the mechanism behind Liquidity Pool V1.
---

# YS Liquidity Pools

{% hint style="info" %}
**YS Liquidity Pool (V1)**&#x20;

Supported Networks: Ethereum, Avalanche, Polygon

Supported Assets: USDT, USDC, DAI, WETH, WBTC

For each supported asset on each network, there is a dedicated liquidity pool.&#x20;
{% endhint %}

## YS Liquidity Provider Rewards

<figure><img src="https://lh4.googleusercontent.com/6E4Qi1oEdd1owBEp7ZSTv3KoXhaThczEQ739RM8F7ZGcnDvg-D11gl8qmqE9Fkes0k3WWlXD41tUxuALiWtDk8mzgBbOxRjbCpVJMMpqqzYThjwOHnomEZOduKLa1ImIjP2JT7nVrpQaZ6l_1bsXjpA1Hl6k5pMnCmPJovzAkiuAPe5YquYJtMbG-g" alt=""><figcaption></figcaption></figure>

**Protocol Fee Rewards technical specifications:**

For example: a user wants to send 10,000 USDT tokens using zk-Transfer.

Under the hood: when a user transfers 10,000 USDT from BNB Chain to Avalanche, the total amount of liquidity provision in the USDT pool on avalanche must be over 10K USDT, otherwise, the transaction will be partially reverted due to lack of liquidity on the target chain. When a user initiates a transfer, YS transactor would take a % as Protocol Fee Rewards which will be given to liquidity providers for each liquidity pool on the target chain (in this example will be given to LPs who provided USDT on Avalanche).

* Each liquidity provider’s reward is pro rata to the liquidity they provide relevant to the total liquidity size of the pool, as the rewards will be shared among all liquidity providers.&#x20;
* Protocol Fee Rewards = Transfer Fee\* Reward Parameter
* Reward time: Reward time will be dependent on the user's cross-chain transfer time.

#### **How to calculate the protocol fee APY?**&#x20;

$$
Protocol APR = (F / B) * 365 / N
$$

* F = aggregated protocol fees in N dasy for a particular token.&#x20;
* B = weighted average of LP balance in N days, calculated after each transaction, weighted by  (USD value of the transaction / aggregated USD value of all transactions in N days) amount of USDT / total amount of the cToken of USDT ) \* Yd / USDT \* My Liquidity）\* 365

