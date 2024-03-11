# Text Classification using Support Vector Machine (SVM)

This repository contains code for text classification using Support Vector Machine (SVM) with TF-IDF and Bag of Words (BoW) approaches. The code demonstrates how to preprocess textual data, vectorize it using TF-IDF and BoW, train SVM models, and evaluate their performance using various evaluation metrics.

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
-   SVM classifier with a linear kernel is trained on the TF-IDF transformed training data and evaluated on the TF-IDF transformed testing data. Similarly, SVM classifier with a linear kernel is trained on the BoW transformed training data and evaluated on the BoW transformed testing data.
-   Evaluation metrics such as accuracy, precision, recall, F1-score, confusion matrix, and classification report are computed for both TF-IDF and BoW approaches.

## Results Analysis

### TF-IDF Approach

-   Accuracy: 83.79%
-   Precision: 83.30%
-   Recall: 83.79%
-   F1 Score: 83.39%

The confusion matrix for TF-IDF approach shows:

-   406 correct predictions for Dessert
-   200 correct predictions for Entrée, but 131 misclassified as Plat principal
-   557 correct predictions for Plat principal

### Bag of Words (BoW) Approach

-   Accuracy: 82.64%
-   Precision: 82.46%
-   Recall: 82.64%
-   F1 Score: 82.53%

The confusion matrix for BoW approach shows:

-   402 correct predictions for Dessert
-   211 correct predictions for Entrée, but 122 misclassified as Plat principal
-   534 correct predictions for Plat principal

Overall, the TF-IDF approach shows slightly better performance compared to the BoW approach, with a slightly higher accuracy and F1 score.

## Usage

1. Install the required dependencies using `pip install -r requirements.txt`.
2. Ensure that `train.csv` and `test.csv` files are in the correct format and directory.
3. Run the `taln.ipynb` notebook or execute the code in your preferred environment.
