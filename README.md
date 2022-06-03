# Income-Preditiction-ML-AIREP
University project, working on the UCI census income data set to solve a classification task using machine learning.


NOTE: Due to the sheer size of the Jupyter Notebook, it is unable to run on GitHub.
-> Instead Please follow this link for a static viewing of the entire code: https://nbviewer.org/github/Nicolai1205/Income-Preditiction-ML-AIREP/blob/main/Airep_V16.ipynb

## Key highlights
### 1.
The project tried to identify whether a Decision Tree or Random Forest approach would yield better results for a binary classification issues
compared to a logistic regression model.

### 2.
Data was cleaned and approximately 3000 rows were removed due to NaN values.

Exploratory, univarite, bivaraite and multivariate analysis was used to identify patterns in the data as well as to
find out how one should group the variables.
e.g. marital status went from 7 to 2 features -> Either Married(1) or Not Married(2).

### 3. 
Scikit-learn's train_test_split was used with a 75/25 split for the data.

Models were run initially with the entire dataset for all models and through feature_importance and permutation_importants,
relevant features were identiied and kept for subset analysis.

For both the logisitc regression and the Decision Tree, in-sample results proved slightly better than out-of-sample results.

Key features that came up again and again were: Level of Education, Age, Marital Status, Hours Worked per Week and capital gain.

### 4.
At the end, overfitting seemed present and the Random Forest model run with the subset achieved an out-of-sample accuracy of 84.29 %.
One could argue that issues arose from the skewness of the data (more people were below 50.000 USD in income than above. 75% to be exact.)

Ideas for different approaches going forward:
Using ROC, AUC to better measure the the ability of the classifier to distinguish between classes.
Use resampling to create a more balanced dataset through under-sampling.
Use a 80/20 split of the data and potentially make use of the StratifiedShuffleSplit.
