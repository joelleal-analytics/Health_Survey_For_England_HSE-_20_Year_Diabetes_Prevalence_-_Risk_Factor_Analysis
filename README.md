# Health Survey for England HSE: 20 Year Diabetes Prevalence and Risk Factor Analysis

## Executive Summary
An exploration an statistical data analysis was conducted on the Health Survey for England datasets from 1999 and 2019 to evaluate the 20-year trajectory of diagnosed diabetes prevalence. Utilizing Python (`pandas`, `scipy.stats`, `statsmodels`), the project investigates the national prevalence growth, demographic risk shifts across age groups and gender, BMI category correlations, and controls for confounding variables via logistic regression.

## Key Findings and Statistical Insights
1. **Significant National Prevalence Increase:**
   * A one-tailed two-proportion z-test confirms a statistically significant increase in diagnosed diabetes prevalence in England, rising from 6.27% in 1999 to 7.78% in 2019 (**z = 3.59, p < 0.001*)
2. **Age Group Vulnerability (Chi-Square Analysis):**
    * A chi-square test of independence revealed an extremely significant association between age brackets and diabetes status (**X<sup>2</sup> = 412.35, p = 6.18e-86*). Older demographics (specifically ages 55-74 carry a disproportionately higher prevalence.
3. **BMI Impact (Mann-Whitney U Test):**
   * Individuals with diagnosed diabetes exhibit a statistically significantly higher mean and median BMI compared to non-diabetics (**p = 9.36e-15*), validated robustly through non-parametric testing to account for distribution skewness.
4. **Multivariate Risk control (Logistic Regression):**
   * Controlling for age and BMI, logistic regression results indicate that females exhibit roughly 38% lower odds ( or ~0.62) of diagnosed diabetes compared to males (reference group) in the 2019 cohort.
  
## Statistical Methodology and Tech Stack
* **Language and Libraries:** Python (`pandas`, `numpy`, `matplotlib`, `scupy.stats`, `statsmodels`)
* **Data Sources: Health Survey for England:** (`HSE_1999.dta`, `HSE_2019.dta`)
* **Statistical Tests Executed:**
  * **Chi-Square Test of Independence:** Testing categorical association between age groups and diabetes.
  * **Mann-Whitney U Test:** Comparing BMI distributions between diabetic and non-diabetic populations.
  * **Logistic Regression:** Estimating odds ratios while controlling for age, BMI, and gender.
  * **Two-Proportion Z-test:** Evaluating directional population growth over the 20-year span.

 ## Repository Structures and Visualizations
 The analysis generates comparative visual artifacts stored directly within the workspace:
 * `diabetes_comparison.png`: National prevalence comparison between 1999 and 2019.
 * `diabetes_by_age.png`: Age-stratified prevalence breakdowns across cohorts.
 * `diabetes_by_gender.png`: Gender-segemented prevalence comparisons.
 * `diabetes_by_bmi.png`: BMI category distribution anaysis.

### Note on Implementation and Methodology:
The complete Python code , data cleaning scripts, demographic breakdowns, and statistical modeling tests are fully documented and executable within the accompanying Jupyter Notebook file.
