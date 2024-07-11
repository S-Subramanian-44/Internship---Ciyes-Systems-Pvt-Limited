## Description

This repository contains code for predicting and forecasting the close price of Amazon (AMZN) stock from 2010 to 2018 and forecasting for the years 2019-2020 using Long Short-Term Memory (LSTM) and Deep VAR (Vector Autoregression) models implemented in PyTorch.

### Project Overview

1. **Data Preparation**:
    - The dataset used is the historical stock prices of Amazon (AMZN) from 2010 to 2018.
    - The data is preprocessed, including normalization using MinMaxScaler.
    - The dataset is split into training (80%) and testing (20%) sets.

2. **Sequence Creation**:
    - Sequential data is created with a sequence length of 3.
    - The sequences are prepared for LSTM input.

3. **Model Architecture**:
    - A Deep VAR model is created using PyTorch, which includes:
        - An LSTM layer.
        - A fully connected (Linear) layer.
    - Hyperparameters include:
        - `input_dim`: 2 (Close and Adj Close prices)
        - `hidden_dim`: 50
        - `output_dim`: 2
        - `num_layers`: 1
        - `num_epochs`: 1
        - `learning_rate`: 0.001

4. **Model Training**:
    - The model is trained using the training dataset with the Adam optimizer and Mean Squared Error (MSE) loss function.
    - Training progress is printed per epoch.

5. **Model Evaluation**:
    - The model is evaluated on the test dataset.
    - Predictions are made and inverse transformed to the original scale.
    - Actual vs. predicted values are compared.

6. **Future Forecasting**:
    - The model is used to forecast future prices for the next 365 days (1 year).
    - Performance metrics like prediction duration, CPU time, and memory usage are recorded.

7. **Results**:
    - Future predictions are inverse transformed and printed along with corresponding dates.

### Requirements

- Python 3.7+
- PyTorch
- Scikit-learn
- Pandas
- Numpy
- Matplotlib
- Psutil

### Future Work

- Experiment with different sequence lengths and model architectures.
- Implement hyperparameter tuning for better performance.
- Extend the forecasting period and validate with more recent data.

### References

- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Pandas Documentation](https://pandas.pydata.org/docs/)

### Let's Connect!
🌐 LinkedIn: https://www.linkedin.com/in/subramanian-s-ab94302a1/ 
📧 Email: subramanian160104@gmail.com
