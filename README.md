## Project Overview

This project, developed as part of the Afretec Summer School on Smart Systems, focuses on predicting the number of confirmed COVID-19 cases using deep learning techniques. The project leverages an LSTM (Long Short-Term Memory) neural network to model and forecast the progression of the pandemic over time based on historical data.

### Team Members:
1. Ahmed Mostafa
2. Youssef Abdel Mottaleb
3. Reem Wael
4. Maram Ahmed

### Supervised By:
Dr. Mariam N. Aboelwafa

## Dataset Description

The dataset used in this project consists of global COVID-19 case data, including daily confirmed cases, deaths, and recoveries. The original dataset includes data fields such as the observation date, country/region, and cumulative case counts. Preprocessing steps included:

- Dropping unnecessary columns like 'SNo', 'Province/State', and 'Last Update'.
- Aggregating the data by 'ObservationDate' to get the total confirmed cases per day.
- Converting dates to timestamps and normalizing them for model input.

## Project Structure

The project is organized as follows:

1. **Data Preprocessing:** The dataset is cleaned and preprocessed to make it suitable for time series prediction. This includes handling missing values, data aggregation, and normalization.

2. **Dataset Class:** A custom `CovidDataset` class is defined to handle the input data for the LSTM model. The class returns date and confirmed cases as input-output pairs for model training.

3. **Model Definition:** The LSTM model is designed with layers to capture the temporal dependencies in the time series data. The model includes:
   - An LSTM layer to process the sequential data.
   - A fully connected layer to produce the final prediction.

4. **Training and Evaluation:** 
   - The model is trained using the MSE (Mean Squared Error) loss function and Adam optimizer.
   - The training is performed over multiple epochs, and the model's performance is evaluated on a validation set to ensure its generalization capability.

5. **Error Handling:** The project includes steps to handle potential errors related to data sequencing and preprocessing, ensuring robust model performance.

## How to Run

1. **Dependencies:** Ensure you have the necessary Python libraries installed:
   ```bash
   pip install pandas numpy matplotlib seaborn torch scikit-learn
   ```

2. **Data:** Place the `covid_19_data.csv` file in the root directory of the project.

3. **Execution:** Run the provided notebook or script to execute the data preprocessing, model training, and evaluation steps.

4. **Results:** After training, the model's performance can be evaluated using the validation data. The notebook includes visualization tools to plot predictions versus actual confirmed cases.

## Conclusion

This project demonstrates the application of deep learning in predicting COVID-19 case trends. The use of LSTM models highlights the importance of capturing temporal dependencies in time series data. This approach can be extended to various time series forecasting problems beyond the scope of this project.
