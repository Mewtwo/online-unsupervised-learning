# online-unsupervised-learning

The code examples provided here are based on the online unsupervised learning method we used in this paper:

We were given patients that were either healthy, had COVID-19, or had CAP. Using full chest CT scans, we then predict the patient's class. 
Our method consisted of dividing a test set into quarters, and then recursively obtaining predictions and retraining the slice level models for each quarter.
After each quarter of predictions are made, we add the data along with the predictions to the training and validation datasets. We then retrain our models using the updated data before moving onto the next quarter of test data.

Usage instructions:

Given a test set, and trained models:
Start with the predictions code first.
Input the desired quarter, file locations, and save names.
Then run model retrainer, again setting quarter, file locations, and save names.
Run predictions code again, updating toggles as needed.
Repeat until predictions obtained for all test instances
