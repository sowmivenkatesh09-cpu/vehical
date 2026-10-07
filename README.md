# Vehicle Coupon Acceptance Prediction

## 📌 Project Overview

This project focuses on predicting whether a customer will accept a vehicle-related coupon based on different customer, travel, weather, and coupon-related characteristics.

The dataset contains information such as destination, passenger type, weather, temperature, time, coupon type, expiration, age, gender, marital status, education, occupation, income, and other coupon-related attributes.

Machine Learning classification algorithms are applied to predict the target variable `Y`, which represents coupon acceptance.

## 📊 Dataset

* **Dataset file:** `vehical.csv`
* **Rows:** 12,684
* **Columns:** 26
* **Target variable:** `Y`

### Major Features

* Destination
* Passenger
* Weather
* Temperature
* Time
* Coupon
* Expiration
* Gender
* Age
* Marital Status
* Has Children
* Education
* Occupation
* Income
* Car
* Bar
* CoffeeHouse
* CarryAway
* RestaurantLessThan20
* Restaurant20To50
* Distance-related features
* Direction-related features

## 🔍 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Checked the dataset structure and statistical information.
3. Checked for missing values and duplicate records.
4. Identified numerical and categorical features.
5. Handled missing values.
6. Converted categorical variables into numerical form using one-hot encoding.
7. Applied outlier handling using the IQR method.
8. Used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the target classes.
9. Applied **Chi-Square SelectKBest** for feature selection.
10. Selected the top 10 features.
11. Applied **StandardScaler** for feature scaling.
12. Split the processed dataset into training and testing sets.

## ⚖️ Class Balancing

The original target distribution was:

* Class `0`: 5,474
* Class `1`: 7,210

SMOTE was applied to balance the classes before model training.

After SMOTE:

* Total samples: **14,420**

## 🎯 Feature Selection

Chi-Square based `SelectKBest` was used to select the most relevant features.

The top features identified include:

* `coupon_Bar`
* `temperature`
* `coupon_Carry out & Take away`
* `expiration_2h`
* `CoffeeHouse_never`

The final model training uses the selected top 10 features.

## 🤖 Machine Learning Models

The following classification algorithms were implemented and compared:

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* Gradient Boosting Classifier
* AdaBoost Classifier

## 📈 Evaluation Metrics

The models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score

The models are trained on the training dataset and evaluated on the test dataset to compare their classification performance.

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn
* Jupyter Notebook

## 📁 Project Structure

```text
Vehicle-Coupon-Prediction/
│
├── vehical.csv
├── Vehicle_Coupon_Prediction.ipynb
└── README.md
```

## 📌 Conclusion

This project demonstrates how machine learning can be used to predict customer coupon acceptance using demographic, travel, weather, and coupon-related information.

Data preprocessing, class balancing, feature selection, feature scaling, and multiple classification algorithms are combined to build and compare predictive models.
