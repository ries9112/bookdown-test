--- 
title: "A Minimal Book Example"
author: "Yihui Xie"
date: "2020-11-13"
site: bookdown::bookdown_site
output: bookdown::gitbook
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
github-repo: rstudio/bookdown-demo
description: "This is a minimal example of using the bookdown package to write a book. The output format for this example is bookdown::gitbook."
---

# Prerequisites

This is a _sample_ book written in **Markdown**. You can use anything that Pandoc's Markdown supports, e.g., a math equation $a^2 + b^2 = c^2$.

The **bookdown** package can be installed from CRAN or Github:


```r
install.packages("bookdown")
# or the development version
# devtools::install_github("rstudio/bookdown")
```

Remember each Rmd file contains one and only one chapter, and a chapter is defined by the first-level heading `#`.

To compile this example to PDF, you need XeLaTeX. You are recommended to install TinyTeX (which includes XeLaTeX): <https://yihui.name/tinytex/>.



<!--chapter:end:index.Rmd-->

# Introduction {#intro}

You can label chapter and section titles using `{#label}` after them, e.g., we can reference Chapter \@ref(intro). If you do not manually label them, there will be automatic labels anyway, e.g., Chapter \@ref(methods).

Figures and tables with captions will be placed in `figure` and `table` environments, respectively.


```r
par(mar = c(4, 4, .1, .1))
plot(pressure, type = 'b', pch = 19)
```

<div class="figure" style="text-align: center">
<img src="_main_files/figure-html/nice-fig-1.png" alt="Here is a nice figure!" width="80%" />
<p class="caption">(\#fig:nice-fig)Here is a nice figure!</p>
</div>

Reference a figure by its code chunk label with the `fig:` prefix, e.g., see Figure \@ref(fig:nice-fig). Similarly, you can reference tables generated from `knitr::kable()`, e.g., see Table \@ref(tab:nice-tab).


```r
knitr::kable(
  head(iris, 20), caption = 'Here is a nice table!',
  booktabs = TRUE
)
```



Table: (\#tab:nice-tab)Here is a nice table!

| Sepal.Length| Sepal.Width| Petal.Length| Petal.Width|Species |
|------------:|-----------:|------------:|-----------:|:-------|
|          5.1|         3.5|          1.4|         0.2|setosa  |
|          4.9|         3.0|          1.4|         0.2|setosa  |
|          4.7|         3.2|          1.3|         0.2|setosa  |
|          4.6|         3.1|          1.5|         0.2|setosa  |
|          5.0|         3.6|          1.4|         0.2|setosa  |
|          5.4|         3.9|          1.7|         0.4|setosa  |
|          4.6|         3.4|          1.4|         0.3|setosa  |
|          5.0|         3.4|          1.5|         0.2|setosa  |
|          4.4|         2.9|          1.4|         0.2|setosa  |
|          4.9|         3.1|          1.5|         0.1|setosa  |
|          5.4|         3.7|          1.5|         0.2|setosa  |
|          4.8|         3.4|          1.6|         0.2|setosa  |
|          4.8|         3.0|          1.4|         0.1|setosa  |
|          4.3|         3.0|          1.1|         0.1|setosa  |
|          5.8|         4.0|          1.2|         0.2|setosa  |
|          5.7|         4.4|          1.5|         0.4|setosa  |
|          5.4|         3.9|          1.3|         0.4|setosa  |
|          5.1|         3.5|          1.4|         0.3|setosa  |
|          5.7|         3.8|          1.7|         0.3|setosa  |
|          5.1|         3.8|          1.5|         0.3|setosa  |

You can write citations, too. For example, we are using the **bookdown** package [@R-bookdown] in this sample book, which was built on top of R Markdown and **knitr** [@xie2015].


## Here adding new test

```r
library(pins)
board_register(name = "pins_board", url = "https://raw.githubusercontent.com/predictcrypto/pins/master/", board = "datatxt")
cryptodata <- pin_get(name = "hitBTC_orderbook")
```

Show data

```r
cryptodata
```

```
## [90m# A tibble: 243,109 x 27[39m
##    pair  symbol quote_currency ask_1_price ask_1_quantity ask_2_price
##    [3m[90m<chr>[39m[23m [3m[90m<chr>[39m[23m  [3m[90m<chr>[39m[23m                [3m[90m<dbl>[39m[23m          [3m[90m<dbl>[39m[23m       [3m[90m<dbl>[39m[23m
## [90m 1[39m BTCU… BTC    USD             [4m1[24m[4m6[24m290.             0.058[4m9[24m  [4m1[24m[4m6[24m290.    
## [90m 2[39m ETHU… ETH    USD               462.             0.4       463.    
## [90m 3[39m EOSU… EOS    USD                 2.46         600           2.46  
## [90m 4[39m LTCU… LTC    USD                60.7            3.75       60.7   
## [90m 5[39m BSVU… BSV    USD               158.             0.6       158.    
## [90m 6[39m ADAU… ADA    USD                 0.105        775           0.105 
## [90m 7[39m ZECU… ZEC    USD                63.0            2.59       63.1   
## [90m 8[39m TRXU… TRX    USD                 0.024[4m9[24m     [4m6[24m[4m5[24m497           0.024[4m9[24m
## [90m 9[39m HTUSD HT     USD                 3.64         105.          3.65  
## [90m10[39m XMRU… XMR    USD               112.             0.023     112.    
## [90m# … with 243,099 more rows, and 21 more variables: ask_2_quantity [3m[90m<dbl>[90m[23m,[39m
## [90m#   ask_3_price [3m[90m<dbl>[90m[23m, ask_3_quantity [3m[90m<dbl>[90m[23m, ask_4_price [3m[90m<dbl>[90m[23m,[39m
## [90m#   ask_4_quantity [3m[90m<dbl>[90m[23m, ask_5_price [3m[90m<dbl>[90m[23m, ask_5_quantity [3m[90m<dbl>[90m[23m,[39m
## [90m#   bid_1_price [3m[90m<dbl>[90m[23m, bid_1_quantity [3m[90m<dbl>[90m[23m, bid_2_price [3m[90m<dbl>[90m[23m,[39m
## [90m#   bid_2_quantity [3m[90m<dbl>[90m[23m, bid_3_price [3m[90m<dbl>[90m[23m, bid_3_quantity [3m[90m<dbl>[90m[23m,[39m
## [90m#   bid_4_price [3m[90m<dbl>[90m[23m, bid_4_quantity [3m[90m<dbl>[90m[23m, bid_5_price [3m[90m<dbl>[90m[23m,[39m
## [90m#   bid_5_quantity [3m[90m<dbl>[90m[23m, date_time_utc [3m[90m<dttm>[90m[23m, date [3m[90m<date>[90m[23m, pkDummy [3m[90m<chr>[90m[23m,[39m
## [90m#   pkey [3m[90m<chr>[90m[23m[39m
```


Show nested data

```r
library(tidyverse)
```

```
## ── [1mAttaching packages[22m ─────────────────────────────────────── tidyverse 1.3.0 ──
```

```
## [32m✔[39m [34mggplot2[39m 3.3.2     [32m✔[39m [34mpurrr  [39m 0.3.4
## [32m✔[39m [34mtibble [39m 3.0.4     [32m✔[39m [34mdplyr  [39m 1.0.2
## [32m✔[39m [34mtidyr  [39m 1.1.2     [32m✔[39m [34mstringr[39m 1.4.0
## [32m✔[39m [34mreadr  [39m 1.4.0     [32m✔[39m [34mforcats[39m 0.5.0
```

```
## ── [1mConflicts[22m ────────────────────────────────────────── tidyverse_conflicts() ──
## [31m✖[39m [34mdplyr[39m::[32mfilter()[39m masks [34mstats[39m::filter()
## [31m✖[39m [34mdplyr[39m::[32mlag()[39m    masks [34mstats[39m::lag()
```

```r
cryptodata <- group_by(cryptodata, symbol)
nest(cryptodata)
```

```
## [90m# A tibble: 218 x 2[39m
## [90m# Groups:   symbol [218][39m
##    symbol data                 
##    [3m[90m<chr>[39m[23m  [3m[90m<list>[39m[23m               
## [90m 1[39m BTC    [90m<tibble [2,280 × 26]>[39m
## [90m 2[39m ETH    [90m<tibble [1,404 × 26]>[39m
## [90m 3[39m EOS    [90m<tibble [2,233 × 26]>[39m
## [90m 4[39m LTC    [90m<tibble [2,280 × 26]>[39m
## [90m 5[39m BSV    [90m<tibble [1,523 × 26]>[39m
## [90m 6[39m ADA    [90m<tibble [1,166 × 26]>[39m
## [90m 7[39m ZEC    [90m<tibble [1,121 × 26]>[39m
## [90m 8[39m TRX    [90m<tibble [1,501 × 26]>[39m
## [90m 9[39m HT     [90m<tibble [2,215 × 26]>[39m
## [90m10[39m XMR    [90m<tibble [2,274 × 26]>[39m
## [90m# … with 208 more rows[39m
```

What does DT look like


```r
library(DT)
cryptodata
```

```
## [90m# A tibble: 243,109 x 27[39m
## [90m# Groups:   symbol [218][39m
##    pair  symbol quote_currency ask_1_price ask_1_quantity ask_2_price
##    [3m[90m<chr>[39m[23m [3m[90m<chr>[39m[23m  [3m[90m<chr>[39m[23m                [3m[90m<dbl>[39m[23m          [3m[90m<dbl>[39m[23m       [3m[90m<dbl>[39m[23m
## [90m 1[39m BTCU… BTC    USD             [4m1[24m[4m6[24m290.             0.058[4m9[24m  [4m1[24m[4m6[24m290.    
## [90m 2[39m ETHU… ETH    USD               462.             0.4       463.    
## [90m 3[39m EOSU… EOS    USD                 2.46         600           2.46  
## [90m 4[39m LTCU… LTC    USD                60.7            3.75       60.7   
## [90m 5[39m BSVU… BSV    USD               158.             0.6       158.    
## [90m 6[39m ADAU… ADA    USD                 0.105        775           0.105 
## [90m 7[39m ZECU… ZEC    USD                63.0            2.59       63.1   
## [90m 8[39m TRXU… TRX    USD                 0.024[4m9[24m     [4m6[24m[4m5[24m497           0.024[4m9[24m
## [90m 9[39m HTUSD HT     USD                 3.64         105.          3.65  
## [90m10[39m XMRU… XMR    USD               112.             0.023     112.    
## [90m# … with 243,099 more rows, and 21 more variables: ask_2_quantity [3m[90m<dbl>[90m[23m,[39m
## [90m#   ask_3_price [3m[90m<dbl>[90m[23m, ask_3_quantity [3m[90m<dbl>[90m[23m, ask_4_price [3m[90m<dbl>[90m[23m,[39m
## [90m#   ask_4_quantity [3m[90m<dbl>[90m[23m, ask_5_price [3m[90m<dbl>[90m[23m, ask_5_quantity [3m[90m<dbl>[90m[23m,[39m
## [90m#   bid_1_price [3m[90m<dbl>[90m[23m, bid_1_quantity [3m[90m<dbl>[90m[23m, bid_2_price [3m[90m<dbl>[90m[23m,[39m
## [90m#   bid_2_quantity [3m[90m<dbl>[90m[23m, bid_3_price [3m[90m<dbl>[90m[23m, bid_3_quantity [3m[90m<dbl>[90m[23m,[39m
## [90m#   bid_4_price [3m[90m<dbl>[90m[23m, bid_4_quantity [3m[90m<dbl>[90m[23m, bid_5_price [3m[90m<dbl>[90m[23m,[39m
## [90m#   bid_5_quantity [3m[90m<dbl>[90m[23m, date_time_utc [3m[90m<dttm>[90m[23m, date [3m[90m<date>[90m[23m, pkDummy [3m[90m<chr>[90m[23m,[39m
## [90m#   pkey [3m[90m<chr>[90m[23m[39m
```

And nested

```r
nest(cryptodata)
```

```
## [90m# A tibble: 218 x 2[39m
## [90m# Groups:   symbol [218][39m
##    symbol data                 
##    [3m[90m<chr>[39m[23m  [3m[90m<list>[39m[23m               
## [90m 1[39m BTC    [90m<tibble [2,280 × 26]>[39m
## [90m 2[39m ETH    [90m<tibble [1,404 × 26]>[39m
## [90m 3[39m EOS    [90m<tibble [2,233 × 26]>[39m
## [90m 4[39m LTC    [90m<tibble [2,280 × 26]>[39m
## [90m 5[39m BSV    [90m<tibble [1,523 × 26]>[39m
## [90m 6[39m ADA    [90m<tibble [1,166 × 26]>[39m
## [90m 7[39m ZEC    [90m<tibble [1,121 × 26]>[39m
## [90m 8[39m TRX    [90m<tibble [1,501 × 26]>[39m
## [90m 9[39m HT     [90m<tibble [2,215 × 26]>[39m
## [90m10[39m XMR    [90m<tibble [2,274 × 26]>[39m
## [90m# … with 208 more rows[39m
```




<!--chapter:end:01-intro.Rmd-->

# Literature

Here is a review of existing methods.

<!--chapter:end:02-literature.Rmd-->

# Methods

We describe our methods in this chapter.

<!--chapter:end:03-method.Rmd-->

# Applications

Some _significant_ applications are demonstrated in this chapter.

## Example one

## Example two

<!--chapter:end:04-application.Rmd-->

# Final Words

We have finished a nice book.

<!--chapter:end:05-summary.Rmd-->


# References {-}


<!--chapter:end:06-references.Rmd-->

