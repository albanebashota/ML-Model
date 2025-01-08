# Used/New Cars Deal Categorization/ ML_Model
This repository contains an end-to-end machine learning pipeline designed to classify used cars into various deal categories such as 'Fair Deal', 'Great Deal', 'Good Deal', 'Overpriced', 'Uncertain', 'No Rating'. The pipeline starts by using K-Means clustering to group cars based on their attributes, followed by training a Decision Tree Classifier to predict the deal categories based on historical data. The project is focused on automating the categorization process and providing valuable insights into the pricing of used cars.
# Project Overview
The goal of this project is to automatically classify used cars into different deal categories based on features like price, mileage, engine size, year,dos_active and statistical reports calculated from these features. The classification provides insights into whether a car is a good or bad deal for potential buyers. To achieve this, the project leverages both unsupervised learning (K-Means) and supervised learning (Decision Tree Classifier).

# Key Features
- Data Exploration
- Correlation Matrix: Analyzes the relationships between numeric variables in the dataset.
- Clustering: Uses **K-Means** clustering to create initial deal categories based on car attributes.
- Modeling: Applies a **Decision Tree Classifier** to predict deal categories for used cars.
- Model Evaluation: Evaluates the model performance using a confusion matrix and classification report.
# Requirements
To run the project, the following Python libraries used:

pandas

numpy

matplotlib

seaborn

scikit-learn

joblib
# Decision Tree Model

The Decision Tree model performance results, as shown in the classification reports for both the NewCars and UsedCars datasets, provide valuable insights into how the model classifies the deal categories. Here’s a breakdown of the results and an explanation of key metrics:
# Accuracy
NewCars: Accuracy = 96%
UsedCars: Accuracy = 93%

![image](https://github.com/user-attachments/assets/189815e3-427d-4bb1-ad29-117bb200ae43)

![image](https://github.com/user-attachments/assets/692833de-78c0-4876-98be-079ed5271e9c)


Accuracy indicates the overall percentage of correct predictions (both true positives and true negatives) in relation to the total number of predictions. For the NewCars dataset, the model performs slightly better with an accuracy of 96%, compared to 93% for the UsedCars dataset.
# NewCars:
  **Fair Deal:**
Precision: 0.99, Recall: 0.96, F1-Score: 0.97
High precision (0.99) and recall (0.96) indicate that the model does an excellent job classifying 'Fair Deal' cars.
 
   **Good Deal:**
Precision: 0.94, Recall: 0.94, F1-Score: 0.94
A balanced precision and recall of 0.94 means the model classifies 'Good Deal' cars fairly well without overfitting or underfitting.
  
   **Great Deal:**
Precision: 1.00, Recall: 0.00, F1-Score: 0.00
Here, the precision is perfect (1.00), but the recall is 0, which means that the model is predicting 'Great Deal' correctly when it does, but it’s not identifying any of the actual 'Great Deal' cars (high false negative rate).
   
   **No Rating:**
Precision: 0.93, Recall: 0.98, F1-Score: 0.96
The model performs well in identifying 'No Rating' cars with high recall (0.98), but precision is lower, meaning there are some false positives.
   
   **Uncertain:**
Precision: 0.96, Recall: 0.95, F1-Score: 0.96
The 'Uncertain' category is predicted fairly well with high precision and recall.


# UsedCars:
 
  **Fair Deal:**
Precision: 0.94, Recall: 0.88, F1-Score: 0.91
The model performs well for 'Fair Deal' cars, but recall could be improved (indicating some misclassifications).

  **Good Deal:**
Precision: 0.92, Recall: 0.93, F1-Score: 0.92
A well-balanced performance for 'Good Deal', showing the model’s ability to predict this category effectively.
  
  **Great Deal:**
Precision: 0.94, Recall: 0.96, F1-Score: 0.95
'Great Deal' is predicted well, with high precision and recall, showing the model's strong ability to detect this category.
  
  **No Rating:**
Precision: 0.97, Recall: 0.89, F1-Score: 0.93
Excellent precision for 'No Rating' with slight room for improvement in recall.
  
  **Uncertain:**
Precision: 0.98, Recall: 0.68, F1-Score: 0.81
High precision, but low recall for 'Uncertain', indicating that the model sometimes fails to identify uncertain cars, which could lead to misclassifications
