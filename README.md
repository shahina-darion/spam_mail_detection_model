# spam_mail_detection_model
# Spam Mail Detection using Logistic Regression

# Step 1: Import Libraries
# We use pandas & numpy for data handling,
# scikit-learn for train-test split, TF-IDF vectorization, logistic regression, and evaluation.
# Metrics used: accuracy score & classification report.
 
# Step 2: Load Dataset
# Load the SMS Spam Collection dataset.
# - If using Kaggle CSV -> only first 2 columns are required.
# - If using UCI dataset -> it's tab-separated with 2 columns (label, message).

# Step 3: Encode Labels
# - Labels are mapped: 'ham' -> 0, 'spam' -> 1
# - Drop rows with NaN values after mapping (to ensure clean data).

# Step 4: Text Preprocessing
# - Drop empty rows in dataset
# - Reset index after cleaning
# - Convert text messages into numerical features using TF-IDF
#   (stop words removed, max_features=3000 for efficiency)

# Step 5: Split Dataset
# - Split features (X) and labels (y) into train and test sets
# - 80% training, 20% testing
# - stratify=y ensures balanced spam/ham distribution
# - random_state=42 for reproducibility

# Step 6: Train Logistic Regression Model
# - Logistic Regression is trained with liblinear solver
# - max_iter=200 ensures convergence

# Step 7: Predict
# - Model predicts labels for X_test

# Step 8: Evaluate
# - Accuracy score: overall performance of the classifier
# - Classification report: precision, recall, F1-score for spam and ham

# Step 9: Test on New Messages
# - A helper function 'predict_message' transforms any new text
#   into TF-IDF features and uses the trained model to classify.
# - Example predictions shown for spam and ham messages.
