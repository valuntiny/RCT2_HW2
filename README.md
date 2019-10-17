A 24 Weeks Study on Efficacy of Exenatide and Phenylpropanolamine Twice Daily in Subjects With Type 2 Diabetes
--------------------------------------------------------------------------------------------------------------

The primary aim of this study is to investigate whether the new drug
Exenatide has a higher efficacy in type 2 diabetes patients from New
York-Presbyterian Hospital, than an existing drug Phenylpropanolamine.
We have four primary outcomes for this study:

-   Change in HbA1c From Baseline to Week 24

-   Change in BMI From Baseline to Week 24

-   Change in Fast Plasma Gloucose From Baseline to Week 24

-   Change in Waist to Height Ratio From Baseline to Week 24

We choose interventional (a.k.a. randomized clinical trial, RCT) study
design, and assign two arms in this study:

-   Treatment Arm: 5 mcg Exenatide twice daily for 24 weeks

-   Active Control Arm: 5 mcg Phenylpropanolamine twice daily for 24
    weeks

Because RCT can help avoid lead time bias and minimize heterogeneity
effect among treatment and control arms. In RCT, we choose *α* level at
0.05 for suitable type I error control, and choose power Design at 80%
level. Then we choose Design Alternative (DA) as 5 to make sure the
standardized effect size is appropriate. The whole study lasts for 24
weeks, so that we leave enough time for drugs to take effect, and also
minimize the environmental/random effect. Also known from prior studies,
we found out that the retention rate is 95%, *σ* is 10 and cross-over
rate in each arm is 5%, no Intra-Class Correlation (ICC).

Based on four primary outcomes, we have four null hypotheses:

-   *H*<sub>01</sub>: no difference between treatment and control arm
    regard to the change in HbA1c from baseline to week 24, or
    *μ*<sub>1*T*</sub> = *μ*<sub>1*C*</sub>

-   *H*<sub>02</sub>: no difference between treatment and control arm
    regard to the change in BMI from baseline to week 24, or
    *μ*<sub>2*T*</sub> = *μ*<sub>2*C*</sub>

-   *H*<sub>03</sub>: no difference between treatment and control arm
    regard to the change in Fast Plasma Gloucose from baseline to week
    24, or *μ*<sub>3*T*</sub> = *μ*<sub>3*C*</sub>

-   *H*<sub>04</sub>: no difference between treatment and control arm
    regard to the change in Waist to Height Ratio from baseline to week
    24, or *μ*<sub>4*T*</sub> = *μ*<sub>4*C*</sub>

For each null hypothesis individually, we use two sample T-test to test
the null, the corresponding statistic =
$\\frac{\\overline{x\_{iT}} - \\overline{x\_{iC}}}{\\sigma \\cdot \\sqrt{\\frac{2}{n}}} \\sim t\_{2n-2}$,
where *n* = *n*<sub>*C*</sub> = *n*<sub>*T*</sub> and *i* = 1, 2, 3, 4.
But overall, since we have multiple outcomes we also need to adjust for
family-wise error rate (FWER), here we choose Holm Step Down method for
adjusting the outcome p-value.

We don't need to include any other covariates because the recruiting and
randomization part eliminates the imbalance of other covariates between
treatment and control arms, and also covariates such as gender or age
are not confounders in this study. But for sure there will be missing
data due to drop out or cross-over, in that case, we treat the missing
data as MCAR, so analyzing the observed data won't include any bias.

Based on our null hypotheses and FWER control method, below is the
procedure:

1.  rank 4 p-values ascending, let's say it's
    *p*<sub>3</sub> &lt; *p*<sub>1</sub> &lt; *p*<sub>2</sub> &lt; *p*<sub>4</sub>

2.  compare *p*<sub>3</sub> with 0.05/4 = 0.0125, if
    *p*<sub>3</sub> &gt; 0.0125 then stop, do not reject any
    *H*<sub>0*i*</sub> and state that there is no difference in efficacy
    on subjects with type 2 diabetes between Exenatide and
    Phenylpropanolamine from baseline to week 24. If
    *p*<sub>3</sub> &lt; 0.0125, then reject *H*<sub>03</sub> and state
    that there is enough evidence to support the difference between
    treatment and control arm regard to the change in Fast Plasma
    Gloucose from baseline to week 24, and go to (3)

3.  compare *p*<sub>1</sub> with 0.05/3 = 0.0167, if
    *p*<sub>1</sub> &gt; 0.0167 then stop, do not reject
    *H*<sub>01</sub>, *H*<sub>02</sub>, *H*<sub>04</sub>. If
    *p*<sub>1</sub> &lt; 0.0167, then reject *H*<sub>01</sub> and state
    that there is enough evidence to support the difference between
    treatment and control arm regard to the change in HbA1c from
    baseline to week 24, and go to (4)

4.  compare *p*<sub>2</sub> with 0.05/2 = 0.025, if
    *p*<sub>2</sub> &gt; 0.025 then stop, do not reject
    *H*<sub>02</sub>, *H*<sub>04</sub>. If *p*<sub>2</sub> &lt; 0.025,
    then reject *H*<sub>02</sub> and state that there is enough evidence
    to support the difference between treatment and control arm regard
    to the change in BMI from baseline to week 24, and go to (5)

5.  compare *p*<sub>4</sub> with 0.05/1 = 0.05, if
    *p*<sub>4</sub> &gt; 0.05 then stop, do not reject *H*<sub>04</sub>.
    If *p*<sub>4</sub> &lt; 0.05, then reject all the *H*<sub>0*i*</sub>
    and state that there is enough evidence to support the difference in
    efficacy on subjects with type 2 diabetes between Exenatide and
    Phenylpropanolamine from baseline to week 24

### power analysis

$$
\\begin{split}
D 
&= (Z\_{\\alpha/2} + Z\_{\\beta})\\sigma\\sqrt{\\frac{1}{n\_{T}} + \\frac{1}{n\_{C}}} \\\\
&= (Z\_{\\alpha/2} + Z\_{\\beta})\\sigma\\sqrt{\\frac{2}{n}} \\\\
where: \\\\
&D = 5 \\\\
n &= n\_{T} = n\_{C} \\\\
\\alpha &= 0.05, Z\_{0.025} = 1.96 \\\\
\\beta &= 0.8, Z\_{0.8} = 0.84 \\\\
\\sigma &= 10
\\end{split}
$$

Then, we calculate the final `n` we need based on retention and
cross-over:

-   get designed n

-   adjust for retention: *n*′=*n*/0.95

-   adjust for cross-over: $n'' = \\frac{n'}{(1 - p\_{T} - p\_{C}) ^ 2}$

We calculate the final *n*″= 81.507 , so in total the sample size we
need ≈ 164.
