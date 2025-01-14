Stat 226 - Lecture 8
========================================================
date: 02/06/14
transition: rotate
incremental: true

Back to Empirical Rule
========================================================

<div align="center">
<img src="empirical.gif" width="650" height="400">
</div>

* OK, but what if I want to find something like $P(Z < -0.5)$?
* This is what Table A is for!

Visualizing Table A
========================================================
incremental:false

<div align="center">
<iframe src="http://glimmer.rstudio.com/cpsievert/cdf/" width="650" height="600"></iframe>
</div>


Some useful facts
========================================================

* Using Table A requires reducing probability statements down to $P(Z < a)$, for some number $a$.
* Given $X \sim N(\mu, \sigma^2)$:
  * $P(X > a) = 1 - P(X < a)$
  * $P(a < X < b) = P(X < b) - P(X < a)$
* Given $Z \sim N(0, 1)$ for any __positive__ number $a$:
  * $P(Z > a) = P(Z < -a)$
  
Your turn
========================================================
incremental:false

* Find the following probabilities using Table A:
  * $P(Z < -1.64)$
  * $P(Z > -0.56)$
  * $P(-1 < Z < 2.27)$
  * $P(Z > 4)$
  
Finding probabilities for any X
========================================================

* Last time we learned how $X \sim N(\mu, \sigma)$ translates to $Z \sim N(0,1)$ via a __z-score__:

<div align="center" class="fragment">$$z = \frac{x-\mu}{\sigma}$$</div>
* Suppose $X \sim N(10, 25)$. 

* $P(X > 15) =$ <div style="display:inline-block" class="fragment"> $P(X-10 > 5) =$ </div> <div style="display:inline-block" class="fragment"> $P(\frac{X-10}{5} > \frac{15-10}{5}) =$ </div> <div style="display:inline-block" class="fragment"> $P(Z > 1)$
* <div style="display:inline-block" class="fragment"> $P(Z > 1) =$ <div style="display:inline-block" class="fragment"> $P(Z < -1) =$ </div> <div style="display:inline-block" class="fragment"> .1587 </div>

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
