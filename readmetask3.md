## PRODIGY INFO TECH TASK 3
## PRAGADEESH G

## Task-03
Build a decision tree classifier to predict whether a customer will purchase a product or service based on their demographic and behavioral data. Use a dataset such as the Bank Marketing dataset from the UCI Machine Learning Repository

# Decision Tree Classifier for Bank Marketing Dataset

This repository contains the implementation of a Decision Tree Classifier to predict whether a customer will subscribe to a term deposit based on the Bank Marketing dataset. The task involves training the model, evaluating its performance, and visualizing the decision tree.

## Table of Contents
- [Installation](#installation)
- [Dataset](#dataset)
- [Features](#features)
- [Usage](#usage)
- [Visualization](#visualization)
- [Results](#results)

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/decision-tree-bank-marketing.git
    cd decision-tree-bank-marketing
    ```

2. Create a virtual environment and activate it:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

## Dataset

The dataset used in this task is the Bank Marketing dataset. It is available from the UCI Machine Learning Repository: [Bank Marketing Data Set](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing).

## Features

The dataset contains the following features:
- `age`: Age of the customer
- `job`: Type of job
- `marital`: Marital status
- `education`: Level of education
- `default`: Has credit in default?
- `housing`: Has housing loan?
- `loan`: Has personal loan?
- `contact`: Contact communication type
- `month`: Last contact month of the year
- `day_of_week`: Last contact day of the week
- `duration`: Last contact duration, in seconds
- `campaign`: Number of contacts performed during this campaign
- `pdays`: Number of days since the client was last contacted from a previous campaign
- `previous`: Number of contacts performed before this campaign
- `poutcome`: Outcome of the previous marketing campaign
- `cons.price.idx`: Consumer price index
- `cons.conf.idx`: Consumer confidence index
- `deposit`: Target variable (yes or no)

## Usage

1. Ensure that the dataset is in the same directory as the script or update the script to load the dataset from the correct path.

2. Run the script to train the Decision Tree Classifier and visualize it:
    ```sh
    python decision_tree_classifier.py
    ```

## Visualization

The decision tree is visualized using the `plot_tree` function from `sklearn.tree`. The plot displays the structure of the decision tree, including the splits based on feature values, sample counts, and class distributions.

## Results

The performance of the Decision Tree Classifier is evaluated using various metrics like accuracy, precision, recall, and the confusion matrix. The results are printed in the console.


