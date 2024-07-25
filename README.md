# Predicting High Traffic Recipes

## Project Overview
This project aims to predict which recipes will lead to high traffic on our website. We analyze various features of the recipes and apply different machine learning models to achieve accurate predictions. The primary goal is to correctly predict high traffic recipes 80% of the time, using the best performing model based on F1 score and AUC.

## Dataset
The dataset contains various features of recipes, including:
- **Category**: Type of recipe (e.g., Beverages, Breakfast, Chicken, etc.)
- **Servings**: Number of servings for the recipe
- **Calories**: Caloric content
- **Carbohydrate**: Carbohydrate content
- **Protein**: Protein content
- **Sugar**: Sugar content
- **Traffic**: High or low traffic indicator

## Data Cleaning and Preprocessing
1. **Missing Values**: Minimized missing values in the dataset.
2. **Standardizing Categories**: Combined non-standard categories with appropriate existing categories.
3. **Data Transformation**: Converted categorical data to appropriate formats and handled numerical data inconsistencies.

## Exploratory Data Analysis (EDA)
Performed EDA to understand the data distribution and identify patterns, including:
- Analyzing the count of servings by traffic
- Analyzing recipe categories by traffic

## Feature Importance
Used Logistic Regression to determine the importance of each feature in predicting high traffic. The following features were significant:
- Category_Beverages
- Category_Vegetable
- Category_Potato
- Category_Pork
- Category_One Dish Meal
- Servings
- Protein
- Category_Lunch/Snacks
- Category_Meat
- Sugar
- Carbohydrate
- Calories
- Category_Dessert
- Category_Chicken
- Category_Breakfast

## Models Used
Four models were evaluated to predict high traffic recipes:
1. **Logistic Regression**
2. **K-Nearest Neighbors (KNN)**
3. **Random Forest**
4. **Decision Tree**

## Model Evaluation
The models were evaluated using the following metrics:
- Precision
- Recall
- F1 Score
- Accuracy
- Area Under the Curve (AUC)

| Model        | Precision | Recall | F1 Score | Accuracy | AUC   |
|--------------|-----------|--------|----------|----------|-------|
| LogisticReg  | 0.81      | 0.82   | 0.81     | 0.78     | 0.85  |
| Knn          | 0.82      | 0.65   | 0.73     | 0.71     | 0.80  |
| RandomForest | 0.72      | 0.86   | 0.79     | 0.72     | 0.84  |
| DecisionTree | 0.81      | 0.82   | 0.82     | 0.78     | 0.79  |

## Best Model Selection
The best model was selected based on achieving 80% or higher in both F1 score and AUC. The Logistic Regression model was identified as the best performer.

## Recommendations
1. **Minimize Missing Values**: Ensure the data has minimal missing values for better model performance.
2. **Feature Engineering**: Record new features like the number of times recipes are ordered and the time of the year to capture seasonality effects.
