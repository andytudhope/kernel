---
title: Understanding Ethereum
description: A short summary of one of Vitalik Buterin's first public talks on Ethereum, taken from DevCon 1 in London.
image: /assets/shares/giving.png
---

# 💡 The idea

<iframe class="video-frame" src="https://www.youtube-nocookie.com/embed/gjwr-7PgpN8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This early video from Devcon 1 contains many gems of insight into the ideas behind Ethereum; why it might be interesting and important to have one, shared, Turing-complete environment which anyone can access and program; and what the vision was (and is). It's especially useful to look back and ask what of the original ideas we have succeeded in implementing, and where there are still opportunities for improvement. This video has been selected to assist you deepen your (more technical) understanding of:

1. Value
2. Trust
3. Incentives
4. Censorship resistance
5. (Not just!) money and speech

## Brief

This video is the genesis of the calculator (Bitcoin) vs smartphone (Ethereum) analogy and a demonstration of the power of generality...

> "Instead of having a protocol that is designed around one very small set of use cases, you just create a **general-purpose operating system** and you let people build whatever they want as applications on top of it."

Ethereum is a blockchain, with a few additions:

- Built-in Turing-complete scripting language - essentially hybrid between standard VM architectures, Bitcoin script and a "few other things".
- People can write programs in this script, or high level languages that compile down to this script, take these compiled scripts, put them into transactions and send them to the blockchain. The transaction gets confirmed and you get a special account at that address.
- Contractual accounts and Externally Owned Accounts have the **same privileges**.
- Anyone can create an application, with any rules. Anyone can then interact with that application, i.e. you can do NameCoin in 10 lines of code...

State is defined as a key value mapping addresses to account objects. Every account object has a nonce and balance. Contract accounts also include a code hash and storage trie root. Vitalik then discusses how transactions work - important low-level details for us to build a full conceptual picture in the weeks ahead.

> "You can actually think of it as being a fairly simple system. You can think of the state as being a database, and you can think of each of these contracts as being programs that are sitting on one computer, **except the computer is massively globally distributed. It's actually a highly secure network backed by tens of thousands computers around the world.** It's bold because it's important."

However, this raises the spectre of "The Halting Problem", which Vitalik explains as being solved by gas: a fee for every computational step the computer must take, where there is a limit to computational steps possible per block.

### Virtual Economy

This means there is no *technical* limit on what can be put in the `data` field of a transaction, but there is an *economic* one, as the more data you include, the more expensive it becomes. It was an extra 68 gas for every byte of data you include at that time, though it may have changed now. 

<div class="lightbulb">
💡 Exercise for the reader: how would you tell what the gas price per byte currently is?
</div>

Vitalik then discusses some of the intricacies around `v`, `r`, and `s` from elliptic curve cryptography, and how `v` is an extra field used for public key recovery. He also provides further information on receipts and logs and why logs are cheaper and allow for efficient light-client access. Although it may sound boring, this is the heart of how we build censorship resistance tools.

This is followed by a description of the **Ethereum Virtual Machine**:

- Stack - up to 1024 32-byte fields.
- Memory - just an infinitely expanding byte array, but the more you expand the byte array, the more gas you have to pay. **Most of the limits aren't static, they're economic and you'll see this idea again and again.**
- Storage - permanent for contracts. You can read and write to it.
- Environment variables - VM can access block number, time, mining difficulty, previous block hash etc.
- Logs - append-only storage in a specific block, not in state.
- Sub-calling - opcode by which VM can itself call other contracts.

Vitalik then discusses ABI and RLP (recursive length prefix) encoding "for people who are set theory geeks". It may seem boring, but it is a demonstration of the early culture and how the people who built all this stuff really think. He follows this with an explanation of memory-hard algorithms for mining and why they were an innovation. Again, worth listening to for cultural context, but 23:50 - 28:57 is now a bit outdated.

Vitalik also emphasises the fast block time (17s) and discusses uncles - which solve the "stale rates" of blocks that arise due to network latency.

He makes the critical point that merkle tries are "a construction that allows for compact, efficiently-verifiable proofs that a particular transaction was included in a particular block." It's not just transactions in the Merkle trie though; it's the state too: i.e. that storage trie root we talked about in the account object earlier.

Understanding how this particular choice of data structure allows us to succinctly express shared state reveals why intimacy with low-level technical details allows one to build a comprehensive conceptual picture of how it all ties together, and what meanings any technology can be used to build.

### Generalised Compute

So, you're less technical then Vitalik (i.e. all of us) and are wondering what this all really means? Well, the critical point is this notion of a **general purpose operating system** - one, monolithic virtual machine distributed across the world which is shared by everyone, owned by no-one and which can't be turned off without also turning off the internet. Even with Bitcoin, we got this feature that you could carry 12 magical words in your head across any border in the world, incant them into an internet-connected machine and have immediate access to value. 

Now, there is the possibility that you could pull down not just monetary value, but _generalised compute_. That is, your 12 or 24-word mnemonic could be your entire personal OS, which would be accessible from anywhere, if we can genuinely create a general-purpose shared history machine which is capable of scaling across the globe. This is Vinay's unimaginable strangeness scaled up another order of magnitude.