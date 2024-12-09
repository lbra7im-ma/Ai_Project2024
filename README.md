# Ai_Project2024

Created: 1/9/2024
Cattle disease prediction using Machine Learning. This project is used to predict the disease based on the symptoms. It predicts using 4 different machine learning algorithms. So, the output is accurate.. Github:https://github.com/lbra7im-ma/Ai_Project2024




# Cattle Disease Prediction Using Machine Learning

## **Overview**
This project predicts cattle diseases based on symptoms provided by the user. Using machine learning models, the system analyzes input symptoms and predicts the most likely disease. The project supports three machine learning models:
- Decision Tree
- Random Forest
- Naive Bayes

The main goal is to assist farmers and veterinarians in identifying cattle diseases early to reduce losses and improve animal health.

---

## **Features**
1. **User Input:**  
   - Enter up to 5 symptoms related to cattle health.  
   - Example symptoms: fever, loss of appetite, diarrhea.  
   
2. **Machine Learning Models:**  
   - Decision Tree Classifier  
   - Random Forest Classifier (with 100 estimators)  
   - Naive Bayes Classifier  

3. **Prediction and Analysis:**  
   - Predicts the disease based on input symptoms.  
   - Calculates accuracy and displays a confusion matrix for each model.  

4. **Data Storage:**  
   - Saves input and prediction results in an SQLite database.  

5. **Visualization:**  
   - Scatter plots for input symptoms.  
   - Scatter plots for predicted diseases and their associated symptoms.

---

## **Dataset**
### **Training Data:**
- File: `training.csv`
- Columns:
  - **Symptoms:** Contains binary values (0 or 1) for each symptom.
  - **Prognosis:** Specifies the disease associated with the symptoms.

### **Testing Data:**
- File: `testing.csv`
- Used to evaluate model performance and calculate accuracy.

### **Data Preprocessing:**
1. **Label Encoding:**  
   The `prognosis` column (disease names) is encoded as integers using Pandas `replace()`.

2. **Feature and Target Separation:**  
   - `X`: All symptom columns (features).  
   - `y`: Prognosis column (target).

---

## **How It Works**
1. User enters symptoms via the GUI.
2. Input symptoms are processed into a binary list.
3. Selected machine learning model predicts the most likely disease.
4. Results are saved in the database, and visualizations are generated.

---

## **Machine Learning Models**
### **1. Decision Tree**
- A tree-based classifier that splits data based on symptom values.
- Provides a straightforward and interpretable prediction process.

### **2. Random Forest**
- An ensemble model that builds multiple decision trees and combines their predictions.
- Achieves higher accuracy by reducing overfitting.

### **3. Naive Bayes**
- A probabilistic model that calculates the likelihood of diseases based on symptoms.
- Suitable for datasets with categorical features.

---

## **Technologies Used**
1. **Programming Language:** Python
2. **Libraries:**
   - **Data Processing:** Pandas, NumPy
   - **Machine Learning:** Scikit-learn
   - **Visualization:** Matplotlib
   - **Database:** SQLite
3. **GUI:** Tkinter

---

## **Database**
- **File:** `database.db`
- Stores user input and prediction results for all three models.
- Tables:
  - `DecisionTree`
  - `RandomForest`
  - `NaiveBayes`

Each table contains:
- User Name
- Symptoms entered
- Predicted Disease

---



Usage
Launch the GUI.
Enter your name and up to 5 symptoms.
Choose a machine learning model to run:
Decision Tree
Random Forest
Naive Bayes
View the predicted disease, accuracy, and confusion matrix.
Check the scatter plots for a visual representation.
