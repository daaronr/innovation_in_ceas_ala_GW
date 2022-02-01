---
description: >-
  Explaining and showing the state of GW model and presentation, and noting how
  it might be improved
---

# Limitations of GiveWell

_(Discussion in progress)_

Givewell presents a model that is transparent and explained in some detail. However, it is not as easy to follow as it might be, and in some ways difficult to adjust, check, or run simulations on.&#x20;

They produce and share their model in Google spreadsheets such as the one [HERE](https://docs.google.com/spreadsheets/d/16XOOB1oWse1ICbF0OVXUYtwWwpvG3mxAAQ6LYAAndQU/edit#gid=1377543212), which I've 'forked' [HERE](broken-reference) to be able to comment on and play with. Note that you need to copy ('fork') it to be able to view the underlying formulas. \
\
The calculations are done in the various cells of the spreadsheet. The formulae look like:&#x20;

![](<../../.gitbook/assets/image (1) (1).png>)

GW provides a route to specifying your own moral weights and discount rates, involving a blank row and changing an indicator in a dropdown. This then permits you to see the "results" on another sheet. You can go back and forth to see how these change, or how it compares to GW.&#x20;

However, it's not easy to see and compare this 'all in one place'.



**Limitations (which can be addressed by our proposed approach)**

1. The modeling and presentation is not terribly succinct. It stretches over multiple pages, sheets, and rows, and to get all the details requires some amount of 'clicking and chasing and following footnotes.'  It's hard to find _explicit statements of the relevant equations_ and to compare these across models. Further muddling the reader, there are elements in the spreadsheet that actually do _not_ affect the final outputs ... such as 'amount donated'. &#x20;
2. They don't explicitly model and present and present uncertainty.  (see '[why make uncertainty explicit](../incorporating-uncertainty.md)' below) They don't give a 'statistical distribution of likely impact (for each charity) under explicitly stated and justified parameter distributions'.  This makes it hard for donors and policymakers to consider the 'risk versus return' of each intervention, and consider how confident they should be in the evaluations.  &#x20;
3. The model is not easily checkable for bugs, nor is there explicit code one could use to do 'type-checking' (see Pedant) and other systematic checks.  Code could also make various robustness checks and simulations easier to do, and make the work more replicable and extendable
4. While users _can_ plug in their own parameters (see '[types of uncertainty](../incorporating-uncertainty.md#what-types-of-uncertainty...)'  below), this requires a few steps ... copying the sheet and consulting certain columns, etc.  And even after doing so it's not so easy to go back and forth between assumptions and outcomes (or outcome distributions). Dashboards like the ones built into [causal.app](../../tools-and-examples/causal.app/ "mention") make this far easier.



**The current setup might lead to**&#x20;

* Unnoticed errors (see [possible-errors-and-misunderstandings-examples-from-gw-and-beyond.md](possible-errors-and-misunderstandings-examples-from-gw-and-beyond.md "mention")... to be expanded
* Limited ability for GiveWell to assess a larger set of charities without sacrificing analytical rigor. But if they can make their uncertainty _explicit_ and transparent, they may feel more comfortable considering charities with harder-to-measure and more long-range benefits.
  * Relatedly, GW may be ignoring "high risk high return 'hitspace' interventions"&#x20;
* Lack of donor, foundation, and researcher  engagement with the model,
* &#x20;Lack of confidence that people 'understand the model', people moving outside the GW model because they can't figure out how to get it to embody their assumptions&#x20;







\
\
