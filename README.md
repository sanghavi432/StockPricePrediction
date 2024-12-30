
# Stock Price Prediction 

## Project Overview

This project involves predicting stock prices for major companies (Tesla, Apple, Google, Microsoft, Amazon) using historical stock data. The models used include:

- **LSTM (Long Short-Term Memory)**: For sequential data prediction.
- **SVM (Support Vector Machine)** and **Random Forest**: As baseline comparison models.

The goal is to evaluate and compare the performance of these models in predicting the adjusted closing price (`Adj Close`) of the stocks.

---

## Prerequisites

Ensure the following dependencies are installed:

- Python 3.8 or higher
- Required Libraries:
  ```bash
  pip install pandas numpy scikit-learn keras matplotlib
  ```

---

## Dataset

### Description
- The dataset includes historical stock data for Tesla, Apple, Google, Microsoft, and Amazon. Each file should have the following columns:
  - `Date`, `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`.
  
- **Note:** Files must be named as `<COMPANY_NAME>_data.csv` (e.g., `TESLA_data.csv`).

---

## Workflow

### 1. **Feature Engineering**
   - Add a `Volatility` column to capture daily price range.
   - Handle missing values using backward fill.

### 2. **Data Preparation**
   - Normalize numerical features using MinMaxScaler.
   - Create input-output sequences for LSTM with a defined sequence length.

### 3. **Sequential Data Split**
   - Use an 80-20 split for training and testing.

### 4. **Model Training and Evaluation**
   - **LSTM**:
     - Two LSTM layers with `Dense` output layers for prediction.
     - Metrics: RMSE, MAE, R-Squared.
   - **SVM** and **Random Forest**:
     - Flatten sequential data for non-sequential models.

### 5. **Results**
   - Compared models using evaluation metrics.
   - Visualized LSTM predictions against actual stock prices.

### 6. **Combined Dataset**
   - Merge all company datasets for a unified prediction model.

---

## File Structure

- **Dataset Files:**  
  Ensure individual `.csv` files for each company exist in the same directory as the script.
  
- **Python Script:** `final_version.ipynb`  
  Contains the complete implementation.

---

## How to Run

1. Place all dataset files (e.g., `TESLA_data.csv`, `APPLE_data.csv`) in the project directory.
2. Execute the script in jupyter notebook



---

## Results

### Evaluation Metrics:
- **Root Mean Square Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **R-Squared**

Results are stored in a structured format and displayed for each company and the combined dataset.

