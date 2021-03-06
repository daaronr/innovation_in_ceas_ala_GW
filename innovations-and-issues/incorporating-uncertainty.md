# Incorporating uncertainty

### Why make uncertainty explicit?

From [`cole_haus`:](https://forum.effectivealtruism.org/posts/gMxTEMvh8RttX9Nt4/uncertainty-and-sensitivity-analyses-of-givewell-s-cost)

> GiveWell produces cost-effectiveness models of its top charities. These models take as inputs many uncertain parameters. Instead of representing those uncertain parameters with point estimates—as the cost-effectiveness analysis spreadsheet does—we can (should) represent them with probability distributions. Feeding probability distributions into the models allows us to output explicit probability distributions on the cost-effectiveness of each charity.

**A common approach:** Consider 'best' and 'worst' case scenarios for each parameter, and consider 'what if all goes best?' and 'what if all goes worst?', for lower and upper bounds.&#x20;

_But this approach is not optimal, because:_

**Either case ('all best' or 'all worst') is extremely unlikely**, and more unlikely  the more 'uncertain things there are'. (At least this is true if the random/uncertain things are independent; we can have correlated uncertainties too). \
_Consider: What are the chances of winning the lottery ten times in a row? What are the chances of getting hit by lightning ten times in a year?_&#x20;

**The details of the uncertainty matter, and may matter to outcomes:** Some 'uncertainties' are far more uncertain than others, or have more meaningfully 'long-tailed' distributions.  Furthermore, if the uncertain events are _correlated_ to one another, this leads to a lot more variance in the outcome.\
\
**There are reasonable ways of explicitly measuring and calibrating uncertainty over each parameter, and making this explicit is helpful**

****

cole\_haus again:

> From a [subjective Bayesian](https://en.wikipedia.org/wiki/Bayesian\_probability) point of view, the best way to represent our state of knowledge on the input parameters is with a [probability distribution](https://en.wikipedia.org/wiki/Probability\_distribution) over the values the parameter could take. For example, I could say that a negative value for increasing consumption seems very improbable to me but that a wide range of positive values seem about equally plausible. Once we specify a probability distribution, we can feed these distributions into the model and, in principle, we'll end up with a probability distribution over our results. This probability distribution on the results helps us understand the uncertainty contained in our estimates and [how literally](https://blog.givewell.org/2011/08/18/why-we-cant-take-expected-value-estimates-literally-even-when-theyre-unbiased/) we should take them.

###

### __[_What types of uncertainty...?_](incorporating-uncertainty.md#what-types-of-uncertainty...)

**From a table for Malaria Consortium Seasonal malaria chemoprevention** (rephrased)

| Input                            | Type of uncertainty  | Meaning/importance                |
| -------------------------------- | -------------------- | --------------------------------- |
| num LLINs distributed per person | Operational          | Affects total cost for effect     |
| deaths avert per protected child | Causal               | How effective is core activity    |
| lifespan of an LLIN              | Empirical            | Years of benefit per distribution |
| internal validity adjustment     | Methodological       | trust underlying studies?         |
| pct mortal. AMF areas v trial    | Empirical/historical | Affects size of problem           |
| value averting child death       | Moral                | Det. how outcomes become value    |

##
