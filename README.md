# ❤️ Heart Disease Prediction using Logistic Regression

This project is a **machine learning model** that predicts whether a person has heart disease or not based on medical attributes.  
The dataset used contains 303 samples with 13 features (age, sex, cholesterol levels, etc.) and a target variable (0 = Healthy, 1 = Heart Disease).

---

## 📂 Dataset
The dataset used is `heart_data.csv` which contains the following columns:

- **age**: Age of the person  
- **sex**: Gender (1 = Male, 0 = Female)  
- **cp**: Chest pain type (0–3)  
- **trestbps**: Resting blood pressure  
- **chol**: Serum cholesterol (mg/dl)  
- **fbs**: Fasting blood sugar > 120 mg/dl (1 = True, 0 = False)  
- **restecg**: Resting electrocardiographic results (0–2)  
- **thalach**: Maximum heart rate achieved  
- **exang**: Exercise induced angina (1 = Yes, 0 = No)  
- **oldpeak**: ST depression induced by exercise  
- **slope**: Slope of the peak exercise ST segment  
- **ca**: Number of major vessels (0–4) colored by fluoroscopy  
- **thal**: Thalassemia (0–3)  
- **target**: Heart disease (1 = Yes, 0 = No)  

---

## ⚙️ Steps in the Project

1. **Data Collection & Processing**
   - Loaded dataset using `pandas`
   - Checked for missing values (none found)
   - Explored dataset with `.head()`, `.tail()`, `.info()`, `.describe()`

2. **Data Splitting**
   - Split dataset into features (`x`) and labels (`y`)
   - Used `train_test_split` with **80% training** and **20% testing**

3. **Model Training**
   - Trained a **Logistic Regression** model using `sklearn`
   - Resolved convergence warning by increasing `max_iter` if needed

4. **Model Evaluation**
   - **Training Accuracy**: ~85%  
   - **Testing Accuracy**: ~82%  

5. **Predictive System**
   - Built a system to predict heart disease for new input data

---

## 🧪 Example Prediction

```python
input_data = (55,1,0,160,289,0,0,145,1,0.8,1,1,3)

prediction = model.predict([input_data])

if prediction[0] == 0:
    print("The person does not have heart disease")
else:
    print("The person has heart disease")
