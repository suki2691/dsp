[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```python
import scipy.Stats

lower_lim = 177.8
upper_lim = 185.42

mean = 178
sd = 7.7
dist = scipy.stats.norm(loc = mean, scale = sd)

#CDF of lower limit
lo = dist.cdf(lower_lim)

#CDF of upper limit
up = dist.cdf(upper_lim)

print("The percentage of men between the heights: %.3f" %((up-lo)*100))
```
