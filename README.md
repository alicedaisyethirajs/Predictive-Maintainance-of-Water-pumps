# Predictive Maintainance of Water Pumps

Predictive maintenance is a crucial aspect of monitoring and maintaining systems like HVAC pumps. By using sensor data, it is possible to predict failures and schedule maintenance in advance, preventing costly repairs and downtime. This project aims to build a predictive maintenance model for HVAC pumps using machine learning techniques on sensor data to predict the machine's operational status.
The dataset used contains sensor data from HVAC pumps, including readings from various sensors (sensor_00 to sensor_51) and a label indicating whether the machine is operating normally or requires maintenance.


**Dataset used**

Here I used the Puump Sensor Dataset :([https://www.kaggle.com/datasets/nphantawee/pump-sensor-data])


**Data Preprocessing**:

Missing Values: Columns with more than 50% missing values were dropped. Missing values in other columns were filled with the mean of the column.
Label Encoding: The machine_status column was encoded to numeric values using LabelEncoder.
Feature Scaling: All sensor data was standardized using StandardScaler to ensure that the features have a mean of 0 and a standard deviation of 1.
Exploratory Data Analysis (EDA):
Correlation Heatmap: A heatmap was plotted to check the correlations between sensors.
Sensor Distribution: The distribution of values for different sensors was plotted to check for outliers or anomalies.
Anomaly Detection: Z-scores were calculated to identify outliers (values that exceed a z-score threshold of 3 were marked as anomalies).


**Model Development and Training**

We trained five machine learning models to predict the machine_status (whether the machine is running normally or needs maintenance):
Logistic Regression
Random Forest Classifier
Support Vector Machine (SVM)
K-Nearest Neighbors (KNN)
XGBoost Classifier


**Each model was evaluated using:**

Accuracy: The proportion of correct predictions.
Precision: The proportion of true positives among the predicted positives.
Recall: The proportion of true positives among the actual positives.
F1-Score: The harmonic mean of precision and recall.


**Model Evaluation**
After training and evaluating all models, we found the XGBoost model to provide the best accuracy, precision, recall, and F1-score. The detailed evaluation metrics for each model are as follows:
Logistic Regression: Accuracy - 85%, F1-score - 0.86
Random Forest: Accuracy - 89%, F1-score - 0.89
SVM: Accuracy - 87%, F1-score - 0.87
KNN: Accuracy - 84%, F1-score - 0.84
XGBoost: Accuracy - 91%, F1-score - 0.91


**Conclusion**
The model was successful to predict machine status, which can be integrated into real-time monitoring systems for HVAC pumps through FastAPIs. This predictive maintenance approach can help in reducing downtime and maintenance costs.


**Visualizations Obtained**

**Correlation of the numeric data**

![image](https://github.com/user-attachments/assets/222a507e-4bd7-4243-98a2-498bae2c5876)


**Distribution of Sensor values**

![image](https://github.com/user-attachments/assets/5faf33de-7c1e-44a9-ad2e-c498722a1c72)

**Anamoly Flag Distrubution**

![image](https://github.com/user-attachments/assets/bda86b17-2d10-4bd2-8832-f52a7925c884)




