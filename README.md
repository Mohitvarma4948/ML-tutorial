Logistic Regression Tutorial – Diabetes Prediction (Pima Dataset)

This repository contains a short tutorial project built around Logistic Regression using the Pima Indians Diabetes dataset.
The aim is to show how logistic regression works on a real medical dataset, explain each step clearly, and evaluate the model in a simple and reproducible way.

The project follows these steps:

Load and inspect the dataset (diabetes.csv)

Prepare the data (scaling, splitting, basic checks)

Train a Logistic Regression classifier

Evaluate performance (accuracy, confusion matrix, ROC curve, AUC)

Look at how the decision threshold affects predictions

Examine model coefficients to see which features matter

The notebook is meant to be easy to follow and educational rather than overly technical.

Repository Structure
├── diabetes.csv                # Dataset (Pima Indians Diabetes)
├── logistic_regression.ipynb   # Main notebook for the tutorial
├── README.md                   # Documentation for the repo
└── LICENSE                     # Project license

About the Dataset

The dataset contains several diagnostic measurements for female patients aged 21+.
Features include glucose level, BMI, blood pressure, age, and insulin.
The target column is Outcome:

0 = no diabetes

1 = diabetes

It’s a commonly used dataset for introductory classification problems because the features are numerical and the task is realistic.

Model Overview

Logistic Regression estimates the probability that a given sample belongs to the positive class (diabetes).
This is done using the sigmoid function, which outputs values between 0 and 1.
By default, values above 0.5 are classified as “diabetes”, and values below are “no diabetes”.

Because the features are on different scales, the model is trained on standardised inputs.
This helps the optimisation behave properly and makes the coefficients easier to interpret.

Results Summary

A quick summary of what the notebook finds:

The baseline accuracy on the test set is reasonable for such a noisy, real-world dataset.

The confusion matrix shows that the model is better at identifying non-diabetic patients than diabetic ones.

The ROC curve and AUC score (~0.75+) show that the model has moderate discriminatory ability.

Lowering or raising the decision threshold changes the balance between sensitivity and specificity.

The coefficients indicate that glucose, BMI, and age contribute most strongly to predicting diabetes.

These results match what you’d expect from medical data where some features play much larger roles than others.

How to Run the Notebook

Download or clone the repository:

git clone <your_repo_url>
cd <repo_folder>


Install required packages:

pip install numpy pandas scikit-learn matplotlib seaborn


Make sure diabetes.csv is in the same folder.

Open the notebook:

jupyter notebook logistic_regression.ipynb


Everything should run as-is.

Figures in the Notebook

The notebook generates a few helpful visuals:

Correlation heatmap

Confusion matrix

ROC curve

Accuracy vs threshold graph

Coefficient bar chart

All plots are saved in-line and can be exported if needed for a report.

Reproducibility

All code is fully reproducible, and each cell includes comments explaining what’s happening.
The only requirement is that the dataset file is named diabetes.csv and stored in the root directory.

License

This work is shared under the MIT License.
You are free to reuse the code for academic and personal learning purposes.