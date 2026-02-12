Practice 1: Solving a Classification Problem (Titanic Dataset)
Project Description
This project focuses on the development and comparison of different machine learning models to solve a supervised classification problem. Using the well-known Titanic dataset, the goal is to predict passenger survival (Survived) based on various technical and demographic attributes.

The project covers the entire machine learning pipeline: from Exploratory Data Analysis (EDA) and data preprocessing to model selection using Cross-Validation and hyperparameter optimization.

Authors and Affiliation
Alejandro Flores Hernández – 1709458

Marc Dalmau Guamis – 1710713

Universitat Autònoma de Barcelona (UAB) – Course: Machine Learning – Group 07

Project Structure
train.csv / test.csv: Original Titanic datasets from Kaggle.

P1_Classificacio.ipynb: Jupyter Notebook containing the full implementation (EDA, Preprocessing, and Modeling).

Data Preprocessing
Missing Values (NaNs):

Age: Imputed using the median to maintain distribution stability.

Fare: Imputed with the median (specifically for test set gaps).

Embarked: Imputed with the mode (most frequent value).

Categorical Encoding:

Label Encoding: Applied to Sex and Embarked to transform textual categories into numerical format.

Feature Selection:

Removed PassengerId and non-numeric features like Name and Ticket to focus on variables with higher correlation to the target.

Standardization:

Applied StandardScaler to numerical variables (Age, Fare, SibSp, Parch) to ensure stability across models like Logistic Regression.

Metric Selection
Since the objective is to predict survival (classification), the following metrics were prioritized:

F1-Score: Chosen as the primary metric to balance Precision and Recall, especially important if classes are slightly imbalanced.

ROC Curve & AUC: Used to evaluate the model's ability to distinguish between classes.

Confusion Matrix: To visualize Type I and Type II errors (false positives vs. false negatives).

Model Selection and Training
The project followed a multi-stage training process:

Base Model Evaluation: Initial testing of Logistic Regression, Decision Trees, Random Forest, and Gradient Boosting.

Cross-Validation (K-Fold): 5-fold cross-validation was used within the training set to ensure the robustness of the results and avoid overfitting.

Hyperparameter Optimization:

Manual search and iterative testing for parameters such as max_depth, n_estimators, and learning_rate.

Use of GridSearchCV / RandomizedSearch logic to find the optimal configuration for each algorithm.

Selected Final Model: Gradient Boosting Classifier / Random Forest (Optimized). Results showed high stability with an F1-score and Accuracy reflecting strong predictive power on the validation set.

Final Analysis and Practical Applications
The final model provides a logical interpretation of survival factors (e.g., the high impact of Sex and Pclass on the results).

Practical Applications:

Historical data analysis to understand survival patterns in maritime disasters.

Benchmark for testing new classification algorithms and preprocessing techniques.

Educational framework for understanding the impact of data imputation on model bias.

Technologies and Libraries Used
Python 3.x

Libraries: pandas, numpy, scikit-learn, matplotlib, itertools

Environment: Jupyter Notebook

Execution
Clone the repository: git clone https://github.com/[marcdalg05]/TitanicClassification.git

Install dependencies: pip install pandas numpy scikit-learn matplotlib

Run the analysis: Open P1_Classificacio.ipynb in Jupyter or VS Code and execute all cells.

License
This project is public and can be used under the CC-BY 4.0 license, citing the original authors.