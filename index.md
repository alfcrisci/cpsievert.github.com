---
layout: page
title: Approximately Normal
---
{% include JB/setup %}

Approximately normal is the personal site of [Carson Sievert](http://cpsievert.github.io). 
The website is based on Github/Jekyll, and graphs are generated dynamically through the R 
package [**knitr**](http://yihui.name/knitr). The source code to these posts are available on [GitHub](http://github.com/cpsievert/cpsievert.github.com/tree/master/_source)

## Latest posts

<ul class="posts">
  {% for post in site.posts limit:10 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
  <li><a href="archive.html">Read More...</a></li>
</ul>

## Copyright

All the content in this website is licensed under [CC BY-NC-SA 3.0](http://creativecommons.org/licenses/by-nc-sa/3.0/). 
