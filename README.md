# ⚽ Data-Driven Football Team Selection and Role Assignment  
**A Machine Learning Project**  
*Supervised by Dr. Franck Jaotombo (emlyon business school)*  

🔗 **[Project Presentation (Google Drive)](https://drive.google.com/drive/folders/1EZd__SqtN-yHQUxzj9liumVBvkQUOyq-?usp=drive_link)

---

## 📌 Project Overview  
This project applies **machine learning and data science** techniques to enhance player selection and role assignment for the **emlyon business school football team**. By analyzing professional football datasets, the objective is to create a fair and unbiased system that maximizes team performance through data-driven insights.

📄 **A PDF file containing the full project analysis is included in this repository.**  

---

## 📋 Table of Contents  
- [Project Overview](#-project-overview)  
- [Key Features](#-key-features)  
- [How It Works](#-how-it-works)  
- [Technologies & Tools](#-technologies--tools)  
- [Model Performance](#-model-performance)  
- [Installation & Setup](#-installation--setup)  
- [Results](#-results)  
- [Future Improvements](#-future-improvements)  
- [References](#-references)  

---

## 🚀 Key Features  
- **Role Assignment**: Automated assignment of players to roles (Forward, Midfielder, Defender, Goalkeeper) using **feature engineering** and weighted scoring.  
- **Unsupervised Learning**:  
   - **Principal Component Analysis (PCA)** to reduce dimensionality.  
   - **K-Means Clustering** to segment players by skills and performance.  
- **Supervised Learning**:  
   - Regression models to predict **player ratings**.  
   - Classification models to assign **player roles**.  
- **Hyperparameter Tuning**: Optimized models through cross-validation and stratified sampling.  
- **Bias Elimination**: Objective, data-driven player selection to remove subjective bias from traditional scouting methods.  

---

## ⚙️ How It Works  
### 1. **Data Collection**  
- Dataset: **FIFA player attributes** (sourced from Kaggle).  
- Format: SQLite database with **183,978 observations and 42 attributes**.  

### 2. **Data Preprocessing**  
- **Cleaning**: Handled missing values and outliers using z-scores and imputation (mode, mean, median).  
- **Outlier Treatment**: Winsorization applied to retain data from top-performing players.  
- **Reduction**: Dropped irrelevant features to reduce dimensionality.  

### 3. **Feature Engineering**  
- Role-specific weighted scoring (based on player attributes).  
- Players assigned to roles based on their highest-scoring category.  

### 4. **Machine Learning Approaches**  
- **Unsupervised Models**:  
   - **PCA**: Transformed data into two primary dimensions representing offensive, defensive, and technical skills.  
   - **K-Means**: Clustered players into roles aligning with football positions.  
- **Supervised Models**:  
   - **k-NN Regressor**: Predicted player ratings (Adjusted R²: **0.9357**).  
   - **k-NN Classifier**: Assigned roles (F1 Score: **0.9**).  
   - Ridge, Lasso, Random Forest, Decision Trees, and XGBoost regressors used for comparison.  

---

## 🛠️ Technologies & Tools  
- **Languages**: Python  
- **Libraries**: Pandas, Scikit-Learn, NumPy, Matplotlib, Seaborn  
- **Database**: SQLite (FIFA dataset from Kaggle)  
- **Modeling Tools**:  
   - Regression: k-Nearest Neighbors (k-NN), Ridge, Lasso, XGBoost  
   - Classification: k-NN Classifier  
- **Visualization**: PCA scatter plots, heatmaps, clustering graphs  
- **Development Tools**: Jupyter Notebooks, Google Colab  

---

## 📊 Model Performance  
- **k-NN Regressor** (Rating Prediction):  
   - Adjusted R²: **0.9357**  
   - RMSE/ymean: **0.0261**  
- **k-NN Classifier** (Role Assignment):  
   - F1 Weighted Average: **0.9**  

Feature importance analysis eliminated less significant PCA components, ensuring efficient model performance with minimal compromise.  

---

## 📥 Installation & Setup  
### 1. Clone the Repository  

- **A dataset and Jupyter notebook are included in the GitHub repository.**
- **Open the notebook and run each cell step-by-step.**   
- **Ensure to update the path to the dataset to match your local PC directory before running the notebook.**  

Example:  
```python
FILE_PATH = "path/to/your/local/datasets/"
```  

---

## 📈 Results  
- **PCA Visualization**: Players grouped into clusters representing their roles (Attackers, Midfielders, Defenders, Goalkeepers).  
- **Cluster Analysis**: K-Means clustering aligned with player positions, validating the model’s accuracy.  
- **Model Insights**:  
   - The most significant PCA component represented offensive and technical skills.  
   - The optimized k-NN model achieved a final Adjusted R² of **0.9043** post-feature elimination.  

---

## 🔧 Future Improvements  
- **Real-World Testing**: Apply model to **emlyon football players** for validation.  
- **Expand Features**: Incorporate intangible traits like leadership, teamwork, and adaptability.  
- **Scalability**: Adapt model for larger datasets to analyze more players.  
- **Application**: Extend to youth academies, amateur leagues, and professional clubs.  

---

## 📚 References  
- [Kaggle FIFA Dataset](https://www.kaggle.com/stefanoleone992/fifa-20-complete-player-dataset)  
- [Scikit-Learn Documentation](https://scikit-learn.org/stable/)  
- [Machine Learning for Sports Analytics](https://towardsdatascience.com/tagged/sports-analytics)  
