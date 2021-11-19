# Staking Pool



To start staking, an IHELP token holder will need to deposit their IHELP token in the IHELP staking contract. Once deposited they will start earning a pro rata share of the interest donation and direct donation fees. Their IHELP stake will earn a share of the fees equal to their share of the total IHELP staked, at the block the fee occurred. You can withdraw your staked IHELP at any time.

XHELP will be the LP Claim token for the IHELP staking pool. When you stake your IHELP, you effectively exchange your IHELP for XHELP. Over time, you’ll always earn more IHELP by holding XHELP tokens. This is because for every donation on the iHelp Protocol, a fee is charged and sent to the XHELP pool. The fee is set at 15% of interest donations and 2.5% of direct donations. This fee is used to buy back IHELP tokens periodically in the open market. Initially, the protocol will execute buy-backs on a weekly basis. So when you exchange your XHELP for IHELP, you'll get the original IHELP deposited plus your pro-rata share of protocol staking fees.

To explain further, a Helper would deposit 1 IHELP in the pool and receive the LP Claim Token (XHELP). As rewards in the pool grow, the deposit token’s balance (XHELP) will remain unchanged, yet its presence in the address will trigger accrual of IHELP (IHELP) tokens to reflect growth of rewards in the pool. The pool will progressively own more IHELP rewards than it started thanks to its programmatic IHELP buybacks funded by the staking fees. Let’s look at an example:

1. Helper A initially funds the staking pool with 10 IHELP tokens, these are exchanged for 10 XHELP tokens at a 1 to 1 exchange rate.
2. IHELP staking fees accrue and the protocol buys back 2 IHELP tokens in the open market and deposits them in the staking pool. There are now 12 IHELP tokens for every 10 XHELP tokens. The new exchange rate is 1.2 IHELP for every XHELP token.
3. Helper B decides to participate in the pool, and funds it with 30 IHELP tokens. At the current 1.2 exchange rate, Helper B will receive 25 XHELP tokens back. The pool now owns 30+10+2 = 42 IHELP tokens and there are 10+25= 35 XHELP LP claim tokens. 42/35 = 1.2 exchange rate.
4. IHELP staking fees accrue again and the protocol purchases 28 IHELP tokens. There are now 42+28=70 IHELP tokens in the staking pool and 35 XHELP claim tokens. The new exchange rate is 2 (70/35).
5. Helper A’s initial stake of 10 IHELP (for which they received 10 XHELP) can now claim 20 IHELP. Helper B’s initial stake of 30 IHELP (for which they received 25 XHELP) can now claim 50 IHELP.

##
