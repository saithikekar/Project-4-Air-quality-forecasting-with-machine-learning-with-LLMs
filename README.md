# Project-4-Air-quality-forecasting-with-machine-learning-with-LLMs
This repository contains selection tasks for a Student Research Internship Program at IIT Gandhinagar.

## 1. Data

1. Downloaded the dataset from https://cpcb.nic.in/automatic-monitoring-data/
2. Features (Variables) in the dataset are {PM10, NO, NO2,	WS,	CO,	Benzene, NOx,	Ozone,	SO2,	NH3,	Toluene,	PM2.5). These are all the pollutants taken in consideration.

## 2. Implementation

### Implemented Models
1. **Feedforward Neural Network (FNN-ADAM)**
   - Suitable for regression tasks.
   - Trained using the Adam optimizer.
2. **Long Short-Term Memory (LSTM)**
   - Designed for sequence modeling.
   - Captures temporal dependencies.
3. **Encoder-Decoder LSTM (ED-LSTM)**
   - Consists of an encoder and a decoder.
   - Used for sequence-to-sequence tasks.
4. **Bidirectional LSTM (BD-LSTM)**
   - Processes input sequences bidirectionally.
   - Captures context from both past and future.

https://github.com/saithikekar/Project-4-Air-quality-forecasting-with-machine-learning-with-LLMs/blob/main/data_implementation%20file.ipynb [Implementaion of models]

https://github.com/saithikekar/Project-4-Air-quality-forecasting-with-machine-learning-with-LLMs/blob/main/data_visualization%20file.ipynb [Visualization of results]

LLM Models:
+ **LLama2 Quantized version**
+ **Gemma:7b**


## 3. Visualization

**1. Predicted PM2.5 Concentration at Anand Vihar Station (Dec 17, 2020 - Jan 9, 2021)**
+ graph illustrates the forecasted PM2.5 concentration over a specific time period (from December 17, 2020, to January 9, 2021).
+ The blue line represents the mean PM2.5 concentration.
+ The green shaded area around the line indicates the prediction error range.
+ The graph provides insights into the expected air quality levels at the Anand Vihar station during this period.

![image](https://github.com/saithikekar/Project-4-Air-quality-forecasting-with-machine-learning-with-LLMs/assets/110020678/d0a8af7f-679d-4c3c-a3e3-2401e344fa03)

**2. Correlation Matrix of Air Pollutants**
+ The graph displays a correlation matrix showcasing the relationships between various air pollutants, including PM10, NO, NO2, WS, CO, Benzene, NOx, Ozone, SO2, NH3, Toluene, and PM2.5.
+ Each cell in the matrix represents the correlation coefficient between two pollutants.
+ The color-coded cells indicate the strength and direction of correlations:
+ Red cells represent positive correlations (values closer to 1).
+ Blue cells represent negative correlations (values closer to -1).
+ This matrix provides insights into how different pollutants are related, which is crucial for understanding air quality dynamics.
   
![image](https://github.com/saithikekar/Project-4-Air-quality-forecasting-with-machine-learning-with-LLMs/assets/110020678/4be99a6c-85c2-4a73-a5a1-792ea1f45262)

## 3. Model Comparison for Air Quality Forecasting
+ All models exhibit similar RMSE values during training and testing.
+ FNN-ADAM, LSTM, and BD-LSTM perform consistently.
+ ED-LSTM shows slightly higher RMSE during testing.

![lstm_models_anand](https://github.com/saithikekar/Project-4-Air-quality-forecasting-with-machine-learning-with-LLMs/assets/110020678/e3214f64-f4de-4088-910b-62d6765a46be)

**4. Actual vs. Predicted PM2.5 Concentration**
+ The close alignment between actual and predicted lines suggests that the model performs well.
+ The green “Error” line shows where the model deviates from actual values.
+ Further investigation into error patterns can guide model improvements.
+ Overall, the model provides reliable PM2.5 forecasts for air quality management.

![image](https://github.com/saithikekar/Project-4-Air-quality-forecasting-with-machine-learning-with-LLMs/assets/110020678/fa2c4f33-f394-4105-8064-a964c5b526ad)

**5. Comparative Analysis of Models Based on RMSE**

1. **_FNN-ADAM (Feedforward Neural Network with Adam optimizer):_**
   - Achieves competitive performance across different step sizes.
   - Robust during both training and testing phases.
   - Suitable for univariate time-series forecasting.

2. **_LSTM (Long Short-Term Memory):_**
   - Demonstrates consistent performance.
   - Effective in capturing temporal dependencies.
   - Well-suited for sequence modeling.

3. _**ED-LSTM (Encoder-Decoder LSTM):**_
   - Combines an encoder and a decoder.
   - Performs well but shows slightly higher RMSE during testing.
   - Useful for sequence-to-sequence tasks.

4. _**BD-LSTM (Bidirectional LSTM)**:_
   - Processes input sequences bidirectionally.
   - Similar performance to other models.
   - Captures context from both past and future.

![step_anand](https://github.com/saithikekar/Project-4-Air-quality-forecasting-with-machine-learning-with-LLMs/assets/110020678/6f8eb933-af0e-4e6a-b548-c44870743f07)

## 4. Model Performance and insights 

+ ![diagram lstm](https://github.com/saithikekar/Project-4-Air-quality-forecasting-with-machine-learning-with-LLMs/assets/110020678/80077a92-d9b6-45ae-8227-0ebeae8a2102)

+ for LLM models Quantized versions were implemented and if we consider climate factors we will be able to predict the values with more accuracy for LLM.
+ Other models like TimeLLM, TimeGPT can be implemented with proper system requirements which can give best results for zero shot time series forecasting.
+ The LSTM models were trained for 200 epochs were as the models used in airfomer solution were trained for 2000+epochs and with proper GPUs.
+ The implemented models were trained on colab using T4 GPU with minimum setup.







   




   

