Data Projects (TripleTen)
#### Project_9_TT  Machine learning in Business.

## PROJECT-9: Optimizing Oil Well Placement: A Predictive Analysis of Profits and Risks for OilyGiant Mining Company

### Project Description

In this project, we aim to help **OilyGiant Mining Company** find the best location for a new oil well. The company has geological data for three potential regions and needs a model to predict the volume of reserves in new wells, estimate profits, and evaluate the risk of losses. The goal is to identify the region with the highest potential profit and the lowest risk, ensuring that the risk of losses does not exceed 2.5%.

### Key Steps in the Project:
1. **Data Collection**: We are provided with data for oil wells in three regions, including features such as oil quality, volume of reserves, and other parameters.
2. **Model Development**: We build a **Linear Regression** model to predict the volume of reserves in new oil wells, using the provided geological data.
3. **Profit Calculation**: After predicting the reserves, we calculate the total profit from selecting the highest-value wells.
4. **Risk Assessment**: We use **Bootstrapping** to assess the risks of losses (negative profits) for each region.
5. **Recommendation**: Based on the predicted profits and risk evaluation, we recommend the best region for the development of new oil wells.

### Data Description

The dataset includes geological exploration data for three regions. Each file contains details about the oil wells, including:

- **ID**: Unique oil well identifier.
- **f0, f1, f2**: Features that represent geological points in each region.
- **Product**: Volume of reserves in the oil well (measured in thousand barrels).

The files for each region are:
- **geo_data_0.csv** — Data for Region 0
- **geo_data_1.csv** — Data for Region 1
- **geo_data_2.csv** — Data for Region 2

Each dataset contains 500 data points, with the objective of selecting the best 200 wells based on predicted reserves to maximize profit.

### Key Assumptions:
- **Revenue per barrel**: $4,500 (for each 1,000 barrels).
- **Development Budget**: $100 million for developing 200 wells.
- **Risk Evaluation**: We only consider regions where the risk of losses (negative profit) is less than 2.5%. Among those, the region with the highest average profit is selected.

### Project Workflow

1. **Data Preprocessing**:
    - Clean and prepare the datasets for analysis.
    - Split the data into a training set (75%) and a validation set (25%).

2. **Model Training**:
    - Train a **Linear Regression** model to predict the volume of reserves for new wells in each region.
    - Evaluate the model's performance using **RMSE** (Root Mean Squared Error) and **R²** score.

3. **Profit Calculation**:
    - Calculate the total profit for each region by summing the reserves predicted by the model for the 200 highest-value wells.
    - Assess which region yields the highest total profit.

4. **Risk Calculation**:
    - Use **Bootstrapping** (resampling) with 1,000 samples to simulate possible future outcomes and estimate the distribution of profits.
    - Calculate the **95% confidence interval** for profit and evaluate the **risk of losses** (the percentage of negative profits).

5. **Final Recommendation**:
    - Choose the region with the highest profit and the lowest risk of losses (below 2.5%).

## Requirements

To run this project, you need the following Python libraries:

- pandas: For data manipulation and analysis.
- numpy: For numerical operations.
- **matplotlib**: For visualizations and plotting results.
- **scikit-learn**: For model training and evaluation.
- **scipy**: For statistical calculations and bootstrapping.

### Conclusion


This project provides a predictive analysis that helps the OilyGiant Mining Company determine the optimal location for the development of new oil wells. By using Linear Regression to predict oil reserves and Bootstrapping to assess the risk of losses, we recommend the region that offers the highest expected profit and meets the company's risk tolerance criteria.

### Key Findings:


Region 1: Average profit = $4,259,385.27, Risk of losses = 6%
Region 2: Average profit = $5,152,227.73, Risk of losses = 1%
Region 3: Average profit = $4,259,385.27, Risk of losses = 6%
Recommendation: Region 2 is the optimal location for new oil wells due to its highest profit and lowest risk of losses (1%).
