---
description: Stating these models as clear mathematical equations and breaking them down
---

# Givewell models in explained maths

## All models - basics

## Give Directly

{% hint style="info" %}
&#x20;Note (DR): the equation below can and should be massively simplified and made clearer. Some tips on this in the fold. I made a start to this below. \
****\
****Note that the equation interface here is limited, at least in the interactive version (e.g., how do I do multiline equations)? ... I recommend writing equations elsewhere and moving them here.&#x20;
{% endhint %}

$$
value/donation =
$$

$$
\ln 2 \times \frac{p}{s} \times ...
$$

$$
\Big[\Big( PV(c, n - 1, -(\ln(b + \frac{s}{h} i r) - \ln(b))\Big) + ...
$$

$$
... + \ln\Big(b + (\frac{s}{h} (1 - i))\Big) - \ln(b)\Big]
$$

****

_**Where**_

p = percent transferred, i.e., 'how much makes it to recipients after admin, leakage etc')

s = average size of ~~donation~~ (transfer to household?)

~~g = Value lost to negative spoiler~~ _DR: I don't see this anywhere_

PV = Present Value function, as represented in excel&#x20;

c = discount rate&#x20;

n = duration of investment&#x20;

h = average household size \[DR: flag -- something possibly weird here -- smaller households mean greater benefits and greater cost-effectiveness ... in such a strong way, with no countervailing 'but we are helping fewer people' thing?]

b = baseline consumption (?in absence of transfer)

v = amount of investment returned (at end of investment period?)

i = percent of transfer invested&#x20;

r = ???



### Side discussion: how to simplify and give insight to equations: 

Some useful techniques for legibility:

1. Use spacing and multiple lines carefully and cleverly&#x20;
2. Use 'large parentheses' _****_ and other shapes of braces ... in latex, `$\Big( x+3 \Big)$` etc for outer terms ... more examples below
3. Factor common terms out where possible (at least if it doesn't destroy intuition)
   1. Sometimes re-expressing things in negatives or reciprocals can aid this
4. Name variables in ways that are easy to connect to the thing they represent&#x20;
5. Under-braces with labels and explanations can be extremely helpful (see examples below)
6. Define intuitive _combinations_ of the elements and break these out to make the equation simpler... (but also make it very quick to see and easy to remember what these represent; so-so example below, from another context)

### Examples _ **(**_**latex code to be shared later where absent)**

_**Multiple sizes of and shapes of braces, brackets, parentheses**_

_****_$$\begin{align*} \Omega(q(\gamma), q(\beta)):=\sum_{s, \sigma} P(s, \sigma)\Big[ q(\sigma)W(e, s)+(1-q(\sigma))W(ne, s)\Big]. \end{align*}$$_****_

_****_

![](<../.gitbook/assets/image (9).png>)

_****_

_**Defining and separating out terms**_

![Defining and separating out terms](<../.gitbook/assets/image (8).png>)

_****_

_**Underbracing and grouping for explanations**_

![](<../.gitbook/assets/image (6).png>)

_**Combining these methods:**_

![](<../.gitbook/assets/image (5).png>)

![](<../.gitbook/assets/image (1).png>)



