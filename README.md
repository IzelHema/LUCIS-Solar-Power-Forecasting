

\# LUCIS — Solar PV Power Forecasting



\### An Intelligent Day-Ahead Solar Power Forecasting System Using Machine Learning and Deep Learning



LUCIS is a data-driven solar photovoltaic (PV) power forecasting project that predicts the next 24 hours of solar electricity generation using historical power data.



The project implements and compares six machine learning and deep learning models to evaluate their forecasting performance on real-world solar power generation data.



\## Project Objectives



\- Predict solar power generation for the next 24 hours.

\- Analyze historical solar power generation patterns.

\- Implement and compare six forecasting models.

\- Evaluate prediction accuracy using MAE, RMSE, and R².

\- Visualize actual versus predicted solar power generation.



\## Dataset



The project uses historical power generation data from a 5 MW solar PV plant located in Telangana, India.



| Property | Details |

|---|---|

| Location | Telangana, India |

| Plant Capacity | 5 MW |

| Data Period | March 2019 – August 2026 |

| Original Resolution | 15 minutes |

| Processed Resolution | Hourly |

| Total Hourly Records | 65,736 |

| Forecast Input | Previous 168 hours |

| Forecast Output | Next 24 hours |



The dataset was cleaned, converted to hourly resolution, and divided chronologically into training, validation, and testing sets.



\## Models Implemented



1\. Random Forest

2\. Original LSTM

3\. Enhanced LSTM

4\. CNN-LSTM

5\. Attention LSTM

6\. N-HiTS



\## Model Performance



The models were evaluated on 243 daily forecasts from the 2026 test period.



| Model | MAE (MW) | RMSE (MW) | R² |

|---|---:|---:|---:|

| Random Forest | 0.1974 | 0.4107 | 0.9096 |

| Original LSTM | 0.2203 | 0.4309 | 0.9005 |

| N-HiTS | 0.2118 | 0.4427 | 0.8950 |

| CNN-LSTM | 0.2452 | 0.4482 | 0.8924 |

| Attention LSTM | 0.2762 | 0.4758 | 0.8787 |

| Enhanced LSTM | 0.2753 | 0.5089 | 0.8612 |



\*\*Key Findings:\*\*



\- Random Forest achieved the best overall performance.

\- Original LSTM achieved the best RMSE and R² among the deep learning models.

\- N-HiTS achieved the lowest MAE among the deep learning models.

\- Original LSTM was selected for the next-day forecasting demonstration.



\## Forecasting Approach



The Original LSTM model uses:



\- Input: 168 hours (7 days) of historical solar power generation.

\- Output: 24 hours of predicted solar power generation.



The forecasting demonstration predicts solar power generation for September 1, 2026, using historical data through August 31, 2026.



\## Results and Visualizations



\### Model Comparison — R²



!\[Model Comparison](outputs/final\_six\_r2.png)



\### Actual vs Predicted Solar Power



!\[Actual vs Predicted](outputs/final\_actual\_vs\_predicted.png)



\### Next-Day Solar Power Forecast



!\[LSTM Forecast](outputs/lstm\_next\_day\_forecast.png)



\## Technologies Used



\- Python

\- Pandas and NumPy

\- Scikit-learn

\- TensorFlow / Keras

\- PyTorch

\- NeuralForecast

\- Matplotlib



\## Installation



Clone the repository:



```bash

git clone https://github.com/YOUR\_USERNAME/LUCIS-Solar-Power-Forecasting.git

cd LUCIS-Solar-Power-Forecasting

```



Install dependencies:



```bash

pip install -r requirements.txt

```



Note: The original dataset and some large trained models are not included in the public repository. These are required for certain training and forecasting scripts.



\## Limitations



\- The primary forecasting models rely on historical solar power generation.

\- Weather data integration is preliminary.

\- N-HiTS was trained using a shorter historical period than some other models.

\- Small positive nighttime predictions may occur.

\- Model comparisons describe the implemented pipelines rather than a fully controlled architecture-only benchmark.



\## Future Enhancements



\- Integrate weather variables such as temperature, irradiance, and wind speed.

\- Develop an interactive real-time forecasting dashboard.

\- Improve nighttime prediction constraints.

\- Deploy the forecasting pipeline as a web application.



\## Contributors



Developed as a collaborative college project.



\## License and Data Availability



The original solar generation dataset is not redistributed in this repository pending confirmation of sharing permissions.



