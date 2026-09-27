# Credit Card Customer Segmentation

A machine learning project for segmenting credit card customers based on their financial behavior and usage patterns using unsupervised learning techniques.

## Overview

Customer segmentation helps identify groups of customers with similar behavioral characteristics. In this project, credit card customer data is analyzed and clustered using several unsupervised machine learning algorithms.

The workflow includes data exploration, missing-value handling, feature scaling, cluster evaluation, dimensionality reduction, and visualization of customer groups.

## Dataset

The dataset contains information about approximately 8,950 credit card customers and includes features related to:

- Account balance
- Purchase amount
- One-off purchases
- Installment purchases
- Cash advances
- Purchase frequency
- Cash advance frequency
- Number of transactions
- Credit limit
- Payments
- Minimum payments
- Percentage of full payments
- Account tenure

Customer IDs are removed before model training because they do not provide meaningful behavioral information for clustering.

## Project Workflow

### 1. Data Exploration

The dataset is first explored using descriptive statistics, missing-value analysis, distribution plots, scatter plots, and correlation analysis.

### 2. Data Preprocessing

Preprocessing includes:

- Removing non-informative identifiers
- Handling missing values
- Inspecting feature distributions
- Standardizing numerical variables using `StandardScaler`

Feature scaling is particularly important for distance-based clustering algorithms such as K-Means because the dataset contains variables with substantially different numerical ranges.

### 3. Selecting the Number of Clusters

Different numbers of clusters are evaluated using:

- Elbow Method
- Silhouette Score

These techniques are used to identify a suitable number of customer segments before training the final clustering model.

### 4. K-Means Clustering

K-Means is used as the primary clustering algorithm to divide customers into groups with similar credit card usage behavior.

After clustering, the distribution and characteristics of each group are explored through multiple visualizations.

### 5. PCA Visualization

Principal Component Analysis (PCA) is used to reduce the standardized feature space to two dimensions.

This makes it possible to visually inspect the separation and distribution of customer clusters.

### 6. Alternative Clustering Algorithms

Several additional clustering techniques are explored for comparison:

- Affinity Propagation
- BIRCH
- MiniBatch K-Means
- Gaussian Mixture Models

These models provide alternative approaches for discovering structure within the customer dataset.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Kneed

## Machine Learning Techniques

- Unsupervised Learning
- K-Means Clustering
- Cluster Evaluation
- Feature Standardization
- Principal Component Analysis (PCA)
- Gaussian Mixture Models
- BIRCH Clustering
- MiniBatch K-Means
- Affinity Propagation

## Key Objective

The objective of this project is to identify distinct patterns of credit card usage and group customers according to their financial behavior.

Such segmentation can provide a foundation for applications such as:

- Customer profiling
- Personalized marketing
- Targeted financial services
- Behavioral analysis
- Customer relationship management

## Repository Structure

```text
credit-card-customer-segmentation/
│
├── customer_segmentation.ipynb
├── README.md
└── requirements.txt
```

## Installation

Clone the repository:

```bash
git clone https://github.com/USERNAME/credit-card-customer-segmentation.git
cd credit-card-customer-segmentation
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Main dependencies include:

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
kneed
```

## Future Improvements

Potential improvements include:

- More systematic cluster profiling
- Comparison using additional clustering metrics
- Automated hyperparameter selection
- Improved handling of outliers
- Interactive cluster visualizations
- Deployment of the segmentation model through an API
- Building a dashboard for exploring customer segments

## Author

Developed as a machine learning and data science project focused on unsupervised customer segmentation.
