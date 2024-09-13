# Amazon Stock Price Prediction Project

## Table of Contents

- [Introduction](#introduction)
- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Features Selected](#features-selected)
- [Technologies Used](#technologies-used)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Model Building](#model-building)
- [Model Evaluation](#model-evaluation)
- [Results and Findings](#results-and-findings)
- [Conclusion](#conclusion)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

---

## Introduction

This project aims to predict Amazon's stock prices using historical market data and various financial indicators. By leveraging machine learning techniques, we seek to understand the complex relationships between Amazon's stock price and influential market variables such as commodity prices and other tech giants' stock performances.

## Project Overview

Stock price prediction is a crucial aspect of financial analytics, offering valuable insights for investors, traders, and stakeholders. In this project, we:

- **Loaded and cleaned historical market data** from multiple sources.
- **Selected key features** that potentially influence Amazon's stock price.
- **Built and evaluated** a Linear Regression model to predict Amazon's stock price.
- **Analyzed feature importance** to understand the impact of each selected variable.

## Dataset Description

The dataset (`Stock Market Dataset.csv`) contains historical data on various commodities, stocks, and indices from January 29, 2024, to February 2, 2024, totaling 1,243 entries with 39 columns. Key data points include:

- **Commodity Prices and Volumes**: Natural Gas, Crude Oil, Copper, Gold, Silver, Platinum.
- **Cryptocurrency Prices and Volumes**: Bitcoin, Ethereum.
- **Stock Prices and Volumes**: Amazon, Meta (Facebook), Netflix, Apple, Tesla, Microsoft, Google, Nvidia, Berkshire Hathaway.
- **Market Indices**: S&P 500, Nasdaq 100.

## Features Selected

The following features were selected for predicting Amazon's stock price:

1. **Natural Gas Price**
2. **Crude Oil Price**
3. **Meta (Facebook) Stock Price**
4. **Netflix Stock Price**
5. **Gold Price**

### Rationale for Feature Selection

- **Natural Gas Price**: Influences Amazon's operational costs due to energy consumption in data centers and warehouses.
- **Crude Oil Price**: Affects transportation and logistics costs, impacting shipping expenses.
- **Meta Stock Price**: Serves as an industry indicator, reflecting market trends affecting tech companies.
- **Netflix Stock Price**: Indicates consumer engagement in digital services, relevant to Amazon's streaming services.
- **Gold Price**: Acts as an economic sentiment indicator, inversely related to stock market performance during uncertainty.

## Technologies Used

- **Programming Language**: Python
- **Data Manipulation and Analysis**: Pandas, NumPy
- **Data Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn
- **Jupyter Notebook**: For interactive coding and analysis

## Data Preprocessing

- **Handled Missing Values**: Filled missing numerical values with column means.
- **Data Type Conversion**: Converted numerical data stored as strings (due to commas) into proper numeric types.
- **Feature Scaling**: Standardized features using `StandardScaler` to ensure equal contribution to the model.

## Exploratory Data Analysis

- **Data Inspection**: Used `data.head()`, `data.info()`, and `data.describe()` to understand data structure and summary statistics.
- **Visualization**:
  - **Histograms**: Analyzed the distribution of Amazon's stock price.
  - **Scatter Plots**: Explored relationships between Amazon's stock price and selected features.
  - **Correlation Matrix**: Identified correlations between variables.

## Model Building

- **Model Selection**: Linear Regression model from Scikit-learn.
- **Data Splitting**: Divided data into training and testing sets (80/20 split).
- **Training**: Fit the model on the training data.
- **Cross-Validation**: Performed 5-fold cross-validation to assess model robustness.

## Model Evaluation

- **Metrics Used**:
  - **Mean Absolute Error (MAE)**: 8.52
  - **Mean Squared Error (MSE)**: 112.80
  - **Root Mean Squared Error (RMSE)**: 10.62
- **Feature Importance**: Analyzed coefficients to determine the impact of each feature on the prediction.

## Results and Findings

- **Model Performance**: The Linear Regression model demonstrated reasonable accuracy in predicting Amazon's stock price.
- **Key Influencers**:
  - **Netflix Price** and **Meta Price** had significant positive coefficients, indicating a strong positive relationship with Amazon's stock price.
  - **Crude Oil Price** had a negative coefficient, suggesting that higher oil prices might negatively impact Amazon's stock price due to increased operational costs.

## Conclusion

The project successfully developed a predictive model for Amazon's stock price using selected market indicators. The findings highlight the interconnectedness of various market factors and their influence on a major tech company's stock performance. This model can serve as a foundation for more complex predictive analytics and can be enhanced with additional data and advanced modeling techniques.

## Project Structure

```
├── README.md
├── Stock Market Dataset.csv
├── Amazon_Stock_Prediction_Model.ipynb  # Jupyter Notebook with code and analysis
├── images                               # Directory for visualizations and plots
└── requirements.txt                     # Python dependencies
```

## Usage

To replicate the analysis:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/Amazon_Stock_Prediction_Model.git
   ```

2. **Navigate to the Project Directory**:

   ```bash
   cd Amazon_Stock_Prediction_Model
   ```

3. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Jupyter Notebook**:

   ```bash
   jupyter notebook Amazon_Stock_Prediction_Model.ipynb
   ```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or suggestions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
