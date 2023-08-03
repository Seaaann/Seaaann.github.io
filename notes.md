---
layout: page
permalink: /notes/index.html
title: Notes
---

# Economic Efficiency Study
## Efficiency

## Methodology
### Data Envelopment Analysis (DEA)
Data envelopment analysis (DEA) is a nonparametric method in operations research and economics for the estimation of production frontiers[^1].

```python
for i in range(len(data)):
    c = np.zeros((len(data)+1))
    c[-1] = 1
    output = np.append(data.q.values,[0])
    input = data[['x1', 'x2']].values

    A_ub = np.array([-output, np.append(input[:,0],-input[i,0]),  np.append(input[:,1],-input[i,1])])
    print(A_ub)
    B_ub = np.zeros(len(A_ub))
    B_ub[0] = -output[i]
    print(B_ub)

    lambda1=(0, None)
    lambda2=(0, None)
    lambda3=(0, None)
    lambda4=(0, None)
    lambda5=(0, None)
    theta=(None, None)

    res = optimize.linprog(c, A_ub, B_ub, bounds=(lambda1,lambda2,lambda3,lambda4,lambda5,theta))
    
    print("CRS DEA for DUM {}".format(i+1))
    print("Efficiency score for DMU {}: {}".format(i+1,np.round(res.fun,3)))
    print("lambads: {}".format(np.round(res.x[:-1],3)))
    print("----------------------------------")
```

[^1]: [Data envelopment analysis](https://en.wikipedia.org/wiki/Data_envelopment_analysis)


