# Funnel Plot Manual

Funnel plot is a graphical display to examine patterns and to detect bias in meta-analyses. The shape of the plot may suggest whether a bias exists (Light & Pillemer, 1984).

“A funnel plot is a scatter plot of the effect estimates from individual studies against some measure of each study’s size or precision” (Sterne et al., 2011).

Standard error with a reversed scale is considered to be the best choice for the vertical axis. Larger, most powerful studies are then placed towards the top of the plot (Sterne et al., 2011; Sterne & Egger, 2001). Precision (1/SE) or inverse of variance (1/variance) can be useful when comparing meta-analyses of small trials with large trials. The use of sample size or log sample size is not advisable because the shape of the plot may be unpredictable when there is no bias (Sterne & Egger, 2001). 
The ratio measure of treatment effect, preferably the log odds ratio should be plotted on the horizontal axis (Sterne & Egger, 2001).
The choice of axis is discussed in detail in the article by Sterne & Egger (2001).

Funnel plots are usually drawn with additional contour lines, displaying areas of statistical significance and indicating its conventional milestones (e.g., !0.01, !0.05, !0.1). This enhancement is an aid to differentiate asymmetry of the funnel plot due to publication bias from bias due to other factors (Peters et al., 2008).

## Practical use

The funnel plot method was implemented in the following R-packages providing methods for meta-analyses:

meta: General Package for Meta-Analysis
https://cran.r-project.org/web/packages/meta/index.html 

metafor: Meta-Analysis Package for R
https://cran.r-project.org/web/packages/metafor/index.html

## Interpretation and limitations

If standard error with a reversed scale is chosen for the vertical axis and if there is no bias, the funnel is expected to be symmetrical: smaller studies should be spread more widely at the bottom, and the spread should be narrower for larger studies. Contour lines to indicate 95% or 99% confidence should be straight (Sterne et al., 2011; Sterne & Egger, 2001).

“If studies appear to be missing in areas of statistical nonsignificance, then this adds credence to the possibility that the asymmetry is due to publication bias. Conversely, if the supposed missing studies are in areas of higher statistical significance, this would suggest the cause of the asymmetry may be more likely to be due to factors other than publication bias” (Peters et al., 2008).

The funnel plot method is considered to be controversial because of questions about appropriate interpretation (Sterne et al., 2011). The interpretation of funnel plots is often subjective (Sterne & Egger, 2001). 

It should be noted that there can be many sources of asymmetry in funnel plots: publication bias, English language bias, citation bias, multiple publication bias, heterogeneity, intensity of intervention, differences in underlying risk, data irregularities, poor methodological design of small studies, fraud, choice of effect measure, chance (Egger et al., 1997).

## Authors and sources

The technique was introduced by Richard J. Light and David B. Pillemer. This method was later improved and refined by various authors, among others: Jonathan A. C. Sterne and Matthias Egger.

## References

Egger, M., Davey Smith, G., Schneider, M., Minder, C. (1997). Bias in meta-analysis detected by a simple, graphical test. BMJ; 315:629-34.

Light, R., Pillemer, D. (1984). Summing up. The science of reviewing research. Cambridge, MA: Harvard University Press. 

Peters, J., Sutton, A., Jones, D., Abrams, K., Rushton, L. (2008). Contour-enhanced meta-analysis funnel plots help distinguish publication bias from other causes of asymmetry. Journal of Clinical Epidemiology. 61(10):991-6. doi: 10.1016/j.jclinepi.2007.11.010. PMID: 18538991.

Sterne, J., Egger, M. (2001). Funnel plots for detecting bias in meta-analysis: Guidelines on choice of axis.  Journal of Clinical Epidemiology. 54. 1046-55. 10.1016/S0895-4356(01)00377-8.

Sterne, J., Sutton, A., Ioannidis, J., Terrin, N., Jones, D., Lau, J., Carpenter, J., Ruecker, G., Harbord, R., Schmid, C., Tetzlaff, J., Deeks, J., Peters, J., Macaskill, P., Schwarzer, G., Duval, S., Altman, D., Moher, D., Higgins, J. (2011). Recommendations for examining and interpreting funnel plot asymmetry in meta-analyses of randomised controlled trials. BMJ. 343. 10.1136/bmj.d4002.
