# Z-curve Manual

The most recent (11/13/2022) version of this technique uses the finite mixture model with the Expectation Maximization algorithm (EM)  
to estimate the power of the studies in the meta-analytic batch after they were selected for significance in one direction.

It uses the distribution of significant z-scores to fit the curve, due to the fact that the distribution of a tests with a given statistical power is a normal distribution. After that, it estimates z-curve on the "insignificant part".

The technique provides the following quantitative metrics to gauge the ammount of publication bias.  
All of the metrics come with confidence intervals arrived at through the use of bootstraping.

1. Observed Discovery Rate (ODR) - The percentage of statistically significant results in the meta-analytic batch.
2. Expected Discovery Rate (EDR) - The mean power of all studies in the meta-analytic batch.
3. Expected Replication Rate (ERR) - The mean power of all statistically significant studies in the meta-analytic batch.  
   Refers to the replication rate of a result in the same direction
   
## Practical use

The method was implemented in an R-package to be found here:  
https://CRAN.R-project.org/package=zcurve

The function embedded in the package takes input of z-statistics or two-sided p-values:  
m.EM <- zcurve(z_scores, method = "EM", bootstrap = FALSE)

The results can be inspected using two additional functions:  
summary(m.EM)  
plot(m.EM)  

## Interpretation and limitations

The discrepancy between the EDR and ODR provides quantitative information about the amount of selection bias.
ERR is an estimation of replication rate if replications will be conducted.
 
"If a meta-analysis shows low selection bias and a high replication rate, the results are credible. If a meta-analysis shows high selection bias and a low replication rate, the results are incredible and require independent verification." (Bartoš, Schimmack, 2021)

"One limitation is that it does not distinguish between significant results with opposite signs. In the presence of multiple tests of the same hypothesis with opposite signs, researchers can exclude inconsistent significant results and estimate z-curve on the basis of significant results with the correct sign." (Bartoš, Schimmack, 2021)

"Another limitation is the assumption that all studies used the same alpha criterion (.05) to select for significance. This possibility can be explored by conducting multiple z-curve analyses with different selection criteria (e.g., .05, .01). The use of lower selection criteria is also useful because some questionable research practices produce a cluster of just significant results." (Bartoš, Schimmack, 2021)

Replication rate in Open Science Colaboration (2015) was lower (25%) than estimated by z-curve (44% to 51%). It could happen by several reason, but "a third possibility for the discrepancy is that questionable research practices change the shape of the z-curve in ways that are different from a simple selection model". (Bartoš, Schimmack, 2021)

"For now, they should be considered the worst and the best possible scenarios and actual replication rates are expected to fall somewhere between [EDR and ERR] estimates." (Bartoš, Schimmack, 2021)

## Auhors and sources

The technique was created by František Bartoš and Ulrich Schimmack
The information above is based on their article outlining the use of that tool:
https://replicationindex.com/2020/01/10/z-curve-2-0/

## References:
Open Science Collaboration. (2015). Estimating the reproducibility of psychological science. Science, 349(6251), aac4716–aac4716. https://doi.org/10.1126/science.aac4716

Bartoš, F., & Schimmack, U. (2021, July 14). Z-Curve.2.0. Replicability-Index. Retrieved January 13, 2022, from https://replicationindex.com/2020/01/10/z-curve-2-0/  

Schimmack, U., & Brunner, J. (2017). Z-curve.