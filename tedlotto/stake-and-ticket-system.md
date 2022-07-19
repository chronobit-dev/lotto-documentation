# Stake and Ticket System

{% hint style="info" %}
For convenience we are using dollars ($), tokens will be expressed in dollars very often when generating/enabling/disabling tickets - This aims to simplify the logic behind every chain, on TedLotto and possible price fluctuation between weeks.&#x20;
{% endhint %}

## Stake

Users can stake and redelegate any amount of tokens from their [KEPLR wallet](https://www.keplr.app/).  For every specific amount of tokens delegated to Tedcrypto, the delegator gets a recurring lottery ticket (i.e. assuming a blockchain ticket is given for every 10TOKENs delegated, if you delegate 40TOKENs, you'll get 4 tickets). Currently, the system is generating these tickets for you automatically, not allowing you to create a specific ticket number this might be possible in the future if there is an evident need from the community.

{% hint style="info" %}
For the example above, If you just delegate 9TOKENs, you wouldn't receive any ticket, but if you ended up delegating an additional 1TOKEN later on, you would get 1 ticket. In that same order, if you delegate 11TOKENs followed by another stake of 19TOKENs, you will receive 1 ticket from your first delegation and then 2 (for a total of 3) tickets respectively after your second stake.
{% endhint %}

Deposits have the usual APR/APY (or interest) that accumulates in the account of the user, which is based on the bounded tokens and inflation of the chain.

If [restake](https://www.restake.app) is enabled, delegator rewards will be automatically claimed (Tedcrypto will pay for the fees) and staked again on your validator. These rewards will be accounted for in the ticket system. We highly encourage our delegators to enable this feature!

#### Details on Tickets

Each ticket is represented by a sequence of 6 numbers, each number between 0 and 15 (both included). "1 2 3 4 5 6", "1 2 3 13 14 15", and "10 11 12 13 14 15" for example are all valid ticket numbers.

There is no limit to delegators sharing the same ticket number. In the case of multiple delegators holding the same winning ticket, all of the corresponding delegators win equally, unless a jackpot or super-jackpot happens, for these cases, the prize will be divided among all those winners, this is known as self-sustained fixed pool size (i.e.: we always guarantee a prize to every delegator)

## Ticket system

Tickets will be enabled/disabled/created when the following happens:

&#x20;\- Wallet is first created/connected to Tedlotto website\
&#x20;\- Delegator makes a stake/redelegation using Tedlotto portal\
&#x20;\- Every 15 minutes when updating Tedlotto staking amounts\
\
To be eligible for the lottery one must connect the wallet to Tedlotto, even if you delegated with us before using external wallet explorers. If the wallet is not connected through tedlotto app the system will not recognise your wallet and therefore no tickets will be created for you. \
\
Ticket price is fixed to roughly $25, this is subject to change and it will create some differences in the amount of tickets allocated to you and in the system, more can be created/deactivated/activated based on this change. Ticket price will be updated manually for now before every draw, and you will be notified on our social groups ([Telegram](https://t.me/TedcryptoOfficial), [Discord](https://discord.gg/snPBETGTBj) and [Twitter](https://twitter.com/tedcrypto\_))\
\
If the ticket price raises then you should expect that some of your tickets will be deactivated. If the ticket price decreases then we will prioritise activating your deactivated tickets and only after that we will create more if the number of tickets to be generated is bigger than the deactivated ones.\
\
Once a prize has been determined for one of your tickets, it will always be possible for you to claim it no matter its current state (i.e.: a prize has been given to one of your tickets that has been deactivated past that draw)
