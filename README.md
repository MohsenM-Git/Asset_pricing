# Optimal Portfolio Theory and Asset Pricing
<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/pic-1.png" width="600"/>


## Background
<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/msr.png" width="500"/>
I start by a brief theoretical review the `Modern Portfolio Theory (MPT)`, which is one of the pillars of portfolio construction. The modern portfolio theory (MPT) is a mathematical framework that maximizes the expected return of a portfolio for a given level of risk (or, alternatively minimize the risk for a given target return). This theory essentially formalizes the concept of `diversification` in investing by providing a coherent basis for comparing the contribution of each asset to the aggregate risk of a portfolio. Harry Markowitz (1952) first introduced this theory, for which he was later awarded a Nobel Prize in Economics. 

<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/pr.png" width="450"/> 


After introducing the framework, to better understand this model, as an example, I empirically analyze the historical monthly returns of various US industries from `1926-07` through `2023-06`. The dataset requires some basic `cleaning`, after which I compute and plot the `efficient frontier` as well as the `minimmum variance portfolio`. 
<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/dd.png" width="400"/> <img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/crr.png" width="400"/> 

 <img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/bp.png" width="400"/>  

The second application uses `daily stock returns` as well as `3-Month Treasury Bill` retruns. The time period for this exercise runs from the beginning of `1990` through the end of `2022`, which is currently the last available data. This exercise requires a bit more `cleaning`. This is specially due to some `missing` data in stock returns, and **frequency mismatch** between the stock data and T-Bill data.


<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/rets.png" width="400"/> <img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/tb-sp500.png" width="400"/>

I also conduct some preliminary tests which include the `Bartlett’s Test of sphericity` and the ` Kaiser-Meyer-Olkin (KMO)` test. The Bartlett’s test of sphericity compares an observed correlation matrix to the identity matrix. The `null hypothesis` of the test is that the variables are orthogonal, i.e. `not correlated`. The alternative hypothesis is that the variables are correlated enough for the correlation matrix to diverge significantly from the identity matrix. The test statistic has a Chi-Square distribution and its degree of freedom is equal to the number of variables in the matrix. On the other hand, the Kaiser-Meyer-Olkin (KMO) test is a measure of how suited the data is for `Factor Analysis`. The test measures sampling adequacy for each variable in the model and for the complete model. The statistic is a measure of the *proportion of variance among variables that might be common variance*. The lower the proportion, the more suited the data for `Factor Analysis`. KMO returns values between 0 and 1. As a rule of thumb, values between 0.8 and 1 indicate the sampling is adequate while values less than 0.6 are usually considered inadequate. 

 <img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/ows.png" width="500"/> 
Having conducted these basic tests, I construct the optimal portfolio of assets for a range of potential target returns. This analysis shows two important features of the data:
* For almost all potential targets, the number of effective assets is noticeably smaller than the total number of available assets.
* Best assets for different return ranges are different. For example, while `XEL` has the highest weight when targeting lower retuns, `MSFT` is the best option if we want to target high returns. 

This takes us to the last section of this notebook where I compare individual characteristics of each asset empirically. For that, I use the Capital Asset Pricing Model (CAPM) and two of its important extensions: 3- and 5-factor Fama-French models.

<center><img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/reg-1.png" width="500"/></center>
<center><img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/reg-2.png" width="500"/></center>
<center><img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/reg-3.png" width="500"/></center>



## Content
[1. Modern Portfolio Theory](#1) 

[2. Application (1): Industry Indices](#2) 

- [Data Exploration](#2.1) 
- [Efficient Frontier Analysis](#2.2)
    * [A Two-Asset Case](#2.2.1)
    * [Multi-Asset Case](#2.2.2)
- [Optimal Portfolios:](#2.3)
     * [Maximum Sharpe Ratio Portfolio(MSRP)](#2.3.1) 
     * [Minimum Variance Portfolio (MVP) ](#2.3.2)


[3. Application (2): Stock Indices](#3) 

- [Data Preprocessing](#3.1)
    * [Graphs](#3.1.1)
    * [Descrpitive and Financial Statistics](#3.1.2) 
    * [Factorability Tests](#3.1.3)
- [Efficient Frontier Analysis](#3.2)
- [Diversification in Practice ](#3.3)

[4. Empirical Asset Pricing Models](#4) 
- [Capital Asset Pricing Model](#4.1)
- [3-Factor Fama-French Model](#4.2)
- [5-Factor Fama-French Model](#4.3)


## Data
Two datasets used:
  1) monthly returns of the US Stock market obtained from [this](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html) webpage
  2) daily stock returns from CRSP via [WRDS](https://wrds-www.wharton.upenn.edu/) and 3-Month Treasury Bill from the [FRED](https://fred.stlouisfed.org/series/WTB3MS#0).
All data used are available in the "Data" folder of this repository.

 ## Code
 "Asset-Pricing.ipynb" + Auxiliary modules "risk-mod" and "Portfolio-mod".
