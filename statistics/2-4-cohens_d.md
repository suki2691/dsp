[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)  

```python
import numpy as np
import nsfg

preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]

firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

def CohenEffectSize(group1, group2):
    """Computes Cohen's effect size for two groups.

    group1: Series or DataFrame
    group2: Series or DataFrame

    returns: float if the arguments are Series;
             Series if the arguments are DataFrames
    """
    diff = group1.mean() - group2.mean()

    var1 = group1.var()
    var2 = group2.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d

cd_wgt = CohenEffectSize(firsts.totalwgt_lb,others.totalwgt_lb)
cd_len = CohenEffectSize(firsts.prglngth,others.prglngth)

print("Cohen's Effect Size for difference in birth weights: %.3f" %cd_wgt)
print("Cohen's Effect Size for difference in pregnancy lengths: %.3f" %cd_len)
```

The Cohen's Effect Size of the two groups is:  
* Live first birth weights vs Live subsequent birth weights = -0.088673
* Live first pregnancy lengths vs Live subsequent pregnancy lengths = 0.02888  

This means that babies that are not first-borns are born heavier than first-borns. Also, first-borns take relatively longer to be born than those that are born after.
