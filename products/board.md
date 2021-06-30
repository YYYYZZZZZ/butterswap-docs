# 🏦 Board \(coming next\)

ButterSwap board is a mechanism for DAO \(Decentralized Autonomous Organization\) aiming to make the community decide on important decisions, such as next halfing time, and give the BUTTER supporters various rewards and benefits.

## Entering the board

You first stake BUTTER to get CREAM tokens $$1:1$$ , and then you stake $$X$$ CREAM tokens to get DAO tokens $$1:1$$, where $$X$$ is at least $$0.1\%$$ of BUTTER total supply. Now you become a board member of ButterSwap! 

For each CREAM token you stake in the board, you get a BOARD token and a DAO token. Similar to CREAM, both BOARD and DAO are free tokens, and they are $$1:1$$ with CREAM. BOARD tokens are for staking and DAO tokens are for voting. Once you become a board member, unless you quit board, you will stay in board even if your staked CREAM tokens becomes less than $$0.1\%$$ of BUTTER total supply, which increases continuously. So for early board members, the entering threshold is lower than later board members, which is reasonable.

After you enter the board, you can always choose to add more CREAM tokens to staking. For example, if the board requires 100 CREAM tokens, and you previously only staked 90 CREAM tokens, it is perfectly fine for you to stake only 1 CREAM token. Even though 91 CREAM tokens is still less than the required 100, since you are already a board member, you will continue to be in board.

## Board benefits

### 1. Voting

With the freely obtained DAO tokens, board members can vote on important community decisions, such as next halfing time, tokenomics, activity rules, etc. Since only board members can have DAO tokens, voting is a special privilege for board members to collaboratively improve the whole eco-system.

For each voting topic, you can vote multiple times and change your vote as long as the voting has not ended yet. Only the last voting would count. The number of the voting tickets is always equal to the number of DAO tokens you possess. For example, after you make your vote, you choose to obtain more DAO tokens by staking more CREAM tokens, your voting tickets increase automatically. Similarly, if you decrease your DAO tokens, so does your voting tickets.

Voting does not cost you any DAO tokens, since your DAO tokens only represent that you have the voting power. After each voting topic, you still have all the DAO tokens and you can always start voting on a new topic with all the DAO tokens you have initially.

### 2. BOARD pools

There will be various BOARD pools, similar to CREAM pools, available only for board members. You can stake you free BOARD tokens to earn in these pools. These pools include DEX revenue sharing pools, eco-system partner airdrop pools, donation pools, NFT revenue sharing pools, etc. You can choose different pools to participate and stake different amount of BOARD tokens to any of them.

The same as in CREAM pools, there is no locking period for BOARD pools, and you can always unstake any amount of BOARD tokens at any time.

### 3. Lucky Lucky

Each day, there is a special round of Lucky Lucky, in which we give one lucky participating board member a special gift \($$1\%$$ of all reward emissions per day, which is 138,240 BUTTERs based on current emission rate\). You can stake any number of BOARD tokens to in the Lucky Lucky, pool and your BOARD tokens will be returned in full amount if you leave Lucky Lucky. If you keep the staked BOARD tokens in Lucky Lucky pools without unstaking, you will automatically participate each round of Lucky Lucky.

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

### 4. Auto BUTTER pools \(to be released in Board Phase 2\)

You stake BUTTER in auto BUTTER pools, and the earnings will be automagically harvested and restaked \(compounded\) for you. A small percent of performance fee will be subtracted automatically from each yield harvest and burned. 

### Other special benefits coming soon

## Leaving the board

After you enter board, you can choose to add any number of CREAM tokens to the staking. However, if you want to unstake CREAM tokens, you have to quit the board and unstake them all at once. You can only quit the board 7 days after entering and only on Sunday. After you quit the board, you return all the BOARD and DAO tokens, and get back all your staked CREAM tokens, which in turn can redeem your staked BUTTER tokens. After you leave the board, if you want to reenter the board, the number of CREAM tokens required to be staked will be recalculated based on the total BUTTER supply by then.

{% hint style="warning" %}
Similar to CREAM token, don't transfer or sell any BOARD or DAO tokens. Before you unstake CREAM, you have to unstake the same amount of BOARD and DAO tokens first. You have to return the same amount of BOARD and DAO in order to unstake the same amount of CREAM. Since you have to unstake all CREAM tokens at once when leaving, transferring away very small amount of BOARD or DAO tokens from you wallet may result in permanent failure to quit board. So do not try these strictly forbidden behaviors.
{% endhint %}

