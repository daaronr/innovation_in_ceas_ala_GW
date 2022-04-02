---
description: >-
  ’improve GiveWell’s tools/analysis” (to permit Montecarlo, transparency, and
  allow user input of moral and epistemic parameters)
---

# Cost-Effect-Anal./"GiveWell"+: Explicit uncertainty, transparency, customizability

## This workspace

Started by **David Reinstein**, Rethink Priorities. See [who-is-involved.md](organization-and-introduction/who-is-involved.md "mention") for other contributors and discussants. The project as a whole is a joint effort with **Sam Nolan** and others.&#x20;

## Introduction

This gitbook gives the motivation for working on tooling to improve CEAs. It also attempts to lay out the current state of the research in this area...  so if you would be interested in contributing, you shouldn't have too much difficulty finding suitable work to do.&#x20;

## Why tooling for CEAs?&#x20;

Quantifying impact is a cornerstone of Effective Altruism, and currently GiveWell is what is considered a gold standard in the EA community. However, GiveWell's analyses suffer from some limitations which we believe are important for the EA community to reconcile.

1. Perhaps the most critical issue with GiveWell's analysis is that the analysis does not formally consider uncertainty. Representing uncertainty is important among EAs, particularly when it comes to determining the value of research, epistemics and forecasting (For an EA org in this space, see [QURI](https://quantifieduncertainty.org)).  More practically, representing uncertainty may will help donors and policymakers consider the 'risk versus return' of each intervention, and consider how confident they should be in the evaluations. (_See also_ [#why-make-uncertainty-explicit](innovations-and-issues/incorporating-uncertainty.md#why-make-uncertainty-explicit "mention")
2. &#x20;A second issue is that the model may have bugs in it, may input wrongly coded data, or may have internal inconsistencies. Making the computations more explicit and transparent could facilitate checking and the use of tools to improve reliability and reduce errors. See [Pedant](https://hazelfire.github.io/pedant/#/) for an EA project in this space focusing on ['type checking'](innovations-and-issues/type-checking-and-code.md).
3. The third issue is that currently the Cost Effectiveness Analysis (CEAs) provided by organizations such as GiveWell are very daunting and confusing to understand. The underlying model can be hard to tease out from a collection of cell references and formulas. Improving the way that users understand and interact with these models could improve accessibility to EAs and to the research community.

That being said, GiveWell is already a positive outlier in terms of the quality of CEAs. Our project also aims  to create tools and examples that help create CEAs for non-GiveWell organizations, particularly longtermist ones, which have often escaped more rigorous analysis of Cost Effectiveness up to now.

Specifically, this project investigates the efficacy of the following innovations:

* Representing CEAs using code (See [code-representations-of-gw-models.md](givewell-model-and-extensions/code-representations-of-gw-models.md "mention") and [pedant.md](tools-and-examples/pedant.md "mention"))
* Using alternatives to spreadsheets (MS Excel etc) for representing CEAs, particularly those that can handle uncertainty (See @Guesstimate  and @Causal.app)
* Presenting these in 'visual dashboard/BI' ways that 'make the uncertainty clear' and enable intuitive comparisons \


We further discuss this case, and responses, under:

[key-writings-and-resources.md](organization-and-introduction/key-writings-and-resources.md "mention")

[limitations-of-givewell](innovations-and-issues/limitations-of-givewell/ "mention")

... and in other sections below.\






\
