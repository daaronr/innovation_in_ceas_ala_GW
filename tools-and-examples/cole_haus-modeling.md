# cole\_haus modeling

{% embed url="https://forum.effectivealtruism.org/posts/gMxTEMvh8RttX9Nt4/uncertainty-and-sensitivity-analyses-of-givewell-s-cost" %}

### He first inputs (and replicates?) GiveWell's "deterministic functional models"

... for cash, nets, smc, deworming, and vas (?)

with code in Github [HERE](https://github.com/colehaus/givewell-analysis), e.g.,&#x20;

the parameters and calculations  of the model for bednets are in [nets.py ](https://github.com/colehaus/givewell-analysis/blob/master/nets.py)\
\
For example...&#x20;

```
def effectiveness(
    deaths_averted_per_protected_child_under_5,
    ... (other arguments used below)
):
    mortality_in_AMF_vs_study_areas = (
        under_5_all_cause_mortality_in_AMF_areas / under_5_all_cause_mortality_in_trials
    )
    mortality_in_AMF_areas_vs_study_wout_ITN_effects = (
        mortality_in_AMF_vs_study_areas
        + (1 - mortality_in_AMF_vs_study_areas)
        * percent_of_mortality_differerence_due_to_ITNs
    )
    deaths_averted_per_child_protected_after_adjusting_for_reduced_mortality_today = (
        deaths_averted_per_protected_child_under_5
        * mortality_in_AMF_areas_vs_study_wout_ITN_effects
    )
    adjusted_deaths_averted_per_child_under_5_targeted = (
        deaths_averted_per_child_protected_after_adjusting_for_reduced_mortality_today
        * net_use_adjustment
        * (1 - efficacy_reduction_due_to_insecticide_resistance)
        * internal_validity_adjustment
        * percent_of_mortality_due_to_malaria_in_AMF_areas_vs_trials
    )
    return {
        "AMF: adjusted deaths averted per child under 5 targeted": adjusted_deaths_averted_per_child_under_5_targeted
    }
```

I'm not exactly sure where and how the numerical parameters are input here.  I&#x20;



### He next incorporates uncertainty

The above, which takes the parameters of the model as arguments, is used in his montecarlo work (jupyter notebook Python-based model in Google collab:&#x20;

{% embed url="https://colab.research.google.com/drive/1TCXBi7lF69Xaaygub5HGD6-Rb6qE924e#sandboxMode=true" %}

> DR: It ran decently when I did the original model or made one change, but when I adjusted multiple parameters it hung up

I paste some of that code below:\


```
params = {
    "Moral weights": {
        "Moral: discount rate": {"lo": 0.03344, "hi": 0.050159999999999996},
        "Moral: value of increasing ln consumption per capita per annum": {
            "lo": 1.152,
            "hi": 1.728,
        },
        "Moral: value of averting death of a person 5 or older": {
            "lo": 68.0,
            "hi": 102.0,
        },
        "Moral: value of averting death of a young child": {
            "lo": 38.400000000000006,
            "hi": 57.599999999999994,
        },
    },
    
    
```

I don't remember where the 'lo' and 'hi' come from -- GiveWell? I guess the simulation will then assert and draw from a distribution, where 'lo' and 'hi' represent the endpoints, or maybe 95% CIs, or something, of these distributions. If so, and if this is done the same across all the moral and other parameters, there is obviously room for improvement.

Some more parameters, this time 'empirical' ("what are the true values of measurable stuff") and maybe 'epistemic' ('how much do we trust the evidence' ... or something)&#x20;

```

    
    "Income": {
        "Income: duration of long-term benefits": {"lo": 32.0, "hi": 48.0},
        "Income: multiplier for sharing w/in households": {"lo": 1.6, "hi": 2.4},
        "Income: increase in income from eliminating prob. of malaria infection in youth": {
            "lo": 0.0184,
            "hi": 0.0276,
        },
        "Income: num yrs between anti-malaria program and long-term benefits": {
            "lo": 8.0,
            "hi": 12.0,
        },
        "Income: replicability adjustment for malaria vs income": {
            "lo": 0.41600000000000004,
            "hi": 0.624,
        },
    },
    "GiveDirectly": {
        "Cash: average household size": {"lo": 3.7600000000000002, "hi": 5.64},
        "Cash: percent of transfers invested": {
            "lo": 0.31200000000000006,
            "hi": 0.46799999999999997,
        },
        "Cash: return on investment": {"lo": 0.08000000000000002, "hi": 0.12},
        "Cash: baseline consumption per capita": {
            "lo": 228.73600000000002,
            "hi": 343.104,
        },
        "Cash: duration of investment benefits": {"lo": 12.0, "hi": 18.0},
        "Cash: percent of investment returned when benefits end": {
            "lo": 0.16000000000000003,
            "hi": 0.24,
        },
        "Cash: discount from negative spillover": {
            "lo": 0.04000000000000001,
            "hi": 0.06,
        },
        "Cash: transfer as percent of total cost": {
            "lo": 0.664,
            "hi": 0.9959999999999999,
        },
    },
    "Deworming": {
        "Income effects": {
            "Deworming: effect on ln income in MK pop": {
                "lo": 0.1144,
                "hi": 0.17159999999999997,
            },
            "Deworming: num yrs between deworming and benefits": {"lo": 6.4, "hi": 9.6},
            "Deworming: adjustment for el nino": {"lo": 0.52, "hi": 0.78},
            "Deworming: adjustment for yrs of treatment in MK vs programs": {
                "lo": 0.7200000000000001,
                "hi": 1.08,
            },
            "Deworming: replicability adjustment": {
                "lo": 0.08800000000000001,
                "hi": 0.132,
      ... ETC
```

\
Now something magic happens... 'main' is doing something here, maybe as defined in the github repo? Not sure where the distributions are specified

```
%matplotlib inline

import main

main.main(params, num_samples=20000, 
phases={"uncertainties", "regressions", "sensitivities", "distances"})
```

It spits out a bunch of graphs. I can't remember what everything means. I think the 'value per dollar' label might be in error here

![](<../.gitbook/assets/image (4).png>)
