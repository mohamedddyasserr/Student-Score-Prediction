# Student Exam Score Prediction

## Problem Statement
The goal of this project is to predict **students' exam scores** based on various factors that may influence academic performance.  
By building and evaluating predictive models, we aim to understand how different variables—such as study hours, attendance, and background information—contribute to exam outcomes.  

## Dataset Overview
The dataset contains multiple features describing student academic behavior and background.  
Some examples of features include:
- `Hours_Studied` — Number of study hours before the exam
- `Attendance` — Percentage of classes attended
- `Tutoring_Sessions` — Number of extra help sessions attended
- `Parental_Education_Level` — Education level of parents
- `Previous_Scores` — Average past academic performance
- Target variable: `Exam_Score`

> **Note:** Data was preprocessed to ensure quality by handling missing values, encoding categorical variables, and scaling numerical features where necessary.

## Model Used
We used a **Linear Regression** model to predict the target variable (`Exam_Score`).  
Linear Regression was chosen for its simplicity, interpretability, and ability to measure relationships between input features and the predicted score.

---

## Model Versions & Results

### **Version 1 — Single Feature Model**
- **Feature Used:** `Hours_Studied` only  
- **R² Score:** *~0.232*  
- **MAE:** *~3–4 points*  
- **MSE:** *~10.856*  
- **Insights:**
  - Shows that study hours have some positive correlation with exam performance.
  - However, the model explains only a small fraction of the variation in scores.
  - Prediction error is relatively high, making it less reliable.

---

### **Version 2 — Multi-Feature Model**
- **Features Used:** **All available features** in the dataset  
- **R² Score:** *0.77*  
- **MAE:** *0.45 points*  
- **MSE:** *3.26*  
- **Insights:**
  - Significantly better performance compared to Version 1.
  - Captures a broader range of factors affecting exam scores.
  - Much lower prediction error, indicating stronger reliability.

---

## Comparison Between Models

| Metric         | Version 1 (Hours Only) | Version 2 (All Features) |
|----------------|------------------------|--------------------------|
| R² Score       | ~0.232                  | **0.77**                 |
| MAE            | ~3–4                   | **0.45**                 |
| MSE            | 10.856                   | **3.26**                 |

**Key Takeaways:**
- Relying on `Hours_Studied` alone oversimplifies the problem and leads to poor predictive performance.
- Including all features allows the model to capture more complex relationships, resulting in much higher accuracy.
- For practical applications, **multi-feature models** should be preferred over single-variable models.

---

## Visualizations
The project includes visualizations comparing predicted vs. actual exam scores for both model versions.  
These plots help visually assess model accuracy and identify patterns or outliers.
![Model V1 Graph] <img width="718" height="561" alt="image" src="https://github.com/user-attachments/assets/5fb17fd2-ef9d-4a5e-81b1-929af2379de9" />
![Model V2 Graph] <img width="999" height="732" alt="image" src="https://github.com/user-attachments/assets/1eba6446-1e3a-4cbe-9756-2fbc6dba549f" />



---

## Conclusion
The comparison between the two model versions clearly shows that relying solely on study hours as a predictor provides limited accuracy. By incorporating all available features, the model achieved significantly better performance across all evaluation metrics. This highlights the importance of considering multiple factors when predicting student exam scores, as real-world academic performance is influenced by a combination of study habits, background, and other contextual variables.
