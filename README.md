## Project Description

This project aims to estimate job satisfaction scores for different jobs using machine learning models. The code provided in the Jupyter Notebook performs the following steps:

1. **Data Preprocessing**
   - Reads the training and test data from Excel files (`train.xlsx` and `test.xlsx`).
   - Saves the training and test data as CSV files (`train.csv` and `test.csv`) in Google Drive.
   - Performs data cleaning and feature engineering:
     - Drops columns with unique label count, less than 1 unique label, or more than 1000 unique labels.
     - Drops columns with more than 60% empty rows (NaN values) and replaces remaining NaN values with the mode of the columns.
     - Maps ordinal categorical attributes to numerical values.
     - Replaces NaN values with the mode for both the training and test data.
     - Creates separate columns from attributes consisting of lists.
     - Performs one-hot encoding of categorical features.
     - Scales the features using Min-Max scaling.

2. **Model Training and Evaluation**
   - Trains and evaluates different machine learning models:
     - Gradient Boosting Regressor: Performs hyperparameter tuning using grid search and cross-validation.
     - Random Forest Regression: Performs hyperparameter tuning using random search and cross-validation.
     - KNeighbors Regressor: Performs hyperparameter tuning using grid search and cross-validation.
     - Support Vector Regressor: Performs hyperparameter tuning using grid search and cross-validation.
   - Selects the best performing model based on cross-validation results.

3. **Prediction and Evaluation**
   - Generates predictions for the test data using the best model.
   - Evaluates the performance of the best model using root mean square error (RMSE) on the training data and cross-validation scores.
   - Saves the predictions as a CSV file (`submission.csv`) in Google Drive.

## Instructions

To run this project, please follow these steps:

1. **Prepare the Data**
   - Ensure you have the training and test data in Excel format (`train.xlsx` and `test.xlsx`).
   - Update the file paths in the code to match the location of your data files.

2. **Set up the Environment**
   - Make sure you have Jupyter Notebook installed.
   - Install the necessary Python packages: pandas, scikit-learn, matplotlib, and GridSearchCV.

3. **Open the Jupyter Notebook**
   - Launch Jupyter Notebook.
   - Open the provided Jupyter Notebook file (`job_satisfaction_prediction.ipynb`).

4. **Run the Code Cells**
   - Run each code cell in the notebook sequentially.
   - Review the output and any error messages to ensure the code runs without issues.

5. **Check the Results**
   - Examine the RMSE values and cross-validation scores to assess the performance of the different models.
   - Retrieve the predictions generated by the best model from the `submission.csv` file.

## Project Dependencies

The following dependencies are required to run this project:

- Python 3.x
- Jupyter Notebook
- pandas
- scikit-learn
- matplotlib
- GridSearchCV

Ensure that you have the necessary packages installed in your Python environment before running the code.

## Additional Resources

For more information on the concepts and techniques used in this project, you may refer to the following resources:

- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [GridSearchCV Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)

Feel free to explore and modify the code to suit your specific needs and datasets. Enjoy predicting job satisfaction scores using machine learning!