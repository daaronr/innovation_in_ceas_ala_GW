# Pedant

{% embed url="https://forum.effectivealtruism.org/posts/xue4yQ5rn6iDsHdmM/pedant-a-type-checker-for-cost-effectiveness-analysis" %}

Pedant has three stages -- only the first stage (type-checking) has been completed.\
There are features in Pedant that don't exist in Squiggle or Causal

* basic language, type-checking
* uncertainty ... normal
* web interface\
  \


[https://hazelfire.github.io/pedant/#/roadmap](https://hazelfire.github.io/pedant/#/roadmap)

\




{% content-ref url="../innovations-and-issues/type-checking-and-code.md" %}
[type-checking-and-code.md](../innovations-and-issues/type-checking-and-code.md)
{% endcontent-ref %}

> Pedant is a minimal math DSL. It's originally designed for use in cost effectiveness analysis. However, it can be used for any important calculations.
>
> The goal of pedant is to make sure that it's difficult or impossible to make math and stats errors, and also allow for the full enumeration of the assumptions used for a calculation. Currently, its only feature is dimensional analysis, but I'm planning to add stats and constraints on stats in the future.

{% embed url="https://hazelfire.github.io/pedant#/" %}

Pedant replicates GiveWell's analysis, e.g., for AMF:

{% embed url="https://github.com/Hazelfire/pedant/blob/main/examples/givewell/amf.ped" %}

'units' are specified up top

`unit usd people nets`

\
Vectors are specified -- for alternative scenarios?\


```
percent_of_population_under_5 = 
  [ 13629465.1519444 / 87670443.7766788
  , 2143394.87689442 / 12643148.9336671
  , 1114855.20710404 / 7921526.58517355
  , 7089749.81596238 / 41117856.2413241
  , 33521637.830718 / 214823785.7115 
  ]
```

And lots of simple functions:

```
total_adjustment_monitoring = risk_misappropriation_without_monitoring + risk_false_monitoring_results

total_downside_adjustment = 1 - total_adjustment_monitoring - total_waste_risk

total_units_of_value_generated_after_downside = total_downside_adjustment * total_units_of_value
```

I guess these functions will be checked for whether the units agree? but I'm not sure where the units are connected to the variables





