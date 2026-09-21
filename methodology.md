# Research Methodology

## 1. Refined Research Question

How accurately can machine learning classification models predict the species of an Iris flower using sepal and petal measurements?

## 2. Dataset Description

The Iris dataset is a small and widely used dataset for classification. It contains 150 flower samples belonging to three Iris species: Iris Setosa, Iris Versicolor, and Iris Virginica.

The dataset contains four numerical input features:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

The target variable is the flower species.

### Dataset Size

- Number of samples: 150
- Number of input features: 4
- Number of target classes: 3
- Samples per class: 50

### Features

The four features represent measurements of the sepal and petal in centimeters.

### Target

The target variable is `species`, which contains three classes:

- Iris-setosa
- Iris-versicolor
- Iris-virginica

### Dataset Limitations

The dataset is relatively small and contains only three Iris species. It is also a very clean and simple benchmark dataset, so results obtained from it may not represent performance on larger and more complex real-world classification problems. In addition, the dataset contains only four numerical measurements and does not include other information such as environmental conditions or visual characteristics.

## 3. Data Cleaning Plan

The following steps will be used to clean the dataset:

1. Load the CSV dataset using pandas.
2. Check the number of rows and columns.
3. Check for missing values.
4. Check for duplicate rows.
5. Check the data types of all columns.
6. Convert feature columns to numeric values if necessary.
7. Remove or handle duplicate or invalid records if found.
8. Check the distribution of the target classes.
9. Separate the input features from the target variable.

Since the Iris dataset is already relatively clean, major data cleaning may not be required.

## 4. Feature Engineering Plan

The four original numerical measurements will be used as the main features.

The following feature engineering steps will be considered:

- Separate the four measurement columns from the target column.
- Encode the categorical target labels into numerical labels if required.
- Standardize the numerical features for models that are sensitive to feature scale, especially K-Nearest Neighbors and Logistic Regression.
- Avoid creating unnecessary features because the dataset is small and already contains meaningful measurements.

## 5. Models

Two supervised machine learning classification models will be used.

### Model 1: Logistic Regression

Logistic Regression will be used as a baseline classification model. It is suitable for multi-class classification and provides a simple way to establish a baseline performance for the Iris dataset.

### Model 2: K-Nearest Neighbors (KNN)

K-Nearest Neighbors will be used as the second classification model. KNN classifies a sample based on the classes of nearby training samples and is suitable for a small numerical dataset such as Iris.

Using two different classification approaches will allow their performance to be compared using the same evaluation metrics.

## 6. Train-Test Split

The dataset will be divided into training and testing sets.

A test size of 20% will be used, meaning approximately 80% of the data will be used for training and 20% for testing.

A fixed random state will be used so that the experiment can be reproduced.

Stratified splitting will be used to maintain a similar class distribution in both the training and testing datasets.

## 7. Evaluation Metrics

The models will be evaluated using the following metrics:

### Accuracy

Accuracy measures the proportion of correctly classified samples out of all test samples. It is appropriate for this dataset because the three classes have equal representation.

### Precision

Precision measures how many samples predicted as a particular class actually belong to that class.

### Recall

Recall measures how many samples from a particular class are correctly identified by the model.

### F1-Score

F1-score combines precision and recall into a single measure and is useful for evaluating classification performance across the three classes.

### Confusion Matrix

A confusion matrix will also be used to examine which Iris species are correctly classified and where classification errors occur.

## 8. Experiment Procedure

The experiment will follow these steps:

1. Load the Iris dataset.
2. Explore the dataset.
3. Clean the data.
4. Separate features and target.
5. Encode the target labels if necessary.
6. Split the data into training and testing sets.
7. Standardize the features.
8. Train the Logistic Regression model.
9. Train the KNN model.
10. Predict the test samples using both models.
11. Calculate accuracy, precision, recall, and F1-score.
12. Display confusion matrices.
13. Compare the results of the two models.
14. Write the findings and possible improvements at the end of the notebook.