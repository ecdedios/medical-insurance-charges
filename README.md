# Medical Insurance Charges - Linear and Ridge Regression

> Work in progress! Exploratory data analysis and machine learning prediction of medical insurance charges framed as a regression problem using Jupyter Notebooks and Power BI.

## Project Description

Exploratory data analyses, linear regression, and interactive dashboard.

## Data

https://www.kaggle.com/datasets/mirichoi0218/insurance/data

## Findings

The most interesting insight is...

![Feature Importances](https://github.com/ecdedios/medical-insurance-charges/blob/main/viz/Screenshot%202024-12-11%20211122.png)

### Key Interpretations

#### 1. Relative Importance of Features

**age (Coefficient: 0.800387):**

This is the most important feature based on the absolute coefficient value.
A unit increase in age (e.g., one additional year) is associated with an average increase of 0.800387 in the target variable (charges), assuming other variables remain constant.

**bmi smoker (Coefficient: 0.654838):**

This interaction term indicates that the combined effect of bmi and smoker is significant.
A unit increase in this combined factor increases charges by approximately 0.654838.

**age smoker (Coefficient: -0.568252):**

This negative coefficient suggests that the combined effect of age and smoker reduces charges by approximately 0.568252 for a unit increase, which could be due to a compensating effect or complex relationship.

#### 2. Positive and Negative Effects

**Positive Coefficients:**

- Features like age, bmi smoker, children, and bmi have positive coefficients, indicating they increase charges.
- Example: Having more children (children) or a higher BMI (bmi) contributes to higher insurance charges.

**Negative Coefficients:**

- Features like age smoker, bmi^2, and age children have negative coefficients, implying they reduce charges.
- Example: The quadratic term bmi^2 suggests diminishing or reversing effects of BMI on charges when BMI becomes very high.

#### 3. Interactions and Non-Linear Effects

**Interaction Terms:**

- bmi smoker, age smoker, and age children represent interactions between variables.
- Example: The interaction bmi smoker suggests that the charges increase significantly for individuals who smoke and have a high BMI.

**Quadratic Terms (bmi^2, age^2):**

- These indicate non-linear relationships.
- Example: bmi^2 with a negative coefficient suggests that while bmi initially increases charges, the effect diminishes or reverses at higher BMI levels.

#### 4. Magnitude of Coefficients

- The absolute coefficient value (Abs_Coefficient) indicates the strength of the feature's impact on the target.
- Features with larger absolute coefficients have a greater influence.
  - Example: age (0.800387) has a much larger impact than age^2 (-0.105856).

### Practical Implications

**1. Age is a Primary Factor:** Age has the largest positive impact on insurance charges, likely reflecting increased health risks or medical needs as people grow older.

**2. Smoking's Influence:** The combined effects of smoking (e.g., bmi smoker, age smoker) show a significant influence, highlighting the added cost burden for smokers.

**3. Children's Effect:** More children slightly increase charges, possibly due to family insurance plans.

**4. BMI's Role:** BMI is positively correlated with charges, but its quadratic term (bmi^2) suggests a complex relationship where the increase levels off or reverses at very high BMI values.

**5. Interactions and Complexity:** Interactions like bmi smoker reveal that the combination of multiple factors (e.g., high BMI and smoking) has a compounding effect on charges.

### Actionable Insights

#### 1. Policy Design:

Insurance providers might focus on age and lifestyle factors like smoking to adjust premiums.

#### 2. Health Interventions:

Programs targeting smoking cessation and BMI management could help reduce overall medical costs.

#### 3. Model Refinement:

Including these interaction terms and quadratic terms ensures the model captures more complex relationships, improving prediction accuracy.

**This analysis highlights the importance of examining both individual and combined effects of features to understand their influence on the target variable.**

## Interactive Dashboard

![Power BI Dashboard](https://github.com/ecdedios/medical-insurance-charges/blob/main/viz/Screenshot%202024-12-11%20210940.png)

[Link to the dashboard](https://app.powerbi.com/view?r=eyJrIjoiMmMxODkxZDQtOTJjMi00N2Y0LTg4MDEtMjdlNTM5OTBjODU0IiwidCI6IjAwZmI2OGUxLWQ5ZTktNGZiOC04MzdjLTNhMzcxMmYyZGNlYiJ9)

## Reference

https://github.com/stedy/Machine-Learning-with-R-datasets

## Usage

Written in Python 3.12. Libraries/packages used:

- power bi
- notebook
- pandas
- matplotlib
- seaborn
- scikit-learn

To see the project in action, open and run the notebooks or view and interact with the dashboard.

## Meta

Ednalyn C. De Dios – [@ecdedios](https://github.com/ecdedios)

Distributed under the MIT license. See `LICENSE` for more information.

- LinkedIn: [in/ecdedios/](https://www.linkedin.com/in/ecdedios/)
- Resumé: [http://ednalyn.com](http://ednalyn.com)
- Data Science Projects [https://datasciencenerd.us](https://datasciencenerd.us)

## Contributing

1. Fork it (<https://github.com/ecdedios/medical-insurance-charges/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

2024
