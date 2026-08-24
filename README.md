# Water-Quality-Analysis

**Water Quality Analysis** 

This repository contains a Notebook for analysing and predicting water quality parameters using machine learning and deep learning models.
The dataset used is Data-Melbourne_F.csv, which contains water quality features from Melbourne.

**Features of the Project**

Exploratory Data Analysis (EDA)

- Statistical summaries and correlation heatmaps

- Visualisations using Matplotlib, Seaborn, and Plotly

Data Preprocessing

- Missing value handling (na_values for SLP = 0)

- Feature scaling with MinMaxScaler

Modeling Approaches

- Classical ML Models:

    - Random Forest Regressor

    - Gradient Boosting Regressor

    - XGBoost Regressor

    - Stacking Regressor (with Linear Regression as meta-learner)

- Deep Learning Model:

    - LSTM (Long Short-Term Memory) network with EarlyStopping

- Model Evaluation Metrics

    - Mean Absolute Error (MAE)

    - Root Mean Squared Error (RMSE)

    - R² Score

- Explainability

    - SHAP (SHapley Additive exPlanations) for feature importance analysis

**Results**

The models were trained to predict three water quality parameters:

_BOD (Biochemical Oxygen Demand)_
| Model             | MAE     | RMSE    | R²     |
| ----------------- | ------- | ------- | ------ |
| Random Forest     | 18.2605 | 27.4408 | 0.7433 |
| Gradient Boosting | 12.3761 | 20.4834 | 0.8569 |
| XGBoost           | 12.8035 | 22.2023 | 0.8319 |
| LSTM              | 40.8785 | 51.7586 | 0.0866 |

_COD (Chemical Oxygen Demand)_
| Model             | MAE     | RMSE     | R²     |
| ----------------- | ------- | -------- | ------ |
| Random Forest     | 32.3218 | 43.7321  | 0.8788 |
| Gradient Boosting | 19.2686 | 27.1821  | 0.9532 |
| XGBoost           | 20.4485 | 29.1119  | 0.9463 |
| LSTM              | 90.8709 | 116.3888 | 0.1417 |

_TN (Total Nitrogen)_
| Model             | MAE    | RMSE   | R²     |
| ----------------- | ------ | ------ | ------ |
| Random Forest     | 0.6060 | 1.0297 | 0.8452 |
| Gradient Boosting | 0.4440 | 0.6369 | 0.9408 |
| XGBoost           | 0.4431 | 0.6392 | 0.9403 |
| LSTM              | 1.7762 | 2.5765 | 0.0306 |


**Best performing models:**

- Gradient Boosting for BOD and COD

- Gradient Boosting / XGBoost for TN

- LSTM underperformed compared to tree-based models.

**Future Improvements**

- Improve deep learning performance with more tuning and feature engineering.

- Try hybrid models combining LSTM with tree-based learners.

- Deploy the best model as a web app or API for real-time predictions.

**Author**

Yoshita Banerjee
