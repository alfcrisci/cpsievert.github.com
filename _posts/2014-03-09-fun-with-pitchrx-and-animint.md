---
layout: post
title: "Fun with pitchRx and animint"
author: Carson Sievert
categories: [PITCHfx, interactive graphics]
tags: [pitchRx, animint]
---
{% include JB/setup %}


If you are anything like me, you spend most of the day wrangling data with
[plyr](http://cran.r-project.org/web/packages/plyr/index.html) (or
[dplyr](http://cran.r-project.org/web/packages/dplyr/index.html)) and visualizing it with
[ggplot2](http://cran.r-project.org/web/packages/ggplot2/index.html). For this reason, I got really
excited when I heard about the [animint](https://github.com/tdhock/animint) package which allows
one to create linked, interactive (even animated) web graphics using ggplot2 code.

This short post demonstrates linked plots using data from the
[pitchRx](http://cran.r-project.org/web/packages/pitchRx/) package. If you click on the bars in the
bar chart below, the corresponding start versus end speed scatterplot should change to reflect the
current selection. I really want to spend more time with animint since it seems to fill a void
where other similar (and also great) packages like [rCharts](http://rcharts.io/) and
[ggvis](http://ggvis.rstudio.com/) currently fall short.


{% highlight r %}
library(pitchRx)
library(animint)
data(pitches, package = "pitchRx")
pitches$type <- interaction(pitches$pitch_type, pitches$pitcher_name)
counts <- ddply(pitches, c("pitch_type", "pitcher_name", "type"),
                summarise, count = length(px))
viz <- list(bars = ggplot() +
              geom_bar(aes(x = factor(pitch_type), y = count,
                           fill = pitcher_name, clickSelects = type),
                      position = "dodge", stat = "identity", data = counts),
            scatter = ggplot() +
              geom_point(aes(start_speed, end_speed, fill = pitcher_name, showSelected = type),
                         alpha = 0.65, data = pitches))
gg2animint(viz)
{% endhighlight %}


<iframe src="http://cpsievert.github.io/pitchRx/animint/" width="1200" height="500"> </iframe>
