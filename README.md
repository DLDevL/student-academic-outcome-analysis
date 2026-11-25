# Student Academic Outcome Analysis

An end-to-end Machine Learning project that analyzes student academic performance using Classification, Clustering, and Linear Regression.

## Project Overview

The goal of this project is to analyze student academic data and apply different Machine Learning techniques to identify patterns, predict academic outcomes, and understand student performance.

The project uses the **Predict Students' Dropout and Academic Success** dataset from the UCI Machine Learning Repository.

## Objectives

- Analyze student academic data using Exploratory Data Analysis (EDA).
- Predict student outcomes using Classification algorithms.
- Identify groups of students with similar academic characteristics using Clustering.
- Predict second-semester grades using Linear Regression.
- Evaluate the performance of the implemented models.

## Technologies Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Dataset

**Dataset:** Predict Students' Dropout and Academic Success

The dataset contains 4,424 student records and 37 columns.

The target variable is `Target`, which contains three categories:

- Graduate
- Dropout
- Enrolled

Dataset source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success)

## Project Workflow

### 1. Data Loading and Exploration

- Loaded the dataset using Pandas.
- Examined dataset dimensions, data types, and statistical summaries.
- Checked for missing values and duplicate records.
- Explored relationships between academic features and student outcomes.

### 2. Data Preprocessing

- Separated input features and target variable.
- Split the dataset into training and testing sets.
- Applied StandardScaler where required.
- Prepared data for Machine Learning algorithms.

### 3. Classification

Implemented the following classification algorithms:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

**Logistic Regression Result:**

- Accuracy: 76.84%

The models were evaluated and compared to understand their classification performance.

### 4. Clustering

Implemented K-Means Clustering to identify groups of students with similar academic characteristics.

**Features selected:**

- Curricular units 1st semester (grade)
- Curricular units 2nd semester (grade)
- Curricular units 1st semester (approved)

**Methodology:**

- Applied StandardScaler to normalize the selected features.
- Used the Elbow Method to help select the number of clusters.
- Implemented K-Means with 5 clusters.
- Visualized student clusters.
- Compared cluster distributions with actual student outcomes.

### 5. Linear Regression

Implemented Simple Linear Regression to predict second-semester grades using first-semester grades.

**Independent Variable:** Curricular units 1st semester (grade)

**Dependent Variable:** Curricular units 2nd semester (grade)

The model was trained and evaluated using the following metrics:

| Evaluation Metric | Result |
|---|---:|
| MAE | 1.4983 |
| MSE | 8.3164 |
| RMSE | 2.8838 |
| R² Score | 0.6928 |

**Interpretation:**

The model explains approximately 69.28% of the variation in second-semester grades.

Residual analysis and Actual vs Predicted visualizations were also performed to understand model performance.

## Project Structure

```text
student-academic-outcome-analysis/
│
├── Student_Academic_Outcome_Analysis.ipynb
├── README.md
└── data/
    └── data.csv
```

*The structure above is the suggested organization. Adjust it to match your actual repository.*

## How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/DLDevL/student-academic-outcome-analysis.git
```

2. Navigate to the project directory:

```bash
cd student-academic-outcome-analysis
```

3. Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

4. Start Jupyter Notebook:

```bash
jupyter notebook
```

5. Open `Student_Academic_Outcome_Analysis.ipynb` and run the cells sequentially.

**Dataset Note:** Place the downloaded dataset in the `data` folder and ensure the notebook uses the correct file path. The CSV is semicolon-separated.

## Limitations

- The regression model uses only one feature to predict second-semester grades.
- Clustering results depend on the selected features and number of clusters.
- Classification predictions are based on historical student data and should not be treated as definitive judgments about individual students.
- Model performance may vary with different data splits and preprocessing choices.

## Future Improvements

- Experiment with additional classification algorithms.
- Improve regression performance using multiple features.
- Explore additional clustering algorithms such as Hierarchical Clustering and DBSCAN.
- Perform hyperparameter tuning.
- Develop an interactive dashboard to visualize student academic patterns.

## Conclusion

This project provided practical experience in implementing three major Machine Learning techniques: Classification, Clustering, and Regression.

It helped explore how Machine Learning can be applied to academic data to identify patterns, understand student performance, and predict academic outcomes.

---

**Author:** DLDevL

**GitHub:** [DLDevL](https://github.com/DLDevL)
