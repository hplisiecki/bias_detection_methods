# Z-curve description

The most recent (1/13/2022) version of this technique uses the finite mixture model with the Expectation Maximization algorithm (EM)  
to estimate the power of the studies in the meta-analytic batch after they were selected for significance in one direction.

It uses the distribution of z-scores to fit the curve, due to their normal distribution property.

The technique provides the following quantitative metrics to gauge the ammount of publication bias.  
All of the metrics come with confidence intervals arrived at through the use of bootstraping.

1. Observed Discovery Rate (ODR) - The percentage of statistically significant results in the meta-analytic batch.
2. Expected Discovery Rate (EDR) - The mean power of all studies in the meta-analytic batch.
3. Expected Replication Rate (ERR) - The mean power of all statistically significant studies in the meta-analytic batch.  
   Refers to the replication rate of a result in the same direction
   
## Practical use

The method was implemented in an R-package to be found here:
https://CRAN.R-project.org/package=zcurve

The function embedded in the package takes input of z-statistics or two-sided p-values.  
m.EM <- zcurve(z_scores, method = "EM", bootstrap = FALSE)

The results can be inspected using to additional functions  
summary(m.EM)  
plot(m.EM)  

## Interpretation and limitation

 The discrepancy between the EDR and ODR provides quantitative information about the amount of selection bias.
 
"If a meta-analysis shows low selection bias and a high replication rate, the results are credible. If a meta-analysis shows high selection bias and a low replication rate, the results are incredible and require independent verification."

"One limitation is that it does not distinguish between significant results with opposite signs. In the presence of multiple tests of the same hypothesis with opposite signs, researchers can exclude inconsistent significant results and estimate z-curve on the basis of significant results with the correct sign."
 
"Another limitation is the assumption that all studies used the same alpha criterion (.05) to select for significance. This possibility can be explored by conducting multiple z-curve analyses with different selection criteria (e.g., .05, .01). The use of lower selection criteria is also useful because some questionable research practices produce a cluster of just significant results."
  
