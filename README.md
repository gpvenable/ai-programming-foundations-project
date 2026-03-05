# AI Programming Foundations Project

## Project Description

This project demonstrates a reproducible data science workflow using Python.  
The notebook loads, cleans, analyzes, and visualizes a real dataset to identify patterns and insights.

## Dataset

Dataset: NYC Airbnb Listings  
Source: https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data

The dataset contains information about Airbnb listings in New York City including price, location, room type, and review activity.

## What This Project Does

- Loads a real-world dataset using Pandas
- Cleans and prepares the data for analysis
- Performs exploratory data analysis
- Creates visualizations to explore pricing and listing patterns
- Documents the workflow in a reproducible notebook

## How to Run This Project

### 1. Clone the repository
git clone https://github.com/gpvenable/ai-programming-foundations-project.git


### 2. Navigate to the project folder
cd ai-programming-foundations-project

### 3. Install dependencies
pip install -r requirements.txt

pip freeze > requirements.txt

### 4. Open the notebook

Run Jupyter Notebook or open the project in VS Code and open:
data_workflow.ipynb

Run the notebook cells from top to bottom.

## Reproducibility

A `requirements.txt` file is included to ensure that the same Python environment can be recreated when running this project.

## Responsible Practice (Bias and Data Quality)

Data cleaning decisions can introduce bias or unintentionally remove meaningful data. In this project, price outliers below $10 and above $1000 were removed to prevent extreme values from distorting visualizations. However, removing high price listings could exclude legitimate luxury properties that represent a different market segment.

Similarly, missing values in the `reviews_per_month` column were replaced with zero. While this assumption works for many listings, it may also represent newly created listings that have not yet received reviews. These types of cleaning choices can influence the conclusions drawn from the data.

To mitigate bias in future analyses, a more nuanced approach could involve analyzing outliers separately rather than removing them entirely and incorporating additional features such as amenities, room size, and geographic location.

## Future Integration Reflections

### Machine Learning Workflow

If this project were extended into a machine learning workflow, additional steps would be required. The dataset would need to be split into training and testing sets to evaluate model performance. Feature engineering would likely be necessary to transform categorical variables such as `room_type` and `neighbourhood_group` into numerical representations using encoding techniques. 

Model evaluation metrics such as Mean Absolute Error (MAE) or Root Mean Squared Error (RMSE) could be used to assess predictive performance if the goal were to predict listing prices.

### Neural Network Data Preparation

Neural networks typically require additional data preparation steps compared to traditional analysis workflows. Numerical features would need to be normalized or scaled to ensure consistent input ranges. Categorical variables would need to be converted into numerical representations using one-hot encoding or embedding layers.

In addition, feature selection or dimensionality reduction techniques might be applied to reduce noise and improve model performance.

### Agentic Automation Opportunities

AI agents could automate several parts of this workflow. For example, agents could automatically perform data quality checks, identify missing values, and recommend appropriate cleaning strategies. Agents could also generate exploratory visualizations, summarize statistical relationships, and suggest potential modeling approaches.

In larger data pipelines, AI agents could orchestrate the workflow by ingesting data, validating schema consistency, running analysis scripts, and generating automated reports. This type of automation would improve efficiency while maintaining reproducibility.