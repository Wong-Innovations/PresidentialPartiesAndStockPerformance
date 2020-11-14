# PresidentialPartiesAndStockPerformance

A Bruce Choe and Dylan Wong Research Project

## Table of Contents

* [Abstract](#abstract)
* [Sourcing Data](#sourcing-data)
  * [GDP](#gdp)
  * [Index Funds](#index-funds)
  * [Recession / Expansion Periods](#recession-expansion)
* [Methodology](#method)
* [Results](#results)
* [Future Plans](#future-plans)
* [Contact](#contact)
* [Acknowledgements](#acknowledgements)

<!-- ABOUT THE PROJECT -->
## Abstract
The purpose of this research project is to determine if there is a correlation between presidential party affiliation and the performance of the U.S. economy? We will compare the behavior of key economic indicators such as the real GDP and Total Market Index Funds (such as the S&P 500, Dow Jones, et cetera). Then if we find a statistically significant difference in these factors based on historical presidential party affiliation, we will try to gain insight as to the reason for said difference. Economic expansion vs recession periods, presidential term lag factors via autocorrelation, and several other factors will be tested to explain the potential difference in economic performance during U.S. presidencies.

<!-- SOURCING DATA -->
## Sourcing Data

We will begin this project using open source stock and GDP data described below. Our hope is that with future research funding we will be able to pay for more complete and accurate data to substantiate our findings.

### GDP

tbu

### Index Funds

Using [Yahoo Finance](https://finance.yahoo.com) we can get reasonably accurate opening and closing prices to calculate percentage increase/decrease ourselves. However, yahoo finance provides very little information on the indexes beyond that.

### Recession / Expansion Periods

The [NBER: National Bureau of Economic Research](https://www.nber.org/research/data/us-business-cycle-expansions-and-contractions) traditional definition of a recession is that it is a significant decline in economic activity that is spread across the economy and that lasts more than a few months. The committee's view is that while each of the three criteria—depth, diffusion, and duration—needs to be met individually to some degree, extreme conditions revealed by one criterion may partially offset weaker indications from another. While other economists define recession as two consecutive periods of decline in real gdp. We will be testing both cases.

<!-- METHODOLOGY -->
## Methodology

We first calculate the change in economic indicator on a yearly and quarterly basis, then we sort these data points based on presidential party affiliation and compare the respective average growth. This is implemented by the following snippet of [python code](https://github.com/Wong-Innovations/PresidentialPartiesAndStockPerformance/blob/aff5aa3d0661e8f8dfda7234b4a89d7ffe239407/IXIC/IXIC.py#L119-L130). The next step is to calculate the likelihood that the Democratic average would vary from the Republican average by the amount observed. For this we calculate t-scores in both directions and use the resulting p-value to say with a given confidence that there is a resulting corelation. More can be learned about t-scores [here](https://www.statisticshowto.com/probability-and-statistics/t-distribution/t-score-formula/), we determined this statistical significance test to be the most appropriate for our data set since it take into account the degrees of freedom (number of samples). If we had a VERY large dataset a z-score would be just as appropriate since the data would be normally distributed.

<!-- RESULTS -->
## Results



<!-- FUTURE PLANS -->
## Future Plans



<!-- CONTACT -->
## Contact

Please contact us with any questions about our research or with any business related propositions.

Bruce Choe: [Github](https://github.com/BruceChoe), [bruceleechoe@gmail.com](bruceleechoe@gmail.com)
Dylan Wong: [Github](https://github.com/Wong-Innovations), [dylanwong@nevada.unr.edu](dylanwong@nevada.unr.edu)

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

Thank you to [UNR ACM](https://acm.cse.unr.edu/) for hosting the hackathon that provided the inspiration and served as a launch pad for this project.
Additionally thank you to all the professors, colleagues, and family who support our education.