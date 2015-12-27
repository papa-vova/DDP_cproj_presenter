Pitch for the Shiny Application
========================================================
author: Vladimir Stepanov
date: Dec 28, 2015
autosize: true

Why bother?
========================================================

To get myself familiar with simple yet powerful presentation techniques working straight from RStudio!

[My Shiny app](https://papa-vova.shinyapps.io/DDP_cproj) demonstrates the following:
- fluid page layout with the title pane, sidebar floating on the right and the main content occupying the major par tof the page;
- simple linear model (Galton's data on childrens and parents heights);
- dynamic controls for altering model's coefficients
- ...and the dynamic update of the Mean Squared Error

What's in the model?
========================================================


```r
library(UsingR)
data(galton)
g_lm <- lm(child ~ parent, data=galton)
plot(galton)
abline(g_lm, col=3)
```

![plot of chunk unnamed-chunk-1](DDP_cproj_presenter-figure/unnamed-chunk-1-1.png) 

What's in the app?
========================================================

- You can change slope and intercept and monitor how the resulting line differs from the ‘best fit’ linear model. 
- The Mean Squared Error is calculated on demand
- It may be seen that different models result in very similar MSE.

Conslusion
========================================================

- I gave up figuring out while Slidify won't work for me (some YAML mapping errors)
- But RStudio Presenter is not that bad as a tool for building quick demos
- [My Shiny application](https://papa-vova.shinyapps.io/DDP_cproj) is nothing more than a PoC, but it gives me some app building confidence
