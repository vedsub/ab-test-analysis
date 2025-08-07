# A/B Test Analysis for a New Checkout Page

## Business Problem
This project analyzes the results of an A/B test conducted by an e-commerce company. The company tested a new checkout page design against their old design to see if it would increase the user conversion rate. The goal of this analysis is to provide a data-driven recommendation on whether to launch the new page for all users.

## Data
The dataset used is a public A/B testing dataset from Kaggle. It contains user-level information on which page they saw and whether they converted. The data was cleaned to remove mismatched entries and duplicate users.

## Methodology
The analysis was conducted in Python using Pandas for data manipulation and Scipy for statistical testing.
1.  **Data Cleaning:** Removed inconsistent data where users in the 'control' group saw the new page and vice-versa. Duplicate user entries were also removed.
2.  **Hypothesis Formulation:**
    -   **Null Hypothesis (H₀):** The new page has no positive effect on the conversion rate.
    -   **Alternative Hypothesis (H₁):** The new page increases the conversion rate.
3.  **Statistical Test:** A one-tailed Z-test for two proportions was used to determine if the increase in conversion rate for the treatment group was statistically significant at a 95% confidence level (α = 0.05).

## Results
-   **Control Conversion Rate:** 12.04%
-   **Treatment Conversion Rate:** 11.88%
-   **P-value:** 0.9093

The p-value is much higher than 0.05, indicating that we do not have statistical evidence to reject the null hypothesis.

![Conversion Rate Comparison](comparison_chart.png)
*(You will need to save the chart from your notebook as `comparison_chart.png` and add it to the folder)*

## Conclusion & Recommendation
**Do not launch the new page.** The new design did not lead to a statistically significant improvement in the conversion rate. Further investigation is recommended to understand user behavior on the new page before iterating on the design.

## How to Run
1. Clone this repository.
2. Install the required libraries: `pip install pandas numpy matplotlib seaborn jupyterlab`
3. Run the Jupyter Notebook: `jupyter lab ab_test_analysis.ipynb`
