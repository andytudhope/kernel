---
title: Engineering Money
description: Andreas Antonopolous describes the three features of money - store of value, unit of account, medium of exchange - making the point that we have moved from having to compromise based on what we find in the world around to an ability to engineer the medium itself to meet our preconceived needs, such as a universal ledger of transactions and who can guess what else.
image: /assets/shares/giving.png
---

# 💎 Engineering money

<iframe class="video-frame" src="https://www.youtube-nocookie.com/embed/MxIrc1rxhyI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This Andreas Antonopoulos talk goes into more detail about the critical features of money and what being able to engineer them really means. We consider it to be one of his more profound and less well-known presentations.

We've now covered the collectible story of money, the links it has to reciprocal altruism and the influence this has had on our evolution as a species, and the importance of closed loops of circulation and lowered transaction costs. We've looked at the alternative story of debt, the deep mythic and religious roots money and morality have in our human story, the link between physical currency and violence, and ancient virtual monies and global trade networks. Now it's time to get down to engineering truly beneficial protocols for the creation and distribution of value.

## **How does this fit into Kernel?**

This has been chosen for Kernel, in particular, because it speaks directly to:

1. **Value** and how we can use technology to engineer its creation and distribution.
2. What **money** as a protocol really means for engineers capable of writing economic code.
3. How we can rethink **incentives** now that we have overhauled the control architecture of money.

## Brief

> "**Money is the killer app**. Money is the killer app because it is the foundational technology for all commerce and, as such, touches everything. In order to make all the stuff that is beyond money - the "blockchain" applications - work as neutral, open, decentralized platforms, we need to transact with a neutral, global, decentralized currency. You can't do the commerce, the trade, the identity, the land registry, the *everything else* without first having the foundation of a fundamentally new way of doing money which is open, borderless, decentralized, censorship-resistant and global."

Remember, what money-as-a-protocol really allows us to do is program incentives at scales never before possible. Yes, this means that there are all sorts of interesting high-level use cases to go after, but it also implies that the only way genuinely to do so is by thinking about the incentives which underpin whatever you want to build. 

<div class="lightbulb">
💡 If you're not altering the incentive structure on which your society runs, you should probably just use a database.
</div>

> "One of our biggest problems is understanding the terms we use, and *money* is probably the most relevant example of this. Very few people understand what it is and how it works. 'Money' as such is not a definitional term, it's really a general classifier."

Here follows an in-depth discussion of the critical features of money: store of value; medium of exchange, and unit of account. "Money" describes things which exhibit some behaviour that allows us to use that thing for one or more of the above purposes. Most importantly, there is always a trade-off between the three. Gold is a great store of value, but a lousy medium of exchange. Visa is a great medium of exchange, but not really a unit of account, or a store of value (as it generally represents a form of debt). When you throw tokens on a blockchain into the mix, things become really confusing, and this is because we're using a descriptive term - "money" - without differentiating between its actual uses.

How do we decide which "things" satisfy the trade-off between these three critical features in the most optimal way? We consider: scarcity, portability, durability, fungibility, divisibility, acceptability and stability. In this context:

> "Metals aren't very good money, because they have some intrinsic value which is separate from the money it represents. Silver and gold can be traded independently for aesthetic reasons or other purposes. **This destroys its fundamental function as a medium of exchange.**"

This is a profound point: most people will tell you that intrinsic value is *required* to make money "money", but the truth is almost the exact opposite. Money is an abstraction, which allows us to speak meaningfully about the value of different items otherwise unrelated. If the medium we use to express such transactional relationship has its own intrinsic value, it is not a very functional abstraction.

### Changing the nature of control

> "Metals represented for humanity an era when we used the materials we found around us in the world and adapted them to the uses for which they fit [...] Human beings looked around at found objects in the world and asked 'How do we take these materials that we have and find suitable uses for them?' At this point, we were adapting nature to the uses that we had, but only in a peripheral way. Gradually, we became more intrusive in our adaptions and started *molding* nature to our needs. We began interacting with nature at a molecular level, turning wood into charcoal, or metal into alloys with unique properties better suited to our needs. Then came the ability to effect the atomic nature of materials: synthetic fertilizers, fabrics, and plastics etc. This is no longer about just finding materials and adapting them to our needs; it's about creating materials which fit uses we have *preconceived*. Today, we can effect the subatomic structure of things - manipulating nature at the nano scale to create carbon nanotubes etc. That is, we are not just manipulating the atomic behaviour of materials; we are giving them new physical properties.

> "We just did something similarly amazing to money. Until now, we have taken money as it exists in the world, accepted the trade-offs different kinds imply between the three critical features and used it as best we can. We accepted the compromise implicit in each type because we could not change its fundamental nature. Take paper money: great medium of exchange and unit of account; really terrible store of value because of its **control architecture** (don't tell your kids what inflation really does!). We adapt our uses to the material, and not the other way around. **Until now, because now - for the very first time - we can engineer the fundamental properties of money**."

Because the protocols for communicating value are now completely abstracted from the value  which they communicate, we can create the properties we need, as opposed to adapting the ones implicit in any physical media. It's debatable whether this 'engineered money' has served as a good medium of exchange and unit of account so far. This is because these two features have as much to do with social contracts and the unit in which we choose to measure as they do with technical protocols. Andreas' argument is that we can use abstract monetary protocols which we can engineer gradually to change higher-order social contracts.

### New conversations

> "Now that we don't have to adapt to compromises, but can engineer trade-offs away, how about we invent some characteristics of money that have never existed before? For instance, our money is now also a universal ledger of transactions. A trackable, auditable ledger that can tell us where money has been and what is has been used for. Or not. Because we can tweak the privacy dial and say individuals should have privacy and governments should be accountable. **We can reset that societal conversation**."

Again, this final sentence may seem glib, but it's an important point. We can literally reset society-level conversations because there has been such a profound innovation in the media through which we communicate value. What powerful narrative will your work speak accountable, public truth to?

> "One of the results of compromising with the forms of money we use is that it is very difficult to move between the choices you make: if you want to move between dollars and gold, it's not a trivial procedure. However, if you want to move from a fully digital, owned asset that is a perfect store of value, to a fully digital, owned asset that is a perfect medium of exchange; you can now do that. Instead of trade-offs, we can just trade. I can disaggregate the fundamental properties of money, on demand: even better, my wallet can do it for me, intelligently."

The technology of money, at base, has always been composed of a system of symbols that allows us to communicate value to one another. What is at issue with compromised versions is the control architecture required to navigate said compromises. Upending control architectures might sound like a good thing to do and, in principle, it is, but remember:

> "This morning someone said, 'Disrupt yourself!' Bullshit. Disruption isn't comfortable or easy. Disruption means losing your job; it means cannibalizing your profit centre; it means destroying your business. You don't do that to yourself! You act like Kodiak - invent digital photography in the 80's and then bury it and pretend that no-one knows, only to get upended by Nokia who shipped a billion cameras, and they're not even a camera company [...] Engineered money, built by a rag-tag crew of anarchists, cypherpunks and misfits who don't care about your business plan, or about being legitimized by regulators, is similar. These people have, for years now, being laying down on the ground **unassailable facts** faster than anyone can keep up with."

What makes one man's fact another's fiction? Arguably; interpretation. However, when you can engineer the linguistic protocol which communicates value between people, and create a common standard for interpretation - i.e. a language compiler which produces the same output whenever you feed it the same code - you get to what Andreas is talking about here: unassailable facts that do no rely on any control architecture. They are true by virtue of the language in which they are expressed, not because anyone in a position of authority said so.