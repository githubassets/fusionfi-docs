# Boardroom

## The Boardroom User Interface

![The Boardroom user interface](<../.gitbook/assets/Screenshot 2022-01-26 193115.png>)

Let's take a look at each element of the Boardroom user interface and what it means.

1. **NEXT EPOCH**\
   The amount of time remaining until the next epoch.
2. **CURRENT EPOCH**\
   The number of the current epoch.
3. **SPARK PEG (TWAP)**\
   The TWAP (time-weighted average price) of the SPARK peg. The Boardroom only mints new SPARK as rewards for REACTOR stakers when this value **is above 1.01** **at the end of the current epoch**.
4. **APR**\
   The yield for REACTOR stakers in the Boardroom **if the Boardroom was printing every epoch**. This calculation is based on **the last recorded print in the Boardroom**.
5. **REACTORS STAKED**\
   ****The total amount of REACTOR currently staked in the Boardroom.
6. **SPARK Earned**\
   ****The amount of SPARK you've earned as rewards for staking REACTOR in the Boardroom.
7. **REACTOR Staked**\
   The amount of REACTOR you currently have staked in the Boardroom.

### Boardroom Specifications

* Epoch duration: 6 hours
* Any interaction with the Boardroom (staking/unstaking REACTOR or withdrawing SPARK rewards) will **lock your staked REACTOR for 6 epochs and SPARK rewards for 3 epochs.**&#x20;
*   Distribution of SPARK during expansion (Boardoom printing):

    **75%** goes to Boardroom REACTOR stakers as rewards\
    **20%** goes to SPARK stakers (xSPARK)

    **5%** goes to DAO fund
* Epoch Expansion: The current expansion cap is based on the currently circulating SPARK supply (see [SPARK Distribution](spark-distribution.md) for details). If there are bonds to be redeemed, 65% of minted SPARK goes to the treasury until its sufficiently stocked to satisfy future bond redemption.

{% hint style="info" %}
Note that the Boardroom **does not** print any rewards for REACTOR stakers when the Boardroom TWAP < 1.01.
{% endhint %}

## Boardroom FAQ

### **1. Once RODSs are issued, does the Boardroom stop printing SPARK until we are above peg again?**

Staking REACTOR will only give you SPARK rewards when the price of SPARK is above the peg (10,000 SPARK to 1 ETH), but not when it is under the peg.

### **2. What happens if I interact with the Boardroom in any way? Are there any lockup periods?**

Yes, there are two lockup timers. One for SPARK rewards and one for staked REACTOR. **Any interaction with the Boardroom will reset both timers.** The lockup period for withdrawing SPARK rewards is **3 epochs (18 hours)**, or **6 epochs (36 hours)** to unstake your REACTOR.

### **3. Are the Boardroom rewards pro-rated by time? For example, if I stake three hours before the end of an epoch versus five hours before the end of an epoch, would I get different rewards?**

No, Boardroom rewards are determined by how much you have staked at the time of printing (i.e., at the end of one epoch and the start of the other). It doesn't matter if you stake three hours before or thirty seconds before the emissions occur.

### 4. If I remove my REACTOR from the Boardroom without first collecting my SPARK, will they be lost forever?

No, they will still be there to collect whenever you need.

### 5. The Boardroom APR dropped because we're in a "debt phase." What does that mean?

A debt phase takes place during expansion epochs that start after a contraction period where there are still RODS to be redeemed.

65% of expansion during a debt phase is allocated to the treasury fund to prepare for subsequent RODS redemption down the road. This amount is always reserved, regardless of whether RODS holders are redeeming bonds or not.

Once enough SPARK is sufficiently stocked in the treasury to satisfy the redemption of all circulating RODS, expansion rates will resume to normal.

### 6. If we're in a debt phase, how long will it last until the Boardroom continues printing as normal?

The debt phase will last as long as is necessary to adequately pay back outstanding RODS debt. Please keep in mind that the DAO will also need to collect a little extra, as there needs to be a cushion to cover the bonus premiums when people redeem RODS over peg.\
\
There's no exact way of calculating how many epochs it will take, since the protocol doesn't know exactly when people will redeem their RODS. The debt phase cannot end until the treasury has enough SPARK to cover the redemption of all outstanding RODSs plus a premium.

### 7. At the end of the epoch, the Boardroom did not print SPARK, but then no RODS(s) were issued either. Why?

There is a balanced state "at peg" when SPARK's TWAP is between 1.00 and 1.01, which results in no contraction or expansion of the circulating supply of SPARK. This is referred to as a **zen epoch**.

### 8. If SPARK continues to climb above the price of the peg, will that influence how long the debt phase lasts?

Depending on the price of SPARK, the Boardroom print will have to adjust to provide a buffer for any unclaimed RODS. As the price of SPARK climbs above the peg, more SPARK needs to be distributed to the treasury to account for RODS redemption plus premiums.

### 9. How can I figure out what my future SPARK rewards will be from the Boardroom?

Let's take a look at a simplified example for a _non-debt phase_: say you have 1 REACTOR staked out of 10 total REACTORs staked in the Boardroom. In this case, you will receive 10% of the total SPARK printed in the Boardroom.&#x20;

For this example we are assuming that there is a total circulating supply of 10,000 SPARK and the current expansion rate is at 4%, so a total of 400 SPARK will be printed in the Boardroom. Under the protocol's current rules, 75% of those newly printed SPARK will be distributed to REACTOR stakers in the Boardroom. (See the [SPARK Distribution](spark-distribution.md) page for more details on how SPARK is distributed within the protocol.)\
\
Therefore, you would get: ((0.04 _\*_ 10000) _\*_ 0.75) \* (1/10) = **30 SPARK**.\
\
Thus, the formula to calculate your rewards is as follows:\
((_ExpansionRate_ \* _CirculatingSPARKSupply)_ \* 0.75) \* (_YourReactorStake_ / _TotalReactorStaked_)

### 10. How long will it take for REACTOR to pay itself off from SPARK rewards based on current prices?

This will vary constantly as the APR in the Boardroom fluctuates, along with other variables such as the price of SPARK.

&#x20;For a quick estimation, however, you can do the following:

1. Take the total APR shown in the Boardroom and divide that by 365 to get the daily APR. (For this example we will say the daily APR is 5%.) 
2. Multiply that daily APR by the current market price of the total REACTOR you have staked to see what your daily rewards are. (In this example, we have 5 REACTOR, each worth $500, for a total amount staked of $2500. Your daily return in this case would be $2500 \* 0.05, which comes out to $125 per day.)
3. Take your initial buy-in price for REACTOR and divide it by your daily rewards. If you bought these 5 REACTOR at a higher price, say $700 for example, in the current market conditions you would recover your initial investment of $3500 in 3500/125 or 28 days.
