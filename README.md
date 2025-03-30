# NNC 2
---

### **Project Overview**  
This project focuses on building a **machine learning model** to predict two key workforce outcomes:  
1. **Employee Attrition** – Whether an employee is likely to leave the company.  
2. **Department Assignment** – Which department an employee belongs to.  

The model uses various factors like **age, travel frequency, education level, job satisfaction, marital status**, and more to make predictions. The project includes multiple stages: **data preprocessing**, **neural network creation**, **model training**, and **evaluation** to ensure accurate predictions. By identifying attrition risks and department fit, companies can improve **employee retention and satisfaction** with data-driven insights.  

---

### **Functionality Breakdown**  

#### **🔹 Data Preprocessing**
- `train_test_split`: Splits the dataset into training and testing sets for evaluation.  
- `StandardScaler`: Standardizes features by removing the mean and scaling to unit variance.  
- `pd.get_dummies`: Converts categorical variables into a **one-hot encoded** format.  
- `OneHotEncoder`: Encodes categorical labels (**department & attrition**) into a format suitable for training the neural network.  

#### **🔹 Neural Network Structure**
- **Input Layer:** Accepts the preprocessed dataset.  
- **Shared Layers:** Two dense layers (**64 & 32 neurons**) using **ReLU activation**, creating a shared representation of the input.  

**Department Prediction Branch**  
- Hidden Layer: **16 neurons**, ReLU activation.  
- Output Layer: **Softmax activation** to classify the department.  

**Attrition Prediction Branch**  
- Hidden Layer: **16 neurons**, ReLU activation.  
- Output Layer: **Softmax activation** to predict attrition status.  

#### **🔹 Training & Evaluation**
- `model.compile`: Uses **Adam optimizer** with **categorical cross-entropy loss** for both outputs.  
- `model.fit`: Trains the model for **100 epochs**.  
- `model.evaluate`: Assesses performance on the test dataset.  
- **Accuracy Metrics:** Measures how well the model predicts both **attrition** and **department assignment**.  

---

### **Summary of Findings**  
- **Attrition Prediction:** The model performed well, achieving around **80% accuracy** in predicting employee attrition.  
- **Department Assignment:** The model struggled more with this task, reaching **56% accuracy**.  
- **Overall Insight:** The model is useful for identifying employees at risk of leaving, but predicting department assignment accurately may require **additional features or different modeling approaches**.  

---

### **Reflection & Next Steps**
These results highlight both the **potential and limitations** of the model.  
✅ **Strengths:** High accuracy in predicting attrition, making it valuable for HR teams to identify turnover risks.  
⚠️ **Limitations:** Lower accuracy in department classification suggests that **feature selection** or **alternative models** might improve performance.  

This project reinforces the importance of **data quality, feature engineering, and rigorous evaluation** when building predictive models for real-world applications.  

---

### **Real-World Applications**  

🔹 **Human Resources:**  
- Predict employees at risk of leaving and take proactive measures like **incentives, better working conditions, and personalized retention strategies**.  

🔹 **Workforce Planning:**  
- Optimize department assignment based on **employee characteristics**, improving **job satisfaction, productivity, and performance**.  
