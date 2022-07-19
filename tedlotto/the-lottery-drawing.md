# The Lottery Drawing

## Overview

The drawing happens once per week on different days and times based on the Tedcrypto blockchain configuration. After the lottery is drawn, the prize is distributed among the winning ticket holders according to the prize distribution algorithm.

## Claiming Lottery Winnings

After winning a lottery (good luck!) You will be able to claim it from your prizes dashboard.\
\
Once you have confirmed your claim it will start an unbounding process of these tokens from our validator to your wallet. You will only need to do this once, the system will be in charge of unbounding the tokens and sending them to the right address (your wallet) once the tokens are available in the wallet.\
\
Unbounding periods change from blockchain to blockchain, we will make it clear from your claiming pane. You will see a number of days counting down and then a success message saying the tokens were sent your way.\
\
Since these claims impact the pool size you should do them BEFORE THE NEXT DRAW! Not doing it in time might lock the claim and you won't be able to claim your tokens at all.  \
\
Every week after each draw we will post a summary of the draw, amount of winners and the total prize on [Twitter](https://twitter.com/tedcrypto\_), [Discord](https://discord.gg/snPBETGTBj) and [Telegram](https://t.me/TedcryptoOfficial). Please pay close attention to these channels and visit often your prizes dashboard.

{% hint style="warning" %}
This process is not ideal but is the best one for Tedlotto as explained in the [Introduction](the-lottery-drawing.md#overview). We are working hard to make it a more pleasant experience for our delegators!
{% endhint %}

## How It Works

When the lottery is drawn, a "perfect winning ticket" is randomly generated. Then, the lottery pool is distributed among winning ticket holders.&#x20;

A ticket is a winning ticket if at least its first two numbers match the first two numbers of the perfect winning ticket. Among winning tickets, there are **five tiers**: bronze, silver, gold, jackpot, super jackpot. Ticket placement into these tiers is best understood through an example. For this example, say the winning ticket is 537801:

* **2 Sequential Matches (Bronze)** - any ticket starting with 53XXXX such as 535840
* **3 Sequential Matches (Silver)** - any ticket starting with 537XXX such as 537012
* **4 Sequential Matches (Gold)** - any ticket starting with 5378XX such as 537810
* **5 Sequential Matches (Jackpot)** - any ticket starting with 53780X such as 537802
* **6 Sequential Matches (Super Jackpot)** - any ticket that exactly matches the perfect winning ticket

The payouts of the corresponding tiers of winning tickets are as follows:

* **Bronze: 1/27171 of the pool size**
* **Silver: 1/5450 of the pool size**
* **Gold: 1/274 of the pool size**
* **Jackpot: 1/13.65 of the pool size**
* **Super Jackpot: 1/1.08355343 of the pool size**

#### Implementation Details

* It should be noted that in the case of multiple delegators holding the same winning ticket, all of the corresponding deposits win equally. This means that if you win with the jackpot ticket, but that the jackpot ticket is also held by one other depositor, each of you will receive 50% of the jackpot payout.
* If there are no tickets of a given category (i.e. no jackpot ticket holders) the corresponding % of the pot gets rolled forward to the lottery pool for the next lottery.

### Fairness

The winning ticket is obtained following a **decentralized, verifiable, and non-predictable process.** This allows Tedlotto to deliver a fair lottery without relying on any central party. Nobody, including the team, can predict the winning ticket combination.

### Lottery Drawing Execution

When the lottery is being drawn (which happens once a week for every chain), delegating more tokens might not be accounted for when doing it close to the draw time and no tickets would have been generated in due time. Prizes are allocated automatically after the draw is known making it impossible to generate a ticket in those miliseconds from draw to selecting winners.
