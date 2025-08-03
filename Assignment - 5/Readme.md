## Task 2: Spam Detection using MultinomialNB

### Dataset
- **Dataset Used**: SMS Spam Collection Dataset  


### Preprocessing Steps
- Loaded the dataset using pandas.
- Renamed columns to `label` and `message`.
- Encoded labels: `spam` as 1 and `ham` as 0.
- Used **CountVectorizer** to transform text into numerical feature vectors.

### Model Training
- Used `MultinomialNB()` from `sklearn.naive_bayes`.
- Split data into **training** and **testing** sets using `train_test_split`.
- Trained the model on the training set.

### Evaluation Metrics
- **Accuracy**: Achieved using `accuracy_score`.
- **Precision**: Indicates how many of the predicted spams were actually spam.
- **Recall**: Indicates how many of the actual spams were correctly detected.
- **Confusion Matrix**: Displayed using `confusion_matrix`.

### Results
- The model achieved good accuracy and high recall.
- Spam detection was effective with minimal false positives.


## Task 3: GaussianNB with Iris Dataset
- Used the Iris dataset from sklearn.
- Compared **GaussianNB** with **Logistic Regression** and **Decision Tree**.

### Model Accuracies:
- GaussianNB: ~93%
- Logistic Regression: ~96%
- Decision Tree: ~96%

### Key Points:
- GaussianNB is good when data follows a Gaussian distribution.
- Logistic Regression works well with linear boundaries.
- Decision Trees can handle complex patterns but might overfit if not pruned.


## Task 5: Decision Tree on Titanic Dataset
- Used Titanic dataset from Seaborn.
- Preprocessed missing values and encoded 'sex' and 'embarked' columns.
- Trained a Decision Tree (max depth 4).
- Visualized the decision tree using `plot_tree`.
- Evaluated using Accuracy and Confusion Matrix.

### Results
- Accuracy: ~82%
- Confusion Matrix: Shows good balance between predicted survival and non-survival.


## Task 6: Model Tuning
- Tuned `max_depth` to observe how model performance changes.
- Tracked both **training** and **testing** accuracy.
- Observed that increasing depth too much improves training accuracy but may reduce test accuracy — a sign of **overfitting**.

### Findings:
- Best performance often occurs with moderate depth (e.g., 4–6).
- Beyond a certain point, test accuracy drops even as training accuracy increases.
- This highlights the importance of tuning and validation.


## Task 8: Random Forest vs Decision Tree
- Trained both a `DecisionTreeClassifier` and a `RandomForestClassifier` on the Titanic dataset.
- Compared metrics like Accuracy, Precision, and Recall.
- Random Forest generally outperformed the standalone Decision Tree in all metrics.
- Also plotted **feature importances** from the Random Forest.

### Result:

| Model          | Accuracy | Precision | Recall |
|----------------|----------|-----------|--------|
| Decision Tree  | ~0.82    | ~0.74     | ~0.68  |
| Random Forest  | ~0.86    | ~0.80     | ~0.74  |


## Task 9: Boosting with AdaBoost
- Trained `AdaBoostClassifier` with 100 estimators.
- Compared it against `RandomForestClassifier` and `DecisionTreeClassifier`.
- Evaluated using **Accuracy** and **F1-Score**.

### Results
| Model           | Accuracy | F1-Score |
|-----------------|----------|----------|
| Decision Tree   | ~0.82    | ~0.74    |
| Random Forest   | ~0.86    | ~0.78    |
| AdaBoost        | ~0.85    | ~0.77    |

### Notes:
- AdaBoost performed comparably to Random Forest.
- Boosting tends to focus on hard-to-classify cases.
