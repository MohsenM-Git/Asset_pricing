# Optimal Portfolio Theory and Asset Pricing
<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/pic-1.png" width="400"/>


## Background
<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/ef.png" width="4500"/> 

This notebook is an introduction to the basics portfolio construction. I start by a brief theoretical review the `Modern Portfolio Theory (MPT)`. The modern portfolio theory (MPT) is a mathematical framework that maximizes the expected return of a portfolio for a given level of risk (or, alternatively minimize the risk for a given target return). This theory essentially formalizes the concept of `diversification` in investing by providing a coherent basis for comparing the contribution of each asset to the aggregate risk of a portfolio. Harry Markowitz (1952) first introduced this theory, for which he was later awarded a Nobel Prize in Economics. 

<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/pr.png" width="450"/> 


After To better understand this model, let's start from the empirical fact that including more assets in a portfolio reduces the average risk. For example, if you were to randomly choose one individual stock from the S&P 500, its average standard deviation would be approximately 50 percent. The key observation is that dding more stocks reduces this standard deviation to less than 20 percent.

Then, I show the implementation of the theory by two empirical applications. The 


Then, I review the `Capital Asset Pricing Model (CAPM)` as a basic asset pricing model, and two of its frequently used extensions 3- and 5-factor `Fama-French` models. I will end this notebook by estimating these models using real world date. 
The modern portfolio theory is a practical method for selecting investments in order to maximize their overall returns within an acceptable level of risk.


<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/dd.png" width="400"/> <img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/crr.png" width="400"/> 
<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/msr.png" width="400"/> <img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/bp.png" width="400"/>  

<img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/rets.png" width="400"/> <img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/tb-sp500.png" width="400"/> <img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/reg-1.png" width="400"/> 


<center><img src="https://github.com/MohsenM-Git/Asset_pricing/blob/main/Images/reg-2.png" width="500"/></center>

## Content
* Introduction to the basics portfolio construction and Modern Portfolio Theory (MPT)
* Two applications of MPT: Industry Indices and Stock Indices
* Empirical Asset Pricing: Capital Asset Pricing Model (CAPM), 3- and 5-factor Fama-French models

## Data
Two datasets used:
  1) monthly returns of the US Stock market obtained from [this](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html) webpage
  2) daily stock returns from CRSP via [WRDS](https://wrds-www.wharton.upenn.edu/) and 3-Month Treasury Bill from the [FRED](https://fred.stlouisfed.org/series/WTB3MS#0).
All data used are available in the "Data" folder of this repository.

 ## Code
 "Asset-Pricing.ipynb" + Auxiliary modules "risk-mod" and "Portfolio-mod".
