# Package "regressr"


## Overview/Synopsis
 Create “regressr”, an R library dedicated to helping user build regression models, providing text output to ease interpretation of the model’s results, and optimizing model specifications. The purpose of this library is to make the process of running regression modeling and coefficient interpretation easier for those unfamiliar with regressions.

## Use
Users who are not familiar with our regression methodologies can use these four functions to run regression analysis.
* Function 1 - summarizer: Users input a dataset. The function returns with a table of variable description and summary statistics, with instructions on choosing a dependent variable and a set of independent variable(s). The function also returns instruction on choosing dependent and independent variables for regression, using accessible language for those unfamiliar with regressions.
* Function 2 - possibleModels: Users input a dataset and dependent variable. The function checks dependent variable for class and recommends an initial regression technique. For instance, if the dependent variable is binary, the function recommends a logit or probit regression as opposed to recommending OLS for a continuous dependent variable.
* Function 3 - interpreter: Users input a data set and a formula of regression. The function runs the regression and outputs the coefficients of predictors and the model’s diagnostics, along with text interpretation for each parameters and explanation of the model’s various diagnostics. The interpretation will be based on model specifications -- log-log, lin-log, quadratics, VARs, etc. For instance, the function could describe what a coefficient means in terms of the user’s independent and dependent variables, for example: “a one unit change in x correlates with a B unit change in y.” Other text outputs could explain the meaning of a p-value and statistical significance, the adjusted R-squared term or the cumulative significance of the model.
* Function 4 - optimizer: Users input a dependent variable and a set of potential independent variables. Function checks combinations of independent variables looking for those with the best model fit, such as the lowest error rate or highest adjusted R-squared, and outputs data frames sorted by the model fit stats. The function also allows users to input options including what variables should be included in all specifications, whether to include quadratic terms, etc.


## Installation
 1. First, you will need to install thee package "devtool" in order to install pacakges on github:
```
install.package("devtool")
```
 2. Load the devtool package:    
```
    library(devtool)
```
 3. Install the regressr package using "author/pacakge":
```
    install_github("GeorgetownMcCourt/regressr")
```
 4. Load the regressr package to use it:
 ```
    library(regressr)
 ```

## Usage
TODO: Write usage instructions
Note: If you're providing a new package or software, provide examples of how to use your code (example: https://github.com/CommerceDataService/eu.us.opendata). If you're providing an analytical output, describe what goes on each file or how to run it.
#### summarizer
```
summarizer(df)
```
#### possibleModels
```
possibleModels(df)
```
#### interpreter
```
interpreter(modelType, dependentVar, independentVar, df, logDepen = F, logIndepen = NULL, squareIndepend = NULL)
```

#### optimizer
```
optimizer(df, dependentVar, independentVar = colnames(df)[colnames(df) != dependentVar], include = NULL,

          model = c("OLS", "binary probit", "binary logit", "ordered probit", "ordered logit", "multinomial logit", "multinomial probit"),
          quadratic = NULL, cubic = NULL,
          time.series = FALSE, time.var = NULL, save.csv = FALSE)


```

## Progress Log
 Write history in bullet form of what progress has been made and when.
 * Proposal submitted, 3/31/2017
 * Project mock code agreed upon, 4/18/2017
 * Function 1 - summarizer
<<<<<<< HEAD
   *  
=======

>>>>>>> origin/yh
 * Function 2 - possibleModels
 * Function 3 - interpreter
 * Function 4 - optimizer
  * Base function created, 4/20/2017
  * More user input options added, 4/23/2017





## Credits
Author: Justin Goss, Yixuan Huang, Nghia-Piotr Le

Credits: Jeff Chen, Dan Hammer :hammer:

## License
MIT License

Copyright (c) 2017 PiotrLeTrong

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
