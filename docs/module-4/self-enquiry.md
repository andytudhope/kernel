---
title: Who Are You?
description: We summarize a classic Vinay Gupta essay on identity and the technical problems we'll face over the next 50 years as we try and figure out how to reveal only what we absolutely must in order to relate valuably with others.
image: /assets/shares/better-questions.png
---

# Who are you?

Almost everything we've discussed so far - [trust](../../module-0/trust/), [value](../../module-1/value/), [meaning](../../module-1/meaning/), [speech](../../module-2/money-speech/), [freedom](../../module-3/freedom/), [intention](../../module-3/intention/), [humility](../../module-3/humility/) and [art](../art/) - depends in some way on the question of identity. The <a href="https://web.archive.org/web/20181024152027/http://www.whitepine.org/wildways.pdf" target="_blank">Wild Ways</a> of Ikkyu explain best:

*No masters only you the master is you.*  
*Wonderful, no?*  

–

*Only one koan matters*  
*You*  

<div markdown="1" class="card half sidebar center gemoji center-content center">

<div markdown="2">
![Tell Me Who You Are!](./img/who-are-you.png)
</div>

<div markdown="3" class="curated-link">
<a href="https://medium.com/humanizing-the-singularity/part-i-are-you-sure-you-exist-we-are-5cfe13ab488c" target="_blank">Read It</a>
</div>

</div>

<div markdown="1" class="clear"></div>

## How does this fit into Kernel?

This essay has been chosen because it identifies a critical practice of the internet age: personal identity. In particular, it will help you deepen your own approach to 

1. Asking informed questions
3. Censorship resistant and future-proof thinking
4. Incentives and seeing how they effect literally everything
5. Understanding the underrated importance of accountability

## Brief

> *"<a href="https://www.youtube.com/watch?v=r5kmCgVhADY" target="_blank">Who are you</a>? A complex construct inside of the head of a naked ape that looks at the sky and wonders, or are you the sum total of your mortgage payments?"*

Vinay begins by describing the seven buckets within which identity is thought of by most people building products around this mysterious phenomenon: a physical body, government records, attributes/reputation bestowed by a community, a username/password combination, ownership of a keypair, a persistent sense of self, or a metaphysical construct. He outlines the basic problem in a way which should be deeply familiar by now:

> "The case that I’m going to make is that the identity debate is magnetically drawn to two opposing poles:

> 1. Humans as *things* identified by their bodies, vs
> 2. Humans as intangible, ever-shifting narrative beings

> "Our job, as software engineers working on identity, is first to <a href="https://sfhfoundation.com/audios/series/self-knowledge/" target="_blank">be philosophers who understand the abstraction</a> that we hope to represent."

He goes on to discuss experiments like the Enlightenment Intensive and their ancient correlates in traditions like Zen Buddhism in order to illustrate the point that:

> "Identity is a deeply secret and mysterious thing for us, and staring right at it for long periods of time is the lifestyle preference of poets, saints, and madmen [...] They’re things we do, or conditions we experience, relationships we participate in, but **the sum of all the roles we play seems to fall short of describing the totality of our identity.** Even when all the parts are put together, there is something indescribable in the whole."

This is great for philosophers, poets, and madmen, but what about the poor software developers on this course?!

> "For now, let’s assume that software isn’t going to help us much with metaphysical or deep psychological models of our identity. What are the areas where software is doing a good job of describing identity? Let's look at four cases:"

1. **Credit Ratings** - sum up huge amounts of information about your financial (and perhaps social) behavior, and reduce it to a number which estimates risk of default. The problem is that in any model of “people like you,” every data point is a cultural decision about whether, for this person, the value is True or False. So we must ask: is information about “people like you” also information about you, or is it simply an accumulated stereotype?
2. **Social Networks** - i.e. the maps of who we read, write messages to, and consider ourselves kin to. The ghostly spirits of these micro-societies inform important parts of our identity and allow us to have conversations not otherwise possible: "there are things I will simply never hear myself say except as part of a discussion with those little square faces." Which is strange, because this "intersubjectivity exists inside of a platform that I have very little control of. It feels like a piece of my identity which is held hostage and at risk: if Twitter goes away, a piece of my political voice ceases to exist."
3. **Names** - "[Documentally](http://documentally.com/) is a good example, in that people use his given name with a certain strangeness, a sense of referring to something not quite for public use. The man and the brand are interpenetrated." Vinay goes on to talk about the brand of *Linus says...* and the effect it's had on software development. "A collection of identities more or less like Linus more or less run the internet — systems like the IETF probably could not function without the tools that support these blended representations of identity and authority."
4. **Surveillance Databases** - "What’s interesting about this version of our identity, apart from its completeness, is that we — the subject — cannot see it. We can infer from the Snowden revelations that the national security databases have access to most or all of our social media, web surfing habits, financial and health records and more [...] This is an identity not made of what we know, but of what others know about us."  

These all frame deep questions about how, when and why identity and software intersect.

1. Is information about you, which you have no access or control over, part of your identity? Or is that information somebody else’s story?
2. How does unconscious knowledge about us and our behavior factor into our identity? There are lots of things that we do not know about ourselves, but that others know about us, that are clearly parts of our identity from their perspective, but outside of our awareness.
3. The algorithms used to cluster people by modern institutions **actually create** large parts of the “identity” which is being stored about us.

### The art of the possible

This might seem like a giant ontological mess - and it is - but

> "if we understand that identity is a set of narratives that rely on culture to be effective, we can talk about what narratives are useful and reliable, and try to construct purpose built ones that help us relate to strangers and make the queues at airport immigration move more quickly."

To construct the beginning of such a narrative, Vinay asks what is simple and clear in the identity space, and considers the limited attributes we have at birth. The first attributes we are given by others in the modern world generally make up our medical history and the

> "attribute-free happy child becomes wrapped up in an entire world of data, identity, relationship and rights. None of this is endogenous — our baby has not generated all of these relationships, data and identities by will."

While this may seem problematic, the system often saves lives based on such data-wrapping, and Vinay notes that as unsatisfying as “identity” might be conceptually, there is no denying that in a variety of critical places, the current identity infrastructure *works*.

He then discusses the origins of identity as a username-password combination. This worked well in the early days of the internet when there was a clear chain of accountability, but fell apart during the <a href="https://en.wikipedia.org/wiki/Eternal_September" target="_blank">Eternal September</a>. The critical point in this section revolves around **accountability** - a concept we don't pay nearly enough attention to online.

> "The result of this breakdown in accountability (a breakdown in the personal relationships between individuals using and providing internet access) was a deep and near-permanent change in the lived experience and culture of the internet."

Vinay then spends some time talking about identifying machines; MAC numbers; keypairs on your SIM card; and the DNS system, run by IANA. All of which work, to a large degree because they have to in order for the companies built on top of them to get paid, and because there is very little commercial competition for things like MAC numbers. So, we can identify machines fairly well (we'll return to DNS and HTTPS). Back to humans for now.

Biometrics are appealing, in that they are not necessarily tightly associated with a State for issuance. However, “you only get one face" or fingerprint and it is easy to exploit. People can make good-enough replicas of your features to break biometric authentication and then it is broken for good, unlike a password which can be changed. But what about DNA?

While this is a perfect identifier - and offers a bunch of additional information about family, ancestry, health etc. - it is not private. Your DNA gets everywhere. And this points to a profound problem we will increasingly face with identifying technologies:

> "Over and over, with biometric information, we are going to discover that the data itself is harmless, but the ability to compare the data with data from other sources is dangerous [...] being networked is a whole different story."

There are many potential harms which arise from DNA, and Vinay claims that it will likely be "a defining quandary of the 21st century." This can be partially solved by hashing DNA sequences, though this is also not without its problems. All of which is to say that:

> "We can be sure that handling personal DNA records is going to be at the core of the hardest problems in future privacy systems. It’s also likely to be at the nexus of interests who want to be able to uniquely identify humans."

Having covered the full landscape, Vinay turns to the intersection of biometrics and blockchains. The problem is that the model of identity encoded in Bitcoin revolves around cryptographic keypairs, which give us anonymity (or at least pseudonymity). You need never meet the other person to trust in the relevant properties of a transaction. This is great for many applications, but interfaces poorly with our current ID systems. Moreover, if we link your real name to a secret key, and then put all the actions taken with this secret key into a blockchain, you have zero privacy.

> "When these two models collide, what’s left is a kind of panopticon: a permanent record, tied to your real name, in a medium which cannot be erased. The 'web of trust' and 'the blockchain' are fundamentally different models of privacy [...] The 'public profile on a blockchain' model just does not seem to have the kinds of properties we want our societies to have."

So, what are our options for future-proof identity which works for, rather than against, us?

#### 1. **Total transparency** 

Which will lead us into Genetic

1. Screening - think Tinder, but more scientific swiping/swabbing
2. Identification - think global surveillance, but even more effective
3. Research - think happier thoughts like open data

Though this may seem strange now, we will likely get used to it, as we have grown used to each click being analyzed, or climate change, or any of a number of other crazy trends. In among all the potential negative side-effects, **here is the most important point for you**:

> "This is the role of critical technologists — to understand that we have choices, that each technology comes with a set of decisions about how we will integrate it into our lives, societies, and culture [...] We must negotiate with each incoming possible future, and individually or collectively adopt or ignore the offers that these futures make us."

#### 2. **Blockchains, biometrics, encryption**

Apple Touch ID meets Bitcoin may seem convenient now, but when each technology independently matures, the intersection between them becomes huge and intrusive. We can potentially work with biometrics and lots of other personal information (like spending records) on a blockchain, but encrypt as much as possible as we go. However, it's likely that both our current cryptography - and understanding of computing power - will be obsolete sooner than we think. That is, if we put sensitive information on a blockchain and encrypt it, it is unlikely we can encrypt it well enough to keep it safe for even the next 30 to 50 years.

#### 3. **Wise as serpents**

We have arrived at the crux of the whole essay, which boils down to these three questions for future-proofing our systems:

1. What does the world really need to know about us?
2. What do specific agencies really need to know about us?
3. Can we get through life revealing less about ourselves, using these technologies?

If we consider these closely and agree that putting identifying information on chain - even if its encrypted - it's not such a hot idea, then we can get to what Vinay calls

> "A **transactional vision of the blockchain**: something that’s a little less about storing the entirety of our being on a permanent record, but more focused on disclosing the minimum required for people to be able to do business (or other critical functions) together [...] Every piece of personal information about you is stored with a different public key: you have a big keyring, and each key reveals only a single fact."

If you think back to [Understanding Ethereum](../../module-1/understanding-ethereum/#generalised-compute) and using a mnemonic to access not just monetary value, but an entire personal OS, then put this together with Vinay's essay and a service like ENS, you begin to see that **your name is your mnemonic is your OS.** Each sub-route under it controls different aspects of your identity, with different kinds of contractual requirements to access it. We can enforce highly secure, multi-party requirements for private information and what we now call wallets; and something more like SSO for social profiles, job hunting, contact details etc.

### Identity we can live with

> "We have to be person-centered if we want to find a stable point which will survive the extremely rapid rates of change which are so much a part of our twenty first century. Put the person in the middle of the story, and work out from there, and generally speaking technological change will not break your model.

> "I believe in a simple division of the identity space into two parts.

> 1. Profiles
> 2. Actions

> **Profiles** are a set of stories that somebody has about me. These might include things like medical records. I’m describing these as stories because I, as an individual, have no idea what is in your profile of me. I cannot validate it. I might not even know it exists, and it might be filled with utter nonsense. Your profile is your business, even if its about me.

> **Actions** are a log of the places where I have made choices. These would typically be key life decisions, like signing an employment contract or mortgage, where the evidence that the signature was valid and accepted is a visible flow of money, ideally across the blockchain itself. In all cases actions ideally lead to a stream of payments into or (better still) out of an account, something which shows that the contract was actually performed."

This is a simple, but profound way to consider a very complex problem. Currently, profiles and actions are inextricably mixed up, because someone else needs to verify your actions.

> "On a blockchain, because my actions are self-certifying, like **performative speech acts**, I can present you with proof of what I have done without any third party having to vouch for me. This identity is all mine: self-sovereign."

If you've made it this far and [remember](../../module-3/remember/) what Andreas and Nick have been saying about [money as an ancient technology](../../module-2/shelling-out/) which birthed writing; [money as a language](../../module-0/money-language/) which nobody owns or controls; [money as a protocol anyone can engineer](../../module-2/engineering/), you'll realise that one of the most interesting things that falls out of this [unimaginable strangeness](../../module-1/promise-blockchains/) is the ability to [speak clearly](../../module-2/money-speech/) and in your own voice (i.e. with your own value) about who and what you are. We are only just beginning to scratch the surface of this unassailable fact.

Of course, not everything fits neatly into profiles and actions. Vinay discusses "privileged profiles" made by those you trust more than me - i.e. Harvard University - and then goes into the intricacies of HTTPS, key management and Certificate Authorities as an anti-pattern.

### Bringing it home

> "If we do not find a compelling alternative to profile-based identities, we are going to live in a world in which we exchange constant surveillance for services, from Facebook through to our own governments. The convergence of interests between national security and advertising is
one of the most unholy pacts made in our time."

To get out of this hole we have to find:

1. New way of paying for services, and
2. New ways of identifying ourselves

> "I’ve made the case that **action-based** rather than profile-based identities are possible for a large subset of adults [...] The result of this 'wise as a serpent' approach might be a mixed ecology of identity solutions, which serves us well enough to navigate around our world, without opening up some of the scary terrain which surrounds us [...] What is not disclosed can be disclosed in future, but what is published now is published forever, encrypted or not."