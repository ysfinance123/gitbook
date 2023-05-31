---
description: New SDK doc coming soon.
---

# Yellow Submarine SDK

### Introduction

`YS-SDK` is a set of SDK that can be integrated to any dApp so that they add privacy similar to the YS Gateway. ​For example, any DEX or lending platform may call the SDK before their withdrawal operation to prevent any public user to know the real withdraw addresses.&#x20;

### Quick Start Guide

> **Import SDK**

```javascript
// Use appropriate ways to importing the YS SDK
import { Sdk } from "ys-sdk";
const { Sdk } = require("ys-sdk");
```

> **Initiate SDK**

```javascript
import { Sdk } from "ys-sdk";
​
const sdkConfig = {
  hostUrl: "ys RPC",
  feeServerUrl: "API for Gas fee estimate",
  configServerUrl: "Configur server for network and tokens data",
  navticeExplorerUrl: "block explorer url",
  web3: "web3 provider",
};
​
// Initiating the SDK configuration
await Sdk.init(sdkConfig);
```

#### Chain IDS

* YS Chain: 0
* BSC: 1
* Avalanche: 2
* Polygon: 3
* Ropsten: 4 ​

#### Official ERC20 Addresses (Testnet)

* **USDT**

<table><thead><tr><th width="157">Chain Network</th><th width="425">Address</th><th width="111">Decimals</th><th>Source</th></tr></thead><tbody><tr><td>Avalanche</td><td>0x4e7ac4fB42a627439A9fA6BaE6582BCa4F0b6138</td><td>6</td><td></td></tr><tr><td>BSC</td><td>0x774C599C2e24C8007C90034Dcbc5022c24D4A3FD</td><td>6</td><td></td></tr><tr><td>Polygon</td><td>0x3AE966811705E80C49ca556120c0b7fa29B75360</td><td>6</td><td></td></tr><tr><td>Ropsten</td><td>0xc62E6a1573307FbbAF0422A0833010F76D6Edcd5</td><td>6</td><td></td></tr><tr><td>​</td><td></td><td></td><td></td></tr></tbody></table>

* **USDC**

<table><thead><tr><th width="221">Chain Network</th><th width="423">Address</th><th>Decimals</th><th>Source</th></tr></thead><tbody><tr><td>Avalanche</td><td>0x0676E2aDECe2b218eE036099288f2d69e3E42433</td><td>6</td><td></td></tr><tr><td>BSC</td><td>0xEA3321e26BeaAd0E25089ff066A333210AE86745</td><td>6</td><td></td></tr><tr><td>Polygon</td><td>0x0b0f79fFe93Cb8B1b9816ABDB4FbE04568d7F1eE</td><td>6</td><td></td></tr><tr><td>Ropsten</td><td>0x8D487e5579767bA3C8A671DAa97C3a7583C096b7</td><td>6</td><td></td></tr><tr><td>​</td><td></td><td></td><td></td></tr></tbody></table>

* **BUSD**

<table><thead><tr><th width="171">Chain Network</th><th width="430">Address</th><th width="182">Decimals</th><th>Source</th></tr></thead><tbody><tr><td>Avalanche</td><td>0x61345191271a78C63dacea72a00269Bf97BaaC03</td><td>18</td><td></td></tr><tr><td>BSC</td><td>0xB894F83a2020393a1E6a697541dD2bc52FD354D4</td><td>18</td><td></td></tr><tr><td>Polygon</td><td>0xEA26078B87AA8A9AF916e49e21c3D855A42BAae4</td><td>18</td><td></td></tr><tr><td>Ropsten</td><td>0x1a5c093D58c84D4FEa83a3d063E91a8166983205</td><td>18</td><td></td></tr><tr><td>​</td><td></td><td></td><td></td></tr></tbody></table>

* **DAI**

<table><thead><tr><th width="185">Chain Network</th><th width="449">Address</th><th width="170">Decimals</th><th>Source</th></tr></thead><tbody><tr><td>Avalanche</td><td>0x63Cc69F1650805d3Df7f670E15888924924dd230</td><td>18</td><td></td></tr><tr><td>BSC</td><td>0x23ec78CaB686Acf5A9e7747daD2194c8AAEe0d28</td><td>18</td><td></td></tr><tr><td>Polygon</td><td>0x621480577b60a0eA394D246610F3C37c81ab84C9</td><td>18</td><td></td></tr><tr><td>Ropsten</td><td>0x2C6A3fca9a7Dec2fBFe6824EBB18e24b0dcf07be</td><td>18</td><td></td></tr><tr><td>​</td><td></td><td></td><td></td></tr></tbody></table>

* **WETH**

<table><thead><tr><th width="183">Chain Network</th><th width="488">Address</th><th width="187">Decimals</th><th>Source</th></tr></thead><tbody><tr><td>Avalanche</td><td>0x59a228B91DE3137f9100073e303559CAf1889FFA</td><td>18</td><td></td></tr><tr><td>BSC</td><td>0x8B739134ad6eC92d016eCB8e9A0Acf90c4144C3D</td><td>18</td><td></td></tr><tr><td>Polygon</td><td>0xA56B9B5c52c1D59aDD05FEE85218c526c4034fc0</td><td>18</td><td></td></tr><tr><td>Ropsten</td><td>0x625201D5ED5D3c0EE4c9094e6ABd1B420D435cB1</td><td>18</td><td></td></tr><tr><td>​</td><td></td><td></td><td></td></tr></tbody></table>

* **WBTC**

<table><thead><tr><th width="187">Chain Network</th><th>Address</th><th>Decimals</th><th>Source</th></tr></thead><tbody><tr><td>Avalanche</td><td>0x142bD9B42e071BaF23eb85F7339b95a3EEf8534E</td><td>18</td><td></td></tr><tr><td>BSC</td><td>0xc2F2af435E8DcE654c09ef6AF551e8AFA07658fA</td><td>18</td><td></td></tr><tr><td>Polygon</td><td>0xf8c3dFa15C6ed967130eb3c6430D25F9389a4c24</td><td>18</td><td></td></tr><tr><td>Ropsten</td><td>0x71171d6f56c693CC4998b0ab110cE6E5E0310346</td><td>18</td><td></td></tr><tr><td>​</td><td></td><td></td><td></td></tr></tbody></table>

* **WBNB**

<table><thead><tr><th>Chain Network</th><th width="483">Address</th><th width="226">Decimals</th><th>Source</th></tr></thead><tbody><tr><td>Avalanche</td><td>0xc8C3b059F0f226f23A5A02dBbFC12ad08280010c</td><td>18</td><td></td></tr><tr><td>BSC</td><td>0xd3BC2740101c5D64F9352923445f083a7F189BF4</td><td>18</td><td></td></tr><tr><td>Polygon</td><td>0xC95a9B048fDa07a7f278d9a89FEb038f70c20bDf</td><td>18</td><td></td></tr><tr><td>Ropsten</td><td>0x19a09B22128Eee4FB408FbA4eaD81d9172b817dE</td><td>18</td><td></td></tr><tr><td>​</td><td></td><td></td><td></td></tr></tbody></table>

* **YES**

​

<table><thead><tr><th width="227">Chain Network</th><th width="538">Address</th><th width="210">Decimals</th><th>Source</th></tr></thead><tbody><tr><td>Avalanche</td><td>0xe5848b0b55d4b9aCaD60Cc4228d3031A991fee56</td><td>18</td><td></td></tr><tr><td>BSC</td><td>0xC9DF3596d22c4bce10573B41F00B24CdeA63CC1E</td><td>18</td><td></td></tr><tr><td>YS Chain</td><td>0x4456796B223CEb1D936AC1D4E2735Ba8B4157f86</td><td>18</td><td></td></tr><tr><td>Polygon</td><td>0x6cdB60E87E4F145D73f5e9822EB97D2102b778Be</td><td>18</td><td></td></tr><tr><td>Ropsten</td><td>0xc243b872F1be30a055Cc7CA187D8C8003dd834D9</td><td>18</td><td></td></tr><tr><td>​</td><td></td><td></td><td></td></tr></tbody></table>

### Cross Chain Swap Fee

​ The Base Fee: dynamically set based on gas used;  The Protocol Fee: 0.1% ​ The Fixed Fee covers the transfer's gas costs. ​ The Protocol Fee is proportional to the transfer amount. This fee is shared with Yellow Submarine LPs to incentivize them to contribute liquidity.

* Stages in which ONLY native token of YS chain are paid for the tx fee ​
  * The assets are bridged from any`EVM compatible chain` to YS UTXO Ledger
  * The assets are converted from 'Sealed Asset' to 'Transparent Asset' in the YS UTXO Ledger (leaving the private cycle) ​
* Stage in which the swap fee is cha. ​
  * The assets are converted from 'Transparent Asset' to 'Sealed Asset' in YS UTXO Ledger (entering the private cycle) ​

````javascript
  // Call this function to get estimated fees for `BAR to ABAR` conversion
  ledger.fra_get_minimal_fee_for_bar_to_abar();
​
  let feeInputs = ledger.FeeInputs.new();
  const feeAmount = BigInt(utxo.record.amount["NonConfidential"]);
  const txoRef = ledger.TxoRef.absolute(BigInt(feeSid)); // feeSid: sid for swap fee
  feeInputs = feeInputs.append2(
    feeAmount,
    txoRef,
    assetRecord,
    ownerMemo?.clone(),
    keypair
  );
  transactionBuilder.add_fee_bar_to_abar();
  ```
````

#### Bridging from `YS UTXO Ledger` to `YS Account Ledger`

```javascript
//Call this function to get estimated fees
ledger.fra_get_minimal_fee();
```



* **None of Source network and Destination network is YS Chain.**

```javascript
const provider = new Web3(
  new Web3.providers.HttpProvider(
    "https://data-seed-prebsc-1-s2.binance.org:8545"
  )
);
​
const contract = evm.contracts.pool(
  "0x.....", // pool contract address
  provider
);
​
// Obtain token decimals for fee calculation.
const tokenContract = evm.contracts.erc20(tokenAddress, provider);
const decimals = await tokenContract.methods.decimals().call();
​
const [minFee, fixedFee] = await Promise.all([
  contract.methods.minFee(tokenAddress).call(), // Get minimal fee
  contract.methods.fixedFee(tokenAddress).call(), // Get fixed fee
]);
​
const fixedFeeBN = new BigNumber(fixedFee).div(10 ** decimals);
​
const amountDecimals = 6;
const totalAmountBN = new BigNumber(amount)
  .multipliedBy(1 / (1 - +minFee / 10000))
  .plus(fixedFeeBN);
​
const roundDownByDecimals = (value, decimals) => {
  const [v1, v2] = value.split(".");
  return `${v1}.${
    v2?.slice(0, decimals) ?? new Array(decimals).fill("0").join("")
  }`;
};
​
return {
  percentage: `${(+minFee / 10000) * 100}`,
  fixedFee: roundDownByDecimals(fixedFeeBN.toString(10), decimals),
  totalFee: totalAmountBN.minus(amount).toFixed(amountDecimals, 1),
};
```

### Cross Chains Transaction

​ Using **YS-SDK** for a complete confidential cross chain transaction by the following steps, ​

* **(1) From `EVM compatible chain` to `YS UTXO Ledger`**

```javascript
/*
Parameters
  deckAddress: YS contract address
  tokenAddress: Erc20 Token address
  bridgeAddress: bridge contract address
  totalAmount: send amount
  recipientAddress: wallet account address
*/
​
// Approve YS contract
await evm.services.approveToken(tokenAddress, deckAddress, totalAmount);
​
return await evm.transfer.erc20ToBar({
  bridgeAddress,
  tokenAddress,
  destinationChainId: "0",
  tokenResourceId:
    "0x000000000000000000000000000000c76ebe4a02bbc34786d860b355f5111501", // Token Resource ID for transfering token
  tokenAmount: totalAmount,
  recipientAddress,
  tokenId: tokenId, // Erc20 Token ID: it's used to identify defferent tokens.
});
```

* **(2) Converting Assets from 'Transparent Asset' to 'Sealed Asset' in the YS Chain (entering the private cycle）**

```javascript
import { ys } from "ys-sdk";
​
/**
Parameters
  sids: consumable utxo sids
*/
const walletWrap = await ys.keypair.getWallet();
ys.transfer.barToAbar(walletWrap, sids);
```

* **(3) Converting Assets from  `Transparent Asset` to `Sealed Asset`  in the YS Chain （leaving the private cycle）**

```javascript
import { ys } from "ys-sdk";
​
/**
Parameters
  commitments: consumable Abar utxo sids
*/
const walletWrap = await ys.keypair.getWallet();
ys.transferabarToBar(
  walletWrap.anonWallet,
  walletWrap.walletEnd,
  commitments
);
```

* **(4) Bridging from `YS UTXO Ledger` to `EVM Compatible chain`(BSC、ETH、Polygon, etc.)**

```javascript
const lowLevelData = await web3.createLowLevelData(
  "1", // ID for the destination network. 1 is BSC Testnet.
  "100", // token amounts including swap fees.
  `${tokenId}`, // Erc20 Token ID: it's used to identify defferent tokens.
  recipientAddress, //  recipient's address
  funcName // function name: 'withdrawFRA' for FRA token. And 'withdrawERC20' for other customized tokens.
);
finalAmount = totalAmount;
await ys.transfer.barToEVM(
  walletWrap.walletEnd,
  "80", // token amounts excluding swap fees.
  relayer, // if both source and destination network are YS, we use 'ys.columbus.chain301'. In other cases, we use 'ys.columbus.chain501'.
  assetCode, // YRC-20 Token address
  lowLevelData.substring(2),
  false
);
```

### Verify Cross Chain Transactions

* **(1) Verify EVM Deposit Transaction**

```javascript
try {
  // Pass Cross-chain transaction (1)'s Hash, and get the blockNumber.
  const { blockNumber } = await new Web3(Provider).eth.getTransaction(txnHash);
  const eventLogs = await evm.contracts
    .bridge(bridge, Provider)
    .getPastEvents("Deposit", { fromBlock: blockNumber, toBlock: blockNumber });
  const eventLog = eventLogs.find((log) => log.transactionHash === txnHash);
  let counter = 15;
  let proposalEvents = [];
  if (eventLog) {
    while (!proposalEvents.length && counter > 0) {
      await sleep(20000);
      counter--;
      // Pass the value on YS Account Ledger.
      proposalEvents = await evm.contracts
        .bridge(bridge, Provider)
        .getPastEvents("ProposalEvent", {
          fromBlock: 0,
          filter: { depositNonce: eventLog.returnValues.depositNonce },
        });
    }
​
    return {
      error: proposalEvents.length
        ? null
        : new Error(
            `check bridge pass failed - depositNonce: ${eventLog.returnValues.depositNonce}`
          ),
    };
  }
} catch (error) {
  return { error };
}
```

* **(2) Verify Transaction on UTXO**

```javascript
// Pass BAR's wallet address
await ys.services.waitUtxoEnough(publickey, 1);
```

* **(3) Verify Withdawl on EVM**

```javascript
const fromBlock = await new Web3(Provider).eth.getBlockNumber();
const contract = evm.contracts.erc20(token, Provider);
let transferLogs = await contract.getPastEvents("Transfer", {
  filter: { to: toAddress },
  fromBlock,
});
let counter = 20;
while (!transferLogs.length && counter > 0) {
  await sleep(30000);
  counter--;
  transferLogs = await contract.getPastEvents("Transfer", {
    filter: { to: toAddress },
    fromBlock,
  });
}
if (transferLogs.length) {
  console.log({ txnHash: transferLogs[0].transactionHash });
}
```
