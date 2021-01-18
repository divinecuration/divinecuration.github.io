---
layout: post
title: "Note on Category Theory"
date: 2021-01-15 05:23:00
categories: [thoughts]
published: true
mathjax: true
---

This is a quick summary of a few points I found striking in a brief high-level dive into category theory. I first has some contact with category theory several years ago while studying computability, logic, and set theory. At the time I had some difficulty seeing what conceptual resources it could offer (to either the foundations of mathematics or philosophy) that weren't already present in set theory. Recently there's been several strings tugging at me to take another look at it---[relationships drawn between Kant's logic and type theory]({{site.baseurl}}/assets/pdf/lof-synthetic-a-priori.pdf), for example, or Badiou's appeal to topos theory in the Logics of Worlds (which I have not read).

A cursory dig around some of the material has been enough to provide a much better grasp on what it can offer. One really great resource has been Tom Leinster's [Basic Category Theory](https://arxiv.org/pdf/1612.09375.pdf), which gives (among other things) a good account of what is missing from the standard set theoretical foundations of mathematics.

One major problem with set theory is that it has no type system. In set theory, _everything_ is a set: integers, reals, functions, relations, tensors, etc. What this means is that a load of statements that ought be nonsensical end up making perfect sense. For example, \\( \mathbb{N}\in\leq \\) is a perfectly meaningful statement in the set theoretic context. Worse: not only does a meaningless statement like this have a truth value, but this value depends on arbitrary implementation details---in how one chooses, for example, to define one's ordinals (as one does).

A categorical approach to sets apparently avoids this flaw. In set theory, what characterises a set is the elements it contains, i.e. the membership relations it stands in to other sets. "Membership" is the primitive relation that set theory uses to define everything else, including functions. (In set theory, a function \\( f:X \to Y \\) is just a subset of the Cartesian product \\( X \times Y \\).)

The penny-drop moment for me came when Leinster shows how category theory allows us to reverse this order of definition, instead taking functions as primitive and using them to characterise the elements of sets. Take the emptyset \\(\emptyset\\), for example. The standard emptyset axiom of ZFC set theory characterises this set with the membership relation:

<p align="center" markdown="1"> \\( \exists x \forall y (y \notin x) \\)</p>

The emptyset is the unique set with no elements (it is unique because there's only one way to have no elements). The categorical way of doing this is really rather neat. Intuitively, a function between sets maps the elements of one onto elements of the other. Since the emptyset has no elements, a function from the emptyset to another set has nothing to do. And since there is only one way to do nothing, there is one and only one function from the emptyset to any given set. This means that in categorical terms, the emptyset can characterised as the unique object \\(A\\) in the category of sets with the property that for all other objects \\(B\\), there exists one and only one map from \\(A\\) to \\(B\\).

This is just the first in a ladder of extremely clever and elegant constructions that recovers all the expressivity of the ZFC axioms by recharacterising them in functional terms. The one-element set, for example, can be be characterised as the object \\(A\\) with the property that for all objects \\(B\\), there exists one and only one map from \\(B\\) to \\(A\\). (This captures the idea that there is only one function to a one-element set from any other set, namely the function that maps all elements in its domain to the unique element in its codomain.) The maps from \\(A\\) to \\(B\\) can then be thought of as the elements of \\(B\\) (since the functions from a one-element set to any other set correspond exactly to the elements of that set)---and so on.

This has impressed on me how category theory can meaningfully rework the set theoretical foundations of mathematics. The payoff here is that since category theory builds in a well-defined notion of function composition, it will end up with a well-defined type system as well---thus fixing one of the major problems with the standard set theoretical approach.

Informally speaking, category theory characterises things in terms of what they do (functions), whereas set theory characterises thing in terms of what they are made of (elements). This ties in fairly directly with the kind of concerns Brandom has in his development of _inferentialism_, and its origins in certain Kantian ideas.

According to Brandom, Kant is responsible for the idea that concepts can be thought of in terms of functions between judgements. Rather than the atomistic picture which sees judgements as built from concepts (which are themselves made up of other concepts, a stack which must inevitably bottom out in some primitive concepts), the functional picture takes the judgement as primary unit of thought---as the smallest thing which one can be responsible for (much as Wittgenstein identified the sentence, not the word, as the smallest thing with which one can make a move in a language-game).

We can think of atomistic picture as being like a set theoretic approach, with its construction of higher level concepts and judgements on top of a base set of simple primitives (what these primitives are is, of course, the question that has always plagued this approach). Kant's functional approach---that concepts are individuated by the role they play in inferential relationships between judgement (functions)---has far more affinity with the categorical approach.
