[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```
import numpy as np
import thinkstats2
import thinkplot

randnum = np.random.random(1000)

pmf = thinkstats2.Pmf(randnum)
thinkplot.Pmf(pmf,linewidth=0.1)
thinkplot(xlabel = 'Random Variable',ylabel = 'PMF')

cdf = thinkstats2.Cdf(randnum)
thinkplot.Cdf(cdf)
thinkplot(xlabel = 'Random Variable',ylabel = 'CDF')
```
According to the CDF plot, the distribution is uniform 
