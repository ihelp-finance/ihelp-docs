---
description: >-
  Outlines the current off-chain processes driving specific aspects of the
  platform.
---

# Off-Chain Processes

The below processes are currently running off-chain in the Rinkeby demo app. The team is considering moving several of these processes to on-chain [Chainlink keeper services](https://docs.chain.link/docs/chainlink-keepers/introduction/).

### Upkeep

The upkeep process specifically runs the _drip_ and _dump_ functions within the iHelp contract for 1) aggregating the total accumulated interest since the last upkeep, 2) circulating (or minting) new HELP tokens based on the total interested generated in accordance with the Distribution Phase map, 3) divides these newly circulated or minted HELP tokens to the contributors pro-rata their overall contributions, and 4) moves the generated incremental interest to a holding pool. This process runs at a cadence of once per day.

### Stat Collector

The stat collector process currently drives many of the leaderboard stats and collects data on the current state of the contracts, contributions, interest generation and overall numbers of contributors and deployed charities over time. Every one (1) minute the stat collector runs and updates an hourly aggregated value of the desired statistics. These stats are stored in an off-chain time-series database, and are served up with a REST API to the Dapp.

### Reward Distribution

The reward process is responsible for initiating the staking pool buyback of HELP tokens from the accumulated DAI in the staking pool. This process currently runs at a cadence of once every 3 days.
