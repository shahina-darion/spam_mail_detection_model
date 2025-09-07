##  Spam Mail Detection using Logistic Regression

### Step 1: Import Libraries
Use pandas, numpy, and sklearn for the ML pipeline.

### Step 2: Load Dataset
Load **spam.csv** or **SMSSpamCollection**.  
Columns: `label` (ham/spam), `message` (text).

### Step 3: Encode Labels
Map labels → ham = 0, spam = 1.  
Drop empty/invalid rows to avoid NaN issues.

### Step 4: Text Preprocessing
Convert messages into features using **TF-IDF vectorizer**  
(max_features=3000, remove stopwords).

### Step 5: Split Dataset
Train = 80%, Test = 20%.  
Use `stratify=y` to balance spam/ham ratio.

### Step 6: Train Model
Train **Logistic Regression** (`solver='liblinear'`).

### Step 7: Predictions
Predict spam/ham on the test set.

### Step 8: Evaluation
Check **accuracy** and **classification report**  
(precision, recall, f1-score).

### Step 9: Custom Testing
Use `predict_message()` to classify new SMS as **Spam** or **Ham**.
