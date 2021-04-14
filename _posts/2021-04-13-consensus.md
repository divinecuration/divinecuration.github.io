---
layout: post
title: "Consensus, Crypto, and Trust"
date: 2021-04-13 05:23:00
categories: [thoughts]
published: true
---

## 1.

Many of the big political questions of our times hinge on the differences between economic and social consensus (or, trustless and trustful consensus), and their relative status as coordination mechanisms in various sites of human interaction. This battle will be played out foremost in the architectures of technical systems.

<!--more-->

## 2.

In an [article from 2016](https://medium.com/@VitalikButerin/a-proof-of-stake-design-philosophy-506585978d51) laying out the design philosophy for Ethereum's proof-of-stake consensus mechanism, Vitalik Buterin argues the long-term security of a blockchain is ultimately provided not by economic incentives, but by social considerations.

> Even if an adversary had access to unlimited hashing power, and came out with a 51% attack of any major blockchain that reverted even the last month of history, convincing the community that this chain is legitimate is much harder than just outrunning the main chain’s hashpower. They would need to subvert block explorers, every trusted member in the community, the New York Times, archive.org, and many other sources on the internet; all in all, convincing the world that the new attack chain is the one that came first in the information technology-dense 21st century is about as hard as convincing the world that the US moon landings never happened.

## 3.

Buterin's assertion of the primacy of the social layer is heresy to those who find the blockchain's emancipatory potential in its _elimination_ of the social. A trustful layer is a corruptable layer, one which can be gamed and distorted. Nick Land's claim that Bitcoin is the first "intrinsically reliable record" is predicated on the unreliability of the social{% sidenote 'land' "Nick Land, [_Crypto-Current: Bitcoin and Philosophy, §0.051_](https://etscrivner.github.io/cryptocurrent/)"%}---the reliability of Bitcoin's ledger is provided by economic (and therefore transparent) mechanisms alone, including security against 51% attack. If one node does acquire enough hashpower to outrun the main chain, so the logic goes, it will always be more profitable for them _not_ to attack. According to this line of thought, Bitcoin renders the social layer obsolete.

## 4.

This dispute makes it possible to consider consensus layers as embedded within one another, forming stacks with different dependencies and affordances. The question becomes: what is the nature of the outermost layer, and how does it relate to its inner layers?

## 5.

Answer 1: Social Realism (Buterin). The integrity of the economic layer is secured by an outer social layer. The social layer is slow, clunky, and gameable, but ultimately required for long-term integrity. The value of an inner economic layer is that it oils the wheels, allowing transactions to remain safe and lively on smaller timescales. Put together, the benefits of both long-term security and short-term liquidity can be harnessed.

## 6.

Answer 2: Social Fictionalism (Land). There was never any true social layer, only more tacit and less distributed{% sidenote 'hayek' "And therefore less efficient, for [Hayekian reasons](/assets/pdf/hayek-use-knowledge.pdf)." %} economic layers. Social institutions never really operate on trust, but as Leviathans which monopolise the use of coercive power to skew economic incentives towards cooperative outcomes dictated by the elites that run them. The choice between social consensus and economic consensus is an illusion---there are only different forms of economic consensus. Nakamoto consensus (etc.) should be lauded as maximally distributed and maximally explicit. Those still beating the drum for the social layer betray an illiberal impulse to re-centralise and re-mask power.

## 7.

Answer 3: Social Historicism (Baudrillard). There once was a social layer, but now there is not.{% sidenote 'macintyre' "Baudrillard is here read as generalising something like Alasdair MacIntyre's historicist meta-ethics, i.e. that emotivism is true now but wasn't always." %} The outermost layer, which can never be fully explicit{% sidenote 'sellars' "See e.g. Wilfrid Sellars, [_Some Reflections on Language Games_](/assets/pdf/sellars-games.pdf)." %} (which is why it is possible to disagree about what it is), has changed over time, its social structure swapped out for an economic structure. In Baudrillard's terms, the spread of the commodity-form to the symbolic economy has remodeled social ties as professional ties, unconditional pacts replaced by instrumental contracts at the deepest level. If Buterin is right that the social layer is required for consensus integrity, then integrity is impossible given current conditions. Neither will the emancipatory trajectory promised by Land's maximally explicit economic consensus ever materialise, because this whole picture depends on a failure to appreciate the significance of the unconditional authority structure of the social layer for cooperative reasoning.

## 8.

Why is the social layer important? What can a trustful consensus achieve that a trustless consensus cannot? As Scott Alexander [puts it](https://slatestarcodex.com/2014/07/30/meditations-on-moloch/), purely economic governance mechanisms are susceptible to capture by multipolar traps (prisoner's dilemma, Malthusian decline, tragedy of the commons, etc.).{% sidenote 'multipolar' "See [Invisible Hand Fail Modes](/2021/01/29/nash.html)." %} To start replacing human interaction with cryptographic mechanisms which do not support anything other than economic consensus (by design, no less) is to willingly place ourselves in a Malthusian death spiral. Baudrillard's point is that this has _already_ happened with the commodification of the symbolic economy. Given these initial conditions new forms of cryptographic governance can only accelerate the process. Scott Alexander seems to agree on this last point.

## 9.

Trustless consensus is agent-mediating; trustful consensus is agent-constituting. Where an economic mechanism finds compromise between multiple distinct agents, a social mechanism integrates distinct nodes into a single super-personal agent via the trust operation---i.e. through mutual recognition.{% sidenote 'brandom' "See e.g. [Self-Consciousness as Reciprocal Recognition](/2020/07/31/brandom-recognition.html)" %} Social consensus is a property of a recognitive community; economic consensus of a strategic alliance.{% sidenote 'conversation' "See also [In the Place of Conversation](https://samuelludford.medium.com/the-space-of-conversation-b91c5413bf86)." %} Economic mechanisms converge on Nash equilibria, social mechanisms on [Kantian equilibria](https://www.jstor.org/stable/40587794?seq=1).


## 10.

Put differently, an economic consensus can only take shape where future uncertainty is locally quantifiable. Since economic mechanisms mediate local decisions they cannot integrate global values by definition---when future pay-offs are unquantifiable from local perspectives no consensus can form around them, even if the cost-benefit analysis is stark from the global perspective. This is significant in e.g. questions of existential risk, such as climate change, where local uncertainties are unlikely to become meaningfully quantifiable until it is far too late.


## 11.

Social consensus solves this problem with a distributed and explicit trust mechanism. Since local decisions aren't caveated by forecasted value extraction, they are counterfactually robust, producing the we-perspective via an implicit suspension of self-interest.{% sidenote 'hayek-2' "Hayek's argument that this is necessarily inefficient because it throws away local information only makes sense if a prior and fixed system of preference-bearing agents are presumed. But this is precisely what cannot be presumed, since what is under consideration is production of the community as a social actor---that a social consensus throws away local information is just to say that a community value overrides at least some individual preferences. But this is a desiderata, not an inefficiency---it is the very property _required_ by coordination against multipolar traps." %} (It is hardly a criticism to point out that trust mechanisms can be gamed---if a trustless mechanism cannot be gamed in the same way it is because it lacks certain capabilities, not because it is more capable.){% sidenote 'euclid' "An analogy could be made with Gödel: 1st-order arithmetic is incomplete, but Euclidean geometry is complete. However, the reason for the discrepancy is simply that 1st-order arithmetic is much more expressive than Euclidean geometry, and it is these extra expressive capabilities that are turned against it by the incompleteness theorem. Similarly, it does not follow from the fact that social consensus can be gamed that economic consensus is more capable---the fact that it can't be gamed may rather point to a _lack_ of capacity." %} Conceived this way social consensus is neither centralised nor tacit. Perhaps Land is right that institutions have often been (perhaps always have been) masks for coercive power, but if so then these are not social mechanisms. The use of coercive force is not an exercise of authority but a failure of authority.

## 12.

If the outer layer is mutable, then Baudrillard's local pessimism points the way to global strategies. What is mutable can be engineered. Seduced by the pure fungibility of trustless interaction---a whole world turned to liquid---the slide from the social to the economic is a monstrous devil's bargain: the collective decision to abandon the labour and obligation of collectivity. If the crytographic revolution marks a major landmark in the engineering of trustlessness, then to move human interactions onto these media is to black-box trustlessness as such---to move it into the outer layer, accelerating the dissolution of the social into the economic. This is both the promise and the peril of technology---to both explicate (make-explicit) black-box (make-implicit). To externalise a memory and then _forget_ it.{% sidenote 'steigler' "C.f [_Yuk Hui on Technics, Time, and Geometry_](/2020/09/26/hui-technics.html)" %} To do so is to engineer the social unconscious, to mutate the implicit outer layer which shapes action indirectly. But if it is possible to engineer a trustless outer layer then, by the same token, it is in principle possible to re-engineer it as trustful.
