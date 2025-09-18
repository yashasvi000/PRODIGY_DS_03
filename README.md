# PRODIGY_DS_03
Task 3 – Decision Tree Classifier on Bank Marketing Dataset
📌 Task Number & Title

Task 3: Build a Decision Tree Classifier to predict whether a customer will purchase a product or service based on their demographic and behavioral data. Dataset used: Bank Marketing dataset (UCI ML Repository / Prodigy GitHub).

⸻

📌 Short Description

The goal of this task was to create a machine learning model using a Decision Tree classifier to predict whether a bank client will subscribe to a term deposit (y = yes/no).
The dataset includes client demographic data (age, job, marital status, education), call-related features (contact, campaign, previous), and socio-economic indicators.

⸻

📌 Approach / Steps Followed
	1.	Load the dataset
	•	Used Pandas to load bank-additional-full.csv (semicolon separated).
	•	Inspected structure, target distribution, and missing values.
	2.	Data Cleaning
	•	Replaced "unknown" values with NaN.
	•	Filled categorical NaNs with mode, numerical with median.
	•	Dropped duration column to avoid data leakage (only known after call).
	3.	Feature Engineering & Encoding
	•	One-hot encoded categorical variables (job, marital, education, etc.).
	•	Converted target y to binary (yes = 1, no = 0).
	4.	Train-Test Split
	•	Split dataset into 80% training and 20% testing sets.
	•	Used stratification to maintain class imbalance.
	5.	Model Training
	•	Trained a DecisionTreeClassifier with:
	•	max_depth=6 (to avoid overfitting)
	•	class_weight='balanced' (to handle class imbalance).
	6.	Evaluation
	•	Computed metrics: Accuracy, Precision, Recall, F1-score.
	•	Generated Confusion Matrix.
	•	Plotted Feature Importances.
	•	Visualized decision tree structure (limited depth).
	7.	Save Outputs
	•	Exported predictions (bank_test_predictions.csv).
	•	Saved trained model as decision_tree_bank.pkl using Joblib.
 📌 How to Run the Project/Code
	1.	Upload dataset (bank-additional-full.csv) in Google Colab.
	2.	Install dependencies (if needed):

                pip install pandas numpy matplotlib seaborn scikit-learn joblib
                
  3.	Run the Jupyter/Colab notebook step by step (loading → cleaning → encoding → training → evaluation).
	4.	Saved outputs:
	•	Model → decision_tree_bank.pkl
	•	Predictions → bank_test_predictions.csv
