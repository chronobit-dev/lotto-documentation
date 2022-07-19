# Prize Details

## Prizes and Odds

The following table shows the expected prize and odds of a winning ticket with a certain count of consecutive matching numbers.

| Number of Consecutive Matching Numbers |         Expected Prize        |      Odds      |
| :------------------------------------: | :---------------------------: | :------------: |
|                    0                   |               0               |    1 / 1.07    |
|                    1                   |               0               |     1 / 17     |
|               2 (Bronze)               |    1/27171 of the pool size   |     1 / 273    |
|               3 (Silver)               |    1/5450 of the pool size    |    1 / 4,370   |
|                4 (Gold)                |     1/274 of the pool size    |   1 / 70,000   |
|               5 (Jackpot)              |    1/13.65 of the pool size   |  1 / 1,120,000 |
|            6 (Super Jackpot)           | 1/1.08355343 of the pool size | 1 / 16,800,000 |

Note that an increase in the number of purchased perpetual lottery tickets will **not** decrease the expected prize payouts per winning ticket. This is because as the number of perpetual lottery tickets goes up, so does the size of the lottery pool. What **will** happen as the number of perpetual tickets goes up is more total prize payouts and more winning tickets each week!

Look [here](../the-lottery-drawing.md) to see examples that identify how many consecutive matching numbers a given ticket has.

Look [here](broken-reference) to see the minimum prize for each blockchain lotto is running.

### The Price Of A Lottery Ticket

Tedlotto works by awarding you one perpetual lottery ticket for $25 tokens worth delegated in our validator. Another way of looking at this is that each week TedLotto uses a portion of the commission reward from your $25 token worth and sends it to the pool wallet.

Continuing with this perspective, an important note is that you will never lose money with this system, as we are not charging you more commission to have your tokens delegated with us and our commission is the average among all validators. This is to be fair to remaining validators so they can also secure the network as it is important that we all do.

Look [here](broken-reference) to see the price of each ticket currently. Please follow our [Twitter](https://twitter.com/tedcrypto\_) for any other announcements and changes to this and other prizes.

### Expected Prize Calculation

Unlike some lotteries which pay out a fixed prize based on a number of matches (i.e. a fixed $50 for a ticket with 3 consecutive matches), TedLotto pays out a variable amount depending on the pool size (and for the jackpots on number of winning tickets).  In the unlikely event of many fewer winning tickets than expected for a given week, each winner will receive a larger prize than expected. Similarly, in the unlikely event of many more winning tickets than expected for a given week, each winner will receive a smaller prize than expected.

Even so, we can calculate what the expected payout will be for a given number of matches and know that the actual payouts will hover around the expected payout. See the code below. Notice that it doesn't depend on the number of purchased perpetual tickets, but it does depend on the prize distribution.

```python
# Get lotto wallet balance
lottery_pool_size = get_lotto_wallet_balance

# Set proportions based on a matching chance and prize distribution
prize_proportions = [0, 0.0000019, 0.00000368, 0.00018349, 0.0036539, 0.07326951, 0.92288942,]

# For each proportion we calculate the rewards based on the pool size
expected_payouts = [lottery_pool_size * proportion for proportion in enumerate(prize_proportions)

# Print the expected payout sizes
print(expected_payouts)

```

And the corresponding output for a given wallet balance of 300.000 tokens

```
The expected payouts are:
- 0 tokens for tickets with 0 matches.
- 0 tokens for tickets with 1 matches.
- ~1.10 tokens for tickets with 2 matches.
- ~55.047 tokens for tickets with 3 matches.
- ~1096.16 tokens for tickets with 4 matches.
- ~21980.853 tokens for tickets with 5 matches.
- ~276866.826 tokens for tickets with 6 matches
```

