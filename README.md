# 🧠 Task 4: Logistic Regression - Binary Classification

## 📁 Files Included

- `Task4_Intern.ipynb` – Jupyter Notebook with **full code, visualizations, and output**
- `data.csv` – The binary classification dataset (**Breast Cancer Wisconsin Diagnostic Data**)

---

## 🎯 Objective

To build and evaluate a **binary classification model** using **Logistic Regression**, following proper data preprocessing, visualization, model training, evaluation, threshold tuning, and sigmoid explanation.

---

## 🛠️ Tools Used

- **Python**  
- **Pandas**, **NumPy** for data handling  
- **Matplotlib**, **Seaborn** for visualization  
- **Scikit-learn** for model building and evaluation  

---

## ✅ Task Overview & Steps Followed

| Step | Description |
|------|-------------|
| 1. 📥 **Import Libraries** | Imported all necessary Python libraries including scikit-learn, pandas, and matplotlib |
| 2. 🧾 **Load Dataset** | Loaded the dataset from `data.csv` |
| 3. 🕵️‍♂️ **Initial Inspection** | Checked dataset structure, types, and previewed rows |
| 4. 🧹 **Dropped Unnecessary Columns** | Removed `id` and `Unnamed: 32` columns |
| 5. 🔍 **Missing Values Check** | Verified that there are no missing values |
| 6. 📊 **Histograms** | Plotted distributions for all numerical features |
| 7. 🔁 **Label Encoding** | Encoded the target variable (`diagnosis`: M = 1, B = 0) |
| 8. 🔥 **Correlation Heatmap** | Visualized feature correlations using a heatmap |
| 9. 🎯 **Feature/Target Split** | Split data into features (X) and target (y) |
| 10. ⚖️ **Standardization** | Scaled features using `StandardScaler` |
| 11. 🧪 **Train-Test Split** | Split the data into training and testing sets |
| 12. 🧠 **Model Training** | Trained a **Logistic Regression** model |
| 13. 📈 **Model Evaluation** | Evaluated model using:  
    - Confusion Matrix  
    - Accuracy Score  
    - Precision & Recall  
    - ROC AUC Score  
    - Classification Report |
| 14. 📉 **ROC Curve** | Plotted the ROC curve and calculated AUC |
| 15. 🧪 **Threshold Tuning** | Adjusted threshold (e.g., 0.3) and observed effect on performance |
| 16. 🧮 **Sigmoid Explanation** | Visualized and explained the sigmoid activation function |

---

## 📊 Model Evaluation Metrics (Threshold = **0.5**)

- **Confusion Matrix:**

```
[[70  1]
 [ 2 41]]
```

- **Accuracy Score**: `0.9737`  
- **Precision Score**: `0.9762`  
- **Recall Score**: `0.9535`  
- **ROC AUC Score**: `0.9697`  

- **Classification Report:**

```
              precision    recall  f1-score   support

           0       0.97      0.99      0.98        71
           1       0.98      0.95      0.96        43

    accuracy                           0.97       114
   macro avg       0.97      0.97      0.97       114
weighted avg       0.97      0.97      0.97       114
```

---

## 🔄 Threshold Tuning (Threshold = **0.3**)

To favor **higher recall** (important in medical diagnosis), the threshold was lowered to `0.3`.

- **Confusion Matrix:**

```
[[67  4]
 [ 1 42]]
```

- **Precision**: `0.9130`  
- **Recall**: `0.9767`  

This demonstrates how adjusting the threshold can improve recall at the cost of a slight drop in precision — useful when false negatives are more harmful than false positives.

---

## 🧠 Sigmoid Function Explanation

The sigmoid function converts raw output values from the logistic regression model into probabilities between 0 and 1.

### 🔣 Mathematical Formula:

```text
Sigmoid(z) = 1 / (1 + e^(-z))
```

### 📐 LaTeX Format (for documentation or reports):

```latex
\sigma(z) = \frac{1}{1 + e^{-z}}
```

---

## 🔗 Author

Internship Task Submission by **Madhavendra Singh**  
Notebook: `Task4_Intern.ipynb`  
Dataset: `data.csv`
