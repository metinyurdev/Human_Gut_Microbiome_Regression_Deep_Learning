# 🧬 **Biological Age Prediction Using Gut Microbiome Data**

In this project, we aim to predict the biological age of individuals using gut microbiome data. DNA samples of microorganisms in the gut can provide significant clues about a person's biological age. In this study, regression models will be developed using gut microbiome data and biological age information from **4274 individuals**.

## 🔍 **Dataset Overview**
The dataset consists of **4274 samples**, each containing the count of DNA fragments from **3200 different types** of microorganisms. These microorganisms represent the diversity of the gut microbiome. The goal is to predict the **biological age** of individuals based on this data.

The project utilizes various **regression models** and evaluates them using:
- **Mean Absolute Error (MAE)**
- **R-squared (R²)** metrics
- **Scatter plot** to visualize the relationship between actual and predicted biological age.

---

## 📈 **Results**

The project involved several stages of data preprocessing, model selection, and evaluation:

### 🧩 **Data Preprocessing**
1. **Data Merging:**
   - Merged `data.csv` and `Ages.csv` files using a left join based on sample names.

2. **Missing Data Analysis:**
   - Checked and handled missing values in the dataset.

3. **Target Variable Analysis:**
   - Visualized the distribution of the target variable **`Age`**.

---

### 🔍 **Feature Engineering and Model Training**
1. **Correlation Analysis:**
   - Analyzed relationships between features and the target variable.

2. **Standardization:**
   - Standardized features using **MinMaxScaler**.

3. **Feature Selection:**
   - Used **RandomForest** to determine feature importance and selected the most significant features.

4. **Outlier Removal:**
   - Removed outliers using the **Z-score** method.

---

### 🧠 **Model Selection and Optimization**
1. **Model Screening with LazyPredict:**
   - Tested several regression algorithms, with **`ExtraTreeRegressor`** being the best-performing model initially.

2. **Cross-Validation:**
   - Performed 5-fold cross-validation with **`ExtraTreeRegressor`**.

3. **Hyperparameter Optimization:**
   - Tuned hyperparameters of **`ExtraTreeRegressor`** using **Grid Search**.

4. **Learning Curve Analysis:**
   - Detected overfitting during model learning.

---

### 🏆 **Model Performance**
1. **LazyPredict Results:**
   - **`ExtraTreeRegressor`** achieved an initial **MAE** of **12**.

2. **Optimization Results:**
   - After cross-validation and grid search, **`ExtraTreeRegressor`** achieved **MAE = 15**.

3. **MLP Regressor Results:**
   - **`MLPRegressor`** achieved an **MAE** of **13.25** with **R² = 0.107** and **Test R² = 0.154**.

4. **Model Comparison:**
   - Reference paper reported an **MAE = 10.6**; the best result here was **MAE = 13.25**.

---

### 💡 **Conclusion and Future Work**
- Although **`ExtraTreeRegressor`** initially showed the best performance, it was excluded due to overfitting.
- **`MLPRegressor`**, which displayed a more balanced performance, was chosen as the final model.
- Future improvements can include:
  - Increasing dataset size.
  - Enhancing feature engineering.
  - Exploring more advanced optimization techniques.

This project demonstrates the potential of using gut microbiome data to predict biological age, achieving results similar to those reported in the reference paper. Further work can improve model performance and generalization.

---

## 📥 **Dataset**
The datasets used in this project were obtained from the paper [Human Gut Microbiome Aging Clock Based on Taxonomic Profiling and Deep Learning](https://www.nature.com/articles/s41591-020-01089-x).


## 🧰 **Libraries and Tools Used**

This project was developed using the following technologies and environment:

- **Programming Language:** Python 🐍
- **Development Environment:** Visual Studio Code 🖥️
- **Notebook Environment:** Jupyter Notebook 📓
- **Libraries:**
  - **Pandas** 📊
  - **Numpy** 🔢
  - **Matplotlib** 📈
  - **Seaborn** 📉
  - **Scikit-learn** 🔧
  - **LazyPredict** 🧠
  - **Missingno** 🚫
  - **Jupyter Summary Tools** 📝

To install the required libraries:

```bash
!pip install pandas
!pip install numpy
!pip install matplotlib
!pip install seaborn
!pip install scikit-learn
!pip install lazypredict
!pip install jupyter-summarytools
!pip install missingno


