# Climate Data Analysis and Modeling Project

## Overview

Advanced climate data analysis project for crop yield prediction using machine learning approaches. This project implements multiple modeling techniques with synthetic data generation to improve prediction accuracy.

## Project Structure

```
├── data_generation.ipynb          # Synthetic data generation
├── EDA_and_data_cleaning.ipynb   # Data exploration and preprocessing
├── modelling.ipynb               # ML model implementation
├── data/
    ├── Cropdata.xlsx             # Source dataset
    ├── model_results_summary.csv # Results overview
    ├── approach_1/              # Seasonal analysis
    └── approach_2/              # Full year analysis
```

## Modeling Approaches

### Approach 1: Seasonal Analysis

- Focuses on wheat crop growing season (winter and early summer)
- Analyzes data from November to March (sowing in Nov-Dec-Jan, harvesting in Feb-Mar)
- Uses climate data specifically from these critical months
- Creates features based on seasonal patterns

### Approach 2: Full Year Analysis

* Considers climate data from all months
* Takes into account year-round weather patterns
* Includes all available climate variables
* Provides a comprehensive view of climate impact on crop yield

## Methodology

1. **Data Preprocessing**
   * Missing value handling using KNN and regression imputation
   * Feature scaling and normalization
   * Synthetic data generation for model robustness
2. **Modeling Approaches**
   * Linear Regression
   * Random Forest
   * XGBoost
3. **Evaluation Metrics**
   * Mean Absolute Error (MAE)
   * Root Mean Square Error (RMSE)
   * R² Score
   * Adjusted R² Score

- **Best Model (Approach 1)**: XGBoost (R² = 0.960)
- **Best Model (Approach 2)**: Random Forest (R² = 0.950)

## Results

Best performing models:

* For Approach 1: XGBoost with regression imputation (R² = 0.960)
* For Approach 2: Random Forest with KNN imputation (R² = 0.950)

## Setup

```bash
python -m pip install -r requirements.txt
```

## Usage

1. Run [EDA_and_data_cleaning.ipynb](vscode-file://vscode-app/c:/Users/Ganesh%20Valtule/AppData/Local/Programs/Microsoft%20VS%20Code/resources/app/out/vs/code/electron-browser/workbench/workbench.html) for initial data processing
2. Execute [data_generation.ipynb](vscode-file://vscode-app/c:/Users/Ganesh%20Valtule/AppData/Local/Programs/Microsoft%20VS%20Code/resources/app/out/vs/code/electron-browser/workbench/workbench.html) to generate synthetic data
3. Run [modelling.ipynb](vscode-file://vscode-app/c:/Users/Ganesh%20Valtule/AppData/Local/Programs/Microsoft%20VS%20Code/resources/app/out/vs/code/electron-browser/workbench/workbench.html) to train and evaluate models

## Requirements

- Python 3.10.11
- pandas
- numpy
- scikit-learn
- xgboost
- matplotlib
