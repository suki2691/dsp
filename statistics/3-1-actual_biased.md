[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

```python
import numpy as np
import nsfg
import first
import thinkstats2
import thinkplot

resp = nsfg.ReadFemResp()
pmf = thinkstats2.Pmf(resp.numkdhh, label = 'numkdhh')
thinkplot.Pmf(pmf)

biased_pmf = BiasPmf(pmf, label = 'biased')

thinkplot.PrePlot(2)
thinkplot.pmfs([pmf,biased])
thinkplot.Config(xlabel='Number of Children', ylabel='PMF')

#Comparing the means of pmf and biased pmf
print("Actual Mean: %.3f" %pmf.Mean())
print("Observed Mean: %.3f" %biased.Mean())
```
Outputs:
* Mean: 1.024
* Biased Mean: 2.404
