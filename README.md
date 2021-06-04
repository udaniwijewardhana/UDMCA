# UDMCA

## Univariate Changepoint Analysis

UDMCA is a Shiny web application that allows to visualize changepoints by using Bayesian changepoint techniques implemented in 'changepoint', 'breakpoint', 'cumSeg' and 'bcp'. To carry out these analyses users simply need to click the buttons that create the input files required, execute the software and process the output to generate tables of values and plots with the results. Changepoint methods can be used only for a single location annual data which estimates using raw data while replacing missing values by zero. Therefore, the input data has taken as a single location to estimate changepoints. Predictors can only use with bcp method.

The application consists of 2 pages with main window: 

1)	Main window allows the user to upload the input files (data file) and also gives the option to normalize or standardize the counts or predictors data. 

2)	Changepoint analysis page that user can choose a Bayesian changepoint method to carry out the changepoint analysis.

This page gives the option to fit Bayesian changepoints for annual raw data. Since still developed univariate changepoint methods, app will consider the annual data CSV as a single located dataset. Four Bayesian changepoint packages (changepoint, breakpoint, cumSeg and bcp) could be used to find the significant changes. This page also visualizes the relevant changepoint profile plots. For bcp package user has the option to use predictor variables to analyse. As the algorithms stated in the page, user can change the relevant parameters for each method and find the best scenario.

## Changepoint packages:

### changepoint package

The changepoint package implements various mainstream and specialised changepoint methods for finding single and multiple changepoints within data which includes many popular non-parametric and frequentist methods (Killick, Haynes and Eckley, 2016). 

### breakpoint package

The breakpoint package implements variants of the Cross-Entropy (CE) method to estimate both the number and the corresponding locations
of break-points in biological sequences of continuous and discrete measurements. The proposed method primarily built to detect multiple
break-points in genomic sequences. However, it can be easily extended and applied to other problems (Priyadarshana and Sofronov, 2016). 

### cumSeg package

The cumSeg package (Muggeo, 2010) estimates the of number and location of change points in mean-shift (piecewise constant) models which is useful to model genomic sequences of continuous measurements. The algorithm first estimates the highest number of change points using the efficient âsegmentedâ algorithm of Muggeo (2003) and then select some of them using a generalized BIC criterion by applying the larâs algorithm of Efron et al. (2004) (Muggeo, 2010). 

### bcp package

The bcp package provides an implementation of the Barry and Hartigan (1993) product partition model for the normal errors change point problem using Markov Chain Monte Carlo. It also extends the methodology to regression models on a connected graph (Wang and Emerson, 2015) and allows estimation of change point models with multivariate responses (Erdman and Emerson, 2007).

## Installation Instructions

### To install and explore the application in your R, you could type the following on your r console. 

```r
shiny::runGitHub( "PPMCA", "uwijewardhana") 
```
### You can also install the "UDMCA" package and run the app on your r console following the steps below.

- Download the https://github.com/uwijewardhana/UDMCA/ repository zip folder and extract.
- Open the extracted folder and open PPMCA.Rproj.
- Then run the below code in UDMCA.Rproj:
                        
```r
devtools::install_github("uwijewardhana/PPMCA")
library(PPMCA)
shiny::runApp(appDir = "./app.R")
```
[UDMCA_manual](https://github.com/uwijewardhana/UDMCA/files/UDMCA_manual.pdf)

```r
Udani A. Wijewardhana1, Madawa Jayawardana1, 2, 3, Denny Meyer1

1 Department of Statistics, Data Science and Epidemiology, Swinburne University of Technology, Hawthorn, Victoria, Australia
2 Peter MacCallum Cancer Centre, Melbourne 3000 Victoria, Australia
3 Sir Peter MacCallum Department of Oncology, The University of Melbourne, Parkville 3010 Victoria, Australia

* uwijewardhana@swin.edu.au
```
