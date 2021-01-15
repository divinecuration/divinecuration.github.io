---
layout: post
title: "Note on Logic"
date: 2021-01-15 05:23:00
categories: [thoughts]
published: true
mathjax: true
---

This is a quick note to summarise some points that I found striking in a quick dive into category theory. I first encountered category theory several years ago when studying set theory (in a fairly thorough kind of way), and at the time I struggled to see what conceptual resources it could offer (for either the foundations of mathematics or for philosophy) that weren't already present in set theory. Recently there's been several strings tugging at me to take another look at it---relationships drawn between Kant and type theory, for example, or Badiou's appeal to topos theory in the Logics of Worlds (which I have not read).

A cursory dig around some of the material has been to enough to answer some of the questions I didn't quite manage to ask all those years ago. One really great resource has been Tom Leinster's [Basic Category Theory](https://arxiv.org/pdf/1612.09375.pdf), which (among other things) gives a good accounts of what is missing from the standard set theoretical account of the foundations of mathematics.

One major problem with set theory is that it has no type system. In set theory, _everything_ is a set: integers, reals, functions, relations, tensors, etc. What this means is that a load of questions that ought be nonsensical end up being totally meaningful according to set theory. For example, \\( \mathbb{N}\in\leq \\) is a perfectly meaningful statement in set theory. Worse---not only does a meaningless statement like this have a truth value, but this value actually depends on arbitrary implementation details---in how one choses, for example, to define one's ordinals.

Using a categorical approach to sets avoids this trap (or so I'm told). In set theory, a set is characterised by the elements it contains (which are themselves always sets)---the _membership_ relation is the primitive relation that set theory uses to define everything else, including functions between sets. (According to set theory, a function \\( f:X \to Y \\) is just a subset of \\( X \times Y \\) which satisfies certain criteria.) The penny-drop moment came for me when Leinster shows how to reverse this order of definition, instead taking functions to be primitive and using functions to characterise the elements of sets.

Take the emptyset \\(\emptyset\\), for example. The emptyset axiom of ZFC characterised this set via the membership relation:

<p align="center" markdown="1"> \\( \exists x \forall y y \notin x \\)</p>

The emptyset is the unique set with no elements (it is unique because there's only one way to have no elements). The categorical way of doing this is really rather neat. Intuitively, a function between sets maps the elements of one onto elements of the other. Since the emptyset has no elements, a function from the emptyset to another set has nothing to do. And since there is only one way to do nothing, there is one and only one function from the emptyset to any given set.

This means that in categorical terms, the emptyset can characterised as the unique object \\(A\\) in the category of sets with the property that for all other objects \\(B\\), there exists one and only one map from \\(A\\) to \\(B\\). This is just the first in a ladder of extremely clever and elegant constructions that allows to recover all the expressivity of the ZFC axioms by recharacterising them in functional terms.

This has impressed on me how category theory can meaningfully rework the set theoretical foundations of mathematics. The payoff here is that since category theory is based on a well-defined notion of function composition, you're going to get a well-defined type system out of it as well---thus fixing some of the problems with the standard set theoretical approach.

Roughly, category theory characterises things in terms of what they do (functions), whereas set theory characterises thing in terms of what they're made of (elements). While I have not yet dug into the relevance of all this to philosophy, I can  immediately see how this way of thinking promises to link in with the kind of concerns that Robert Brandom has in his development of inferentialism, and its origins in Kant.

According to Brandom, Kant is responsible for the idea that concepts can be thought of as sets of functions between judgements. Rather than the atomistic picture which sees judgements as made up of concepts (which are themselves made up of other concepts, a stack which must inevitably bottom out in some kind of primitive concepts), the functional picture take the judgement as primary unit of thought (as the smallest thing which one can be responsible to, much as Wittgenstein identified the sentence, not the word, as the smallest thing with which one can make a move in a language-game).

We can think of atomistic picture as being like a set theoretic approach, with its construction of higher level concepts and judgements on top of a base set of simple primitives (what these primitives are is, of course, the question that has always beset this approach). Kant's functional approach---that concepts are individuated by the role they play in establishing inferential relationships (functions) between judgement---has far more affinity with the categorical approach.
