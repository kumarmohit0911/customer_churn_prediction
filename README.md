
# Customer Churn Prediction

## Overview
This project aims to predict customer churn (whether a customer will leave or stay) using machine learning techniques. The dataset contains customer information such as demographics, account details, and transaction history.

## Dataset
The dataset used for this project is **Churn_Modelling.csv**, which includes the following features:
- **RowNumber, CustomerId, Surname** (Dropped as they are irrelevant for prediction)
- **CreditScore**: Customer's credit score
- **Geography**: Customer's location (converted to numerical values using one-hot encoding)
- **Gender**: Male or Female (encoded as 0 and 1)
- **Age**: Customer's age
- **Tenure**: Number of years the customer has been with the bank
- **Balance**: Account balance
- **NumOfProducts**: Number of products held by the customer
- **HasCrCard**: Whether the customer has a credit card (1: Yes, 0: No)
- **IsActiveMember**: Whether the customer is an active member (1: Yes, 0: No)
- **EstimatedSalary**: Customer's estimated salary
- **Exited**: Target variable (1: Churned, 0: Stayed)

## Data Processing
- Removed irrelevant columns (`RowNumber`, `CustomerId`, `Surname`)
- Converted categorical variables (`Geography`, `Gender`) into numerical format using `pd.get_dummies()`
- Replaced boolean values (`True` -> `1`, `False` -> `0`)
- Scaled numerical features using `StandardScaler`

## Model Training
A deep learning model was built using TensorFlow and Keras:
1. **Data Splitting**: The dataset was split into training and testing sets (80%-20%)
2. **Feature Scaling**: Standardized features using `StandardScaler`
3. **Neural Network Architecture**:
   - Input Layer
   - Two Hidden Layers with ReLU activation
   - Output Layer with Sigmoid activation
   - Optimizer: Adam
   - Loss Function: Binary Crossentropy

## Performance Evaluation
The model's performance was evaluated using:
- Accuracy
- Confusion Matrix
- ROC-AUC Score

## Installation & Usage
To run the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/customer-churn-prediction.git
   cd customer-churn-prediction
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:
   ```bash
   jupyter notebook customer_churn_pred.ipynb
   ```

## Results
The model was able to achieve a reasonable accuracy in predicting customer churn. Future improvements may include hyperparameter tuning and trying other ML algorithms like Random Forest and XGBoost.

## Author
[Kumar Mohit](https://www.linkedin.com/in/kumar-mohit-20324827b/)

## License
This project is open-source and available under the MIT License.

