# Text Classification using RandomForestClassifier

This repository contains code for text classification using RandomForestClassifier with TF-IDF and Bag of Words (BoW) approaches. The code demonstrates how to preprocess textual data, vectorize it using TF-IDF and BoW, train RandomForestClassifier models, and evaluate their performance.

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
-   Performance metrics such as accuracy, classification report, and confusion matrix are computed for both TF-IDF and BoW approaches.

## Usage

1. Install the required dependencies using `pip install -r requirements.txt`.
2. Ensure that `train.csv` and `test.csv` files are in the correct format and directory.
3. Run the `taln.ipynb` notebook or execute the code in your preferred environment.
