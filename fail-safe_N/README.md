# Fail-Safe N Manual

Fail-safe N (fail-safe number) is a method originally proposed by Rosenthal (1979) “for testing whether a significant result of meta-analysis can be made not significant by the addition of N studies that have an average null effect” (Evans, 1996). It is “a procedure by which one can estimate whether publication biases (if they exist) may be safely ignored” (Rosenberg, 2005).

Fail-safe N (fail-safe number) is the number of new, unreported or unretrieved studies with non-significant or null results that would be required to bring the overall significance of a meta-analysis to non-significant level (or any other desired level) (Rosenthal, 1979; Persaud, 1996).

Calculation of the Rosenthal’s fail-safe N involves adding the standard normal deviates (Z) associated with statistical significance (p) of each study and then dividing it by the square root of the number of studies that are being combined (Rosenthal, 1979).

Orwin developed the method further by proposing a fail-safe N for effect size, based on Cohen’s d. The method estimates the number of additional studies that are required to lower the observed mean effect size to minimal effect size (Orwin, 1983; Rosenberg, 2005).

Next development came from Rosenberg who suggested a weighted fail-safe N, in which “N is equivalent to the number of studies of null effect and mean weight necessary to reduce the observed significance level to α” (Rosenberg, 2005).

Gleser & Olkin on the other hand put forward a fail-safe N method that “provides a model (or models) to explain how reported p-values could be predominantly small (significant)” (Gleser & Olkin, 1996).

## Practical use

The fail-safe N method was implemented in the following R-packages:

metafor: Meta-Analysis Package for R
https://cran.r-project.org/web/packages/metafor/index.html 
Possible options for the fail-safe N calculation are "Rosenthal" (the default), "Orwin", or "Rosenberg".

fsn: Rosenthal's Fail Safe Number and Related Functions
https://cran.r-project.org/web/packages/fsn/index.html
Package enables calculation of Rosenthal’s fail-safe number including confidence intervals. Details of the proposed method are described in papers by Fragkos, Tsagris, and Frangos (2014; 2017).

## Interpretation and limitations

Usually, Rosenthal's fail-safe number turns out to be high, suggesting that results of the meta-analysis are trustworthy. However, the fail-safe number is considered to be a gross overestimate and an unreliable metric, giving its users a false sense of security (Ferguson & Heene, 2012).

Rosenthal's fail-safe N method is based on the assumption that effect size of unreported studies is zero, but there are instances in which the unpublished studies could have an effect in the opposite direction or that their effect is small but not zero. In those cases, the number of studies needed to nullify the effect may be different than the fail-safe N estimate, either smaller or larger (Evans, 1996; Fragkos, Tsagris & Frangos, 2017).  

Scargle and Schonemann point out that Rosenthal's fail-safe N “treats the file drawer of unpublished studies as unbiased by assuming that their average Z value is zero. But if only 5% of studies that show Type I errors were published, the mean Z value of the remaining unpublished studies cannot be zero but must be negative” (Fragkos, Tsagris & Frangos, 2017).

## Authors and sources

The technique was introduced by Robert Rosenthal. There are other versions of the method proposed by Robert G. Orwin, Michael S. Rosenberg, Leon J. Gleser and Ingram Olkin.

Michail Tsagris, Constantinos Frangos and Christos Frangos proposed calculation of Rosenthal’s fail safe number including confidence intervals.

## References

Evans, S. (1996). Misleading meta-analysis. Statistician’s comment. BMJ (Clinical research ed.). 312. 125.

Ferguson, C. J., & Heene, M. (2012). A Vast Graveyard of Undead Theories: Publication Bias and Psychological Science’s Aversion to the Null. Perspectives on Psychological Science, 7(6), 555–561. https://doi.org/10.1177/1745691612459059

Fragkos, K.C, Tsagris, M., & Frangos, Ch.C. (2017). Exploring the distribution for the estimator of Rosenthal’s "fail-safe" number of unpublished studies in meta-analysis. Communications in Statistics-Theory and Methods, 46(11):5672–5684. https://doi.org/10.1155%2F2014%2F825383

Fragkos, K.C, Tsagris, M., & Frangos, Ch.C. (2014). Publication Bias in Meta-Analysis: Confidence Intervals for Rosenthal’s Fail-Safe Number. International Scholarly Research Notices, Volume 2014. https://doi.org/10.1080%2F03610926.2015.1109664

Gleser, L.J. & Olkin, I. (1996). Models for estimating the number of unpublished studies. Statistics in Medicine, 15: 2493-2507.

Orwin, R. G. (1983). A Fail-Safe N for Effect Size in Meta-Analysis. Journal of Educational Statistics, 8(2), 157–159. https://doi.org/10.2307/1164923

Persaud, R. (1996). Misleading meta-analysis. "Fail safe N" is a useful mathematical measure of the stability of results. BMJ (Clinical research ed.). 312. 125.

Rosenberg, M.S. (2005). The file-drawer problem revisited: a general weighted method for calculating fail-safe numbers in meta-analysis. Evolution, 59: 464-468. https://doi.org/10.1111/j.0014-3820.2005.tb01004.x

Rosenthal, R. (1979). The file drawer problem and tolerance for null results. Psychological Bulletin, 86(3), 638–641. https://doi.org/10.1037/0033-2909.86.3.638





