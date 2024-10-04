# Airbnb-NYC-Listing

**New York City Airbnb Open Data** | Performing Data Wrangling, Analysis, Visualization, Regression, Classification, Hypothesis-Testing

This repository contains the code and workflows for handling, analyzing, and modeling the New York City Airbnb listing data from 2019. The project aims to extract insights, explore market trends, and build predictive models related to Airbnb listings in New York City.

## Table of Contents

- [Dataset](#dataset)
- [Wrangling](#wrangling)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis)
- [Visualization](#visualization)
- [Modeling](#modeling)
- [Hypothesis Testing](#hypothesis-testing)
- [Conclusions](#conclusions)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Dataset

The dataset used for this analysis is the **New York City Airbnb Open Data** for 2019. It includes over 48,000 Airbnb listings across the five boroughs of NYC. This dataset captures various attributes about the listings and hosts, enabling in-depth data analysis.

Key features of the dataset include:

- **Listing ID**: Unique identifier for each listing.
- **Host Information**: Host ID, Host Name, and other demographic data.
- **Location**: Neighborhood group (Manhattan, Brooklyn, etc.), Specific Neighborhood.
- **Room Type**: Entire home/apt, Private room, Shared room.
- **Pricing**: Price per night for each listing.
- **Availability**: Number of available nights and booking windows.
- **Review Metrics**: Total number of reviews, Last review date, Review scores, etc.
  
The dataset is publicly available and can be downloaded [here](http://insideairbnb.com/get-the-data.html).

## Wrangling

The data wrangling step ensures that the dataset is clean, well-structured, and ready for analysis. The following tasks were performed:

- **Handling Missing Data**: Identifying and filling/removing missing values.
- **Outlier Detection**: Detecting extreme values in variables such as `price` and `availability`.
- **Feature Engineering**: Creating additional relevant features such as:
  - Length of time since last review.
  - Price per person (based on room type and capacity).
- **Data Type Conversion**: Ensuring the correct format for variables like dates and prices.

All of these preprocessing steps are located in the `wrangle` module.

## Exploratory Data Analysis (EDA)

The `analysis` module dives deep into the data, offering:

- **Descriptive Statistics**: Understanding the basic distribution of key features like price, number of reviews, and availability.
- **Neighborhood Trends**: Insights into which neighborhoods are more expensive, have higher demand, or receive more reviews.
- **Correlation Analysis**: Investigating how variables like price, availability, and review scores are correlated with each other.
  
EDA provides the foundation for further predictive modeling and hypothesis testing.

## Visualization

The visualizations offer a clear understanding of the dataset, revealing trends, patterns, and outliers. The visualizations generated in this project include:

- **Histograms**: Distribution of prices, reviews, and availability.
- **Scatter Plots**: Relationships between features like price vs. number of reviews.
- **Box Plots**: Price comparisons across neighborhoods or room types.
- **Heatmaps**: Correlations between numeric features.
  
Visualizations are essential for both exploratory analysis and communicating the findings effectively. All visualizations are generated using popular libraries such as Matplotlib and Seaborn.

## Modeling

This project employs various predictive models to derive insights from the data. The `modeling` module includes:

- **Regression Models**: Linear and multiple regression models to predict prices or availability based on key features.
- **Classification Models**: Classifying listings into categories, such as predicting whether a listing will be booked or receive high reviews.
- **Model Evaluation**: Evaluating the performance of models using metrics like R², accuracy, precision, recall, and F1 score.

The modeling results can help potential hosts optimize their listings or guests identify the best neighborhoods to stay in.

## Hypothesis Testing

Several hypotheses were tested in this project to verify assumptions about the Airbnb market in NYC:

- **Price Differences by Neighborhood**: Do listings in Manhattan charge significantly higher prices than listings in other boroughs?
- **Room Type vs. Price**: Does room type (Entire home vs. Private room) have a significant impact on the price?
- **Reviews vs. Demand**: Does the number of reviews correlate with higher occupancy rates?

By testing these hypotheses, the project provides insights into market dynamics and guest behavior.

## Conclusions

This project successfully provides a comprehensive analysis of the New York City Airbnb listing data, with key findings such as:

- **Price Trends**: Manhattan consistently has the highest average listing prices, with entire homes/apartments commanding the most.
- **Review Patterns**: Listings with more reviews tend to have higher booking rates, indicating guest trust and demand.
- **Room Type Insights**: Shared rooms are less in demand and priced significantly lower than private rooms or entire apartments.
  
These insights can be valuable for Airbnb hosts looking to optimize their listings or guests seeking affordable stays in New York City.

## Installation

To run this project locally, you need to install the following dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Additionally, ensure you have the following tools installed:

- **Python 3.7+**
- **Jupyter Notebook** (optional, for running and editing notebooks)

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/Airbnb-NYC-Listing.git
   cd Airbnb-NYC-Listing
   ```

2. Load the dataset and run the analysis notebooks:

   ```bash
   jupyter notebook
   ```

3. Open and execute the `.ipynb` files in sequence:
   - `01-Wrangle.ipynb`
   - `02-EDA.ipynb`
   - `03-Visualization.ipynb`
   - `04-Modeling.ipynb`

4. Analyze the results and interpret the visualizations to draw conclusions about the NYC Airbnb market.

## Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository, make your changes, and submit a pull request. Before submitting, ensure that your code passes any relevant tests and includes documentation where appropriate.

---
