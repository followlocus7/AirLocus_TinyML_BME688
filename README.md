# AirLocus TinyML Gas Sensor

## Project Overview
This project predicts concentrations of gases (CO, CO2, SO2, NO2, CH4) from BME688 sensor readings using TinyML. The sensor provides raw environmental data (temperature, humidity, pressure, gas resistance), and a trained neural network estimates actual gas concentrations.

## Project Structure
├── Predict_gas_concentration.ipynb # Notebook for testing and inference
├── train.csv # Dataset used for training
├── models/ # Folder containing trained models & scaler
│ ├── gas_model.h5 # Keras model
│ ├── gas_model.keras # Keras native format model
│ ├── gas_model_int8.tflite # Quantized TFLite model
│ ├── gas_model_int8.cc # C array for MCU deployment
│ └── scaler_params.npz # Input scaler parameters
└── README.md # Project description
## Usage
1. Load `Predict_gas_concentration.ipynb` to run inference using sample inputs.
2. The TFLite model (`gas_model_int8.tflite`) can be deployed on MCU (ESP32-C3) via the generated C array (`gas_model_int8.cc`).
3. Use the scaler parameters (`scaler_params.npz`) to normalize sensor inputs before prediction.

## Team
**Team Name:** AirLocus  
**GitHub:** [https://github.com/followlocus7/AirLocus_TinyML_BME688](https://github.com/followlocus7/AirLocus_TinyML_BME688)

## Notes
- The BME688 sensor provides indirect gas readings; the model converts them to actual gas concentration estimates.
- TinyML model is fully quantized for efficient MCU deployment.
=======
\# AirLocus TinyML Gas Sensor



\## Project Overview

This project predicts concentrations of gases (CO, CO2, SO2, NO2, CH4) from BME688 sensor readings using TinyML. The sensor provides raw environmental data (temperature, humidity, pressure, gas resistance), and a trained neural network estimates actual gas concentrations.



\## Project Structure

Predict\_gas\_concentration.ipynb # Notebook for testing and inference

train.csv # Dataset used for training

models/ # Folder containing trained models \& scaler

gas\_model.h5 # Keras model

gas\_model.keras # Keras native format model

gas\_model\_int8.tflite # Quantized TFLite model

gas\_model\_int8.cc # C array for MCU deployment

scaler\_params.npz # Input scaler parameters

README.md # Project description



\## Usage

1\. Load `Predict\_gas\_concentration.ipynb` to run inference using sample inputs.

2\. The TFLite model (`gas\_model\_int8.tflite`) can be deployed on MCU (ESP32-C3) via the generated C array (`gas\_model\_int8.cc`).

3\. Use the scaler parameters (`scaler\_params.npz`) to normalize sensor inputs before prediction.



\## Team

\*\*Team Name:\*\* AirLocus  

\*\*GitHub:\*\* \[https://github.com/followlocus7/AirLocus\_TinyML\_BME688](https://github.com/followlocus7/AirLocus\_TinyML\_BME688)



\## Notes

\- The BME688 sensor provides indirect gas readings; the model converts them to actual gas concentration estimates.

\- TinyML model is fully quantized for efficient MCU deployment.
