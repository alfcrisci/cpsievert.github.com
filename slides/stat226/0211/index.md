Stat 226 - Lecture 9
========================================================
date: 02/11/14
transition: rotate
incremental: true

Your Turn
========================================================
incremental:false

* Find the following probabilities using Table A:
* Given $X \sim N(150, 100)$, find:
  * $P(X < 137)$
  * $P(X > 137)$
  * $P(140 < X < 165)$
* Given $Y \sim N(-10, 3^2)$, find:
  * $P(Y > -9)$
  * $P(-9 < Y < -7)$
  
Percentiles
========================================================
incremental:false

* __Definition__: The $p^{th}$ percentile is a value, say $v$, where $p$ percent of observations are lower than $v$.

<div align="center">
<iframe src="http://glimmer.rstudio.com/cpsievert/cdf/" width="650" height="600"></iframe>
</div>

  
Finding Percentiles of Z
========================================================

* Remember that for the normal distribution, mean = median = mode!
* Thus, the median of the __standard__ normal is...<div style="display:inline-block" class="fragment"> 0! </div>
* Therefore the __50th percentile__ of the standard normal is ...<div style="display:inline-block" class="fragment"> 0! </div>
* If we denote $Z \sim N(0, 1)$, we just said that $P(Z < 0) = 1/2$.
* Suppose I want to find the $99^{th}$ percentile of $Z$...
* We have to find a value $z^*$ that yields $P(Z < z^*) = 0.99$


Your Turn
========================================================
incremental:false

1. Find the value of $z^*$ for each of the following scenarios:
  * $P(Z < z^*) = 0.025$ (__Note__: $z^*$ is called the 2.5th percentile)
  * $P(Z < z^*) = 0.975$ (__Note__: $z^*$ is called the 97.5th percentile)
  * $P(Z < z^*) = 0.25$ (__Note__: $z^*$ is called the 25th percentile)
2. Find the two values that bound the middle 90% of the standard normal distribution.

Finding percentiles for any X
========================================================

* As before, $X \sim N(\mu, \sigma)$ translates to $Z \sim N(0,1)$ via a __z-score__:

<div align="center" class="fragment">$$z = \frac{x-\mu}{\sigma}$$</div>

* Rearranging this equation a bit gives us:

<div align="center" class="fragment">$$z \times \sigma + \mu = x$$</div>

* Thus, if $z^*$ is the $p^{th}$ percentile of the __standard__ normal, then $\mu + \sigma \times z^*$ is the $p^{th}$ percentile of $X \sim N(\mu, \sigma)$!

Average Debt
========================================================

* __Example:__ Let $X$ be the debt of an ISU undergraduate upon graduation (in thousands of dollars). Suppose $X$ is known to have a mean of 20 and standard deviation of 5.
  * How much debt does it take to have __more__ debt than 95% of other undergraduates?
  * In other words, what value of $z^*$ gives us $P(Z < z^*) = 0.95$?
  * From Table A, $z^* =$ 1.64 or 1.65 (either one is fine).
  * Using our 'backwards z-score calculation': $x = \mu + \sigma \times z^* = 20 + 5 \times 1.65 =$ 28.25
  * So, if you have $28,500 in debt upon graduating, you have more debt than 95% of graduates!
  
Your Turn
========================================================
incremental:false

1. Suppose $X \sim N(12, 2^2)$. Find the value of $x^*$ for each of the following scenarios:
  * $P(X < x^*) = 0.33$ ($x^*$ is called the 33rd percentile)
  * $P(X < x^*) = 0.66$ ($x^*$ is called the 66th percentile)
  * $P(X < x^*) = 0.01$ ($x^*$ is called the 1st percentile)
2. Suppose monthly revenue in your business market is known to vary according to a normal distribution with mean of $500 thousand and variance of $200 thousand.
  * How much revenue do you need next month in order to sell more than 98% of the entire market?
  * What monthly revenue figure would imply that 40% of the market receieved a higher revenue?
