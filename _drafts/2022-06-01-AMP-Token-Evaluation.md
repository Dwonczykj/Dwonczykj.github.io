---
created: May 25, 2022 11:38 AM
entities: Amp, Flexa
layout: post
title: Payments without the fees (AMP Token) - Draft
categories: [Payments, Crypto]
comments: true
---
In this article, I discuss AMP, a Crypto ERC20 compatible token that seeks to radically improve the process of paying.

I mainly verbalise my notes from reading AMP's Whitepaper (the specification and intention of the coin from its creators), with the addition of other sources such as the interviews and speeches from the founders.

I begin with a higher level overview of the intended direction and goals of the AMP token and its coupled network, Flexa. I then present a more in depth analysis of the tokens architecture and characteristics using a mind map as this more clearly denotes the connections between the various parts of the revolutionary Flexa payments ecosystem and the design of the AMP token.

# Description

Amp is a collateral token. A cryptocurrency token is like a chip on a poker table, it represents an asset ($5 of gambling power in poker) or a specific use and is stored on a blockchain.

It exists to act as collateral for financial transactions where traditionally, bonds, money etc would be used and be held by custodians (third parties) all charging fees for their services.

## Mission Statement

Its goal is to reduce counterparty risk on transactions through **financially efficient** collateralization.

# Design Overview

Amp enables tokens to be conditionally allocated as collateral **without requiring additional transfers** to another smart contract to store the collateral for the transaction. This is cheaper and removes the custody risk, whereby collateral tokens need to be temporarily transferred between smart contracts to act as collateral.

AMP has been designed using economics fundamentals models to ensure that the token is low volatility and hence suitable for collateralization due to the economic surety of its value over the lifetime of a transaction. Amp's value compounds, exclusively as a result of any utility that it provides. This means that the more transactions that it collateralises, the more valuable the collateral that is used. This feedback loop is described in the white paper abstract as a '*virtuous feedback loop of increasing spending capacity*'. Additionally, using a decentralised architecture significantly reduces fees traditionally charged by collateral custodians in financial systems. This fee reuduction is facilitated via open validator sets and distributed convergence mechanisms.

To put in perspective the cost to society currently for the cost to make a payment, it's estimated (see [https://youtu.be/32_3fUPJJVA?t=1178](https://youtu.be/32_3fUPJJVA?t=1178)) at 2% of U.S. GDP. Considering that the entire U.S. Military defense budget is 3% of U.S. GDP, it puts into perspective the size of the payments interchange market which is charged to merchants and consumers.

# Digital Payments

[Flexa](https://www.notion.so/Flexa-87a0689f5e6a4a0493bdc13486e02428) integrates natively with existing point of sale (POS) systems<style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mrow></mrow><mn>9</mn></msup></mrow><annotation encoding="application/x-tex">^{9}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.8141079999999999em;vertical-align:0em;"></span><span class="mord"><span></span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">9</span></span></span></span></span></span></span></span></span></span></span></span></span><span>﻿</span></span> and online platforms to enable payment in a typical checkout experience. The network Spend SDK is permissionless; mobile wallets or applications can create unique, interoperable authorisation codes for conveyance.$^{10}$

## Digital collateral providers & their incentive

To enable payment functionality, applications and communities can collectively stake Amp tokens on behalf of users. As incentive for supplying collateral, the entirety of network transaction revenue funds the continuous open-market purchase of Amp tokens for redistribution as network rewards.

<aside>
📘 Numeraire Good → A good that acts a base point of reference value for a good's market.
• *A numeraire is usually applied to a single good, which becomes the base value for the entire index or market.
• The U.S. dollar remains the numeraire for most commodity prices.*

</aside>

Link to reason for needing collateral from original conference note:

[FLEXA: HODL. BUIDL. SPEDN! [Sponsored] | Consensus 2019](https://youtu.be/XaXbl-og23o?t=1423)

![point of sale network](point-of-sale.png)

# Amp token description

Amp resembles a rudimentary token in that balances are assigned to Ethereum addresses, but the tokens also belong to a particular 32-byte partition which effectively serves as a second-dimension in the distribution array of the balances. (i.e. we can see how much token there is for a particular ethereum address, but we can also see how much token there is on any specified address to a 32-byte partition of memory.

Amp supports transfers between addresses and partitions through the `transferByPartition`
function, and includes the `approveByPartition` function that authorises an address to transfer
tokens on behalf of the caller, but only from a particular partition.

For backwards compatibility of the ERC20 token, the token must support the `transfer` and `approve` contract functions. To do this, it uses the zero partition ("default partition") with address of x0.

We can think of partition as its location on the chain storage and address as the address of the ethereum wallet holding it perhaps.

![partition semantics](partition-semantics.png)

For every transfer, 2 events are emitted from the smart contract so that balances can be tracked off the chain too (i.e. without having to aggregate all transactions since genesis block to know balances). These events are:

- `Transfer` containing the to, from address and the amount
- `TransferByPartition` contains the same data as Transfer, as well as the to and from
partitions and any metadata or operatorData parameters.

# Amp's Unique Differentiator

The partition. I go into depth on what this is and why it is so powerful in the next section that links together all aspects of the design. For developers, the key interface is:

<aside>
🤔 `IAmpPartitionStrategyValidator`

</aside>

# In-depth Architecture Evaluation

The below is an in depth look at the architecture of the AMP token as described in the AMP Whitepaper. It reiterates the implementation description of the AMP token that we have just covered. The graph then goes into far more detail answering questions such as "*Why is the AMP token has this design?*", "*How does this tie in to the Flexa payments pipe network?*" and "*How can blockchain DApp developers leverage the functionality of the AMP token (contract) for their own use-cases and applications in the payments ecosystem?*".

[https://whimsical.com/amp-token-TM67rPRGs5boowrueSZ2oN](https://whimsical.com/amp-token-TM67rPRGs5boowrueSZ2oN)

The next section displays an overview of the different participants in a payments network and how they interact with one another. This is useful for understanding the role of the Flexa network and its AMP token in the worldwide payments ecosystem.

[https://whimsical.com/payments-networks-M7bqDoDFCJrh7WsumZ8ck2](https://whimsical.com/payments-networks-M7bqDoDFCJrh7WsumZ8ck2)

# AMP Economic Token Pricing Model

Initially consider the pricing model for any token network in which the token is an asset on that network (*participants perform transactions to own the asset*):

$$
P_t = \frac{N(A_t)S(A_t)A_t}{M}\left(\frac{1-\alpha}{r - \mu^{P}(A_t)}\right)^{\frac{1}{\alpha}}
$$

- $N$ - Users or participants on the platform
- $S$ - Aggregate transaction need (*demand*)
- $A_t$ - platform productivity factor
- $M$ - total fixed token supply
- $\alpha$  - an autoregressive constant
- $\mu^{P}$ - Expected price appreciation of the token

We next update this identity for AMP by recognising that AMP tokens are **not** transactional like tokens generally are above, but exist to facilitate spending capacity (utility) on the payments network.

So, we simplify the above identity:

- make payment volume $A_t$ unconditional because the network is used to facilitate payments, not to purchase AMP itself.
- similarly, assume a constant aggregate transaction need, $S$. In the Flexa payments network transaction need is not conditional on the productivity of the platform.

This results in the following modification of the above general token pricing identity:

$$
P_t = \frac{N_tU_t^{P}A_t}{M}\left(\frac{1-\alpha}{r-\mu_t^{P}}\right)^\frac{1}{\alpha}
$$

Note that as capacity, $U_t^P$(*total staked value on the network*), increases, this results in a proportional increase in $P_t$ and directly causes an increase in the value of staking rewards. This compounds user adoption to the network leading to further network growth which should lead to further increases in capacity.