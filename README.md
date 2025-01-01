# A/B Testing Analysis

This project performs A/B testing analysis to evaluate the impact of different groups (control and treatment) on various metrics such as conversion rates and purchase amounts.

## Data Source

The dataset is generated synthetically for demonstration purposes. It includes various features such as session duration, pages viewed, purchase amount, device type, traffic source, location, group (control/treatment), conversion status, customer segment, and ad spend.

## Steps

### 1. Generating Synthetic Data
- Set a random seed for reproducibility.
- Generate synthetic data for session duration, pages viewed, purchase amount, device type, traffic source, location, group, conversion status, customer segment, and ad spend.
- Create a DataFrame and save it as `enhanced_cro_data.csv`.

### 2. Data Preparation
- Load the dataset from `enhanced_cro_data.csv`.
- Add calculated variables to simulate higher conversion likelihood for the treatment group and higher purchase amounts for converted users.

### 3. A/B Testing Analysis
- Evaluate the impact of group (control/treatment) on conversion rates.
- Calculate the correlation between group and conversion.
- Fit a logistic regression model to predict conversion based on group and other features.
- Visualize the purchase amount by group.

## Key Functions and Methods

- `np.random.normal()`: Generates random numbers from a normal distribution.
- `np.random.poisson()`: Generates random numbers from a Poisson distribution.
- `np.random.choice()`: Generates random samples from a given array.
- `pd.DataFrame()`: Creates a DataFrame from a dictionary.
- `pd.to_csv()`: Saves a DataFrame to a CSV file.
- `sns.histplot()`: Creates a histogram plot with Seaborn.
- `ols()`: Fits an ordinary least squares regression model.
- `ttest_ind()`: Performs a t-test for the means of two independent samples.

## Findings

- **Correlation between Group and Conversion**: The correlation between the group (control/treatment) and conversion was calculated.
- **Logistic Regression Model**: A logistic regression model was fitted to predict conversion based on group and other features.
- **Purchase Amount Visualization**: The purchase amounts were visualized by group (control/treatment) using a histogram plot.


## Dependencies

- pandas
- numpy
- seaborn
- matplotlib
- statsmodels

## Usage

1. Ensure all dependencies are installed.
2. Run the notebook to generate synthetic data, evaluate the impact of A/B testing on conversion rates, and visualize the results.

## Notes

- Adjust the parameters for synthetic data generation as needed based on specific requirements.
- Ensure the dataset contains the necessary columns: `session_duration`, `pages_viewed`, `purchase_amount`, `device`, `source`, `location`, `group`, `converted`, `customer_segment`, and `ad_spend`.
