# Titanic Survival Prediction

Predicting passenger survival on the Titanic using advanced ensemble machine learning.

---

## 🚢 Project Overview

This project analyzes the [Kaggle Titanic dataset](https://www.kaggle.com/c/titanic) to predict which passengers survived the 1912 disaster. By leveraging exploratory data analysis (EDA), feature engineering, and an ensemble of Random Forest and XGBoost classifiers, we achieve robust classification performance on this classic binary prediction task.

---

## 📊 Dataset

- **Source:** Kaggle Titanic Competition
- **Files Used:** `train.csv`, `test.csv`
- **Features:** Passenger demographics, ticket class, fare, family structure, title, and more.
- **Target:** `Survived` (0 = No, 1 = Yes)

---

## 🔬 Project Structure


---

## 📈 Exploratory Data Analysis (EDA)

- **Survival rates** analyzed by class, gender, age, family size, and embarkation port.
- **Feature engineering:** Extracted titles from names, created family size and IsAlone features, binned age and fare, and imputed missing values.
- **Key insights:** Women, children, and first-class passengers had higher survival rates; solo travelers and third-class males had the lowest.

---

## 🧠 Modeling Approach

- **Feature Set:**  
  `Pclass`, `Sex`, `Age`, `Fare`, `Embarked`, `Title`, `IsAlone`, plus engineered features from EDA.

- **Model Selection:**  
  An ensemble model combining Random Forest and XGBoost classifiers using soft voting was chosen for its superior accuracy and generalization.

- **Validation:**  
  - 80/20 stratified train/validation split
  - 10-fold cross-validation for robust performance metrics

---

## 🚀 Usage

### 1. Install Requirements

pip install -r requirements.txt


### 2. Run the Notebook

Open and execute `Titanic.ipynb` in Jupyter or Google Colab to reproduce the EDA, feature engineering, and model training.

### 3. Train and Evaluate the Model

The notebook includes code to:
- Prepare features
- Train the ensemble model
- Evaluate accuracy and classification metrics
- Save the trained model as `titanic_ensemble_model.pkl`

### 4. Predict on New Data

To use the trained model for predictions:


---

## 📊 Results

| Model                | Validation Accuracy | Cross-Validated Accuracy |
|----------------------|--------------------|-------------------------|
| Random Forest + XGB  | ~81%               | ~80% ± 3%               |

- **Best Features:** Title, Sex, Pclass, Age, IsAlone, Fare, Embarked
- **Key Finding:** Ensemble models with engineered features outperform single algorithms.

---

## 📁 Data Preprocessing & Feature Engineering

- Imputed missing ages and fares
- Extracted and grouped titles from names
- Created `FamilySize` and `IsAlone` features
- Encoded categorical variables (LabelEncoder)
- Binned continuous variables (Age, Fare) for robustness

---

## 🛠️ Deployment

- The trained ensemble model (`titanic_ensemble_model.pkl`) can be deployed as a REST API using Flask or FastAPI.
- Ensure the same preprocessing pipeline is applied to new data before prediction.

---

## 📚 References & Acknowledgements

- [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic)
- [DataCamp Titanic Tutorial]
- [Project structure and README best practices]
- Thanks to the open-source data science community for inspiration and guidance.

---

## 📄 License

This project is open-source under the MIT License.  
Please check the Kaggle dataset license for data usage terms.

---

## 🤝 Contributing

Pull requests and suggestions are welcome!  
Please open an issue or submit a PR to contribute.

---

*For questions or feedback, please contact the repository maintainer.*

---

**Happy predicting!**
