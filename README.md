# Meta-analysis-of-Ocean-Acidification-Effects-on-Behaviour

## Data Structure
Data from the Clark *et al* paper, as well as meta data from 91 other studies on the effects of ocean acidification on the behavious of various fish species. 


## Workflow 
Summary statistics of data from the Clark *et al.* (2020) were calculated for each of the fish species and each treatment: Means, standard deviation (sd), sample size (N). Species names were altered to scientific names, and column names were altered to match the ocean_meta_data. 
The data sets were added together, and a column of residuals for observation level analysis added. 

Calculated the log response ratio (lnRR) effect size between the treatment and control mean of the meta data. NAs were generated from negative means, these data points were excluded from further analysis. 

Multivariate meta-analytic model using rma.mv function from metafor package were fitted to the data, controlling for sampling variance and including the random effect of the study and observation. The r^2^ and I^2^ values were calculated from the model. An orchard plot showing the mean log response ratio (lnRR) was generated. 

To visualise if there was any publication bias, a funnel plot of the response ratio against precision (1/SE) was generated. Then a timelag plot was created, to visualise the change in effect size (lnRR) over time, including the change in precision. 

A multi-level regression model of the effect size with publication year as a fixed effect was fitted to the data. The r^2^ values were calculated from the model.
A multi-level regression model of the effect size with the inverse sampling variance as a fixed effect, was fitted to the data. The r^2^ values were calculated from the model.

The created models and graphs were analysed to indicate whether or not publication bias is present in the data. The meta-analysis by Clement *et al* (2022) was contrasted to, in regards to findings.
