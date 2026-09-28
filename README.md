# Employee Workplace Analytics

## Employee Burnout, Job Satisfaction, Technology Adoption & Productivity

A Python-based workplace survey analytics project examining employee wellbeing, technology adoption, turnover intention and productivity using statistical hypothesis testing and exploratory factor analysis.

### Project objective

The project investigates seven hypotheses using a cleaned workplace survey dataset. The analysis combines the results from Assessment 2 and Assessment 3 into one reproducible Jupyter Notebook.

### Key questions

- Does work arrangement relate to employee burnout?
- Does technology adoption differ across departments?
- Is department associated with turnover intention?
- Is role overload associated with burnout?
- Is burnout associated with job satisfaction?
- Do technology adoption, burnout and job satisfaction jointly predict productivity?
- Do the questionnaire items form the expected Role Overload, Burnout and Job Satisfaction constructs?

## Dataset

- **320 cleaned employee responses**
- Survey-based workplace data
- Main constructs: Role Overload, Burnout, Job Satisfaction, Technology Adoption and Productivity
- Reverse-worded items were reverse-coded before composite/factor analysis.
- The EFA used **309 complete cases** because it required complete responses across the 12 factor-analysis items.

## Statistical methods

| Hypothesis | Method | Main result |
|---|---|---|
| H1 | Welch's independent-samples t-test | t(130.98) = 4.110, p < .001, Cohen's d = .624 |
| H2 | One-way ANOVA + Tukey HSD | F(4,315) = 20.694, p < .001, η² = .208 |
| H3 | Chi-square test of independence | χ²(4) = 11.343, p = .023, Cramer's V = .188 |
| H4 | Pearson correlation | r = .426, p < .001 |
| H5 | Pearson correlation | r = -.496, p < .001 |
| H6 | Multiple linear regression | R² = .306, F(3,316) = 46.34, p < .001 |
| H7 | Exploratory factor analysis | KMO = .896; Bartlett p < .001; 3 factors; 66.879% variance |

All seven hypotheses were supported under the decision rules used in the coursework.

## Main findings

- Employees working onsite reported higher burnout than remote employees in H1.
- Technology adoption differed across departments in H2; Tukey HSD identified significant differences involving IT.
- Department and turnover intention were associated in H3.
- Higher role overload was associated with higher burnout in H4.
- Higher burnout was associated with lower job satisfaction in H5.
- Technology adoption and job satisfaction were positive predictors of productivity, while burnout was a negative predictor in H6.
- EFA supported three distinct constructs: Role Overload, Burnout and Job Satisfaction in H7.

## Regression details

The H6 model used:

**Dependent variable:** Employee productivity

**Predictors:**
- Technology adoption
- Burnout
- Job satisfaction

The model explained **30.6%** of the variance in productivity. Assumption checks did not indicate major problems: VIF values were low, Shapiro-Wilk p = .669, Breusch-Pagan p = .480, and Durbin-Watson = 2.162.

## EFA details

The EFA used:
- Principal axis factoring
- Oblimin rotation
- Kaiser criterion (eigenvalues > 1)
- Scree plot confirmation

The three retained factors corresponded to:
1. Role Overload
2. Burnout
3. Job Satisfaction

The three factors explained **66.879%** of total variance.

## Tools and technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- SciPy
- Statsmodels
- Matplotlib
- Statistical hypothesis testing
- Multiple linear regression
- Exploratory factor analysis

## Project structure

```text
employee-workplace-analytics/
├── employee_workplace_analytics.ipynb
├── data/
│   └── cleaned_workplace_survey.csv
├── README.md
├── requirements.txt
└── .gitignore
```

## How to run

```bash
git clone <your-github-repository-url>
cd employee-workplace-analytics

python -m pip install -r requirements.txt
jupyter notebook employee_workplace_analytics.ipynb
```

Run the notebook from top to bottom. The dataset path is already configured as:

```text
data/cleaned_workplace_survey.csv
```

## Portfolio / resume description

**Employee Workplace Analytics — Python | Pandas | SciPy | Statsmodels | Jupyter**

- Analysed 320 cleaned employee survey responses to investigate burnout, job satisfaction, technology adoption and productivity.
- Applied Welch's t-test, one-way ANOVA with Tukey HSD, chi-square, Pearson correlation and multiple linear regression.
- Performed exploratory factor analysis with KMO, Bartlett's test, eigenvalue/scree-plot retention and oblimin rotation.
- Found that technology adoption and job satisfaction positively predicted productivity, while burnout was a negative predictor.

## Note

This is an academic/portfolio analytics project. The findings describe statistical associations and prediction within the analysed dataset; they should not be interpreted as proof of causation.
