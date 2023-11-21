---
layout: page
permalink: /notes/index.html
title: Notes
---

# Economic Efficiency Study
## Efficiency
In economics, **productivity** and **efficiency** are related but distinct concepts:

Productivity refers to how much output (goods or services) is produced per unit of input (labor, capital, etc). It measures the rate of output relative to the resources used to generate that output. Higher productivity means more efficient use of resources to increase production.

Efficiency refers to how well the inputs are utilized to achieve a given output. An efficient process maximizes output for a given set of resource inputs. It produces as much output as possible from the inputs available.

The key differences:
- Productivity is a measure of output relative to input. Efficiency considers just the relationship between inputs and outputs.
- Increasing productivity means increasing output with the same inputs. Increasing efficiency means getting more output from the same inputs.
- Productivity can be improved by increasing output or decreasing inputs. Efficiency only focuses on maximizing output for a given amount of inputs.
- Productivity is a broader metric of performance. Efficiency is more narrowly focused on the technical relationship between inputs and outputs.
  
So in summary:
- Productivity measures outputs relative to inputs.
- Efficiency measures how well inputs are converted into outputs.
- Improving productivity requires increasing outputs and/or decreasing inputs.
- Improving efficiency requires getting more output from given inputs.

## Methodology
### Data Envelopment Analysis (DEA)
Data envelopment analysis (DEA) is a nonparametric method in operations research and economics for the estimation of production frontiers[^1].
My note on implementing DEA and Radial Directional Distance function in Python: 
- [DEA in Python](https://nbviewer.org/github/Seaaann/Seaaann.github.io/blob/main/notes/DEA.ipynb)
A package for efficiency study using Python. I did not check if my codes show the same results as theirs. Hope someone can check.
- [pyStoNED](https://pystoned.readthedocs.io/en/latest/index.html)
I think they should speak to each other, since the DEA is simple (in some ways). I guess it is the solvers or their version causing the differences, if there are.


[^1]: [Data envelopment analysis](https://en.wikipedia.org/wiki/Data_envelopment_analysis)



### Stochastic Frontier Modeling (or Analysis, SFM or SFA)
#### History:
  1. The first paper specifies the SFA. [ALS1977](https://Seaaann.github.io/notes/Reference/ALS1977.pdf). Aother paper, [BCC1977](https://Seaaann.github.io/notes/Reference/ALS1977.pdf) proposes an improved parameterization of the ratio of the variance of the two errors. This improves the estimation efficiency. However, two studies only bring out the inefficiency with given frontier, with no mentioning of how to separate the composited error term (of random noise and technology inefficiency). [Stevenson1980](https://Seaaann.github.io/notes/Reference/stevenson1980.pdf) propose truncated normal and gamma distributions for inefficiency.
  2. [Jondrow1982](https://Seaaann.github.io/notes/Reference/jondrow1982.pdf) sugggests a solution on estimating expected value of inefficiency term, conditioned on the compsited error *exp(E(-u|e))*.
  3. [Pitt1981](https://Seaaann.github.io/notes/Reference/pitt1981.pdf) extends the frontier modeling to panel data. It should be first paper that defines the inefficiency is a time-invariant term, like a random effect model. Differences are the inefficiency term is truncated normal distribution. In a case of fixed effect model, [SS1984](https://Seaaann.github.io/notes/Reference/schmidt1984.pdf) discuss the inefficiency term should be changing over time. It should be unit-specific.
  4. [BC1988](https://Seaaann.github.io/notes/Reference/battese1988.pdf) suggest to use *E(exp(-u)|e)* to estimate inefficiency term.
  5. [BC1992](https://Seaaann.github.io/notes/Reference/battese1992.pdf) propose time-variant inefficiency term. Several papers specify the term, see [kumbhakar1990](https://Seaaann.github.io/notes/Reference/kumbhakar1990.pdf), [CSS1990](https://Seaaann.github.io/notes/Reference/cornwell1990.pdf).
  6. [BC1995](https://Seaaann.github.io/notes/Reference/battese1995.pdf) assumes that inefficiency term is a function of firm-specific variables and time. The model accounts for some heterogeneity.
  7. [Greene2003](https://Seaaann.github.io/notes/Reference/greene2003.pdf) propose maximum simulated likelihood estimation since the log-likelihood function of inefficiency is complex. 
  8. [Greene2005](https://Seaaann.github.io/notes/Reference/greene2005.pdf) propose true fixed effect model to describe time-variant inefficiency and firm heterogeneity. [Greene2005](https://Seaaann.github.io/notes/Reference/greene2005r.pdf) propose true random effect model.
  9. [Wang2010](https://Seaaann.github.io/notes/Reference/wang2010.pdf) propose a new method to avoid *incidental parameters problem*. The study suggests to delete the individual effect.



A Review Paper on SFA. [Kumbhakar2017](https://Seaaann.github.io/notes/Reference/Kumbhakar_2017_SFA_Review.pdf)
