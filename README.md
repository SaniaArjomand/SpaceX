🚀 Falcon 9 First Stage Booster Landing Prediction
Predicting the landing success of the Falcon 9 first stage booster using historical launch data.
Target variable: Class
* 0 = Not landed
* 1 = Landed successfully

📄 Project Overview
SpaceX reduces launch costs by reusing rockets. Predicting successful landings can:
* Help SpaceX optimize launch operations
* Provide insights for cost-effective mission planning
* Demonstrate practical machine learning applications in aerospace
This project uses historical Falcon 9 data to predict first stage booster landing outcomes.

📊 Dataset
The dataset contains 90 launches with 18 features, including:
Column	Description
FlightNumber	Sequential flight number
Date	Launch date
BoosterVersion	Version of the booster
PayloadMass	Mass of the payload (kg)
Orbit	Orbit type
LaunchSite	Launch site
Outcome	Mission outcome
Flights	Number of flights of the booster
GridFins	Whether booster has grid fins
Reused	Whether booster is reused
Legs	Whether booster has landing legs
LandingPad	Landing pad location (may have missing values)
Block	Block version
ReusedCount	Number of times booster has been reused
Serial	Booster serial number
Longitude	Launch site longitude
Latitude	Launch site latitude
Class	Target variable: 0 = not landed, 1 = landed
⚙️ Methodology
1. Data Exploration (EDA)
    * Examined numerical and categorical features
    * Calculated correlations between features and Class
2. Preprocessing (Data Cleaning & Feature Engineering)
    * Removed irrelevant columns (e.g., FlightNumber, Date)
    * One-hot encoded categorical features using get_dummies()
    * Standardized numerical features
3. Modeling Tested multiple algorithms:
    * Logistic Regression
    * Support Vector Machine (SVM)
    * K-Nearest Neighbors (KNN)
    * Decision Tree
4. Evaluation
    * Metrics: Accuracy, Precision, Recall, F1-score
    * Cross-validation for generalization

🧠 Key Findings
* Structural and operational features strongly influence landing success: boosters with landing legs, grid fins, newer block versions, higher reused counts, and later flights tend to land more reliably.
* Simple models like Decision Tree and Support Vector Machine (SVM) achieved reasonable accuracy, showing that even straightforward approaches can capture meaningful patterns in the data.
* Data-driven predictions can help optimize first stage landing strategies, providing actionable insights for cost reduction and operational planning.

📈 Results
Model	Accuracy	Precision	Recall	F1-Score
Logistic Regression	0.85	0.83	0.93	0.88
SVM	0.85	0.80	1.0	0.88
KNN	0.77	0.75	0.93	0.83
Decision Tree	0.88	0.88	0.93	0.90
Decision Tree achieved the best performance among tested models.

📦 Technologies Used
* Python 🐍
* Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* Environment: Jupyter Notebook

🔮 Future Work
* Explore ensemble models (Random Forest, Gradient Boosting) for improved performance
* Try deep learning approaches (Neural Networks)
* Deploy predictions on an interactive web dashboard
