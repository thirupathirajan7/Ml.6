# Task 6: Phishing URL Detection Using Machine Learning

## Project Overview
This project uses a Decision Tree Classifier to classify URLs as **phishing** or **legitimate**. The model is trained using features from the PhiUSIIL Phishing URL Dataset.

## Objectives
- Explore and understand the phishing URL dataset.
- Prepare the data for machine learning.
- Train a Decision Tree classification model.
- Evaluate the model using classification metrics and a confusion matrix.

## Dataset
- **Dataset file:** `PhiUSIIL_Phishing_URL_Dataset.csv`
- **Records:** 13,394 in the initial dataset; 13,393 after removing rows with missing target labels.
- **Columns:** 56 in the initial dataset.
- **Features used:** 50 numeric features, excluding the target `label` column.
- **Target mapping in this notebook:** `label = 0` is mapped to phishing (`1`), and `label = 1` is mapped to legitimate (`0`).

Place the CSV file in the same directory as the notebook, or update the file path in the code.

## Technologies and Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Workflow
1. **Load the dataset** and inspect its shape, columns, missing values, and label counts.
2. **Preprocess the data** by removing rows with missing target labels, selecting numeric features, replacing infinite values with missing values, and filling missing feature values with column medians.
3. **Split the data** into 80% training data and 20% testing data, using stratification to preserve the class proportions.
4. **Train the model** with a Decision Tree Classifier (`max_depth=5`, `class_weight="balanced"`, `random_state=42`).
5. **Visualize the decision tree** to view the model's decision rules.
6. **Make predictions** on the test data.
7. **Evaluate the model** using a confusion matrix, accuracy, precision, recall, F1-score, and specificity.

## Results
The notebook's current output reports the following metrics:

| Metric | Result |
|---|---:|
| Accuracy | 1.0000 (100%) |
| Precision | 1.0000 (100%) |
| Recall | 1.0000 (100%) |
| F1-score | 1.0000 (100%) |
| Specificity | 1.0000 (100%) |

The confusion matrix shown in the notebook is:

```text
[[1615    0]
 [   0 1064]]
```

These are the results recorded in the current notebook run. Perfect scores are unusual for real-world phishing detection, so further validation is recommended before relying on the model. Check for data leakage, duplicate or highly related records across the train/test split, and whether any features indirectly reveal the target label. Consider evaluating on a separate, unseen dataset.

## How to Run
1. Install Python and Jupyter Notebook.
2. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib scikit-learn notebook
   ```

3. Download or place `PhiUSIIL_Phishing_URL_Dataset.csv` in the notebook's directory.
4. Open the notebook:

   ```bash
   jupyter notebook Task6_ML.ipynb
   ```

5. Run the cells from top to bottom.

## Project Files
```text
.
├── Task6_ML.ipynb
├── PhiUSIIL_Phishing_URL_Dataset.csv
└── README.md
```

## Conclusion
This project demonstrates a basic machine learning workflow for phishing URL classification, from data preparation and model training to visualization and evaluation. Additional testing on independent data is needed to understand how well the model performs on URLs it has never seen.

## Disclaimer
This project is for educational purposes. Its predictions should not be treated as a guarantee that a URL is safe or malicious.
