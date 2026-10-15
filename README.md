# Machine Learning-Based Anomaly Detection System for University Network Traffic

## Project Overview

This project explores the application of Machine Learning techniques to detect anomalous network connections and distinguish normal traffic from potentially malicious activity.

The project uses the NSL-KDD benchmark dataset to investigate how machine learning can support network intrusion detection and contribute to network security monitoring.

## Objectives

* Analyze network connection records and their characteristics.
* Preprocess network traffic data for machine learning.
* Develop a binary classification approach to distinguish normal connections from attacks.
* Explore machine learning techniques for network intrusion detection.
* Evaluate model performance using appropriate classification metrics.

## Dataset

### NSL-KDD

This project uses the **NSL-KDD dataset**, a benchmark dataset for evaluating network intrusion detection systems.

The dataset contains labeled network connection records representing normal activity and different categories of network attacks.

**Dataset details:**

* **Dataset Name:** NSL-KDD
* **Training File:** `KDDTrain+.txt`
* **Testing File:** `KDDTest+.txt`
* **Data Format:** Comma-separated text files
* **Data Type:** Structured, connection-level network traffic records
* **Original Dataset Family:** KDD Cup 99

### Data Sources

The project notebook loads the training and testing data from the following public repository:

* **Training Data:** [KDDTrain+.txt](https://raw.githubusercontent.com/defcom17/NSL_KDD/master/KDDTrain%2B.txt)
* **Testing Data:** [KDDTest+.txt](https://raw.githubusercontent.com/defcom17/NSL_KDD/master/KDDTest%2B.txt)
* **Dataset Reference:** [Canadian Institute for Cybersecurity — NSL-KDD](https://www.unb.ca/cic/datasets/nsl.html)

### Network Traffic Features

The dataset describes network connections through features such as:

* Connection duration
* Protocol type
* Network service
* Connection status
* Source and destination byte counts
* Connection statistics and error rates
* Host-based traffic statistics

These features provide information that machine learning models can use to identify patterns associated with normal connections and network attacks.

**Important:** NSL-KDD is a benchmark dataset, not a collection of traffic captured directly from a university network.

## Data Preprocessing

The project notebook includes the following preprocessing steps:

1. Loading the training and testing datasets.
2. Inspecting the data structure and numerical statistics.
3. Removing selected columns with predominantly zero values.
4. Converting the original attack labels into a binary classification target:

   * `normal`: Normal network connections.
   * `attack`: Connections labeled as attacks.
5. Encoding categorical features into numerical values.
6. Scaling the input features using `StandardScaler`.

The target variable is used to distinguish normal network connections from attack-related connections.

## Machine Learning Approach

The notebook imports several machine learning algorithms and identifies tree-based models, including:

* Random Forest
* LightGBM

The notebook also imports tools for feature selection, hyperparameter tuning, handling imbalanced data, and model interpretability.

The final set of trained models and their evaluation results should be documented after verifying the completed experiments.

## Model Evaluation

The notebook includes evaluation and visualization utilities for assessing classification performance.

The evaluation metrics include:

* **Accuracy:** The proportion of correctly classified samples.
* **Precision:** The proportion of predicted attacks that are actual attacks.
* **Recall:** The proportion of actual attacks correctly identified.
* **F1-Score:** The harmonic mean of precision and recall.
* **AUC-ROC:** A measure of the model's ability to distinguish between the two classes.

The notebook also contains utilities for generating confusion matrices, ROC curves, precision-recall curves, and feature-importance plots.

Actual performance values should be reported only after confirming the results of the final model runs.

## Technologies

* Python
* Google Colab
* Pandas
* NumPy
* Scikit-learn
* LightGBM
* Matplotlib
* Seaborn
* Machine Learning
* Network Intrusion Detection

## Project Notebook

The project notebook is available on Google Colab:

[Open the Project Notebook](https://colab.research.google.com/drive/1jnDgpnhHhWPCHXyhnAsQjKcI4Kt_hPei?usp=sharing)

## Repository Contents

The repository contains:

* The Jupyter Notebook with the project code.
* Project documentation.
* An MIT License.

## Limitations

* The project uses a benchmark dataset rather than live traffic captured from a university network.
* Results obtained using NSL-KDD may not directly represent performance on modern university networks.
* The effectiveness of the final system depends on the trained models, preprocessing choices, and evaluation methodology.

## Future Improvements

Potential improvements include:

* Completing and documenting the model training and evaluation pipeline.
* Comparing multiple classification algorithms.
* Analyzing feature importance and model interpretability.
* Evaluating the impact of class imbalance.
* Testing the approach on additional network intrusion detection datasets.
* Exploring how the approach could be adapted for university network monitoring.

## Author

**Hamid Mamoun**

Electronics and Semiconductors Engineering

**Areas of Interest:** Computer Networks, Cybersecurity, Machine Learning, and Artificial Intelligence.
