# Titanic Survival Prediction Model

## Basic Information
- **Group Members**: 
  - Jiwon (jiwon78@gwmail.gwu.edu)
  - Mehak (mehakpreet.kaur@gwmail.gwu.edu)
  - Owen (owandalowski@gwmail.gwu.edu)
  - Julia (jmillietsciorra@gwmail.gwu.edu)
- **Date**: 2024-12-02
- **Model Version**: 0.1
- **License**: MIT License
- **Model Implementation Code**: [Titanic_LogisticRegression](https://github.com/jiwonyun780/titanic-machine-learning-disaster/blob/main/Titanic_Project.ipynb)

### Intended Use
- **Primary Intended Uses**: Educational example for predicting Titanic survival outcomes using machine learning.
- **Primary Intended Users**: GWU students learning machine learning concepts.
- **Out-of-Scope Use Cases**: Any application beyond education or research purposes.

## Training Data
- **Source**: [Kaggle Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)
- **Split Method**:
  - 80% for training
  - 20% for validation
- **Number of Rows**:
  - Training: 713 rows
  - Validation: 178 rows

- **Data dictionary**:

| Name           | Modeling Role           | Measurement Level | Description                                                                                   |
|----------------|-------------------------|-------------------|-----------------------------------------------------------------------------------------------|
| ID             | ID                      | int               | unique row identifier                                                                         |
| LIMIT_BAL      | input                   | float             | amount of previously awarded credit                                                          |
| SEX            | demographic information | int               | 1 = male; 2 = female                                                                         |
| RACE           | demographic information | int               | 1 = hispanic; 2 = black; 3 = white; 4 = asian                                                |
| EDUCATION      | demographic information | int               | 1 = graduate school; 2 = university; 3 = high school; 4 = others                             |
| MARRIAGE       | demographic information | int               | 1 = married; 2 = single; 3 = others                                                          |
| AGE            | demographic information | int               | age in years                                                                                 |
| PAY_0, PAY_2 - PAY_6 | inputs             | int               | history of past payment; PAY_0 = the repayment status in September, 2005; PAY_2 = the repayment status in August, 2005; ...; PAY_6 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; ...; 8 = payment delay for eight months; 9 = payment delay for nine months and above |
| BILL_AMT1 - BILL_AMT6 | inputs           | float             | amount of bill statement; BILL_AMT1 = amount of bill statement in September, 2005; BILL_AMT2 = amount of bill statement in August, 2005; ...; BILL_AMT6 = amount of bill statement in April, 2005 |
| PAY_AMT1 - PAY_AMT6 | inputs              | float             | amount of previous payment; PAY_AMT1 = amount paid in September, 2005; PAY_AMT2 = amount paid in August, 2005; ...; PAY_AMT6 = amount paid in April, 2005 |
| DELINQ_NEXT    | target                  | int               | whether a customer's next payment is delinquent (late), 1 = late; 0 = on-time                |


### Test Data
- **Source of test data**: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- **Number of Rows**:
- **Differences in columns between training and test data**: 

### Model Details
- **Input Columns**: 
- **Target Column**: 
- **Model Type**:
- **Software Used**: 
- **Version**: 
- **Hyperparameters**: 

### Quantitative analysis
- **Evaluation Metrics**:
  - **Accuracy**: 
  - **ROC AUC**:
 ### Performance Metrics Table
| Data Split   | Accuracy | ROC AUC |
|--------------|----------|---------|
| Validation   | 81.01%   | 88.24%  |

![ROC Curve](path-to-roc-curve.png)
![Feature Importance](path-to-feature-importance.png)

### Ethical Considerations
- **Potential Negative Impacts**:
  - 
- **Potential Uncertainties**:
  -

