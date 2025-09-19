# Human Activity Recognition (HAR)

This project focuses on **Human Activity Recognition (HAR)** using data collected from smartphones’ embedded sensors such as accelerometers and gyroscopes. The task is to classify physical activities (e.g., walking, sitting, standing, etc.) based on extracted features.

---

## 📌 Dataset Info

- **Train set**: 7,353 samples  
- **Test set**: 1,000 samples  
- **Features**: 562 sensor-derived features (accelerometer, gyroscope, etc.)  
- **Activity classes**:  
  - Laying  
  - Standing  
  - Sitting  
  - Walking  
  - Walking Upstairs  
  - Walking Downstairs  

---

## 🔬 Methodology

1. **Data Preprocessing & Feature Engineering**  
   - Normalization and cleaning  
   - Dimensionality reduction explored via **PCA** and **t-SNE**  

2. **Train/Test Split**  
   - Dataset split in **80:20 ratio**  

3. **Models Trained & Tuned**  
   - **Logistic Regression**  
     - Parameters: `{ 'max_iter': [100, 200, 500] }`  
     - Best: `max_iter=500`  
     - Accuracy: **95.5%**  

   - **Support Vector Machine (SVM)**  
     - Parameters: `{ 'kernel': ['linear', 'rbf', 'poly', 'sigmoid'], 'C': [100, 50] }`  
     - Best: `kernel='rbf', C=50`  
     - Accuracy: **96.6%**  

   - **Decision Tree**  
     - Parameters: `{ 'max_depth': [2, 4, 6, 8] }`  
     - Best: `max_depth=6`  
     - Accuracy: **83.6%**  

   - **Random Forest**  
     - Parameters: `{ 'n_estimators': [20–100], 'max_depth': [2–16] }`  
     - Best: `n_estimators=100, max_depth=14`  
     - Accuracy: **91.6%**  

---

## 📊 Results

- **Best performing model**: **SVM (RBF kernel, C=50)** with **96.6% accuracy**  
- Logistic Regression also performed strongly with 95.5% accuracy.  
- Ensemble methods (Random Forest) showed competitive results but slightly lower accuracy compared to SVM.  
- Decision Tree underperformed relative to other approaches.  

---

## 🛠 Technologies and Packages Used

- Python (Jupyter Notebook)  
- NumPy, Pandas, Matplotlib, Seaborn  
- scikit-learn (Logistic Regression, SVM, Decision Tree, Random Forest)  

---

---

## 👤 Author

Developed by **Dipean Dasgupta** <br> 
BTech CSE Graduate, AI & ML Enthusiast <br><br>
**Feel free to fork, modify, and improve!**
