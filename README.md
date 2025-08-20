# 🌍 Air Quality Forecasting with LSTM  

This project uses a **Deep Learning model (LSTM)** to predict **Ambient Temperature (AT)** from **air quality and meteorological data**.  
The dataset contains pollutant concentrations, weather features, and temporal information, making it suitable for **time series forecasting**.  

---

## 📊 Dataset Features  

- **from_date**: Start time of air quality recording (datetime)  
- **to_date**: End time of air quality recording (datetime, usually +1h from from_date)  
- **pm2_5**: Fine particulate matter (≤2.5 μm), harmful to respiratory health  
- **pm10**: Coarse particulate matter (≤10 μm), from dust/road/construction  
- **no**: Nitric oxide (NO), vehicle exhaust gas  
- **no2**: Nitrogen dioxide (NO₂), toxic air pollutant  
- **nox**: Nitrogen oxides (NO + NO₂), traffic emission indicator  
- **nh3**: Ammonia (NH₃), biological & industrial source  
- **so2**: Sulfur dioxide (SO₂), fossil fuel combustion  
- **co**: Carbon monoxide (CO), toxic gas from incomplete combustion  
- **ozone**: Ground-level ozone (O₃), harmful pollutant  
- **benzene**: Volatile organic compound (VOC), toxic, common in cities  
- **toluene**: VOC from solvents & industry, affects nervous system  
- **eth_benzene**: Ethylbenzene, VOC from fuels & solvents  
- **mp_xylene**: Meta-para-xylene, VOC from fuels  
- **xylene**: Total xylene (ortho + isomers), VOC from traffic emissions  
- **temperature**: Air temperature (duplicate of ambient_temp, ignored)  
- **humidity**: Relative humidity (%)  
- **wind_speed**: Wind speed (m/s)  
- **wind_direction**: Wind direction (°)  
- **solar_radiation**: Solar radiation (W/m²), impacts ozone formation  
- **pressure**: Atmospheric pressure (mmHg)  
- **vertical_wind_speed**: Vertical air movement, affects pollutant circulation  
- **ambient_temp**: Target variable – actual ambient air temperature (°C)  
- **rainfall**: Rainfall (mm), cleans pollutants from air  

---

## 🧠 Model Architecture  

The model is a **Deep Learning LSTM-based Regressor** with:  
- **LSTM layers** to capture time series dependencies  
- **Batch Normalization** for stable training  
- **Dropout** for regularization  
- **Dense output layer** with linear activation  

Loss: **MSE**  
Optimizer: **Adam** with learning rate scheduling  
Callbacks: **EarlyStopping** & **LR Scheduler**  

---

## 🛠️ Tech Stack  

- **Python 3.10**  
- **TensorFlow / Keras**  
- **Scikit-learn** (scaling, splitting, metrics)  
- **NumPy, Pandas** (data preprocessing)  
- **Matplotlib, Seaborn** (visualization)  

---

## 📂 Project Structure

📁 air-quality-lstm
│── data/                 # Dataset files
│── train_lstm.py         # Model training script
│── evaluate.py           # Evaluation & visualization
│── model_lstm.h5         # Saved LSTM model
│── requirements.txt      # Dependencies
│── README.md             # Project documentation

---

