
# California Housing Price Prediction
### Predictive Modeling Using Socioeconomic and Spatial Data

**Author:** Criselvi Lindsey  
**Course:** DSC 630 – Predictive Analytics  
**Institution:** Bellevue University  
**Completed:** March 2026

## Project Overview

This project explores the use of predictive analytics and machine learning to estimate median housing values in California based on socioeconomic, housing, and geographic characteristics.

Using the California Housing dataset, I conducted exploratory data analysis, prepared and transformed the data, and developed regression models to evaluate how well different variables predict housing values.

The project compares Linear Regression, Ridge Regression, and Lasso Regression, evaluates their predictive performance, and examines the factors influencing housing prices.

## Business Problem and Objectives

Housing prices are influenced by multiple factors, including household income, housing characteristics, population, and geographic location.

The objective of this project was to:

- Examine relationships between socioeconomic and spatial variables and housing values.
- Identify important predictors of median housing prices.
- Prepare and transform the data for predictive modeling.
- Develop and compare multiple regression models.
- Evaluate prediction accuracy and model limitations.
- Interpret the results to better understand housing value patterns.

## Dataset

**Dataset:** California Housing Dataset  
**Source:** Scikit-learn, based on 1990 California census data  
**Observations:** 20,640  
**Predictor Variables:** 8  
**Target Variable:** `MedHouseVal`

The target represents median house value in units of $100,000.

### Dataset Features

| Variable | Description |
|---|---|
| MedInc | Median household income |
| HouseAge | Median age of housing units |
| AveRooms | Average rooms per household |
| AveBedrms | Average bedrooms per household |
| Population | Population of the census block group |
| AveOccup | Average household occupancy |
| Latitude | Geographic latitude |
| Longitude | Geographic longitude |
| MedHouseVal | Median house value (target) |

The dataset is retrieved directly using Python:

```python
from sklearn.datasets import fetch_california_housing

housing = fetch_california_housing(as_frame=True)
df = housing.frame
```

A separate CSV file is not required.

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas and NumPy
- Scikit-learn
- Matplotlib and Seaborn
- Exploratory Data Analysis (EDA)
- Predictive Modeling
- Regression Analysis
- Model Evaluation

## Project Methodology

### 1. Exploratory Data Analysis

Explored the distribution of median housing values and examined relationships among income, housing characteristics, population, and location.

The analysis included:

- Housing value distribution
- Correlation analysis
- Median income versus housing value
- Geographic housing patterns
- Identification of outliers and skewed variables

### 2. Data Preparation

Prepared the dataset for modeling through several preprocessing techniques:

- Capped extreme values in Population and AveOccup at the 99th percentile.
- Applied logarithmic transformations to selected skewed variables.
- Standardized model features using z-score scaling.
- Divided the dataset into training and testing subsets.

The modeling dataset included 16,512 training observations and 4,128 testing observations.

### 3. Predictive Modeling

Developed and evaluated three regression models:

**Linear Regression**

Established a baseline model for predicting median housing values.

**Ridge Regression**

Applied L2 regularization to address correlated predictors and evaluate model stability.

**Lasso Regression**

Applied L1 regularization to evaluate coefficient shrinkage and predictive performance.

### 4. Model Evaluation

Evaluated model performance using:

- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Coefficient of Determination (R²)
- Predicted versus actual values
- Residual analysis

## Model Performance

| Model | RMSE | MAE | R² |
|---|---:|---:|---:|
| Linear Regression | 0.674 | 0.492 | 0.653 |
| Ridge Regression | 0.674 | 0.492 | 0.653 |
| Lasso Regression | 0.676 | 0.493 | 0.652 |

*RMSE and MAE are expressed in the dataset's target units of $100,000.*

### Interpretation

The baseline Linear Regression model explained approximately 65.3% of the variation in median housing values on the test dataset.

Ridge and Lasso Regression produced similar results, without meaningful improvements in predictive accuracy.

Regularization provided an alternative approach for managing correlated predictors and controlling coefficient magnitude.

## Key Findings

**1. Median income is a major predictor.**

Median household income demonstrated a strong positive relationship with median housing values.

**2. Geographic location influences housing values.**

Spatial analysis revealed higher housing values concentrated in certain coastal and urban areas.

**3. Housing and population characteristics contribute to predictions.**

Transformed housing and population variables provided additional predictive information.

**4. Regularization did not significantly improve model accuracy.**

Ridge and Lasso performed similarly to the baseline Linear Regression model.

**5. The dataset has important limitations.**

The dataset is based on historical census information, and median housing values are capped at approximately $500,000.

Consequently, the models should not be interpreted as estimates of current California real estate prices.

## Visualizations

The Jupyter Notebook includes visualizations covering:

- Distribution of median housing values
- Income and housing value relationships
- Correlation heatmap
- Geographic housing value patterns
- Variable transformations
- Predicted versus actual housing values
- Regression coefficient importance
- Residual analysis

These visualizations support interpretation of the modeling results and identification of limitations.

## Project Deliverables

### Python Analysis

[View Jupyter Notebook](CriselviLindsey_DSC630T302_Project_Milestone5_Final.ipynb)

Contains the Python analysis, data preparation, regression modeling, evaluation metrics, and visualizations.

### Final Written Report

[View Final Project Report](Criselvi%20Lindsey%20DSC630%20Milestone%205%20Final.docx)

Documents the research objectives, dataset, methodology, model performance, findings, and conclusions.

### Narrated Project Presentation

**[▶ Watch the California Housing Price Prediction Presentation](https://drive.google.com/file/d/1zkuXdqsmmPnoyj5DzHPsQQJoLAfPZzHY/view?usp=drive_link)**

The narrated presentation summarizes the analytical approach, visualizations, regression results, and key conclusions.

*Video hosted on Google Drive.*

## How to Run the Project

1. Download or clone this repository.
2. Install Python and Jupyter Notebook.
3. Install the required Python packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

4. Open `CriselviLindsey_DSC630T302_Project_Milestone5_Final.ipynb`.
5. Run the notebook cells in sequence.

The notebook retrieves the California Housing dataset through scikit-learn. An internet connection may be needed when the dataset is first downloaded.

## Project Limitations

- Housing information is based on the 1990 census.
- The target variable is capped at approximately $500,000.
- Linear models may not capture all nonlinear housing market relationships.
- Historical data limits applicability to current housing prices.
- Results describe predictive relationships rather than causal effects.

## Conclusion

This project demonstrates the application of predictive analytics to a real-world housing valuation problem.

By combining exploratory data analysis, data preprocessing, regression modeling, and model evaluation, the study identified important relationships between housing values and socioeconomic and geographic characteristics.

The findings illustrate the value of systematic data preparation, model comparison, and careful interpretation when applying machine learning to business and economic questions.

---

**Criselvi Lindsey**  
MBA, Business Analytics  
Data Analytics | Business Intelligence | Predictive Modeling

[GitHub Profile](https://github.com/crisevilindsey)
