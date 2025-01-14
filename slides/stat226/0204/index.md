Stat 226 - Lecture 7
========================================================
date: 02/04/14
transition: rotate
incremental: true


Probability...It's as easy as flipping a coin!
========================================================
incremental:false

<div align="center">
<img class="decoded" src="https://i.chzbgr.com/maxW500/8034803968/hEFF2B1E7/" width=800 height=600>
</div>

Probability made easy
========================================================

* What's the __probability__ that a coin lands heads-up?
* Assuming it's a _fair_ coin, the probability is 0.5.
* What's the __probability__ that a coin lands tails-up?
* We just fully described a __probability distribution function (pdf)__!

Probability continued
========================================================
title:false
left:45%

<div align="center">
<img src="map.png" width=800 height=400>
</div>
* In essence, a __pdf__ assigns __probability__ to value(s) of a __random variable__.
***

* Technically, value(s) of a __random variable__ define __event(s)__ and each __event__ has a probability. 
* Suppose I flip a coin twice. What are the different possible __events__?
* Let $X$ be the # of heads after two flips. What event(s) correspond to $X=1$?
* 2 out of 4 (equally likely) events lead to $X=1$, so $P(X=1) = 0.5$.

A couple facts
========================================================
title:false

* What are all the different possible values $X$?
* What is the probability $X$ takes on each value?

<li class="fragment">
probability distribution function for $X$:
<div align="center">
<!-- html table generated in R 3.0.2 by xtable 1.7-1 package -->
<!-- Tue Feb  4 12:16:02 2014 -->
<TABLE border=1>
  <TR> <TD> P(X=0) </TD> <TD> P(X=1) </TD> <TD> P(X=2) </TD> </TR>
  <TR> <TD> 0.25 </TD> <TD> .5 </TD> <TD> 0.25 </TD> </TR>
   </TABLE>

</div>
</li>

* Since $X$ takes on a small # of values, it is a __discrete__ random variable (think categorical).
* From now on, we study __continuous__ random variables (can you guess the difference?)
* __Continuous__ random variables can take on an infinite number of values (think quantitative)!
* __Events__ are defined by __intervals:__ $X \leq 0$, not $X=0$

Effort
========================================================
title:false
type: alert

* __IMPORTANT__: probabilities are __always__ between 0 and 1! pdfs __always__ add to 1!

<li class="fragment">
<div align="center">
<img src="110" width=600 height=550>
</div>
</li>

Back to normal distributions
========================================================

* The __Normal distribution__ is a special type of __pdf__. 
* A __normal__ random variable is a __continous__ random variable whose __pdf__ is __symmetric__ and __bell-shaped__.
* If $X$ is a normally distributed random variable, it has a mean $\mu$ and variance $\sigma^2$.
* More succinctly, $X \sim N(\mu, \sigma^2)$

<li class="fragment">
<div align="center">
<img src="normal.png" width=400 height=290>
</div>
</li>

The Empirical Rule
========================================================

<div align="center">
<img src="empirical.jpg" width=400 height=400>
</div>
* Given $X \sim N(\mu, \sigma^2)$, the empirical rule says:

***


* The probability that $X$ is within __one__ standard devation of the mean is 0.68:
* That is, $P(\mu - \sigma < X < \mu + \sigma ) = 0.68$.
* The probability that $X$ is within __two__ standard devations of the mean is 0.95.
* That is, $P(\mu - 2\sigma < X < \mu + 2\sigma ) = 0.95$.
* The probability that $X$ is within __three__ standard devations of the mean is 0.997.
* That is, $P(\mu - 3\sigma < X < \mu + 3\sigma ) = 0.997$.

Your Turn 
========================================================
incremental:false

(1) Let $X \sim N(100, 50^2)$. Find the following probabilities:
  * $P(X < 100)$
  * $P(X < 150)$
  * $P(100 < X < 150)$
  * $P(X < 0)$

***

(2) Suppose $Z \sim N(0, 1)$. Find the following probabilities:
  * $P(Z < 0)$
  * $P(Z < 1)$
  * $P(0 < Z < 1)$
  * $P(Z < -2)$

Standard Normal Distribution
========================================================

* The __standard normal__ distribution is a normal distribution with mean 0 and variance 1.
* We typically use $Z$ to represent a standard normal distribution.
* It turns out that we can transform any $X \sim N(\mu, \sigma)$ into $Z \sim N(0,1)$ using a __z-score__:
<li class="fragment">
$$
z = \frac{x-\mu}{\sigma}
$$
</li>
* Example(s) on board.
