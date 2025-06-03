# 🌳 Task 5: Decision Trees and Random Forests

**Internship Task | Elevate Labs | AI & ML Track**

## 📌 Objective

Implement and compare tree-based models (Decision Tree and Random Forest) for classification using the Heart Disease dataset. Analyze overfitting, visualize trees, evaluate with cross-validation, and interpret feature importance.

---

## 🧠 Concepts Covered

- Decision Trees
- Random Forests (Bagging Ensemble)
- Overfitting vs Underfitting
- Tree Depth Control
- Feature Importance
- Cross-Validation Evaluation

---

## 📂 Dataset Used

- **Heart Disease Dataset**  
  Source: [Kaggle - Heart Disease](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset)

- **Target Column:** `target`  
  - 0 = No Heart Disease  
  - 1 = Heart Disease

---

## 🧪 Tools & Libraries

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib
- Graphviz (optional for tree export)
- Jupyter Notebook (for experimentation)

---

## ⚙️ Steps Performed

### 1. Load & Explore Data
- Loaded CSV locally
- Checked data types, class balance, and null values

### 2. Preprocessing
- Split data into `X` (features) and `y` (target)
- Scaled features using `StandardScaler`
- Split into 80% training and 20% testing sets

### 3. Decision Tree (Unrestricted)
- Trained a Decision Tree without limiting depth
- Visualized tree using `plot_tree`
- Observed overfitting (very high train accuracy, lower test accuracy)

### 4. Decision Tree (Limited Depth)
- Set `max_depth=4` to control overfitting
- Accuracy improved on test set, more balanced

### 5. Random Forest
- Trained a `RandomForestClassifier` with 100 estimators
- Evaluated accuracy and compared with single decision tree

### 6. Feature Importance
- Extracted and plotted feature importances using `.feature_importances_`

### 7. Cross-Validation
- Used `cross_val_score` with 5-fold CV to evaluate generalization
- Compared CV accuracy for both Decision Tree and Random Forest

---

## 📊 Results

| Model                  | Train Accuracy | Test Accuracy | CV Accuracy (Mean ± Std) |
|------------------------|----------------|---------------|---------------------------|
| Decision Tree (default)| High (~1.00)   | Lower         | ~ varies                  |
| Decision Tree (depth=4)| ~0.85          | ~0.84         | ~0.82 ± 0.04              |
| Random Forest          | ~0.91          | ~0.89         | ~0.87 ± 0.03              |

> Random Forest performed the best overall in generalization and robustness.

---

## 📈 Visualizations Included

- Decision Tree (Unrestricted):![randomforest](https://github.com/user-attachments/assets/086bfb7a-9ddc-4b44-a7ac-0a6e9fd75e94)


- Decision Tree (Depth-Limited)![randomforest](https://github.com/user-attachments/assets/2c842f04-f8b1-4d44-9a30-8af4f582907d)


- Random Forest Feature Importances![randomforest](https://github.com/user-attachments/assets/485e1811-d7fa-4752-a11d-939d1c25b693)





## 📁 Repository Contents

