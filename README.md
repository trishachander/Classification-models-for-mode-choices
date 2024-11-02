# 🚆 Transport Mode Choice Prediction Using Classification Models

## 📚 Course Information
- **Course**: AH2179
- **Module**: 3
- **Project**: Classification Models for Travel Mode Choice Prediction

## 🎯 Project Overview
This project implements and compares multiple classification models to predict transportation mode choices (air, bus, rail, car) using various machine learning techniques, with a focus on handling class imbalance.

## 📊 Data Distribution
- Rail: 41.8% (1288 samples)
- Car: 31.8% (978 samples)
- Air: 22.9% (705 samples)
- Bus: 3.5% (109 samples)

## 🏗️ Model Architecture
### Data Preprocessing
- **Features**: All columns except 'choice'
- **Scaling**: StandardScaler implementation
- **Encoding**: One-hot encoding
- **Data Split**: 75% training, 25% testing
- **Cross-Validation**: Stratified K-fold

### 🤖 Models Implemented
1. Logistic Regression (Best Performer)
2. XGBoost Classifier
3. Random Forests
4. Decision Trees
5. KNN
6. SVM
7. Nearest Centroid

## ⭐ Best Model Configuration
Logistic Regression parameters:
- **C**: 0.1
- **penalty**: 'l2'
- **solver**: 'newton-cg'

## 📈 Performance Metrics
### Logistic Regression Results
- **Accuracy**: 57%
- **Precision**: [0.546, 0.0, 0.471, 0.663]
- **Recall**: [0.524, 0.0, 0.533, 0.669]

## 💡 Key Findings & Detailed Reflections

### 🔍 Model Performance Analysis
1. **Class Imbalance Impact**
   - Models showed bias towards majority classes (rail, car)
   - KNN and Nearest Centroid uniquely detected 'bus' class despite low overall accuracy
   - Random Forests and Decision Trees showed high sensitivity to imbalanced data

2. **Model-Specific Observations**
   - **Logistic Regression**: 
     - L2 regularization prevented overfitting
     - Newton-CG solver optimized classification accuracy
   - **XGBoost**: Performed similarly to Logistic Regression
   - **KNN & Nearest Centroid**: Better at minority class detection
   - **SVM**: Struggled with imbalanced classes
   - 
<img src="https://github.com/user-attachments/assets/62d8da83-2e68-4ee6-a19a-449f30a4a67b" width="400">

### 🎓 Technical Lessons Learned
1. **Data Preprocessing Insights**
   - Critical importance of feature encoding methods
   - Impact of training/testing split ratios
   - Value of standardization in model performance

2. **Model Selection Considerations**
   - LazyPredict library's utility in initial model screening
   - Importance of class_weight parameter
   - Trade-offs between accuracy and minority class detection

3. **Optimization Techniques**
   - Grid search effectiveness for parameter tuning
   - Cross-validation strategies for imbalanced data
   - Regularization impact on model robustness

## 🔮 Future Applications & Transport Problems

### 📋 Potential Applications
1. **Bus Delay Classification**
   - Handling imbalanced on-time vs delayed data
   - Implementing resampling techniques (SMOTE, oversampling)
   - Ensemble methods for improved performance

2. **Traffic Pattern Classification**
   - Multi-class prediction for congestion levels
   - Real-time pattern recognition
   - Seasonal variation analysis

3. **Infrastructure Usage Prediction**
   - Peak vs off-peak utilization
   - Facility type selection
   - Maintenance scheduling

### 🛠️ Recommended Techniques
1. **Handling Imbalanced Data**
   - SMOTE (Synthetic Minority Over-sampling Technique)
   - Adaptive synthetic sampling
   - Hybrid sampling approaches

2. **Ensemble Methods**
   - Voting Classifiers
   - Stacking multiple models
   - Boosting algorithms

3. **Advanced Feature Engineering**
   - Temporal feature extraction
   - Spatial correlation analysis
   - Domain-specific feature creation

## 🛠️ Dependencies
- Scikit-learn
- XGBoost
- Pandas
- NumPy
- LazyPredict
- Matplotlib
- Seaborn

---
*Note: This project was completed as part of the AH2179 course, Module 3.* 🎓
