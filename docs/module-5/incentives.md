---
title: Incentives
description: Economic code on a shared ledger can be used to program crowds. Here we begin the exploration of what kinds of programs we should think about writing anf why.
---

# Incentives

The best 3 (slack) responses or (PR) improvements to this note will be awarded 50 DAI each.

---

Need we say more about why incentives matter?

## Persuasion

What constitutes persuasive language? Words which perform what they say. If an essay about humour is itself funny, then that essay is more likely to convince you about what humour is.

What happens when you use code to both model and build economic systems, and then have that same code execute transactions? Well, you can build really persuasive incentives for any kind of economic behaviour. How do we know what behaviour we should incentivize though?

## Economics in the computer age

Here's a [new kind of economic essay](https://github.com/norvig/pytudes/blob/master/ipynb/Economics.ipynb). What makes it interesting is that with a few lines of Python, Peter Norvig proves a surprising result about wealth inequality. The initial distribution of wealth in the economy doesn’t affect the long-run distribution of wealth nearly as much as the *nature of the transactions*. His code also suggests that constraining agents to trade only with people geographically near them makes little difference to the final distribution of wealth.

Results like these challenge your intuition. But instead of those challenges being on the basis of abstract arguments, you can engage his model. If you don’t agree that the initial distribution of wealth doesn’t affect long-run wealth inequality, you can try find a counterexample: an initial distribution which does affect inequality. You can experiment easily, making modifications to a few lines of code, trying to find instances where the initial distribution matters. No matter whether you succeed or fail, you will build a better understanding of the problem.

Used well, Jupyter notebooks become environments for transformative thought. They’re a new media form, with different possibilities from either essays or code. And that's just a notebook, let alone a smart contract. Such contracts deployed on a shared, global network not only demonstrate new economic insights and ideas, they **implement** them.

## Programming crowds

You must <a href="https://blog.oceanprotocol.com/towards-a-practice-of-token-engineering-b02feeeff7ca" target="_blank" rel="noopener noreferrer">think like an engineer</a> about the <a href="https://www.youtube.com/channel/UC-o87lCF9HaEuj0R-3VT1yg" target="_blank" rel="noopener noreferrer">economic games</a> your contracts incentivize. Ironically, the best place to go looking for clear thinking and research in this domain is neither economics, nor psychology. It is computer game design.

The reason for this is that contractual economic code on a shared, public ledger actually programs crowd behaviour. Don't get too excited by this, for with great power comes great responsibility - which is why the thinking patterns we outlined at the start of these modules have fundamentally to do with **[humility](../../module-3/humility/)**. You cannot, as an individual, know what the second and third order effects of such code will be. But you can be deeply aware that such effects exist, and you can use your awareness to inform the intention with which you write and deploy contracts.

This is software as **service**. We are all Satoshi.

