# Distribution-Checker
Python Distribution Checker for datas using Scipy package

## Installation
```bash
pip install Distribution_Checker
```

## Usage
```python
from Distribution_Checker import Dist_Checker
import pandas as pd

# Load sample dataset
data = pd.read_csv('weight-height.csv')

# verbose=1 prints the log while fitting and verbose=0 doesn't
p = Dist_Checker(verbose=1)
p = p.fit(data)

# After fitting, you can get distribution sorted by Sum of Squered Error that fit your data, so the first distribution is the distribution that is closer to your data
p.get_distributions()

# You can also plot distributions and your data to see this visualy. top=10 means that you want to plot top 10 distributions that match your data
p.plot(top=10)
```
Output plot from [weight-height.csv](https://github.com/amirhr098/Distribution-Checker/files/9228716/weight-height.csv) DataFrame
![image](https://user-images.githubusercontent.com/95343201/182023160-48c8b978-6f71-433e-8f57-40965ed5ce35.png)

## Distributions list
```
            alpha, anglit, arcsine, argus, beta, betaprime, bradford,
            burr, burr12, cauchy, chi, chi2, cosine, crystalball,
            dgamma, dweibull, erlang, expon, exponnorm, exponweib,
            exponpow, f, fatiguelife, fisk, foldcauchy, foldnorm,
            genlogistic, gennorm, genpareto,weibull_max, wrapcauchy,
            genexpon, genextreme, gausshyper, gamma, gengamma, genhalflogistic,
            geninvgauss, gilbrat, gompertz, gumbel_r, gumbel_l, halfcauchy,
            halflogistic, halfnorm, halfgennorm, hypsecant, invgamma, invgauss,
            invweibull, johnsonsb, johnsonsu, kappa4, kappa3, ksone, kstwo,
            kstwobign, laplace, levy, levy_l, logistic, loggamma,
            loglaplace, lognorm, loguniform, lomax, maxwell, mielke, moyal,
            nakagami, norm, norminvgauss, pareto, pearson3,
            powerlaw, powerlognorm, powernorm, rdist, rayleigh, rice, recipinvgauss,
            semicircular, skewnorm, t, trapz, triang, truncexpon, truncnorm,
            tukeylambda, uniform, vonmises, vonmises_line, wald, weibull_min
```
---
If any problem was founded, feel free to inform me :)