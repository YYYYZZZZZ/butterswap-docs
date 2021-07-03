# ✨ Lucky Lucky

{% hint style="success" %}
[Lucky Lucky Prize History](https://www.butterswap.me/board/lucky_history)
{% endhint %}

Each day, there is a special round of Lucky Lucky, in which we give one lucky participating board member a special prize \($$1\%$$ of all reward emissions per day, which is 138,240 BUTTERs based on current emission rate\).

You can stake any number of BOARD tokens to in the Lucky Lucky, pool and your BOARD tokens will be returned in full amount if you leave Lucky Lucky. If you keep the staked BOARD tokens in Lucky Lucky pools without unstaking, you will automatically participate each round of Lucky Lucky.

Winning probability, what we name it _**power**_, is determined by both the number of staked BOARD tokens and the staking timing. If you have not staked any BOARD tokens before the current round of Lucky Lucky starts, the initial _**power**_ is set to 0. If you have already staked some BOARD tokens before the current round of Lucky Lucky starts, the initial _**power**_ is given as follows:

```text
power = board_current * (end_block - start_block)
```

_**board\_current**_ is the current number of BOARD tokens you have already staked, _**end\_block**_ is the predicted end block number of this round of Lucky Lucky, and _**start\_block**_ is the start block number.

During the day, you can stake and unstake freely any mount of BOARD tokens to Lucky Lucky event.

Each time you stake BOARD tokens to Lucky Lucky event, the _**power**_ is updated as follows:

```text
power = power + board_num * (end_block - current_block)
```

_**board\_num**_ is the number of BOARD tokens you stake this time, _**end\_block**_ is the predicted end block number of this round of Lucky Lucky, and _**current\_block**_ is the current block number.

Each time you unstake BOARD tokens from Lucky Lucky event, the _**power**_ is updated as follows:

```text
power = power * (board_total - board_num) / board_total 
```

_**board\_total**_ is the number of staked BOARD tokens before this unstaking, and _**board\_num**_ is the number of BOARD tokens to be unstaked.

By the end of day, the smart contract will calculate a _**power**_ value for each participants. And a weighted random selection based on the _**power**_ value will be used to select the winner for the Lucky Lucky event.

Everything is calculated inside smart contracts on blockchain, and we believe it is a fair and fun event to participate.

