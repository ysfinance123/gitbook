# Why do we choose Liquidity Pool Model

### Liquidity Pool Model v.s. Mint-Burn Model

There are two major shortcomings of most bridges: lack of privacy protection; inability to support native assets. By using the Liquidity Model, YS Transacotr solves the second problem.&#x20;

The problem is that the native assets of one blockchain cannot be easily transferred and used on another blockchain. An intermediate step is required: bridging. Bridging lets users transfer liquidity across chains in many different ways. Currently, however, there is no way to efficiently complete a bridge transaction. The process involves many different steps, requires a non-trivial understanding of how a given bridge protocol works, and can be expensive.

The difficulty stems in part from the Bridging Trilemma that developers face when designing a bridge. They must make a compromise between native asset transaction requirements, instant guaranteed finality, and unified liquidity. Most bridge designs favor sacrificing the use of native assets and instead utilize a wrapped token to replace the native token. The end result is typically a Lock-and-Mint or Burn-and-Redeem mechanism. In general, the way these approaches work is by requiring the user to deposit the native asset of their source chain into the bridge’s smart contract, at which time the bridge then mints a wrapped version of the asset (e.g. $ETH → $WETH) on the destination chain. This achieves instant guaranteed finality since assets are minted 1:1 on the destination chain. It also removes the risk of reversion due to lack of liquidity. Yet a critical issue with this method is that once a wrapped token is minted on the destination chain, the user must then manually convert it into a native asset on the destination chain.&#x20;







