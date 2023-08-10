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

```python

```

[^1]: [Data envelopment analysis](https://en.wikipedia.org/wiki/Data_envelopment_analysis)


### Stochastic Frontier Modeling (or Analysis, SFM or SFA)
#### History:
The first paper specifies the SFA. [ALS1977](https://Seaaann.github.io/notes/Reference/ALS1977.pdf)
- It proposes a new stochastic frontier production function model where the error term has two components: a symmetric error to capture noise, and a one-sided error to represent inefficiency.
- The one-sided error is modeled as being half-normal or exponentially distributed to capture technical inefficiency.
Maximum likelihood estimation is used to estimate the model parameters along with the variances of the two error components.
- Monte Carlo simulations show the model performs reasonably well in recovering true parameters, though some bias exists.
- Empirical examples on US manufacturing and agriculture data find the symmetric error dominates, implying high efficiency relative to the stochastic frontier.
- The model allows direct estimation of the two error variances, giving information on their relative magnitude.
- It avoids some issues with previous deterministic frontier models, and provides a stochastic frontier with statistical properties.
- Key limitations are computational complexity and some remaining small sample bias.
