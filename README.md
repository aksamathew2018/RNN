

# 🌡️ Temperature Forecasting using SimpleRNN

## 📌 Project Overview

This project focuses on forecasting next-day temperature using historical weather data and a Simple Recurrent Neural Network (SimpleRNN). The model learns temporal patterns from past weather observations to predict future temperature trends.

---

## 📂 Dataset Features Used

The following features were used as input:

* Temperature (C)
* Humidity
* Wind Speed (km/h)

Target:

* Next day Temperature (C)

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing

* Sorted dataset by date.
* Selected relevant weather features.
* Applied feature scaling using `StandardScaler`.
* Created sliding window sequences using past 14 days of data.
* Target defined as next-day temperature.

### 2️⃣ Train–Validation–Test Split

* 70% Training
* 15% Validation
* 15% Testing
* No shuffling (to preserve time-series structure)

---

## 🧠 Model Architecture

* Input Layer: (14 days × 3 features)
* SimpleRNN Layer: 64 units (tanh activation)
* Dropout Layer: 0.2 (to reduce overfitting)
* Dense Output Layer: 1 neuron (linear activation)

Loss Function: Mean Squared Error (MSE)
Optimizer: Adam
Metric: Mean Absolute Error (MAE)

---

## 📊 Model Performance

* Training and validation loss decreased steadily.
* Validation loss closely followed training loss.
* Model successfully captured seasonal temperature patterns.
* Predictions closely aligned with actual test values.

Evaluation Metrics (Test Set):

* RMSE
* MAE
* R² Score

---

## 📈 Results

* The model effectively captured long-term seasonal trends.
* Predictions were slightly smoother than actual values, which is common in RNN models.
* No significant overfitting observed.

---

## 🔮 Forecasting

The trained model was used to forecast the next 7 days of temperature using recursive prediction. The forecast followed recent historical patterns, demonstrating the model’s ability to generalize future trends.

---




## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* TensorFlow / Keras

---

