# Hotel Reservation Cancellations Analysis

## Business Problem

The City Hotel and Resort Hotel have experienced a significant rise in cancellation rates in recent years. This has led to challenges such as reduced revenue and underutilized hotel rooms. This project aims to analyze hotel booking cancellations, identify contributing factors, and provide recommendations to mitigate cancellations and improve hotel profitability.

## Project Overview

This project uses data analysis techniques to explore the relationship between various factors and hotel reservation cancellations. The primary goal is to identify patterns that can help reduce cancellations and optimize pricing strategies, especially during peak cancellation periods.

### Key Insights:
- **Price Impact:** Increasing prices are associated with higher cancellation rates. 
  - **Solution:** Implement more dynamic pricing strategies, such as offering discounted rates for specific room types or locations to attract more bookings and reduce cancellations.
  
- **Seasonal Trends:** Cancellations peak in January, likely due to factors such as post-holiday financial constraints.
  - **Solution:** Launch marketing campaigns with attractive offers during January to boost bookings and revenue.

- **Policy Adjustment:** A high number of cancellations may be attributed to lenient no-deposit policies.
  - **Solution:** Introduce stricter cancellation and deposit policies, such as higher withdrawal fees or non-refundable deposits, to decrease cancellations.
 
## Cleaning Data
Here’s a description for your GitHub README that outlines the data cleaning process:

---

## Data Cleaning Process

This project involves cleaning a dataset to ensure it is ready for analysis. Below are the steps taken to clean the data:

### 1. Identifying Missing Values
We start by checking the dataset for any missing values (NaN) using `df.isnull().sum()`. This allows us to see which columns contain missing data and how many values are missing in each column.

### 2. Dropping Unnecessary Columns
In this step, we remove the columns that are not required for analysis. For example, the `company` and `agent` columns were dropped using:
```python
df.drop(['company', 'agent'], axis=1, inplace=True)
```

### 3. Handling Missing Data
For columns with missing values, we decided to remove rows containing any missing values (NaN) to ensure the dataset only includes complete rows. This was done using:
```python
df.dropna(inplace=True)
```
This step ensures that there are no missing values left in the dataset, making it suitable for analysis.

### 4. Rechecking for Missing Values
After cleaning, we rechecked the dataset for any remaining missing values with:
```python
df.isnull().sum()
```
This step confirms that the dataset is now free from missing values and is ready for further analysis.


## Data Analysis and Findings

The data analyzed includes factors such as room types, average daily rate (ADR), and hotel type. One of the visualizations used in the analysis is:

```python
sns.boxplot(data=data, x='reserved_room_type', y='adr', hue='hotel')
```

This box plot provides insights into the relationship between the room type, ADR, and cancellation rates across both hotel types.

## Suggestions

- Refine pricing strategies to offer discounts for specific locations and customers to reduce cancellations.
- Launch marketing campaigns during January with special offers to mitigate the seasonal spike in cancellations.
- Adjust cancellation policies to include stricter fees and deposit requirements to reduce the high rate of cancellations.

## Getting Started

### Prerequisites:
- Python 3.x
- Jupyter Notebook or any Python IDE
- Required libraries:
  - pandas
  - seaborn
  - matplotlib

To install the required dependencies, run:

```bash
pip install pandas seaborn matplotlib
```

### Running the Analysis:

Clone the repository and run the `analysis.py` script to perform the data analysis.

```bash
git clone https://github.com/yourusername/hotel-cancellation-analysis.git
cd hotel-cancellation-analysis
python analysis.py
```

### Results and Outputs:

The analysis outputs several visualizations and insights, including the box plot showing the relationship between room types, ADR, and hotel types. The results will guide the formulation of strategies to reduce cancellations and increase revenue.
