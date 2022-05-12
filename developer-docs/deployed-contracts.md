---
description: Description and overview of contracts deployed on various blockchains
---

# Deployed Contracts

### IHelp (ERC20Upgradeable)

The primary Protocol ERC20 Upgradeable contract that drives HELP token issuance, phase control, contribution tracking, _dripping_ of HELP tokens based on latest aggregate contributions across all charities and finally _dumping_ the accumulated interest to the respective charity pools, swappers and staking/development pools.

### xHelp (ERC20Upgradeable)

Contributors to the iHelp Protocol are incrementally awarded HELP tokens based on the interest generated through the protocol (and ultimately donated to the charities of their choosing). These holders of HELP tokens can stake their HELP tokens and are provided xHELP in exchange. This  xHelp ERC20 Upgradable contract handles deposits, withdrawals and exchange of HELP to xHELP tokens and interacts directly with the iHelp contract for reward distribution.

### CharityPool

This is a primary custom contract developed to support charity contributions from ERC20 tokens (DAI, USDC, wETH, etc). This CharityPool contract is initialized for each specific charity wallet and specific holding token, and handles contribution, withdrawal, sending of the contributed tokens to the lending protocol selected for the charity pool, direct donation to the charity, and finally tracks the interest generated for each contributor by specify charity.  The CharityPool contract directly interacts with the iHelp and Swapper contracts when dripping the interest generated from the contributed token lending protocol.

### Swapper

The Swapper contract is specifically designed to handle exchanges from CharityPool contract tokens that do NOT match the underlying token of a specific exchange destination. For example, if a CharityPool is deployed as DAI pool, it is assumed the charity will receive their donation generated from interest / lending protocol will also be in DAI. Since the staking and developer pools for the iHelp Protocol are currently in DAI, no swapping is necessary in these situations. If the CharityPool is deployed as a USDC pool, the charity will receive their donation in USDC, but the Swapping contract is called before the staking and developer shares are sent to the DAI holding wallets.
