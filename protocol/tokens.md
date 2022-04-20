# Tokens

### SPARK - fusionfi.energy Token

![fusionfi.energy (SPARK)](<../.gitbook/assets/spark.png>)

Contract: [0xded](https://explorer.fuse.io/token/0xdead)

The SPARK token is designed to be used as a medium of exchange. The built-in stability mechanisms within the protocol aim to maintain SPARK's peg of 4,000 SPARK = 1 Ethereum (ETH) in the long run.&#x20;

{% hint style="warning" %}
Note that SPARK **actively pegs via an algorithm**, but that **does not mean** it will be valued at 4,000 SPARK to 1 ETH at all times as **it is not collateralized**. **SPARK is not to be confused for a crypto or fiat-backed stablecoin.**
{% endhint %}

### REACTOR - Spark Shares

![REACTOR](<../.gitbook/assets/reactor.png>)

Contract: [0xded](https://explorer.fuse.io/token/0xdead)

SPARK Shares (REACTOR) are one of the ways to measure the value of the Fusion Protocol and shareholder trust in its ability to consistently maintain SPARK close to peg. During epoch expansions the protocol mints SPARK and distributes it proportionally to all REACTOR holders who have staked their tokens in the [**Boardroom**](boardroom.md).

REACTOR has a **maximum total supply of 70,001** tokens distributed as follows:

1. _DAO Allocation: 5,500_ REACTOR vested linearly 12 months
2. _Team Allocation: 5,000_ REACTOR vested linearly over 12 months
3. _Remaining: 59,500_ REACTOR are allocated for incentivizing liquidity providers in two farming pools for 12 months
4. Initial mint: 1 REACTOR minted upon contract creation for the initial pool

### [RODS - Spark Bonds](bonds-mechanism.md)

![RODS](<../.gitbook/assets/rods.png>)

Contract: [0xded](https://explorer.fuse.io/token/0xdead)

The main purpose of SPARK Bonds (RODS) is to help incentivize fluctuations in the SPARK supply during epoch contraction periods. When the TWAP (time-weighted average price) of SPARK falls below 4,000 to 1 ETH, RODS are issued and can be bought with SPARK at the current price. Exchanging SPARK for RODS burns SPARK tokens, taking them out of circulation (deflation) and helps to get the price back up to peg. These RODS can be redeemed for SPARK when the price is above peg in the future, plus a premium based on how high above peg we currently are. This conversely creates inflation and subsequent sell pressure for SPARK when it is above peg, helping to push it back toward 4,000 SPARK to 1 ETH ratio.

{% hint style="info" %}
Contrary to early algorithmic protocols, RODS do not have expiration dates.
{% endhint %}

All RODS holders will be able to redeem their RODS for SPARK tokens as long as the treasury has a positive SPARK balance, which typically happens when the protocol is in epoch expansion periods.
