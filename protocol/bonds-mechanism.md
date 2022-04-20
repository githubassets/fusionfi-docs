# Bonds (RODS)

![The "Pit", where you can interact with the protocol's bonding mechanism](<../.gitbook/assets/image (9).png>)

### What are RODS (Bonds)?

Bonds are unique tokens that can be utilized to help stabilize SPARK price around peg (10,000 SPARK = 1 ETH) by reducing the circulating supply of SPARK if the TWAP (time-weighted average price) goes below peg.

### When can I buy RODS (Bonds)?

RODS can be purchased only during periods of supply contraction and when the TWAP of SPARK is below 1.

At the beginning of every new epoch during contraction periods, RODSs are issued in the amount of 3% of SPARK's circulating supply, with a max debt amount of 35%. This means that if bonds reach 35% of the circulating supply of SPARK, no more bonds will be issued.

{% hint style="info" %}
Note that during a zen epoch (when an epoch ends with a TWAP between 1.0 - 1.01), **no RODS will be issued, even though the Boardroom does not print.**
{% endhint %}

{% hint style="danger" %}
RODS TWAP (time-weighted average price) is based on the SPARK TWAP from the previous epoch as it ends. In other words, the SPARK TWAP is real-time but the RODS TWAP is not.
{% endhint %}

### Where can I buy RODS (Bonds)?

You can buy RODSs if any are available through [WEBSITEHERE](https://WEBSITEHERE/bond) in the [Pit](https://WEBSITEHERE/bond). Anyone can buy as many RODSs as they want as long as they have enough SPARK to pay for them.

There is a limit of available RODSs per epoch during contraction periods (3% of SPARK's current  circulating supply), and are sold first-come-first-serve.

### Why should I buy RODS (Bonds)?

The first and most important reason to buy RODS is that they help to maintain the peg, but they are not the only measure in place to keep the protocol on track.&#x20;

RODSs don't have an expiration date, so you can view them as an investment in the long-term health of the protocol to be redeemed for a premium at a later date.

#### Incentives for Holding RODS

The idea is to reward RODS buyers for helping the protocol, while also protecting the protocol from being manipulated by big players.

So after you buy RODS using SPARK, you have two possible ways to get your SPARK back:

1. Sell back your RODS for SPARK **while the peg is between 1 - 1.1** (10,000 SPARK = 1 ETH) with no redemption bonus. This is in place to prevent an instant dump as soon as peg is recovered.
2. Sell back your RODS for SPARK **while the peg is above 1.1** (10,000 SPARK = 1 ETH) with a bonus redemption rate.

The longer you hold, the more both the protocol and you benefit from RODS.

{% hint style="success" %}
Example:

1. When SPARK = 0.8, burn 1 SPARK to get 1 RODS (RODS price = 0.8)
2. When SPARK = 1.15, redeem 1 RODS to get 1.105 SPARK (RODS price = 1.27)&#x20;
{% endhint %}

So, which one is better?

If I buy SPARK at 0.8, and hold it until 1.15 and then sell, I'm getting +$0.35 per SPARK.

But, if I buy SPARK at 0.8, burn it for RODS, and redeem it at 1.15, I'm getting 1.105 SPARK \* 1.15 (SPARK current price) = 1,271 (+$0.47) per RODS redeemed.

But, what if getting back to peg is taking too long?

We will adjust our use cases to have different behaviors on contraction and expansion periods to benefit both SPARK and RODS holders when needed.

### What is the formula to calculate the redemption bonus for RODS?

To encourage the redemption of RODS for SPARK when SPARK's TWAP > 1.1 and in order to incentivize users to redeem bonds at a higher price, RODS redemption is designed to be more profitable with a higher SPARK TWAP value. The RODS to SPARK ratio is 1:R, where R can be calculated using the formula as shown below:

$$
R=1+[(SPARKtwapprice)-1)*coeff)]
$$

$$
coeff = 0.7
$$

### When can I swap RODS for a premium?

You can only redeem RODSs for a premium when the previous epoch's TWAP is greater than 1.1.
