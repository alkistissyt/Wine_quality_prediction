### Wine Quality Prediction using Machine Learning

## Introduction
This project aims to predict the quality of wine based on its chemical properties. We used the UCI Wine Quality dataset from Kaggle, which includes various chemical measurements of wine samples and their quality ratings. The primary objective is to build a model that can accurately predict wine quality and evaluate its performance using various metrics.

## Model Training
Classification is a type of supervised learning where the goal is to assign labels to instances based on their features. In our case, the wine quality ratings are categorical labels that we want to predict. The quality of wine was originally rated on a scale from 3 to 8, but for better interpretability and to simplify the problem, we categorized these ratings into three labels: "low", "mid", and "high". This transforms our problem into a classification task where the goal is to assign one of these three labels to each wine sample.


#### Database Description
- **Dataset**: 1,143 red wine samples with 12 chemical features each.
- **Target Variable**: Wine quality rating (3 to 8).
- **Features**: Fixed acidity, Volatile acidity, Citric acid, Residual sugar, Chlorides, Free sulfur dioxide, Total sulfur dioxide, Density, pH, Sulphates, Alcohol.

#### Data Preprocessing
1. **Feature Selection**: Removed non-informative columns (e.g., id).
2. **Handling Missing Values**: Verified no missing values in the dataset.
3. **Outlier Removal**: Identified and removed outliers in features like free sulfur dioxide and total sulfur dioxide.
4. **Label Mapping**: Categorized quality ratings into three labels: low (3, 4), mid (5, 6), and high (7, 8).

#### Exploratory Data Analysis (EDA)
- **Boxplots**: Show trends and outliers in features related to wine quality.
- **Histograms**: Highlight the distribution of each feature.
- **Pairplot and Heatmap**: Indicate positive correlations (e.g., alcohol and quality) and negative correlations (e.g., volatile acidity and quality).

#### Model Training
Classification is a type of supervised learning where the goal is to assign labels to instances based on their features. In our case, the wine quality ratings are categorical labels that we want to predict. The quality of wine was originally rated on a scale from 3 to 8, but for better interpretability and to simplify the problem, we categorized these ratings into three labels: "low", "mid", and "high". This transforms our problem into a classification task where the goal is to assign one of these three labels to each wine sample.
- **Model Used**: Random Forest classifier with 100 decision trees.
- **Data Splitting**: Split dataset into training (80%) and testing (20%) sets.
- **Training Process**: Trained the Random Forest model on the training set and evaluated it on the test set.

#### Model Evaluation
- **Accuracy**: Achieved an accuracy of 0.91.
- **Confusion Matrix**: Highlighted issues with predicting 'low' quality wines.
- **Class Imbalance**: Noted imbalance in the dataset, affecting model performance. Considered adjusting class weights to address this.

#### Conclusion
The Random Forest model performed well in predicting wine quality, especially for 'mid' quality wines. Future work includes addressing class imbalance and further model tuning to improve predictions for 'low' and 'high' quality wines.

#### References
- Kaggle notebooks and other resources used are listed in the project documentation.
