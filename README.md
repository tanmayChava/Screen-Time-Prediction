# Screen-Time-Prediction
📊 Predicting Health Impacts of Screen Time in Indian Kids
This project analyzes the screen time habits of Indian children and uses machine learning to predict whether their screen usage exceeds recommended limits and its potential health impacts.

📁 Dataset
The dataset includes the following features:

Age – Child's age in years

Gender – Male/Female

Avg_Daily_Screen_Time_hr – Average daily screen time

Primary_Device – Device used most frequently (Mobile, Tablet, etc.)

Exceeded_Recommended_Limit – Whether screen time exceeds WHO guidelines

Educational_to_Recreational_Ratio – Time spent on educational vs recreational content

Health_Impacts – Reported health impacts (e.g., Poor Sleep, Eye Strain)

Urban_or_Rural – Location type

🎯 Objectives
Classification Task 1: Predict whether a child's screen time exceeds the recommended limit.

Classification Task 2: Predict the type of health impacts based on screen usage patterns (multiclass).

🛠️ Preprocessing
Dropped Avg_Daily_Screen_Time_hr to prevent target leakage.

One-hot encoded categorical features: Gender, Primary_Device, Urban_or_Rural.

Handled class imbalance using SMOTE (Synthetic Minority Oversampling Technique).

Used label encoding for multiclass target Health_Impacts.

🤖 Models Used
For Exceeded_Recommended_Limit (Binary Classification):
Random Forest Classifier

XGBoost Classifier

Used scale_pos_weight to address imbalance

Performed threshold tuning to optimize F1 for the minority (False) class

Final threshold selected: 0.54

For Health_Impacts (Multiclass Classification):
(Optional based on implementation)

Models: Random Forest / XGBoost / Logistic Regression

Evaluation via macro-averaged F1-score due to class imbalance

📈 Evaluation Metrics
Accuracy

Confusion Matrix

Precision, Recall, F1-score

Special focus on recall and F1 for minority class in imbalanced problems

🔍 Results
Exceeded Recommended Limit (after threshold tuning):

Accuracy: ~79%

F1 (False class): ~0.24 (improved from ~0.05)

Recall (False class): 23%

Balanced performance using threshold of 0.54

📚 Conclusion
Threshold tuning and resampling strategies (SMOTE, scale_pos_weight) significantly improved performance for minority classes. The model is better at identifying children not exceeding screen time, which is crucial for early prevention.

