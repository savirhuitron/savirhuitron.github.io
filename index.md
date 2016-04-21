---
title       : CAPM
subtitle    : Capital Asset Pricing Model
author      : Savir Huitron
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax, highcharts]            # {mathjax, quiz, bootstrap}
ext_widgets : {rCharts: [libraries/highcharts]}
mode        : selfcontained
knit        : slidify::knit2slides
github: 
    user: savirhuitron
    repo: capm1
---

## Capital Asset Pricing Model

The Capital Asset Pricing Model is a model that describes the relationship between **risk** and **expected return** and that is used in the pricing of risky securities. [investopedia](http://www.investopedia.com/terms/c/capm.asp)

The model takes into account the asset's sensitivity to non-diversifiable risk (also known as systematic risk or market risk), often represented by the quantity **beta** (**$\beta$**)  in the financial industry, as well as the expected return of the market and the expected return of a theoretical risk-free asset. 


## The Model

The formula for the model was introduced by **Jack Traynor**, **William F. Sharpe**, **John Lintner** and **Jan Mossin** independently, building on the earlier work of **Harry Markowitz** on diversification and modern portfolio theory. Sharpe, Markowitz and Merton Miller jointly received the 1990 Nobel Memorial Prize in Economics for this contribution to the field of financial economics. [wikipedia](https://en.wikipedia.org/wiki/Capital_asset_pricing_model)


--- .class #id 

## The Model

The model is the next: 

$$E(R_i) = R_f + \beta_i  (E(R_m)- R_f)$$

Where: 

$E(R_i) =$ *Is the expected return on the capital asset*

$R_f =$ *Is the risk-free rate of interest*

$\beta_i =$ *Is the beta of the capital asset, which is in our linear model* $\hat{\beta_i} = Cor(Y,X) \frac{Sd(Y)}{Sd(X)}$

$R_m =$ *Is the expected return of the market*


--- 

## The Interpretation

* CAPM helps investors calculate risk and what type of return they should expect on their investment. 

* In our model, the $\beta_i$ it's a measure of the volatility, or systematic risk, of a security or a portfolio in comparision to the market as a whole, in this case we are using the [IPC](http://www.bmv.com.mx/en/indices/main/) as the whole market,  and its [components](http://www.bmv.com.mx/en/markets/special-information). 

* Beta is calculated using regression analysis, and you can think of beta as the tendency of a security's returns to respond to swings in the market. a beta of 1 indicates that the security's price will move with the market. A beta of less than 1 means that the security will be less volatile than the market. A beta greater than 1 indicates that the security's price will be less volatile than the market. For example, if a stock's __beta__ is 1.2, it's theoretically 20% more volatile than the market. [investopedia](http://www.investopedia.com/terms/b/beta.asp?utm_term=beta&utm_content=sem-unp&utm_medium=organic&utm_source=&utm_campaign=&ad=&an=&am=&o=40186&askid=&l=dir&qsrc=999&qo=investopediaSiteSearch)


---

## CAPM 

This shows in the "x axis" the nivels of the Beta, the size of the bubble it's the expected return on the capital asset.


<div id = 'myChart' class = 'rChart highcharts'></div>
<script type='text/javascript'>
    (function($){
        $(function () {
            var chart = new Highcharts.Chart({
 "dom": "myChart",
"width":            800,
"height":            400,
"credits": {
 "href": null,
"text": null 
},
"exporting": {
 "enabled": true 
},
"title": {
 "text": "BETAS of the Components of IPC Index" 
},
"yAxis": [
 {
 "title": {
 "text": "EMISORA" 
} 
} 
],
"series": [
 {
 "data": [
 [
              1,
35,
         4.825 
],
[
       1.025932,
27,
      4.949214 
],
[
       1.105967,
11,
       5.33258 
],
[
        1.11668,
2,
      5.383899 
],
[
       1.153395,
16,
      5.559763 
],
[
       1.161378,
14,
      5.598001 
],
[
       1.209218,
4,
      5.827153 
],
[
       2.025752,
7,
      9.738351 
],
[
       2.312633,
18,
      11.11251 
] 
],
"name": "HIGH",
"type": "bubble",
"marker": {
 "radius":              3 
} 
},
{
 "data": [
 [
       0.730774,
17,
      3.535408 
],
[
       0.732694,
21,
      3.544602 
],
[
       0.736135,
8,
      3.561086 
],
[
       0.737972,
25,
      3.569887 
],
[
       0.743939,
28,
      3.598466 
],
[
       0.769128,
24,
      3.719125 
],
[
       0.780758,
22,
      3.774832 
],
[
       0.781527,
34,
      3.778514 
],
[
       0.854243,
9,
      4.126822 
] 
],
"name": "LOW",
"type": "bubble",
"marker": {
 "radius":              3 
} 
},
{
 "data": [
 [
       0.875687,
12,
      4.229542 
],
[
       0.944363,
6,
      4.558501 
],
[
       0.945461,
3,
      4.563758 
],
[
       0.966126,
13,
      4.662744 
],
[
       0.969663,
26,
      4.679683 
],
[
       0.978669,
29,
      4.722826 
],
[
       0.990046,
31,
       4.77732 
],
[
       0.998722,
33,
      4.818876 
] 
],
"name": "MEDIA",
"type": "bubble",
"marker": {
 "radius":              3 
} 
},
{
 "data": [
 [
       0.309372,
15,
      1.516894 
],
[
       0.394211,
20,
      1.923273 
],
[
       0.505084,
19,
      2.454352 
],
[
       0.508406,
32,
      2.470263 
],
[
       0.545573,
23,
      2.648293 
],
[
       0.563582,
1,
      2.734559 
],
[
       0.674892,
30,
      3.267732 
],
[
       0.694692,
5,
      3.362574 
],
[
       0.704172,
10,
      3.407985 
] 
],
"name": "MINIMUM",
"type": "bubble",
"marker": {
 "radius":              3 
} 
} 
],
"xAxis": [
 {
 "title": {
 "text": "BETA" 
} 
} 
],
"subtitle": {
 "text": null 
},
"chart": {
 "zoomType": "xy",
"renderTo": "myChart" 
},
"id": "myChart" 
});
        });
    })(jQuery);
</script>

