# Medicine Usefulness Prediction

## Project Overview

This project aims to predict the usefulness of medicines based on their reviews and various features. The usefulness score helps in understanding and predicting the market potential of new medicines. The project involves data preprocessing, feature engineering, model training, and optimization to achieve accurate predictions while maintaining efficient memory usage.

## Data Description

### Files
- `train.csv`: Training data
- `test.csv`: Test data

### Column Descriptions
1. **medicine_no**: Represents the medicine number
2. **disease type**: Represents the type of disease for which the medicine is used
3. **medicine review**: Represents the review of the medicine
4. **rtuarkiet watche**: Represents the market value of medicine based on its sale and usage by patients
5. **launch date**: Represents the time when the medicine was launched
6. **score**: Represents the score that determines how useful the medicine can be in the market

## Project Structure
```
.
├──dataset\
    |──train.csv
    ├──test.csv
├── submission.csv
├── Medicine_Usefulness_Prediction.ipynb
└── README.md
```

## Requirements

- Python 3.6+
- pandas
- numpy
- scikit-learn

Install the required packages using:
```bash
pip install pandas numpy scikit-learn
```

## Steps to Run the Project

1. **Data Preprocessing**:
    - Handle missing values by filling them with empty strings.
    - Encode categorical features using Label Encoding.
    - Convert date features to datetime objects and extract year, month, and day as separate features.
    - Downcast numerical columns to optimize memory usage.

2. **Feature Extraction**:
    - Use TF-IDF Vectorizer to convert textual reviews into numerical features.
    - Limit the number of TF-IDF features to 500 to save memory.
    - Use sparse matrices for efficient memory management.

3. **Model Training and Evaluation**:
    - Split the training data into training and validation sets.
    - Train a RandomForestRegressor model.
    - Evaluate the model using Root Mean Square Error (RMSE).

4. **Prediction and Submission**:
    - Predict usefulness scores for the test data.
    - Save the predictions in the `submission.csv` file.


## Conclusion

This project demonstrates the use of machine learning to predict the usefulness of medicines based on various features, achieving efficient memory usage and accurate predictions. It showcases the importance of data preprocessing, feature extraction, and model optimization in building effective predictive models.

For more details, feel free to check out the code and contribute to the project.
