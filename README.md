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
- **Primary Intended Uses**: The model is an example of a classifier used for machine learning educational purposes only.
- **Primary Intended Users**: Students and anyone interested in machine learning education. 
- **Out-of-Scope Use Cases**: Anything that is not for machine learning educational purposes.


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

## Test Data
- **Source**: [Kaggle Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)
- **Number of Rows**: 
  - Test data: 418 rows
- **Differences from Training Data**:
  - The test data does not include the `Survived` column, which is the target variable in the training data.

## Model Details
- **Input Columns**: 
  - Age
  - Fare
  - Sex male
  - Embarked Q
  - Embarked S
- **Target Column**: 
  - Survived
- **Model Type**: 
  - Logistic Regression
- **Software Used**: 
  - Google Colab / Python
- **Version**: 
  - Python 3
- **Hyperparameters**: 
  - **Max_iter**: 1000  
    Ensures sufficient iterations for convergence of the optimization algorithm.
  - **Random_state**: 42  
    Ensures reproducibility by fixing the randomness in processes.

## Quantitative Analysis

### **Evaluation Metrics**
- **ROC AUC**: The Area Under the Receiver Operating Characteristic Curve measures the model's ability to distinguish between classes.

### **Performance Metrics Table**

| Train Accuary  | Validation Accuracy | Test Accuracy  |
|--------------|--------------|----------|
|    0.80056 | 0.81006      | 0.76315     |

| Data Split   | ROC AUC  | 
|--------------|----------|
| Training     | 85.0     |
| Validation   | 88.0     |

---

### **Visualization**
Below is the ROC Curve for the Logistic Regression Model:

![ROC Curve](images/ROC_curve.png)



## Ethical Considerations

### Potential Negative Impacts
- **Math or Software Problems**:
  - Bias in training data (e.g., imbalanced classes) can lead to poor generalization.
  - Missing or imputed values might introduce inaccuracies in predictions.
- **Real-World Risks**:
  - Misclassification could lead to incorrect decisions in critical scenarios.
  - Discrimination against underrepresented groups in the dataset.

### Potential Uncertainties
- **Math or Software Problems**:
  - Uncertainty in the model’s performance on unseen data, especially given class imbalance.
  - Overfitting to training data due to dataset-specific patterns.
- **Real-World Risks**:
  - The model might not generalize well across different populations or settings.
  - Ethical implications may arise when predictions affect human lives or rights.

### Unexpected Results
- The test set containing only one class highlighted the need for balanced datasets.
- This unexpected outcome underscores the importance of careful dataset preparation before training and evaluation.


