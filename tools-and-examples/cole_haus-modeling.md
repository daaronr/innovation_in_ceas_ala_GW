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

I suspect that the above, which takes the parameters of the model as arguments, is used in his montecarlo model) (jupyter notebook Python-based model in Google collab:&#x20;

{% embed url="https://colab.research.google.com/drive/1TCXBi7lF69Xaaygub5HGD6-Rb6qE924e#sandboxMode=true" %}

>
>
> DR: It ran decently when I did the original model or made one change, but when I adjusted multiple parameters it hung up
