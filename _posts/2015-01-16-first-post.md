---
title: "first post"
description: ''
layout: post
output:
  html_document:
    highlight: pygments
  pdf_document: default
  word_document: default
tags: R
category: code
---
{% include JB/setup %}




{% highlight r %}
library("knitr")
library("ggplot2")

df <- data.frame(a = rnorm(500),
                 b = rt(500, df = 5))

head(df)
{% endhighlight %}



{% highlight text %}
##             a           b
## 1 -0.81756609 -0.73968733
## 2  1.15506724  0.75849791
## 3  0.88511044 -0.02536199
## 4 -1.87698581 -0.10098786
## 5  0.87878087 -0.55482675
## 6 -0.03892207  1.13197887
{% endhighlight %}



{% highlight r %}
p <- ggplot(df)+
     geom_point(aes(x = a, y = b))
plot(p)
{% endhighlight %}

![plot of chunk setup](/figure/Rmd/2015-01-16-first-post/setup-1.png) 

### Test knitr

