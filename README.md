# Text Classification using RandomForestClassifier

This repository contains code for text classification using RandomForestClassifier with TF-IDF and Bag of Words (BoW) approaches. The code demonstrates how to preprocess textual data, vectorize it using TF-IDF and BoW, train RandomForestClassifier models, and evaluate their performance using various evaluation metrics.

## Files

-   `train.csv`: Contains training data with columns 'titre', 'ingredients', and 'type'.
-   `test.csv`: Contains testing data with columns 'titre', 'ingredients', and 'type'.
-   `taln.ipynb`: Jupyter Notebook containing the code.

## Dependencies

-   pandas
-   scikit-learn

## Code Explanation

-   `train.csv` and `test.csv` are loaded separately using pandas.
-   Text data in 'titre' and 'ingredients' columns are concatenated to form the feature, and 'type' column is considered as the label.
-   The data is split into training and testing sets.
-   Text data is vectorized using TF-IDF and BoW approaches separately for both training and testing sets.
-   RandomForestClassifier is trained on the TF-IDF transformed training data and evaluated on the TF-IDF transformed testing data. Similarly, RandomForestClassifier is trained on the BoW transformed training data and evaluated on the BoW transformed testing data.
-   Evaluation metrics such as accuracy, precision, recall, F1-score, confusion matrix, and classification report are computed for both TF-IDF and BoW approaches.

## Results Analysis

### TF-IDF Approach

-   Accuracy: 79.90%
-   Precision: 79.20%
-   Recall: 79.90%
-   F1 Score: 79.34%

The confusion matrix for TF-IDF approach shows:

-   399 correct predictions for Dessert
-   173 correct predictions for Entrée, but 157 misclassified as Plat principal
-   537 correct predictions for Plat principal

### Bag of Words (BoW) Approach

-   Accuracy: 80.91%
-   Precision: 80.15%
-   Recall: 80.91%
-   F1 Score: 80.16%

The confusion matrix for BoW approach shows:

-   403 correct predictions for Dessert
-   171 correct predictions for Entrée, but 160 misclassified as Plat principal
-   549 correct predictions for Plat principal

Overall, the BoW approach shows slightly better performance compared to the TF-IDF approach, with a slightly higher accuracy and F1 score.

## Usage

1. Install the required dependencies using `pip install -r requirements.txt`.
2. Ensure that `train.csv` and `test.csv` files are in the correct format and directory.
3. Run the `taln.ipynb` notebook or execute the code in your preferred environment.
