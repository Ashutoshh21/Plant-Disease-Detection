# Plant-Disease-Detection
ABSTRACT
—————————————————————————————————
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
—————————————————————————————————
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


