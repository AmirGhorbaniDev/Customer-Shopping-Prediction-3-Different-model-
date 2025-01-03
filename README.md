# Customer Churn Prediction and Spending Prediction Project

This project analyzes customer behavior and uses machine learning models to predict:
1. **Customer Spending Amount** (Regression).
2. **Customer Churn** (Classification).

---

## **Dataset**
The dataset includes information about customer demographics, shopping behavior, and purchase details.

### **Columns Overview**
| Column                    | Description                                |
|---------------------------|--------------------------------------------|
| `Customer ID`             | Unique identifier for each customer        |
| `Age`                     | Age of the customer                       |
| `Gender`                  | Gender of the customer                    |
| `Item Purchased`          | Name of the purchased item                |
| `Category`                | Product category                          |
| `Purchase Amount (USD)`   | Amount spent in USD                       |
| `Location`                | Customer's location                       |
| `Size`                    | Size of the purchased item                |
| `Color`                   | Color of the purchased item               |
| `Season`                  | Season of the purchase                    |
| `Review Rating`           | Rating provided by the customer (0-5)     |
| `Subscription Status`     | Active or Inactive subscription           |
| `Payment Method`          | Method of payment used                    |
| `Shipping Type`           | Type of shipping chosen                   |
| `Discount Applied`        | Whether a discount was applied            |
| `Promo Code Used`         | Whether a promo code was used             |
| `Previous Purchases`      | Total previous purchases made             |
| `Preferred Payment Method`| Customer's preferred payment method       |
| `Frequency of Purchases`  | High, Medium, or Low purchase frequency    |

---

## **Project Goals**
1. **Customer Spending Prediction**:
   - Use regression models to predict the `Purchase Amount (USD)` based on customer features.

2. **Customer Churn Prediction**:
   - Use classification models to predict whether a customer will churn based on behavioral and demographic features.

---

## **Approach**

### **Step 1: Data Preprocessing**
- **Handling Missing Values**:
  - Checked and imputed missing values.
- **Encoding Categorical Variables**:
  - One-Hot Encoding for multi-class variables (e.g., `Category`, `Location`).
  - Label Encoding for binary variables (e.g., `Gender`, `Subscription Status`).
- **Feature Scaling**:
  - Scaled numerical variables using `StandardScaler` for regression and classification models.
- **Correlation Analysis**:
  - Visualized correlations to identify highly correlated features.
- **Splitting Data**:
  - Used `train_test_split()` for creating training and testing sets (80/20 split).

---

### **Step 2: Customer Spending Prediction**
- **Model Used**:
  - Started with `Linear Regression` as a baseline.
  - Enhanced performance using `Random Forest Regressor` and `XGBoost Regressor`.

- **Evaluation Metrics**:
  - **Mean Squared Error (MSE)**
  - **Root Mean Squared Error (RMSE)**
  - **R-squared (R²)**

- **Results**:
  - R² improved significantly with Random Forest and XGBoost.
  - Visualized predicted vs. actual spending using scatter plots.

---

### **Step 3: Customer Churn Prediction**
- **Target**:
  - Created a binary column (`Churn`) based on `Frequency of Purchases` (Low → Churn).

- **Model Used**:
  - Logistic Regression (baseline).
  - Random Forest Classifier and XGBoost Classifier for advanced modeling.

- **Evaluation Metrics**:
  - **Accuracy**
  - **Precision**
  - **Recall**
  - **F1-Score**
  - **ROC-AUC Score**

- **Results**:
  - Identified key drivers of churn using feature importance plots.
  - Visualized performance with a confusion matrix and ROC curve.

---

## **Key Visualizations**
1. **Correlation Heatmap**:
   - Displayed relationships between numerical features.
2. **Feature Importance**:
   - Highlighted the most important features influencing predictions.
3. **Confusion Matrix**:
   - Showed the model's performance for classification.
4. **Predicted vs. Actual Spending**:
   - Scatter plot comparing predicted and actual spending.

---

## **How to Run the Project**
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repository-name.git
2.Navigate to the project directory:
```cd your-repository-name```
3.Run the notebook or script:
```python churn_spending_analysis.py```

Let me know if you need further adjustments!


