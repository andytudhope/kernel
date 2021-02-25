---
title: Censorship Resistance
description: When the incentives which define the structure of power in society can be programmed by anyone, anywhere; censorship resistance becomes an engineering problem, not an ideological one. Can we engineer truth in the face of power?
image: /assets/shares/censorship-resistant.png
---

# 👮 Censorship Resistance

<a href="https://blog.ethereum.org/2015/06/06/the-problem-of-censorship/" target="_blank">Vitalik has defined the ills of censorship</a>. And who are we to argue with the boy genius...

Well, that's kind of the point, isn't it? We want to live in a society where we can engage in *effective* debate with anyone. While we enjoy freedom of speech in many places today, expressing an opinion is not the same as acting upon it. However, blockchains fuse [money and speech](../../module-2/money-speech/), meaning that [expression and (economic) action](../../module-4/self-enquiry/#identity-we-can-live-with) occur simultaneously.

It's critical to speak [truth](../../module-5/reveal-the-universe/#the-value-of-truth) to power; history is proof of this. However, history also shows how the existence of any kind of power structure influences what truths can be thought and enunciated in the first place. How can we [free ourselves](../../module-3/freedom/) from this constraint? With adaptive [incentives](../../module-5/incentives/)!

When the incentives which define [the structure of power in society](../../module-5/the-peoples-narrative/#the-nudge) can be programmed by anyone, anywhere; censorship resistance becomes an [engineering](../../module-2/engineering/) problem, not an ideological one. This is clear if you read Vitalik's post - it's all about implementation details, not ideology. 

"[Don't fight the system. Just abandon it.](../../module-4/governance/#anarchy)" We can literally engineer more expressive solutions.

## Economic proof

Recall that [trust](../../module-0/trust/) is only possible once you have encoded what it means to cheat. Similarly, we're not interested in debating the evils of censorship. We're interested in building clear and complete **threat models** which allow us to understand all possible benefits for potential censors.

Instead of using legal code to uphold the supposed good of free speech, we can use economic code to make censorship prohibitively expensive. This has profound second-order effects: i.e. even if you have the economic-computational power required to revert history, there is *still no benefit* in doing so due to the verifiable, shared nature of blockchains.

Censorship can be more insidious than overt reversions of history though. So, we need to develop even clearer **cost models**. Proof of Work actually fails to ensure that censorship is not profitable, since if you censor a block you can (i) take all of its transactions for yourself, and (ii) in the long run take its block reward. You could potentially solve this using timelock consensus, though this has its own drawbacks and remains largely theoretical.

Quasi Turing-complete object models (i.e. Ethereum) already provide interesting means of making censorship costly outside the actual consensus mechanism. For instance, we prevent the Halting Problem and denial of service attacks by assigning a "gas" cost to each operation and limiting the amount of gas per block to ensure all programs terminate. Much Eth2 research is about both <a href="https://vitalik.ca/general/2018/08/07/99_fault_tolerant.html" target="_blank">higher fault tolerance</a> and stronger censorship resistance based on more complete threat models and cost analysis. Such research and implementation indicates why economic engineering is orders of magnitude more effective than legal lip-service.

## Higher Stakes

In [Understanding Ethereum](../../module-1/understanding-ethereum/#virtual-economy) we discussed how there are, for instance, no technical limits on what can be put in the `data` field of an Ethereum transaction, though there are economic ones: it costs 68 units of gas per byte. This feature crops up over and over, and takes on new dimensions in a full Proof of Stake architecture. No behaviour is technically impossible, though we carefully encode what we define as malicious, and institute clear economic penalties. 

Bitcoin uses mathematics in the form of elliptic curve cryptography to route around the need for human regulation and thereby ensure some degree of censorship resistance. Ethereum does this too. However, Eth2 will use a different kind of mathematics - game theory - in addition to cryptography to ensure not just censorship resistance, but to prove objectively that censorship is asymmetrically expensive for those who would attempt it.

We'll be using value created on a public network to secure that same public network. This is the kind of profound economic feedback loop which lays the foundation for what comes after the central bank of the internet; what Vinay Gupta called "[Acts II and III](../../module-1/promise-blockchains/#the-2010s-satoshis-vision)".

---

## Further References

<a href="https://twitter.com/vitalikbuterin/status/1256227159707877378" target="_blank">Levels of resistance</a>