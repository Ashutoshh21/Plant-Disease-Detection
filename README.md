# Plant-Disease-Detection
ABSTRACT

Plant diseases are a huge problem for farmers and can seriously impact our food
supply. To prevent devastating crop losses, it's vital to catch these diseases early. We
decided to tackle this challenge using machine learning, building a smart system that
can predict when a plant is getting sick.
We "trained" our system using data on a plant's leaf color, the size of any spots, and
environmental factors like humidity and temperature. It quickly became clear that
leaf spot size and humidity were major red flags. After extensive testing, our model
proved to be highly accurate at identifying various diseases. We even used it on new
plant samples to show it works in real-world conditions, offering farmers a reliable
tool to stay one step ahead of disease and manage their crops more effectively.


METHODOLOGY
1. The methodology adopted for plant disease prediction in this project is divided into
several systematic phases:
1. Dataset Collection and Preparation
• The dataset containing plant attributes such as plant type, leaf colour, leaf spot
size, humidity, and temperature was used.
• Data cleaning and preprocessing steps ensured the dataset had no missing
values and was ready for analysis.
• Categorical variables (Plant Type, Leaf Colour, and Disease Status) were
encoded using LabelEncoder to convert them into numeric form.
plant_disease_dataset

2. Exploratory Data Analysis
• Descriptive statistics and correlation analysis were performed to understand
feature distributions and relationships.
• Visualisation techniques such as count plots, box plots, and heatmaps were
applied to study the effect of features on disease status.
• Class balance analysis highlighted potential imbalance in disease categories.

3. Feature Engineering and Selection
• Feature importance was extracted from the Random Forest model to identify
significant predictors of disease.
• Additional statistical techniques such as SelectKBest with ANOVA F-test were
used to rank features.
• Outlier detection through box plots provided insights into unusual data points
across plant types.

4. Model Training and Validation
• The dataset was split into training and testing sets using an 80:20 ratio.
• A Random Forest Classifier with 100 decision trees was trained on the
feature set.
• Cross-validation was applied to evaluate model robustness and reduce
overfitting.

6. Model Evaluation
• The model’s performance was assessed using metrics such as accuracy,
precision, recall, F1-score, and confusion matrix.
• Heat maps were generated for better visualisation of true vs predicted
classifications.


RESULT AND DISCUSSION

The Random Forest Classifier was trained on the plant disease dataset using features
such as plant type, leaf colour, leaf spot size, humidity, and temperature. The
following outcomes were observed:
1. Model Performance
• The classifier achieved a high overall accuracy (as observed in the
classification report).
• Metrics such as precision, recall, and F1-score demonstrated that the model
performs reliably in identifying different disease statuses.
• Cross-validation results confirmed the robustness of the model with consistent
accuracy across folds.

2. Confusion Matrix Analysis
• The confusion matrix and its heatmap highlighted that the majority of
predictions were correctly classified.
• However, certain misclassifications occurred among disease categories with
fewer samples, indicating the influence of class imbalance.

3. Feature Importance
• Feature importance analysis revealed that Leaf Spot Size and Humidity were
the most significant predictors of disease status.
• Plant type and leaf colour also contributed, but their influence was
comparatively lower.
• Temperature showed moderate importance, suggesting that environmental
factors affect disease progression.

4. Exploratory Insights
• Box plots and distribution plots showed clear distinctions in leaf spot size
between healthy and diseased samples.
• High humidity levels were associated with severe disease presence, supporting
known biological patterns of fungal and bacterial growth.

5. Practical Implications
• The trained model can be applied to new plant samples to predict disease status
effectively, as demonstrated by test predictions on unseen data.
• The ability to save and reload the model and encoders ensures reusability and
practical deployment.

# Plant Disease Detection using Machine Learning

## Overview
This project predicts plant disease status using structured plant features such as leaf color, humidity, temperature, and leaf spot size.

Instead of using image-based methods, the model uses **tabular agricultural data** to classify whether a plant is diseased or healthy. This approach demonstrates how machine learning can detect patterns in plant characteristics and assist in early disease diagnosis.

---

## Dataset

The dataset consists of plant observations stored in CSV files.

Each row represents a plant instance with features describing plant characteristics and environmental conditions.

### Example Features

| Feature | Description |
|------|------|
| Plant_Type | Type of plant |
| Leaf_Color | Color of plant leaves |
| Leaf_Spot_Size | Size of spots present on leaves |
| Humidity | Environmental humidity |
| Temperature | Environmental temperature |
| Disease_Status | Target label indicating disease presence |

Two datasets were combined to create the final training dataset.

---

## Machine Learning Pipeline

### 1. Data Loading
Two CSV datasets are loaded and merged using pandas.

### 2. Exploratory Data Analysis (EDA)
Visualization techniques are used to understand the dataset:

- Plant type distribution
- Disease status distribution
- Boxplots for feature comparison
- Correlation analysis for numeric features

Libraries used:
- Matplotlib
- Seaborn

---

### 3. Data Preprocessing

Categorical features are encoded using **LabelEncoder**:

- Plant_Type
- Leaf_Color
- Disease_Status

---

### 4. Train-Test Split

The dataset is split into training and testing sets using:


train_test_split(test_size=0.2, stratify=y)


This ensures balanced representation of disease classes.

---

### 5. Model Training

A **Random Forest Classifier** is used for training.

Reasons for choosing Random Forest:

- Works well for tabular datasets
- Handles nonlinear relationships
- Provides feature importance insights

---

### 6. Model Evaluation

Model performance is evaluated using:

- **Classification Report**
- **Confusion Matrix**
- **Feature Importance Visualization**

Metrics include:

- Precision
- Recall
- F1-score


confusion Matrix: ![alt text](image-1.png)
---

### 7. Feature Importance

Random Forest provides feature importance scores that show which plant characteristics contribute most to disease prediction.

---

### 8. Model Saving

The trained model and encoders are saved using **joblib**:


plant_disease_model.pkl
plant_encoder.pkl
color_encoder.pkl
status_encoder.pkl


This allows the model to be reused without retraining.

---

## Project Structure


Plant-Disease-Detection
│
├── dataset/
│ plant_disease.csv
│
├── notebook/
│ plant_disease_detection.ipynb
│
├── README.md
└── requirements.txt


---

## How to Run

Install dependencies:


pip install -r requirements.txt


Open the notebook:


notebook/plant_disease_detection.ipynb


Run all cells to train and evaluate the model.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib

---

## Future Improvements

Possible improvements include:

- Adding more plant features for better prediction
- Hyperparameter tuning
- Deploying the model as a web or mobile application
- Integrating image-based detection with structured data

---

## Author

Ashutosh Dubey  
B.Tech: 3rd-Information Technology

