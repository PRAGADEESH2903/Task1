# Country Data Analysis and Visualization
### Create a bar chart or histogram to visualize the distribution of a categorical or continuous variable, such as the distribution of ages or genders in a population.
This project provides scripts to analyze and visualize country data. It includes sorting the top 10 countries, forward-filling duplicate data, and creating various bar charts to visualize the data.

## Table of Contents

- [Introduction](#introduction)
- [Setup](#setup)
- [Usage](#usage)
  - [Step 1: Sorting Top 10 Countries and Forward-Filling Data](#task-1-sorting-top-10-countries-and-forward-filling-data)
  - [Step 2: Plotting Total Values per Year](#task-2-plotting-total-values-per-year)
  - [Step 3: Plotting Each Country's Data Values Separately](#task-3-plotting-each-countrys-data-values-separately)
  - [Step 4: Plotting Top 10 Countries by 2023 Indicator](#task-4-plotting-top-10-countries-by-2023-indicator)


## Introduction

The purpose of this project is to visualize and analyze country data over time. The project includes several steps that demonstrate different aspects of data visualization using bar charts.

## Setup

1. **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/country-data-analysis.git
    cd country-data-analysis
    ```

2. **Install the required dependencies:**

    This project uses Python and the following libraries:
    - `pandas`
    - `matplotlib`
    - `seaborn`

    You can install the dependencies using `pip`:

    ```bash
    pip install pandas matplotlib seaborn
    ```

3. **Prepare your data:**

    Ensure your data is in a CSV file with the following format:

    ```csv
    Year,Country1,Country2,...,CountryN
    1960,Value1,Value2,...,ValueN
    1961,Value1,Value2,...,ValueN
    ...
    ```

## Usage

### Step 1: Sorting Top 10 Countries and Forward-Filling Data

1. **Load your data into a DataFrame:**

    ```python
    import pandas as pd

    # Load data from CSV file
    df = pd.read_csv("D:\prodigy info tech\Data1.csv")  ##use your path...
    ```

2. **Sort the top 10 countries based on the latest year's data:**

    ```python
    top_countries = df.nlargest(10, '2023')  # Replace '2023' with the latest year in your dataset
    ```

3. **Forward-fill the duplicate data:**

    ```python
    df = df.ffill(axis=1)
    ```

### Step 2: Plotting Total Values per Year

1. **Calculate total values per year:**

    ```python
    years = df.columns[1:]
    total_values = df[years].sum()
    ```

2. **Plot total values per year:**

    ```python
    import matplotlib.pyplot as plt

    plt.figure(figsize=(30, 30))
    plt.barh(years, total_values, color='#FFA500')
    plt.xlabel('Total Values')
    plt.ylabel('Year', size=20)
    plt.title('Total Values per Year', size=20)
    plt.show()
    ```

### Step 3: Plotting Each Country's Data Values Separately

1. **Transpose the DataFrame:**

    ```python
    country_by_1960_t = df.transpose()
    countries = country_by_1960_t.index
    years = country_by_1960_t.columns
    ```

2. **Plot each country's data values separately:**

    ```python
    import matplotlib.pyplot as plt

    for i, country in enumerate(countries):
        plt.figure(figsize=(10, 6))
        plt.bar(years, country_by_1960_t.loc[country], color='blue')
        plt.xlabel('Year')
        plt.ylabel('Data Values')
        plt.title(f'Data Values for {country}')
        plt.xticks(rotation=70)
        plt.show()
    ```

### Step 4: Plotting Top 10 Countries by 2023 Indicator

1. **Plot the top 10 countries for the latest year:**

    ```python
    plt.figure(figsize=(12, 8))
    plt.bar(top_countries['Country Name'], top_countries['2023'], color='skyblue')
    plt.title('Top 10 Countries by 2023 Indicator')
    plt.xlabel('Country Name')
    plt.ylabel('2023 Value')
    plt.xticks(rotation=45, ha='right')
    plt.grid(False)
    plt.show()
    ```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any features, bug fixes, or enhancements.....

