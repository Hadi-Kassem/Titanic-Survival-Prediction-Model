# Titanic Survival Prediction 

This project is a classic binary classification task using the Titanic dataset. The goal is to predict whether a passenger survived the Titanic disaster based on features like age, gender, passenger class, and more.

---

##  Dataset

The dataset is from [Kaggle's Titanic Competition](https://www.kaggle.com/c/titanic/data):

- `train.csv`: Labeled data with the `Survived` column.
- `test.csv`: Unlabeled data used for prediction.

---


---

##  Preprocessing

- **Missing Values**:
  - Age imputed with median.
  - Cabin dropped due to high missing ratio.

- **Categorical Encoding**:
  - `Sex`, `Embarked`, and `Pclass` one-hot encoded.


- **Pipeline Used**: `ColumnTransformer` + `Pipeline` from `sklearn`.

---

##  Model

- **Model Used**: `RandomForestClassifier`
- **Tuning**: Hyperparameter tuning using `GridSearchCV`
- **Cross-Validation**: 5-fold stratified cross-validation on training set

---

## 📊 Evaluation

On the validation set:

- **Accuracy**: 0.81
- **Precision**: 0.75
- **Recall**: 0.75
- **F1 Score**: 0.75

Confusion Matrix:
[[94 17]
[17 51]]



---

## 📈 Visualizations

- Correlation heatmap of numeric features
- Survival rate by gender
- training and tesing data main features' distribution

---

## 🚀 How to Run

1. **Clone the repo**:
   ```bash
   git clone <your-repo-url>
   cd titanic_project
2.  **Set up virtual environment**:
   python -m venv titanicvenv
   source titanicvenv/bin/activate  # or `titanicvenv\Scripts\activate` on Windows
   pip install -r requirements.txt
3.  **Run the notebook**:
   Open titanic.ipynb in VS Code or Jupyter Notebook and run all cells.