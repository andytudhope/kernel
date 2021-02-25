---
title: Serenity
description: A summary of the Ethereum 2.0 Design Rationale as ideological heir to the cypherpunk spirit of defender's advantage and a discussion of why Proof of Stake eliminates various critical conflicts of interests, allowing us to build and maintain a planetary-scale incentive machine anyone can use and no-one owns.
image: /assets/shares/giving.png
---

# 🦋 Serenity

You've finally reached the tranquil waters of Eth2 - congratulations! Like the network it describes, this post will be completed in some indefinite series of stages over the next "little while". Please check back here periodically for at least a few years.

<div markdown="1" class="card half sidebar center gemoji center-content center">

**Eth2 Design Rationale**

<div markdown="2">
![Design Rationale](/assets/images/ethereum.png)
</div>

<div markdown="3" class="curated-link">
<a href="https://notes.ethereum.org/@vbuterin/rkhCgQteN?type=view" target="_blank">Read it</a>
</div>

</div>

<div markdown="1" class="clear"></div>

### How does this fit into Kernel?

In a way, this is what Kernel has been preparing you for: what Vinay Gupta called ["unimaginable strangeness"](../../module-1/promise-blockchains/#the-2010s-satoshis-vision), wherein we deploy a global, public, decentralized and censorship-resistant computing surface which anyone can use and no-one owns. 

What this [*means*](../../module-1/meaning/) for our networked species remains an open [question](../../module-2/better-questions/). One thing seems clear: it is an upgrade the likes of which is only seen once in a generation at most. You'll need to recall the arguments made in [value](../../module-1/value/) and [incentives](../../module-5/incentives) to understand the design rationale for these next few scenes of the [human](../../module-0/conversation/) [story](../../module-5/listening-stories/).

In particular, [we claimed that](../../module-2/money-speech/#regulation-vs-expense) - with blockchains - the best way to protect free speech is to price it correctly. We don't enforce "the good" by legal fiat and deal with exceptions like libel and hate speech through human interpretation and violent enforcement; we define what is "bad" and set a price on it such that malicious expression is provably more expensive than its potential effects. Eth2 extends this idea greatly: it is our generation's <a href="https://www.ribbonfarm.com/2019/01/31/elderblog-sutra-1/" target="_blank">elder game</a> of economic penalties.

## Brief

### Principled Layers

Just as [we did for Kernel](../../getting-started/#kernel-principles), Vitalik begins Eth2's design rational with a series of core principles:

- **Simplicity**: given the inherent complexity of such networks, this (i) minimizes development costs, (ii) reduces the risk of unforeseen security issues, and (iii) helps protocol designers to more easily convince users that parameter choices are legitimate. When complexity is unavoidable to achieve a given level of functionality, the preference order for where the complexity goes is: layer 2 protocols → client implementations → protocol spec.
- **Long-term stability**: the low levels of the protocol should ideally be built so that there is no need to change them for a decade or longer.
- **Sufficiency**: it should be possible to build *any class* of applications on top of the protocol.
- **Defense in depth**: the protocol should continue to work as well as possible under a variety of possible security assumptions (network latency, fault count, the motivations of users etc.)
- **Full light-client verifiability**: given some assumptions, a client verifying `O(c)` data should be able to gain indirect assurance that all of the data in the full system is available and valid, even under a 51% attack.

In our [very first note](../../module-0/play-of-pattern), we made the point that our way of thinking and solving problems _always_ has to do with trade-offs. The trade-off between complexity and functionality is a deep one and goes to the heart of the debate about whether we should be innovating on layer 1 or 2. The answer is "both", and you need to understand your own context in order to best decide where on the spectrum your most optimal solution lies.

Vitalik calls this "<a href="https://vitalik.ca/general/2019/12/26/mvb.html" target="_blank">functional escape velocity</a>": we need layer 2 solutions to ensure **simplicity** and **long-term stability** by reducing the complexity of the consensus layer; and we need layer 1 innovation in order to ensure **sufficiency**. In practice, this means:

1. *Quasi-Turing-complete and richly-stateful code execution*, allowing robust L2 trust solutions.
2. *Scalable data availability and computation,* along with
3. *Fast block times,* both of which ensure that L2 is not limited to channel and Plasma-like techniques which are not general and suffer capital inefficiencies and/or mass-exit issues.

There are other features deliberately left to L2: (i) privacy, (ii) high-level programming languages, (iii) scalable state storage, and (iv) signature schemes, because these features are all areas of rapid innovation, which tilts the trade-off towards ensuring we don't set some solution in the stone of our protocol spec for an area likely to develop extensively over the next 10 years.

### A Defender's Game

Bitcoin was a major innovation - it's almost like time-travelers came back to 2009 and dropped it on an obscure mailing list for us to puzzle over. However, <a href="https://www.gwern.net/Bitcoin-is-Worse-is-Better" target="_blank">it is not elegant</a> and its consensus algorithm breaks one of the fundamental advantages cryptography provides: **adversarial conflict should heavily favor defenders**. Sea steads are easier to destroy than build, but an average person’s ECC keys are secure enough to resist even state-level actors.

> Systems that consider themselves ideological heirs to the cypherpunk spirit should maintain this basic property, and be much more expensive to destroy or disrupt than they are to use and maintain.

Proof of Work security can only come from block rewards, and incentives to miners can only come from the risk of losing future block rewards. Proof of work necessarily operates on a logic of massive power incentivized into existence by massive rewards. It's effective, but inefficient. The cost of attack and cost of defense are at a 1:1 ratio, so there is no **defender’s advantage**.

> Proof of stake breaks this symmetry by relying not on rewards for security, but rather penalties [...] The “one-sentence philosophy” of proof of stake is thus not “security comes from burning energy”, but rather “security comes from putting up economic value-at-loss”.

Consider Amazon's algorithm and how they solved unbounded search by turning everything into a platform, only to find that [advertising is intractable to platform solutions](../../module-5/amazon-unbounded-search/#unsolved-advertising). This is because the limited number of top spots on infinite-length shelves, and the crazy amounts of revenue they generate, create a conflict of interest between Amazon and its users. This kind of conflict can only be [solved with a **protocol**, not a platform](../../module-0/money-language/#open-protocols-and-a-network-of-value). However, PoW protocols still have a comparable conflict of interests between miners and users. Miners must pay for the massive power they are incentivized to use in securing a PoW network, which creates both (i) consistent forced sellers in any market and (ii) skewed incentives around, for instance, block sizes which lead to sub-optimal outcomes for users of the network.

Ensuring that anyone, even with entry-level hardware and a small amount of ETH, can act as a validator and that the protocol relies on penalties rather than rewards, means that users and validators are more likely to be *the same people*, thus reducing conflict. Just as protocols which define and encode what it means to cheat do no need to be [trusted](../../module-0/trust/), protocols which define and encode penalties are **more likely to benefit all their users**. This is because encoding rewards creates inevitably skewed incentives that only accrue to the subset of network participants who are best placed to game the system required to earn them.

### Proving Stake

Eth2 uses a slashing mechanism where a validator that is detected to have misbehaved can be penalized: in the best case ~1%, but in the worst case up to its entire deposit. This raises the cost of an attack such that we achieve the defender's asymmetry described above and overcome the validator's dilemma, i.e. lazily validating everything without properly checking each transaction.

Vitalik describes why Casper FFG was chosen - it was the simplest available at the time - and how other options continue to be explored. He highlights the problem of "supernodes" and why sharding is better: less centralization risk, more censorship resistance, and better long-term scalability. Critically, he then considers the security models of any system we choose, and how it operates not just under the "honest majority" model of 51% chains, but also the *uncoordinated rational majority* and *worst-case* models. Assuming the worst-case, the question remains:

- Can we force the attacker to have to pay a very high cost to break the chain’s guarantees?
- What guarantees can we unconditionally preserve?

Slashing ensures the first condition, and Vitalik provides a detailed table of the guarantees we can preserve with Proof of Stake systems in <a href="https://notes.ethereum.org/@vbuterin/rkhCgQteN?type=view#Security-models" target="_blank">this section</a>. In a system designed around penalties, you need to distinguish between various types of validator failure - most of which are benign (like simply being offline) - and only a few of which are genuinely malicious. Critically, **it is the trade-off between different penalties** which informs how we structure rewards.

#### Aligning Incentives

Validators must attest to what they believe to be the head of the chain in each epoch. If they do so, they earn a **base reward**, which is split into 5 parts described <a href="https://notes.ethereum.org/@vbuterin/rkhCgQteN?type=view#Base-rewards" target="_blank">here</a>. There are two features to understand about this reward: how it prevents "<a href="https://raw.githubusercontent.com/ethereum/research/master/papers/discouragement/discouragement.pdf" target="_blank">griefing</a>", and how it is calculated. 

1. Griefing occurs when an attacker seeks to reduce other validators’ revenue, even at some cost to themselves, in order to encourage the victims to drop out of the mechanism (either so the attacker can get more revenue, or as part of a longer-term 51% attack). By multiplying the **base fee *B*** with ***P***, the portion of validators that agree - and penalizing any validator who doesn't with **−B** - we implement a *collective rewards scheme* where “if anyone performs better, everyone performs better”. This bounds the griefing factors in an optimal way and is the best example of [explicitly prosocial mechanism design](../../module-5/prosocial-value) we know of in any blockchain.

2. The **base fee** is proportional to the inverse square root of all deposits. This strikes a compromise between a *fixed reward rate* and a *fixed total reward*. The first creates too much uncertainty about both issuance and the total level of deposits; the second potentially incentivizes griefing more than can be disincentivzed by the collective scheme above. Again, mechanism design is *all about balancing trade-offs*.

Rewards are designed this way *only as a result* of the thinking about how to penalize different kinds of undesirable validator behaviour. Now that we understand this premise, we can check that the rewards fit our requirements by considering the **break-even uptime** for any validator. If everyone is validating, you need only be online ~44.44% of the time. However, if other validators are offline - say P = 2/3 - then you need to be online ~53.6% of the time.

The incentives ensure that, as more validators go offline, the penalty for doing so is greater, which creates something Vitalik calls an **inactivity leak**. If the chain fails to finalize for more than 4 epochs, a second penalty component is added which increases quadratically over time. This:

- Penalizes being offline much more heavily in the case where you being offline is actually preventing blocks from being finalized and
- Ensures that if more than 1/3 do go offline, eventually the portion online goes back up to 2/3 because of the declining deposits of the offline validators.

So, we can handle elegantly the penalties for common and benign kinds of validator failures, but what about actual attacks and/or malicious behaviour? If a validator is caught violating the Casper FFG slashing condition, <a href="https://github.com/ethereum/eth2.0-specs/blob/dev/specs/phase0/beacon-chain.md#proposer-slashings" target="_blank">they get penalized</a> a portion of their deposit equal <a href="https://github.com/ethereum/eth2.0-specs/blob/dev/specs/phase0/beacon-chain.md#slashings" target="_blank">to three times</a> the portion of validators that were penalized around the same time.

- A validator misbehaving is only really bad for the network if they misbehave at the same time as many other validators, so it makes sense to punish them more in that case.
- It heavily penalizes actual attacks, but applies very light penalties to single isolated failures that are likely to be honest mistakes.
- It ensures that smaller validators take on less risk than larger validators (in the normal case, a large validator would be the only one failing at the same time as themselves).
- It creates a disincentive against everyone joining the largest pool.

### Technicalities

Vitalik then discusses some of the technical choices favored in the design, like BLS signatures (which are easy to aggregate) and SSZ (a simpler serialization suite which aligns with the principle of **simplicity**). We'll summarize very briefly here.

1. **32 ETH** minimum deposits <a href="https://notes.ethereum.org/@vbuterin/rkhCgQteN?type=view#Why-32-ETH-validator-sizes" target="_blank">strike a good balance</a> between decentralization / finality time / message overhead. This is a trade-off because the size of deposits defines the total possible number of validators (smaller deposits = more validators), which increases decentralization at the cost of message overhead, and potentially finality time.
2. Various techniques around **random sampling** for different committees are discussed, including Verifiable Delay Functions and the current <a href="https://notes.ethereum.org/@vbuterin/rkhCgQteN?type=view#Shuffling" target="_blank">swap-or-not</a> algorithm used to shuffle the validator set and assign responsibilities every epoch.
3. The **LMD GHOST fork choice rule**, which incorporates information from all validators, hundreds in each slot, making it extremely unlikely in the normal case that even a single block will be reverted.
4. The **beacon chain and shard structure** is described, along with reasons for not going with a different design, such as 
    1. Having distinct shard chains and linking them into the beacon chain more rarely. This was rejected to allow for fast (single-slot) base-layer cross-shard communication capability. See <a href="https://notes.ethereum.org/@vbuterin/HkiULaluS" target="_blank">here</a> for more.
    2. Not having a beacon chain, and connecting shard chains to each other in some other structure. This was rejected to maintain **simplicity**. The hub-and-spoke beacon chain structure with a hierarchical fork choice is simpler to implement and reason about.
5. The **proof of custody game**, which revolves around validators needing to produce "period sub-keys" such that they can prove they were not lazily verifying data. This creates a disincentive so as to overcome the validator's dilemma mentioned above.
6. The **validator lifecycle**, which involves depositing, activating, exiting, withdrawing and the reason for using a more convenient construction of "effective balance" for validators.
7. Finally, Vitalik describes **fork choice rule** - because the ability to exit the network at any stage is critical to the system's game theoretic equilibria.

### The Positive Sum

What is Eth2? Well, we said it already: our generation's elder game of economic penalties. These penalties are the game mechanics we use to reveal a [unique kind of truth](../../module-5/reveal-the-universe/#the-value-of-truth): it is possible to build - and asymmetrically defend/maintain - an explicitly prosocial, global, and ownerless system that provably benefits all the people who choose to use it. The benefits of encoding penalties extend to all layers of this game, including our ability to <a href="https://twitter.com/VitalikButerin/status/1294461236680130560" target="_blank">use co-ordination costs to our advantage</a>.

Welcome. Most of us [friends](../../module-5/prosocial-value/#friendship) here, because the alternatives are more expensive.