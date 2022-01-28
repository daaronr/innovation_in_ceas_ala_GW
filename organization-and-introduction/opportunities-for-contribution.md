---
description: Here we list ways that you can contribute if you wish to this project.
---

# Opportunities for Contribution

### Trialling out Excel alternatives for GiveWell CEAs

One of the first steps in this project is to trial out using different interfaces for CEAs. This could help determine whether different interfaces could be valuable for representation.

Currently, **Sam Nolan** has created a primitive representation of the GiveDirectly model inside Causal:

{% embed url="https://my.causal.app/models/71712" %}
GiveDirectly model within Causal
{% endembed %}

There are a number of issues with this, notably:

* The documentation of the parameters only fits on one line and as of such takes up too much horizontal space, this can be fixed by using Freeform charts.
* The uncertainty on all the parameters is guessed quite vaguely, and could be improved upon if investigated.
* It would be great to also include/try creating an AMF/DtW version of this, so that it may be possible to compare different interventions.

In other work, it would be great if another representation could be done in Guesstimate for comparison.

### Improving Pedant

Pedant offers an exploration of code like languages to represent CEAs. If you wish to help develop Pedant, lo[ok at open issues on GitHub](https://github.com/Hazelfire/pedant/issues), as well as get in contact with Sam Nolan on the EA Forum, Discord, or the EA Public Interest Technologists Slack. I am currently looking for people to transcribe other models, as well as Haskell Developers.

### Guessing uncertainty in GiveWell estimates

Currently, as far as I am aware, no one is yet to attempt to properly guess the amount of uncertainty in each of the parameters in GiveWell's model. I believe [cole\_haus-modeling.md](../tools-and-examples/cole\_haus-modeling.md "mention")is the closest thing to it. Representing a GiveWell CEA (or several) with uncertainty bounds in any form would be valuable.
